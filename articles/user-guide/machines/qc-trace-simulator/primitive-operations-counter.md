---
title: Счетчик примитивных операций — пакет средств разработки тактов
description: 'Сведения о счетчике примитивных операций Microsoft КДК, который использует симулятор трассировки тактов для отслеживания простых процессов, используемых операциями в :::no-loc(Q#)::: программе.'
author: vadym-kl
ms.author: vadym
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.primitive-counter
no-loc:
- ':::no-loc(Q#):::'
- ':::no-loc($$v):::'
ms.openlocfilehash: bf75eb94696a489a587316928bc3f33baa4a1785
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92690948"
---
# <a name="quantum-trace-simulator-primitive-operations-counter"></a><span data-ttu-id="ac3e5-103">Симулятор трассировки тактов: Счетчик примитивных операций</span><span class="sxs-lookup"><span data-stu-id="ac3e5-103">Quantum trace simulator: primitive operations counter</span></span>

<span data-ttu-id="ac3e5-104">Счетчик операции примитива является частью [имитатора тактовой трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro)пакета разработки тактов.</span><span class="sxs-lookup"><span data-stu-id="ac3e5-104">The primitive operation counter is a part of the Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="ac3e5-105">Он подсчитывает количество простых процессов, используемых каждой операцией, вызванной в тактовой программе.</span><span class="sxs-lookup"><span data-stu-id="ac3e5-105">It counts the number of primitive processes used by every operation invoked in a quantum program.</span></span> 

