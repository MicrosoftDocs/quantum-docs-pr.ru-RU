---
title: Недействительная Проверка использования Кубитс-пакет разработки тактов
description: Узнайте о недействительности Кубитс Microsoft КДК, которая использует симулятор трассировки тактов для проверки Q# кода на наличие потенциально недействительного Кубитс.
author: vadym-kl
ms.author: vadym
ms.date: 06/25/2020
ms.topic: conceptual
uid: microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits
no-loc:
- Q#
- $$v
ms.openlocfilehash: 9014097ace7c9f19d93a92372da40f71fa7f87ee
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858626"
---
# <a name="quantum-trace-simulator-invalidated-qubits-use-checker"></a>Симулятор трассировки тактов: недействительная Проверка использования Кубитс

Недействительная Проверка использования Кубитс является частью [симулятора отслеживания тактов](xref:microsoft.quantum.machines.qc-trace-simulator.intro)пакета разработки тактов. Его можно использовать для обнаружения потенциальных ошибок в коде, вызванных недопустимым Кубитс. 

## <a name="invalid-qubits"></a>Недопустимый Кубитс

Рассмотрим следующий фрагмент кода, Q# чтобы продемонстрировать проблемы, обнаруженные недействительным Кубитс использованием средства проверки.

```qsharp
operation UseReleasedQubit() : Unit {
    mutable q = new Qubit[1];
    using (ans = Qubit()) {
        set q w/= 0 <- ans;
    }
    H(q[0]);
}
```

При применении `H` операции к `q[0]` она указывает на уже выпущенную кубит, которая может привести к неопределенному поведению. Если функция проверки использования непроверенных Кубитс включена, она создает исключение, `InvalidatedQubitsUseCheckerException` Если программа применяет операцию к уже выпущенной кубит. Для получения дополнительной информации см. <xref:Microsoft.Quantum.Simulation.QCTraceSimulatorRuntime.InvalidatedQubitsUseCheckerException>.

## <a name="invoking-the-invalidated-qubits-use-checker"></a>Вызов проверки непроверенного использования Кубитс

Чтобы запустить симулятор трассировки тактов с проверкой непроверенного использования Кубитс, необходимо создать <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> экземпляр, присвоить `UseInvalidatedQubitsUseChecker` свойству **значение true**, а затем создать новый <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> экземпляр с `QCTraceSimulatorConfiguration` параметром в качестве параметра. 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseInvalidatedQubitsUseChecker = true;
var sim = new QCTraceSimulator(config);
```


## <a name="using-the-invalidated-qubits-use-checker-in-a-c-host-program"></a>Использование недействительной проверки использования Кубитс в основной программе C#

Ниже приведен пример ведущих программ C#, использующих симулятор трассировки тактов с включенной проверкой подлинности Кубитс. 

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
            traceSimCfg.UseInvalidatedQubitsUseChecker = true; // enables UseInvalidatedQubitsUseChecker
            QCTraceSimulator sim = new QCTraceSimulator(traceSimCfg);
            var res = MyQuantumProgram.Run().Result;
            System.Console.WriteLine("Press any key to continue...");
            System.Console.ReadKey();
        }
    }
}
```

## <a name="see-also"></a>См. также

- Обзор [имитатора трассировки такта](xref:microsoft.quantum.machines.qc-trace-simulator.intro) в пакете разработки тактов.
- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator>Справочник по API.
- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>Справочник по API.
- <xref:Microsoft.Quantum.Simulation.QCTraceSimulatorRuntime.InvalidatedQubitsUseCheckerException>Справочник по API.
