---
title: Счетчик глубины
description: Узнайте о счетчике Microsoft КДК Depth, который собирает количество всех операций, вызванных в тактовой программе.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.depth-counter
ms.openlocfilehash: d532a9f512b8c87d83d62ed26e3bb67e1b6f668b
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/28/2020
ms.locfileid: "77906106"
---
# <a name="depth-counter"></a>Счетчик глубины

`Depth Counter` является частью [симулятора трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro)компьютерных тактов.
Он используется для сбора данных о глубине каждой операции, вызванной в тактовой программе. Все операции от <xref:microsoft.quantum.intrinsic> выражаются в виде кубитных поворотов, T-шлюзов, одного кубит Клиффорд Gates, кнот шлюзов и измерений многокубит Паули observable. Пользователи могут задать глубину для каждой из примитивных операций с помощью `gateTimes` поля <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>.

По умолчанию все операции имеют глубину 0, кроме шлюза T, имеющего глубину 1. Это означает, что вычисление производится только по умолчанию (что часто желательно). Собранные статистические данные суммируются по всем краям графа вызовов операций. 

Теперь давайте вычислим глубину <xref:microsoft.quantum.intrinsic.t> <xref:microsoft.quantum.intrinsic.ccnot> операции. Мы будем использовать следующий пример кода Q #:

```qsharp
open Microsoft.Quantum.Intrinsic;

operation ApplySampleWithCCNOT() : Unit {
    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    }
}
```

## <a name="using-depth-counter-within-a-c-program"></a>Использование счетчика глубины в C# программе

Чтобы проверить, имеет ли `CCNOT` `T` глубины 5, а `ApplySampleWithCCNOT` имеет `T` глубину 6, можно C# использовать следующий код:

```csharp
using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.useDepthCounter = true;
var sim = new QCTraceSimulator(config);
var res = ApplySampleWithCCNOT.Run(sim).Result;

double tDepth = sim.GetMetric<Intrinsic.CCNOT, ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
double tDepthAll = sim.GetMetric<ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
```

Первая часть программы выполняет `ApplySampleWithCCNOT`. Во второй части мы используем метод `QCTraceSimulator.GetMetric` для получения `T` глубины `CCNOT` и `ApplySampleWithCCNOT`: 

```csharp
double tDepth = sim.GetMetric<Intrinsic.CCNOT, ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
double tDepthAll = sim.GetMetric<ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
```

Наконец, чтобы вывести всю статистику, собранную `Depth Counter` в формате CSV, можно использовать следующее:
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.depthCounter];
```

## <a name="see-also"></a>См. также раздел ##

- Обзор [имитатора трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro) компьютерных тактов.
