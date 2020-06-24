---
title: Получение оценок энергетических уровней
description: 'Рассмотрим пример программы Q #, которая оценивает значения уровня энергии молекулярное водорода.'
author: guanghaolow
ms.author: gulow
ms.date: 10/23/2018
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.examples.energyestimate
ms.openlocfilehash: 3242d8c6dc6fad2bd99055027dd7ce4ec3510ff4
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2020
ms.locfileid: "85276056"
---
# <a name="obtaining-energy-level-estimates"></a>Получение оценок энергетических уровней
Оценка значений уровня энергии является одним из основных приложений тактовой химия. Здесь показано, как это можно сделать для канонического примера молекулярное водорода. Образец, указанный в этом разделе, находится `MolecularHydrogen` в репозитории примеров химия. Более наглядным примером, который отображает выходные данные, является `MolecularHydrogenGUI` демонстрация.

Первым шагом является создание Хамилтониан, представляющего молекулярное водорода. Хотя это можно сделать с помощью средства Нвчем, мы вручную добавили термины Хамилтониан для краткости в этом примере.

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

    // We initialize a fermion Hamiltonian data structure and add terms to it.
    var fermionHamiltonian = new OrbitalIntegralHamiltonian(orbitalIntegrals).ToFermionHamiltonian();
```

Для имитации Хамилтониан необходимо преобразовать операторы фермион в операторы кубит. Это преобразование выполняется с помощью Вигнер кодирования следующим образом.

```csharp
    // The Jordan-Wigner encoding converts the fermion Hamiltonian, 
    // expressed in terms of fermionic operators, to a qubit Hamiltonian,
    // expressed in terms of Pauli matrices. This is an essential step
    // for simulating our constructed Hamiltonians on a qubit quantum
    // computer.
    var jordanWignerEncoding = fermionHamiltonian.ToPauliHamiltonian(Pauli.QubitEncoding.JordanWigner);

    // We also need to create an input quantum state to this Hamiltonian.
    // Let us use the Hartree-Fock state.
    var fermionWavefunction = fermionHamiltonian.CreateHartreeFockState(nElectrons);

    // This Jordan-Wigner data structure also contains a representation 
    // of the Hamiltonian and wavefunction made for consumption by the Q# operations.
    var qSharpHamiltonianData = jordanWignerEncoding.ToQSharpFormat();
    var qSharpWavefunctionData = fermionWavefunction.ToQSharpFormat();
    var qSharpData = QSharpFormat.Convert.ToQSharpFormat(qSharpHamiltonianData, qSharpWavefunctionData);
```

Теперь мы передаем `qSharpData` хамилтониан, представляющий функцию, `TrotterStepOracle` в [имитацию хамилтониан Dynamics](xref:microsoft.quantum.libraries.standard.algorithms). `TrotterStepOracle`Возвращает операцию с тактом, которая приблизительно является развитием Хамилтониан в реальном времени.

```qsharp
// qSharpData passed from driver
let qSharpData = ... 

// Choose the integrator step size
let stepSize = 1.0;

// Choose the order of the Trotter—Suzuki integrator.
let integratorOrder = 4;

// `oracle` is an operation that applies a single time-step of evolution for duration `stepSize`.
// `rescale` is just `1.0/stepSize` -- the number of steps required to simulate unit-time evolution.
// `nQubits` is the number of qubits that must be allocated to run the `oracle` operatrion.
let (nQubits, (rescale, oracle)) =  TrotterStepOracle (qSharpData, stepSize, integratorOrder);
```

Теперь мы можем использовать алгоритмы оценки этапа стандартной библиотеки для изучения энергии в состоянии заземления с помощью описанной выше модели. Для этого необходимо подготовить хорошее приближение к состоянию земли в такте. В схеме предусмотрены предложения для таких приближений `Broombridge` , но отсутствуют эти предложения. подход по умолчанию добавляет ряд `hamiltonian.NElectrons` электронов в гридили, чтобы сократить силы по диагонали на один электрон. Функции и операции оценки этапа находятся в [пространстве имен Microsoft. такт. character](xref:microsoft.quantum.characterization in DocFX notation).

В следующем фрагменте кода показано, как в реальном времени с помощью библиотеки моделирования химия можно интегрировать результаты оценки тактовой фазы.

```qsharp
operation GetEnergyByTrotterization (
    qSharpData : JordanWignerEncodingData, 
    nBitsPrecision : Int, 
    trotterStepSize : Double, 
    trotterOrder : Int) : (Double, Double) {
    
    // The data describing the Hamiltonian for all these steps is contained in
    // `qSharpData`
    let (nSpinOrbitals, fermionTermData, statePrepData, energyOffset) = qSharpData!;
    
    // We use a Product formula, also known as `Trotterization` to
    // simulate the Hamiltonian.
    let (nQubits, (rescaleFactor, oracle)) = 
        TrotterStepOracle(qSharpData, trotterStepSize, trotterOrder);
    
    // The operation that creates the trial state is defined below.
    // By default, greedy filling of spin-orbitals is used.
    let statePrep = PrepareTrialState(statePrepData, _);
    
    // We use the Robust Phase Estimation algorithm
    // of Kimmel, Low and Yoder.
    let phaseEstAlgorithm = RobustPhaseEstimation(nBitsPrecision, _, _);
    
    // This runs the quantum algorithm and returns a phase estimate.
    let estPhase = EstimateEnergy(nQubits, statePrep, oracle, phaseEstAlgorithm);
    
    // We obtain the energy estimate by rescaling the phase estimate
    // with the trotterStepSize. We also add the constant energy offset
    // to the estimated energy.
    let estEnergy = estPhase * rescaleFactor + energyOffset;
    
    // We return both the estimated phase, and the estimated energy.
    return (estPhase, estEnergy);
}
```

Этот код Q # теперь можно вызывать из программы драйвера. В следующем примере мы создадим симулятор с полным состоянием и выполняем `GetEnergyByTrotterization` для получения энергии в состоянии "Земля".

```csharp
using (var qsim = new QuantumSimulator())
{
    // We specify the bits of precision desired in the phase estimation 
    // algorithm
    var bits = 7;

    // We specify the step-size of the simulated time-evolution. This needs to
    // be small enough to avoid aliasing of phases, and also to control the
    // error of simulation.
    var trotterStep = 0.4;

    // Choose the Trotter integrator order
    Int64 trotterOrder = 1;

    // As the quantum algorithm is probabilistic, let us run a few trials.

    // This may be compared to true value of
    Console.WriteLine("Exact molecular Hydrogen ground state energy: -1.137260278.\n");
    Console.WriteLine("----- Performing quantum energy estimation by Trotter simulation algorithm");
    for (int i = 0; i < 5; i++)
    {
        // EstimateEnergyByTrotterization
        var (phaseEst, energyEst) = GetEnergyByTrotterization.Run(qsim, qSharpData, bits, trotterStep, trotterOrder).Result;
    }
}
```

Обратите внимание, что возвращаются два параметра. `energyEst`представляет собой оценку энергии в состоянии "Земля" и должно быть `-1.137` в среднем. `phaseEst`— Это необработанный этап, возвращенный алгоритмом оценки этапа. он полезен для диагностики, когда происходит присвоение псевдонимов из-за `trotterStep` слишком большого размера.
