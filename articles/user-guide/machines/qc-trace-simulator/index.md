---
title: Квантовый симулятор трассировки — пакет средств разработки Quantum
description: Сведения о том, как с помощью симулятора трассировки квантового компьютера от Майкрософт выполнять отладку классического кода и оценивать требования к ресурсам для программы Q#.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.intro
no-loc:
- Q#
- $$v
ms.openlocfilehash: 5d5efef037ff236bd040dfd88e94f7f3dd331aef
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868225"
---
# <a name="microsoft-quantum-development-kit-qdk-quantum-trace-simulator"></a>Пакет средств разработки Microsoft Quantum (QDK) — квантовый симулятор трассировки

QDK <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> выполняет квантовую программу без фактической имитации состояния квантового компьютера. По этой причине квантовый симулятор трассировки может выполнять квантовые программы, использующие тысячи кубитов.  Это полезно для двух основных целей: 

* Отладка классического кода, который является частью квантовой программы. 
* Оценка ресурсов, необходимых для запуска заданного экземпляра квантовой программы на квантовом компьютере. [Оценщик ресурсов](xref:microsoft.quantum.machines.resources-estimator), который предоставляет более ограниченный набор метрик, создано на основе симулятора трассировки.

## <a name="invoking-the-quantum-trace-simulator"></a>Вызов квантового симулятора трассировки

Вы можете использовать квантовый симулятор трассировки для выполнения любой операции Q#.

Как и в случае с другими целевыми компьютерами, вам сначала нужно создать экземпляр класса `QCTraceSimulator`, а затем передать его в качестве первого параметра метода `Run` операции.

Учтите, что в отличие от класса `QuantumSimulator` класс `QCTraceSimulator` не реализует интерфейс <xref:System.IDisposable>, поэтому вам не нужно заключать его в оператор `using`.

```csharp
using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;
using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;

namespace Quantum.MyProgram
{
    class Driver
    {
        static void Main(string[] args)
        {
            QCTraceSimulator sim = new QCTraceSimulator();
            var res = MyQuantumProgram.Run(sim).Result;
            System.Console.WriteLine("Press any key to continue...");
            System.Console.ReadKey();
        }
    }
}
```

## <a name="providing-the-probability-of-measurement-outcomes"></a>Предоставление вероятности результатов измерения

Так как квантовый симулятор трассировки не имитирует фактическое квантовое состояние, он не может вычислить вероятность результатов измерения в операции. 

Таким образом, если операция включает измерения, необходимо явно предоставить эти вероятности с помощью операции <xref:microsoft.quantum.diagnostics.assertmeasurementprobability> из пространства имен <xref:microsoft.quantum.diagnostics>. Проиллюстрируем это на примере.

```qsharp
operation TeleportQubit(source : Qubit, target : Qubit) : Unit {
    using (qubit = Qubit()) {
        H(qubit);
        CNOT(qubit, target);
        CNOT(source, qubit);
        H(source);

        AssertMeasurementProbability([PauliZ], [source], Zero, 0.5, "Outcomes must be equally likely", 1e-5);
        AssertMeasurementProbability([PauliZ], [q], Zero, 0.5, "Outcomes must be equally likely", 1e-5);

        if (M(source) == One)  { Z(target); X(source); }
        if (M(q) == One) { X(target); X(q); }
    }
}
```

Когда квантовый симулятор трассировки вычисляет `AssertMeasurementProbability`, он записывает измерение `PauliZ` в `source`, и ожидается, что `q` выдаст результат `Zero` с вероятностью **0,5**. При выполнении операции `M` в дальнейшем он находит записанные значения вероятностей результата, и `M` возвращает `Zero` или `One` с вероятностью **0,5**. Если один и тот же код выполняется в симуляторе, который отслеживает квантовое состояние, такой симулятор проверяет правильность предоставленных вероятностей в `AssertMeasurementProbability`.

Учтите, что, если есть хотя бы одна операция измерения, не помеченная с помощью `AssertMeasurementProbability`, симулятор выдаст [`UnconstrainedMeasurementException`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.unconstrainedmeasurementexception).

## <a name="quantum-trace-simulator-tools"></a>Средства квантового симулятора трассировки

QDK включает пять средств, которые можно использовать с квантовым симулятором трассировки для обнаружения ошибок в программах и выполнения оценки ресурсов квантовой программы. 

|Средство | Описание |
|-----| -----|
|[Средство проверки уникальных значений](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs) |Проверяет наличие потенциальных конфликтов с использованием общих кубитов. |
|[Средство проверки недействительных кубитов](xref:microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits)  |Проверяет, применяет ли программа операцию к кубиту, который уже выпущен. |
|[Счетчик примитивных операций](xref:microsoft.quantum.machines.qc-trace-simulator.primitive-counter)  | Подсчитывает количество примитивных выполнений, используемых каждой операцией, вызываемой в квантовой программе.  |
|[Измеритель глубины](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter)  |Собирает счетчики, представляющие нижнюю границу глубины каждой операции, вызываемой в квантовой программе.   |
|[Измеритель ширины](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter)  |Подсчитывает количество кубитов, выделенных и заимствованных каждой операцией в квантовой программе. |

Каждое из этих средств включается путем установки соответствующих флагов в `QCTraceSimulatorConfiguration` и последующей передачи конфигурации в объявление `QCTraceSimulator`. Сведения об использовании каждого из этих средств см. в приведенных выше ссылках. Дополнительные сведения о настройке `QCTraceSimulator` см. в разделе [QCTraceSimulatorConfiguration](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration).

## <a name="qctracesimulator-methods"></a>Методы QCTraceSimulator

В `QCTraceSimulator` есть несколько встроенных методов для получения значений метрик, которые отслеживаются во время квантовой операции. Примеры методов [QCTraceSimulator.GetMetric](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) и [QCTraceSimulator.ToCSV](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.tocsv) см. в статьях, посвященных [счетчику примитивных операций](xref:microsoft.quantum.machines.qc-trace-simulator.primitive-counter), [измерителю глубины](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter) и [измерителю ширины](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter). Дополнительные сведения обо всех доступных методах см. в разделе [QCTraceSimulator](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) в справочнике по API Q#.  

## <a name="see-also"></a>См. также раздел

- [Квантовый оценщик ресурсов](xref:microsoft.quantum.machines.resources-estimator)
- [Квантовый симулятор Тоффоли](xref:microsoft.quantum.machines.toffoli-simulator)
- [Квантовый симулятор полного состояния](xref:microsoft.quantum.machines.full-state-simulator) 