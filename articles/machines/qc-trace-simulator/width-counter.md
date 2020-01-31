---
title: Счетчик ширины | Симулятор трассировки компьютерных тактов | Документация Майкрософт
description: Обзор симулятора трассировки квантового компьютера
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.width-counter
ms.openlocfilehash: 9c3601e74eec17bd6b463e90f8f3085c959d6f95
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820374"
---
# <a name="width-counter"></a><span data-ttu-id="7c12b-103">Счетчик ширины</span><span class="sxs-lookup"><span data-stu-id="7c12b-103">Width Counter</span></span>

<span data-ttu-id="7c12b-104">`Width Counter` подсчитывает количество Кубитс, выделенных и заимствованных каждой операцией.</span><span class="sxs-lookup"><span data-stu-id="7c12b-104">The `Width Counter` counts the number of qubits allocated and borrowed by each operation.</span></span>
<span data-ttu-id="7c12b-105">Все операции из пространства имен `Microsoft.Quantum.Intrinsic` выражены в виде однокубитных поворотов, T-шлюзов, одного кубит Клиффорд Гейтсов, шлюзов кнот и измерений Multi-кубит Паули observable.</span><span class="sxs-lookup"><span data-stu-id="7c12b-105">All operations from the `Microsoft.Quantum.Intrinsic` namespace are expressed in terms of single qubit rotations, T gates, single qubit Clifford gates, CNOT gates and measurements of multi-qubit Pauli observables.</span></span> <span data-ttu-id="7c12b-106">Некоторые примитивные операции могут выделить дополнительные Кубитс.</span><span class="sxs-lookup"><span data-stu-id="7c12b-106">Some of the primitive operations can allocate extra qubits.</span></span> <span data-ttu-id="7c12b-107">Например, умножьте управляемый `X` Gates или контролируемый `T` Гейтс.</span><span class="sxs-lookup"><span data-stu-id="7c12b-107">For example, multiply controlled `X` gates or controlled `T` gates.</span></span> <span data-ttu-id="7c12b-108">Давайте вычислим количество дополнительных Кубитс, выделенных реализацией многофакторного `X` вентиля:</span><span class="sxs-lookup"><span data-stu-id="7c12b-108">Let us compute the number of extra qubits allocated by the implementation of a multiply controlled `X` gate:</span></span>

```qsharp
open Microsoft.Quantum.Intrinsic;
open Microsoft.Quantum.Arrays;
operation ApplyMultiControlledX( numberOfQubits : Int ) : Unit {
    using(qubits = Qubit[numberOfQubits]) {
        Controlled X (Rest(qubits), Head(qubits));
    } 
}
```

## <a name="using-width-counter-within-a-c-program"></a><span data-ttu-id="7c12b-109">Использование счетчика ширины в C# программе</span><span class="sxs-lookup"><span data-stu-id="7c12b-109">Using Width Counter within a C# Program</span></span>

<span data-ttu-id="7c12b-110">Умножение управляемого `X`, действующего на сумму 5 Кубитс, выделит 2 дополнительных Кубитс, и его входная ширина будет равна 5.</span><span class="sxs-lookup"><span data-stu-id="7c12b-110">Multiply controlled `X` acting on a total of 5 qubits will allocate 2 ancillary qubits and its input width will be 5.</span></span> <span data-ttu-id="7c12b-111">Чтобы убедиться, что это так, можно использовать следующую C# программу:</span><span class="sxs-lookup"><span data-stu-id="7c12b-111">To check that this is the case, we can use the following C# program:</span></span>

```csharp 
var config = new QCTraceSimulatorConfiguration();
config.useWidthCounter = true;
var sim = new QCTraceSimulator(config);
int totalNumberOfQubits = 5;
var res = ApplyMultiControlledX.Run(sim, totalNumberOfQubits).Result;

double allocatedQubits = 
    sim.GetMetric<Primitive.X, ApplyMultiControlledX>(
        WidthCounter.Metrics.ExtraWidth,
        functor: OperationFunctor.Controlled); 

double inputWidth =
    sim.GetMetric<Primitive.X, ApplyMultiControlledX>(
        WidthCounter.Metrics.InputWidth,
        functor: OperationFunctor.Controlled);
```

<span data-ttu-id="7c12b-112">Первая часть программы выполняет `ApplyMultiControlledX`.</span><span class="sxs-lookup"><span data-stu-id="7c12b-112">The first part of the program executes `ApplyMultiControlledX`.</span></span> <span data-ttu-id="7c12b-113">Во второй части мы используем метод `QCTraceSimulator.GetMetric`, чтобы получить количество выделенных Кубитс, а также число Кубитс, которые управляются `X` получения в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="7c12b-113">In the second part we use the method `QCTraceSimulator.GetMetric` to get the number of allocated qubits as well as the number of qubits that Controlled `X` received as input.</span></span> 

<span data-ttu-id="7c12b-114">Наконец, чтобы вывести всю статистику, собранную счетчиком ширины, в формате CSV, можно использовать следующее:</span><span class="sxs-lookup"><span data-stu-id="7c12b-114">Finally, to output all the statistics collected by width counter in CSV format we can use the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.widthCounter];
```

## <a name="see-also"></a><span data-ttu-id="7c12b-115">См. также</span><span class="sxs-lookup"><span data-stu-id="7c12b-115">See also</span></span> ##

- <span data-ttu-id="7c12b-116">Обзор [имитатора трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro) компьютерных тактов.</span><span class="sxs-lookup"><span data-stu-id="7c12b-116">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
