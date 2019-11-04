---
title: 'Q # Стандартные библиотеки — управление и поток | Документация Майкрософт'
description: 'Q # Стандартные библиотеки — управление и последовательность'
author: QuantumWriter
uid: microsoft.quantum.concepts.control-flow
ms.author: martinro@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 5e865dbb48029724b6f507ecb63b85d10d80c9a7
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/29/2019
ms.locfileid: "73185653"
---
# <a name="higher-order-control-flow"></a><span data-ttu-id="18cd6-103">Поток управления высшего порядка</span><span class="sxs-lookup"><span data-stu-id="18cd6-103">Higher-Order Control Flow</span></span> #

<span data-ttu-id="18cd6-104">Одна из основных ролей стандартной библиотеки заключается в том, чтобы упростить выражать алгоритмы, основанные на высоком уровне, в качестве [тактовых программ](https://en.wikipedia.org/wiki/Quantum_programming).</span><span class="sxs-lookup"><span data-stu-id="18cd6-104">One of the primary roles of the standard library is to make it easier to express high-level algorithmic ideas as [quantum programs](https://en.wikipedia.org/wiki/Quantum_programming).</span></span>
<span data-ttu-id="18cd6-105">Таким же, Q # Canon предоставляет множество различных конструкций управления потоком, каждый из которых реализуется с помощью частичного применения функций и операций.</span><span class="sxs-lookup"><span data-stu-id="18cd6-105">Thus, the Q# canon provides a variety of different flow control constructs, each implemented using partial application of functions and operations.</span></span>
<span data-ttu-id="18cd6-106">В качестве примера рассмотрим случай, когда один из них хочет создать «КНОТную лестницу» для регистра:</span><span class="sxs-lookup"><span data-stu-id="18cd6-106">Jumping immediately into an example, consider the case in which one wants to construct a "CNOT ladder" on a register:</span></span>

```qsharp
let nQubits = Length(register);
CNOT(register[0], register[1]);
CNOT(register[1], register[2]);
// ...
CNOT(register[nQubits - 2], register[nQubits - 1]);
```

<span data-ttu-id="18cd6-107">Этот шаблон можно выразить с помощью циклов итерации и `for`.</span><span class="sxs-lookup"><span data-stu-id="18cd6-107">We can express this pattern by using iteration and `for` loops:</span></span>

```qsharp
for (idxQubit in 0..nQubits - 2) {
    CNOT(register[idxQubit], register[idxQubit + 1]);
}
```

<span data-ttu-id="18cd6-108">Однако в терминах <xref:microsoft.quantum.canon.applytoeachca> и функций работы с массивами, таких как <xref:microsoft.quantum.arrays.zip>, это гораздо короче и проще в чтении:</span><span class="sxs-lookup"><span data-stu-id="18cd6-108">Expressed in terms of <xref:microsoft.quantum.canon.applytoeachca> and array manipulation functions such as <xref:microsoft.quantum.arrays.zip>, however, this is much shorter and easier to read:</span></span>

```qsharp
ApplyToEachCA(CNOT, Zip(register[0..nQubits - 2], register[1..nQubits - 1]));
```

<span data-ttu-id="18cd6-109">В оставшейся части этого раздела мы предоставили несколько примеров того, как использовать различные операции и функции управления потоком, предоставляемые процедурой Canon для сжатия тактовых программ.</span><span class="sxs-lookup"><span data-stu-id="18cd6-109">In the rest of this section, we will provide a number of examples of how to use the various flow control operations and functions provided by the canon to compactly express quantum programs.</span></span>

## <a name="applying-operations-and-functions-over-arrays-and-ranges"></a><span data-ttu-id="18cd6-110">Применение операций и функций к массивам и диапазонам</span><span class="sxs-lookup"><span data-stu-id="18cd6-110">Applying Operations and Functions over Arrays and Ranges</span></span> ##

<span data-ttu-id="18cd6-111">Одной из основных абстракций, предоставляемых Canon, является итерация.</span><span class="sxs-lookup"><span data-stu-id="18cd6-111">One of the primary abstractions provided by the canon is that of iteration.</span></span>
<span data-ttu-id="18cd6-112">Например, рассмотрим единую форму $U \отимес U \отимес \кдотс \отимес U $ для однокубит единого $U $.</span><span class="sxs-lookup"><span data-stu-id="18cd6-112">For instance, consider a unitary of the form $U \otimes U \otimes \cdots \otimes U$ for a single-qubit unitary $U$.</span></span>
<span data-ttu-id="18cd6-113">В Q # можно использовать <xref:microsoft.quantum.arrays.indexrange>, чтобы представить это как `for` цикл по регистру:</span><span class="sxs-lookup"><span data-stu-id="18cd6-113">In Q#, we might use <xref:microsoft.quantum.arrays.indexrange> to represent this as as a `for` loop over a register:</span></span>

```qsharp
/// # Summary
/// Applies $H$ to all qubits in a register.
operation HAll(register : Qubit[]) : Unit 
is Adj + Ctl {

    for (qubit in register) {
        H(qubit);
    }
}
```

<span data-ttu-id="18cd6-114">Затем эту новую операцию можно использовать в качестве `HAll(register)` для применения $H \отимес H \кдотс \отимес H $.</span><span class="sxs-lookup"><span data-stu-id="18cd6-114">We can then use this new operation as `HAll(register)` to apply $H \otimes H \otimes \cdots \otimes H$.</span></span>

<span data-ttu-id="18cd6-115">Однако это довольно сложно, особенно в более крупном алгоритме.</span><span class="sxs-lookup"><span data-stu-id="18cd6-115">This is cumbersome to do, however, especially in a larger algorithm.</span></span>
<span data-ttu-id="18cd6-116">Более того, этот подход специализируется на конкретной операции, которую мы хотим применить к каждому кубит.</span><span class="sxs-lookup"><span data-stu-id="18cd6-116">Moreover, this approach is specialized to the particular operation that we wish to apply to each qubit.</span></span>
<span data-ttu-id="18cd6-117">Мы можем использовать тот факт, что операции являются первым классом для более четкого выражения этой концепции алгоритма:</span><span class="sxs-lookup"><span data-stu-id="18cd6-117">We can use the fact that operations are first-class to express this algorithmic concept more explicitly:</span></span>

```qsharp
ApplyToEachCA(H, register);
```

<span data-ttu-id="18cd6-118">В этом случае суффикс `CA` указывает, что вызов `ApplyToEach` сам является аджоинтабле и управляемым.</span><span class="sxs-lookup"><span data-stu-id="18cd6-118">Here, the suffix `CA` indicates that the call to `ApplyToEach` is itself adjointable and controllable.</span></span>
<span data-ttu-id="18cd6-119">Таким образом, если `U` поддерживает `Adjoint` и `Controlled`, следующие строки эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="18cd6-119">Thus, if `U` supports `Adjoint` and `Controlled`, the following lines are equivalent:</span></span>

```qsharp
Adjoint ApplyToEachCA(U, register);
ApplyToEachCA(Adjoint U, register);
```

<span data-ttu-id="18cd6-120">В частности, это означает, что вызовы `ApplyToEachCA` могут присутствовать в операциях, для которых происходит автоматическое создание примыкающей специализации.</span><span class="sxs-lookup"><span data-stu-id="18cd6-120">In particular, this means that calls to `ApplyToEachCA` can appear in operations for which an adjoint specialization is auto-generated.</span></span>
<span data-ttu-id="18cd6-121">Аналогичным образом <xref:microsoft.quantum.canon.applytoeachindex> удобно использовать для представления шаблонов формы `U(0, targets[0]); U(1, targets[1]); ...`и предоставляет версии для каждого сочетания операторов, поддерживаемого его входными данными.</span><span class="sxs-lookup"><span data-stu-id="18cd6-121">Similarly, <xref:microsoft.quantum.canon.applytoeachindex> is useful for representing patterns of the form `U(0, targets[0]); U(1, targets[1]); ...`, and offers versions for each combination of functors supported by its input.</span></span>

> [!TIP]
> <span data-ttu-id="18cd6-122">`ApplyToEach` является параметризованным, так что его можно использовать с операциями, принимающими входные данные, отличные от `Qubit`.</span><span class="sxs-lookup"><span data-stu-id="18cd6-122">`ApplyToEach` is type-parameterized such that it can be used with operations that take inputs other than `Qubit`.</span></span>
> <span data-ttu-id="18cd6-123">Например, предположим, что `codeBlocks` является массивом <xref:microsoft.quantum.errorcorrection.logicalregister> значений, которые необходимо восстановить.</span><span class="sxs-lookup"><span data-stu-id="18cd6-123">For example, suppose that `codeBlocks` is an array of <xref:microsoft.quantum.errorcorrection.logicalregister> values that need to be recovered.</span></span>
> <span data-ttu-id="18cd6-124">Затем `ApplyToEach(Recover(code, recoveryFn, _), codeBlocks)` применит код исправления ошибок `code` и функции восстановления `recoveryFn` в каждом блоке отдельно.</span><span class="sxs-lookup"><span data-stu-id="18cd6-124">Then `ApplyToEach(Recover(code, recoveryFn, _), codeBlocks)` will apply the error-correcting code `code` and recovery function `recoveryFn` to each block independently.</span></span>
> <span data-ttu-id="18cd6-125">Это справедливо даже для классических входных данных: `ApplyToEach(R(_, _, qubit), [(PauliX, PI() / 2.0); (PauliY(), PI() / 3.0]))` применит поворот на $ \пи/$2 о $X $, за которым следует поворот $pi/$3 о $Y $.</span><span class="sxs-lookup"><span data-stu-id="18cd6-125">This holds even for classical inputs: `ApplyToEach(R(_, _, qubit), [(PauliX, PI() / 2.0); (PauliY(), PI() / 3.0]))` will apply a rotation of $\pi / 2$ about $X$ followed by a rotation of $pi / 3$ about $Y$.</span></span>

<span data-ttu-id="18cd6-126">В Q # Canon также предусмотрена поддержка классических схем перечисления, знакомых с функциональным программированием.</span><span class="sxs-lookup"><span data-stu-id="18cd6-126">The Q# canon also provides support for classical enumeration patterns familiar to functional programming.</span></span>
<span data-ttu-id="18cd6-127">Например, <xref:microsoft.quantum.arrays.fold> реализует шаблон $f (f (s\_{\текст{инитиал}}, x\_0), x\_1), \дотс) $ для сокращения функции по списку.</span><span class="sxs-lookup"><span data-stu-id="18cd6-127">For instance, <xref:microsoft.quantum.arrays.fold> implements the pattern $f(f(f(s\_{\text{initial}}, x\_0), x\_1), \dots)$ for reducing a function over a list.</span></span>
<span data-ttu-id="18cd6-128">Этот шаблон можно использовать для реализации сумм, продуктов, прыжка, прыжка и других таких функций:</span><span class="sxs-lookup"><span data-stu-id="18cd6-128">This pattern can be used to implement sums, products, minima, maxima and other such functions:</span></span>

