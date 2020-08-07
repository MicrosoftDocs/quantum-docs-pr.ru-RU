---
title: Средство проверки различных входов — пакет средств разработки тактов
description: Сведения о проверке различных входных данных Microsoft КДК, которая использует симулятор трассировки тактов для проверки Q# кода на наличие потенциальных конфликтов с общими Кубитс.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.distinct-inputs
no-loc:
- Q#
- $$v
ms.openlocfilehash: 750c94e7f861678d37f051619ff5b29bf4fd3d3e
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868276"
---
# <a name="quantum-trace-simulator-distinct-inputs-checker"></a><span data-ttu-id="0064b-103">Симулятор трассировки тактов: отдельный модуль проверки входных данных</span><span class="sxs-lookup"><span data-stu-id="0064b-103">Quantum trace simulator: distinct inputs checker</span></span>

<span data-ttu-id="0064b-104">Средство проверки индивидуальных входных значений входит в состав [симулятора тактовой](xref:microsoft.quantum.machines.qc-trace-simulator.intro)программы пакета разработки тактов.</span><span class="sxs-lookup"><span data-stu-id="0064b-104">The distinct inputs checker is a part of the Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="0064b-105">Его можно использовать для обнаружения потенциальных ошибок в коде, вызванных конфликтами с Shared Кубитс.</span><span class="sxs-lookup"><span data-stu-id="0064b-105">You can use it to detect potential bugs in the code caused by conflicts with shared qubits.</span></span> 

## <a name="conflicts-with-shared-qubits"></a><span data-ttu-id="0064b-106">Конфликты с общими Кубитс</span><span class="sxs-lookup"><span data-stu-id="0064b-106">Conflicts with shared qubits</span></span>

<span data-ttu-id="0064b-107">Рассмотрим следующий фрагмент кода, Q# чтобы продемонстрировать проблемы, обнаруженные при проверке различных входных значений:</span><span class="sxs-lookup"><span data-stu-id="0064b-107">Consider the following piece of Q# code to illustrate the issues detected by the distinct inputs checker:</span></span>

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

<span data-ttu-id="0064b-108">При просмотре этой программы можно предположить, что порядок, в котором она вызывает и не `op1` `op2` имеет значения, так как `q1` и `q2` является различными Кубитс и операциями, работающими с различными кубитсми.</span><span class="sxs-lookup"><span data-stu-id="0064b-108">When you look at this program, you can assume that the order in which it calls `op1` and `op2` does not matter, because `q1` and `q2` are different qubits and operations acting on different qubits commute.</span></span> 

<span data-ttu-id="0064b-109">Теперь рассмотрим следующий пример:</span><span class="sxs-lookup"><span data-stu-id="0064b-109">Now, consider this example:</span></span>

```qsharp
operation ApplyWithNonDistinctInputs() : Unit {
    using (qubits = Qubit[3]) {
        let op1 = CNOT(_, qubits[1]);
        let op2 = CNOT(qubits[1], _);
        ApplyBoth(qubits[0], qubits[2], op1, op2);
    }
}
```

<span data-ttu-id="0064b-110">Обратите внимание, что `op1` и `op2` они получаются с помощью частичного приложения и совместно используют кубит.</span><span class="sxs-lookup"><span data-stu-id="0064b-110">Note that `op1` and `op2` are both obtained using partial application and share a qubit.</span></span> <span data-ttu-id="0064b-111">При вызове `ApplyBoth` в этом примере результат операции зависит от порядка следования `op1` и `op2` внутреннего результата `ApplyBoth` .</span><span class="sxs-lookup"><span data-stu-id="0064b-111">When you call `ApplyBoth` in this example, the result of the operation depends on the order of `op1` and `op2` inside `ApplyBoth` - not what you would expect to happen.</span></span> <span data-ttu-id="0064b-112">При включении проверки различных входных параметров обнаруживает такие ситуации и создает исключение `DistinctInputsCheckerException` .</span><span class="sxs-lookup"><span data-stu-id="0064b-112">When you enable the distinct inputs checker, it detects such situations and throws a `DistinctInputsCheckerException`.</span></span> <span data-ttu-id="0064b-113">Дополнительные сведения см <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException> . в разделе Q# библиотеки API.</span><span class="sxs-lookup"><span data-stu-id="0064b-113">For more information, see <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException> in the Q# API library.</span></span>

## <a name="invoking-the-distinct-inputs-checker"></a><span data-ttu-id="0064b-114">Вызов средства проверки различных значений</span><span class="sxs-lookup"><span data-stu-id="0064b-114">Invoking the distinct inputs checker</span></span>

<span data-ttu-id="0064b-115">Чтобы запустить симулятор трассировки тактов с помощью средства проверки различных входных данных, необходимо создать <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> экземпляр, присвоить `UseDistinctInputsChecker` свойству **значение true**, а затем создать новый <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> экземпляр с `QCTraceSimulatorConfiguration` параметром в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="0064b-115">To run the quantum trace simulator with the distinct inputs checker you must create a <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instance, set the `UseDistinctInputsChecker` property to **true**, and then create a new <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instance with `QCTraceSimulatorConfiguration` as the parameter.</span></span> 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseDistinctInputsChecker = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-distinct-inputs-checker-in-a-c-host-program"></a><span data-ttu-id="0064b-116">Использование средства проверки различных входных значений в управляющей программе C#</span><span class="sxs-lookup"><span data-stu-id="0064b-116">Using the distinct inputs checker in a C# host program</span></span>

<span data-ttu-id="0064b-117">Ниже приведен пример основной программы C#, которая использует симулятор трассировки тактов с включенным средством проверки различных входных значений:</span><span class="sxs-lookup"><span data-stu-id="0064b-117">The following is an example of C# host program that uses the quantum trace simulator with the distinct inputs checker enabled:</span></span>

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

## <a name="see-also"></a><span data-ttu-id="0064b-118">См. также</span><span class="sxs-lookup"><span data-stu-id="0064b-118">See also</span></span>

- <span data-ttu-id="0064b-119">Обзор [имитатора трассировки такта](xref:microsoft.quantum.machines.qc-trace-simulator.intro) в пакете разработки тактов.</span><span class="sxs-lookup"><span data-stu-id="0064b-119">The Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
- <span data-ttu-id="0064b-120"><xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator>Справочник по API.</span><span class="sxs-lookup"><span data-stu-id="0064b-120">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API reference.</span></span>
- <span data-ttu-id="0064b-121"><xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>Справочник по API.</span><span class="sxs-lookup"><span data-stu-id="0064b-121">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API reference.</span></span>
- <span data-ttu-id="0064b-122"><xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException>Справочник по API.</span><span class="sxs-lookup"><span data-stu-id="0064b-122">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException> API reference.</span></span>
