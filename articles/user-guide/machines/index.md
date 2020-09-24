---
title: Квантовые симуляторы и программы Q#
description: Описание квантовых симуляторов, доступных в качестве целевых компьютеров для программ Q#.
author: QuantumWriter
ms.author: v-benbra
ms.date: 6/17/2020
ms.topic: article
uid: microsoft.quantum.machines
no-loc:
- Q#
- $$v
ms.openlocfilehash: 6a2a4bb829301f9db9bd14f3240556a403b9a54f
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/21/2020
ms.locfileid: "90833425"
---
# <a name="quantum-simulators"></a><span data-ttu-id="46b50-103">Квантовые симуляторы</span><span class="sxs-lookup"><span data-stu-id="46b50-103">Quantum simulators</span></span>

<span data-ttu-id="46b50-104">Квантовые симуляторы — это компьютерные программы, которые выполняются на традиционных компьютерах и которые действуют как *целевые компьютеры* для программы Q#. Они позволяют запускать и тестировать квантовые программы в среде, которая прогнозирует поведение кубитов в ответ на разные операции.</span><span class="sxs-lookup"><span data-stu-id="46b50-104">Quantum simulators are software programs that run on classical computers and act as the *target machine* for a Q# program, making it possible to run and test quantum programs in an environment that predicts how qubits will react to different operations.</span></span> <span data-ttu-id="46b50-105">В этой статье показано, какие квантовые симуляторы включены в пакет средств разработки Quantum (QDK), а также описаны разные способы передачи программы Q# в квантовые симуляторы, например с помощью командной строки или кода драйвера, написанного на классическом языке.</span><span class="sxs-lookup"><span data-stu-id="46b50-105">This article describes which quantum simulators are included with the Quantum Development Kit (QDK), and different ways that you can pass a Q# program to the quantum simulators, for example, via the command line or by using driver code written in a classical language.</span></span>  



## <a name="the-quantum-development-kit-qdk-quantum-simulators"></a><span data-ttu-id="46b50-106">Пакет средств разработки Quantum (QDK) — квантовые симуляторы</span><span class="sxs-lookup"><span data-stu-id="46b50-106">The Quantum Development Kit (QDK) quantum simulators</span></span>

<span data-ttu-id="46b50-107">Квантовый симулятор выполняет реализации квантовых примитивов для алгоритма.</span><span class="sxs-lookup"><span data-stu-id="46b50-107">The quantum simulator is responsible for providing implementations of quantum primitives for an algorithm.</span></span> <span data-ttu-id="46b50-108">Сюда входят такие примитивные операции, такие как `H`, `CNOT` и `Measure`, а также управление кубитами и их отслеживание.</span><span class="sxs-lookup"><span data-stu-id="46b50-108">This includes primitive operations such as `H`, `CNOT`, and `Measure`, as well as qubit management and tracking.</span></span> <span data-ttu-id="46b50-109">Пакет QDK включает разные классы квантовых симуляторов, которые представляют разные модели выполнения для одного и того же квантового алгоритма.</span><span class="sxs-lookup"><span data-stu-id="46b50-109">The QDK includes different classes of quantum simulators representing different run models for the same quantum algorithm.</span></span> 


