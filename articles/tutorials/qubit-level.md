---
title: Создавайте и имитируйте программы уровня кубит в Q#
description: Пошаговое руководство по написанию и моделированию тактовой программы, работающей на уровне отдельного кубита
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 10/06/2019
uid: microsoft.quantum.circuit-tutorial
ms.topic: tutorial
no-loc:
- Q#
- $$v
ms.openlocfilehash: 39b2d762c0efbfa4bb3a60a1dcee6bcbe2bd91a9
ms.sourcegitcommit: 75c4edc7c410cc63dc8352e2a5bef44b433ed188
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/25/2020
ms.locfileid: "88863334"
---
# <a name="tutorial-write-and-simulate-qubit-level-programs-in-q"></a><span data-ttu-id="d7d61-103">Учебник. Создание и имитация программ уровня кубит в Q\#</span><span class="sxs-lookup"><span data-stu-id="d7d61-103">Tutorial: Write and simulate qubit-level programs in Q\#</span></span>

<span data-ttu-id="d7d61-104">Добро пожаловать в учебник по созданию и моделированию основной тактовой программы, которая работает с отдельными Кубитс.</span><span class="sxs-lookup"><span data-stu-id="d7d61-104">Welcome to the Quantum Development Kit tutorial on writing and simulating a basic quantum program that operates on individual qubits.</span></span> 

