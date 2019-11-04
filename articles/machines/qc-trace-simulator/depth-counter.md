---
title: Счетчик глубины | Симулятор трассировки компьютерных тактов | Документация Майкрософт
description: Обзор имитатора трассировки тактов компьютера
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.depth-counter
ms.openlocfilehash: f5fcaa64e91290d377eeba597df2e307e187277c
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/29/2019
ms.locfileid: "73184905"
---
# <a name="depth-counter"></a><span data-ttu-id="9ff1b-103">Счетчик глубины</span><span class="sxs-lookup"><span data-stu-id="9ff1b-103">Depth Counter</span></span>

<span data-ttu-id="9ff1b-104">`Depth Counter` является частью [симулятора трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro)компьютерных тактов.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-104">The `Depth Counter` is a part of the quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span>
<span data-ttu-id="9ff1b-105">Он используется для сбора данных о глубине каждой операции, вызванной в тактовой программе.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-105">It is used to gather counts of the depth of every operation invoked in a quantum program.</span></span> <span data-ttu-id="9ff1b-106">Все операции от <xref:microsoft.quantum.intrinsic> выражаются в виде кубитных поворотов, T-шлюзов, одного кубит Клиффорд Gates, кнот шлюзов и измерений многокубит Паули observable.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-106">All operations from <xref:microsoft.quantum.intrinsic> are expressed in terms of single qubit rotations, T gates, single qubit Clifford gates, CNOT gates and measurements of multi-qubit Pauli observables.</span></span> <span data-ttu-id="9ff1b-107">Пользователи могут задать глубину для каждой из примитивных операций с помощью `gateTimes` поля <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-107">Users can set the depth for each of the primitive operations via the `gateTimes` field of <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>.</span></span>

<span data-ttu-id="9ff1b-108">По умолчанию все операции имеют глубину 0, кроме шлюза T, имеющего глубину 1.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-108">By default, all operations have depth 0 except the T gate which has depth 1.</span></span> <span data-ttu-id="9ff1b-109">Это означает, что вычисление производится только по умолчанию (что часто желательно).</span><span class="sxs-lookup"><span data-stu-id="9ff1b-109">This means that by default, only the T depth of operations is computed (which is often desirable).</span></span> <span data-ttu-id="9ff1b-110">Собранные статистические данные суммируются по всем краям графа вызовов операций.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-110">Collected statistics are aggregated over all the edges of the operations call graph.</span></span> 

<span data-ttu-id="9ff1b-111">Теперь давайте вычислим глубину <xref:microsoft.quantum.intrinsic.t> <xref:microsoft.quantum.intrinsic.ccnot> операции.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-111">Let us now compute the <xref:microsoft.quantum.intrinsic.t> depth of the <xref:microsoft.quantum.intrinsic.ccnot> operation.</span></span> <span data-ttu-id="9ff1b-112">Мы будем использовать следующий код драйвера Q #:</span><span class="sxs-lookup"><span data-stu-id="9ff1b-112">We will use the following Q# driver code:</span></span> 

```qsharp
open Microsoft.Quantum.Primitive;
operation CCNOTDriver() : Unit {

    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    }
}
```

## <a name="using-depth-counter-within-a-c-program"></a><span data-ttu-id="9ff1b-113">Использование счетчика глубины в C# программе</span><span class="sxs-lookup"><span data-stu-id="9ff1b-113">Using Depth Counter within a C# Program</span></span>

<span data-ttu-id="9ff1b-114">Чтобы проверить, имеет ли `CCNOT` `T` глубины 5, а `CCNOTDriver` имеет `T` глубину 6, можно C# использовать следующий код:</span><span class="sxs-lookup"><span data-stu-id="9ff1b-114">To check that `CCNOT` has `T` depth 5 and `CCNOTDriver` has `T` depth 6 we can use the following C# code:</span></span>

```csharp 
using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.useDepthCounter = true;
var sim = new QCTraceSimulator(config);
var res = CCNOTDriver.Run(sim).Result;

double tDepth = sim.GetMetric<Primitive.CCNOT, CCNOTDriver>(DepthCounter.Metrics.Depth);
double tDepthAll = sim.GetMetric<CCNOTDriver>(DepthCounter.Metrics.Depth);
```

<span data-ttu-id="9ff1b-115">Первая часть программы выполняет `CCNOTDriver`.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-115">The first part of the program executes `CCNOTDriver`.</span></span> <span data-ttu-id="9ff1b-116">Во второй части мы используем метод `QCTraceSimulator.GetMetric` для получения `T` глубины `CCNOT` и `CCNOTDriver`:</span><span class="sxs-lookup"><span data-stu-id="9ff1b-116">In the second part, we use the method `QCTraceSimulator.GetMetric` to get the `T` depth of `CCNOT` and `CCNOTDriver`:</span></span> 

```csharp
double tDepth = sim.GetMetric<Primitive.CCNOT, CCNOTDriver>(DepthCounter.Metrics.Depth);
double tDepthAll = sim.GetMetric<CCNOTDriver>(DepthCounter.Metrics.Depth);
```

<span data-ttu-id="9ff1b-117">Наконец, чтобы вывести всю статистику, собранную `Depth Counter` в формате CSV, можно использовать следующее:</span><span class="sxs-lookup"><span data-stu-id="9ff1b-117">Finally, to output all the statistics collected by `Depth Counter` in CSV format we can use the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.depthCounter];
```

## <a name="see-also"></a><span data-ttu-id="9ff1b-118">Дополнительные материалы</span><span class="sxs-lookup"><span data-stu-id="9ff1b-118">See also</span></span> ##

- <span data-ttu-id="9ff1b-119">Обзор [имитатора трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro) компьютерных тактов.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-119">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