<span data-ttu-id="46b50-110">Каждый тип квантового симулятора может предоставлять различные реализации этих примитивов.</span><span class="sxs-lookup"><span data-stu-id="46b50-110">Each type of quantum simulator can provide different implementations of these primitives.</span></span> <span data-ttu-id="46b50-111">Например, [симулятор полного состояния](xref:microsoft.quantum.machines.full-state-simulator) выполняет квантовый алгоритм путем полной имитации [вектора квантового состояния](xref:microsoft.quantum.glossary#quantum-state), в то время как [симулятор трассировки квантового компьютера](xref:microsoft.quantum.machines.qc-trace-simulator.intro) не учитывает фактическое квантовое состояние.</span><span class="sxs-lookup"><span data-stu-id="46b50-111">For example, the [full state simulator](xref:microsoft.quantum.machines.full-state-simulator) runs the quantum algorithm by fully simulating the [quantum state vector](xref:microsoft.quantum.glossary#quantum-state), whereas the [quantum computer trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) doesn't consider the actual quantum state at all.</span></span> <span data-ttu-id="46b50-112">Вместо этого он отслеживает использование шлюза, кубита и других ресурсов для алгоритма.</span><span class="sxs-lookup"><span data-stu-id="46b50-112">Rather, it tracks gate, qubit, and other resource usage for the algorithm.</span></span>

### <a name="quantum-machine-classes"></a><span data-ttu-id="46b50-113">Классы квантовых компьютеров</span><span class="sxs-lookup"><span data-stu-id="46b50-113">Quantum machine classes</span></span>

<span data-ttu-id="46b50-114">В будущем в QDK будут определены дополнительные классы квантовых компьютеров для реализации других типов имитирования и выполнения на квантовом аппаратном обеспечении.</span><span class="sxs-lookup"><span data-stu-id="46b50-114">In the future, the QDK will define additional quantum machine classes to support other types of simulation and to support running on quantum hardware.</span></span> <span data-ttu-id="46b50-115">Благодаря тому, что алгоритм остается постоянным при изменяющихся базовых реализациях машины, упрощается тестирование и отладка алгоритма в моделировании, а также его запуск на реальном оборудовании. При этом вы можете быть уверены, что алгоритм не изменился.</span><span class="sxs-lookup"><span data-stu-id="46b50-115">Allowing the algorithm to stay constant while varying the underlying machine implementation makes it easy to test and debug an algorithm in simulation and then run it on real hardware with confidence that the algorithm hasn't changed.</span></span>

<span data-ttu-id="46b50-116">QDK включает несколько классов квантовых компьютеров. Все они определены в пространстве имен `Microsoft.Quantum.Simulation.Simulators`.</span><span class="sxs-lookup"><span data-stu-id="46b50-116">The QDK includes several quantum machine classes, all defined in the `Microsoft.Quantum.Simulation.Simulators` namespace.</span></span>

|<span data-ttu-id="46b50-117">Симулятор</span><span class="sxs-lookup"><span data-stu-id="46b50-117">Simulator</span></span> |<span data-ttu-id="46b50-118">Класс</span><span class="sxs-lookup"><span data-stu-id="46b50-118">Class</span></span>|<span data-ttu-id="46b50-119">Описание</span><span class="sxs-lookup"><span data-stu-id="46b50-119">Description</span></span>|
|-----|------|---|
|[<span data-ttu-id="46b50-120">Симулятор полного состояния</span><span class="sxs-lookup"><span data-stu-id="46b50-120">Full state simulator</span></span>](xref:microsoft.quantum.machines.full-state-simulator)| `QuantumSimulator` | <span data-ttu-id="46b50-121">Выполняет и отлаживает квантовые алгоритмы. Ограничение — примерно 30 кубитов.</span><span class="sxs-lookup"><span data-stu-id="46b50-121">Runs and debugs quantum algorithms, and is limited to about 30 qubits.</span></span> |
|[<span data-ttu-id="46b50-122">Простой оценщик ресурсов</span><span class="sxs-lookup"><span data-stu-id="46b50-122">Simple resources estimator</span></span>](xref:microsoft.quantum.machines.resources-estimator)| `ResourcesEstimator` | <span data-ttu-id="46b50-123">Выполняет анализ ресурсов верхнего уровня, необходимый для выполнения квантового алгоритма. Ограничение — тысячи кубитов.</span><span class="sxs-lookup"><span data-stu-id="46b50-123">Performs a top level analysis of the resources needed to run a quantum algorithm, and supports thousands of qubits.</span></span>|
|[<span data-ttu-id="46b50-124">Оценщик ресурсов на основе трассировки</span><span class="sxs-lookup"><span data-stu-id="46b50-124">Trace-based resource estimator</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.intro)|  `QCTraceSimulator` |<span data-ttu-id="46b50-125">Выполняет расширенный анализ потребления ресурсов для всего графа вызовов алгоритма. Ограничение — тысячи кубитов.</span><span class="sxs-lookup"><span data-stu-id="46b50-125">Runs advanced analysis of resources consumptions for the algorithm's entire call-graph, and supports thousands of qubits.</span></span>|
|[<span data-ttu-id="46b50-126">Симулятор Тоффоли</span><span class="sxs-lookup"><span data-stu-id="46b50-126">Toffoli simulator</span></span>](xref:microsoft.quantum.machines.toffoli-simulator)| `ToffoliSimulator` |<span data-ttu-id="46b50-127">Имитирует квантовые алгоритмы, которые ограничиваются операциями `X` и `CNOT`, а также многоуправляемыми квантовыми операциями `X`. Ограничение — миллионы кубитов.</span><span class="sxs-lookup"><span data-stu-id="46b50-127">Simulates quantum algorithms that are limited to `X`, `CNOT`, and multi-controlled `X` quantum operations, and supports million of qubits.</span></span> |

## <a name="invoking-the-quantum-simulator"></a><span data-ttu-id="46b50-128">Вызов квантового симулятора</span><span class="sxs-lookup"><span data-stu-id="46b50-128">Invoking the quantum simulator</span></span>

<span data-ttu-id="46b50-129">В статье [Способы выполнения программы Q#](xref:microsoft.quantum.guide.host-programs) показаны три способа передачи кода Q# в квантовый симулятор:</span><span class="sxs-lookup"><span data-stu-id="46b50-129">In [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs), three ways of passing the Q# code to the quantum simulator are demonstrated:</span></span> 

* <span data-ttu-id="46b50-130">с помощью командной строки;</span><span class="sxs-lookup"><span data-stu-id="46b50-130">Using the command line</span></span>
* <span data-ttu-id="46b50-131">с помощью основной программы Python;</span><span class="sxs-lookup"><span data-stu-id="46b50-131">Using a Python host program</span></span>
* <span data-ttu-id="46b50-132">с помощью основной программы C#.</span><span class="sxs-lookup"><span data-stu-id="46b50-132">Using a C# host program</span></span>

<span data-ttu-id="46b50-133">Квантовые машины — это экземпляры обычных классов .NET, поэтому они создаются путем вызова своего конструктора, как любой другой класс .NET.</span><span class="sxs-lookup"><span data-stu-id="46b50-133">Quantum machines are instances of normal .NET classes, so they are created by invoking their constructor, just like any .NET class.</span></span> <span data-ttu-id="46b50-134">Как вы это будете делать, зависит от способа выполнения программы Q#.</span><span class="sxs-lookup"><span data-stu-id="46b50-134">How you do this depends on how you run the Q# program.</span></span>

## <a name="next-steps"></a><span data-ttu-id="46b50-135">Дальнейшие шаги</span><span class="sxs-lookup"><span data-stu-id="46b50-135">Next steps</span></span>

* <span data-ttu-id="46b50-136">Сведения о том, как вызывать целевые компьютеры для программ Q# в разных средах, см. в статье [Способы выполнения программы Q#](xref:microsoft.quantum.guide.host-programs).</span><span class="sxs-lookup"><span data-stu-id="46b50-136">For details about how to invoke target machines for Q# programs in different environments, see [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs).</span></span>
