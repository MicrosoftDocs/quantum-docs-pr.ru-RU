---
title: Симулятор трассировки квантового компьютера
description: Узнайте, как с помощью симулятора трассировки компьютера Microsoft Quantum выполнять отладку классического кода и оценивать требования к ресурсам для квантовой программы.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.intro
ms.openlocfilehash: 72c259933d2df8f79319e6c0c65ae181a9f9cff3
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/28/2020
ms.locfileid: "77906089"
---
# <a name="quantum-trace-simulator"></a><span data-ttu-id="85e5c-103">Квантовый симулятор трассировки</span><span class="sxs-lookup"><span data-stu-id="85e5c-103">Quantum Trace Simulator</span></span>

<span data-ttu-id="85e5c-104">Симулятор трассировки квантового компьютера Microsoft выполняет квантовую программу без фактической симуляции состояния квантового компьютера.</span><span class="sxs-lookup"><span data-stu-id="85e5c-104">The Microsoft quantum computer trace simulator executes a quantum program without actually simulating the state of a quantum computer.</span></span>  <span data-ttu-id="85e5c-105">По этой причине симулятор трассировки может выполнять квантовые программы, использующие тысячи кубитов.</span><span class="sxs-lookup"><span data-stu-id="85e5c-105">For this reason, the trace simulator can execute quantum programs that use thousands of qubits.</span></span>  <span data-ttu-id="85e5c-106">Это полезно для двух основных целей:</span><span class="sxs-lookup"><span data-stu-id="85e5c-106">It is useful for two main purposes:</span></span> 

* <span data-ttu-id="85e5c-107">Отладка классического кода, который является частью квантовой программы.</span><span class="sxs-lookup"><span data-stu-id="85e5c-107">Debugging classical code that is part of a quantum program.</span></span> 
* <span data-ttu-id="85e5c-108">Оценка ресурсов, необходимых для запуска заданного экземпляра квантовой программы на квантовом компьютере.</span><span class="sxs-lookup"><span data-stu-id="85e5c-108">Estimating the resources required to run a given instance of a quantum program on a quantum computer.</span></span>

