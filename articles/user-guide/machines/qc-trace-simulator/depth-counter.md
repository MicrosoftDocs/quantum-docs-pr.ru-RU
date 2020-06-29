---
title: Счетчик глубины
description: Узнайте о счетчике Microsoft КДК Depth, который собирает количество всех операций, вызванных в тактовой программе.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.depth-counter
ms.openlocfilehash: 0029a00e6a3563dc542daeda2afa7cabf42441fb
ms.sourcegitcommit: af10179284967bd7a72a52ae7e1c4da65c7d128d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "85415274"
---
# <a name="depth-counter"></a>Счетчик глубины

`Depth Counter`Компонент является частью [имитатора трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro)компьютерных тактов.
Он используется для сбора счетчиков, представляющих нижнюю границу глубины каждой операции, вызванной в тактовой программе. Все операции из <xref:microsoft.quantum.intrinsic> выражаются в виде однокубитных поворотов, T-шлюзов, одного кубит Клиффорд Гейтсов, шлюзов кнот и измерений Multi-кубит Паули observable. Пользователи могут задать глубину для каждой из примитивных операций с помощью `gateTimes` поля <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> .

По умолчанию все операции имеют глубину 0, кроме шлюза T, имеющего глубину 1. Это означает, что вычисление производится только по умолчанию (что часто желательно). Собранные статистические данные суммируются по всем краям графа вызовов операций. 

Теперь мы вычислим <xref:microsoft.quantum.intrinsic.t> глубину <xref:microsoft.quantum.intrinsic.ccnot> операции. Мы будем использовать следующий пример кода Q #:

```qsharp
open Microsoft.Quantum.Intrinsic;

operation ApplySampleWithCCNOT() : Unit {
    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    }
}
```

## <a name="using-depth-counter-within-a-c-program"></a>Использование счетчика глубины в программе C#

Чтобы проверить, что `CCNOT` имеет `T` глубину 5 и `ApplySampleWithCCNOT` имеет `T` глубину 6, мы можем использовать следующий код C#:

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

Выполняется первая часть программы `ApplySampleWithCCNOT` . Во второй части мы используем метод `QCTraceSimulator.GetMetric` для получения `T` глубины `CCNOT` и `ApplySampleWithCCNOT` : 

```csharp
double tDepth = sim.GetMetric<Intrinsic.CCNOT, ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
double tDepthAll = sim.GetMetric<ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
```

Наконец, чтобы вывести всю статистику, собранную `Depth Counter` в формате CSV, можно использовать следующую команду:
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.depthCounter];
```

## <a name="see-also"></a>См. также ##

- Обзор [имитатора трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro) компьютерных тактов.
