---
title: Симулятор трассировки квантового компьютера
description: Узнайте, как с помощью симулятора трассировки компьютера Microsoft Quantum выполнять отладку классического кода и оценивать требования к ресурсам для квантовой программы.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.intro
ms.openlocfilehash: 72c259933d2df8f79319e6c0c65ae181a9f9cff3
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/28/2020
ms.locfileid: "77906089"
---
# <a name="quantum-trace-simulator"></a>Квантовый симулятор трассировки

Симулятор трассировки квантового компьютера Microsoft выполняет квантовую программу без фактической симуляции состояния квантового компьютера.  По этой причине симулятор трассировки может выполнять квантовые программы, использующие тысячи кубитов.  Это полезно для двух основных целей: 

* Отладка классического кода, который является частью квантовой программы. 
* Оценка ресурсов, необходимых для запуска заданного экземпляра квантовой программы на квантовом компьютере.

В симуляторе трассировки используются дополнительные сведения, предоставляемые пользователем, когда необходимо выполнить измерения. Дополнительные сведения об этом см. в разделе [Providing the Probability of Measurement Outcomes](#providing-the-probability-of-measurement-outcomes) (Предоставление вероятности результатов измерения. 

## <a name="providing-the-probability-of-measurement-outcomes"></a>Предоставление вероятности результатов измерения

Существует два типа измерений, которые отображаются в квантовых алгоритмах. Первый тип играет вспомогательную роль, где пользователь обычно знает вероятность результатов. В этом случае пользователь может записывать <xref:microsoft.quantum.intrinsic.assertprob> из пространства имен <xref:microsoft.quantum.intrinsic>, чтобы выразить этот набор знаний. Проиллюстрируем это на примере.

```qsharp
operation TeleportQubit(source : Qubit, target : Qubit) : Unit {
    using (qubit = Qubit()) {
        H(qubit);
        CNOT(qubit, target);
        CNOT(source, qubit);
        H(source);

        AssertProb([PauliZ], [source], Zero, 0.5, "Outcomes must be equally likely", 1e-5);
        AssertProb([PauliZ], [q], Zero, 0.5, "Outcomes must be equally likely", 1e-5);

        if (M(source) == One)  { Z(target); X(source); }
        if (M(q) == One) { X(target); X(q); }
    }
}
```

При выполнении `AssertProb` симулятором трассировки он записывает измерения `PauliZ` в `source` и `q` должен получить результат `Zero` с вероятностью 0,5. Когда симулятор выполняет `M` позже, он найдет записанные значения вероятностей результата и `M` возвратит `Zero` или `One` с вероятностью 0,5. Если один и тот же код выполняется в симуляторе, который отслеживает квантовое состояние, такой симулятор проверяет правильность предоставленных вероятностей в `AssertProb`.

## <a name="running-your-program-with-the-quantum-computer-trace-simulator"></a>Запуск программы с симулятором трассировки квантового компьютера 

Симулятор трассировки квантового компьютера можно рассматривать как еще один целевой компьютер. Программа драйвера C# очень похожа на программу для любого другого квантового симулятора: 

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
            var res = MyQuantumProgram.Run().Result;
            System.Console.WriteLine("Press any key to continue...");
            System.Console.ReadKey();
        }
    }
}
```

Обратите внимание, что если имеется хотя бы одно измерение, не помеченное с помощью `AssertProb`, симулятор выдаст `UnconstrainedMeasurementException` из пространства имен `Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators`. Дополнительные сведения см. в документации по API [UnconstrainedMeasurementException](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.UnconstrainedMeasurementException) (Неограниченное исключение измерения).

В дополнение к запущенным квантовым программам симулятор трассировки включает пять компонентов для обнаружения ошибок в программах и выполнения оценки ресурсов квантовых программ: 

* [Средство проверки уникальных значений](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs)
* [Средство проверки недействительных кубитов](xref:microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits)
* [Счетчик примитивных операций](xref:microsoft.quantum.machines.qc-trace-simulator.primitive-counter)
* [Circuit Depth Counter](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter) (Счетчик глубины канала)
* [Circuit Width Counter](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter) (Счетчик ширины канала)

Каждый из этих компонентов можно включить, установив соответствующие флажки в `QCTraceSimulatorConfiguration`. Дополнительные сведения об использовании каждого из этих компонентов приведены в соответствующих справочных файлах. Конкретные сведения см. в документации API [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration) (Настройка симулятора трассировки QC).

## <a name="see-also"></a>См. также раздел
Справочник по C# [симулятора трассировки](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) квантового компьютера 