<span data-ttu-id="85e5c-109">В симуляторе трассировки используются дополнительные сведения, предоставляемые пользователем, когда необходимо выполнить измерения.</span><span class="sxs-lookup"><span data-stu-id="85e5c-109">The trace simulator relies on additional information provided by the user when measurements must be performed.</span></span> <span data-ttu-id="85e5c-110">Дополнительные сведения об этом см. в разделе [Providing the Probability of Measurement Outcomes](#providing-the-probability-of-measurement-outcomes) (Предоставление вероятности результатов измерения.</span><span class="sxs-lookup"><span data-stu-id="85e5c-110">See Section [Providing the probability of measurement outcomes](#providing-the-probability-of-measurement-outcomes) for more details on this.</span></span> 

## <a name="providing-the-probability-of-measurement-outcomes"></a><span data-ttu-id="85e5c-111">Предоставление вероятности результатов измерения</span><span class="sxs-lookup"><span data-stu-id="85e5c-111">Providing the Probability of Measurement Outcomes</span></span>

<span data-ttu-id="85e5c-112">Существует два типа измерений, которые отображаются в квантовых алгоритмах.</span><span class="sxs-lookup"><span data-stu-id="85e5c-112">There are two kinds of measurements that appear in quantum algorithms.</span></span> <span data-ttu-id="85e5c-113">Первый тип играет вспомогательную роль, где пользователь обычно знает вероятность результатов.</span><span class="sxs-lookup"><span data-stu-id="85e5c-113">The first kind plays an auxiliary role where the user usually knows the probability of the outcomes.</span></span> <span data-ttu-id="85e5c-114">В этом случае пользователь может записывать <xref:microsoft.quantum.intrinsic.assertprob> из пространства имен <xref:microsoft.quantum.intrinsic>, чтобы выразить этот набор знаний.</span><span class="sxs-lookup"><span data-stu-id="85e5c-114">In this case the user can write <xref:microsoft.quantum.intrinsic.assertprob> from the <xref:microsoft.quantum.intrinsic> namespace to express this knowledge.</span></span> <span data-ttu-id="85e5c-115">Проиллюстрируем это на примере.</span><span class="sxs-lookup"><span data-stu-id="85e5c-115">The following example illustrates this:</span></span>

```qsharp
operation TeleportQubit(source : Qubit, target : Qubit) : Unit {
    using (qubit = Qubit()) {
        H(qubit);
        CNOT(qubit, target);
        CNOT(source, qubit);
        H(source);

        AssertProb([PauliZ], [source], Zero, 0.5, "Outcomes must be equally likely", 1e-5);
        AssertProb([PauliZ], [q], Zero, 0.5, "Outcomes must be equally likely", 1e-5);

        if (M(source) == One)  { Z(target); X(source); }
        if (M(q) == One) { X(target); X(q); }
    }
}
```

<span data-ttu-id="85e5c-116">При выполнении `AssertProb` симулятором трассировки он записывает измерения `PauliZ` в `source` и `q` должен получить результат `Zero` с вероятностью 0,5.</span><span class="sxs-lookup"><span data-stu-id="85e5c-116">When the trace simulator executes `AssertProb` it will record that measuring `PauliZ` on `source` and `q` should be given an outcome of `Zero` with probability 0.5.</span></span> <span data-ttu-id="85e5c-117">Когда симулятор выполняет `M` позже, он найдет записанные значения вероятностей результата и `M` возвратит `Zero` или `One` с вероятностью 0,5.</span><span class="sxs-lookup"><span data-stu-id="85e5c-117">When the simulator executes `M` later, it will find the recorded values of the outcome probabilities and `M` will return `Zero` or `One` with probability 0.5.</span></span> <span data-ttu-id="85e5c-118">Если один и тот же код выполняется в симуляторе, который отслеживает квантовое состояние, такой симулятор проверяет правильность предоставленных вероятностей в `AssertProb`.</span><span class="sxs-lookup"><span data-stu-id="85e5c-118">When the same code is executed on a simulator that keeps track of the quantum state, such a simulator will check that the provided probabilities in `AssertProb` are correct.</span></span>

## <a name="running-your-program-with-the-quantum-computer-trace-simulator"></a><span data-ttu-id="85e5c-119">Запуск программы с симулятором трассировки квантового компьютера</span><span class="sxs-lookup"><span data-stu-id="85e5c-119">Running your Program with the Quantum Computer Trace Simulator</span></span> 

<span data-ttu-id="85e5c-120">Симулятор трассировки квантового компьютера можно рассматривать как еще один целевой компьютер.</span><span class="sxs-lookup"><span data-stu-id="85e5c-120">The quantum computer trace simulator may be viewed as just another target machine.</span></span> <span data-ttu-id="85e5c-121">Программа драйвера C# очень похожа на программу для любого другого квантового симулятора:</span><span class="sxs-lookup"><span data-stu-id="85e5c-121">The C# driver program for using it is very similar to the one for any other quantum Simulator:</span></span> 

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
            QCTraceSimulator sim = new QCTraceSimulator();
            var res = MyQuantumProgram.Run().Result;
            System.Console.WriteLine("Press any key to continue...");
            System.Console.ReadKey();
        }
    }
}
```

<span data-ttu-id="85e5c-122">Обратите внимание, что если имеется хотя бы одно измерение, не помеченное с помощью `AssertProb`, симулятор выдаст `UnconstrainedMeasurementException` из пространства имен `Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators`.</span><span class="sxs-lookup"><span data-stu-id="85e5c-122">Note that if there is at least one measurement not annotated using `AssertProb`, the simulator will throw `UnconstrainedMeasurementException` from the `Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators` namespace.</span></span> <span data-ttu-id="85e5c-123">Дополнительные сведения см. в документации по API [UnconstrainedMeasurementException](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.UnconstrainedMeasurementException) (Неограниченное исключение измерения).</span><span class="sxs-lookup"><span data-stu-id="85e5c-123">See the API documentation on [UnconstrainedMeasurementException](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.UnconstrainedMeasurementException) for more details.</span></span>

<span data-ttu-id="85e5c-124">В дополнение к запущенным квантовым программам симулятор трассировки включает пять компонентов для обнаружения ошибок в программах и выполнения оценки ресурсов квантовых программ:</span><span class="sxs-lookup"><span data-stu-id="85e5c-124">In addition to running quantum programs, the trace simulator comes with five components for detecting bugs in programs and performing quantum program resource estimates:</span></span> 

* [<span data-ttu-id="85e5c-125">Средство проверки уникальных значений</span><span class="sxs-lookup"><span data-stu-id="85e5c-125">Distinct Inputs Checker</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs)
* [<span data-ttu-id="85e5c-126">Средство проверки недействительных кубитов</span><span class="sxs-lookup"><span data-stu-id="85e5c-126">Invalidated Qubits Use Checker</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits)
* [<span data-ttu-id="85e5c-127">Счетчик примитивных операций</span><span class="sxs-lookup"><span data-stu-id="85e5c-127">Primitive Operations Counter</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.primitive-counter)
* <span data-ttu-id="85e5c-128">[Circuit Depth Counter](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter) (Счетчик глубины канала)</span><span class="sxs-lookup"><span data-stu-id="85e5c-128">[Circuit Depth Counter](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter)</span></span>
* <span data-ttu-id="85e5c-129">[Circuit Width Counter](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter) (Счетчик ширины канала)</span><span class="sxs-lookup"><span data-stu-id="85e5c-129">[Circuit Width Counter](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter)</span></span>

<span data-ttu-id="85e5c-130">Каждый из этих компонентов можно включить, установив соответствующие флажки в `QCTraceSimulatorConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="85e5c-130">Each of these components may be enabled by setting appropriate flags in `QCTraceSimulatorConfiguration`.</span></span> <span data-ttu-id="85e5c-131">Дополнительные сведения об использовании каждого из этих компонентов приведены в соответствующих справочных файлах.</span><span class="sxs-lookup"><span data-stu-id="85e5c-131">More details about using each of these components are provided in the corresponding reference files.</span></span> <span data-ttu-id="85e5c-132">Конкретные сведения см. в документации API [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration) (Настройка симулятора трассировки QC).</span><span class="sxs-lookup"><span data-stu-id="85e5c-132">See the API documentation on [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration) for specific details.</span></span>

## <a name="see-also"></a><span data-ttu-id="85e5c-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="85e5c-133">See also</span></span>
<span data-ttu-id="85e5c-134">Справочник по C# [симулятора трассировки](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) квантового компьютера</span><span class="sxs-lookup"><span data-stu-id="85e5c-134">The quantum computer [trace simulator](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) C# reference</span></span> 

