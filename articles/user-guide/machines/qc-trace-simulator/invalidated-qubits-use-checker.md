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
# <a name="quantum-trace-simulator-invalidated-qubits-use-checker"></a><span data-ttu-id="509db-103">Симулятор трассировки тактов: недействительная Проверка использования Кубитс</span><span class="sxs-lookup"><span data-stu-id="509db-103">Quantum trace simulator: invalidated qubits use checker</span></span>

<span data-ttu-id="509db-104">Недействительная Проверка использования Кубитс является частью [симулятора отслеживания тактов](xref:microsoft.quantum.machines.qc-trace-simulator.intro)пакета разработки тактов.</span><span class="sxs-lookup"><span data-stu-id="509db-104">The invalidated qubits use checker is a part of the Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="509db-105">Его можно использовать для обнаружения потенциальных ошибок в коде, вызванных недопустимым Кубитс.</span><span class="sxs-lookup"><span data-stu-id="509db-105">You can use it to detect potential bugs in the code caused by invalid qubits.</span></span> 

## <a name="invalid-qubits"></a><span data-ttu-id="509db-106">Недопустимый Кубитс</span><span class="sxs-lookup"><span data-stu-id="509db-106">Invalid qubits</span></span>

<span data-ttu-id="509db-107">Рассмотрим следующий фрагмент кода, Q# чтобы продемонстрировать проблемы, обнаруженные недействительным Кубитс использованием средства проверки.</span><span class="sxs-lookup"><span data-stu-id="509db-107">Consider the following piece of Q# code to illustrate the issues detected by the invalidated qubits use checker:</span></span>

```qsharp
operation UseReleasedQubit() : Unit {
    mutable q = new Qubit[1];
    using (ans = Qubit()) {
        set q w/= 0 <- ans;
    }
    H(q[0]);
}
```

<span data-ttu-id="509db-108">При применении `H` операции к `q[0]` она указывает на уже выпущенную кубит, которая может привести к неопределенному поведению.</span><span class="sxs-lookup"><span data-stu-id="509db-108">When you apply the `H` operation to `q[0]`, it points to an already released qubit, which can cause undefined behavior.</span></span> <span data-ttu-id="509db-109">Если функция проверки использования непроверенных Кубитс включена, она создает исключение, `InvalidatedQubitsUseCheckerException` Если программа применяет операцию к уже выпущенной кубит.</span><span class="sxs-lookup"><span data-stu-id="509db-109">When the Invalidated Qubits Use Checker is enabled, it throws the exception `InvalidatedQubitsUseCheckerException` if the program applies an operation to an already released qubit.</span></span> <span data-ttu-id="509db-110">Для получения дополнительной информации см. <xref:Microsoft.Quantum.Simulation.QCTraceSimulatorRuntime.InvalidatedQubitsUseCheckerException>.</span><span class="sxs-lookup"><span data-stu-id="509db-110">For more information, see <xref:Microsoft.Quantum.Simulation.QCTraceSimulatorRuntime.InvalidatedQubitsUseCheckerException>.</span></span>

## <a name="invoking-the-invalidated-qubits-use-checker"></a><span data-ttu-id="509db-111">Вызов проверки непроверенного использования Кубитс</span><span class="sxs-lookup"><span data-stu-id="509db-111">Invoking the invalidated qubits use checker</span></span>

<span data-ttu-id="509db-112">Чтобы запустить симулятор трассировки тактов с проверкой непроверенного использования Кубитс, необходимо создать <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> экземпляр, присвоить `UseInvalidatedQubitsUseChecker` свойству **значение true**, а затем создать новый <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> экземпляр с `QCTraceSimulatorConfiguration` параметром в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="509db-112">To run the quantum trace simulator with the invalidated qubits use checker you must create a <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instance, set the `UseInvalidatedQubitsUseChecker` property to **true**, and then create a new <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instance with `QCTraceSimulatorConfiguration` as the parameter.</span></span> 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseInvalidatedQubitsUseChecker = true;
var sim = new QCTraceSimulator(config);
```


## <a name="using-the-invalidated-qubits-use-checker-in-a-c-host-program"></a><span data-ttu-id="509db-113">Использование недействительной проверки использования Кубитс в основной программе C#</span><span class="sxs-lookup"><span data-stu-id="509db-113">Using the invalidated qubits use checker in a C# host program</span></span>

<span data-ttu-id="509db-114">Ниже приведен пример ведущих программ C#, использующих симулятор трассировки тактов с включенной проверкой подлинности Кубитс.</span><span class="sxs-lookup"><span data-stu-id="509db-114">The following is an example of C# host programs that uses the quantum trace simulator with the invalidated qubits use checker enabled:</span></span> 

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

## <a name="see-also"></a><span data-ttu-id="509db-115">См. также</span><span class="sxs-lookup"><span data-stu-id="509db-115">See also</span></span>

- <span data-ttu-id="509db-116">Обзор [имитатора трассировки такта](xref:microsoft.quantum.machines.qc-trace-simulator.intro) в пакете разработки тактов.</span><span class="sxs-lookup"><span data-stu-id="509db-116">The Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
- <span data-ttu-id="509db-117"><xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator>Справочник по API.</span><span class="sxs-lookup"><span data-stu-id="509db-117">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API reference.</span></span>
- <span data-ttu-id="509db-118"><xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>Справочник по API.</span><span class="sxs-lookup"><span data-stu-id="509db-118">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API reference.</span></span>
- <span data-ttu-id="509db-119"><xref:Microsoft.Quantum.Simulation.QCTraceSimulatorRuntime.InvalidatedQubitsUseCheckerException>Справочник по API.</span><span class="sxs-lookup"><span data-stu-id="509db-119">The <xref:Microsoft.Quantum.Simulation.QCTraceSimulatorRuntime.InvalidatedQubitsUseCheckerException> API reference.</span></span>
