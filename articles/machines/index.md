---
title: Квантовые симуляторы и ведущие приложения | Документация Майкрософт
description: Здесь объясняется, как с помощью классического вычислительного языка .NET можно управлять квантовыми симуляторами, как правило, C# или Q#.
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines
ms.openlocfilehash: 14aed75ed0ed192f88699b1c7dbacfae23f74642
ms.sourcegitcommit: 9d1c045cf1a2c3e19030cb38dbc7496dbd24ab58
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2020
ms.locfileid: "73442223"
---
# <a name="quantum-simulators-and-host-applications"></a><span data-ttu-id="847e4-103">Квантовые симуляторы и ведущие приложения</span><span class="sxs-lookup"><span data-stu-id="847e4-103">Quantum simulators and host applications</span></span>

## <a name="what-youll-learn"></a><span data-ttu-id="847e4-104">Цели обучения</span><span class="sxs-lookup"><span data-stu-id="847e4-104">What You'll Learn</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="847e4-105">Выполнение квантовых алгоритмов</span><span class="sxs-lookup"><span data-stu-id="847e4-105">How quantum algorithms are executed</span></span>
> * <span data-ttu-id="847e4-106">Какие квантовые симуляторы включены в этот выпуск</span><span class="sxs-lookup"><span data-stu-id="847e4-106">What quantum simulators are included in this release</span></span>
> * <span data-ttu-id="847e4-107">Как написать драйвер C# для квантового алгоритма</span><span class="sxs-lookup"><span data-stu-id="847e4-107">How to write a C# driver for your quantum algorithm</span></span>

## <a name="the-quantum-development-kit-execution-model"></a><span data-ttu-id="847e4-108">Модель выполнения Microsoft Quantum Development Kit</span><span class="sxs-lookup"><span data-stu-id="847e4-108">The Quantum Development Kit Execution Model</span></span>

<span data-ttu-id="847e4-109">В статье о [написании первой квантовой программы](xref:microsoft.quantum.write-program) мы выполнили квантовый алгоритм, передав объект `QuantumSimulator` в метод `Run` класса алгоритма.</span><span class="sxs-lookup"><span data-stu-id="847e4-109">In [Writing a quantum program](xref:microsoft.quantum.write-program), we executed our quantum algorithm by passing a `QuantumSimulator` object to the algorithm class's `Run` method.</span></span>
<span data-ttu-id="847e4-110">Класс `QuantumSimulator` выполняет квантовый алгоритм путем полного моделирования вектора квантового состояния, что идеально подходит для выполнения и тестирования `Teleport`.</span><span class="sxs-lookup"><span data-stu-id="847e4-110">The `QuantumSimulator` class executes the quantum algorithm by fully simulating the quantum state vector, which is perfect for running and testing `Teleport`.</span></span>
<span data-ttu-id="847e4-111">Дополнительные сведения о векторах квантового состояния см. в статье [Общие сведения о квантовых вычислениях](xref:microsoft.quantum.concepts.intro).</span><span class="sxs-lookup"><span data-stu-id="847e4-111">See the [Concepts guide](xref:microsoft.quantum.concepts.intro) for more on quantum state vectors.</span></span>

<span data-ttu-id="847e4-112">Для запуска квантового алгоритма можно использовать другие целевые машины.</span><span class="sxs-lookup"><span data-stu-id="847e4-112">Other target machines may be used to run a quantum algorithm.</span></span>
<span data-ttu-id="847e4-113">Машина выполняет реализации квантовых примитивов для алгоритма.</span><span class="sxs-lookup"><span data-stu-id="847e4-113">The machine is responsible for providing implementations of quantum primitives for the algorithm.</span></span>
<span data-ttu-id="847e4-114">Сюда входят примитивные операции, такие как H, CNOT и Measure, а также управление кубитами и их отслеживание.</span><span class="sxs-lookup"><span data-stu-id="847e4-114">This includes primitive operations such as H, CNOT, and Measure, as well as qubit management and tracking.</span></span>
<span data-ttu-id="847e4-115">Разные классы квантовых машин представляют разные модели выполнения для одного и того же квантового алгоритма.</span><span class="sxs-lookup"><span data-stu-id="847e4-115">Different classes of quantum machines represent different execution models for the same quantum algorithm.</span></span>

