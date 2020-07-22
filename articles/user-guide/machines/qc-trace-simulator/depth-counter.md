---
title: Счетчик глубины — пакет разработки тактов
description: 'Узнайте о счетчике Microsoft КДК Depth, который использует симулятор трассировки тактов для сбора данных о глубине каждой операции, вызванной в программе Q #.'
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.depth-counter
ms.openlocfilehash: 811e387fedf547d2681518ae0bb525c13dc84ff4
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/21/2020
ms.locfileid: "86871133"
---
# <a name="quantum-trace-simulator-depth-counter"></a><span data-ttu-id="9b457-103">Симулятор тактовой трассировки: счетчик глубины</span><span class="sxs-lookup"><span data-stu-id="9b457-103">Quantum trace simulator: depth counter</span></span>

<span data-ttu-id="9b457-104">Счетчик глубины является частью [имитатора тактовой трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro)пакета разработки тактов.</span><span class="sxs-lookup"><span data-stu-id="9b457-104">The depth counter is a part of the Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span>
<span data-ttu-id="9b457-105">Его можно использовать для сбора счетчиков, представляющих нижнюю границу глубины каждой операции, вызванной в тактовой программе.</span><span class="sxs-lookup"><span data-stu-id="9b457-105">You can use it to gather counts that represent the lower bound of the depth of every operation invoked in a quantum program.</span></span> 

## <a name="depth-values"></a><span data-ttu-id="9b457-106">Значения глубины</span><span class="sxs-lookup"><span data-stu-id="9b457-106">Depth values</span></span>

