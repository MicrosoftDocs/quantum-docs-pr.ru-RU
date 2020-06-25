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
# <a name="width-counter"></a>Счетчик ширины

`Width Counter`Подсчитывает количество Кубитс, выделенных и заимствованных каждой операцией.
Все операции из `Microsoft.Quantum.Intrinsic` пространства имен выражаются в виде однокубитных поворотов, T-шлюзов, одного кубит Клиффорд Gates, ШЛЮЗОВ кнот и измерений Multi-кубит Паули observable. Некоторые примитивные операции могут выделить дополнительные Кубитс. Например, перемножьте контролируемые `X` шлюзы или контролируемые `T` шлюзы. Давайте вычислим количество дополнительных Кубитс, выделенных реализацией шлюза, управляемого умножением `X` :

```qsharp
open Microsoft.Quantum.Intrinsic;
open Microsoft.Quantum.Arrays;
operation ApplyMultiControlledX( numberOfQubits : Int ) : Unit {
    using(qubits = Qubit[numberOfQubits]) {
        Controlled X (Rest(qubits), Head(qubits));
    } 
}
```

## <a name="using-width-counter-within-a-c-program"></a>Использование счетчика ширины в программе C#

Умножение `X` на 5 Кубитс выделит 2 дополнительных Кубитс, и его входная ширина будет равна 5. Чтобы убедиться, что это так, можно использовать следующую программу C#:

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

Выполняется первая часть программы `ApplyMultiControlledX` . Во второй части мы используем метод, `QCTraceSimulator.GetMetric` чтобы получить количество выделенных Кубитс, а также число Кубитс, контролируемых `X` в качестве входных данных. 

Наконец, чтобы вывести всю статистику, собранную счетчиком ширины, в формате CSV, можно использовать следующее:
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.widthCounter];
```

## <a name="see-also"></a>См. также ##

- Обзор [имитатора трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro) компьютерных тактов.