<span data-ttu-id="847e4-116">Каждый тип квантовой машины может предоставлять различные реализации этих примитивов.</span><span class="sxs-lookup"><span data-stu-id="847e4-116">Each type of quantum machine may provide different implementations of these primitives.</span></span>
<span data-ttu-id="847e4-117">Например, симулятор трассировки квантового компьютера, входящий в комплект SDK, не выполняет никакого моделирования.</span><span class="sxs-lookup"><span data-stu-id="847e4-117">For instance, the quantum computer trace simulator included in the development kit doesn't do any simulation at all.</span></span>
<span data-ttu-id="847e4-118">Вместо этого он отслеживает использование шлюза, кубита и других ресурсов для алгоритма.</span><span class="sxs-lookup"><span data-stu-id="847e4-118">Rather, it tracks gate, qubit, and other resource usage for the algorithm.</span></span>

### <a name="quantum-machines"></a><span data-ttu-id="847e4-119">Квантовые машины</span><span class="sxs-lookup"><span data-stu-id="847e4-119">Quantum Machines</span></span>

<span data-ttu-id="847e4-120">В будущем мы определим дополнительные классы квантовых машин для поддержки других типов моделирования и поддержки выполнения на топологических квантовых компьютерах.</span><span class="sxs-lookup"><span data-stu-id="847e4-120">In the future, we will define additional quantum machine classes to support other types of simulation and to support execution on topological quantum computers.</span></span>
<span data-ttu-id="847e4-121">Благодаря тому, что алгоритм остается постоянным при изменяющихся базовых реализациях машины, упрощается тестирование и отладка алгоритма в моделировании, а также его запуск на реальном оборудовании. При этом вы можете быть уверены, что алгоритм не изменился.</span><span class="sxs-lookup"><span data-stu-id="847e4-121">Allowing the algorithm to stay constant while varying the underlying machine implementation makes it easy to test and debug an algorithm in simulation and then run it on real hardware with confidence that the algorithm hasn't changed.</span></span>

### <a name="whats-included-in-this-release"></a><span data-ttu-id="847e4-122">Что входит в этот выпуск</span><span class="sxs-lookup"><span data-stu-id="847e4-122">What's Included in this Release</span></span>

<span data-ttu-id="847e4-123">В этот выпуск Quantum Developer Kit входит несколько классов квантовых машин.</span><span class="sxs-lookup"><span data-stu-id="847e4-123">This release of the quantum developer kit includes several quantum machine classes.</span></span>
<span data-ttu-id="847e4-124">Все они определены в пространстве имен `Microsoft.Quantum.Simulation.Simulators`.</span><span class="sxs-lookup"><span data-stu-id="847e4-124">All of them are defined in the `Microsoft.Quantum.Simulation.Simulators` namespace.</span></span>

* <span data-ttu-id="847e4-125">[Полный симулятор вектора состояния](xref:microsoft.quantum.machines.full-state-simulator), класс `QuantumSimulator`.</span><span class="sxs-lookup"><span data-stu-id="847e4-125">A [full state vector simulator](xref:microsoft.quantum.machines.full-state-simulator), the `QuantumSimulator` class.</span></span>
* <span data-ttu-id="847e4-126">[Простой оценщик ресурсов](xref:microsoft.quantum.machines.resources-estimator), класс `ResourcesEstimator`, позволяет проводить анализ ресурсов верхнего уровня, необходимый для выполнения квантового алгоритма.</span><span class="sxs-lookup"><span data-stu-id="847e4-126">A [simple resources estimator](xref:microsoft.quantum.machines.resources-estimator), the `ResourcesEstimator` class, it allows a top level analysis of the resources needed to run a quantum algorithm.</span></span>
* <span data-ttu-id="847e4-127">[Оценщик ресурсов на основе трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro), класс `QCTraceSimulator`, позволяет выполнять расширенный анализ потребления ресурсов для всего графа вызовов алгоритма.</span><span class="sxs-lookup"><span data-stu-id="847e4-127">A [trace-based resource estimator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), the `QCTraceSimulator` class, it allows advanced analysis of resources consumptions for the algorithm's entire call-graph.</span></span>
* <span data-ttu-id="847e4-128">[Симулятор Тоффоли](xref:microsoft.quantum.machines.toffoli-simulator), класс `ToffoliSimulator`.</span><span class="sxs-lookup"><span data-stu-id="847e4-128">A [Toffoli simulator](xref:microsoft.quantum.machines.toffoli-simulator), the `ToffoliSimulator` class.</span></span>

