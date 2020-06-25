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
# <a name="distinct-inputs-checker"></a><span data-ttu-id="645a3-103">Средство проверки различных значений</span><span class="sxs-lookup"><span data-stu-id="645a3-103">Distinct Inputs Checker</span></span>

<span data-ttu-id="645a3-104">`Distinct Inputs Checker`Компонент является частью [имитатора трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro)компьютерных тактов.</span><span class="sxs-lookup"><span data-stu-id="645a3-104">The `Distinct Inputs Checker` is a part of the quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="645a3-105">Он предназначен для обнаружения потенциальных ошибок в коде.</span><span class="sxs-lookup"><span data-stu-id="645a3-105">It is designed for detecting potential bugs in the code.</span></span> <span data-ttu-id="645a3-106">Рассмотрим следующий фрагмент кода Q #, чтобы продемонстрировать проблемы, обнаруженные этим пакетом:</span><span class="sxs-lookup"><span data-stu-id="645a3-106">Consider the following piece of Q# code to illustrate the issues detected by this package:</span></span>

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

<span data-ttu-id="645a3-107">Когда пользователь просматривает эту программу, предполагается, что порядок, в котором `op1` и `op2` они вызываются, не имеет значения, поскольку `q1` и `q2` являются различными Кубитс и операциями, работающими с различными кубитсми.</span><span class="sxs-lookup"><span data-stu-id="645a3-107">When the user looks at this program, they assume that the order in which `op1` and `op2` are called does not matter because `q1` and `q2` are different qubits and operations acting on different qubits commute.</span></span> <span data-ttu-id="645a3-108">Теперь рассмотрим пример, в котором используется эта операция:</span><span class="sxs-lookup"><span data-stu-id="645a3-108">Let us now consider an example, where this operation is used:</span></span>

```qsharp
operation ApplyWithNonDistinctInputs() : Unit {
    using (qubits = Qubit[3]) {
        let op1 = CNOT(_, qubits[1]);
        let op2 = CNOT(qubits[1], _);
        ApplyBoth(qubits[0], qubits[2], op1, op2);
    }
}
```

<span data-ttu-id="645a3-109">Теперь `op1` и `op2` получаются с помощью частичного приложения и совместно используют кубит.</span><span class="sxs-lookup"><span data-stu-id="645a3-109">Now `op1` and `op2` are both obtained using partial application and share a qubit.</span></span> <span data-ttu-id="645a3-110">Когда пользователь вызывает в приведенном `ApplyBoth` выше примере, результат операции будет зависеть от порядка `op1` и `op2` внутри `ApplyBoth` .</span><span class="sxs-lookup"><span data-stu-id="645a3-110">When the user calls `ApplyBoth` in the example above the result of the operation will depend on the order of `op1` and `op2` inside `ApplyBoth`.</span></span> <span data-ttu-id="645a3-111">Это, безусловно, не то, что может произойти пользователю.</span><span class="sxs-lookup"><span data-stu-id="645a3-111">This is definitely not what the user would expect to happen.</span></span> <span data-ttu-id="645a3-112">`Distinct Inputs Checker`Определяет такие ситуации, когда включен и выдает исключение `DistinctInputsCheckerException` .</span><span class="sxs-lookup"><span data-stu-id="645a3-112">The `Distinct Inputs Checker` will detect such situations when enabled and will throw `DistinctInputsCheckerException`.</span></span> <span data-ttu-id="645a3-113">Дополнительные сведения см. в документации по API в [дистинктинпутсчеккерексцептион](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException) .</span><span class="sxs-lookup"><span data-stu-id="645a3-113">See the API documentation on [DistinctInputsCheckerException](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException) for more details.</span></span>

## <a name="using-the-distinct-inputs-checker-in-your-c-program"></a><span data-ttu-id="645a3-114">Использование средства проверки различных входных данных в программе C#</span><span class="sxs-lookup"><span data-stu-id="645a3-114">Using the Distinct Inputs Checker in your C# Program</span></span>

<span data-ttu-id="645a3-115">Ниже приведен пример кода драйвера C# для использования имитатора трассировки тактов компьютера с `Distinct Inputs Checker` включенным:</span><span class="sxs-lookup"><span data-stu-id="645a3-115">The following is an example of C# driver code for using the quantum computer trace simulator with the `Distinct Inputs Checker` enabled:</span></span>

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

<span data-ttu-id="645a3-116">Класс `QCTraceSimulatorConfiguration` хранит конфигурацию симулятора трассировки компьютерных тактов и может быть предоставлена в качестве аргумента для `QCTraceSimulator` конструктора.</span><span class="sxs-lookup"><span data-stu-id="645a3-116">The class `QCTraceSimulatorConfiguration` stores the configuration of the quantum computer trace simulator and can be provided as an argument for the `QCTraceSimulator` constructor.</span></span> <span data-ttu-id="645a3-117">Если параметр `useDistinctInputsChecker` имеет значение true, `Distinct Inputs Checker` включен.</span><span class="sxs-lookup"><span data-stu-id="645a3-117">When `useDistinctInputsChecker` is set to true the `Distinct Inputs Checker` is enabled.</span></span> <span data-ttu-id="645a3-118">Дополнительные сведения см. в документации по API на [кктрацесимулатор](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) и [кктрацесимулаторконфигуратион](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration?) .</span><span class="sxs-lookup"><span data-stu-id="645a3-118">See the API documentation on [QCTraceSimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) and [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration?) for more details.</span></span>

## <a name="see-also"></a><span data-ttu-id="645a3-119">См. также</span><span class="sxs-lookup"><span data-stu-id="645a3-119">See also</span></span>

- <span data-ttu-id="645a3-120">Обзор [имитатора трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro) компьютерных тактов.</span><span class="sxs-lookup"><span data-stu-id="645a3-120">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
