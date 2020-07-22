---
title: Получение оценок энергетических уровней
description: 'Рассмотрим пример программы Q #, которая оценивает значения уровня энергии молекулярное водорода.'
author: guanghaolow
ms.author: gulow
ms.date: 07/02/2020
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.examples.energyestimate
ms.openlocfilehash: b26538980366cf4cbe01fc2ef59580ae182f1e8a
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/21/2020
ms.locfileid: "86871574"
---
# <a name="obtaining-energy-level-estimates"></a>Получение оценок энергетических уровней
Оценка значений уровня энергии является одним из основных приложений тактовой химия. В этой статье описано, как это сделать для канонического примера водомолекулярное. Образец, указанный в этом разделе, находится [`MolecularHydrogen`](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/MolecularHydrogen) в репозитории примеров химия. Более наглядным примером, который отображает выходные данные, является [`MolecularHydrogenGUI`](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/MolecularHydrogenGUI) демонстрация.

## <a name="estimating-the-energy-values-of-molecular-hydrogen"></a>Оценка значений энергии для молекулярное водорода

Первым шагом является создание Хамилтониан, представляющего молекулярное водорода. Хотя это можно создать с помощью средства Нвчем, для краткости в этом примере термины Хамилтониан добавляются вручную.

```csharp
    // These orbital integrals are represented using the OrbitalIntegral
    // data structure.
    var energyOffset = 0.713776188; // This is the coulomb repulsion
    var nElectrons = 2; // Molecular hydrogen has two electrons
    var orbitalIntegrals = new OrbitalIntegral[]
    {
        new OrbitalIntegral(new[] { 0,0 }, -1.252477495),
        new OrbitalIntegral(new[] { 1,1 }, -0.475934275),
        new OrbitalIntegral(new[] { 0,0,0,0 }, 0.674493166),
        new OrbitalIntegral(new[] { 0,1,0,1 }, 0.181287518),
        new OrbitalIntegral(new[] { 0,1,1,0 }, 0.663472101),
        new OrbitalIntegral(new[] { 1,1,1,1 }, 0.697398010),
        // This line adds the identity term.
        new OrbitalIntegral(new int[] { }, energyOffset)
    };

    // Initialize a fermion Hamiltonian data structure and add terms to it.
    var fermionHamiltonian = new OrbitalIntegralHamiltonian(orbitalIntegrals).ToFermionHamiltonian();
```

Для имитации Хамилтониан необходимо преобразовать операторы фермион в операторы кубит. Это преобразование выполняется с помощью Вигнер кодирования следующим образом:

```csharp
    // The Jordan-Wigner encoding converts the fermion Hamiltonian, 
    // expressed in terms of fermionic operators, to a qubit Hamiltonian,
    // expressed in terms of Pauli matrices. This is an essential step
    // for simulating our constructed Hamiltonians on a qubit quantum
    // computer.
    var jordanWignerEncoding = fermionHamiltonian.ToPauliHamiltonian(Pauli.QubitEncoding.JordanWigner);

    // You also need to create an input quantum state to this Hamiltonian.
    // Use the Hartree-Fock state.
    var fermionWavefunction = fermionHamiltonian.CreateHartreeFockState(nElectrons);

    // This Jordan-Wigner data structure also contains a representation 
    // of the Hamiltonian and wavefunction made for consumption by the Q# operations.
    var qSharpHamiltonianData = jordanWignerEncoding.ToQSharpFormat();
    var qSharpWavefunctionData = fermionWavefunction.ToQSharpFormat();
    var qSharpData = QSharpFormat.Convert.ToQSharpFormat(qSharpHamiltonianData, qSharpWavefunctionData);
```

Затем Pass `qSharpData` , который представляет хамилтониан, для `TrotterStepOracle` функции. `TrotterStepOracle`Возвращает операцию такта, которая приблизительно соответствует эволюции Хамилтониан в реальном времени. Дополнительные сведения см. в разделе [имитация хамилтониан Dynamics](xref:microsoft.quantum.chemistry.concepts.simulationalgorithms).

