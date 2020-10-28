---
title: Счетчик ширины — пакет разработки тактов
description: Сведения о счетчике ширины Microsoft КДК, который использует симулятор трассировки тактов для подсчета количества Кубитс, выделенных и заимствованных операциями в Q# программе.
author: vadym-kl
ms.author: vadym
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.width-counter
no-loc:
- Q#
- $$v
ms.openlocfilehash: e54e92cc4a76ce9f9c5aead84f2b64320d6b4f1c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92691127"
---
# <a name="quantum-trace-simulator-width-counter"></a>Симулятор тактовой трассировки: Счетчик ширины

Счетчик ширины является частью [имитатора тактовой трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro)пакета разработки тактов. Его можно использовать для подсчета количества Кубитс, выделенных и заимствованных каждой операцией в Q# программе. Некоторые примитивные операции могут выделять дополнительные Кубитс, например, умножение управляемых `X` операций или контролируемых `T` операций.

## <a name="invoking-the-width-counter"></a>Вызов счетчика ширины

Чтобы запустить симулятор трассировки тактов с счетчиком Width, необходимо создать <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> экземпляр, установить `UseWidthCounter` свойство в **значение true** , а затем создать новый <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> экземпляр с `QCTraceSimulatorConfiguration` параметром в качестве параметра. 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseWidthCounter = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-width-counter-in-a-c-host-program"></a>Использование счетчика ширины в управляющей программе C#

В примере C#, приведенном ниже в этом разделе, вычисляется количество дополнительных Кубитс, выделенных реализацией операции умножения <xref:Microsoft.Quantum.Intrinsic.X> , на основе следующего Q# примера кода:

```qsharp
open Microsoft.Quantum.Intrinsic;
open Microsoft.Quantum.Arrays;
operation ApplyMultiControlledX( numberOfQubits : Int ) : Unit {
    using(qubits = Qubit[numberOfQubits]) {
        Controlled X (Rest(qubits), Head(qubits));
    } 
}
```

Операция умножения выполняется <xref:Microsoft.Quantum.Intrinsic.X> для всего пяти Кубитс, выделяет два [вспомогательных Кубитс](xref:microsoft.quantum.glossary#ancilla)и имеет ширину ввода **5** . Используйте следующую программу C# для проверки счетчиков:

```csharp 
var config = new QCTraceSimulatorConfiguration();
config.UseWidthCounter = true;
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

Первая часть программы выполняет `ApplyMultiControlledX` операцию. Во второй части используется [`QCTraceSimulator.GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) метод для получения количества выделенных Кубитс, а также количества Кубитс, которые `Controlled X` операция получает в качестве входных данных. 

Наконец, можно вывести всю статистику, собранную счетчиком ширины, в формате CSV, используя следующую команду:
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.widthCounter];
```

## <a name="see-also"></a>См. также статью

- Обзор [имитатора трассировки такта](xref:microsoft.quantum.machines.qc-trace-simulator.intro) в пакете разработки тактов.
- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator>Справочник по API.
- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>Справочник по API.
- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.MetricsNames.WidthCounter>Справочник по API.
