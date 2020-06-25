---
title: Средство проверки недействительных кубитов
description: 'Сведения о проверке подлинности Microsoft КДК unvalidateed Кубитс, которая проверяет код Q # для потенциально недействительного Кубитс.'
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits
ms.openlocfilehash: e2bbb12448e27f28db030a0084302fb24f46f26b
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275571"
---
# <a name="invalidated-qubits-use-checker"></a>Недействительная Проверка использования Кубитс

`Invalidated Qubits Use Checker`Компонент является частью тактового компьютера [трацесимулатор](xref:microsoft.quantum.machines.qc-trace-simulator.intro) , предназначенного для обнаружения потенциальных ошибок в коде. Рассмотрим следующий фрагмент кода Q #, чтобы продемонстрировать проблемы, обнаруженные компонентом `Invalidated Qubits Use Checker` .

```qsharp
operation UseReleasedQubit() : Unit {
    mutable q = new Qubit[1];
    using (ans = Qubit()) {
        set q w/= 0 <- ans;
    }
    H(q[0]);
}
```

Когда `H` применяется к, `q[0]` он указывает на уже выпущенную кубит. Это может привести к неопределенному поведению. Если параметр `Invalidated Qubits Use Checker` включен, то исключение `InvalidatedQubitsUseCheckerException` будет создано, если операция применяется к уже выпущенному кубит. Дополнительные сведения см. в документации по API в [инвалидатедкубитсусечеккерексцептион](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException) .

## <a name="using-the-invalidated-qubits-use-checker-in-your-c-program"></a>Использование недействительной проверки использования Кубитс в программе C#

Ниже приведен пример кода драйвера C# для использования тактового компьютера `Trace
Simulator` с `Invalidated Qubits Use Checker` включенным: 

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

Класс `QCTraceSimulatorConfiguration` хранит конфигурацию симулятора трассировки компьютерных тактов и может быть предоставлена в качестве аргумента для `QCTraceSimulator` конструктора. Если параметр `useInvalidatedQubitsUseChecker` имеет значение true, `Invalidated Qubits Use Checker` включен. Дополнительные сведения см. в документации по API на [кктрацесимулатор](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) и [кктрацесимулаторконфигуратион](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration) .

## <a name="see-also"></a>См. также ##

- Обзор [имитатора трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro) компьютерных тактов.