```qsharp
// qSharpData passed from driver
let qSharpData = ... 

// Choose the integrator step size
let stepSize = 1.0;

// Choose the order of the Trotter—Suzuki integrator.
let integratorOrder = 4;

// `oracle` is an operation that applies a single time-step of evolution for duration `stepSize`.
// `rescale` is just `1.0/stepSize` -- the number of steps required to simulate unit-time evolution.
// `nQubits` is the number of qubits that must be allocated to run the `oracle` operation.
let (nQubits, (rescale, oracle)) =  TrotterStepOracle (qSharpData, stepSize, integratorOrder);
```

На этом этапе можно использовать [алгоритмы оценки этапа](xref:microsoft.quantum.libraries.characterization) стандартной библиотеки для изучения энергии в состоянии заземления с помощью предыдущего моделирования. Для этого необходимо подготовить хорошее приближение к состоянию земли в такте. В схеме представлены предложения по подобным приближениям [`Broombridge`](xref:microsoft.quantum.libraries.chemistry.schema.broombridge) . Однако в отсутствие этих предложений подход по умолчанию добавляет ряд `hamiltonian.NElectrons` электронов в гридили, чтобы сократить силы по диагонали на один электрон. Функции и операции оценки этапа предоставляются в нотации DocFX в пространстве имен [Microsoft. тактов. character](xref:microsoft.quantum.characterization) .

В следующем фрагменте кода показано, как в режиме реального времени результаты развития библиотеки моделирования химия интегрируются с оценкой фазы такта.

```qsharp
operation GetEnergyByTrotterization (
    qSharpData : JordanWignerEncodingData, 
    nBitsPrecision : Int, 
    trotterStepSize : Double, 
    trotterOrder : Int) : (Double, Double) {
    
    // The data describing the Hamiltonian for all these steps is contained in
    // `qSharpData`
    let (nSpinOrbitals, fermionTermData, statePrepData, energyOffset) = qSharpData!;
    
    // Using a Product formula, also known as `Trotterization`, to
    // simulate the Hamiltonian.
    let (nQubits, (rescaleFactor, oracle)) = 
        TrotterStepOracle(qSharpData, trotterStepSize, trotterOrder);
    
    // The operation that creates the trial state is defined here.
    // By default, greedy filling of spin-orbitals is used.
    let statePrep = PrepareTrialState(statePrepData, _);
    
    // Using the Robust Phase Estimation algorithm
    // of Kimmel, Low and Yoder.
    let phaseEstAlgorithm = RobustPhaseEstimation(nBitsPrecision, _, _);
    
    // This runs the quantum algorithm and returns a phase estimate.
    let estPhase = EstimateEnergy(nQubits, statePrep, oracle, phaseEstAlgorithm);
    
    // Now, obtain the energy estimate by rescaling the phase estimate
    // with the trotterStepSize. We also add the constant energy offset
    // to the estimated energy.
    let estEnergy = estPhase * rescaleFactor + energyOffset;
    
    // Return both the estimated phase and the estimated energy.
    return (estPhase, estEnergy);
}
```

Теперь можно вызвать код Q # из основной программы. В следующем коде C# создается симулятор с полным состоянием и выполняется `GetEnergyByTrotterization` для получения энергии в состоянии заземления.

```csharp
using (var qsim = new QuantumSimulator())
{
    // Specify the bits of precision desired in the phase estimation 
    // algorithm
    var bits = 7;

    // Specify the step size of the simulated time evolution. The step size needs to
    // be small enough to avoid aliasing of phases, and also to control the
    // error of simulation.
    var trotterStep = 0.4;

    // Choose the Trotter integrator order
    Int64 trotterOrder = 1;

    // As the quantum algorithm is probabilistic, run a few trials.

    // This may be compared to true value of
    Console.WriteLine("Exact molecular hydrogen ground state energy: -1.137260278.\n");
    Console.WriteLine("----- Performing quantum energy estimation by Trotter simulation algorithm");
    for (int i = 0; i < 5; i++)
    {
        // EstimateEnergyByTrotterization
        var (phaseEst, energyEst) = GetEnergyByTrotterization.Run(qsim, qSharpData, bits, trotterStep, trotterOrder).Result;
    }
}
```

Операция возвращает два параметра: 

- `energyEst`является оценкой энергии в состоянии "Земля" и должно быть близко к `-1.137` среднему значению. 
- `phaseEst`— Это необработанный этап, возвращенный алгоритмом оценки этапа. Это полезно для диагностики псевдонимов, когда это происходит из-за `trotterStep` слишком большого значения.
