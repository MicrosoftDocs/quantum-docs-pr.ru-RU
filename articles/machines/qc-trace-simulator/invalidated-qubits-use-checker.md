---
title: Недействительная Проверка использования Кубитс | Симулятор трассировки компьютерных тактов | Документация Майкрософт
description: Обзор имитатора трассировки тактов компьютера
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits
ms.openlocfilehash: 7403381b995ab660aa5cbc5a52b1e12c5c9ce442
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/29/2019
ms.locfileid: "73184973"
---
# <a name="invalidated-qubits-use-checker"></a><span data-ttu-id="e1166-103">Недействительная Проверка использования Кубитс</span><span class="sxs-lookup"><span data-stu-id="e1166-103">Invalidated Qubits Use Checker</span></span>

<span data-ttu-id="e1166-104">`Invalidated Qubits Use Checker` является частью тактового компьютера, [трацесимулатор](xref:microsoft.quantum.machines.qc-trace-simulator.intro) , предназначенного для обнаружения потенциальных ошибок в коде.</span><span class="sxs-lookup"><span data-stu-id="e1166-104">The `Invalidated Qubits Use Checker` is a part of the quantum computer [TraceSimulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) designed for detecting potential bugs in the code.</span></span> <span data-ttu-id="e1166-105">Рассмотрим следующий фрагмент кода Q #, чтобы продемонстрировать проблемы, обнаруженные `Invalidated Qubits Use Checker`.</span><span class="sxs-lookup"><span data-stu-id="e1166-105">Consider the following piece of Q# code to illustrate the issues detected by the `Invalidated Qubits Use Checker`.</span></span>

```qsharp
operation UseReleasedQubitTest () : Unit {
    mutable q = new Qubit[1];
    using (ans = Qubit()) {
        set q w/= 0 <- ans;
    }
    H(q[0]);
}
```

<span data-ttu-id="e1166-106">Когда `H` применяется к `q[0]` он указывает на уже выпущенную кубит.</span><span class="sxs-lookup"><span data-stu-id="e1166-106">When `H` is applied to `q[0]` it points to an already released qubit.</span></span> <span data-ttu-id="e1166-107">Это может привести к неопределенному поведению.</span><span class="sxs-lookup"><span data-stu-id="e1166-107">This can cause undefined behavior.</span></span> <span data-ttu-id="e1166-108">Если `Invalidated Qubits Use Checker` включена, исключение `InvalidatedQubitsUseCheckerException` возникает, если операция применяется к уже выпущенному кубит.</span><span class="sxs-lookup"><span data-stu-id="e1166-108">When the `Invalidated Qubits Use Checker` is enabled, the exception `InvalidatedQubitsUseCheckerException` will be thrown if an operation is applied to an already released qubit.</span></span> <span data-ttu-id="e1166-109">Дополнительные сведения см. в документации по API в [инвалидатедкубитсусечеккерексцептион](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException) .</span><span class="sxs-lookup"><span data-stu-id="e1166-109">See the API documentation on [InvalidatedQubitsUseCheckerException](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException) for more details.</span></span>

## <a name="using-the-invalidated-qubits-use-checker-in-your-c-program"></a><span data-ttu-id="e1166-110">Использование в C# программе средства проверки использования непроверенных Кубитс</span><span class="sxs-lookup"><span data-stu-id="e1166-110">Using the Invalidated Qubits Use Checker in your C# Program</span></span>

<span data-ttu-id="e1166-111">Ниже приведен пример кода C# драйвера для использования тактового компьютера `Trace
Simulator` с включенным `Invalidated Qubits Use Checker`.</span><span class="sxs-lookup"><span data-stu-id="e1166-111">The following is an example of C# driver code for using the quantum computer `Trace
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

<span data-ttu-id="e1166-112">Класс `QCTraceSimulatorConfiguration` хранит конфигурацию симулятора трассировки компьютерных тактов и может быть предоставлена в качестве аргумента для конструктора `QCTraceSimulator`.</span><span class="sxs-lookup"><span data-stu-id="e1166-112">The class `QCTraceSimulatorConfiguration` stores the configuration of the quantum computer trace simulator and can be provided as an argument for the `QCTraceSimulator` constructor.</span></span> <span data-ttu-id="e1166-113">Если `useInvalidatedQubitsUseChecker` имеет значение true, `Invalidated Qubits Use Checker` включен.</span><span class="sxs-lookup"><span data-stu-id="e1166-113">When `useInvalidatedQubitsUseChecker` is set to true the `Invalidated Qubits Use Checker` is enabled.</span></span> <span data-ttu-id="e1166-114">Дополнительные сведения см. в документации по API на [кктрацесимулатор](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) и [кктрацесимулаторконфигуратион](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="e1166-114">See the API documentation on [QCTraceSimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) and [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration) for more details.</span></span>

## <a name="see-also"></a><span data-ttu-id="e1166-115">Дополнительные материалы</span><span class="sxs-lookup"><span data-stu-id="e1166-115">See also</span></span> ##

- <span data-ttu-id="e1166-116">Обзор [имитатора трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro) компьютерных тактов.</span><span class="sxs-lookup"><span data-stu-id="e1166-116">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
