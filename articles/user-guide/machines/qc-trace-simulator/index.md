---
title: Квантовый симулятор трассировки — пакет средств разработки Quantum
description: Сведения о том, как с помощью симулятора трассировки квантового компьютера от Майкрософт выполнять отладку классического кода и оценивать требования к ресурсам для программы Q#.
author: vadym-kl
ms.author: vadym
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.intro
no-loc:
- Q#
- $$v
ms.openlocfilehash: 54a1f63461cfcc8146f7dc4d18d321238d77454d
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/21/2020
ms.locfileid: "90833356"
---
# <a name="microsoft-quantum-development-kit-qdk-quantum-trace-simulator"></a><span data-ttu-id="fac75-103">Пакет средств разработки Microsoft Quantum (QDK) — квантовый симулятор трассировки</span><span class="sxs-lookup"><span data-stu-id="fac75-103">Microsoft Quantum Development Kit (QDK) quantum trace simulator</span></span>

<span data-ttu-id="fac75-104">QDK <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> выполняет квантовую программу без фактической имитации состояния квантового компьютера.</span><span class="sxs-lookup"><span data-stu-id="fac75-104">The QDK <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> class runs a quantum program without actually simulating the state of a quantum computer.</span></span> <span data-ttu-id="fac75-105">По этой причине квантовый симулятор трассировки может выполнять квантовые программы, использующие тысячи кубитов.</span><span class="sxs-lookup"><span data-stu-id="fac75-105">For this reason, the quantum trace simulator is able to run quantum programs that use thousands of qubits.</span></span>  <span data-ttu-id="fac75-106">Это полезно для двух основных целей:</span><span class="sxs-lookup"><span data-stu-id="fac75-106">It is useful for two main purposes:</span></span> 

* <span data-ttu-id="fac75-107">Отладка классического кода, который является частью квантовой программы.</span><span class="sxs-lookup"><span data-stu-id="fac75-107">Debugging classical code that is part of a quantum program.</span></span> 
* <span data-ttu-id="fac75-108">Оценка ресурсов, необходимых для запуска заданного экземпляра квантовой программы на квантовом компьютере.</span><span class="sxs-lookup"><span data-stu-id="fac75-108">Estimating the resources required to run a given instance of a quantum program on a quantum computer.</span></span> <span data-ttu-id="fac75-109">[Оценщик ресурсов](xref:microsoft.quantum.machines.resources-estimator), который предоставляет более ограниченный набор метрик, создано на основе симулятора трассировки.</span><span class="sxs-lookup"><span data-stu-id="fac75-109">In fact, the [Resources estimator](xref:microsoft.quantum.machines.resources-estimator), which provides a more limited set of metrics, is built upon the trace simulator.</span></span>

## <a name="invoking-the-quantum-trace-simulator"></a><span data-ttu-id="fac75-110">Вызов квантового симулятора трассировки</span><span class="sxs-lookup"><span data-stu-id="fac75-110">Invoking the quantum trace simulator</span></span>

<span data-ttu-id="fac75-111">Вы можете использовать квантовый симулятор трассировки для выполнения любой операции Q#.</span><span class="sxs-lookup"><span data-stu-id="fac75-111">You can use the quantum trace simulator to run any Q# operation.</span></span>

<span data-ttu-id="fac75-112">Как и в случае с другими целевыми компьютерами, вам сначала нужно создать экземпляр класса `QCTraceSimulator`, а затем передать его в качестве первого параметра метода `Run` операции.</span><span class="sxs-lookup"><span data-stu-id="fac75-112">As with other target machines, you first create an instance of the `QCTraceSimulator` class and then pass it as the first parameter of an operation's `Run` method.</span></span>

