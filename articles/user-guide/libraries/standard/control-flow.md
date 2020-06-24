---
title: 'Элементы управления потоком в Q # Standard либарариес'
description: 'Сведения об операциях и функциях управления потоком в стандартной библиотеке Microsoft Q #.'
author: QuantumWriter
uid: microsoft.quantum.concepts.control-flow
ms.author: martinro@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: b41b3edd7a3e3ac13dbda106a869f4cba8183600
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275756"
---
# <a name="higher-order-control-flow"></a><span data-ttu-id="3b4db-103">Поток управления высшего порядка</span><span class="sxs-lookup"><span data-stu-id="3b4db-103">Higher-Order Control Flow</span></span> #

<span data-ttu-id="3b4db-104">Одна из основных ролей стандартной библиотеки заключается в том, чтобы упростить выражать алгоритмы, основанные на высоком уровне, в качестве [тактовых программ](https://en.wikipedia.org/wiki/Quantum_programming).</span><span class="sxs-lookup"><span data-stu-id="3b4db-104">One of the primary roles of the standard library is to make it easier to express high-level algorithmic ideas as [quantum programs](https://en.wikipedia.org/wiki/Quantum_programming).</span></span>
<span data-ttu-id="3b4db-105">Таким же, Q # Canon предоставляет множество различных конструкций управления потоком, каждый из которых реализуется с помощью частичного применения функций и операций.</span><span class="sxs-lookup"><span data-stu-id="3b4db-105">Thus, the Q# canon provides a variety of different flow control constructs, each implemented using partial application of functions and operations.</span></span>
<span data-ttu-id="3b4db-106">В качестве примера рассмотрим случай, когда один из них хочет создать «КНОТную лестницу» для регистра:</span><span class="sxs-lookup"><span data-stu-id="3b4db-106">Jumping immediately into an example, consider the case in which one wants to construct a "CNOT ladder" on a register:</span></span>

```qsharp
let nQubits = Length(register);
CNOT(register[0], register[1]);
CNOT(register[1], register[2]);
// ...
CNOT(register[nQubits - 2], register[nQubits - 1]);
```

<span data-ttu-id="3b4db-107">Этот шаблон можно выразить с помощью итераций и `for` циклов:</span><span class="sxs-lookup"><span data-stu-id="3b4db-107">We can express this pattern by using iteration and `for` loops:</span></span>

```qsharp
for (idxQubit in 0..nQubits - 2) {
    CNOT(register[idxQubit], register[idxQubit + 1]);
}
```

<span data-ttu-id="3b4db-108">Но в терминах <xref:microsoft.quantum.canon.applytoeachca> функций и операций с массивами <xref:microsoft.quantum.arrays.zip> , таких как, это гораздо короче и проще в чтении:</span><span class="sxs-lookup"><span data-stu-id="3b4db-108">Expressed in terms of <xref:microsoft.quantum.canon.applytoeachca> and array manipulation functions such as <xref:microsoft.quantum.arrays.zip>, however, this is much shorter and easier to read:</span></span>

```qsharp
ApplyToEachCA(CNOT, Zip(register[0..nQubits - 2], register[1..nQubits - 1]));
```

<span data-ttu-id="3b4db-109">В оставшейся части этого раздела мы предоставили несколько примеров того, как использовать различные операции и функции управления потоком, предоставляемые процедурой Canon для сжатия тактовых программ.</span><span class="sxs-lookup"><span data-stu-id="3b4db-109">In the rest of this section, we will provide a number of examples of how to use the various flow control operations and functions provided by the canon to compactly express quantum programs.</span></span>

## <a name="applying-operations-and-functions-over-arrays-and-ranges"></a><span data-ttu-id="3b4db-110">Применение операций и функций к массивам и диапазонам</span><span class="sxs-lookup"><span data-stu-id="3b4db-110">Applying Operations and Functions over Arrays and Ranges</span></span> ##

<span data-ttu-id="3b4db-111">Одной из основных абстракций, предоставляемых Canon, является итерация.</span><span class="sxs-lookup"><span data-stu-id="3b4db-111">One of the primary abstractions provided by the canon is that of iteration.</span></span>
<span data-ttu-id="3b4db-112">Например, рассмотрим единую форму $U \отимес U \отимес \кдотс \отимес U $ для однокубит единого $U $.</span><span class="sxs-lookup"><span data-stu-id="3b4db-112">For instance, consider a unitary of the form $U \otimes U \otimes \cdots \otimes U$ for a single-qubit unitary $U$.</span></span>
<span data-ttu-id="3b4db-113">В Q # мы можем использовать <xref:microsoft.quantum.arrays.indexrange> , чтобы представить это как `for` цикл по регистру:</span><span class="sxs-lookup"><span data-stu-id="3b4db-113">In Q#, we might use <xref:microsoft.quantum.arrays.indexrange> to represent this as as a `for` loop over a register:</span></span>

```qsharp
/// # Summary
/// Applies $H$ to all qubits in a register.
operation ApplyHadamardToAll(
    register : Qubit[])
: Unit is Adj + Ctl {
    for (qubit in register) {
        H(qubit);
    }
}
```

<span data-ttu-id="3b4db-114">Затем эту новую операцию можно использовать как `HAll(register)` для применения $H \Отимес H \отимес \кдотс \Отимес H $.</span><span class="sxs-lookup"><span data-stu-id="3b4db-114">We can then use this new operation as `HAll(register)` to apply $H \otimes H \otimes \cdots \otimes H$.</span></span>

<span data-ttu-id="3b4db-115">Однако это довольно сложно, особенно в более крупном алгоритме.</span><span class="sxs-lookup"><span data-stu-id="3b4db-115">This is cumbersome to do, however, especially in a larger algorithm.</span></span>
<span data-ttu-id="3b4db-116">Более того, этот подход специализируется на конкретной операции, которую мы хотим применить к каждому кубит.</span><span class="sxs-lookup"><span data-stu-id="3b4db-116">Moreover, this approach is specialized to the particular operation that we wish to apply to each qubit.</span></span>
<span data-ttu-id="3b4db-117">Мы можем использовать тот факт, что операции являются первым классом для более четкого выражения этой концепции алгоритма:</span><span class="sxs-lookup"><span data-stu-id="3b4db-117">We can use the fact that operations are first-class to express this algorithmic concept more explicitly:</span></span>

```qsharp
ApplyToEachCA(H, register);
```

<span data-ttu-id="3b4db-118">В этом случае суффикс `CA` указывает, что вызов `ApplyToEach` сам является аджоинтабле и управляемым.</span><span class="sxs-lookup"><span data-stu-id="3b4db-118">Here, the suffix `CA` indicates that the call to `ApplyToEach` is itself adjointable and controllable.</span></span>
<span data-ttu-id="3b4db-119">Таким образом, если `U` поддерживает `Adjoint` и `Controlled` , следующие строки эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="3b4db-119">Thus, if `U` supports `Adjoint` and `Controlled`, the following lines are equivalent:</span></span>

```qsharp
Adjoint ApplyToEachCA(U, register);
ApplyToEachCA(Adjoint U, register);
```

<span data-ttu-id="3b4db-120">В частности, это означает, что вызовы `ApplyToEachCA` могут появляться в операциях, для которых происходит автоматическое создание примыкающей специализации.</span><span class="sxs-lookup"><span data-stu-id="3b4db-120">In particular, this means that calls to `ApplyToEachCA` can appear in operations for which an adjoint specialization is auto-generated.</span></span>
<span data-ttu-id="3b4db-121">Аналогично, <xref:microsoft.quantum.canon.applytoeachindex> полезно для представления шаблонов формы `U(0, targets[0]); U(1, targets[1]); ...` и предоставляет версии для каждого сочетания операторов, поддерживаемого его входными данными.</span><span class="sxs-lookup"><span data-stu-id="3b4db-121">Similarly, <xref:microsoft.quantum.canon.applytoeachindex> is useful for representing patterns of the form `U(0, targets[0]); U(1, targets[1]); ...`, and offers versions for each combination of functors supported by its input.</span></span>

> [!TIP]
> <span data-ttu-id="3b4db-122">`ApplyToEach`является параметризованным, так что его можно использовать с операциями, принимающими входные данные, отличные от `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="3b4db-122">`ApplyToEach` is type-parameterized such that it can be used with operations that take inputs other than `Qubit`.</span></span>
> <span data-ttu-id="3b4db-123">Например, предположим, что `codeBlocks` является массивом <xref:microsoft.quantum.errorcorrection.logicalregister> значений, которые необходимо восстановить.</span><span class="sxs-lookup"><span data-stu-id="3b4db-123">For example, suppose that `codeBlocks` is an array of <xref:microsoft.quantum.errorcorrection.logicalregister> values that need to be recovered.</span></span>
> <span data-ttu-id="3b4db-124">Затем `ApplyToEach(Recover(code, recoveryFn, _), codeBlocks)` применит код исправления ошибок `code` и функцию восстановления `recoveryFn` к каждому блоку независимо друг от друга.</span><span class="sxs-lookup"><span data-stu-id="3b4db-124">Then `ApplyToEach(Recover(code, recoveryFn, _), codeBlocks)` will apply the error-correcting code `code` and recovery function `recoveryFn` to each block independently.</span></span>
> <span data-ttu-id="3b4db-125">Это справедливо даже для классических входных данных: `ApplyToEach(R(_, _, qubit), [(PauliX, PI() / 2.0); (PauliY(), PI() / 3.0]))` будет применяться вращение $ \пи/$2 о $X $, за которым следует поворот $PI/$3 о $Y $.</span><span class="sxs-lookup"><span data-stu-id="3b4db-125">This holds even for classical inputs: `ApplyToEach(R(_, _, qubit), [(PauliX, PI() / 2.0); (PauliY(), PI() / 3.0]))` will apply a rotation of $\pi / 2$ about $X$ followed by a rotation of $pi / 3$ about $Y$.</span></span>

<span data-ttu-id="3b4db-126">В Q # Canon также предусмотрена поддержка классических схем перечисления, знакомых с функциональным программированием.</span><span class="sxs-lookup"><span data-stu-id="3b4db-126">The Q# canon also provides support for classical enumeration patterns familiar to functional programming.</span></span>
<span data-ttu-id="3b4db-127">Например, <xref:microsoft.quantum.arrays.fold> реализует шаблон $f (f (s \_ {\текст{инитиал}}, x \_ 0), x \_ 1), \дотс) $ для сокращения функции по списку.</span><span class="sxs-lookup"><span data-stu-id="3b4db-127">For instance, <xref:microsoft.quantum.arrays.fold> implements the pattern $f(f(f(s\_{\text{initial}}, x\_0), x\_1), \dots)$ for reducing a function over a list.</span></span>
<span data-ttu-id="3b4db-128">Этот шаблон можно использовать для реализации сумм, продуктов, прыжка, прыжка и других таких функций:</span><span class="sxs-lookup"><span data-stu-id="3b4db-128">This pattern can be used to implement sums, products, minima, maxima and other such functions:</span></span>

```qsharp
open Microsoft.Quantum.Arrays;
function Plus(a : Int, b : Int) : Int { return a + b; }
function Sum(xs : Int[]) {
    return Fold(Sum, 0, xs);
}
```

<span data-ttu-id="3b4db-129">Аналогично, такие функции, как <xref:microsoft.quantum.arrays.mapped> и, <xref:microsoft.quantum.arrays.mappedbyindex> можно использовать для выражения концепций функционального программирования в Q #.</span><span class="sxs-lookup"><span data-stu-id="3b4db-129">Similarly, functions like <xref:microsoft.quantum.arrays.mapped> and <xref:microsoft.quantum.arrays.mappedbyindex> can be used to express functional programming concepts in Q#.</span></span>

## <a name="composing-operations-and-functions"></a><span data-ttu-id="3b4db-130">Составление операций и функций</span><span class="sxs-lookup"><span data-stu-id="3b4db-130">Composing Operations and Functions</span></span> ##

<span data-ttu-id="3b4db-131">Конструкции потока управления, предлагаемые процедурой Canon, принимают операции и функции в качестве их входных данных, поэтому полезно иметь возможность объединить несколько операций или функций в один вызываемый.</span><span class="sxs-lookup"><span data-stu-id="3b4db-131">The control flow constructs offered by the canon take operations and functions as their inputs, such that it is helpful to be able to compose several operations or functions into a single callable.</span></span>
<span data-ttu-id="3b4db-132">Например, шаблон $UVU ^ {\дагжер} $ является чрезвычайно распространенным при программировании на такт, так что Canon предоставляет эту операцию <xref:microsoft.quantum.canon.applywith> как абстракцию для этого шаблона.</span><span class="sxs-lookup"><span data-stu-id="3b4db-132">For instance, the pattern $UVU^{\dagger}$ is extremely common in quantum programming, such that the canon provides the operation <xref:microsoft.quantum.canon.applywith> as an abstraction for this pattern.</span></span>
<span data-ttu-id="3b4db-133">Эта абстракция также позволяет более эффективно выполнять обработку в цепи, так как `Controlled` работа над этой последовательностью `U(qubit); V(qubit); Adjoint U(qubit);` не требуется `U` .</span><span class="sxs-lookup"><span data-stu-id="3b4db-133">This abstraction also allows for more efficient compliation into circuits, as `Controlled` acting on the sequence `U(qubit); V(qubit); Adjoint U(qubit);` does not need to act on each `U`.</span></span>
<span data-ttu-id="3b4db-134">Чтобы увидеть это, дайте $c (U) $ быть единым представлением, `Controlled U([control], target)` а $c (V) $ — таким же образом.</span><span class="sxs-lookup"><span data-stu-id="3b4db-134">To see this, let $c(U)$ be the unitary representing `Controlled U([control], target)` and let $c(V)$ be defined in the same way.</span></span>
<span data-ttu-id="3b4db-135">Затем для произвольного состояния $ \кет{\пси} $, \бегин{алигн} c (U) c (V) c (U) ^ \дагжер \кет {1} \отимес \кет{\пси} & = \кет {1} \ОТИМЕС (УВУ ^ {\дагжер} \кет{\пси}) \\ \\ & = (\boldone \otimes u) (c (V)) (\boldone \otimes u ^ \dagger) \ket {1} \otimes \ket{\psi}.</span><span class="sxs-lookup"><span data-stu-id="3b4db-135">Then for an arbitrary state $\ket{\psi}$, \begin{align} c(U) c(V) c(U)^\dagger \ket{1} \otimes \ket{\psi} & = \ket{1} \otimes (UVU^{\dagger} \ket{\psi}) \\\\ & = (\boldone \otimes U) (c(V)) (\boldone \otimes U^\dagger) \ket{1} \otimes \ket{\psi}.</span></span>
<span data-ttu-id="3b4db-136">\енд{алигн} по определению `Controlled` .</span><span class="sxs-lookup"><span data-stu-id="3b4db-136">\end{align} by the definition of `Controlled`.</span></span>
<span data-ttu-id="3b4db-137">С другой стороны, \бегин{алигн} c (U) c (V) c (U) ^ \дагжер \кет {0} \отимес \кет{\пси} & = \кет {0} \отимес \кет{\пси} \\ \\ & = \кет {0} \отимес (уу ^ \dagger \ket{\psi}) \\ \\ & = (\Boldone \otimes u) (c (V)) (\boldone \otimes u ^ \dagger) \ket {0} \otimes \ket{\psi}.</span><span class="sxs-lookup"><span data-stu-id="3b4db-137">On the other hand, \begin{align} c(U) c(V) c(U)^\dagger \ket{0} \otimes \ket{\psi} & = \ket{0} \otimes \ket{\psi} \\\\ & = \ket{0} \otimes (UU^\dagger \ket{\psi}) \\\\ & = (\boldone \otimes U) (c(V)) (\boldone \otimes U^\dagger) \ket{0} \otimes \ket{\psi}.</span></span>
<span data-ttu-id="3b4db-138">\енд{алигн} по линейной шкале, мы можем заключить, что мы можем $U $ out таким образом для всех состояний входных данных.</span><span class="sxs-lookup"><span data-stu-id="3b4db-138">\end{align} By linearity, we can conclude that we can factor $U$ out in this way for all input states.</span></span>
<span data-ttu-id="3b4db-139">То есть $c (УВУ ^ \дагжер) = U c (V) U ^ \дагжер $.</span><span class="sxs-lookup"><span data-stu-id="3b4db-139">That is, $c(UVU^\dagger) = U c(V) U^\dagger$.</span></span>
<span data-ttu-id="3b4db-140">Так как управление операциями может быть дорогостоящей в целом, использование контролируемых вариантов, таких как `WithC` и, `WithCA` может помочь сократить число операторов элементов управления, которые необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="3b4db-140">Since controlling operations can be expensive in general, using controlled variants such as `WithC` and `WithCA` can help reduce the number of control functors that need to be applied.</span></span>

> [!NOTE]
> <span data-ttu-id="3b4db-141">Еще одним следствием того, $U $, является то, что нам не нужно знать, как применять `Controlled` функтор к `U` .</span><span class="sxs-lookup"><span data-stu-id="3b4db-141">One other consequence of factoring out $U$ is that we need not even know how to apply the `Controlled` functor to `U`.</span></span>
> <span data-ttu-id="3b4db-142">`ApplyWithCA`Поэтому сигнатура более слаба, чем может быть ожидаемой:</span><span class="sxs-lookup"><span data-stu-id="3b4db-142">`ApplyWithCA` therefore has a weaker signature than might be expected:</span></span>
> ```qsharp
> ApplyWithCA<'T> : (('T => Unit is Adj),
>     ('T => Unit is Adj + Ctl), 'T) => Unit
> ```

<span data-ttu-id="3b4db-143">Аналогичным образом <xref:microsoft.quantum.canon.bound> создает операции, которые в свою очередь применяют последовательность других операций.</span><span class="sxs-lookup"><span data-stu-id="3b4db-143">Similarly, <xref:microsoft.quantum.canon.bound> produces operations which apply a sequence of other operations in turn.</span></span>
<span data-ttu-id="3b4db-144">Например, следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="3b4db-144">For instance, the following are equivalent:</span></span>

```qsharp
H(qubit); X(qubit);
Bound([H, X], qubit);
```

<span data-ttu-id="3b4db-145">Сочетание с шаблонами итерации может сделать это особенно полезно:</span><span class="sxs-lookup"><span data-stu-id="3b4db-145">Combining with iteration patterns can make this especially useful:</span></span>

```qsharp
// Bracket the quantum Fourier transform with $XH$ on each qubit.
ApplyWith(ApplyToEach(Bound([H, X]), _), QFT, _);
```

### <a name="time-ordered-composition"></a><span data-ttu-id="3b4db-146">Компоновка с сортировкой по времени</span><span class="sxs-lookup"><span data-stu-id="3b4db-146">Time-Ordered Composition</span></span> ###

<span data-ttu-id="3b4db-147">Мы можем еще дальше придумать управление потоком в терминах частичного приложения и классических функций, а также моделировать даже довольно сложные тактовые концепции с точки зрения классического управления потоком.</span><span class="sxs-lookup"><span data-stu-id="3b4db-147">We can go still further by thinking of flow control in terms of partial application and classical functions, and can model even fairly sophisticated quantum concepts in terms of classical flow control.</span></span>
<span data-ttu-id="3b4db-148">Эта аналогия выполняется точно в соответствии с определением того, что единые операторы точно соответствуют побочным эффектам вызывающих операций, таким образом, что декомпозиция отдельных операторов в терминах других действующих операторов соответствует созданию определенной вызывающей последовательности для классических подпрограмм, которые выдают инструкции для выполнения в качестве отдельных собственных операторов.</span><span class="sxs-lookup"><span data-stu-id="3b4db-148">This analogy is made precise by the recognition that unitary operators correspond exactly to the side effects of calling operations, such that any decomposition of unitary operators in terms of other unitary operators corresponds to constructing a particular calling sequence for classical subroutines which emit instructions to act as particular unitary operators.</span></span>
<span data-ttu-id="3b4db-149">В этом представлении `Bound` является точным представлением матричного произведения, поскольку `Bound([A, B])(target)` эквивалентно `A(target); B(target);` , который, в свою очередь, является вызывающей последовательность, соответствующей $BA $.</span><span class="sxs-lookup"><span data-stu-id="3b4db-149">Under this view, `Bound` is precisely the representation of the matrix product, since `Bound([A, B])(target)` is equivalent to `A(target); B(target);`, which in turn is the calling sequence corresponding to $BA$.</span></span>

<span data-ttu-id="3b4db-150">Более сложным примером является [расширение Троттер – Сузуки](https://arxiv.org/abs/math-ph/0506007v1).</span><span class="sxs-lookup"><span data-stu-id="3b4db-150">A more sophisticated example is the [Trotter–Suzuki expansion](https://arxiv.org/abs/math-ph/0506007v1).</span></span>
<span data-ttu-id="3b4db-151">Как обсуждалось в разделе представление динамического генератора [структур данных](xref:microsoft.quantum.libraries.data-structures), расширение Троттер – Сузуки предоставляет особенно полезный способ выражения экспоненциальных Экспонент.</span><span class="sxs-lookup"><span data-stu-id="3b4db-151">As discussed in the Dynamical Generator Representation section of [data structures](xref:microsoft.quantum.libraries.data-structures), the Trotter–Suzuki expansion provides a particularly useful way of expressing matrix exponentials.</span></span>
<span data-ttu-id="3b4db-152">Например, применение расширения в самом нижнем порядке дает для любых операторов $A $ и $B $ таким, что $A = A ^ \дагжер $ and $B = B ^ \дагжер $, \бегин{алигн} \таг{★} \лабел{ЕК: Троттер-Сузуки-0} \експ (i [A + B] t) = \ lim_ {н\то\инфти} \лефт (\експ (я A т/д) \exp (i B t/n) \right) ^ n.</span><span class="sxs-lookup"><span data-stu-id="3b4db-152">For instance, applying the expansion at its lowest order yields that for any operators $A$ and $B$ such that $A = A^\dagger$ and $B = B^\dagger$, \begin{align} \tag{★} \label{eq:trotter-suzuki-0} \exp(i [A + B] t) = \lim_{n\to\infty} \left(\exp(i A t / n) \exp(i B t / n)\right)^n.</span></span>
<span data-ttu-id="3b4db-153">\енд{алигн} разговорной речи, это говорит о том, что мы можем приблизительно развивать состояние в $A + B $B $A $.</span><span class="sxs-lookup"><span data-stu-id="3b4db-153">\end{align} Colloquially, this says that we can approximately evolve a state under $A + B$ by alternately evolving under $A$ and $B$ alone.</span></span>
<span data-ttu-id="3b4db-154">Если мы будем представлять развитие в рамках $A $ по операции `A : (Double, Qubit[]) => Unit` , которая применяет $e ^ {i t} $, то представление расширения Троттер – Сузуки в плане переупорядочения последовательностей вызовов станет ясным.</span><span class="sxs-lookup"><span data-stu-id="3b4db-154">If we represent evolution under $A$ by an operation `A : (Double, Qubit[]) => Unit` that applies $e^{i t A}$, then the representation of the Trotter–Suzuki expansion in terms of rearranging calling sequences becomes clear.</span></span>
<span data-ttu-id="3b4db-155">В частности, при наличии такой операции, `U : ((Int, Double, Qubit[]) => Unit is Adj + Ctl` что `A = U(0, _, _)` и `B = U(1, _, _)` , мы можем определить новую операцию, представляющую целую часть `U` времени $t $ путем создания последовательностей формы.</span><span class="sxs-lookup"><span data-stu-id="3b4db-155">Concretely, given an operation `U : ((Int, Double, Qubit[]) => Unit is Adj + Ctl` such that `A = U(0, _, _)` and `B = U(1, _, _)`, we can define a new operation representing the integral of `U` at time $t$ by generating sequences of the form</span></span>

```qsharp
U(0, time / Float(nSteps), target);
U(1, time / Float(nSteps), target);
U(0, time / Float(nSteps), target);
U(1, time / Float(nSteps), target);
// ...
```

<span data-ttu-id="3b4db-156">На этом этапе мы теперь можем потроттер о расширении Сузуки *без ссылки на механизм тактов*.</span><span class="sxs-lookup"><span data-stu-id="3b4db-156">At this point, we can now reason about the Trotter–Suzuki expansion *without reference to quantum mechanics at all*.</span></span>
<span data-ttu-id="3b4db-157">Развертывание фактически представляет собой очень конкретный шаблон итерации, на который послужила $ \екреф{ЕК: Троттер-Сузуки-0} $.</span><span class="sxs-lookup"><span data-stu-id="3b4db-157">The expansion is effectively a very particular iteration pattern motivated by $\eqref{eq:trotter-suzuki-0}$.</span></span>
<span data-ttu-id="3b4db-158">Этот шаблон итерации реализуется <xref:microsoft.quantum.canon.decomposeintotimestepsca> следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3b4db-158">This iteration pattern is implemented by <xref:microsoft.quantum.canon.decomposeintotimestepsca>:</span></span>

```qsharp
// The 2 indicates how many terms we need to decompose,
// while the 1 indicates that we are using the
// first-order Trotter–Suzuki decomposoition.
DecomposeIntoTimeStepsCA((2, U), 1);
```

<span data-ttu-id="3b4db-159">Сигнатура `DecomposeIntoTimeStepsCA` соответствует общему шаблону в Q #, где коллекции, которые могут быть включены в массивы, или что-то, какие элементы вычислений в режиме реального времени представлены кортежами, первыми элементами которых являются `Int` значения, указывающие на их длину.</span><span class="sxs-lookup"><span data-stu-id="3b4db-159">The signature of `DecomposeIntoTimeStepsCA` follows a common pattern in Q#, where collections that may be backed either by arrays or by something which compute elements on the fly are represented by tuples whose first elements are `Int` values indicating their lengths.</span></span>

## <a name="putting-it-together-controlling-operations"></a><span data-ttu-id="3b4db-160">Совместное размещение: управление операциями</span><span class="sxs-lookup"><span data-stu-id="3b4db-160">Putting it Together: Controlling Operations</span></span> ##

<span data-ttu-id="3b4db-161">Наконец, Canon строится на `Controlled` функтор, предоставляя дополнительные способы выполнения условных операций в такте.</span><span class="sxs-lookup"><span data-stu-id="3b4db-161">Finally, the canon builds on the `Controlled` functor by providing additional ways to condition quantum operations.</span></span>
<span data-ttu-id="3b4db-162">Обычно, особенно в тактовой арифметике, к условным операциям на основе состояний вычислительных операций, отличных от $ \ket{0\cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="3b4db-162">It is common, especially in quantum arithmetic, to condition operations on computational basis states other than $\ket{0\cdots 0}$.</span></span>
<span data-ttu-id="3b4db-163">Используя операции управления и функции, представленные выше, можно использовать более общие тактовые условия в одной инструкции.</span><span class="sxs-lookup"><span data-stu-id="3b4db-163">Using the control operations and functions introduced above, we can more general quantum conditions in a single statement.</span></span>
<span data-ttu-id="3b4db-164">Давайте вернемся к тому <xref:microsoft.quantum.canon.controlledonbitstring> , как это делает (параметры типа San), а затем разбивает части по одному.</span><span class="sxs-lookup"><span data-stu-id="3b4db-164">Let's jump in to how <xref:microsoft.quantum.canon.controlledonbitstring> does it (sans type parameters), then we'll break down the pieces one by one.</span></span>
<span data-ttu-id="3b4db-165">Первое, что нужно сделать, — это определить операцию, которая фактически выполняет тяжелую работу по реализации элемента управления на случайном уровне вычислительных операций.</span><span class="sxs-lookup"><span data-stu-id="3b4db-165">The first thing we'll need to do is to define an operation which actually does the heavy lifting of implementing the control on arbitrary computational basis states.</span></span>
<span data-ttu-id="3b4db-166">Однако мы не будем вызывать эту операцию напрямую, поэтому мы добавляем `_` в начало имени, чтобы указать, что это реализация другой конструкции в другом расположении.</span><span class="sxs-lookup"><span data-stu-id="3b4db-166">We won't call this operation directly, however, and so we add `_` to the beginning of the name to indicate that it's an implementation of another construct elsewhere.</span></span>

```qsharp
operation _ControlledOnBitString(
    bits : Bool[],
    oracle: (Qubit[] => Unit is Adj + Ctl),
    controlRegister : Qubit[],
    targetRegister: Qubit[])
: Unit is Adj + Ctl
```

<span data-ttu-id="3b4db-167">Обратите внимание, что мы принимаем строку битов, представленную в виде `Bool` массива, которую мы используем для указания условия, которое нужно применить к `oracle` определенной операции.</span><span class="sxs-lookup"><span data-stu-id="3b4db-167">Note that we take a string of bits, represented as a `Bool` array, that we use to specify the conditioning that we want to apply to the operation `oracle` that we are given.</span></span>
<span data-ttu-id="3b4db-168">Так как эта операция фактически выполняет приложение напрямую, нам также нужно взять контрольные и целевые регистры, представленные здесь как `Qubit[]` .</span><span class="sxs-lookup"><span data-stu-id="3b4db-168">Since this operation actually does the application directly, we also need to take the control and target registers, both represented here as `Qubit[]`.</span></span>

<span data-ttu-id="3b4db-169">Далее обратите внимание на то, что Управление вычислительным состоянием $ \кет{\век{с}} = \кет{с \_ 0 s \_ 1 \дотс s \_ {n-1}} $ для битовой строки $ \век{с} $ может быть реализовано путем преобразования $ \кет{\век{с}} $ в $ \ket{0\cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="3b4db-169">Next, we note that controlling on the computational basis state $\ket{\vec{s}} = \ket{s\_0 s\_1 \dots s\_{n - 1}}$ for a bit string $\vec{s}$ can be realized by transforming $\ket{\vec{s}}$ into $\ket{0\cdots 0}$.</span></span>
<span data-ttu-id="3b4db-170">В частности, $ \кет{\век{с}} = X ^ {s \_ 0} \Отимес x ^ {s \_ 1} \отимес \Кдотс \отимес x ^ {s \_ {n-1}} \ket{0\cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="3b4db-170">In particular, $\ket{\vec{s}} = X^{s\_0} \otimes X^{s\_1} \otimes \cdots \otimes X^{s\_{n - 1}} \ket{0\cdots 0}$.</span></span>
<span data-ttu-id="3b4db-171">Начиная с $X ^ {\дагжер} = X $, это означает, что $ \ket{0\dots 0} = X ^ {s \_ 0} \Отимес x ^ {s \_ 1} \отимес \Кдотс \отимес X ^ {s \_ {n-1}} \кет{\век{с}} $.</span><span class="sxs-lookup"><span data-stu-id="3b4db-171">Since $X^{\dagger} = X$, this implies that $\ket{0\dots 0} = X^{s\_0} \otimes X^{s\_1} \otimes \cdots \otimes X^{s\_{n - 1}} \ket{\vec{s}}$.</span></span>
<span data-ttu-id="3b4db-172">Таким образом, можно применить $P = X ^ {s \_ 0} \Отимес X ^ {s \_ 1} \отимес \Кдотс \отимес x ^ {s \_ {n-1}} $, Apply `Controlled oracle` и преобразовать обратно в $ \век{с} $.</span><span class="sxs-lookup"><span data-stu-id="3b4db-172">Thus, we can apply $P = X^{s\_0} \otimes X^{s\_1} \otimes \cdots \otimes X^{s\_{n - 1}}$, apply `Controlled oracle`, and transform back to $\vec{s}$.</span></span>
<span data-ttu-id="3b4db-173">Эта конструкция является точной `ApplyWith` , поэтому мы записываем тело нашей новой операции соответствующим образом:</span><span class="sxs-lookup"><span data-stu-id="3b4db-173">This construction is precisely `ApplyWith`, so we write the body of our new operation accordingly:</span></span>

```qsharp
{
    ApplyWithCA(
        ApplyPauliFromBitString(PauliX, false, bits, _),
        (Controlled oracle)(_, targetRegister),
        controlRegister
    );
}
```

<span data-ttu-id="3b4db-174">Здесь мы использовали, <xref:microsoft.quantum.canon.applypaulifrombitstring> чтобы применить $P $, частично применить его к цели для использования с `ApplyWith` .</span><span class="sxs-lookup"><span data-stu-id="3b4db-174">Here, we have used <xref:microsoft.quantum.canon.applypaulifrombitstring> to apply $P$, partially applying over its target for use with `ApplyWith`.</span></span>
<span data-ttu-id="3b4db-175">Однако обратите внимание, что нам нужно преобразовать *контрольную* регистрацию в нужную форму, поэтому мы частично приведем внутреннюю операцию к `(Controlled oracle)` *целевому объекту*.</span><span class="sxs-lookup"><span data-stu-id="3b4db-175">Note, however, that we need to transform the *control* register to our desired form, so we partially apply the inner operation `(Controlled oracle)` on the *target*.</span></span>
<span data-ttu-id="3b4db-176">Это покидает `ApplyWith` круглую скобку элемента управления с $P $ точно так же, как нам нужно.</span><span class="sxs-lookup"><span data-stu-id="3b4db-176">This leaves `ApplyWith` acting to bracket the control register with $P$, exactly as we desired.</span></span>

<span data-ttu-id="3b4db-177">На этом этапе можно было бы сделать, но это не противоречит тем, что наша новая операция не работает, как применение `Controlled` функтор.</span><span class="sxs-lookup"><span data-stu-id="3b4db-177">At this point, we could be done, but it is somehow unsatisfying that our new operation does not "feel" like applying the `Controlled` functor.</span></span>
<span data-ttu-id="3b4db-178">Поэтому мы завершаем определение нашей новой концепции потока управления путем написания функции, которая принимает Управление Oracle и возвращает новую операцию.</span><span class="sxs-lookup"><span data-stu-id="3b4db-178">Thus, we finish defining our new control flow concept by writing a function that takes the oracle to be controlled and that returns a new operation.</span></span>
<span data-ttu-id="3b4db-179">Таким образом, наша новая функция выглядит и похожа на ту `Controlled` , что мы можем легко определить мощные новые конструкции потока управления, используя Q # и Canon вместе:</span><span class="sxs-lookup"><span data-stu-id="3b4db-179">In this way, our new function looks and feels very much like `Controlled`, illustrating that we can easily define powerful new control flow constructs using Q# and the canon together:</span></span>

```qsharp
function ControlledOnBitString(
    bits : Bool[],
    oracle: (Qubit[] => Unit is Adj + Ctl))
: ((Qubit[], Qubit[]) => Unit is Adj + Ctl) {
    return _ControlledOnBitString(bits, oracle, _, _);
}
```
