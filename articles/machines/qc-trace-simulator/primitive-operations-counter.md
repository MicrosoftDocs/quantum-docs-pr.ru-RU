---
title: Счетчик примитивных операций | Симулятор трассировки компьютерных тактов | Документация Майкрософт
description: Обзор имитатора трассировки тактов компьютера
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.primitive-counter
ms.openlocfilehash: b7ec8b0d7a713051e36cb778c087050f0257710f
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/29/2019
ms.locfileid: "73184888"
---
# <a name="primitive-operations-counter"></a><span data-ttu-id="f9a9d-103">Счетчик примитивных операций</span><span class="sxs-lookup"><span data-stu-id="f9a9d-103">Primitive Operations Counter</span></span>  

<span data-ttu-id="f9a9d-104">`Primitive Operations Counter` является частью [симулятора трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro)компьютерных тактов.</span><span class="sxs-lookup"><span data-stu-id="f9a9d-104">The `Primitive Operations Counter` is a part of the quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="f9a9d-105">Он подсчитывает количество простых выполнений, используемых каждой операцией, вызванной в тактовой программе.</span><span class="sxs-lookup"><span data-stu-id="f9a9d-105">It counts the number of primitive executions used by every operation invoked in a quantum program.</span></span> <span data-ttu-id="f9a9d-106">Все операции от `Microsoft.Quantum.Primitive` выражаются в виде кубитных поворотов, T-шлюзов, одного кубит Клиффорд Gates, кнот шлюзов и измерений многокубит Паули observable.</span><span class="sxs-lookup"><span data-stu-id="f9a9d-106">All operations from `Microsoft.Quantum.Primitive` are expressed in terms of single qubit rotations, T gates, single qubit Clifford gates, CNOT gates and measurements of multi-qubit Pauli observables.</span></span> <span data-ttu-id="f9a9d-107">Собранные статистические данные суммируются по краям графа вызовов операций.</span><span class="sxs-lookup"><span data-stu-id="f9a9d-107">Collected statistics are aggregated over the edges of the operations call graph.</span></span> <span data-ttu-id="f9a9d-108">Теперь давайте подсчитани количество `T` шлюзов, необходимых для реализации операции `CCNOT`.</span><span class="sxs-lookup"><span data-stu-id="f9a9d-108">Let us now count how many `T` gates are needed to implement the `CCNOT` operation.</span></span> 

```qsharp
open Microsoft.Quantum.Primitive;
operation CCNOTDriver() : Unit {

    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    } 
}
```

## <a name="using-the-primitive-operations-counter-within-a-c-program"></a><span data-ttu-id="f9a9d-109">Использование счетчика примитивных операций в C# программе</span><span class="sxs-lookup"><span data-stu-id="f9a9d-109">Using the Primitive Operations Counter within a C# Program</span></span>

<span data-ttu-id="f9a9d-110">Чтобы убедиться, что `CCNOT` действительно требуется 7 `T` шлюзов и что `CCNOTDriver` выполняет 8 `T` шлюзов, можно использовать следующий C# код:</span><span class="sxs-lookup"><span data-stu-id="f9a9d-110">To check that `CCNOT` indeed requires 7 `T` gates and that `CCNOTDriver` executes 8 `T` gates we can use the following C# code:</span></span>

```csharp 
// using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
// using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.usePrimitiveOperationsCounter = true;
var sim = new QCTraceSimulator(config);
var res = CCNOTDriver.Run(sim).Result;

double tCountAll = sim.GetMetric<CCNOTDriver>(PrimitiveOperationsGroupsNames.T);
double tCount = sim.GetMetric<Primitive.CCNOT, CCNOTDriver>(PrimitiveOperationsGroupsNames.T);
```

<span data-ttu-id="f9a9d-111">Первая часть программы выполняет `CCNOTDriver`.</span><span class="sxs-lookup"><span data-stu-id="f9a9d-111">The first part of the program executes `CCNOTDriver`.</span></span> <span data-ttu-id="f9a9d-112">Во второй части мы используем метод `QCTraceSimulator.GetMetric` для получения числа T Gates, выполняемых `CCNOTDriver`:</span><span class="sxs-lookup"><span data-stu-id="f9a9d-112">In the second part, we use the method `QCTraceSimulator.GetMetric` to get the number of T gates executed by `CCNOTDriver`:</span></span> 

```csharp
double tCount = sim.GetMetric<Primitive.CCNOT, CCNOTDriver>(PrimitiveOperationsGroupsNames.T);
double tCountAll = sim.GetMetric<CCNOTDriver>(PrimitiveOperationsGroupsNames.T);
```

<span data-ttu-id="f9a9d-113">При вызове `GetMetric` с двумя параметрами типа он возвращает значение метрики, связанной с данным ребром графа вызовов.</span><span class="sxs-lookup"><span data-stu-id="f9a9d-113">When `GetMetric` is called with two type parameters it returns the value of the metric associated with a given call graph edge.</span></span> <span data-ttu-id="f9a9d-114">В нашем примере операции `Primitive.CCNOT` вызывается в `CCNOTDriver` и, следовательно, граф вызовов содержит `<Primitive.CCNOT,CCNOTDriver>`ребра.</span><span class="sxs-lookup"><span data-stu-id="f9a9d-114">In our example operation `Primitive.CCNOT` is called within `CCNOTDriver` and therefore the call graph contains the edge `<Primitive.CCNOT,CCNOTDriver>`.</span></span> 

<span data-ttu-id="f9a9d-115">Чтобы узнать количество используемых шлюзов `CNOT`, можно добавить следующую строку:</span><span class="sxs-lookup"><span data-stu-id="f9a9d-115">To get the number of `CNOT` gates used, we can add the following line:</span></span>
```csharp
double cxCount = sim.GetMetric<Primitive.CCNOT, CCNOTDriver>(PrimitiveOperationsGroupsNames.CX);
```

<span data-ttu-id="f9a9d-116">Наконец, чтобы вывести всю статистику, собранную счетчиком шлюзов в формате CSV, можно использовать следующее:</span><span class="sxs-lookup"><span data-stu-id="f9a9d-116">Finally, to output all the statistics collected by the gate counter in CSV format we can use the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.primitiveOperationsCounter];
```

## <a name="see-also"></a><span data-ttu-id="f9a9d-117">Дополнительные материалы</span><span class="sxs-lookup"><span data-stu-id="f9a9d-117">See also</span></span> ##

- <span data-ttu-id="f9a9d-118">Обзор [имитатора трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro) компьютерных тактов.</span><span class="sxs-lookup"><span data-stu-id="f9a9d-118">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
