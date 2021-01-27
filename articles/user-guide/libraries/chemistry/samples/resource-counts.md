---
title: Получение счетчиков ресурсов
description: Узнайте, как получить оценку ресурсов с помощью симулятора трассировки тактов.
author: guanghaolow
ms.author: gulow
ms.date: 10/23/2018
ms.topic: sample
uid: microsoft.quantum.chemistry.examples.resourcecounts
no-loc:
- Q#
- $$v
ms.openlocfilehash: b8974114a5629fa1928b5774e79aba93fa3d1f7d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856246"
---
# <a name="obtaining-resource-counts"></a>Получение счетчиков ресурсов

Затраты на моделирование $n $ Кубитс на классическая компьютеры масштабируются экспоненциально с $n $. Это значительно ограничивает размер имитации тактовой химияи, которую можно выполнить с помощью симулятора полного состояния. Для больших экземпляров химия, тем не менее, мы можем получить полезную информацию. Здесь мы рассмотрим, как издержки ресурсов, например количество шлюзов T-Гейтс или Кнот, для имитации химия можно получить в автоматическом режиме с помощью [симулятора трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro). Такая информация информирует нас о том, что тактовые компьютеры могут быть достаточно большими для выполнения этих алгоритмов тактовой химияи. Для справки см. предоставленный `GetGateCount` пример.

Предположим, что у нас уже есть `FermionHamiltonian` экземпляр, скажем, загруженный из схемы брумбридже, как описано в примере [загрузки из файла](xref:microsoft.quantum.chemistry.examples.loadhamiltonian) . 

```csharp
    // Filename of Hamiltonian to be loaded.
    var filename = "...";

    // This deserializes Broombridge.
    var problem = Broombridge.Deserializers.DeserializeBroombridge(filename).ProblemDescriptions.First();

    // This is a data structure representing the Jordan-Wigner encoding 
    // of the Hamiltonian that we may pass to a Q# algorithm.
    var qSharpData = problem.ToQSharpFormat();
```

Синтаксис для получения оценки ресурсов практически идентичен запуску алгоритма в симуляторе с полным состоянием. Мы просто выбираем другой целевой компьютер. В целях оценки ресурсов достаточно оценить стоимость отдельного Троттер шага или тактовой анализ, созданный методом Кубитизатион. Ниже приведен стандартный шаблон для вызова этих алгоритмов.

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

Теперь мы настроим симулятор трассировки, чтобы отслеживать интересующие вас ресурсы. В этом случае мы подсчитани простые тактовые операции, установив `usePrimitiveOperationsCounter` для флага значение `true` . Технические подробности `throwOnUnconstraintMeasurement` устанавливаются в значение `false` , чтобы избежать исключений в случаях Q# , когда код неправильно утверждает вероятность результатов измерения, если таковые выполняются.

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

Теперь мы запускаем алгоритм такта из программы драйвера, как показано ниже.

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