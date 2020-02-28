---
title: Счетчик ширины
description: Сведения о счетчике ширины Microsoft КДК, который подсчитывает количество Кубитс, выделенных и заимствованных каждой операцией в тактовой программе.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.width-counter
ms.openlocfilehash: a76292222950310acc90dded02980e4a5b792e76
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907092"
---
# <a name="width-counter"></a>Счетчик ширины

`Width Counter` подсчитывает количество Кубитс, выделенных и заимствованных каждой операцией.
Все операции из пространства имен `Microsoft.Quantum.Intrinsic` выражены в виде однокубитных поворотов, T-шлюзов, одного кубит Клиффорд Гейтсов, шлюзов кнот и измерений Multi-кубит Паули observable. Некоторые примитивные операции могут выделить дополнительные Кубитс. Например, умножьте управляемый `X` Gates или контролируемый `T` Гейтс. Давайте вычислим количество дополнительных Кубитс, выделенных реализацией многофакторного `X` вентиля:

```qsharp
open Microsoft.Quantum.Intrinsic;
open Microsoft.Quantum.Arrays;
operation ApplyMultiControlledX( numberOfQubits : Int ) : Unit {
    using(qubits = Qubit[numberOfQubits]) {
        Controlled X (Rest(qubits), Head(qubits));
    } 
}
```

## <a name="using-width-counter-within-a-c-program"></a>Использование счетчика ширины в C# программе

Умножение управляемого `X`, действующего на сумму 5 Кубитс, выделит 2 дополнительных Кубитс, и его входная ширина будет равна 5. Чтобы убедиться, что это так, можно использовать следующую C# программу:

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

Первая часть программы выполняет `ApplyMultiControlledX`. Во второй части мы используем метод `QCTraceSimulator.GetMetric`, чтобы получить количество выделенных Кубитс, а также число Кубитс, которые управляются `X` получения в качестве входных данных. 

Наконец, чтобы вывести всю статистику, собранную счетчиком ширины, в формате CSV, можно использовать следующее:
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.widthCounter];
```

## <a name="see-also"></a>См. также раздел ##

- Обзор [имитатора трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro) компьютерных тактов.
