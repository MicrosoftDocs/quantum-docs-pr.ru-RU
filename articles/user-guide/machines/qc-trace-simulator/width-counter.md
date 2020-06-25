---
title: Счетчик ширины
description: Сведения о счетчике ширины Microsoft КДК, который подсчитывает количество Кубитс, выделенных и заимствованных каждой операцией в тактовой программе.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.width-counter
ms.openlocfilehash: a76292222950310acc90dded02980e4a5b792e76
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275564"
---
# <a name="width-counter"></a><span data-ttu-id="0e5d8-103">Счетчик ширины</span><span class="sxs-lookup"><span data-stu-id="0e5d8-103">Width Counter</span></span>

<span data-ttu-id="0e5d8-104">`Width Counter`Подсчитывает количество Кубитс, выделенных и заимствованных каждой операцией.</span><span class="sxs-lookup"><span data-stu-id="0e5d8-104">The `Width Counter` counts the number of qubits allocated and borrowed by each operation.</span></span>
<span data-ttu-id="0e5d8-105">Все операции из `Microsoft.Quantum.Intrinsic` пространства имен выражаются в виде однокубитных поворотов, T-шлюзов, одного кубит Клиффорд Gates, ШЛЮЗОВ кнот и измерений Multi-кубит Паули observable.</span><span class="sxs-lookup"><span data-stu-id="0e5d8-105">All operations from the `Microsoft.Quantum.Intrinsic` namespace are expressed in terms of single qubit rotations, T gates, single qubit Clifford gates, CNOT gates and measurements of multi-qubit Pauli observables.</span></span> <span data-ttu-id="0e5d8-106">Некоторые примитивные операции могут выделить дополнительные Кубитс.</span><span class="sxs-lookup"><span data-stu-id="0e5d8-106">Some of the primitive operations can allocate extra qubits.</span></span> <span data-ttu-id="0e5d8-107">Например, перемножьте контролируемые `X` шлюзы или контролируемые `T` шлюзы.</span><span class="sxs-lookup"><span data-stu-id="0e5d8-107">For example, multiply controlled `X` gates or controlled `T` gates.</span></span> <span data-ttu-id="0e5d8-108">Давайте вычислим количество дополнительных Кубитс, выделенных реализацией шлюза, управляемого умножением `X` :</span><span class="sxs-lookup"><span data-stu-id="0e5d8-108">Let us compute the number of extra qubits allocated by the implementation of a multiply controlled `X` gate:</span></span>

```qsharp
open Microsoft.Quantum.Intrinsic;
open Microsoft.Quantum.Arrays;
operation ApplyMultiControlledX( numberOfQubits : Int ) : Unit {
    using(qubits = Qubit[numberOfQubits]) {
        Controlled X (Rest(qubits), Head(qubits));
    } 
}
```

## <a name="using-width-counter-within-a-c-program"></a><span data-ttu-id="0e5d8-109">Использование счетчика ширины в программе C#</span><span class="sxs-lookup"><span data-stu-id="0e5d8-109">Using Width Counter within a C# Program</span></span>

<span data-ttu-id="0e5d8-110">Умножение `X` на 5 Кубитс выделит 2 дополнительных Кубитс, и его входная ширина будет равна 5.</span><span class="sxs-lookup"><span data-stu-id="0e5d8-110">Multiply controlled `X` acting on a total of 5 qubits will allocate 2 ancillary qubits and its input width will be 5.</span></span> <span data-ttu-id="0e5d8-111">Чтобы убедиться, что это так, можно использовать следующую программу C#:</span><span class="sxs-lookup"><span data-stu-id="0e5d8-111">To check that this is the case, we can use the following C# program:</span></span>

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

<span data-ttu-id="0e5d8-112">Выполняется первая часть программы `ApplyMultiControlledX` .</span><span class="sxs-lookup"><span data-stu-id="0e5d8-112">The first part of the program executes `ApplyMultiControlledX`.</span></span> <span data-ttu-id="0e5d8-113">Во второй части мы используем метод, `QCTraceSimulator.GetMetric` чтобы получить количество выделенных Кубитс, а также число Кубитс, контролируемых `X` в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="0e5d8-113">In the second part we use the method `QCTraceSimulator.GetMetric` to get the number of allocated qubits as well as the number of qubits that Controlled `X` received as input.</span></span> 

<span data-ttu-id="0e5d8-114">Наконец, чтобы вывести всю статистику, собранную счетчиком ширины, в формате CSV, можно использовать следующее:</span><span class="sxs-lookup"><span data-stu-id="0e5d8-114">Finally, to output all the statistics collected by width counter in CSV format we can use the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.widthCounter];
```

## <a name="see-also"></a><span data-ttu-id="0e5d8-115">См. также</span><span class="sxs-lookup"><span data-stu-id="0e5d8-115">See also</span></span> ##

- <span data-ttu-id="0e5d8-116">Обзор [имитатора трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro) компьютерных тактов.</span><span class="sxs-lookup"><span data-stu-id="0e5d8-116">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
