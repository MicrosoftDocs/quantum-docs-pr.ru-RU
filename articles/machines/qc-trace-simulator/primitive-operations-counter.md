---
title: Счетчик примитивных операций
description: Сведения о счетчике Microsoft КДК-примитивных операций, который отслеживает количество простых выполнений, используемых операциями в тактовой программе.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.primitive-counter
ms.openlocfilehash: 8bdb0aed370e72b58b23025f1685ad7ce1a77a43
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/28/2020
ms.locfileid: "77905953"
---
# <a name="primitive-operations-counter"></a>Счетчик примитивных операций  

`Primitive Operations Counter` является частью [симулятора трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro)компьютерных тактов. Он подсчитывает количество простых выполнений, используемых каждой операцией, вызванной в тактовой программе. Все операции от `Microsoft.Quantum.Intrinsic` выражаются в виде кубитных поворотов, T-шлюзов, одного кубит Клиффорд Gates, кнот шлюзов и измерений многокубит Паули observable. Собранные статистические данные суммируются по краям графа вызовов операций. Теперь давайте подсчитани количество `T` шлюзов, необходимых для реализации операции `CCNOT`. 

```qsharp
open Microsoft.Quantum.Intrinsic;
operation ApplySampleWithCCNOT() : Unit {

    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    } 
}
```

## <a name="using-the-primitive-operations-counter-within-a-c-program"></a>Использование счетчика примитивных операций в C# программе

Чтобы убедиться, что `CCNOT` действительно требуется 7 `T` шлюзов и что `ApplySampleWithCCNOT` выполняет 8 `T` шлюзов, можно использовать следующий C# код:

```csharp 
// using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
// using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.usePrimitiveOperationsCounter = true;
var sim = new QCTraceSimulator(config);
var res = ApplySampleWithCCNOT.Run(sim).Result;

double tCountAll = sim.GetMetric<ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
double tCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
```

Первая часть программы выполняет `ApplySampleWithCCNOT`. Во второй части мы используем метод `QCTraceSimulator.GetMetric` для получения числа T Gates, выполняемых `ApplySampleWithCCNOT`: 

```csharp
double tCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
double tCountAll = sim.GetMetric<ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
```

При вызове `GetMetric` с двумя параметрами типа он возвращает значение метрики, связанной с данным ребром графа вызовов. В нашем примере операции `Primitive.CCNOT` вызывается в `ApplySampleWithCCNOT` и, следовательно, граф вызовов содержит `<Primitive.CCNOT, ApplySampleWithCCNOT>`ребра. 

Чтобы узнать количество используемых шлюзов `CNOT`, можно добавить следующую строку:
```csharp
double cxCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.CX);
```

Наконец, чтобы вывести всю статистику, собранную счетчиком шлюзов в формате CSV, можно использовать следующее:
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.primitiveOperationsCounter];
```

## <a name="see-also"></a>См. также раздел ##

- Обзор [имитатора трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro) компьютерных тактов.
