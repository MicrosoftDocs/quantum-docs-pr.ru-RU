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
# <a name="invalidated-qubits-use-checker"></a><span data-ttu-id="4689d-103">Недействительная Проверка использования Кубитс</span><span class="sxs-lookup"><span data-stu-id="4689d-103">Invalidated Qubits Use Checker</span></span>

<span data-ttu-id="4689d-104">`Invalidated Qubits Use Checker`Компонент является частью тактового компьютера [трацесимулатор](xref:microsoft.quantum.machines.qc-trace-simulator.intro) , предназначенного для обнаружения потенциальных ошибок в коде.</span><span class="sxs-lookup"><span data-stu-id="4689d-104">The `Invalidated Qubits Use Checker` is a part of the quantum computer [TraceSimulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) designed for detecting potential bugs in the code.</span></span> <span data-ttu-id="4689d-105">Рассмотрим следующий фрагмент кода Q #, чтобы продемонстрировать проблемы, обнаруженные компонентом `Invalidated Qubits Use Checker` .</span><span class="sxs-lookup"><span data-stu-id="4689d-105">Consider the following piece of Q# code to illustrate the issues detected by the `Invalidated Qubits Use Checker`.</span></span>

```qsharp
operation UseReleasedQubit() : Unit {
    mutable q = new Qubit[1];
    using (ans = Qubit()) {
        set q w/= 0 <- ans;
    }
    H(q[0]);
}
```

<span data-ttu-id="4689d-106">Когда `H` применяется к, `q[0]` он указывает на уже выпущенную кубит.</span><span class="sxs-lookup"><span data-stu-id="4689d-106">When `H` is applied to `q[0]` it points to an already released qubit.</span></span> <span data-ttu-id="4689d-107">Это может привести к неопределенному поведению.</span><span class="sxs-lookup"><span data-stu-id="4689d-107">This can cause undefined behavior.</span></span> <span data-ttu-id="4689d-108">Если параметр `Invalidated Qubits Use Checker` включен, то исключение `InvalidatedQubitsUseCheckerException` будет создано, если операция применяется к уже выпущенному кубит.</span><span class="sxs-lookup"><span data-stu-id="4689d-108">When the `Invalidated Qubits Use Checker` is enabled, the exception `InvalidatedQubitsUseCheckerException` will be thrown if an operation is applied to an already released qubit.</span></span> <span data-ttu-id="4689d-109">Дополнительные сведения см. в документации по API в [инвалидатедкубитсусечеккерексцептион](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException) .</span><span class="sxs-lookup"><span data-stu-id="4689d-109">See the API documentation on [InvalidatedQubitsUseCheckerException](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException) for more details.</span></span>

## <a name="using-the-invalidated-qubits-use-checker-in-your-c-program"></a><span data-ttu-id="4689d-110">Использование недействительной проверки использования Кубитс в программе C#</span><span class="sxs-lookup"><span data-stu-id="4689d-110">Using the Invalidated Qubits Use Checker in your C# Program</span></span>

<span data-ttu-id="4689d-111">Ниже приведен пример кода драйвера C# для использования тактового компьютера `Trace
Simulator` с `Invalidated Qubits Use Checker` включенным:</span><span class="sxs-lookup"><span data-stu-id="4689d-111">The following is an example of C# driver code for using the quantum computer `Trace
Simulator` with the `Invalidated Qubits Use Checker` enabled:</span></span> 

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

<span data-ttu-id="4689d-112">Класс `QCTraceSimulatorConfiguration` хранит конфигурацию симулятора трассировки компьютерных тактов и может быть предоставлена в качестве аргумента для `QCTraceSimulator` конструктора.</span><span class="sxs-lookup"><span data-stu-id="4689d-112">The class `QCTraceSimulatorConfiguration` stores the configuration of the quantum computer trace simulator and can be provided as an argument for the `QCTraceSimulator` constructor.</span></span> <span data-ttu-id="4689d-113">Если параметр `useInvalidatedQubitsUseChecker` имеет значение true, `Invalidated Qubits Use Checker` включен.</span><span class="sxs-lookup"><span data-stu-id="4689d-113">When `useInvalidatedQubitsUseChecker` is set to true the `Invalidated Qubits Use Checker` is enabled.</span></span> <span data-ttu-id="4689d-114">Дополнительные сведения см. в документации по API на [кктрацесимулатор](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) и [кктрацесимулаторконфигуратион](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="4689d-114">See the API documentation on [QCTraceSimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) and [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration) for more details.</span></span>

## <a name="see-also"></a><span data-ttu-id="4689d-115">См. также</span><span class="sxs-lookup"><span data-stu-id="4689d-115">See also</span></span> ##

- <span data-ttu-id="4689d-116">Обзор [имитатора трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro) компьютерных тактов.</span><span class="sxs-lookup"><span data-stu-id="4689d-116">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