```qsharp
open Microsoft.Quantum.Arrays;
function Plus(a : Int, b : Int) : Int { return a + b; }
function Sum(xs : Int[]) {
    return Fold(Sum, 0, xs);
}
```

<span data-ttu-id="18cd6-129">Аналогично, такие функции, как <xref:microsoft.quantum.arrays.mapped> и <xref:microsoft.quantum.arrays.mappedbyindex>, можно использовать для выражения концепций функционального программирования в Q #.</span><span class="sxs-lookup"><span data-stu-id="18cd6-129">Similarly, functions like <xref:microsoft.quantum.arrays.mapped> and <xref:microsoft.quantum.arrays.mappedbyindex> can be used to express functional programming concepts in Q#.</span></span>

## <a name="composing-operations-and-functions"></a><span data-ttu-id="18cd6-130">Составление операций и функций</span><span class="sxs-lookup"><span data-stu-id="18cd6-130">Composing Operations and Functions</span></span> ##

<span data-ttu-id="18cd6-131">Конструкции потока управления, предлагаемые процедурой Canon, принимают операции и функции в качестве их входных данных, поэтому полезно иметь возможность объединить несколько операций или функций в один вызываемый.</span><span class="sxs-lookup"><span data-stu-id="18cd6-131">The control flow constructs offered by the canon take operations and functions as their inputs, such that it is helpful to be able to compose several operations or functions into a single callable.</span></span>
<span data-ttu-id="18cd6-132">Например, шаблон $UVU ^ {\дагжер} $ является чрезвычайно распространенным при программировании на такте, так что Canon предоставляет операцию <xref:microsoft.quantum.canon.applywith> в качестве абстракции для этого шаблона.</span><span class="sxs-lookup"><span data-stu-id="18cd6-132">For instance, the pattern $UVU^{\dagger}$ is extremely common in quantum programming, such that the canon provides the operation <xref:microsoft.quantum.canon.applywith> as an abstraction for this pattern.</span></span>
<span data-ttu-id="18cd6-133">Эта абстракция также позволяет более эффективно выполнять обработку в цепи, так как `Controlled`, действуя в `U(qubit); V(qubit); Adjoint U(qubit);` последовательности, не требуется действовать на каждом `U`.</span><span class="sxs-lookup"><span data-stu-id="18cd6-133">This abstraction also allows for more efficient compliation into circuits, as `Controlled` acting on the sequence `U(qubit); V(qubit); Adjoint U(qubit);` does not need to act on each `U`.</span></span>
<span data-ttu-id="18cd6-134">Чтобы увидеть это, позвольте $c (U) $ быть единым, представляющим `Controlled U([control], target)`, и позвольте $c (V) $ быть определено таким же образом.</span><span class="sxs-lookup"><span data-stu-id="18cd6-134">To see this, let $c(U)$ be the unitary representing `Controlled U([control], target)` and let $c(V)$ be defined in the same way.</span></span>
<span data-ttu-id="18cd6-135">Затем для произвольного состояния $ \кет{\пси} $, \бегин{алигн} c (U) c (V) c (U) ^ \дагжер \кет{1} \отимес \кет{\пси} & = \кет{1} \отимес (УВУ ^ {\дагжер} \кет{\пси}) \\\\ & = (\boldone \otimes u) (c (V)) (\boldone \otimes U ^ \dagger) \ Сисакет{1} \отимес \кет{\пси}.</span><span class="sxs-lookup"><span data-stu-id="18cd6-135">Then for an arbitrary state $\ket{\psi}$, \begin{align} c(U) c(V) c(U)^\dagger \ket{1} \otimes \ket{\psi} & = \ket{1} \otimes (UVU^{\dagger} \ket{\psi}) \\\\ & = (\boldone \otimes U) (c(V)) (\boldone \otimes U^\dagger) \ket{1} \otimes \ket{\psi}.</span></span>
<span data-ttu-id="18cd6-136">\енд{алигн} по определению `Controlled`.</span><span class="sxs-lookup"><span data-stu-id="18cd6-136">\end{align} by the definition of `Controlled`.</span></span>
<span data-ttu-id="18cd6-137">С другой стороны, \бегин{алигн} c (U) c (V) c (U) ^ \дагжер \кет{0} \отимес \кет{\пси} & = \кет{0} \отимес \кет{\пси} \\\\ & = \кет{0} \отимес (УУ ^ \dagger \ket{\psi}) \\\\ & = (\boldone \otimes U) (c ( V)) (\болдоне \отимес U ^ \дагжер) \кет{0} \отимес \кет{\пси}.</span><span class="sxs-lookup"><span data-stu-id="18cd6-137">On the other hand, \begin{align} c(U) c(V) c(U)^\dagger \ket{0} \otimes \ket{\psi} & = \ket{0} \otimes \ket{\psi} \\\\ & = \ket{0} \otimes (UU^\dagger \ket{\psi}) \\\\ & = (\boldone \otimes U) (c(V)) (\boldone \otimes U^\dagger) \ket{0} \otimes \ket{\psi}.</span></span>
<span data-ttu-id="18cd6-138">\енд{алигн} по линейной шкале, мы можем заключить, что мы можем $U $ out таким образом для всех состояний входных данных.</span><span class="sxs-lookup"><span data-stu-id="18cd6-138">\end{align} By linearity, we can conclude that we can factor $U$ out in this way for all input states.</span></span>
<span data-ttu-id="18cd6-139">То есть $c (УВУ ^ \дагжер) = U c (V) U ^ \дагжер $.</span><span class="sxs-lookup"><span data-stu-id="18cd6-139">That is, $c(UVU^\dagger) = U c(V) U^\dagger$.</span></span>
<span data-ttu-id="18cd6-140">Так как управление операциями может быть дорогостоящей в целом, использование контролируемых вариантов, таких как `WithC` и `WithCA`, может помочь уменьшить число операторов элементов управления, которые необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="18cd6-140">Since controlling operations can be expensive in general, using controlled variants such as `WithC` and `WithCA` can help reduce the number of control functors that need to be applied.</span></span>

