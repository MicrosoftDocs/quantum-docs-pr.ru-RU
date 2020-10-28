---
title: Счетчик примитивных операций — пакет средств разработки тактов
description: Сведения о счетчике примитивных операций Microsoft КДК, который использует симулятор трассировки тактов для отслеживания простых процессов, используемых операциями в Q# программе.
author: vadym-kl
ms.author: vadym
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.primitive-counter
no-loc:
- Q#
- $$v
ms.openlocfilehash: bf75eb94696a489a587316928bc3f33baa4a1785
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92690948"
---
# <a name="quantum-trace-simulator-primitive-operations-counter"></a>Симулятор трассировки тактов: Счетчик примитивных операций

Счетчик операции примитива является частью [имитатора тактовой трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro)пакета разработки тактов. Он подсчитывает количество простых процессов, используемых каждой операцией, вызванной в тактовой программе. 

Все <xref:Microsoft.Quantum.Intrinsic> операции выражаются с точки зрения однокубитного вращения, T Operations, кубит Клиффорд Operations, кнот операций и измерений Multi-кубит Паули observable. Счетчик примитивных операций выполняет статистическую обработку и собирает статистические данные по всем краям [графа вызовов](https://en.wikipedia.org/wiki/Call_graph)операции.

## <a name="invoking-the-primitive-operation-counter"></a>Вызов счетчика примитивной операции

Чтобы запустить симулятор трассировки тактов со счетчиком операций-примитивов, необходимо создать <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> экземпляр, присвоить `UsePrimitiveOperationsCounter` свойству **значение true** , а затем создать новый <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> экземпляр с `QCTraceSimulatorConfiguration` параметром в качестве параметра.

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UsePrimitiveOperationsCounter = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-primitive-operation-counter-in-a-c-host-program"></a>Использование счетчика примитивных операций в основной программе C#

В примере C#, приведенном в этом разделе, подсчитывается количество <xref:Microsoft.Quantum.Intrinsic.T> операций, необходимых для реализации <xref:Microsoft.Quantum.Intrinsic.ccnot> операции, на основе следующего Q# примера кода:

```qsharp
open Microsoft.Quantum.Intrinsic;
operation ApplySampleWithCCNOT() : Unit {

    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    }
}
```

Чтобы проверить, `CCNOT` требуется ли семь `T` операций и которые `ApplySampleWithCCNOT` выполняют восемь `T` операций, используйте следующий код C#:

```csharp 
// using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
// using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.UsePrimitiveOperationsCounter = true;
var sim = new QCTraceSimulator(config);
var res = ApplySampleWithCCNOT.Run(sim).Result;

double tCountAll = sim.GetMetric<ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
double tCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
```

Запускается первая часть программы `ApplySampleWithCCNOT` . Во второй части используется [`QCTraceSimulator.GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) метод для получения количества `T` операций, выполняемых `ApplySampleWithCCNOT` : 

При вызове `GetMetric` с двумя параметрами типа он возвращает значение метрики, связанной с данным ребром графа вызовов. В предыдущем примере программа вызывает `Primitive.CCNOT` операцию в `ApplySampleWithCCNOT` и, следовательно, граф вызовов содержит ребро `<Primitive.CCNOT, ApplySampleWithCCNOT>` . 

Чтобы получить количество `CNOT` используемых операций, добавьте следующую строку:
```csharp
double cxCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.CX);
```

Наконец, можно вывести всю статистику, собранную счетчиком примитивных операций в формате CSV, с помощью следующей команды:
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.primitiveOperationsCounter];
```

## <a name="see-also"></a>См. также статью

- Обзор [имитатора трассировки такта](xref:microsoft.quantum.machines.qc-trace-simulator.intro) в пакете разработки тактов.
- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator>Справочник по API.
- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>Справочник по API.
- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.PrimitiveOperationsGroupsNames>Справочник по API.