---
title: Счетчик ширины | Симулятор трассировки компьютерных тактов | Документация Майкрософт
description: Обзор симулятора трассировки квантового компьютера
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.width-counter
ms.openlocfilehash: ae0c0ec2e677be03dc8dc1497dc62ad9034295a4
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2019
ms.locfileid: "73442409"
---
# <a name="width-counter"></a>Счетчик ширины

`Width Counter` подсчитывает количество Кубитс, выделенных и заимствованных каждой операцией.
Все операции из пространства имен `Microsoft.Quantum.Primitive` выражены в виде однокубитных поворотов, T-шлюзов, одного кубит Клиффорд Гейтсов, шлюзов кнот и измерений Multi-кубит Паули observable. Некоторые примитивные операции могут выделить дополнительные Кубитс. Например, умножьте управляемый `X` Gates или контролируемый `T` Гейтс. Давайте вычислим количество дополнительных Кубитс, выделенных реализацией многофакторного `X` вентиля:

```qsharp
open Microsoft.Quantum.Primitive;
open Microsoft.Quantum.Arrays;
operation MultiControlledXDriver( numberOfQubits : Int ) : Unit {

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
var res = MultiControlledXDriver.Run(sim, totalNumberOfQubits).Result;

double allocatedQubits = 
    sim.GetMetric<Primitive.X, MultiControlledXDriver>(
        WidthCounter.Metrics.ExtraWidth,
        functor: OperationFunctor.Controlled); 

double inputWidth =
    sim.GetMetric<Primitive.X, MultiControlledXDriver>(
        WidthCounter.Metrics.InputWidth,
        functor: OperationFunctor.Controlled);
```

Первая часть программы выполняет `MultiControlledXDriver`. Во второй части мы используем метод `QCTraceSimulator.GetMetric`, чтобы получить количество выделенных Кубитс, а также число Кубитс, которые управляются `X` получения в качестве входных данных. 

Наконец, чтобы вывести всю статистику, собранную счетчиком ширины, в формате CSV, можно использовать следующее:
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.widthCounter];
```

## <a name="see-also"></a>Дополнительные материалы ##

- Обзор [имитатора трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro) компьютерных тактов.