## <a name="writing-a-host-application"></a><span data-ttu-id="847e4-129">Создание основного приложения</span><span class="sxs-lookup"><span data-stu-id="847e4-129">Writing a host application</span></span>

<span data-ttu-id="847e4-130">В статье о [написании первой квантовой программы](xref:microsoft.quantum.write-program) мы написали простой драйвер C# для алгоритма телепортирования.</span><span class="sxs-lookup"><span data-stu-id="847e4-130">In [Writing a quantum program](xref:microsoft.quantum.write-program), we wrote a simple C# driver for our teleport algorithm.</span></span> <span data-ttu-id="847e4-131">Драйвер C# необходим для 4 основных целей:</span><span class="sxs-lookup"><span data-stu-id="847e4-131">A C# driver has 4 main purposes:</span></span>

* <span data-ttu-id="847e4-132">создание целевой машины;</span><span class="sxs-lookup"><span data-stu-id="847e4-132">Constructing the target machine</span></span>
* <span data-ttu-id="847e4-133">вычисление всех аргументов для квантового алгоритма;</span><span class="sxs-lookup"><span data-stu-id="847e4-133">Computing any arguments required for the quantum algorithm</span></span>
* <span data-ttu-id="847e4-134">запуск квантового алгоритма с помощью симулятора;</span><span class="sxs-lookup"><span data-stu-id="847e4-134">Running the quantum algorithm using the simulator</span></span>
* <span data-ttu-id="847e4-135">обработка результата операции.</span><span class="sxs-lookup"><span data-stu-id="847e4-135">Processing the result of the operation</span></span>

<span data-ttu-id="847e4-136">Здесь мы рассмотрим каждый шаг подробнее.</span><span class="sxs-lookup"><span data-stu-id="847e4-136">Here we'll discuss each step in more detail.</span></span>

### <a name="constructing-the-target-machine"></a><span data-ttu-id="847e4-137">Создание целевой машины</span><span class="sxs-lookup"><span data-stu-id="847e4-137">Constructing the Target Machine</span></span>

<span data-ttu-id="847e4-138">Квантовые машины — это экземпляры обычных классов .NET, поэтому они создаются путем вызова своего конструктора, как любой другой класс .NET.</span><span class="sxs-lookup"><span data-stu-id="847e4-138">Quantum machines are instances of normal .NET classes, so they are created by invoking their constructor, just like any .NET class.</span></span>
<span data-ttu-id="847e4-139">Некоторые симуляторы, в том числе `QuantumSimulator`, реализуют интерфейс <xref:System.IDisposable?displayProperty=nameWithType> .NET и поэтому должны быть заключены в инструкцию `using` C#.</span><span class="sxs-lookup"><span data-stu-id="847e4-139">Some simulators, including the `QuantumSimulator`, implement the .NET <xref:System.IDisposable?displayProperty=nameWithType> interface, and so should be wrapped in a C# `using` statement.</span></span>

### <a name="computing-arguments-for-the-algorithm"></a><span data-ttu-id="847e4-140">Вычисление аргументов для алгоритма</span><span class="sxs-lookup"><span data-stu-id="847e4-140">Computing Arguments for the Algorithm</span></span>

<span data-ttu-id="847e4-141">В нашем примере `Teleport` мы рассчитали некоторые относительно искусственные аргументы для передачи в квантовый алгоритм.</span><span class="sxs-lookup"><span data-stu-id="847e4-141">In our `Teleport` example, we computed some relatively artificial arguments to pass to our quantum algorithm.</span></span>
<span data-ttu-id="847e4-142">Тем не менее в большинстве случаев для квантового алгоритма требуется значительный объем данных. Проще всего предоставить их из классического драйвера.</span><span class="sxs-lookup"><span data-stu-id="847e4-142">More typically, however, there is significant data required by the quantum algorithm, and it is easiest to provide it from the classical driver.</span></span>