> [!NOTE]
> <span data-ttu-id="18cd6-141">Еще одним следствием того, $U $, является то, что нам не нужно знать, как применить `Controlled` функтор к `U`.</span><span class="sxs-lookup"><span data-stu-id="18cd6-141">One other consequence of factoring out $U$ is that we need not even know how to apply the `Controlled` functor to `U`.</span></span>
> <span data-ttu-id="18cd6-142">`ApplyWithCA`, таким образом, имеет более слабую сигнатуру, чем может быть ожидаемо:</span><span class="sxs-lookup"><span data-stu-id="18cd6-142">`ApplyWithCA` therefore has a weaker signature than might be expected:</span></span>
> ```qsharp
> ApplyWithCA<'T> : (('T => Unit is Adj),
>     ('T => Unit is Adj + Ctl), 'T) => Unit
> ```

<span data-ttu-id="18cd6-143">Аналогичным образом <xref:microsoft.quantum.canon.bind> создает операции, которые в свою очередь применяют последовательность других операций.</span><span class="sxs-lookup"><span data-stu-id="18cd6-143">Similarly, <xref:microsoft.quantum.canon.bind> produces operations which apply a sequence of other operations in turn.</span></span>
<span data-ttu-id="18cd6-144">Например, следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="18cd6-144">For instance, the following are equivalent:</span></span>