<span data-ttu-id="9b457-107">По умолчанию все операции имеют глубину **0** , за исключением `T` операции с глубиной **1**.</span><span class="sxs-lookup"><span data-stu-id="9b457-107">By default, all operations have a depth of **0** except the `T` operation, which has a depth of **1**.</span></span> <span data-ttu-id="9b457-108">Это означает, что по умолчанию `T` вычисляются только глубина операций (что часто желательно).</span><span class="sxs-lookup"><span data-stu-id="9b457-108">This means that by default, only the `T` depth of operations is computed (which is often desirable).</span></span> <span data-ttu-id="9b457-109">Счетчик глубины выполняет статистическую обработку и собирает статистические данные по всем краям [графа вызовов](https://en.wikipedia.org/wiki/Call_graph)операции.</span><span class="sxs-lookup"><span data-stu-id="9b457-109">The depth counter aggregates and collects statistics over all the edges of the operation's [call graph](https://en.wikipedia.org/wiki/Call_graph).</span></span>

<span data-ttu-id="9b457-110">Все <xref:microsoft.quantum.intrinsic> операции выражаются с точки зрения однокубитных поворотов, <xref:microsoft.quantum.intrinsic.t> операций, операций с одной кубит Клиффорд операции, <xref:microsoft.quantum.intrinsic.cnot> операций и измерений множества кубит Паули observable.</span><span class="sxs-lookup"><span data-stu-id="9b457-110">All <xref:microsoft.quantum.intrinsic> operations are expressed in terms of single-qubit rotations, <xref:microsoft.quantum.intrinsic.t> operations, single-qubit Clifford operations, <xref:microsoft.quantum.intrinsic.cnot> operations, and measurements of multi-qubit Pauli observables.</span></span> <span data-ttu-id="9b457-111">Пользователи могут задать глубину для каждой из примитивных операций с помощью `gateTimes` поля <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> .</span><span class="sxs-lookup"><span data-stu-id="9b457-111">Users can set the depth for each of the primitive operations via the `gateTimes` field of <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>.</span></span>

## <a name="invoking-the-depth-counter"></a><span data-ttu-id="9b457-112">Вызов счетчика глубины</span><span class="sxs-lookup"><span data-stu-id="9b457-112">Invoking the depth counter</span></span>

<span data-ttu-id="9b457-113">Чтобы запустить симулятор трассировки тактов с счетчиком глубины, необходимо создать <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> экземпляр, присвоить его `UseDepthCounter` свойству **значение true**, а затем создать новый <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> экземпляр с `QCTraceSimulatorConfiguration` параметром в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="9b457-113">To run the quantum trace simulator with the depth counter, you must create a <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instance, set its `UseDepthCounter` property to **true**, and then create a new <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instance with `QCTraceSimulatorConfiguration` as the parameter.</span></span> 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseDepthCounter = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-depth-counter-in-a-c-host-program"></a><span data-ttu-id="9b457-114">Использование счетчика глубины в основной программе C#</span><span class="sxs-lookup"><span data-stu-id="9b457-114">Using the depth counter in a C# host program</span></span>

<span data-ttu-id="9b457-115">В примере C#, приведенном ниже в этом разделе, выполняется вычисление `T` глубины `CCNOT` операции на основе следующего примера кода Q #:</span><span class="sxs-lookup"><span data-stu-id="9b457-115">The C# example that follows in this section computes the `T` depth of the `CCNOT` operation, based on the following Q# sample code:</span></span>

```qsharp
open Microsoft.Quantum.Intrinsic;

operation ApplySampleWithCCNOT() : Unit {
    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    }
}
```

<span data-ttu-id="9b457-116">Чтобы проверить, что `CCNOT` имеет `T` глубину **5** и `ApplySampleWithCCNOT` имеет `T` глубину **6**, используйте следующий код C#:</span><span class="sxs-lookup"><span data-stu-id="9b457-116">To check that `CCNOT` has `T` depth **5** and `ApplySampleWithCCNOT` has `T` depth **6**, use the following C# code:</span></span>

```csharp
using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.UseDepthCounter = true;
var sim = new QCTraceSimulator(config);
var res = ApplySampleWithCCNOT.Run(sim).Result;

double tDepth = sim.GetMetric<Intrinsic.CCNOT, ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
double tDepthAll = sim.GetMetric<ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
```

<span data-ttu-id="9b457-117">Запускается первая часть программы `ApplySampleWithCCNOT` .</span><span class="sxs-lookup"><span data-stu-id="9b457-117">The first part of the program runs `ApplySampleWithCCNOT`.</span></span> <span data-ttu-id="9b457-118">Во второй части используется [`GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) метод для получения `T` глубины `CCNOT` и `ApplySampleWithCCNOT` .</span><span class="sxs-lookup"><span data-stu-id="9b457-118">The second part uses the [`GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) method to retrieve the `T` depth of `CCNOT` and `ApplySampleWithCCNOT`.</span></span> 

<span data-ttu-id="9b457-119">Наконец, можно вывести всю статистику, собранную счетчиком глубины в формате CSV, с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="9b457-119">Finally, you can output all the statistics collected by the depth counter in CSV format using the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.depthCounter];
```

## <a name="see-also"></a><span data-ttu-id="9b457-120">См. также статью</span><span class="sxs-lookup"><span data-stu-id="9b457-120">See also</span></span>

- <span data-ttu-id="9b457-121">Обзор [имитатора трассировки такта](xref:microsoft.quantum.machines.qc-trace-simulator.intro) в пакете разработки тактов.</span><span class="sxs-lookup"><span data-stu-id="9b457-121">The Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
- <span data-ttu-id="9b457-122"><xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator>Справочник по API.</span><span class="sxs-lookup"><span data-stu-id="9b457-122">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API reference.</span></span>
- <span data-ttu-id="9b457-123"><xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>Справочник по API.</span><span class="sxs-lookup"><span data-stu-id="9b457-123">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API reference.</span></span>
- <span data-ttu-id="9b457-124"><xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.MetricsNames.DepthCounter>Справочник по API.</span><span class="sxs-lookup"><span data-stu-id="9b457-124">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.MetricsNames.DepthCounter> API reference.</span></span>