<span data-ttu-id="847e4-143">Например, при выполнении химических моделирований для квантового алгоритма требуется большая таблица интегралов взаимодействия молекулярных орбиталей.</span><span class="sxs-lookup"><span data-stu-id="847e4-143">For instance, when doing chemical simulations, the quantum algorithm requires a large table of molecular orbital interaction integrals.</span></span>
<span data-ttu-id="847e4-144">Обычно они считываются из файла, который предоставляется при выполнении алгоритма.</span><span class="sxs-lookup"><span data-stu-id="847e4-144">Generally these are read in from a file that is provided when running the algorithm.</span></span>
<span data-ttu-id="847e4-145">Так как в Q# не предусмотрен механизм доступа к файловой системе, сбор данных этого типа лучше всего выполняется с помощью классического драйвера, а затем они передаются в метод `Run` квантового алгоритма.</span><span class="sxs-lookup"><span data-stu-id="847e4-145">Since Q# does not have a mechanism for accessing the file system, this sort of data is best collected by the classical driver and then passed to the quantum algorithm's `Run` method.</span></span>

<span data-ttu-id="847e4-146">Классический драйвер также играет ключевую роль в вариативных методах.</span><span class="sxs-lookup"><span data-stu-id="847e4-146">Another case where the classical driver plays a key role is in variational methods.</span></span>
<span data-ttu-id="847e4-147">В этом классе алгоритмов квантовое состояние подготавливается на основе некоторых классических параметров, и это состояние используется для расчета интересующего значения.</span><span class="sxs-lookup"><span data-stu-id="847e4-147">In this class of algorithms, a quantum state is prepared based on some classical parameters, and that state is used to compute some value of interest.</span></span>
<span data-ttu-id="847e4-148">Параметры корректируются путем поиска восхождением к вершине или с помощью алгоритма машинного обучения, а затем квантовый алгоритм выполняется снова.</span><span class="sxs-lookup"><span data-stu-id="847e4-148">The parameters are adjusted based on some type of hill climbing or machine learning algorithm and the quantum algorithm run again.</span></span>
<span data-ttu-id="847e4-149">Алгоритм поиска восхождением к вершине наилучшим образом реализуется в виде сугубо классической функции, которая вызывается классическим драйвером. Результаты поиска восхождением к вершине затем передаются в следующее выполнение квантового алгоритма.</span><span class="sxs-lookup"><span data-stu-id="847e4-149">For such algorithms, the hill climbing algorithm itself is best implemented as a purely classical function that is called by the classical driver; the results of the hill climbing are then passed to the next execution of the quantum algorithm.</span></span>

### <a name="running-the-quantum-algorithm"></a><span data-ttu-id="847e4-150">Выполнение квантового алгоритма</span><span class="sxs-lookup"><span data-stu-id="847e4-150">Running the Quantum Algorithm</span></span>

<span data-ttu-id="847e4-151">Как правило, эта часть очень проста.</span><span class="sxs-lookup"><span data-stu-id="847e4-151">This part is generally very straightforward.</span></span>
<span data-ttu-id="847e4-152">Каждая операция Q# компилируется в класс, предоставляющий статический метод `Run`.</span><span class="sxs-lookup"><span data-stu-id="847e4-152">Each Q# operation is compiled into a class that provides a static `Run` method.</span></span>
<span data-ttu-id="847e4-153">Аргументы для этого метода предоставляются плоским кортежем аргументов самой операции, а также дополнительный аргумент, который является симулятором для выполнения.</span><span class="sxs-lookup"><span data-stu-id="847e4-153">The arguments to this method are given by the flattened argument tuple of the operation itself, plus an additional first argument which is the simulator to execute with.</span></span> <span data-ttu-id="847e4-154">Для операции, которая ожидает именованный кортеж типа `(a: String, (b: Double, c: Double))`, его плоский аналог относится к типу `(String a, Double b, Double c)`.</span><span class="sxs-lookup"><span data-stu-id="847e4-154">For an operation that expects the named tuple of type `(a: String, (b: Double, c: Double))` its flattened counterpart is of type `(String a, Double b, Double c)`.</span></span>


<span data-ttu-id="847e4-155">С передачей аргументов в метод `Run` связаны определенные тонкости:</span><span class="sxs-lookup"><span data-stu-id="847e4-155">There are some subtleties when passing arguments to a `Run` method:</span></span>

* <span data-ttu-id="847e4-156">Массивы должны быть заключены в объект `Microsoft.Quantum.Simulation.Core.QArray<T>`.</span><span class="sxs-lookup"><span data-stu-id="847e4-156">Arrays must be wrapped in a `Microsoft.Quantum.Simulation.Core.QArray<T>` object.</span></span>
    <span data-ttu-id="847e4-157">У класса `QArray` есть конструктор, который может принимать любую упорядоченную коллекцию (`IEnumerable<T>`) соответствующих объектов.</span><span class="sxs-lookup"><span data-stu-id="847e4-157">A `QArray` class has a constructor that can take any ordered collection (`IEnumerable<T>`) of appropriate objects.</span></span>
