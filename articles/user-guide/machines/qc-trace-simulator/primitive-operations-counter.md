---
title: Счетчик примитивных операций
description: Сведения о счетчике Microsoft КДК-примитивных операций, который отслеживает количество простых выполнений, используемых операциями в тактовой программе.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.primitive-counter
ms.openlocfilehash: 8bdb0aed370e72b58b23025f1685ad7ce1a77a43
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275555"
---
# <a name="primitive-operations-counter"></a>Счетчик примитивных операций  

`Primitive Operations Counter`Компонент является частью [имитатора трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro)компьютерных тактов. Он подсчитывает количество простых выполнений, используемых каждой операцией, вызванной в тактовой программе. Все операции из `Microsoft.Quantum.Intrinsic` выражаются в виде однокубитных поворотов, T-шлюзов, одного кубит Клиффорд Гейтсов, шлюзов кнот и измерений Multi-кубит Паули observable. Собранные статистические данные суммируются по краям графа вызовов операций. Теперь давайте подсчитани количество `T` шлюзов, необходимых для реализации `CCNOT` операции. 

```qsharp
open Microsoft.Quantum.Intrinsic;
operation ApplySampleWithCCNOT() : Unit {

    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    } 
}
```

## <a name="using-the-primitive-operations-counter-within-a-c-program"></a>Использование счетчика примитивных операций в программе C#

Чтобы убедиться, что в `CCNOT` действительно требуется 7 `T` шлюзов и `ApplySampleWithCCNOT` выполняется 8 `T` шлюзов, можно использовать следующий код C#:

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

Выполняется первая часть программы `ApplySampleWithCCNOT` . Во второй части мы используем метод `QCTraceSimulator.GetMetric` для получения числа T Gates, выполненных `ApplySampleWithCCNOT` : 

```csharp
double tCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
double tCountAll = sim.GetMetric<ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
```

Когда `GetMetric` вызывается с двумя параметрами типа, он возвращает значение метрики, связанной с данным ребром графа вызова. В нашем примере операции `Primitive.CCNOT` вызывается внутри `ApplySampleWithCCNOT` и, следовательно, граф вызовов содержит ребро `<Primitive.CCNOT, ApplySampleWithCCNOT>` . 

Чтобы получить количество `CNOT` используемых шлюзов, можно добавить следующую строку:
```csharp
double cxCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.CX);
```

Наконец, чтобы вывести всю статистику, собранную счетчиком шлюзов в формате CSV, можно использовать следующее:
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.primitiveOperationsCounter];
```

## <a name="see-also"></a>См. также ##

- Обзор [имитатора трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro) компьютерных тактов.
