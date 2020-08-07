---
title: Получение оценок энергетических уровней
description: Пошаговое руководство по примерам Q# программы, которая оценивает значения уровня энергии молекулярное водорода.
author: guanghaolow
ms.author: gulow
ms.date: 07/02/2020
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.examples.energyestimate
no-loc:
- Q#
- $$v
ms.openlocfilehash: a2df4b829a3f4946c6de6e6b80ad72a5bc192b2c
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869211"
---
# <a name="obtaining-energy-level-estimates"></a><span data-ttu-id="2d0dd-103">Получение оценок энергетических уровней</span><span class="sxs-lookup"><span data-stu-id="2d0dd-103">Obtaining energy level estimates</span></span>
<span data-ttu-id="2d0dd-104">Оценка значений уровня энергии является одним из основных приложений тактовой химия.</span><span class="sxs-lookup"><span data-stu-id="2d0dd-104">Estimating the values of energy levels is one of the principal applications of quantum chemistry.</span></span> <span data-ttu-id="2d0dd-105">В этой статье описано, как это сделать для канонического примера водомолекулярное.</span><span class="sxs-lookup"><span data-stu-id="2d0dd-105">This article outlines how you can perform this for the canonical example of molecular hydrogen.</span></span> <span data-ttu-id="2d0dd-106">Образец, указанный в этом разделе, находится [`MolecularHydrogen`](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/MolecularHydrogen) в репозитории примеров химия.</span><span class="sxs-lookup"><span data-stu-id="2d0dd-106">The sample referenced in this section is [`MolecularHydrogen`](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/MolecularHydrogen) in the chemistry samples repository.</span></span> <span data-ttu-id="2d0dd-107">Более наглядным примером, который отображает выходные данные, является [`MolecularHydrogenGUI`](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/MolecularHydrogenGUI) демонстрация.</span><span class="sxs-lookup"><span data-stu-id="2d0dd-107">A more visual example that plots the output is the [`MolecularHydrogenGUI`](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/MolecularHydrogenGUI) demo.</span></span>

## <a name="estimating-the-energy-values-of-molecular-hydrogen"></a><span data-ttu-id="2d0dd-108">Оценка значений энергии для молекулярное водорода</span><span class="sxs-lookup"><span data-stu-id="2d0dd-108">Estimating the energy values of molecular hydrogen</span></span>

<span data-ttu-id="2d0dd-109">Первым шагом является создание Хамилтониан, представляющего молекулярное водорода.</span><span class="sxs-lookup"><span data-stu-id="2d0dd-109">The first step is to construct the Hamiltonian representing molecular hydrogen.</span></span> <span data-ttu-id="2d0dd-110">Хотя это можно создать с помощью средства Нвчем, для краткости в этом примере термины Хамилтониан добавляются вручную.</span><span class="sxs-lookup"><span data-stu-id="2d0dd-110">Although you can construct this using the NWChem tool, for brevity, this sample adds the Hamiltonian terms manually.</span></span>

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

<span data-ttu-id="2d0dd-111">Для имитации Хамилтониан необходимо преобразовать операторы фермион в операторы кубит.</span><span class="sxs-lookup"><span data-stu-id="2d0dd-111">Simulating the Hamiltonian requires converting the fermion operators to qubit operators.</span></span> <span data-ttu-id="2d0dd-112">Это преобразование выполняется с помощью Вигнер кодирования следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2d0dd-112">This conversion is performed through the Jordan-Wigner encoding as follows:</span></span>

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

<span data-ttu-id="2d0dd-113">Затем Pass `qSharpData` , который представляет хамилтониан, для `TrotterStepOracle` функции.</span><span class="sxs-lookup"><span data-stu-id="2d0dd-113">Next, pass `qSharpData`, which represents the Hamiltonian, to the `TrotterStepOracle` function.</span></span> <span data-ttu-id="2d0dd-114">`TrotterStepOracle`Возвращает операцию такта, которая приблизительно соответствует эволюции Хамилтониан в реальном времени.</span><span class="sxs-lookup"><span data-stu-id="2d0dd-114">`TrotterStepOracle` returns a quantum operation that approximates the real-time evolution of the Hamiltonian.</span></span> <span data-ttu-id="2d0dd-115">Дополнительные сведения см. в разделе [имитация хамилтониан Dynamics](xref:microsoft.quantum.chemistry.concepts.simulationalgorithms).</span><span class="sxs-lookup"><span data-stu-id="2d0dd-115">For more information, see [Simulating Hamiltonian dynamics](xref:microsoft.quantum.chemistry.concepts.simulationalgorithms).</span></span>

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

