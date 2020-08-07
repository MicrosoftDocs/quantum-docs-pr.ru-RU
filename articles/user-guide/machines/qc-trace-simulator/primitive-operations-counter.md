---
title: Счетчик примитивных операций — пакет средств разработки тактов
description: Сведения о счетчике Microsoft КДК-примитивных операций, который использует симулятор трассировки тактов для отслеживания выполнения примитивов, используемых операциями в Q# программе.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.primitive-counter
no-loc:
- Q#
- $$v
ms.openlocfilehash: ceb70cef6dc0a4530b992b5a529248a8b283c17f
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868242"
---
# <a name="quantum-trace-simulator-primitive-operations-counter"></a><span data-ttu-id="9fc01-103">Симулятор трассировки тактов: Счетчик примитивных операций</span><span class="sxs-lookup"><span data-stu-id="9fc01-103">Quantum trace simulator: primitive operations counter</span></span>

<span data-ttu-id="9fc01-104">Счетчик операции примитива является частью [имитатора тактовой трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro)пакета разработки тактов.</span><span class="sxs-lookup"><span data-stu-id="9fc01-104">The primitive operation counter is a part of the Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="9fc01-105">Он подсчитывает количество простых выполнений, используемых каждой операцией, вызванной в тактовой программе.</span><span class="sxs-lookup"><span data-stu-id="9fc01-105">It counts the number of primitive executions used by every operation invoked in a quantum program.</span></span> 

