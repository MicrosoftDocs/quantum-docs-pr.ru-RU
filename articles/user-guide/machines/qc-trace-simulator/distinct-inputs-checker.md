---
title: Средство проверки различных входов — пакет средств разработки тактов
description: Сведения о проверке различных входных данных Microsoft КДК, которая использует симулятор трассировки тактов для проверки Q# кода на наличие потенциальных конфликтов с общими Кубитс.
author: vadym-kl
ms.author: vadym
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.distinct-inputs
no-loc:
- Q#
- $$v
ms.openlocfilehash: bcb0bc92a546279496d27ad9b8c5f943ac133e2a
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/21/2020
ms.locfileid: "90833468"
---
# <a name="quantum-trace-simulator-distinct-inputs-checker"></a>Симулятор трассировки тактов: отдельный модуль проверки входных данных

Средство проверки индивидуальных входных значений входит в состав [симулятора тактовой](xref:microsoft.quantum.machines.qc-trace-simulator.intro)программы пакета разработки тактов. Его можно использовать для обнаружения потенциальных ошибок в коде, вызванных конфликтами с Shared Кубитс. 

## <a name="conflicts-with-shared-qubits"></a>Конфликты с общими Кубитс

Рассмотрим следующий фрагмент кода, Q# чтобы продемонстрировать проблемы, обнаруженные при проверке различных входных значений:

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

При просмотре этой программы можно предположить, что порядок, в котором она вызывает и не `op1` `op2` имеет значения, так как `q1` и `q2` является различными Кубитс и операциями, работающими с различными кубитсми. 

Теперь рассмотрим следующий пример:

```qsharp
operation ApplyWithNonDistinctInputs() : Unit {
    using (qubits = Qubit[3]) {
        let op1 = CNOT(_, qubits[1]);
        let op2 = CNOT(qubits[1], _);
        ApplyBoth(qubits[0], qubits[2], op1, op2);
    }
}
```

Обратите внимание, что `op1` и `op2` они получаются с помощью частичного приложения и совместно используют кубит. При вызове `ApplyBoth` в этом примере результат операции зависит от порядка следования `op1` и `op2` внутреннего результата `ApplyBoth` . При включении проверки различных входных параметров обнаруживает такие ситуации и создает исключение `DistinctInputsCheckerException` . Дополнительные сведения см <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException> . в разделе Q# библиотеки API.

## <a name="invoking-the-distinct-inputs-checker"></a>Вызов средства проверки различных значений

Чтобы запустить симулятор трассировки тактов с помощью средства проверки различных входных данных, необходимо создать <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> экземпляр, присвоить `UseDistinctInputsChecker` свойству **значение true**, а затем создать новый <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> экземпляр с `QCTraceSimulatorConfiguration` параметром в качестве параметра. 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseDistinctInputsChecker = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-distinct-inputs-checker-in-a-c-host-program"></a>Использование средства проверки различных входных значений в управляющей программе C#

Ниже приведен пример основной программы C#, которая использует симулятор трассировки тактов с включенным средством проверки различных входных значений:

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
            traceSimCfg.UseDistinctInputsChecker = true; //enables distinct inputs checker
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
- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException>Справочник по API.
