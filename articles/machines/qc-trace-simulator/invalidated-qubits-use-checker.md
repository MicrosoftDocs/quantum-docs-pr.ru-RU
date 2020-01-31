---
title: Недействительная Проверка использования Кубитс | Симулятор трассировки компьютерных тактов | Документация Майкрософт
description: Обзор симулятора трассировки квантового компьютера
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits
ms.openlocfilehash: 093937346488725eacb69ef7da6affde764ec5c1
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820884"
---
# <a name="invalidated-qubits-use-checker"></a><span data-ttu-id="1dd1d-103">Недействительная Проверка использования Кубитс</span><span class="sxs-lookup"><span data-stu-id="1dd1d-103">Invalidated Qubits Use Checker</span></span>

<span data-ttu-id="1dd1d-104">`Invalidated Qubits Use Checker` является частью тактового компьютера, [трацесимулатор](xref:microsoft.quantum.machines.qc-trace-simulator.intro) , предназначенного для обнаружения потенциальных ошибок в коде.</span><span class="sxs-lookup"><span data-stu-id="1dd1d-104">The `Invalidated Qubits Use Checker` is a part of the quantum computer [TraceSimulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) designed for detecting potential bugs in the code.</span></span> <span data-ttu-id="1dd1d-105">Рассмотрим следующий фрагмент кода Q #, чтобы продемонстрировать проблемы, обнаруженные `Invalidated Qubits Use Checker`.</span><span class="sxs-lookup"><span data-stu-id="1dd1d-105">Consider the following piece of Q# code to illustrate the issues detected by the `Invalidated Qubits Use Checker`.</span></span>

```qsharp
operation UseReleasedQubit() : Unit {
    mutable q = new Qubit[1];
    using (ans = Qubit()) {
        set q w/= 0 <- ans;
    }
    H(q[0]);
}
```

<span data-ttu-id="1dd1d-106">Когда `H` применяется к `q[0]` он указывает на уже выпущенную кубит.</span><span class="sxs-lookup"><span data-stu-id="1dd1d-106">When `H` is applied to `q[0]` it points to an already released qubit.</span></span> <span data-ttu-id="1dd1d-107">Это может привести к неопределенному поведению.</span><span class="sxs-lookup"><span data-stu-id="1dd1d-107">This can cause undefined behavior.</span></span> <span data-ttu-id="1dd1d-108">Если `Invalidated Qubits Use Checker` включена, исключение `InvalidatedQubitsUseCheckerException` возникает, если операция применяется к уже выпущенному кубит.</span><span class="sxs-lookup"><span data-stu-id="1dd1d-108">When the `Invalidated Qubits Use Checker` is enabled, the exception `InvalidatedQubitsUseCheckerException` will be thrown if an operation is applied to an already released qubit.</span></span> <span data-ttu-id="1dd1d-109">Дополнительные сведения см. в документации по API в [инвалидатедкубитсусечеккерексцептион](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException) .</span><span class="sxs-lookup"><span data-stu-id="1dd1d-109">See the API documentation on [InvalidatedQubitsUseCheckerException](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException) for more details.</span></span>

## <a name="using-the-invalidated-qubits-use-checker-in-your-c-program"></a><span data-ttu-id="1dd1d-110">Использование в C# программе средства проверки использования непроверенных Кубитс</span><span class="sxs-lookup"><span data-stu-id="1dd1d-110">Using the Invalidated Qubits Use Checker in your C# Program</span></span>

<span data-ttu-id="1dd1d-111">Ниже приведен пример кода C# драйвера для использования тактового компьютера `Trace
Simulator` с включенным `Invalidated Qubits Use Checker`.</span><span class="sxs-lookup"><span data-stu-id="1dd1d-111">The following is an example of C# driver code for using the quantum computer `Trace
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

<span data-ttu-id="1dd1d-112">Класс `QCTraceSimulatorConfiguration` хранит конфигурацию симулятора трассировки компьютерных тактов и может быть предоставлена в качестве аргумента для конструктора `QCTraceSimulator`.</span><span class="sxs-lookup"><span data-stu-id="1dd1d-112">The class `QCTraceSimulatorConfiguration` stores the configuration of the quantum computer trace simulator and can be provided as an argument for the `QCTraceSimulator` constructor.</span></span> <span data-ttu-id="1dd1d-113">Если `useInvalidatedQubitsUseChecker` имеет значение true, `Invalidated Qubits Use Checker` включен.</span><span class="sxs-lookup"><span data-stu-id="1dd1d-113">When `useInvalidatedQubitsUseChecker` is set to true the `Invalidated Qubits Use Checker` is enabled.</span></span> <span data-ttu-id="1dd1d-114">Дополнительные сведения см. в документации по API на [кктрацесимулатор](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) и [кктрацесимулаторконфигуратион](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="1dd1d-114">See the API documentation on [QCTraceSimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) and [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration) for more details.</span></span>

## <a name="see-also"></a><span data-ttu-id="1dd1d-115">См. также</span><span class="sxs-lookup"><span data-stu-id="1dd1d-115">See also</span></span> ##

- <span data-ttu-id="1dd1d-116">Обзор [имитатора трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro) компьютерных тактов.</span><span class="sxs-lookup"><span data-stu-id="1dd1d-116">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