<span data-ttu-id="9fc01-106">Все <xref:microsoft.quantum.intrinsic> операции выражаются с точки зрения однокубитного вращения, T Operations, кубит Клиффорд Operations, кнот операций и измерений Multi-кубит Паули observable.</span><span class="sxs-lookup"><span data-stu-id="9fc01-106">All <xref:microsoft.quantum.intrinsic> operations are expressed in terms of single-qubit rotations, T operations, single-qubit Clifford operations, CNOT operations, and measurements of multi-qubit Pauli observables.</span></span> <span data-ttu-id="9fc01-107">Счетчик примитивных операций выполняет статистическую обработку и собирает статистические данные по всем краям [графа вызовов](https://en.wikipedia.org/wiki/Call_graph)операции.</span><span class="sxs-lookup"><span data-stu-id="9fc01-107">The Primitive Operations Counter aggregates and collects statistics over all the edges of the operation's [call graph](https://en.wikipedia.org/wiki/Call_graph).</span></span>

## <a name="invoking-the-primitive-operation-counter"></a><span data-ttu-id="9fc01-108">Вызов счетчика примитивной операции</span><span class="sxs-lookup"><span data-stu-id="9fc01-108">Invoking the primitive operation counter</span></span>

<span data-ttu-id="9fc01-109">Чтобы запустить симулятор трассировки тактов со счетчиком операций-примитивов, необходимо создать <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> экземпляр, присвоить `UsePrimitiveOperationsCounter` свойству **значение true**, а затем создать новый <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> экземпляр с `QCTraceSimulatorConfiguration` параметром в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="9fc01-109">To run the quantum trace simulator with the primitive operation counter, you must create a <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instance, set the `UsePrimitiveOperationsCounter` property to **true**, and then create a new <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instance with the `QCTraceSimulatorConfiguration` as the parameter.</span></span>

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UsePrimitiveOperationsCounter = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-primitive-operation-counter-in-a-c-host-program"></a><span data-ttu-id="9fc01-110">Использование счетчика примитивных операций в основной программе C#</span><span class="sxs-lookup"><span data-stu-id="9fc01-110">Using the primitive operation counter in a C# host program</span></span>

<span data-ttu-id="9fc01-111">В примере C#, приведенном в этом разделе, подсчитывается количество <xref:microsoft.quantum.intrinsic.t> операций, необходимых для реализации <xref:microsoft.quantum.intrinsic.ccnot> операции, на основе следующего Q# примера кода:</span><span class="sxs-lookup"><span data-stu-id="9fc01-111">The C# example that follows in this section counts how many <xref:microsoft.quantum.intrinsic.t> operations are needed to implement the <xref:microsoft.quantum.intrinsic.ccnot> operation, based on the following Q# sample code:</span></span>

```qsharp
open Microsoft.Quantum.Intrinsic;
operation ApplySampleWithCCNOT() : Unit {

    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    }
}
```

<span data-ttu-id="9fc01-112">Чтобы проверить, `CCNOT` требуется ли семь `T` операций и которые `ApplySampleWithCCNOT` выполняют восемь `T` операций, используйте следующий код C#:</span><span class="sxs-lookup"><span data-stu-id="9fc01-112">To check that `CCNOT` requires seven `T` operations and that `ApplySampleWithCCNOT` runs eight `T` operations, use the following C# code:</span></span>

```csharp 
// using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
// using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.UsePrimitiveOperationsCounter = true;
var sim = new QCTraceSimulator(config);
var res = ApplySampleWithCCNOT.Run(sim).Result;

double tCountAll = sim.GetMetric<ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
double tCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
```

<span data-ttu-id="9fc01-113">Запускается первая часть программы `ApplySampleWithCCNOT` .</span><span class="sxs-lookup"><span data-stu-id="9fc01-113">The first part of the program runs `ApplySampleWithCCNOT`.</span></span> <span data-ttu-id="9fc01-114">Во второй части используется [`QCTraceSimulator.GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) метод для получения количества `T` операций, выполняемых `ApplySampleWithCCNOT` :</span><span class="sxs-lookup"><span data-stu-id="9fc01-114">The second part uses the [`QCTraceSimulator.GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) method to retrieve the number of `T` operations run by `ApplySampleWithCCNOT`:</span></span> 

<span data-ttu-id="9fc01-115">При вызове `GetMetric` с двумя параметрами типа он возвращает значение метрики, связанной с данным ребром графа вызовов.</span><span class="sxs-lookup"><span data-stu-id="9fc01-115">When you call `GetMetric` with two type parameters, it returns the value of the metric associated with a given call graph edge.</span></span> <span data-ttu-id="9fc01-116">В предыдущем примере программа вызывает `Primitive.CCNOT` операцию в `ApplySampleWithCCNOT` и, следовательно, граф вызовов содержит ребро `<Primitive.CCNOT, ApplySampleWithCCNOT>` .</span><span class="sxs-lookup"><span data-stu-id="9fc01-116">In the preceding example, the program calls the `Primitive.CCNOT` operation  within `ApplySampleWithCCNOT` and therefore the call graph contains the edge `<Primitive.CCNOT, ApplySampleWithCCNOT>`.</span></span> 

<span data-ttu-id="9fc01-117">Чтобы получить количество `CNOT` используемых операций, добавьте следующую строку:</span><span class="sxs-lookup"><span data-stu-id="9fc01-117">To retrieve the number of `CNOT` operations used, add the following line:</span></span>
```csharp
double cxCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.CX);
```

<span data-ttu-id="9fc01-118">Наконец, можно вывести всю статистику, собранную счетчиком примитивных операций в формате CSV, с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="9fc01-118">Finally, you can output all the statistics collected by the Primitive Operations Counter in CSV format using the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.primitiveOperationsCounter];
```

## <a name="see-also"></a><span data-ttu-id="9fc01-119">См. также</span><span class="sxs-lookup"><span data-stu-id="9fc01-119">See also</span></span>

- <span data-ttu-id="9fc01-120">Обзор [имитатора трассировки такта](xref:microsoft.quantum.machines.qc-trace-simulator.intro) в пакете разработки тактов.</span><span class="sxs-lookup"><span data-stu-id="9fc01-120">The Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
- <span data-ttu-id="9fc01-121"><xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator>Справочник по API.</span><span class="sxs-lookup"><span data-stu-id="9fc01-121">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API reference.</span></span>
- <span data-ttu-id="9fc01-122"><xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>Справочник по API.</span><span class="sxs-lookup"><span data-stu-id="9fc01-122">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API reference.</span></span>
- <span data-ttu-id="9fc01-123"><xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.PrimitiveOperationsGroupsNames>Справочник по API.</span><span class="sxs-lookup"><span data-stu-id="9fc01-123">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.PrimitiveOperationsGroupsNames> API reference.</span></span>