<span data-ttu-id="d7d61-105">Несмотря на то, что в Q# основном создавалось как высокоуровневый язык программирования для крупномасштабных тактовых программ, его можно легко использовать для изучения более низкого уровня тактовых программ: прямой адресации для конкретных Кубитс.</span><span class="sxs-lookup"><span data-stu-id="d7d61-105">Although Q# was primarily created as a high-level programming language for large-scale quantum programs, it can just as easily be used to explore the lower level of quantum programs: directly addressing specific qubits.</span></span>
<span data-ttu-id="d7d61-106">Гибкость Q# позволяет пользователям подходить к созданию тактовых систем с любого такого уровня абстракции, а в этом учебнике мы подробно рассмотрим Кубитс.</span><span class="sxs-lookup"><span data-stu-id="d7d61-106">The flexibility of Q# allows users to approach quantum systems from any such level of abstraction, and in this tutorial we dive into the qubits themselves.</span></span>
<span data-ttu-id="d7d61-107">В частности, мы рассмотрим внешний вид [преобразования Фурье в тактовой](https://en.wikipedia.org/wiki/Quantum_Fourier_transform)области — подпрограммы, которая является неотъемлемой для многих более крупных алгоритмов такта.</span><span class="sxs-lookup"><span data-stu-id="d7d61-107">Specifically, we take a look under the hood of the [quantum Fourier transform](https://en.wikipedia.org/wiki/Quantum_Fourier_transform), a subroutine that is integral to many larger quantum algorithms.</span></span>

<span data-ttu-id="d7d61-108">Обратите внимание, что это низкоуровневое представление обработки данных о такте часто описывается в терминах «[тактовые цепи](xref:microsoft.quantum.concepts.circuits)», которые представляют последовательные приложения шлюзов для конкретных Кубитс системы.</span><span class="sxs-lookup"><span data-stu-id="d7d61-108">Note that this low-level view of quantum information processing is often described in terms of "[quantum circuits](xref:microsoft.quantum.concepts.circuits)," which represent the sequential application of gates to specific qubits of a system.</span></span>

<span data-ttu-id="d7d61-109">Таким же кубит операции, которые последовательно применяются, можно легко представить в виде «схемы цепи».</span><span class="sxs-lookup"><span data-stu-id="d7d61-109">Thus, the single- and multi-qubit operations we sequentially apply can be readily represented in a "circuit diagram."</span></span>
<span data-ttu-id="d7d61-110">В нашем случае мы определим Q# операцию для выполнения полного преобразования Фурье из трех кубит, которое в качестве цепи имеет следующее представление:</span><span class="sxs-lookup"><span data-stu-id="d7d61-110">In our case, we will define a Q# operation to perform the full three-qubit quantum Fourier transform, which has the following representation as a circuit:</span></span>

<br/>
<img src="../media/qft_full.PNG" alt="Three qubit quantum Fourier transform circuit diagram" width="600">

## <a name="prerequisites"></a><span data-ttu-id="d7d61-111">Обязательные условия</span><span class="sxs-lookup"><span data-stu-id="d7d61-111">Prerequisites</span></span>

* <span data-ttu-id="d7d61-112">[Установите](xref:microsoft.quantum.install) пакет средств разработки тактов, используя предпочитаемый язык и среду разработки.</span><span class="sxs-lookup"><span data-stu-id="d7d61-112">[Install](xref:microsoft.quantum.install) the Quantum Development Kit using your preferred language and development environment.</span></span>
* <span data-ttu-id="d7d61-113">Если эта платформа уже установлена, убедитесь, что она [обновлена](xref:microsoft.quantum.update) до последней версии.</span><span class="sxs-lookup"><span data-stu-id="d7d61-113">If you already have the QDK installed, make sure you have [updated](xref:microsoft.quantum.update) to the latest version</span></span>


## <a name="in-this-tutorial-youll-learn-how-to"></a><span data-ttu-id="d7d61-114">Из этого руководства вы узнаете, как выполнять следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="d7d61-114">In this tutorial, you'll learn how to:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="d7d61-115">Определение операций такта в Q#</span><span class="sxs-lookup"><span data-stu-id="d7d61-115">Define quantum operations in Q#</span></span>
> * <span data-ttu-id="d7d61-116">Вызов Q# операций непосредственно из командной строки или с помощью классического ведущего приложения</span><span class="sxs-lookup"><span data-stu-id="d7d61-116">Call Q# operations directly from the command prompt or using a classical host program</span></span>
> * <span data-ttu-id="d7d61-117">Моделирование операции-такта от выделения кубит до выходных данных измерения</span><span class="sxs-lookup"><span data-stu-id="d7d61-117">Simulate a quantum operation from qubit allocation to measurement output</span></span>
> * <span data-ttu-id="d7d61-118">Обратите внимание на то, как имитация вавефунктион в тактовой системе развивается во всей операции.</span><span class="sxs-lookup"><span data-stu-id="d7d61-118">Observe how the quantum system's simulated wavefunction evolves throughout the operation</span></span>

<span data-ttu-id="d7d61-119">Выполнение тактовой программы с помощью пакета Microsoft тактов Development Kit обычно состоит из двух частей:</span><span class="sxs-lookup"><span data-stu-id="d7d61-119">Running a quantum program with Microsoft's Quantum Development Kit typically consists of two parts:</span></span>
1. <span data-ttu-id="d7d61-120">Сама программа, которая реализуется с помощью Q# языка программирования тактов, а затем вызывается для запуска на тактовой или имитаторной системе.</span><span class="sxs-lookup"><span data-stu-id="d7d61-120">The program itself, which is implemented using the Q# quantum programming language, and then invoked to run on a quantum computer or quantum simulator.</span></span> <span data-ttu-id="d7d61-121">Они состоят из</span><span class="sxs-lookup"><span data-stu-id="d7d61-121">These consist of</span></span> 
    - <span data-ttu-id="d7d61-122">Q# операции: подпрограммы, действующие в тактовые регистры и</span><span class="sxs-lookup"><span data-stu-id="d7d61-122">Q# operations: subroutines acting on quantum registers, and</span></span> 
    - <span data-ttu-id="d7d61-123">Q# функции: классические подпрограммы, используемые в алгоритме такта.</span><span class="sxs-lookup"><span data-stu-id="d7d61-123">Q# functions: classical subroutines used within the quantum algorithm.</span></span>
2. <span data-ttu-id="d7d61-124">Точка входа, используемая для вызова тактовой программы и указания целевого компьютера, на котором она должна быть запущена.</span><span class="sxs-lookup"><span data-stu-id="d7d61-124">The entry point used to call the quantum program and specify the target machine on which it should be run.</span></span>
    <span data-ttu-id="d7d61-125">Это можно сделать непосредственно из командной строки или с помощью основной программы, написанной на основе классического языка программирования, такого как Python или C#.</span><span class="sxs-lookup"><span data-stu-id="d7d61-125">This can be done directly from the command prompt, or through a host program written in a classical programming language like Python or C#.</span></span>
    <span data-ttu-id="d7d61-126">Этот учебник содержит инструкции для любого предпочтительного метода.</span><span class="sxs-lookup"><span data-stu-id="d7d61-126">This tutorial includes instructions for whichever method you prefer.</span></span>

## <a name="allocate-qubits-and-define-quantum-operations"></a><span data-ttu-id="d7d61-127">Выделение Кубитс и определение операций такта</span><span class="sxs-lookup"><span data-stu-id="d7d61-127">Allocate qubits and define quantum operations</span></span>

<span data-ttu-id="d7d61-128">Первая часть этого руководства состоит из определения Q# операции `Perform3qubitQFT` , которая выполняет преобразование Фурье в тактовую операцию для трех Кубитс.</span><span class="sxs-lookup"><span data-stu-id="d7d61-128">The first part of this tutorial consists of defining the Q# operation `Perform3qubitQFT`, which performs the quantum Fourier transform on three qubits.</span></span> 

<span data-ttu-id="d7d61-129">Кроме того, мы будем использовать [`DumpMachine`](xref:microsoft.quantum.diagnostics.dumpmachine) функцию, чтобы увидеть, как имитация вавефунктиона нашей кубит системы в рамках всей операции.</span><span class="sxs-lookup"><span data-stu-id="d7d61-129">In addition, we will use the [`DumpMachine`](xref:microsoft.quantum.diagnostics.dumpmachine) function to observe how the simulated wavefunction of our three qubit system evolves across the operation.</span></span>

<span data-ttu-id="d7d61-130">Первым шагом является создание Q# проекта и файла.</span><span class="sxs-lookup"><span data-stu-id="d7d61-130">The first step is creating your Q# project and file.</span></span>
<span data-ttu-id="d7d61-131">Действия для этого зависят от среды, которая будет использоваться для вызова программы. подробные сведения можно найти в соответствующих [руководствах по установке](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="d7d61-131">The steps for this depend on the environment you will use to call the program, and you can find the details in the respective [installation guides](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="d7d61-132">Мы рассмотрим компоненты файла пошаговым образом, но код также доступен в полном блоке ниже.</span><span class="sxs-lookup"><span data-stu-id="d7d61-132">We will walk you through the components of the file step-by-step, but the code is also available as a full block below.</span></span>

### <a name="namespaces-to-access-other-no-locq-operations"></a><span data-ttu-id="d7d61-133">Пространства имен для доступа к другим Q# операциям</span><span class="sxs-lookup"><span data-stu-id="d7d61-133">Namespaces to access other Q# operations</span></span>
<span data-ttu-id="d7d61-134">Внутри файла сначала определяется пространство имен, доступ к `NamespaceQFT` которому будет осуществляться компилятором.</span><span class="sxs-lookup"><span data-stu-id="d7d61-134">Inside the file, we first define the namespace `NamespaceQFT` which will be accessed by the compiler.</span></span>
<span data-ttu-id="d7d61-135">Чтобы в нашей операции использовались существующие Q# операции, мы откроем соответствующие `Microsoft.Quantum.<>` пространства имен.</span><span class="sxs-lookup"><span data-stu-id="d7d61-135">For our operation to make use of existing Q# operations, we open the relevant `Microsoft.Quantum.<>` namespaces.</span></span>

```qsharp
namespace NamespaceQFT {
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Diagnostics;
    open Microsoft.Quantum.Math;
    open Microsoft.Quantum.Arrays;

    // operations go here
}
```

### <a name="define-operations-with-arguments-and-returns"></a><span data-ttu-id="d7d61-136">Определение операций с аргументами и возвраты</span><span class="sxs-lookup"><span data-stu-id="d7d61-136">Define operations with arguments and returns</span></span>
<span data-ttu-id="d7d61-137">Далее мы определим `Perform3qubitQFT` операцию:</span><span class="sxs-lookup"><span data-stu-id="d7d61-137">Next, we define the `Perform3qubitQFT` operation:</span></span>

```qsharp
    operation Perform3qubitQFT() : Unit {
        // do stuff
    }
```

<span data-ttu-id="d7d61-138">Пока операция не принимает аргументов и не возвращает ничего,---в этом случае мы записываем, что он возвращает `Unit` объект, который в `void` C# или пустой кортеж, `Tuple[()]` в Python.</span><span class="sxs-lookup"><span data-stu-id="d7d61-138">For now, the operation takes no arguments and does not return anything---in this case we write that it returns a `Unit` object, which is akin to `void` in C# or an empty tuple, `Tuple[()]`, in Python.</span></span>
<span data-ttu-id="d7d61-139">Позже мы изменим его, чтобы возвращался массив результатов измерения, после чего точка `Unit` будет заменена `Result[]` .</span><span class="sxs-lookup"><span data-stu-id="d7d61-139">Later, we will modify it to return an array of measurement results, at which point `Unit` will be replaced by `Result[]`.</span></span> 

### <a name="allocate-qubits-with-using"></a><span data-ttu-id="d7d61-140">Выделить Кубитс с помощью `using`</span><span class="sxs-lookup"><span data-stu-id="d7d61-140">Allocate qubits with `using`</span></span>
<span data-ttu-id="d7d61-141">В рамках нашей Q# операции мы сначала выделили регистр из трех Кубитс с помощью `using` инструкции:</span><span class="sxs-lookup"><span data-stu-id="d7d61-141">Within our Q# operation, we first allocate a register of three qubits with the `using` statement:</span></span>

```qsharp
        using (qs = Qubit[3]) {

            Message("Initial state |000>:");
            DumpMachine();

        }
```

<span data-ttu-id="d7d61-142">При использовании `using` Кубитс автоматически выделяются в состоянии $ \кет {0} $.</span><span class="sxs-lookup"><span data-stu-id="d7d61-142">With `using`, the qubits are automatically allocated in the $\ket{0}$ state.</span></span> <span data-ttu-id="d7d61-143">Мы можем проверить это с помощью [`Message(<string>)`](xref:microsoft.quantum.intrinsic.message) и [`DumpMachine()`](xref:microsoft.quantum.diagnostics.dumpmachine) , чтобы вывести строку и текущее состояние системы на консоль.</span><span class="sxs-lookup"><span data-stu-id="d7d61-143">We can verify this by using [`Message(<string>)`](xref:microsoft.quantum.intrinsic.message) and [`DumpMachine()`](xref:microsoft.quantum.diagnostics.dumpmachine), which print a string and the system's current state to the console.</span></span>

> [!NOTE]
> <span data-ttu-id="d7d61-144">`Message(<string>)`Функции и `DumpMachine()` (от [`Microsoft.Quantum.Intrinsic`](xref:microsoft.quantum.intrinsic) и [`Microsoft.Quantum.Diagnostics`](xref:microsoft.quantum.diagnostics) соответственно) печатаются непосредственно на консоли.</span><span class="sxs-lookup"><span data-stu-id="d7d61-144">The `Message(<string>)` and `DumpMachine()` functions (from [`Microsoft.Quantum.Intrinsic`](xref:microsoft.quantum.intrinsic) and [`Microsoft.Quantum.Diagnostics`](xref:microsoft.quantum.diagnostics), respectively) both print directly to the console.</span></span> <span data-ttu-id="d7d61-145">Как и в реальном такте, не Q# позволяет нам получить прямой доступ к кубит состояниям.</span><span class="sxs-lookup"><span data-stu-id="d7d61-145">Just like a real quantum computation, Q# does not allow us to directly access qubit states.</span></span>
> <span data-ttu-id="d7d61-146">Однако, как `DumpMachine` выводит текущее состояние целевого компьютера, оно может предоставить ценную информацию для отладки и обучения при использовании в сочетании с симулятором полного состояния.</span><span class="sxs-lookup"><span data-stu-id="d7d61-146">However, as `DumpMachine` prints the target machine's current state, it can provide valuable insight for debugging and learning when used in conjunction with the full state simulator.</span></span>


### <a name="applying-single-qubit-and-controlled-gates"></a><span data-ttu-id="d7d61-147">Применение кубит и контролируемых шлюзов</span><span class="sxs-lookup"><span data-stu-id="d7d61-147">Applying single-qubit and controlled gates</span></span>

<span data-ttu-id="d7d61-148">Далее мы применяем шлюз, который состоит из самой операции.</span><span class="sxs-lookup"><span data-stu-id="d7d61-148">Next, we apply the gates which comprise the operation itself.</span></span>
<span data-ttu-id="d7d61-149">Q# уже содержит много основных шлюзов тактов в качестве операций в [`Microsoft.Quantum.Intrinsic`](xref:microsoft.quantum.intrinsic) пространстве имен, и это не исключение.</span><span class="sxs-lookup"><span data-stu-id="d7d61-149">Q# already contains many basic quantum gates as operations in the [`Microsoft.Quantum.Intrinsic`](xref:microsoft.quantum.intrinsic) namespace, and these are no exception.</span></span> 

<span data-ttu-id="d7d61-150">В рамках Q# операции операторы, вызывающие вызываемые, будут выполняться в последовательном порядке.</span><span class="sxs-lookup"><span data-stu-id="d7d61-150">Within a Q# operation, the statements invoking callables will of course be executed in sequential order.</span></span>
<span data-ttu-id="d7d61-151">Следовательно, первый применяемый шлюз — это [`H`](xref:microsoft.quantum.intrinsic.h) (хадамард) к первому кубит:</span><span class="sxs-lookup"><span data-stu-id="d7d61-151">Hence, the first gate to apply is the [`H`](xref:microsoft.quantum.intrinsic.h) (Hadamard) to the first qubit:</span></span>

<br/>
<img src="../media/qft_firstH.PNG" alt="Circuit diagram for three qubit QFT through first Hadamard" width="120">

<span data-ttu-id="d7d61-152">Чтобы применить операцию к определенному кубит из регистра (т. е. отдельного объекта `Qubit` из массива `Qubit[]` ), мы используем стандартную нотацию индекса.</span><span class="sxs-lookup"><span data-stu-id="d7d61-152">To apply an operation to a specific qubit from a register (i.e. a single `Qubit` from an array `Qubit[]`) we use standard index notation.</span></span>
<span data-ttu-id="d7d61-153">Таким образом, применение [`H`](xref:microsoft.quantum.intrinsic.h) к первому кубиту регистра `qs` имеет вид:</span><span class="sxs-lookup"><span data-stu-id="d7d61-153">So, applying the [`H`](xref:microsoft.quantum.intrinsic.h) to the first qubit of our register `qs` takes the form:</span></span>

```qsharp
            H(qs[0]);
```

<span data-ttu-id="d7d61-154">Помимо применения `H` шлюза (хадамард) к отдельным Кубитс, цепь Кфт состоит в основном из контролируемых [`R1`](xref:microsoft.quantum.intrinsic.r1) поворотов.</span><span class="sxs-lookup"><span data-stu-id="d7d61-154">Besides applying the `H` (Hadamard) gate to individual qubits, the QFT circuit consists primarily of controlled [`R1`](xref:microsoft.quantum.intrinsic.r1) rotations.</span></span>
<span data-ttu-id="d7d61-155">`R1(θ, <qubit>)`Операция в целом оставляет компонент $ \кет {0} $ кубит без изменений, одновременно применяя поворот $e ^ {и\сета} $ к {1} компоненту $ \кет $.</span><span class="sxs-lookup"><span data-stu-id="d7d61-155">An `R1(θ, <qubit>)` operation in general leaves the $\ket{0}$ component of the qubit unchanged, while applying a rotation of $e^{i\theta}$ to the $\ket{1}$ component.</span></span>

#### <a name="controlled-operations"></a><span data-ttu-id="d7d61-156">Управляемые операции</span><span class="sxs-lookup"><span data-stu-id="d7d61-156">Controlled operations</span></span>

<span data-ttu-id="d7d61-157">Q# делает несложным условие выполнения операции в одном или нескольких кубитсах элементов управления.</span><span class="sxs-lookup"><span data-stu-id="d7d61-157">Q# makes it extremely easy to condition the execution of an operation upon one or multiple control qubits.</span></span>
<span data-ttu-id="d7d61-158">В целом, мы просто предваряем вызов `Controlled` , а аргументы операции изменяются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d7d61-158">In general, we merely preface the call with `Controlled`, and the operation arguments change as:</span></span>

 <span data-ttu-id="d7d61-159">`Op(<normal args>)` $ \то $ `Controlled Op([<control qubits>], (<normal args>))` .</span><span class="sxs-lookup"><span data-stu-id="d7d61-159">`Op(<normal args>)` $\to$ `Controlled Op([<control qubits>], (<normal args>))`.</span></span>

<span data-ttu-id="d7d61-160">Обратите внимание, что элемент управления Кубитс должен быть предоставлен как массив, даже если он является одним кубит.</span><span class="sxs-lookup"><span data-stu-id="d7d61-160">Note that the control qubits must be provided as an array, even if it is a single qubit.</span></span>

<span data-ttu-id="d7d61-161">После этого `H` мы видим, что следующие шлюзы являются `R1` шлюзами, действующими на первый кубит (и контролируются вторым/третьим):</span><span class="sxs-lookup"><span data-stu-id="d7d61-161">After the `H`, we see that the next gates are the `R1` gates acting on the first qubit (and controlled by the second/third):</span></span>

<br/>
<img src="../media/qft_firstqubit.PNG" alt="Circuit diagram for three qubit QFT through first qubit" width="310">

<span data-ttu-id="d7d61-162">Мы вызываем их с помощью</span><span class="sxs-lookup"><span data-stu-id="d7d61-162">We call these with</span></span>

```qsharp
            Controlled R1([qs[1]], (PI()/2.0, qs[0]));
            Controlled R1([qs[2]], (PI()/4.0, qs[0]));
```

<span data-ttu-id="d7d61-163">Обратите внимание, что мы используем [`PI()`](xref:microsoft.quantum.math.pi) функцию из [`Microsoft.Quantum.Math`](xref:microsoft.quantum.math) пространства имен для определения поворотов с точки зрения PI радиан.</span><span class="sxs-lookup"><span data-stu-id="d7d61-163">Note that we use the [`PI()`](xref:microsoft.quantum.math.pi) function from the [`Microsoft.Quantum.Math`](xref:microsoft.quantum.math) namespace to define the rotations in terms of pi radians.</span></span>
<span data-ttu-id="d7d61-164">Кроме того, мы разделены на `Double` (например, `2.0` ), так как деление на целое число `2` вызовет ошибку типа.</span><span class="sxs-lookup"><span data-stu-id="d7d61-164">Additionally, we divide by a `Double` (e.g. `2.0`) because dividing by an integer `2` would throw a type error.</span></span> 

> [!TIP]
> <span data-ttu-id="d7d61-165">`R1(π/2)` и `R1(π/4)` эквивалентны `S` `T` операциям и (также в `Microsoft.Quantum.Intrinsic` ).</span><span class="sxs-lookup"><span data-stu-id="d7d61-165">`R1(π/2)` and `R1(π/4)` are equivalent to the `S` and `T` operations (also in `Microsoft.Quantum.Intrinsic`).</span></span>


<span data-ttu-id="d7d61-166">После применения соответствующих `H` операций и управляемых поворотов ко второму и третьему Кубитс:</span><span class="sxs-lookup"><span data-stu-id="d7d61-166">After applying the relevant `H` operations and controlled rotations to the second and third qubits:</span></span>

```qsharp
            //second qubit:
            H(qs[1]);
            Controlled R1([qs[2]], (PI()/2.0, qs[1]));

            //third qubit:
            H(qs[2]);
```

<span data-ttu-id="d7d61-167">[`SWAP`](xref:microsoft.quantum.intrinsic.swap)для завершения канала необходимо применить только шлюз:</span><span class="sxs-lookup"><span data-stu-id="d7d61-167">we need only apply a [`SWAP`](xref:microsoft.quantum.intrinsic.swap) gate to complete the circuit:</span></span>

```qsharp
            SWAP(qs[2], qs[0]);
```

<span data-ttu-id="d7d61-168">Это необходимо потому, что природа преобразования Фурье в тактовой области выводит Кубитс в обратную последовательность, поэтому замена позволяет легко интегрировать подпрограммы в большие алгоритмы.</span><span class="sxs-lookup"><span data-stu-id="d7d61-168">This is necessary because the nature of the quantum Fourier transform outputs the qubits in reverse order, so the swaps allow for seamless integration of the subroutine into larger algorithms.</span></span>

<span data-ttu-id="d7d61-169">Поэтому мы завершили запись операций кубит-уровня в процессе преобразования Фурье в нашу Q# операцию:</span><span class="sxs-lookup"><span data-stu-id="d7d61-169">Hence we have finished writing the qubit-level operations of the quantum Fourier transform into our Q# operation:</span></span>

<img src="../media/qft_full.PNG" alt="Three qubit quantum Fourier transform circuit diagram" width="600">

<span data-ttu-id="d7d61-170">Тем не менее, мы не можем вызвать его еще раз в день.</span><span class="sxs-lookup"><span data-stu-id="d7d61-170">However, we can't call it a day just yet.</span></span>
<span data-ttu-id="d7d61-171">Наш Кубитс находился в штате $ \кет {0} $, когда мы выделили их, и во многом похоже на то, что Q# мы должны оставить вещи так же, как мы нашли их (или лучше!).</span><span class="sxs-lookup"><span data-stu-id="d7d61-171">Our qubits were in state $\ket{0}$ when we allocated them, and much like in life, in Q# we should leave things the same way we found them (or better!).</span></span>

### <a name="deallocate-qubits"></a><span data-ttu-id="d7d61-172">Освобождение Кубитс</span><span class="sxs-lookup"><span data-stu-id="d7d61-172">Deallocate qubits</span></span>

<span data-ttu-id="d7d61-173">Мы [`DumpMachine()`](xref:microsoft.quantum.diagnostics.dumpmachine) опять вызываем состояние после операции и, наконец, применяемся [`ResetAll`](xref:microsoft.quantum.intrinsic.resetall) к регистру кубит для сброса Кубитс в $ \кет {0} $ перед выполнением операции:</span><span class="sxs-lookup"><span data-stu-id="d7d61-173">We call [`DumpMachine()`](xref:microsoft.quantum.diagnostics.dumpmachine) again to see the post-operation state, and finally apply [`ResetAll`](xref:microsoft.quantum.intrinsic.resetall) to the qubit register to reset our qubits to $\ket{0}$ before completing the operation:</span></span>

```qsharp
            Message("After:");
            DumpMachine();

            ResetAll(qs);
```

<span data-ttu-id="d7d61-174">Обязательно, чтобы все освобожденные Кубитс были явно заданы как $ \кет {0} $ — это базовая функция Q# , так как она позволяет другим операциям точно узнавать свое состояние, когда они начинают использовать те же Кубитс (дефицит ресурсов).</span><span class="sxs-lookup"><span data-stu-id="d7d61-174">Requiring that all deallocated qubits be explicitly set to $\ket{0}$ is a basic feature of Q#, as it allows other operations to know their state precisely when they begin using those same qubits (a scarce resource).</span></span>
<span data-ttu-id="d7d61-175">Кроме того, это гарантирует, что они не будут запутанными с другими Кубитс в системе.</span><span class="sxs-lookup"><span data-stu-id="d7d61-175">Additionally, this assures that they not be entangled with any other qubits in the system.</span></span>
<span data-ttu-id="d7d61-176">Если сброс не выполняется в конце `using` блока выделения, возникнет ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="d7d61-176">If the reset is not performed at the end of a `using` allocation block, a runtime error will be thrown.</span></span>

<span data-ttu-id="d7d61-177">Теперь полный Q# файл должен выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d7d61-177">Your full Q# file should now look like this:</span></span>

```qsharp
namespace NamespaceQFT {
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Diagnostics;
    open Microsoft.Quantum.Math;
    open Microsoft.Quantum.Arrays;

    operation Perform3qubitQFT() : Unit {

        using (qs = Qubit[3]) {

            Message("Initial state |000>:");
            DumpMachine();

            //QFT:
            //first qubit:
            H(qs[0]);
            Controlled R1([qs[1]], (PI()/2.0, qs[0]));
            Controlled R1([qs[2]], (PI()/4.0, qs[0]));

            //second qubit:
            H(qs[1]);
            Controlled R1([qs[2]], (PI()/2.0, qs[1]));

            //third qubit:
            H(qs[2]);

            SWAP(qs[2], qs[0]);

            Message("After:");
            DumpMachine();

            ResetAll(qs);
        }
    }
}
```


<span data-ttu-id="d7d61-178">Q#После завершения файла и операции наша тактовая программа готова к вызову и имитации.</span><span class="sxs-lookup"><span data-stu-id="d7d61-178">With the Q# file and operation complete, our quantum program is ready to be called and simulated.</span></span>

## <a name="execute-the-program"></a><span data-ttu-id="d7d61-179">Выполнение программы</span><span class="sxs-lookup"><span data-stu-id="d7d61-179">Execute the program</span></span>

<span data-ttu-id="d7d61-180">Определив Q# операцию в `.qs` файле, теперь нужно вызвать эту операцию и просмотреть все возвращенные классические данные.</span><span class="sxs-lookup"><span data-stu-id="d7d61-180">Having defined our Q# operation in a `.qs` file, we now need to call that operation and observe any returned classical data.</span></span>
<span data-ttu-id="d7d61-181">Пока что ничего не возвращается (Помните, что наша операция, определенная выше, возвращает `Unit` ), но когда позже мы изменим Q# операцию для возврата массива результатов измерения ( `Result[]` ), мы будем решать это.</span><span class="sxs-lookup"><span data-stu-id="d7d61-181">For now, there isn't anything returned (recall that our operation defined above returns `Unit`), but when we later modify the Q# operation to return an array of measurement results (`Result[]`), we will address this.</span></span>

<span data-ttu-id="d7d61-182">Хотя Q# программа является повсеместной во всех средах, используемых для ее вызова, способ ее выполнения будет зависеть.</span><span class="sxs-lookup"><span data-stu-id="d7d61-182">While the Q# program is ubiquitous across the environments used to call it, the manner of doing so will of course vary.</span></span> <span data-ttu-id="d7d61-183">Таким образом, просто следуйте инструкциям на вкладке, соответствующей вашей программе установки: работа с Q# приложением или использование основной программы в Python или C#.</span><span class="sxs-lookup"><span data-stu-id="d7d61-183">As such, simply follow the instructions in the tab corresponding to your setup: working from the Q# application or using a host program in Python or C#.</span></span>

#### <a name="command-prompt"></a>[<span data-ttu-id="d7d61-184">Командная строка</span><span class="sxs-lookup"><span data-stu-id="d7d61-184">Command prompt</span></span>](#tab/tabid-cmdline)

<span data-ttu-id="d7d61-185">Запуск Q# программы из командной строки требует лишь небольшого изменения Q# файла.</span><span class="sxs-lookup"><span data-stu-id="d7d61-185">Running the Q# program from the command prompt requires only a small change to the Q# file.</span></span>

<span data-ttu-id="d7d61-186">Просто добавьте `@EntryPoint()` в строку, предшествующую определению операции:</span><span class="sxs-lookup"><span data-stu-id="d7d61-186">Simply add `@EntryPoint()` to a line preceding the operation definition:</span></span>

```qsharp
    @EntryPoint()
    operation Perform3qubitQFT() : Unit {
        // ...
```

<span data-ttu-id="d7d61-187">Чтобы запустить программу, откройте терминал в папке проекта и введите</span><span class="sxs-lookup"><span data-stu-id="d7d61-187">To run the program, open the terminal in the folder of your project and enter</span></span>

```dotnetcli
dotnet run
```

<span data-ttu-id="d7d61-188">После выполнения вы увидите приведенные `Message` `DumpMachine` ниже выходные данные и выводимые в консоли.</span><span class="sxs-lookup"><span data-stu-id="d7d61-188">Upon execution, you should see the `Message` and `DumpMachine` outputs below printed in your console.</span></span>


#### <a name="python"></a>[<span data-ttu-id="d7d61-189">Python</span><span class="sxs-lookup"><span data-stu-id="d7d61-189">Python</span></span>](#tab/tabid-python)

<span data-ttu-id="d7d61-190">Создайте файл узла Python: `host.py` .</span><span class="sxs-lookup"><span data-stu-id="d7d61-190">Create a Python host file: `host.py`.</span></span>

<span data-ttu-id="d7d61-191">Файл узла создается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d7d61-191">The host file is constructed as follows:</span></span> 
1. <span data-ttu-id="d7d61-192">Сначала импортируется `qsharp` модуль, который регистрирует загрузчик модуля для Q# взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="d7d61-192">First, we import the `qsharp` module, which registers the module loader for Q# interoperability.</span></span> 
    <span data-ttu-id="d7d61-193">Это позволяет Q# пространствам имен (например, `NamespaceQFT` определенному в нашем Q# файле) выглядеть как модули Python, из которых можно импортировать Q# операции.</span><span class="sxs-lookup"><span data-stu-id="d7d61-193">This allows Q# namespaces (e.g. the `NamespaceQFT` we defined in our Q# file) to appear as Python modules, from which we can import Q# operations.</span></span>
2. <span data-ttu-id="d7d61-194">Затем импортируйте Q# операции, которые будут напрямую вызывать---в этом случае `Perform3qubitQFT` .</span><span class="sxs-lookup"><span data-stu-id="d7d61-194">Then, import the Q# operations which we will directly invoke---in this case, `Perform3qubitQFT`.</span></span>
    <span data-ttu-id="d7d61-195">Нам нужно только импортировать точку входа в Q# программу (т. е. _не_ такие операции `H` , как и `R1` , которые вызываются другими Q# операциями, но никогда не являются классическим узлом).</span><span class="sxs-lookup"><span data-stu-id="d7d61-195">We need only import the entry point into a Q# program (i.e. _not_ operations like `H` and `R1`, which are called by other Q# operations but never by the classical host).</span></span>
3. <span data-ttu-id="d7d61-196">При моделировании Q# операций или функций используйте форму `<Q#callable>.simulate(<args>)` для их запуска на `QuantumSimulator()` целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="d7d61-196">In simulating Q# operations or functions, use the form `<Q#callable>.simulate(<args>)` to run them on the `QuantumSimulator()` target machine.</span></span> 

> [!NOTE]
> <span data-ttu-id="d7d61-197">Если бы мы хотели вызвать операцию на другом компьютере, например `ResourceEstimator()` , мы просто используем `<Q#callable>.estimate_resources(<args>)` .</span><span class="sxs-lookup"><span data-stu-id="d7d61-197">If we wanted to call the operation on a different machine, for example the `ResourceEstimator()`, we would simply use `<Q#callable>.estimate_resources(<args>)`.</span></span>
> <span data-ttu-id="d7d61-198">Как правило, Q# операции не зависят от компьютеров, на которых они выполняются, но некоторые функции, например, `DumpMachine` могут вести себя по-разному.</span><span class="sxs-lookup"><span data-stu-id="d7d61-198">In general, Q# operations are agnostic to the machines on which they're run, but some features such as `DumpMachine` may behave differently.</span></span>

4. <span data-ttu-id="d7d61-199">При выполнении моделирования вызов операции возвратит значения, определенные в Q# файле.</span><span class="sxs-lookup"><span data-stu-id="d7d61-199">Upon performing the simulation, the operation call will return values as defined in the Q# file.</span></span>
    <span data-ttu-id="d7d61-200">Пока ничего не возвращается, но позже мы увидим пример назначения и обработки этих значений.</span><span class="sxs-lookup"><span data-stu-id="d7d61-200">For now there is nothing returned, but later on we will see an example of assigning and processing these values.</span></span>
    <span data-ttu-id="d7d61-201">Используя итоговые данные в наших практических занятиях, мы можем выполнить все, что нам бы хотелось.</span><span class="sxs-lookup"><span data-stu-id="d7d61-201">With the resultant data in our hands and totally classical, we can do whatever we'd like with it.</span></span>

<span data-ttu-id="d7d61-202">Полный `host.py` файл должен быть следующим:</span><span class="sxs-lookup"><span data-stu-id="d7d61-202">Your full `host.py` file should be this:</span></span>

```python
import qsharp
from NamespaceQFT import Perform3qubitQFT

Perform3qubitQFT.simulate()
```

<span data-ttu-id="d7d61-203">Запустите файл Python и распечатайте его в консоли `Message` `DumpMachine` . ниже показаны выходные данные и.</span><span class="sxs-lookup"><span data-stu-id="d7d61-203">Run the Python file, and printed in your console you should see the `Message` and `DumpMachine` outputs below.</span></span> 


#### <a name="c"></a>[<span data-ttu-id="d7d61-204">C#</span><span class="sxs-lookup"><span data-stu-id="d7d61-204">C#</span></span>](#tab/tabid-csharp)

<span data-ttu-id="d7d61-205">Следуя тем же инструкциям, что и в разделе [руководство по установке](xref:microsoft.quantum.install.cs), создайте файл узла C# и переименуйте его в `host.cs` .</span><span class="sxs-lookup"><span data-stu-id="d7d61-205">Following the same instructions as in the [install guide](xref:microsoft.quantum.install.cs), create a C# host file, and rename it to `host.cs`.</span></span>

<span data-ttu-id="d7d61-206">Узел C# состоит из четырех частей:</span><span class="sxs-lookup"><span data-stu-id="d7d61-206">The C# host has four parts:</span></span>
1. <span data-ttu-id="d7d61-207">Создание квантового симулятора.</span><span class="sxs-lookup"><span data-stu-id="d7d61-207">Construct a quantum simulator.</span></span>
    <span data-ttu-id="d7d61-208">В приведенном ниже коде это переменная `qsim` .</span><span class="sxs-lookup"><span data-stu-id="d7d61-208">In the code below, this is the variable `qsim`.</span></span>
2. <span data-ttu-id="d7d61-209">Вычисление всех аргументов для квантового алгоритма.</span><span class="sxs-lookup"><span data-stu-id="d7d61-209">Compute any arguments required for the quantum algorithm.</span></span>
    <span data-ttu-id="d7d61-210">В этом примере нет ни одного.</span><span class="sxs-lookup"><span data-stu-id="d7d61-210">There are none in this example.</span></span>
3. <span data-ttu-id="d7d61-211">Выполнение квантового алгоритма.</span><span class="sxs-lookup"><span data-stu-id="d7d61-211">Run the quantum algorithm.</span></span> 
    <span data-ttu-id="d7d61-212">Каждая Q# операция создает класс C# с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="d7d61-212">Each Q# operation generates a C# class with the same name.</span></span> 
    <span data-ttu-id="d7d61-213">Этот класс содержит метод `Run`, который **асинхронно** выполняет соответствующую операцию.</span><span class="sxs-lookup"><span data-stu-id="d7d61-213">This class has a `Run` method that **asynchronously** executes the operation.</span></span>
    <span data-ttu-id="d7d61-214">Асинхронное выполнение имитирует асинхронный процесс на реальном оборудовании.</span><span class="sxs-lookup"><span data-stu-id="d7d61-214">The execution is asynchronous because execution on actual hardware will be asynchronous.</span></span> 
    <span data-ttu-id="d7d61-215">Так как `Run` метод является асинхронным, мы вызываем `Wait()` метод. он блокирует выполнение до завершения задачи и возвращает результат в синхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="d7d61-215">Because the `Run` method is asynchronous, we call the `Wait()` method; this blocks execution until the task completes and returns the result synchronously.</span></span> 
4. <span data-ttu-id="d7d61-216">Обработать возвращенный результат операции.</span><span class="sxs-lookup"><span data-stu-id="d7d61-216">Process the returned result of the operation.</span></span>
    <span data-ttu-id="d7d61-217">Пока операция не возвращает ничего.</span><span class="sxs-lookup"><span data-stu-id="d7d61-217">For now, the operation returns nothing.</span></span>


```csharp
using System;

using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;

namespace NamespaceQFT
{
    class Driver
    {
        static void Main(string[] args)
        {
            using (var qsim = new QuantumSimulator())
            {
                Perform3QubitQFT.Run(qsim).Wait();
            }
            
            System.Console.WriteLine("Press any key to continue...");
            Console.ReadKey();
        }
    }
}

```
<span data-ttu-id="d7d61-218">Запустите приложение, и выходные данные должны соответствовать приведенным ниже данным.</span><span class="sxs-lookup"><span data-stu-id="d7d61-218">Run the application, and your output should match that below.</span></span>
<span data-ttu-id="d7d61-219">Программа завершает работу после нажатия любой клавиши.</span><span class="sxs-lookup"><span data-stu-id="d7d61-219">The program will exit after you press a key.</span></span>
***

```Output
Initial state |000>:
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
|1>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|2>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|3>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|4>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|5>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|6>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|7>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
After:
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|1>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|2>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|3>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|4>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|5>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|6>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|7>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
```

<span data-ttu-id="d7d61-220">При вызове в симуляторе с полным состоянием `DumpMachine()` предоставляет эти множественные представления вавефунктион состояния такта.</span><span class="sxs-lookup"><span data-stu-id="d7d61-220">When called on the full-state simulator, `DumpMachine()` provides these mutliple representations of the quantum state's wavefunction.</span></span> <span data-ttu-id="d7d61-221">Возможные состояния системы $n $-кубит могут быть представлены в виде $2 ^ n $ вычислительных показателей, каждый из которых имеет соответствующий сложный коэффициент (просто амплитуда и фаза).</span><span class="sxs-lookup"><span data-stu-id="d7d61-221">The possible states of an $n$-qubit system can be represented by $2^n$ computational basis states, each with a corresponding complex coefficient (simply an amplitude and a phase).</span></span>
<span data-ttu-id="d7d61-222">Состояние вычислительных операций соответствует всем возможным двоичным строкам длиной $n $---т. е. все возможные сочетания состояний кубит $ \кет {0} $ и $ \кет {1} $, где каждая двоичная цифра соответствует отдельному кубит.</span><span class="sxs-lookup"><span data-stu-id="d7d61-222">The computational basis states correspond to all the possible binary strings of length $n$---that is, all the possible combinations of qubit states $\ket{0}$ and $\ket{1}$, where each binary digit corresponds to an individual qubit.</span></span>

<span data-ttu-id="d7d61-223">Первая строка содержит комментарий с идентификаторами соответствующего Кубитс в значительном порядке.</span><span class="sxs-lookup"><span data-stu-id="d7d61-223">The first row provides a comment with the IDs of the corresponding qubits in their significant order.</span></span>
<span data-ttu-id="d7d61-224">Кубит `2` является «самым значимым» просто означает, что в двоичном представлении вектора состояния «\кет{и} $» состояние кубит `2` соответствует крайней левой разрядности.</span><span class="sxs-lookup"><span data-stu-id="d7d61-224">Qubit `2` being the "most significant" simply means that in the binary representation of basis state vector $\ket{i}$, the state of qubit `2` corresponds to the left-most digit.</span></span> <span data-ttu-id="d7d61-225">Например, $ \кет {6} = \кет {110} $ состоит из Кубитс `2` и `1` в $ \кет {1} $ и кубит `0` в $ \кет {0} $.</span><span class="sxs-lookup"><span data-stu-id="d7d61-225">For example, $\ket{6} = \ket{110}$ comprises qubits `2` and `1` both in $\ket{1}$ and qubit `0` in $\ket{0}$.</span></span>


<span data-ttu-id="d7d61-226">Остальные строки описывают амплитуду вероятности по измерению вектора состояния базы данных $ \кет{и} $ в декартовой и полярной форматах.</span><span class="sxs-lookup"><span data-stu-id="d7d61-226">The rest of the rows describe the probability amplitude of measuring the basis state vector $\ket{i}$ in both Cartesian and polar formats.</span></span>
<span data-ttu-id="d7d61-227">Подробно для первой строки нашего входного состояния $ \кет {000} $:</span><span class="sxs-lookup"><span data-stu-id="d7d61-227">In detail for the first row of our input state $\ket{000}$:</span></span>
* <span data-ttu-id="d7d61-228">**`|0>:`** Эта строка соответствует `0` определенному вычислительному состоянию (учитывая, что начальное состояние после выделения было равно $ \кет {000} $, мы бы ожидали, что это единственное состояние с амплитудой вероятности на этом этапе).</span><span class="sxs-lookup"><span data-stu-id="d7d61-228">**`|0>:`** this row corresponds to the `0` computational basis state (given that our initial state post-allocation was $\ket{000}$, we would expect this to be the only state with probability amplitude at this point).</span></span>
* <span data-ttu-id="d7d61-229">**`1.000000 +  0.000000 i`**: амплитуда вероятности в формате Декарт.</span><span class="sxs-lookup"><span data-stu-id="d7d61-229">**`1.000000 +  0.000000 i`**: the probability amplitude in Cartesian format.</span></span>
* <span data-ttu-id="d7d61-230">**` == `**: `equal` знак разделяет оба эквивалентных представления.</span><span class="sxs-lookup"><span data-stu-id="d7d61-230">**` == `**: the `equal` sign separates both equivalent representations.</span></span>
* <span data-ttu-id="d7d61-231">**`********************`**: Графическое представление величины, количество `*` пропорционально вероятности измерения этого вектора состояния.</span><span class="sxs-lookup"><span data-stu-id="d7d61-231">**`********************`**: A graphical representation of the magnitude, the number of `*` is proportionate to the probability of measuring this state vector.</span></span> 
* <span data-ttu-id="d7d61-232">**`[ 1.000000 ]`**: числовое значение величины.</span><span class="sxs-lookup"><span data-stu-id="d7d61-232">**`[ 1.000000 ]`**: the numeric value of the magnitude</span></span>
* <span data-ttu-id="d7d61-233">**`    ---`**— Графическое представление фазы амплитуды.</span><span class="sxs-lookup"><span data-stu-id="d7d61-233">**`    ---`**: A graphical representation of the amplitude's phase.</span></span>
* <span data-ttu-id="d7d61-234">**`[ 0.0000 rad ]`**: числовое значение этапа (в радианах).</span><span class="sxs-lookup"><span data-stu-id="d7d61-234">**`[ 0.0000 rad ]`**: the numeric value of the phase (in radians).</span></span>

<span data-ttu-id="d7d61-235">Как величина, так и фаза отображаются с графическим представлением.</span><span class="sxs-lookup"><span data-stu-id="d7d61-235">Both the magnitude and the phase are displayed with a graphical representation.</span></span> <span data-ttu-id="d7d61-236">Представление величины является простым: оно показывает полоску `*` , а чем выше вероятность, тем больше будет полоска.</span><span class="sxs-lookup"><span data-stu-id="d7d61-236">The magnitude representation is straightforward: it shows a bar of `*`, and the higher the probability, the larger the bar will be.</span></span> <span data-ttu-id="d7d61-237">Для этапа см. раздел [тестирование и отладка. функции дампа](xref:microsoft.quantum.guide.testingdebugging#dump-functions) для возможных представлений символов на основе диапазонов угла.</span><span class="sxs-lookup"><span data-stu-id="d7d61-237">For the phase, see [Testing and debugging: dump functions](xref:microsoft.quantum.guide.testingdebugging#dump-functions) for the possible symbol representations based on angle ranges.</span></span>


<span data-ttu-id="d7d61-238">Таким образом, выводимые данные показывают, что наши запрограммированные Шлюзы преобразуют состояние из</span><span class="sxs-lookup"><span data-stu-id="d7d61-238">So, the printed output is illustrating that our programmed gates transformed our state from</span></span>

<span data-ttu-id="d7d61-239">$ $ \кет{\пси} \_ {Initial} = \кет {000} $ $</span><span class="sxs-lookup"><span data-stu-id="d7d61-239">$$ \ket{\psi}\_{initial} = \ket{000} $$</span></span>

<span data-ttu-id="d7d61-240">значение</span><span class="sxs-lookup"><span data-stu-id="d7d61-240">to</span></span> 

<span data-ttu-id="d7d61-241">$ $ \бегин{алигн} \кет{\пси} \_ {final} &= \фрак {1} {\скрт} \лефт (\кет \кет + \кет + \кет + \кет {8} {000} {001} {010} {011} {100} + \кет {101} + \кет {110} + \кет {111} \ригхт) \\ \\ &= \frac {1} {\sqrt{2 ^ n}} \sum \_ {j = 0} ^ {2 ^ n-1} \ket{j}, \end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="d7d61-241">$$ \begin{align} \ket{\psi}\_{final} &= \frac{1}{\sqrt{8}} \left( \ket{000} + \ket{001} + \ket{010} + \ket{011} + \ket{100} + \ket{101} + \ket{110} + \ket{111}  \right) \\\\ &= \frac{1}{\sqrt{2^n}}\sum\_{j=0}^{2^n-1} \ket{j}, \end{align} $$</span></span>

<span data-ttu-id="d7d61-242">что является точным поведением преобразования «3-кубит Фурье».</span><span class="sxs-lookup"><span data-stu-id="d7d61-242">which is precisely the behavior of the 3-qubit Fourier transform.</span></span> 

<span data-ttu-id="d7d61-243">Если вы хотите узнать, как затрагиваются другие входные состояния, мы рекомендуем поэкспериментировать с применением операций кубит перед преобразованием.</span><span class="sxs-lookup"><span data-stu-id="d7d61-243">If you are curious about how other input states are affected, we encourage you to play around with applying qubit operations before the transform.</span></span>

## <a name="adding-measurements"></a><span data-ttu-id="d7d61-244">Добавление измерений</span><span class="sxs-lookup"><span data-stu-id="d7d61-244">Adding measurements</span></span>

<span data-ttu-id="d7d61-245">К сожалению, в результате механики тактовой задержки говорится, что в реальной тактовой системе не может быть такой `DumpMachine` функции.</span><span class="sxs-lookup"><span data-stu-id="d7d61-245">Unfortunately, a cornerstone of quantum mechanics tells us that a real quantum system cannot have such a `DumpMachine` function.</span></span> <span data-ttu-id="d7d61-246">Вместо этого мы вынуждены извлекать информацию с помощью измерений, что в целом не только дает нам полное состояние такта, но и радикально изменяет саму систему.</span><span class="sxs-lookup"><span data-stu-id="d7d61-246">Instead, we're forced to extract information through measurements, which in general not only fail to provide us the full quantum state, but can also drastically alter the system itself.</span></span>
<span data-ttu-id="d7d61-247">Существует множество видов измерений такта, но мы будем сосредоточиться на самых базовых: проецированные измерения на одном Кубитс.</span><span class="sxs-lookup"><span data-stu-id="d7d61-247">There are many sorts of quantum measurements, but we will focus on the most basic: projective measurements on single qubits.</span></span>
<span data-ttu-id="d7d61-248">При измерении на определенном уровне (например, на основе вычислительной базы $ \{ \кет {0} , \кет {1} \} $) состояние кубит проецируется на то, что было измерено по отдельности,---таким образом удаление любого из них.</span><span class="sxs-lookup"><span data-stu-id="d7d61-248">Upon measurement in a given basis (e.g. the computational basis $ \{ \ket{0}, \ket{1} \} $), the qubit state is projected onto whichever basis state was measured---hence destroying any superposition between the two.</span></span>

<span data-ttu-id="d7d61-249">Чтобы реализовать измерения в Q# программе, мы используем `M` операцию (FROM `Microsoft.Quantum.Intrinsic` ), которая возвращает `Result` тип.</span><span class="sxs-lookup"><span data-stu-id="d7d61-249">To implement measurements within a Q# program, we use the `M` operation (from `Microsoft.Quantum.Intrinsic`), which returns a `Result` type.</span></span>

<span data-ttu-id="d7d61-250">Сначала мы изменим `Perform3QubitQFT` операцию, чтобы вернуть массив результатов измерения, `Result[]` вместо `Unit` .</span><span class="sxs-lookup"><span data-stu-id="d7d61-250">First, we modify our `Perform3QubitQFT` operation to return an array of measurement results, `Result[]`, instead of `Unit`.</span></span>

```qsharp
    operation Perform3QubitQFT() : Result[] {
```

#### <a name="define-and-initialize-result-array"></a><span data-ttu-id="d7d61-251">Определение и инициализация `Result[]` массива</span><span class="sxs-lookup"><span data-stu-id="d7d61-251">Define and initialize `Result[]` array</span></span>

<span data-ttu-id="d7d61-252">Прежде чем даже выделять Кубитс (т. е. перед `using` инструкцией), мы объявляем и привязали этот массив length-3 ( `Result` по одному для каждого кубит):</span><span class="sxs-lookup"><span data-stu-id="d7d61-252">Before even allocating qubits (i.e. before the `using` statement), we declare and bind this length-3 array (one `Result` for each qubit):</span></span> 

```qsharp
        mutable resultArray = new Result[3];
```

<span data-ttu-id="d7d61-253">`mutable`Преднаправленное ключевое слово `resultArray` позволяет позже повторно привязать переменную в коде---например, при добавлении результатов измерения.</span><span class="sxs-lookup"><span data-stu-id="d7d61-253">The `mutable` keyword prefacing `resultArray` allows the variable to be rebound later in the code---for example, when adding our measurement results.</span></span>

#### <a name="perform-measurements-in-a-for-loop-and-add-results-to-array"></a><span data-ttu-id="d7d61-254">Выполнение измерений в `for` цикле и добавление результатов в массив</span><span class="sxs-lookup"><span data-stu-id="d7d61-254">Perform measurements in a `for` loop and add results to array</span></span>

<span data-ttu-id="d7d61-255">После выполнения операций преобразования Фурье внутри `using` блока вставьте следующий код:</span><span class="sxs-lookup"><span data-stu-id="d7d61-255">After the Fourier transform operations inside the `using` block, insert the following code:</span></span>

```qsharp
            for(i in IndexRange(qs)) {
                set resultArray w/= i <- M(qs[i]);
            }
```
<span data-ttu-id="d7d61-256">[`IndexRange`](xref:microsoft.quantum.arrays.indexrange)Функция, вызываемая для массива (например, наш массив Кубитс, `qs` ), возвращает диапазон по индексам массива.</span><span class="sxs-lookup"><span data-stu-id="d7d61-256">The [`IndexRange`](xref:microsoft.quantum.arrays.indexrange) function called on an array (e.g. our array of qubits, `qs`) returns a range over the indices of the array.</span></span> <span data-ttu-id="d7d61-257">Здесь мы используем его в нашем `for` цикле, чтобы последовательно измерять каждую кубит с помощью `M(qs[i])` инструкции.</span><span class="sxs-lookup"><span data-stu-id="d7d61-257">Here, we use it in our `for` loop to sequentially measure each qubit using the `M(qs[i])` statement.</span></span>
<span data-ttu-id="d7d61-258">Затем каждый измеряемый `Result` тип ( `Zero` или `One` ) добавляется в соответствующую позиции индекса в `resultArray` с помощью инструкции UPDATE и REASSIGN.</span><span class="sxs-lookup"><span data-stu-id="d7d61-258">Each measured `Result` type (either `Zero` or `One`) is then added to the corresponding index position in `resultArray` with an update-and-reassign statement.</span></span>

> [!NOTE]
> <span data-ttu-id="d7d61-259">Синтаксис этой инструкции уникален для Q# , но соответствует аналогичному повторному назначению переменной, представленному `resultArray[i] <- M(qs[i])` на других языках, таких как F # и R.</span><span class="sxs-lookup"><span data-stu-id="d7d61-259">The syntax of this statement is unique to Q#, but corresponds to the similar variable reassignment `resultArray[i] <- M(qs[i])` seen in other languages such as F# and R.</span></span>

<span data-ttu-id="d7d61-260">Ключевое слово `set` всегда используется для повторного присвоения переменных, привязанных с помощью `mutable` .</span><span class="sxs-lookup"><span data-stu-id="d7d61-260">The keyword `set` is always used to reassign variables bound using `mutable`.</span></span>

#### <a name="return-resultarray"></a><span data-ttu-id="d7d61-261">Вернул `resultArray`</span><span class="sxs-lookup"><span data-stu-id="d7d61-261">Return `resultArray`</span></span>

<span data-ttu-id="d7d61-262">Если все три Кубитс измерения и результаты добавлены в `resultArray` , мы сможем сбросить и отменить выделение Кубитс как раньше.</span><span class="sxs-lookup"><span data-stu-id="d7d61-262">With all three qubits measured and the results added to `resultArray`, we are safe to reset and deallocate the qubits as before.</span></span>
<span data-ttu-id="d7d61-263">После `using` закрытия блока вставьте</span><span class="sxs-lookup"><span data-stu-id="d7d61-263">After the `using` block's close, insert</span></span>

```qsharp
        return resultArray;
```
<span data-ttu-id="d7d61-264">чтобы возвратить результат нашей операции в конечном итоге.</span><span class="sxs-lookup"><span data-stu-id="d7d61-264">to ultimately return the output of our operation.</span></span> 

### <a name="understanding-the-effects-of-measurement"></a><span data-ttu-id="d7d61-265">Основные сведения о влиянии измерения</span><span class="sxs-lookup"><span data-stu-id="d7d61-265">Understanding the effects of measurement</span></span>

<span data-ttu-id="d7d61-266">Давайте изменим размещение наших `DumpMachine` функций для вывода состояния до и после измерений.</span><span class="sxs-lookup"><span data-stu-id="d7d61-266">Let's change the placement of our `DumpMachine` functions to output the state before and after the measurements.</span></span>
<span data-ttu-id="d7d61-267">Окончательный код операции должен выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d7d61-267">The final operation code should look like:</span></span> 

```qsharp
    operation Perform3QubitQFT() : Result[] {

        mutable resultArray = new Result[3];

        using (qs = Qubit[3]) {

            //QFT:
            //first qubit:
            H(qs[0]);
            Controlled R1([qs[1]], (PI()/2.0, qs[0]));
            Controlled R1([qs[2]], (PI()/4.0, qs[0]));

            //second qubit:
            H(qs[1]);
            Controlled R1([qs[2]], (PI()/2.0, qs[1]));

            //third qubit:
            H(qs[2]);

            SWAP(qs[2], qs[0]);

            Message("Before measurement: ");
            DumpMachine();

            for(i in IndexRange(qs)) {
                set resultArray w/= i <- M(qs[i]);
            }

            Message("After measurement: ");
            DumpMachine();

            ResetAll(qs);
        }
        return resultArray;
    }
}
```

<span data-ttu-id="d7d61-268">Если вы работаете из командной строки, возвращаемый массив будет просто напечатан непосредственно на консоли в конце выполнения.</span><span class="sxs-lookup"><span data-stu-id="d7d61-268">If you are working from the command prompt, the returned array will simply be printed directly to the console at the end of the execution.</span></span>
<span data-ttu-id="d7d61-269">В противном случае обновите программу узла для обработки возвращенного массива.</span><span class="sxs-lookup"><span data-stu-id="d7d61-269">Otherwise, update your host program to process the returned array.</span></span>

#### <a name="command-prompt"></a>[<span data-ttu-id="d7d61-270">Командная строка</span><span class="sxs-lookup"><span data-stu-id="d7d61-270">Command prompt</span></span>](#tab/tabid-cmdline)

<span data-ttu-id="d7d61-271">Чтобы получить более полное представление о возвращенном массиве, который будет напечатан в консоли, мы можем добавить еще один `Message` в Q# файл непосредственно перед `return` инструкцией:</span><span class="sxs-lookup"><span data-stu-id="d7d61-271">To have more understanding of the returned array which will be printed in the console, we can add another `Message` in the Q# file just before the `return` statement:</span></span>

```qsharp
        Message("Post-QFT measurement results [qubit0, qubit1, qubit2]: ");
        return resultArray;
```

<span data-ttu-id="d7d61-272">Запустите проект, и выходные данные должны выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d7d61-272">Run the project, and your output should look similar to the following:</span></span>

```Output
Before measurement: 
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|1>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|2>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|3>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|4>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|5>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|6>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|7>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
After measurement:
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|1>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|2>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|3>:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
|4>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|5>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|6>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|7>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]

Post-QFT measurement results [qubit0, qubit1, qubit2]: 
[One,One,Zero]
```

#### <a name="python"></a>[<span data-ttu-id="d7d61-273">Python</span><span class="sxs-lookup"><span data-stu-id="d7d61-273">Python</span></span>](#tab/tabid-python)

<span data-ttu-id="d7d61-274">Обновите программу Python следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d7d61-274">Update your Python program to the following:</span></span>

```python
import qsharp
from NamespaceQFT import Perform3QubitQFT

measurementResult = Perform3QubitQFT.simulate()
print("\n")
print("Measured post-QFT state: [qubit0, qubit1, qubit2]")
print(measurementResult)

# reversing order to show corresponding basis state in binary form
binaryCompBasisState = ""
for i in measurementResult:
    binaryCompBasisState = str(i) + binaryCompBasisState
print("Corresponding basis state in binary:")
print("|" + binaryCompBasisState + ">")
```

<span data-ttu-id="d7d61-275">Запустите файл, и выходные данные должны выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d7d61-275">Run the file, and your output should look similar to the following:</span></span>

```Output
Before measurement: 
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|1>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|2>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|3>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|4>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|5>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|6>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|7>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
After measurement: 
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|1>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|2>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|3>:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
|4>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|5>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|6>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|7>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   

Post-QFT measurement results [qubit0, qubit1, qubit2]: 
[1, 1, 0]

Corresponding basis state in binary:
|011>
```

#### <a name="c"></a>[<span data-ttu-id="d7d61-276">C#</span><span class="sxs-lookup"><span data-stu-id="d7d61-276">C#</span></span>](#tab/tabid-csharp)

<span data-ttu-id="d7d61-277">Теперь, когда наша операция возвращает результат, замените вызов метода `Wait()` на выборку `Result` Свойства.</span><span class="sxs-lookup"><span data-stu-id="d7d61-277">Now that our operation is returning a result, replace the method call `Wait()` with fetching the `Result` property.</span></span> <span data-ttu-id="d7d61-278">Это по-прежнему выполняет ту же синхронности, что обсуждалось ранее, и мы можем напрямую привязать это значение к переменной `measurementResult` .</span><span class="sxs-lookup"><span data-stu-id="d7d61-278">This still accomplishes the same synchronicity discussed earlier, and we can directly bind this value to the variable `measurementResult`.</span></span>

```csharp
using System;

using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;

namespace NamespaceQFT
{
    class Driver
    {
        static void Main(string[] args)
        {
            using (var qsim = new QuantumSimulator())
            {
                var measurementResult = Perform3QubitQFT.Run(qsim).Result;
                System.Console.WriteLine(
                    $"Post-QFT measurement results [qubit0, qubit1, qubit2]: ");
                System.Console.WriteLine(
                    measurementResult);

                // reversing order to show corresponding basis state in binary form
                string binaryCompBasisState = String.Empty;

                foreach (Result i in measurementResult)
                {
                    string iString = i.ToString();
                    binaryCompBasisState = iString + binaryCompBasisState;
                }
                binaryCompBasisState = "|" + binaryCompBasisState + ">";
                System.Console.WriteLine(
                    $"Corresponding basis state in binary:");
                System.Console.WriteLine(
                    binaryCompBasisState);
            }
            
            System.Console.WriteLine("Press any key to continue...");
            Console.ReadKey();
        }
    }
}
```

<span data-ttu-id="d7d61-279">Запустите проект, и выходные данные должны выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d7d61-279">Run the project, and your output should look similar to the following:</span></span>

```Output
Before measurement: 
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|1>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|2>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|3>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|4>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|5>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|6>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|7>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
After measurement:
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|1>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|2>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|3>:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
|4>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|5>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|6>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|7>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]

Post-QFT measurement results [qubit0, qubit1, qubit2]: 
[One,One,Zero]

Corresponding basis state in binary:
|ZeroOneOne>

Press any key to continue...
```
***

<span data-ttu-id="d7d61-280">В этих выходных данных показано несколько различных моментов.</span><span class="sxs-lookup"><span data-stu-id="d7d61-280">This output illustrates a few different things:</span></span>
1. <span data-ttu-id="d7d61-281">Сравнивая возвращенный результат с предварительным измерением `DumpMachine` , он четко _не_ иллюстрирует ПОшаговую кфтную перестановку на основе состояния.</span><span class="sxs-lookup"><span data-stu-id="d7d61-281">Comparing the returned result to the pre-measurement `DumpMachine`, it clearly does _not_ illustrate the post-QFT superposition over basis states.</span></span>
    <span data-ttu-id="d7d61-282">Измерение возвращает только одно состояние основания с вероятностью, которое определяется амплитудой этого состояния в вавефунктионе системы.</span><span class="sxs-lookup"><span data-stu-id="d7d61-282">A measurement only returns a single basis state, with a probability determined by the amplitude of that state in the system's wavefunction.</span></span>
2. <span data-ttu-id="d7d61-283">С момента последующей единицы `DumpMachine` измерения видно, что измерение _изменяет_ само состояние, проецирование его из первоначального перестановки в поверх состояний в одно состояние, соответствующее измеренному значению.</span><span class="sxs-lookup"><span data-stu-id="d7d61-283">From the post-measurement `DumpMachine`, we see that measurement _changes_ the state itself, projecting it from the initial superposition over basis states to the single basis state that corresponds to the measured value.</span></span>

<span data-ttu-id="d7d61-284">Если бы нам пришлось повторить эту операцию несколько раз, мы увидим, что статистика результатов начинается с одинаковой взвешенной части состояния после Кфт, что дает случайному результату на каждом снимке.</span><span class="sxs-lookup"><span data-stu-id="d7d61-284">If we were to repeat this operation many times, we would see the result statistics begin to illustrate the equally weighted superposition of the post-QFT state that gives rise to a random result on each shot.</span></span>
<span data-ttu-id="d7d61-285">_Однако_, помимо неэффективного и неидеальны, это, тем не менее, будет воспроизводить только относительные амплитуды базисных состояний, а не относительные этапы между ними.</span><span class="sxs-lookup"><span data-stu-id="d7d61-285">_However_, besides being inefficient and still imperfect, this would nevertheless only reproduce the relative amplitudes of the basis states, not the relative phases between them.</span></span>
<span data-ttu-id="d7d61-286">Последнее не является проблемой в этом примере, но будут отображены относительные этапы, если для Кфт более сложным входом, чем $ \кет {000} $.</span><span class="sxs-lookup"><span data-stu-id="d7d61-286">The latter is not an issue in this example, but we would see relative phases appear if given a more complex input to the QFT than $\ket{000}$.</span></span>

#### <a name="partial-measurements"></a><span data-ttu-id="d7d61-287">Частичные измерения</span><span class="sxs-lookup"><span data-stu-id="d7d61-287">Partial measurements</span></span> 
<span data-ttu-id="d7d61-288">Чтобы узнать, как измерение только некоторых Кубитс ККМ может повлиять на состояние системы, попробуйте добавить следующее в `for` цикле после строки измерения:</span><span class="sxs-lookup"><span data-stu-id="d7d61-288">To explore how measuring only some qubits of the register can affect the system's state, try adding the following inside the `for` loop, after the measurement line:</span></span>
```qsharp
                let iString = IntAsString(i);
                Message("After measurement of qubit " + iString + ":");
                DumpMachine();
```

<span data-ttu-id="d7d61-289">Обратите внимание, что для доступа к `IntAsString` функции потребуется добавить</span><span class="sxs-lookup"><span data-stu-id="d7d61-289">Note that to access the `IntAsString` function you will have to add</span></span> 
```qsharp
    open Microsoft.Quantum.Convert;
```
<span data-ttu-id="d7d61-290">с остальными `open` операторами пространства имен.</span><span class="sxs-lookup"><span data-stu-id="d7d61-290">with the rest of the namespace `open` statements.</span></span>

<span data-ttu-id="d7d61-291">В результирующих выходных данных вы увидите постепенное проецирование на подпространства при измерении каждого кубит.</span><span class="sxs-lookup"><span data-stu-id="d7d61-291">In the resulting output, you will see the gradual projection into subspaces as each qubit is measured.</span></span>


## <a name="use-the-no-locq-libraries"></a><span data-ttu-id="d7d61-292">Использование Q# библиотек</span><span class="sxs-lookup"><span data-stu-id="d7d61-292">Use the Q# libraries</span></span>
<span data-ttu-id="d7d61-293">Как упоминалось во введении, значительная часть Q# питания в том факте, что она позволяет получить более абстрактные сведения о работе с отдельными Кубитс.</span><span class="sxs-lookup"><span data-stu-id="d7d61-293">As we mentioned in the introduction, much of Q#'s power rests in the fact that it allows you to abstract-away the worries of dealing with individual qubits.</span></span>
<span data-ttu-id="d7d61-294">В действительности, если вы хотите разрабатывать масштабируемые, применимые тактовые программы, не беспокойтесь о том, `H` проходит ли операция до или после определенного вращения, вы замедляете работу.</span><span class="sxs-lookup"><span data-stu-id="d7d61-294">Indeed, if you want to develop full-scale, applicable quantum programs, worrying about whether an `H` operation goes before or after a particular rotation would only slow you down.</span></span> 

<span data-ttu-id="d7d61-295">Q#Библиотеки содержат операцию [Кфт](xref:microsoft.quantum.canon.qft) , которую можно просто взять и применить для любого числа Кубитс.</span><span class="sxs-lookup"><span data-stu-id="d7d61-295">The Q# libraries contain the [QFT](xref:microsoft.quantum.canon.qft) operation, which you can simply take and apply for any number of qubits.</span></span>
<span data-ttu-id="d7d61-296">Чтобы придать ему возможность, определите в файле новую операцию Q# , имеющую то же содержимое `Perform3QubitQFT` , но со всеми первыми, `H` `SWAP` замененными двумя простыми линиями:</span><span class="sxs-lookup"><span data-stu-id="d7d61-296">To give it a try, define a new operation in your Q# file which has the same contents of `Perform3QubitQFT`, but with everything from the first `H` to the `SWAP` replaced by two easy lines:</span></span>
```qsharp
            let register = BigEndian(qs);    //from Microsoft.Quantum.Arithmetic
            QFT(register);                   //from Microsoft.Quantum.Canon
```
<span data-ttu-id="d7d61-297">В первой строке просто создается [`BigEndian`](xref:microsoft.quantum.arithmetic.bigendian) выражение выделенного массива Кубитс, то `qs` есть операция [Кфт](xref:microsoft.quantum.canon.qft) принимает в качестве аргумента.</span><span class="sxs-lookup"><span data-stu-id="d7d61-297">The first line simply creates a [`BigEndian`](xref:microsoft.quantum.arithmetic.bigendian) expression of the allocated array of qubits, `qs`, which is what the [QFT](xref:microsoft.quantum.canon.qft) operation takes as an argument.</span></span>
<span data-ttu-id="d7d61-298">Это соответствует упорядочению индексов Кубитс в регистре.</span><span class="sxs-lookup"><span data-stu-id="d7d61-298">This corresponds to index ordering of the qubits in the register.</span></span>

<span data-ttu-id="d7d61-299">Чтобы получить доступ к этим операциям, добавьте `open` в начало файла инструкции для соответствующих пространств имен Q# .</span><span class="sxs-lookup"><span data-stu-id="d7d61-299">To have access to these operations, add `open` statements for their respective namespaces at the beginning of the Q# file:</span></span>
```qsharp
    open Microsoft.Quantum.Canon;
    open Microsoft.Quantum.Arithmetic;
```

<span data-ttu-id="d7d61-300">Теперь настройте программу для вызова имени новой операции (например `PerformIntrinsicQFT` ,) и присвойте ей попробуйте.</span><span class="sxs-lookup"><span data-stu-id="d7d61-300">Now, adjust your host program to call the name of your new operation (e.g. `PerformIntrinsicQFT`), and give it a whirl.</span></span>

<span data-ttu-id="d7d61-301">Чтобы увидеть реальное преимущество использования Q# операций с библиотекой, измените число Кубитс на что-либо, отличное от `3` :</span><span class="sxs-lookup"><span data-stu-id="d7d61-301">To see the real benefit of using the Q# library operations, change the number of qubits to something other than `3`:</span></span>
```qsharp
        mutable resultArray = new Result[4]; 

        using (qs = Qubit[4]) {
            //...
        }
```
<span data-ttu-id="d7d61-302">Таким образом, можно применить правильный Кфт для любого определенного числа Кубитс, не заботясь о новых `H` операциях и поворотах для каждого кубит.</span><span class="sxs-lookup"><span data-stu-id="d7d61-302">You can thus apply the proper QFT for any given number of qubits, without having to worry about the mess of new `H` operations and rotations on each qubit.</span></span>

<span data-ttu-id="d7d61-303">Обратите внимание, что тактовый симулятор занимает больше времени, так как вы увеличиваете число Кубитс---точно, почему мы надеемся на работу с реальными тактами!</span><span class="sxs-lookup"><span data-stu-id="d7d61-303">Note that the quantum simulator takes exponentially more time to run as you increase the number of qubits---precisely why we look forward to real quantum hardware!</span></span>