```qsharp
H(qubit); X(qubit);
Bind([H, X], qubit);
```

<span data-ttu-id="18cd6-145">Сочетание с шаблонами итерации может сделать это особенно полезно:</span><span class="sxs-lookup"><span data-stu-id="18cd6-145">Combining with iteration patterns can make this especially useful:</span></span>

```qsharp
// Bracket the quantum Fourier transform with $XH$ on each qubit.
ApplyWith(ApplyToEach(Bind([H, X]), _), QFT, _);
```

### <a name="time-ordered-composition"></a><span data-ttu-id="18cd6-146">Компоновка с сортировкой по времени</span><span class="sxs-lookup"><span data-stu-id="18cd6-146">Time-Ordered Composition</span></span> ###

<span data-ttu-id="18cd6-147">Мы можем еще дальше придумать управление потоком в терминах частичного приложения и классических функций, а также моделировать даже довольно сложные тактовые концепции с точки зрения классического управления потоком.</span><span class="sxs-lookup"><span data-stu-id="18cd6-147">We can go still further by thinking of flow control in terms of partial application and classical functions, and can model even fairly sophisticated quantum concepts in terms of classical flow control.</span></span>
<span data-ttu-id="18cd6-148">Эта аналогия выполняется точно в соответствии с определением того, что единые операторы точно соответствуют побочным эффектам вызывающих операций, так что любая декомпозиция отдельных операторов с точки зрения других операторов соответствует созданию определенного вызов последовательности для классических подпрограмм, которые выдают инструкции для выполнения в качестве отдельных операторов.</span><span class="sxs-lookup"><span data-stu-id="18cd6-148">This analogy is made precise by the recognition that unitary operators correspond exactly to the side effects of calling operations, such that any decomposition of unitary operators in terms of other unitary operators corresponds to constructing a particular calling sequence for classical subroutines which emit instructions to act as particular unitary operators.</span></span>
<span data-ttu-id="18cd6-149">В этом представлении `Bind` является точным представлением матричного произведения, поскольку `Bind([A, B])(target)` эквивалентна `A(target); B(target);`, которая, в свою очередь, является вызывающей последовательностью, соответствующей $BA $.</span><span class="sxs-lookup"><span data-stu-id="18cd6-149">Under this view, `Bind` is precisely the representation of the matrix product, since `Bind([A, B])(target)` is equivalent to `A(target); B(target);`, which in turn is the calling sequence corresponding to $BA$.</span></span>

