---
title: Получение количества ресурсов | Документация Майкрософт
description: Получение документов о количестве ресурсов
author: guanghaolow
ms.author: gulow
ms.date: 10/23/2018
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.examples.resourcecounts
ms.openlocfilehash: b28a27c4c1f1e64644fcfb074a731ff7b65cacb6
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/26/2019
ms.locfileid: "73184089"
---
## <a name="obtaining-resource-counts"></a><span data-ttu-id="d5541-103">Получение счетчиков ресурсов</span><span class="sxs-lookup"><span data-stu-id="d5541-103">Obtaining resource counts</span></span>

<span data-ttu-id="d5541-104">Затраты на моделирование $n $ Кубитс на классическая компьютеры масштабируются экспоненциально с $n $.</span><span class="sxs-lookup"><span data-stu-id="d5541-104">The cost of simulating $n$ qubits on a classical computers scales exponentially with $n$.</span></span> <span data-ttu-id="d5541-105">Это значительно ограничивает размер имитации тактовой химияи, которую можно выполнить с помощью симулятора полного состояния.</span><span class="sxs-lookup"><span data-stu-id="d5541-105">This greatly limits the size of an quantum chemistry simulation we may perform with the full-state simulator.</span></span> <span data-ttu-id="d5541-106">Для больших экземпляров химия, тем не менее, мы можем получить полезную информацию.</span><span class="sxs-lookup"><span data-stu-id="d5541-106">For large instances of chemistry, we may nevertheless obtain useful information.</span></span> <span data-ttu-id="d5541-107">Здесь мы рассмотрим, как издержки ресурсов, например количество шлюзов T-Гейтс или Кнот, для имитации химия можно получить в автоматическом режиме с помощью [симулятора трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span><span class="sxs-lookup"><span data-stu-id="d5541-107">Here, we examine how resource costs, such as the number of T-gates or CNOT gates, for simulating chemistry may be obtained in an automated fashion using the [trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="d5541-108">Такая информация информирует нас о том, что тактовые компьютеры могут быть достаточно большими для выполнения этих алгоритмов тактовой химияи.</span><span class="sxs-lookup"><span data-stu-id="d5541-108">Such information informs us of when quantum computers might be large enough to run these quantum chemistry algorithms.</span></span> <span data-ttu-id="d5541-109">Для справки см. предоставленный образец `GetGateCount`.</span><span class="sxs-lookup"><span data-stu-id="d5541-109">For reference, see the provided `GetGateCount` sample.</span></span>

<span data-ttu-id="d5541-110">Предположим, что у нас уже есть экземпляр `FermionHamiltonian`, скажем, загруженный из схемы Брумбридже, как описано в примере [загрузки из файла](xref:microsoft.quantum.chemistry.examples.loadhamiltonian) .</span><span class="sxs-lookup"><span data-stu-id="d5541-110">Let us assume that we already have a `FermionHamiltonian` instance, say, loaded from the Broombridge schema as discussed in the [loading-from-file](xref:microsoft.quantum.chemistry.examples.loadhamiltonian) example.</span></span> 

```csharp
    // Filename of Hamiltonian to be loaded.
    var filename = "...";

    // This deserializes Broombridge.
    var problem = Broombridge.Deserializers.DeserializeBroombridge(filename).ProblemDescriptions.First();

    // This is a data structure representing the Jordan-Wigner encoding 
    // of the Hamiltonian that we may pass to a Q# algorithm.
    var qSharpData = problem.ToQSharpFormat();
```

<span data-ttu-id="d5541-111">Синтаксис для получения оценки ресурсов практически идентичен запуску алгоритма в симуляторе с полным состоянием.</span><span class="sxs-lookup"><span data-stu-id="d5541-111">The syntax for obtaining resource estimates is almost identical to running the algorithm on the full-state simulator.</span></span> <span data-ttu-id="d5541-112">Мы просто выбираем другой целевой компьютер.</span><span class="sxs-lookup"><span data-stu-id="d5541-112">We simply choose a different target machine.</span></span> <span data-ttu-id="d5541-113">В целях оценки ресурсов достаточно оценить стоимость отдельного Троттер шага или тактовой анализ, созданный методом Кубитизатион.</span><span class="sxs-lookup"><span data-stu-id="d5541-113">For the purposes of resource estimates, it suffices to evaluate the cost of a single Trotter step, or a quantum walk created by the Qubitization technique.</span></span> <span data-ttu-id="d5541-114">Ниже приведен стандартный шаблон для вызова этих алгоритмов.</span><span class="sxs-lookup"><span data-stu-id="d5541-114">The boilerplate for invoking these algorithms are as follows.</span></span>

```qsharp
//////////////////////////////////////////////////////////////////////////
// Using Trotterization //////////////////////////////////////////////////
//////////////////////////////////////////////////////////////////////////

/// # Summary
/// This allocates qubits and applies a single Trotter step.
operation RunTrotterStep (qSharpData: JordanWignerEncodingData) : Unit {
    
    // The data describing the Hamiltonian for all these steps is contained in
    // `qSharpData`
    // We use a Product formula, also known as `Trotterization` to
    // simulate the Hamiltonian.
    // The integrator step size does not affect the gate cost of a single step.
    let trotterStepSize = 1.0;
    
    // Order of integrator
    let trotterOrder = 1;
    let (nQubits, (rescaleFactor, oracle)) = TrotterStepOracle(qSharpData, trotterStepSize, trotterOrder);
    
    // We not allocate qubits an run a single step.
    using (qubits = Qubit[nQubits]) {
        oracle(qubits);
        ResetAll(qubits);
    }
}


//////////////////////////////////////////////////////////////////////////
// Using Qubitization ////////////////////////////////////////////////////
//////////////////////////////////////////////////////////////////////////

/// # Summary
/// This allocates qubits and applies a single qubitization step.
operation RunQubitizationStep (qSharpData: JordanWignerEncodingData) : Double {
    
    // The data describing the Hamiltonian for all these steps is contained in
    // `qSharpData`
    let (nQubits, (l1Norm, oracle)) = QubitizationOracle(qSharpData);
    
    // We now allocate qubits and run a single step.
    using (qubits = Qubit[nQubits]) {
        oracle(qubits);
        ResetAll(qubits);
    }
    
    return l1Norm;
}
```

<span data-ttu-id="d5541-115">Теперь мы настроим симулятор трассировки, чтобы отслеживать интересующие вас ресурсы.</span><span class="sxs-lookup"><span data-stu-id="d5541-115">We now configure the trace simulator to track the resources we are interested in.</span></span> <span data-ttu-id="d5541-116">В этом случае мы подсчитани простые тактовые операции, установив для флага `usePrimitiveOperationsCounter` значение `true`.</span><span class="sxs-lookup"><span data-stu-id="d5541-116">In this case, we count primitive quantum operations by setting the `usePrimitiveOperationsCounter` flag to `true`.</span></span> <span data-ttu-id="d5541-117">Техническая информация `throwOnUnconstraintMeasurement` имеет значение `false`, чтобы избежать исключений в случаях, когда код Q # неправильно утверждает пробабилтий результатов измерения, если таковые были выполнены.</span><span class="sxs-lookup"><span data-stu-id="d5541-117">A technical detail `throwOnUnconstraintMeasurement` is set to `false` to avoid exceptions in cases where the Q# code does not correctly assert of probabiltiy of measurement outcomes, if any are performed.</span></span>

```csharp
private static QCTraceSimulator CreateAndConfigureTraceSim()
{
    // Create and configure Trace Simulator
    var config = new QCTraceSimulatorConfiguration()
    {
        usePrimitiveOperationsCounter = true,
        throwOnUnconstraintMeasurement = false
    };

    return new QCTraceSimulator(config);
}
```

<span data-ttu-id="d5541-118">Теперь мы запускаем алгоритм такта из программы драйвера, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="d5541-118">We now run the quantum algorithm from the driver program as follows.</span></span>

```csharp
// Instantiate a trace simulator instance
QCTraceSimulator sim = CreateAndConfigureTraceSim();

// Run the quantum algorithm on the trace simulator.
RunQubitizationStep.Run(sim, qSharpData);

// Print all resource counts to file.
var gateStats = sim.ToCSV();
foreach (var x in gateStats)
{
    System.IO.File.WriteAllLines($"QubitizationGateCountEstimates.{x.Key}.csv", new string[] { x.Value });
}
```