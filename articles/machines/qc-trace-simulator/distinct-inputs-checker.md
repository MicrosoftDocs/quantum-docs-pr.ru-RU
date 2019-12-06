---
title: Средство проверки уникальных значений | Симулятор трассировки компьютерных тактов | Документация Майкрософт
description: Обзор симулятора трассировки квантового компьютера
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.distinct-inputs
ms.openlocfilehash: ce3f156a84a4509781a74c9276b953c79670a756
ms.sourcegitcommit: 27c9bf1aae923527aa5adeaee073cb27d35c0ca1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2019
ms.locfileid: "74864310"
---
# <a name="distinct-inputs-checker"></a>Средство проверки различных значений

`Distinct Inputs Checker` является частью [симулятора трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro)компьютерных тактов. Он предназначен для обнаружения потенциальных ошибок в коде. Рассмотрим следующий фрагмент кода Q #, чтобы продемонстрировать проблемы, обнаруженные этим пакетом:

```qsharp
operation DoBoth(q1 : Qubit, q2 : Qubit, op1 : (Qubit => Unit), op2 : (Qubit => Unit)) : Unit {

    op1(q1);
    op2(q2);
}
```

Когда пользователь просматривает эту программу, предполагается, что порядок вызова `op1` и `op2` не имеет значения, так как `q1` и `q2` являются различными Кубитс и операциями, работающими с различными кубитсми. Теперь рассмотрим пример, в котором используется эта операция:

```qsharp
operation CapturedQubits () : Unit {

    using (q = Qubit[3]) {
        let op1 = CNOT(_, q[1]);
        let op2 = CNOT(q[1], _);
        DoBoth(q[0], q[2], op1, op2);
    }
}
```

Теперь `op1` и `op2` получены с помощью частичного приложения и совместно используют кубит. Когда пользователь вызывает `DoBoth` в примере выше, результат операции будет зависеть от порядка `op1` и `op2` внутри `DoBoth`. Это, безусловно, не то, что может произойти пользователю. `Distinct Inputs Checker` обнаружит такие ситуации при включении и выдаст `DistinctInputsCheckerException`. Дополнительные сведения см. в документации по API в [дистинктинпутсчеккерексцептион](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException) .

## <a name="using-the-distinct-inputs-checker-in-your-c-program"></a>Использование средства проверки различных входных значений C# в программе

Ниже приведен пример кода C# драйвера для использования симулятора трассировки компьютерных тактов с включенным `Distinct Inputs Checker`.

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

Класс `QCTraceSimulatorConfiguration` хранит конфигурацию симулятора трассировки компьютерных тактов и может быть предоставлена в качестве аргумента для конструктора `QCTraceSimulator`. Если `useDistinctInputsChecker` имеет значение true, `Distinct Inputs Checker` включен. Дополнительные сведения см. в документации по API на [кктрацесимулатор](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) и [кктрацесимулаторконфигуратион](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration?) .

## <a name="see-also"></a>Дополнительные материалы

- Обзор [имитатора трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro) компьютерных тактов.