* <span data-ttu-id="847e4-158">Пустой кортеж, `()` на языке Q#, представлен `QVoid.Instance` на языке C#.</span><span class="sxs-lookup"><span data-stu-id="847e4-158">The empty tuple, `()` in Q#, is represented by `QVoid.Instance` in C#.</span></span>
* <span data-ttu-id="847e4-159">Непустые кортежи представлены в виде экземпляров `ValueTuple` .NET.</span><span class="sxs-lookup"><span data-stu-id="847e4-159">Non-empty tuples are represented as .NET `ValueTuple` instances.</span></span>
* <span data-ttu-id="847e4-160">Пользовательские типы Q# передаются в качестве базового типа.</span><span class="sxs-lookup"><span data-stu-id="847e4-160">Q# user-defined types are passed as their base type.</span></span>
* <span data-ttu-id="847e4-161">Чтобы передать операцию или функцию в метод `Run`, необходимо получить экземпляр класса операции или функции, используя метод `Get<>` симулятора.</span><span class="sxs-lookup"><span data-stu-id="847e4-161">To pass an operation or a function to a `Run` method, you have to obtain an   instance of the operation's or function's class, using the simulator's `Get<>` method.</span></span>

### <a name="processing-the-results"></a><span data-ttu-id="847e4-162">Обработка результатов</span><span class="sxs-lookup"><span data-stu-id="847e4-162">Processing the Results</span></span>

