---
title: Средство проверки различных значений
description: 'Сведения о проверке различных входных данных Microsoft КДК, которая проверяет код Q # на наличие потенциальных конфликтов с общим Кубитс.'
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.distinct-inputs
ms.openlocfilehash: 11a0573242c8afb12f242aa3be5f9cff18290452
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275619"
---
# <a name="distinct-inputs-checker"></a>Средство проверки различных значений

`Distinct Inputs Checker`Компонент является частью [имитатора трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro)компьютерных тактов. Он предназначен для обнаружения потенциальных ошибок в коде. Рассмотрим следующий фрагмент кода Q #, чтобы продемонстрировать проблемы, обнаруженные этим пакетом:

```qsharp
operation ApplyBoth(
    q1 : Qubit,
    q2 : Qubit,
    op1 : (Qubit => Unit),
    op2 : (Qubit => Unit))
: Unit {
    op1(q1);
    op2(q2);
}
```

Когда пользователь просматривает эту программу, предполагается, что порядок, в котором `op1` и `op2` они вызываются, не имеет значения, поскольку `q1` и `q2` являются различными Кубитс и операциями, работающими с различными кубитсми. Теперь рассмотрим пример, в котором используется эта операция:

```qsharp
operation ApplyWithNonDistinctInputs() : Unit {
    using (qubits = Qubit[3]) {
        let op1 = CNOT(_, qubits[1]);
        let op2 = CNOT(qubits[1], _);
        ApplyBoth(qubits[0], qubits[2], op1, op2);
    }
}
```

Теперь `op1` и `op2` получаются с помощью частичного приложения и совместно используют кубит. Когда пользователь вызывает в приведенном `ApplyBoth` выше примере, результат операции будет зависеть от порядка `op1` и `op2` внутри `ApplyBoth` . Это, безусловно, не то, что может произойти пользователю. `Distinct Inputs Checker`Определяет такие ситуации, когда включен и выдает исключение `DistinctInputsCheckerException` . Дополнительные сведения см. в документации по API в [дистинктинпутсчеккерексцептион](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException) .

## <a name="using-the-distinct-inputs-checker-in-your-c-program"></a>Использование средства проверки различных входных данных в программе C#

Ниже приведен пример кода драйвера C# для использования имитатора трассировки тактов компьютера с `Distinct Inputs Checker` включенным:

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
            traceSimCfg.useDistinctInputsChecker = true; //enables distinct inputs checker
            QCTraceSimulator sim = new QCTraceSimulator(traceSimCfg);
            var res = MyQuantumProgram.Run().Result;
            System.Console.WriteLine("Press any key to continue...");
            System.Console.ReadKey();
        }
    }
}
```

Класс `QCTraceSimulatorConfiguration` хранит конфигурацию симулятора трассировки компьютерных тактов и может быть предоставлена в качестве аргумента для `QCTraceSimulator` конструктора. Если параметр `useDistinctInputsChecker` имеет значение true, `Distinct Inputs Checker` включен. Дополнительные сведения см. в документации по API на [кктрацесимулатор](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) и [кктрацесимулаторконфигуратион](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration?) .

## <a name="see-also"></a>См. также

- Обзор [имитатора трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro) компьютерных тактов.
