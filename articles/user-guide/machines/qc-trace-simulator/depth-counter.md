---
title: Счетчик глубины — пакет разработки тактов
description: Узнайте о счетчике Microsoft КДК Depth, который использует симулятор трассировки тактов для сбора данных о глубине каждой операции, вызванной в Q# программе.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.depth-counter
no-loc:
- Q#
- $$v
ms.openlocfilehash: 5c54f6fc479203d30c68c4958329605d4323f9ea
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868327"
---
# <a name="quantum-trace-simulator-depth-counter"></a>Симулятор тактовой трассировки: счетчик глубины

Счетчик глубины является частью [имитатора тактовой трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro)пакета разработки тактов.
Его можно использовать для сбора счетчиков, представляющих нижнюю границу глубины каждой операции, вызванной в тактовой программе. 

## <a name="depth-values"></a>Значения глубины

По умолчанию все операции имеют глубину **0** , за исключением `T` операции с глубиной **1**. Это означает, что по умолчанию `T` вычисляются только глубина операций (что часто желательно). Счетчик глубины выполняет статистическую обработку и собирает статистические данные по всем краям [графа вызовов](https://en.wikipedia.org/wiki/Call_graph)операции.

Все <xref:microsoft.quantum.intrinsic> операции выражаются с точки зрения однокубитных поворотов, <xref:microsoft.quantum.intrinsic.t> операций, операций с одной кубит Клиффорд операции, <xref:microsoft.quantum.intrinsic.cnot> операций и измерений множества кубит Паули observable. Пользователи могут задать глубину для каждой из примитивных операций с помощью `gateTimes` поля <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> .

## <a name="invoking-the-depth-counter"></a>Вызов счетчика глубины

Чтобы запустить симулятор трассировки тактов с счетчиком глубины, необходимо создать <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> экземпляр, присвоить его `UseDepthCounter` свойству **значение true**, а затем создать новый <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> экземпляр с `QCTraceSimulatorConfiguration` параметром в качестве параметра. 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseDepthCounter = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-depth-counter-in-a-c-host-program"></a>Использование счетчика глубины в основной программе C#

В примере C#, приведенном ниже в этом разделе, выполняется вычисление `T` глубины `CCNOT` операции на основе следующего Q# примера кода:

```qsharp
open Microsoft.Quantum.Intrinsic;

operation ApplySampleWithCCNOT() : Unit {
    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    }
}
```

Чтобы проверить, что `CCNOT` имеет `T` глубину **5** и `ApplySampleWithCCNOT` имеет `T` глубину **6**, используйте следующий код C#:

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

Запускается первая часть программы `ApplySampleWithCCNOT` . Во второй части используется [`GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) метод для получения `T` глубины `CCNOT` и `ApplySampleWithCCNOT` . 

Наконец, можно вывести всю статистику, собранную счетчиком глубины в формате CSV, с помощью следующей команды:
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.depthCounter];
```

## <a name="see-also"></a>См. также

- Обзор [имитатора трассировки такта](xref:microsoft.quantum.machines.qc-trace-simulator.intro) в пакете разработки тактов.
- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator>Справочник по API.
- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>Справочник по API.
- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.MetricsNames.DepthCounter>Справочник по API.