<span data-ttu-id="2d0dd-116">На этом этапе можно использовать [алгоритмы оценки этапа](xref:microsoft.quantum.libraries.characterization) стандартной библиотеки для изучения энергии в состоянии заземления с помощью предыдущего моделирования.</span><span class="sxs-lookup"><span data-stu-id="2d0dd-116">At this point, you can use the standard library's [phase estimation algorithms](xref:microsoft.quantum.libraries.characterization) to learn the ground state energy using the previous simulation.</span></span> <span data-ttu-id="2d0dd-117">Для этого необходимо подготовить хорошее приближение к состоянию земли в такте.</span><span class="sxs-lookup"><span data-stu-id="2d0dd-117">This requires preparing a good approximation to the quantum ground state.</span></span> <span data-ttu-id="2d0dd-118">В схеме представлены предложения по подобным приближениям [`Broombridge`](xref:microsoft.quantum.libraries.chemistry.schema.broombridge) .</span><span class="sxs-lookup"><span data-stu-id="2d0dd-118">Suggestions for such approximations are provided in the [`Broombridge`](xref:microsoft.quantum.libraries.chemistry.schema.broombridge) schema.</span></span> <span data-ttu-id="2d0dd-119">Однако в отсутствие этих предложений подход по умолчанию добавляет ряд `hamiltonian.NElectrons` электронов в гридили, чтобы сократить силы по диагонали на один электрон.</span><span class="sxs-lookup"><span data-stu-id="2d0dd-119">However, absent these suggestions, the default approach adds a number of `hamiltonian.NElectrons` electrons to greedily minimize the diagonal one-electron term energies.</span></span> <span data-ttu-id="2d0dd-120">Функции и операции оценки этапа предоставляются в нотации DocFX в пространстве имен [Microsoft. тактов. character](xref:microsoft.quantum.characterization) .</span><span class="sxs-lookup"><span data-stu-id="2d0dd-120">The phase estimation functions and operations are provided in DocFX notation in the [Microsoft.Quantum.Characterization](xref:microsoft.quantum.characterization) namespace.</span></span>

<span data-ttu-id="2d0dd-121">В следующем фрагменте кода показано, как в режиме реального времени результаты развития библиотеки моделирования химия интегрируются с оценкой фазы такта.</span><span class="sxs-lookup"><span data-stu-id="2d0dd-121">The following snippet shows how the real-time evolution output by the chemistry simulation library integrates with quantum phase estimation.</span></span>

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

<span data-ttu-id="2d0dd-122">Теперь можно вызвать Q# код из основной программы.</span><span class="sxs-lookup"><span data-stu-id="2d0dd-122">You can now invoke the Q# code from the host program.</span></span> <span data-ttu-id="2d0dd-123">В следующем коде C# создается симулятор с полным состоянием и выполняется `GetEnergyByTrotterization` для получения энергии в состоянии заземления.</span><span class="sxs-lookup"><span data-stu-id="2d0dd-123">The following C# code creates a full-state simulator and runs `GetEnergyByTrotterization` to obtain the ground state energy.</span></span>

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

<span data-ttu-id="2d0dd-124">Операция возвращает два параметра:</span><span class="sxs-lookup"><span data-stu-id="2d0dd-124">The operation returns two parameters:</span></span> 

- <span data-ttu-id="2d0dd-125">`energyEst`является оценкой энергии в состоянии "Земля" и должно быть близко к `-1.137` среднему значению.</span><span class="sxs-lookup"><span data-stu-id="2d0dd-125">`energyEst` is the estimate of the ground state energy and should be close to `-1.137` on average.</span></span> 
- <span data-ttu-id="2d0dd-126">`phaseEst`— Это необработанный этап, возвращенный алгоритмом оценки этапа.</span><span class="sxs-lookup"><span data-stu-id="2d0dd-126">`phaseEst` is the raw phase returned by the phase estimation algorithm.</span></span> <span data-ttu-id="2d0dd-127">Это полезно для диагностики псевдонимов, когда это происходит из-за `trotterStep` слишком большого значения.</span><span class="sxs-lookup"><span data-stu-id="2d0dd-127">This useful for diagnosing aliasing when it occurs due to a `trotterStep` value that is too large.</span></span>
