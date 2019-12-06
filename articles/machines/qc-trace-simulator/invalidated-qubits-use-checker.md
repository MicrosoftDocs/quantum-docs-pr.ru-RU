---
title: Недействительная Проверка использования Кубитс | Симулятор трассировки компьютерных тактов | Документация Майкрософт
description: Обзор симулятора трассировки квантового компьютера
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits
ms.openlocfilehash: 283cc7d7d88f731f40fa396c38ae5ea8dd90537f
ms.sourcegitcommit: 27c9bf1aae923527aa5adeaee073cb27d35c0ca1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2019
ms.locfileid: "74863186"
---
# <a name="invalidated-qubits-use-checker"></a>Недействительная Проверка использования Кубитс

`Invalidated Qubits Use Checker` является частью тактового компьютера, [трацесимулатор](xref:microsoft.quantum.machines.qc-trace-simulator.intro) , предназначенного для обнаружения потенциальных ошибок в коде. Рассмотрим следующий фрагмент кода Q #, чтобы продемонстрировать проблемы, обнаруженные `Invalidated Qubits Use Checker`.

```qsharp
operation UseReleasedQubit () : Unit {
    mutable q = new Qubit[1];
    using (ans = Qubit()) {
        set q w/= 0 <- ans;
    }
    H(q[0]);
}
```

Когда `H` применяется к `q[0]` он указывает на уже выпущенную кубит. Это может привести к неопределенному поведению. Если `Invalidated Qubits Use Checker` включена, исключение `InvalidatedQubitsUseCheckerException` возникает, если операция применяется к уже выпущенному кубит. Дополнительные сведения см. в документации по API в [инвалидатедкубитсусечеккерексцептион](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException) .

## <a name="using-the-invalidated-qubits-use-checker-in-your-c-program"></a>Использование в C# программе средства проверки использования непроверенных Кубитс

Ниже приведен пример кода C# драйвера для использования тактового компьютера `Trace
Simulator` с включенным `Invalidated Qubits Use Checker`. 

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
            var traceSimCfg = new QCTraceSimulatorConfiguration();
            traceSimCfg.useInvalidatedQubitsUseChecker = true; // enables useInvalidatedQubitsUseChecker
            QCTraceSimulator sim = new QCTraceSimulator(traceSimCfg);
            var res = MyQuantumProgram.Run().Result;
            System.Console.WriteLine("Press any key to continue...");
            System.Console.ReadKey();
        }
    }
}
```

Класс `QCTraceSimulatorConfiguration` хранит конфигурацию симулятора трассировки компьютерных тактов и может быть предоставлена в качестве аргумента для конструктора `QCTraceSimulator`. Если `useInvalidatedQubitsUseChecker` имеет значение true, `Invalidated Qubits Use Checker` включен. Дополнительные сведения см. в документации по API на [кктрацесимулатор](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) и [кктрацесимулаторконфигуратион](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration) .

## <a name="see-also"></a>Дополнительные материалы ##

- Обзор [имитатора трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro) компьютерных тактов.
