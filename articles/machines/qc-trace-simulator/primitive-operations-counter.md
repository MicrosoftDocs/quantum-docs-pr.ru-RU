---
title: Счетчик примитивных операций | Симулятор трассировки компьютерных тактов | Документация Майкрософт
description: Обзор имитатора трассировки тактов компьютера
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.primitive-counter
ms.openlocfilehash: b7ec8b0d7a713051e36cb778c087050f0257710f
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/29/2019
ms.locfileid: "73184888"
---
# <a name="primitive-operations-counter"></a>Счетчик примитивных операций  

`Primitive Operations Counter` является частью [симулятора трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro)компьютерных тактов. Он подсчитывает количество простых выполнений, используемых каждой операцией, вызванной в тактовой программе. Все операции от `Microsoft.Quantum.Primitive` выражаются в виде кубитных поворотов, T-шлюзов, одного кубит Клиффорд Gates, кнот шлюзов и измерений многокубит Паули observable. Собранные статистические данные суммируются по краям графа вызовов операций. Теперь давайте подсчитани количество `T` шлюзов, необходимых для реализации операции `CCNOT`. 

```qsharp
open Microsoft.Quantum.Primitive;
operation CCNOTDriver() : Unit {

    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    } 
}
```

## <a name="using-the-primitive-operations-counter-within-a-c-program"></a>Использование счетчика примитивных операций в C# программе

Чтобы убедиться, что `CCNOT` действительно требуется 7 `T` шлюзов и что `CCNOTDriver` выполняет 8 `T` шлюзов, можно использовать следующий C# код:

```csharp 
// using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
// using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.usePrimitiveOperationsCounter = true;
var sim = new QCTraceSimulator(config);
var res = CCNOTDriver.Run(sim).Result;

double tCountAll = sim.GetMetric<CCNOTDriver>(PrimitiveOperationsGroupsNames.T);
double tCount = sim.GetMetric<Primitive.CCNOT, CCNOTDriver>(PrimitiveOperationsGroupsNames.T);
```

Первая часть программы выполняет `CCNOTDriver`. Во второй части мы используем метод `QCTraceSimulator.GetMetric` для получения числа T Gates, выполняемых `CCNOTDriver`: 

```csharp
double tCount = sim.GetMetric<Primitive.CCNOT, CCNOTDriver>(PrimitiveOperationsGroupsNames.T);
double tCountAll = sim.GetMetric<CCNOTDriver>(PrimitiveOperationsGroupsNames.T);
```

При вызове `GetMetric` с двумя параметрами типа он возвращает значение метрики, связанной с данным ребром графа вызовов. В нашем примере операции `Primitive.CCNOT` вызывается в `CCNOTDriver` и, следовательно, граф вызовов содержит `<Primitive.CCNOT,CCNOTDriver>`ребра. 

Чтобы узнать количество используемых шлюзов `CNOT`, можно добавить следующую строку:
```csharp
double cxCount = sim.GetMetric<Primitive.CCNOT, CCNOTDriver>(PrimitiveOperationsGroupsNames.CX);
```

Наконец, чтобы вывести всю статистику, собранную счетчиком шлюзов в формате CSV, можно использовать следующее:
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.primitiveOperationsCounter];
```

## <a name="see-also"></a>Дополнительные материалы ##

- Обзор [имитатора трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro) компьютерных тактов.