<span data-ttu-id="847e4-163">Результаты квантового алгоритма возвращаются из метода `Run`.</span><span class="sxs-lookup"><span data-stu-id="847e4-163">The results of the quantum algorithm are returned from the `Run` method.</span></span>
<span data-ttu-id="847e4-164">Метод `Run` выполняется асинхронно, поэтому возвращает экземпляр <xref:System.Threading.Tasks.Task`1>.</span><span class="sxs-lookup"><span data-stu-id="847e4-164">The `Run` method executes asynchronously thus it returns an instance of <xref:System.Threading.Tasks.Task`1>.</span></span>
<span data-ttu-id="847e4-165">Получить результаты фактической операции можно несколькими способами.</span><span class="sxs-lookup"><span data-stu-id="847e4-165">There are multiple ways to get the actual operation's results.</span></span> <span data-ttu-id="847e4-166">Самый простой способ заключается в использовании свойства[`Result`](https://docs.microsoft.com/dotnet/api/system.threading.tasks.task-1.result)`Task`.</span><span class="sxs-lookup"><span data-stu-id="847e4-166">The simplest is by using the `Task`'s [`Result` property](https://docs.microsoft.com/dotnet/api/system.threading.tasks.task-1.result):</span></span>

```csharp
    var res = BellTest.Run(sim, 1000, initial).Result;
```
<span data-ttu-id="847e4-167">Но другие приемы, такие как использование метода [`Wait`](https://docs.microsoft.com/dotnet/api/system.threading.tasks.task.wait) или ключевого слова [`await`](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/await) C# также будут работать.</span><span class="sxs-lookup"><span data-stu-id="847e4-167">but other techniques, like using the [`Wait` method](https://docs.microsoft.com/dotnet/api/system.threading.tasks.task.wait) or C# [`await` keyword](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/await) will also work.</span></span>

<span data-ttu-id="847e4-168">Как и в случае с аргументами, кортежи Q# представляются в виде экземпляров `ValueTuple`, а массивы Q# — в виде экземпляров `QArray`.</span><span class="sxs-lookup"><span data-stu-id="847e4-168">As with arguments, Q# tuples are represented as `ValueTuple` instances and Q# arrays are represented as `QArray` instances.</span></span>
<span data-ttu-id="847e4-169">Пользовательские типы возвращаются в качестве базового типа.</span><span class="sxs-lookup"><span data-stu-id="847e4-169">User-defined types are returned as their base types.</span></span>
<span data-ttu-id="847e4-170">Пустой кортеж, `()`, возвращается как экземпляр класса `QVoid`.</span><span class="sxs-lookup"><span data-stu-id="847e4-170">The empty tuple, `()`, is returned as an instance of the `QVoid` class.</span></span>

<span data-ttu-id="847e4-171">Для получения полезных ответов при использовании многих квантовых алгоритмов требуется значительная последующая обработка.</span><span class="sxs-lookup"><span data-stu-id="847e4-171">Many quantum algorithms require substantial post-processing to derive useful answers.</span></span>
<span data-ttu-id="847e4-172">Например, квантовая часть алгоритма Шора — это всего лишь начало вычисления, позволяющего найти факторы числа.</span><span class="sxs-lookup"><span data-stu-id="847e4-172">For instance, the quantum part of Shor's algorithm is just the beginning of a computation that finds the factors of a number.</span></span>

<span data-ttu-id="847e4-173">В большинстве случаев это самый простой способ выполнить последующую обработку такого рода в классическом драйвере.</span><span class="sxs-lookup"><span data-stu-id="847e4-173">In most cases, it is simplest and easiest to do this sort of post-processing in the classical driver.</span></span>
<span data-ttu-id="847e4-174">Только классический драйвер может передавать результаты пользователю или записывать их на диск.</span><span class="sxs-lookup"><span data-stu-id="847e4-174">Only the classical driver can report results to the user or write them to disk.</span></span>
<span data-ttu-id="847e4-175">Классический драйвер будет иметь доступ к аналитическим библиотекам и другим математическим функциям, не представленным в Q#.</span><span class="sxs-lookup"><span data-stu-id="847e4-175">The classical driver will have access to analytical libraries and other mathematical functions that are not exposed in Q#.</span></span>


## <a name="failures"></a><span data-ttu-id="847e4-176">Сбои</span><span class="sxs-lookup"><span data-stu-id="847e4-176">Failures</span></span>

<span data-ttu-id="847e4-177">При достижении инструкции Q# `fail` во время выполнения операции создается исключение `ExecutionFailException`.</span><span class="sxs-lookup"><span data-stu-id="847e4-177">When the Q# `fail` statement is reached during the execution of an operation, an `ExecutionFailException` is thrown.</span></span>

<span data-ttu-id="847e4-178">В результате использования `System.Task` в методе `Run` исключение, выдаваемое в результате выполнения инструкции `fail`, будет заключено в `System.AggregateException`.</span><span class="sxs-lookup"><span data-stu-id="847e4-178">Due to the use of `System.Task` in the `Run` method, the exception thrown as a result of a `fail` statement will be wrapped into a `System.AggregateException`.</span></span>
<span data-ttu-id="847e4-179">Чтобы найти фактическую причину сбоя, необходимо выполнить итерацию в `AggregateException` 
`InnerExceptions`, например:</span><span class="sxs-lookup"><span data-stu-id="847e4-179">To find the actual reason for the failure, you need to iterate into the `AggregateException` 
`InnerExceptions`, for example:</span></span>

```csharp

            try
            {
                using(var sim = new QuantumSimulator())
                {
                    /// call your operations here...
                }
            }
            catch (AggregateException e)
            {
                // Unwrap AggregateException to get the message from Q# fail statement.
                // Go through all inner exceptions.
                foreach (Exception inner in e.InnerExceptions)
                {
                    // If the exception of type ExecutionFailException
                    if (inner is ExecutionFailException failException)
                    {
                        // Print the message it contains
                        Console.WriteLine($" {failException.Message}");
                    }
                }
            }
```

## <a name="other-classical-languages"></a><span data-ttu-id="847e4-180">Другие классические языки</span><span class="sxs-lookup"><span data-stu-id="847e4-180">Other Classical Languages</span></span>

<span data-ttu-id="847e4-181">Несмотря на то что предоставленные нами примеры, написаны на языке C#, F# и Python, Quantum Development Kit также поддерживает написание классических программных приложений на других языках.</span><span class="sxs-lookup"><span data-stu-id="847e4-181">While the samples we have provided are in C#, F#, and Python, the Quantum Development Kit also supports writing classical host programs in other languages.</span></span>
<span data-ttu-id="847e4-182">Например, если необходимо написать основную программу в Visual Basic, [вы получите корректный результат](https://github.com/tcNickolas/MiscQSharp/blob/master/Quantum_VBNet/README.md#using-q-with-visual-basic-net).</span><span class="sxs-lookup"><span data-stu-id="847e4-182">For example, if you want to write a host program in Visual Basic, [it should work just fine](https://github.com/tcNickolas/MiscQSharp/blob/master/Quantum_VBNet/README.md#using-q-with-visual-basic-net).</span></span>