<span data-ttu-id="ac3e5-106">Все <xref:Microsoft.Quantum.Intrinsic> операции выражаются с точки зрения однокубитного вращения, T Operations, кубит Клиффорд Operations, кнот операций и измерений Multi-кубит Паули observable.</span><span class="sxs-lookup"><span data-stu-id="ac3e5-106">All <xref:Microsoft.Quantum.Intrinsic> operations are expressed in terms of single-qubit rotations, T operations, single-qubit Clifford operations, CNOT operations, and measurements of multi-qubit Pauli observables.</span></span> <span data-ttu-id="ac3e5-107">Счетчик примитивных операций выполняет статистическую обработку и собирает статистические данные по всем краям [графа вызовов](https://en.wikipedia.org/wiki/Call_graph)операции.</span><span class="sxs-lookup"><span data-stu-id="ac3e5-107">The Primitive Operations Counter aggregates and collects statistics over all the edges of the operation's [call graph](https://en.wikipedia.org/wiki/Call_graph).</span></span>

## <a name="invoking-the-primitive-operation-counter"></a><span data-ttu-id="ac3e5-108">Вызов счетчика примитивной операции</span><span class="sxs-lookup"><span data-stu-id="ac3e5-108">Invoking the primitive operation counter</span></span>

<span data-ttu-id="ac3e5-109">Чтобы запустить симулятор трассировки тактов со счетчиком операций-примитивов, необходимо создать <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> экземпляр, присвоить `UsePrimitiveOperationsCounter` свойству **значение true** , а затем создать новый <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> экземпляр с `QCTraceSimulatorConfiguration` параметром в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="ac3e5-109">To run the quantum trace simulator with the primitive operation counter, you must create a <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instance, set the `UsePrimitiveOperationsCounter` property to **true** , and then create a new <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instance with the `QCTraceSimulatorConfiguration` as the parameter.</span></span>

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UsePrimitiveOperationsCounter = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-primitive-operation-counter-in-a-c-host-program"></a><span data-ttu-id="ac3e5-110">Использование счетчика примитивных операций в основной программе C#</span><span class="sxs-lookup"><span data-stu-id="ac3e5-110">Using the primitive operation counter in a C# host program</span></span>

<span data-ttu-id="ac3e5-111">В примере C#, приведенном в этом разделе, подсчитывается количество <xref:Microsoft.Quantum.Intrinsic.T> операций, необходимых для реализации <xref:Microsoft.Quantum.Intrinsic.ccnot> операции, на основе следующего :::no-loc(Q#)::: примера кода:</span><span class="sxs-lookup"><span data-stu-id="ac3e5-111">The C# example that follows in this section counts how many <xref:Microsoft.Quantum.Intrinsic.T> operations are needed to implement the <xref:Microsoft.Quantum.Intrinsic.ccnot> operation, based on the following :::no-loc(Q#)::: sample code:</span></span>

```qsharp
open Microsoft.Quantum.Intrinsic;
operation ApplySampleWithCCNOT() : Unit {

    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    }
}
```

<span data-ttu-id="ac3e5-112">Чтобы проверить, `CCNOT` требуется ли семь `T` операций и которые `ApplySampleWithCCNOT` выполняют восемь `T` операций, используйте следующий код C#:</span><span class="sxs-lookup"><span data-stu-id="ac3e5-112">To check that `CCNOT` requires seven `T` operations and that `ApplySampleWithCCNOT` runs eight `T` operations, use the following C# code:</span></span>

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

<span data-ttu-id="ac3e5-113">Запускается первая часть программы `ApplySampleWithCCNOT` .</span><span class="sxs-lookup"><span data-stu-id="ac3e5-113">The first part of the program runs `ApplySampleWithCCNOT`.</span></span> <span data-ttu-id="ac3e5-114">Во второй части используется [`QCTraceSimulator.GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) метод для получения количества `T` операций, выполняемых `ApplySampleWithCCNOT` :</span><span class="sxs-lookup"><span data-stu-id="ac3e5-114">The second part uses the [`QCTraceSimulator.GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) method to retrieve the number of `T` operations run by `ApplySampleWithCCNOT`:</span></span> 

<span data-ttu-id="ac3e5-115">При вызове `GetMetric` с двумя параметрами типа он возвращает значение метрики, связанной с данным ребром графа вызовов.</span><span class="sxs-lookup"><span data-stu-id="ac3e5-115">When you call `GetMetric` with two type parameters, it returns the value of the metric associated with a given call graph edge.</span></span> <span data-ttu-id="ac3e5-116">В предыдущем примере программа вызывает `Primitive.CCNOT` операцию в `ApplySampleWithCCNOT` и, следовательно, граф вызовов содержит ребро `<Primitive.CCNOT, ApplySampleWithCCNOT>` .</span><span class="sxs-lookup"><span data-stu-id="ac3e5-116">In the preceding example, the program calls the `Primitive.CCNOT` operation  within `ApplySampleWithCCNOT` and therefore the call graph contains the edge `<Primitive.CCNOT, ApplySampleWithCCNOT>`.</span></span> 

<span data-ttu-id="ac3e5-117">Чтобы получить количество `CNOT` используемых операций, добавьте следующую строку:</span><span class="sxs-lookup"><span data-stu-id="ac3e5-117">To retrieve the number of `CNOT` operations used, add the following line:</span></span>
```csharp
double cxCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.CX);
```

<span data-ttu-id="ac3e5-118">Наконец, можно вывести всю статистику, собранную счетчиком примитивных операций в формате CSV, с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="ac3e5-118">Finally, you can output all the statistics collected by the Primitive Operations Counter in CSV format using the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.primitiveOperationsCounter];
```

## <a name="see-also"></a><span data-ttu-id="ac3e5-119">См. также статью</span><span class="sxs-lookup"><span data-stu-id="ac3e5-119">See also</span></span>

- <span data-ttu-id="ac3e5-120">Обзор [имитатора трассировки такта](xref:microsoft.quantum.machines.qc-trace-simulator.intro) в пакете разработки тактов.</span><span class="sxs-lookup"><span data-stu-id="ac3e5-120">The Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
- <span data-ttu-id="ac3e5-121"><xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator>Справочник по API.</span><span class="sxs-lookup"><span data-stu-id="ac3e5-121">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API reference.</span></span>
- <span data-ttu-id="ac3e5-122"><xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>Справочник по API.</span><span class="sxs-lookup"><span data-stu-id="ac3e5-122">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API reference.</span></span>
- <span data-ttu-id="ac3e5-123"><xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.PrimitiveOperationsGroupsNames>Справочник по API.</span><span class="sxs-lookup"><span data-stu-id="ac3e5-123">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.PrimitiveOperationsGroupsNames> API reference.</span></span>