<span data-ttu-id="fac75-113">Учтите, что в отличие от класса `QuantumSimulator` класс `QCTraceSimulator` не реализует интерфейс <xref:System.IDisposable>, поэтому вам не нужно заключать его в оператор `using`.</span><span class="sxs-lookup"><span data-stu-id="fac75-113">Note that, unlike the `QuantumSimulator` class, the `QCTraceSimulator` class does not implement the <xref:System.IDisposable> interface, and thus you do not need to enclose it within a `using` statement.</span></span>

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
            var res = MyQuantumProgram.Run(sim).Result;
            System.Console.WriteLine("Press any key to continue...");
            System.Console.ReadKey();
        }
    }
}
```

## <a name="providing-the-probability-of-measurement-outcomes"></a><span data-ttu-id="fac75-114">Предоставление вероятности результатов измерения</span><span class="sxs-lookup"><span data-stu-id="fac75-114">Providing the probability of measurement outcomes</span></span>

<span data-ttu-id="fac75-115">Так как квантовый симулятор трассировки не имитирует фактическое квантовое состояние, он не может вычислить вероятность результатов измерения в операции.</span><span class="sxs-lookup"><span data-stu-id="fac75-115">Because the quantum trace simulator does not simulate the actual quantum state, it cannot calculate the probability of measurement outcomes within an operation.</span></span> 

<span data-ttu-id="fac75-116">Таким образом, если операция включает измерения, необходимо явно предоставить эти вероятности с помощью операции <xref:microsoft.quantum.diagnostics.assertmeasurementprobability> из пространства имен <xref:microsoft.quantum.diagnostics>.</span><span class="sxs-lookup"><span data-stu-id="fac75-116">Therefore, if an operation includes measurements, you must explicitly provide these probabilities using the <xref:microsoft.quantum.diagnostics.assertmeasurementprobability> operation from the <xref:microsoft.quantum.diagnostics> namespace.</span></span> <span data-ttu-id="fac75-117">Проиллюстрируем это на примере.</span><span class="sxs-lookup"><span data-stu-id="fac75-117">The following example illustrates this:</span></span>

```qsharp
operation TeleportQubit(source : Qubit, target : Qubit) : Unit {
    using (qubit = Qubit()) {
        H(qubit);
        CNOT(qubit, target);
        CNOT(source, qubit);
        H(source);

        AssertMeasurementProbability([PauliZ], [source], Zero, 0.5, "Outcomes must be equally likely", 1e-5);
        AssertMeasurementProbability([PauliZ], [q], Zero, 0.5, "Outcomes must be equally likely", 1e-5);

        if (M(source) == One)  { Z(target); X(source); }
        if (M(q) == One) { X(target); X(q); }
    }
}
```

<span data-ttu-id="fac75-118">Когда квантовый симулятор трассировки вычисляет `AssertMeasurementProbability`, он записывает измерение `PauliZ` в `source`, и ожидается, что `q` выдаст результат `Zero` с вероятностью **0,5**.</span><span class="sxs-lookup"><span data-stu-id="fac75-118">When the quantum trace simulator encounters `AssertMeasurementProbability` it records that measuring `PauliZ` on `source` and `q` should give an outcome of `Zero`, with probability **0.5**.</span></span> <span data-ttu-id="fac75-119">При выполнении операции `M` в дальнейшем он находит записанные значения вероятностей результата, и `M` возвращает `Zero` или `One` с вероятностью **0,5**.</span><span class="sxs-lookup"><span data-stu-id="fac75-119">When it runs the `M` operation later, it finds the recorded values of the outcome probabilities, and `M` returns `Zero` or `One`, with probability **0.5**.</span></span> <span data-ttu-id="fac75-120">Если один и тот же код выполняется в симуляторе, который отслеживает квантовое состояние, такой симулятор проверяет правильность предоставленных вероятностей в `AssertMeasurementProbability`.</span><span class="sxs-lookup"><span data-stu-id="fac75-120">When the same code runs on a simulator that keeps track of the quantum state, that simulator checks that the provided probabilities in `AssertMeasurementProbability` are correct.</span></span>

<span data-ttu-id="fac75-121">Учтите, что, если есть хотя бы одна операция измерения, не помеченная с помощью `AssertMeasurementProbability`, симулятор выдаст [`UnconstrainedMeasurementException`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.unconstrainedmeasurementexception).</span><span class="sxs-lookup"><span data-stu-id="fac75-121">Note that if there is at least one measurement operation that is not annotated using `AssertMeasurementProbability`, the simulator throws an [`UnconstrainedMeasurementException`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.unconstrainedmeasurementexception).</span></span>

## <a name="quantum-trace-simulator-tools"></a><span data-ttu-id="fac75-122">Средства квантового симулятора трассировки</span><span class="sxs-lookup"><span data-stu-id="fac75-122">Quantum trace simulator tools</span></span>

<span data-ttu-id="fac75-123">QDK включает пять средств, которые можно использовать с квантовым симулятором трассировки для обнаружения ошибок в программах и выполнения оценки ресурсов квантовой программы.</span><span class="sxs-lookup"><span data-stu-id="fac75-123">The QDK includes five tools that you can use with the quantum trace simulator to detect bugs in your programs and perform quantum program resource estimates:</span></span> 

|<span data-ttu-id="fac75-124">Средство</span><span class="sxs-lookup"><span data-stu-id="fac75-124">Tool</span></span> | <span data-ttu-id="fac75-125">Описание</span><span class="sxs-lookup"><span data-stu-id="fac75-125">Description</span></span> |
|-----| -----|
|[<span data-ttu-id="fac75-126">Средство проверки уникальных значений</span><span class="sxs-lookup"><span data-stu-id="fac75-126">Distinct inputs checker</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs) |<span data-ttu-id="fac75-127">Проверяет наличие потенциальных конфликтов с использованием общих кубитов.</span><span class="sxs-lookup"><span data-stu-id="fac75-127">Checks for potential conflicts with shared qubits</span></span> |
|[<span data-ttu-id="fac75-128">Средство проверки недействительных кубитов</span><span class="sxs-lookup"><span data-stu-id="fac75-128">Invalidated qubits use checker</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits)  |<span data-ttu-id="fac75-129">Проверяет, применяет ли программа операцию к кубиту, который уже выпущен.</span><span class="sxs-lookup"><span data-stu-id="fac75-129">Checks if the program applies an operation to a qubit that is already released</span></span> |
|[<span data-ttu-id="fac75-130">Счетчик примитивных операций</span><span class="sxs-lookup"><span data-stu-id="fac75-130">Primitive operations counter</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.primitive-counter)  | <span data-ttu-id="fac75-131">Подсчитывает количество примитивных процессов, которые используются каждой операцией, вызываемой в квантовой программе.</span><span class="sxs-lookup"><span data-stu-id="fac75-131">Counts the number of primitive processes used by every operation invoked in a quantum program</span></span>  |
|[<span data-ttu-id="fac75-132">Измеритель глубины</span><span class="sxs-lookup"><span data-stu-id="fac75-132">Depth counter</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter)  |<span data-ttu-id="fac75-133">Собирает счетчики, представляющие нижнюю границу глубины каждой операции, вызываемой в квантовой программе.</span><span class="sxs-lookup"><span data-stu-id="fac75-133">Gathers counts that represent the lower bound of the depth of every operation invoked in a quantum program</span></span>   |
|[<span data-ttu-id="fac75-134">Измеритель ширины</span><span class="sxs-lookup"><span data-stu-id="fac75-134">Width counter</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter)  |<span data-ttu-id="fac75-135">Подсчитывает количество кубитов, выделенных и заимствованных каждой операцией в квантовой программе.</span><span class="sxs-lookup"><span data-stu-id="fac75-135">Counts the number of qubits allocated and borrowed by each operation in a quantum program</span></span> |

<span data-ttu-id="fac75-136">Каждое из этих средств включается путем установки соответствующих флагов в `QCTraceSimulatorConfiguration` и последующей передачи конфигурации в объявление `QCTraceSimulator`.</span><span class="sxs-lookup"><span data-stu-id="fac75-136">Each of these tools is enabled by setting appropriate flags in `QCTraceSimulatorConfiguration` and then passing the configuration to the `QCTraceSimulator` declaration.</span></span> <span data-ttu-id="fac75-137">Сведения об использовании каждого из этих средств см. в приведенных выше ссылках.</span><span class="sxs-lookup"><span data-stu-id="fac75-137">For information on using each of these tools, see the links in the preceding list.</span></span> <span data-ttu-id="fac75-138">Дополнительные сведения о настройке `QCTraceSimulator` см. в разделе [QCTraceSimulatorConfiguration](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration).</span><span class="sxs-lookup"><span data-stu-id="fac75-138">For more information about configuring `QCTraceSimulator`, see [QCTraceSimulatorConfiguration](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration).</span></span>

## <a name="qctracesimulator-methods"></a><span data-ttu-id="fac75-139">Методы QCTraceSimulator</span><span class="sxs-lookup"><span data-stu-id="fac75-139">QCTraceSimulator methods</span></span>

<span data-ttu-id="fac75-140">В `QCTraceSimulator` есть несколько встроенных методов для получения значений метрик, которые отслеживаются во время квантовой операции.</span><span class="sxs-lookup"><span data-stu-id="fac75-140">`QCTraceSimulator` has several built-in methods to retrieve the values of the metrics tracked during a quantum operation.</span></span> <span data-ttu-id="fac75-141">Примеры методов [QCTraceSimulator.GetMetric](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) и [QCTraceSimulator.ToCSV](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.tocsv) см. в статьях, посвященных [счетчику примитивных операций](xref:microsoft.quantum.machines.qc-trace-simulator.primitive-counter), [измерителю глубины](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter) и [измерителю ширины](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter).</span><span class="sxs-lookup"><span data-stu-id="fac75-141">Examples of the [QCTraceSimulator.GetMetric](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) and the [QCTraceSimulator.ToCSV](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.tocsv) methods can be found in the [Primitive operations counter](xref:microsoft.quantum.machines.qc-trace-simulator.primitive-counter), [Depth counter](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter), and [Width counter](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter) articles.</span></span> <span data-ttu-id="fac75-142">Дополнительные сведения обо всех доступных методах см. в разделе [QCTraceSimulator](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) в справочнике по API Q#.</span><span class="sxs-lookup"><span data-stu-id="fac75-142">For more information on all available methods, see [QCTraceSimulator](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) in the Q# API reference.</span></span>  

## <a name="see-also"></a><span data-ttu-id="fac75-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fac75-143">See also</span></span>

- [<span data-ttu-id="fac75-144">Квантовый оценщик ресурсов</span><span class="sxs-lookup"><span data-stu-id="fac75-144">Quantum resources estimator</span></span>](xref:microsoft.quantum.machines.resources-estimator)
- [<span data-ttu-id="fac75-145">Квантовый симулятор Тоффоли</span><span class="sxs-lookup"><span data-stu-id="fac75-145">Quantum Toffoli simulator</span></span>](xref:microsoft.quantum.machines.toffoli-simulator)
- [<span data-ttu-id="fac75-146">Квантовый симулятор полного состояния</span><span class="sxs-lookup"><span data-stu-id="fac75-146">Quantum full state simulator</span></span>](xref:microsoft.quantum.machines.full-state-simulator) 