<span data-ttu-id="18cd6-150">Более сложным примером является [расширение Троттер – Сузуки](https://arxiv.org/abs/math-ph/0506007v1).</span><span class="sxs-lookup"><span data-stu-id="18cd6-150">A more sophisticated example is the [Trotter–Suzuki expansion](https://arxiv.org/abs/math-ph/0506007v1).</span></span>
<span data-ttu-id="18cd6-151">Как обсуждалось в разделе представление динамического генератора [структур данных](xref:microsoft.quantum.libraries.data-structures), расширение Троттер – Сузуки предоставляет особенно полезный способ выражения экспоненциальных Экспонент.</span><span class="sxs-lookup"><span data-stu-id="18cd6-151">As discussed in the Dynamical Generator Representation section of [data structures](xref:microsoft.quantum.libraries.data-structures), the Trotter–Suzuki expansion provides a particularly useful way of expressing matrix exponentials.</span></span>
<span data-ttu-id="18cd6-152">Например, применение расширения в самом низком порядке дает, что для любых операторов $A $ и $B $ таким образом, $A = A ^ \дагжер $ and $B = B ^ \дагжер $, \бегин{алигн} \таг{★} \лабел{ЕК: Троттер-Сузуки-0} \експ (я [A + B] t) = \lim_{n\to\infty} \лефт (\експ (я A т/д) \експ (i B t/n ) \ригхт) ^ n.</span><span class="sxs-lookup"><span data-stu-id="18cd6-152">For instance, applying the expansion at its lowest order yields that for any operators $A$ and $B$ such that $A = A^\dagger$ and $B = B^\dagger$, \begin{align} \tag{★} \label{eq:trotter-suzuki-0} \exp(i [A + B] t) = \lim_{n\to\infty} \left(\exp(i A t / n) \exp(i B t / n)\right)^n.</span></span>
<span data-ttu-id="18cd6-153">\енд{алигн} разговорной речи, это говорит о том, что мы можем приблизительно развивать состояние в $A + B $B $A $.</span><span class="sxs-lookup"><span data-stu-id="18cd6-153">\end{align} Colloquially, this says that we can approximately evolve a state under $A + B$ by alternately evolving under $A$ and $B$ alone.</span></span>
<span data-ttu-id="18cd6-154">Если мы представляем развитие в рамках $A $ с помощью операции `A : (Double, Qubit[]) => Unit`, которая применяет $e ^ {i t} $, то представление расширения Троттер – Сузуки в плане переупорядочения последовательностей вызовов станет ясным.</span><span class="sxs-lookup"><span data-stu-id="18cd6-154">If we represent evolution under $A$ by an operation `A : (Double, Qubit[]) => Unit` that applies $e^{i t A}$, then the representation of the Trotter–Suzuki expansion in terms of rearranging calling sequences becomes clear.</span></span>
<span data-ttu-id="18cd6-155">Конкретнее, при наличии операции, `U : ((Int, Double, Qubit[]) => Unit is Adj + Ctl` такой `A = U(0, _, _)` и `B = U(1, _, _)`, мы можем определить новую операцию, представляющую целую часть `U` $t $ путем создания последовательностей формы.</span><span class="sxs-lookup"><span data-stu-id="18cd6-155">Concretely, given an operation `U : ((Int, Double, Qubit[]) => Unit is Adj + Ctl` such that `A = U(0, _, _)` and `B = U(1, _, _)`, we can define a new operation representing the integral of `U` at time $t$ by generating sequences of the form</span></span>

```qsharp
U(0, time / Float(nSteps), target);
U(1, time / Float(nSteps), target);
U(0, time / Float(nSteps), target);
U(1, time / Float(nSteps), target);
// ...
```

<span data-ttu-id="18cd6-156">На этом этапе мы теперь можем потроттер о расширении Сузуки *без ссылки на механизм тактов*.</span><span class="sxs-lookup"><span data-stu-id="18cd6-156">At this point, we can now reason about the Trotter–Suzuki expansion *without reference to quantum mechanics at all*.</span></span>
<span data-ttu-id="18cd6-157">Развертывание фактически представляет собой очень конкретный шаблон итерации, на который послужила $ \екреф{ЕК: Троттер-Сузуки-0} $.</span><span class="sxs-lookup"><span data-stu-id="18cd6-157">The expansion is effectively a very particular iteration pattern motivated by $\eqref{eq:trotter-suzuki-0}$.</span></span>
<span data-ttu-id="18cd6-158">Этот шаблон итерации реализуется <xref:microsoft.quantum.canon.decomposeintotimestepsca>:</span><span class="sxs-lookup"><span data-stu-id="18cd6-158">This iteration pattern is implemented by <xref:microsoft.quantum.canon.decomposeintotimestepsca>:</span></span>

```qsharp
// The 2 indicates how many terms we need to decompose,
// while the 1 indicates that we are using the
// first-order Trotter–Suzuki decomposoition.
DecomposeIntoTimeStepsCA((2, U), 1);
```

<span data-ttu-id="18cd6-159">Сигнатура `DecomposeIntoTimeStepsCA` соответствует общему шаблону в Q #, где коллекции, которые могут быть включены в массивы, или что-то, какие элементы вычислений в режиме реального времени представлены кортежами, первыми элементами которых являются `Int` значения длины.</span><span class="sxs-lookup"><span data-stu-id="18cd6-159">The signature of `DecomposeIntoTimeStepsCA` follows a common pattern in Q#, where collections that may be backed either by arrays or by something which compute elements on the fly are represented by tuples whose first elements are `Int` values indicating their lengths.</span></span>

## <a name="putting-it-together-controlling-operations"></a><span data-ttu-id="18cd6-160">Совместное размещение: управление операциями</span><span class="sxs-lookup"><span data-stu-id="18cd6-160">Putting it Together: Controlling Operations</span></span> ##

<span data-ttu-id="18cd6-161">Наконец, Canon строится на `Controlled` функтор, предоставляя дополнительные способы выполнения условных операций в такте.</span><span class="sxs-lookup"><span data-stu-id="18cd6-161">Finally, the canon builds on the `Controlled` functor by providing additional ways to condition quantum operations.</span></span>
<span data-ttu-id="18cd6-162">Обычно, особенно в тактовой арифметике, к условным операциям на основе состояний вычислительных операций, отличных от $ \ket{0\cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="18cd6-162">It is common, especially in quantum arithmetic, to condition operations on computational basis states other than $\ket{0\cdots 0}$.</span></span>
<span data-ttu-id="18cd6-163">Используя операции управления и функции, представленные выше, можно использовать более общие тактовые условия в одной инструкции.</span><span class="sxs-lookup"><span data-stu-id="18cd6-163">Using the control operations and functions introduced above, we can more general quantum conditions in a single statement.</span></span>
<span data-ttu-id="18cd6-164">Давайте перейдем к тому, как <xref:microsoft.quantum.canon.controlledonbitstring> делает это (параметры типа San), а затем разбивает их на одну.</span><span class="sxs-lookup"><span data-stu-id="18cd6-164">Let's jump in to how <xref:microsoft.quantum.canon.controlledonbitstring> does it (sans type parameters), then we'll break down the pieces one by one.</span></span>
<span data-ttu-id="18cd6-165">Первое, что нужно сделать, — это определить операцию, которая фактически выполняет тяжелую работу по реализации элемента управления на случайном уровне вычислительных операций.</span><span class="sxs-lookup"><span data-stu-id="18cd6-165">The first thing we'll need to do is to define an operation which actually does the heavy lifting of implementing the control on arbitrary computational basis states.</span></span>
<span data-ttu-id="18cd6-166">Однако мы не будем вызывать эту операцию напрямую, поэтому мы добавляем `_` к началу имени, чтобы указать, что это реализация другой конструкции в другом расположении.</span><span class="sxs-lookup"><span data-stu-id="18cd6-166">We won't call this operation directly, however, and so we add `_` to the beginning of the name to indicate that it's an implementation of another construct elsewhere.</span></span>

```qsharp
operation _ControlledOnBitString(
        bits : Bool[],
        oracle: (Qubit[] => Unit is Adj + Ctl),
        controlRegister : Qubit[],
        targetRegister: Qubit[]) 
: Unit 
is Adj + Ctl {
```

<span data-ttu-id="18cd6-167">Обратите внимание, что мы принимаем строку битов, представленную в виде массива `Bool`, который мы используем для указания условия, которое нужно применить к операции `oracle`, которую мы присваиваем.</span><span class="sxs-lookup"><span data-stu-id="18cd6-167">Note that we take a string of bits, represented as a `Bool` array, that we use to specify the conditioning that we want to apply to the operation `oracle` that we are given.</span></span>
<span data-ttu-id="18cd6-168">Так как эта операция фактически выполняет приложение напрямую, нам также нужно взять контрольные и целевые регистры, представленные здесь как `Qubit[]`.</span><span class="sxs-lookup"><span data-stu-id="18cd6-168">Since this operation actually does the application directly, we also need to take the control and target registers, both represented here as `Qubit[]`.</span></span>

<span data-ttu-id="18cd6-169">Далее обратите внимание, что Управление состоянием вычислительного основания $ \кет{\век{с}} = \кет{с\_0 s\_1 \дотс s\_{n-1}} $ для разрядной строки $ \век{с} $ может быть реализовано путем преобразования $ \кет{\век{с}} $ в $ \ket{0\cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="18cd6-169">Next, we note that controlling on the computational basis state $\ket{\vec{s}} = \ket{s\_0 s\_1 \dots s\_{n - 1}}$ for a bit string $\vec{s}$ can be realized by transforming $\ket{\vec{s}}$ into $\ket{0\cdots 0}$.</span></span>
<span data-ttu-id="18cd6-170">В частности, $ \кет{\век{с}} = X ^ {s\_0} \отимес X ^ {s\_1} \отимес \кдотс \отимес X ^ {s\_{n-1}} \ket{0\cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="18cd6-170">In particular, $\ket{\vec{s}} = X^{s\_0} \otimes X^{s\_1} \otimes \cdots \otimes X^{s\_{n - 1}} \ket{0\cdots 0}$.</span></span>
<span data-ttu-id="18cd6-171">Начиная с $X ^ {\дагжер} = X $, это означает, что $ \ket{0\dots 0} = X ^ {s\_0} \отимес X ^ {s\_1} \отимес \кдотс \отимес X ^ {s\_{n-1}} \кет{\век{с}} $.</span><span class="sxs-lookup"><span data-stu-id="18cd6-171">Since $X^{\dagger} = X$, this implies that $\ket{0\dots 0} = X^{s\_0} \otimes X^{s\_1} \otimes \cdots \otimes X^{s\_{n - 1}} \ket{\vec{s}}$.</span></span>
<span data-ttu-id="18cd6-172">Таким образом, можно применить $P = X ^ {s\_0} \отимес X ^ {s\_1} \отимес \кдотс \отимес X ^ {s\_{n-1}} $, Apply `Controlled oracle`и преобразовать обратно в $ \век{с} $.</span><span class="sxs-lookup"><span data-stu-id="18cd6-172">Thus, we can apply $P = X^{s\_0} \otimes X^{s\_1} \otimes \cdots \otimes X^{s\_{n - 1}}$, apply `Controlled oracle`, and transform back to $\vec{s}$.</span></span>
<span data-ttu-id="18cd6-173">Эта конструкция в точности `ApplyWith`, поэтому мы записываем тело нашей новой операции соответствующим образом:</span><span class="sxs-lookup"><span data-stu-id="18cd6-173">This construction is precisely `ApplyWith`, so we write the body of our new operation accordingly:</span></span>

```qsharp
    ApplyWithCA(
        ApplyPauliFromBitString(PauliX, false, bits, _),
        (Controlled oracle)(_, targetRegister),
        controlRegister
    );
}
```

<span data-ttu-id="18cd6-174">Здесь мы использовали <xref:microsoft.quantum.canon.applypaulifrombitstring> для применения $P $, частичного применения к его цели для использования с `ApplyWith`.</span><span class="sxs-lookup"><span data-stu-id="18cd6-174">Here, we have used <xref:microsoft.quantum.canon.applypaulifrombitstring> to apply $P$, partially applying over its target for use with `ApplyWith`.</span></span>
<span data-ttu-id="18cd6-175">Однако обратите внимание, что нам нужно преобразовать *контрольную* регистрацию в нашу требуемую форму, поэтому мы частично применяли внутреннюю операцию `(Controlled oracle)` на *целевом объекте*.</span><span class="sxs-lookup"><span data-stu-id="18cd6-175">Note, however, that we need to transform the *control* register to our desired form, so we partially apply the inner operation `(Controlled oracle)` on the *target*.</span></span>
<span data-ttu-id="18cd6-176">Это оставляет `ApplyWith`, действуя в скобки с $P $ точно так же, как и нужно.</span><span class="sxs-lookup"><span data-stu-id="18cd6-176">This leaves `ApplyWith` acting to bracket the control register with $P$, exactly as we desired.</span></span>

<span data-ttu-id="18cd6-177">На этом этапе можно было бы сделать, но это не противоречит тем, что наша новая операция не имеет такого поведения, как применение `Controlled` функтор.</span><span class="sxs-lookup"><span data-stu-id="18cd6-177">At this point, we could be done, but it is somehow unsatisfying that our new operation does not "feel" like applying the `Controlled` functor.</span></span>
<span data-ttu-id="18cd6-178">Поэтому мы завершаем определение нашей новой концепции потока управления путем написания функции, которая принимает Управление Oracle и возвращает новую операцию.</span><span class="sxs-lookup"><span data-stu-id="18cd6-178">Thus, we finish defining our new control flow concept by writing a function that takes the oracle to be controlled and that returns a new operation.</span></span>
<span data-ttu-id="18cd6-179">В этом случае наша новая функция выглядит и работает так же, как `Controlled`, что позволяет легко определять мощные новые конструкции потока управления с помощью Q # и Canon вместе:</span><span class="sxs-lookup"><span data-stu-id="18cd6-179">In this way, our new function looks and feels very much like `Controlled`, illustrating that we can easily define powerful new control flow constructs using Q# and the canon together:</span></span>

```qsharp
function ControlledOnBitString(
        bits : Bool[],
        oracle: (Qubit[] => Unit is Adj + Ctl)) 
: ((Qubit[], Qubit[]) => Unit is Adj + Ctl) {
    return _ControlledOnBitString(bits, oracle, _, _);
}
```
