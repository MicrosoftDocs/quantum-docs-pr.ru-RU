---
title: Операции и функции вQ#
description: Определение и вызов операций и функций, а также управляемых и примыкающих специализаций операций.
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.operationsfunctions
no-loc:
- Q#
- $$v
ms.openlocfilehash: 76437c83df894fa86409e680f961d97e267c6869
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2020
ms.locfileid: "87867885"
---
# <a name="operations-and-functions-in-no-locq"></a><span data-ttu-id="f3ab7-103">Операции и функции вQ#</span><span class="sxs-lookup"><span data-stu-id="f3ab7-103">Operations and Functions in Q#</span></span>

## <a name="defining-new-operations"></a><span data-ttu-id="f3ab7-104">Определение новых операций</span><span class="sxs-lookup"><span data-stu-id="f3ab7-104">Defining New Operations</span></span>

<span data-ttu-id="f3ab7-105">Операции являются ядром Q# .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-105">Operations are the core of Q#.</span></span>
<span data-ttu-id="f3ab7-106">После объявления их можно вызывать из классических приложений .NET, например с помощью симулятора или других операций в Q# .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-106">Once declared, they can either be called from classical .NET applications, for example, using a simulator or by other operations within Q#.</span></span>
<span data-ttu-id="f3ab7-107">Каждая операция, определенная в Q# , может вызывать любое количество других операций, включая встроенные внутренние операции, определенные в языке.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-107">Each operation defined in Q# can call any number of other operations, including the built-in intrinsic operations defined by the language.</span></span> <span data-ttu-id="f3ab7-108">Конкретный способ, который Q# определяет эти внутренние операции, зависит от целевого компьютера.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-108">The particular way in which Q# defines these intrinsic operations depends on the target machine.</span></span>
<span data-ttu-id="f3ab7-109">При компиляции каждая операция представляется как тип класса .NET, который можно предоставить целевым компьютерам.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-109">When compiled, each operation is represented as a .NET class type that can be provided to target machines.</span></span>

<span data-ttu-id="f3ab7-110">Каждый Q# исходный файл может определять любое количество операций.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-110">Each Q# source file can define any number of operations.</span></span>
<span data-ttu-id="f3ab7-111">Имена операций должны быть уникальными в пределах пространства имен и не могут конфликтовать с именами типа или функции.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-111">Operation names must be unique within a namespace and can not conflict with type or function names.</span></span>

<span data-ttu-id="f3ab7-112">Объявление операции состоит из ключевого слова `operation` , за которым следует символ, который представляет собой имя операции, кортеж типизированного идентификатора, определяющий аргументы для операции, двоеточие `:` , аннотацию типа, которая описывает тип результата операции, при необходимости заметку с характеристиками операции, открывающую фигурную скобку, а затем текст объявления операции, заключенный в фигурные скобки `{ }` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-112">An operation declaration consists of the keyword `operation`, followed by the symbol that is the operation's name, a typed identifier tuple that defines the arguments to the operation, a colon `:`, a type annotation that describes the operation's result type, optionally an annotation with the operation characteristics, an open brace, and then the body of the operation declaration, enclosed in braces `{ }`.</span></span>

<span data-ttu-id="f3ab7-113">Каждая операция принимает входные данные, создает выход и задает реализацию для одной или нескольких специализаций операций.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-113">Each operation takes an input, produces an output, and specifies the implementation for one or more operation specializations.</span></span>
<span data-ttu-id="f3ab7-114">Возможные специализации, а также способы их определения и вызова описаны в различных разделах этой статьи.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-114">The possible specializations, and how to define and call them, are detailed in the different sections of this article.</span></span>
<span data-ttu-id="f3ab7-115">Сейчас рассмотрим следующую операцию, которая определяет только специализацию тела по умолчанию и принимает одну кубит в качестве входных данных, а затем вызывает встроенную <xref:microsoft.quantum.intrinsic.x> операцию над этими входными данными:</span><span class="sxs-lookup"><span data-stu-id="f3ab7-115">For now, consider the following operation, which defines only a default body specialization and takes a single qubit as its input, then calls the built-in <xref:microsoft.quantum.intrinsic.x> operation on that input:</span></span>

```qsharp
operation BitFlip(target : Qubit) : Unit {
    X(target);
}
```

<span data-ttu-id="f3ab7-116">Ключевое слово `operation` начинается с определения операции, за которым следует имя; здесь, `BitFlip` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-116">The keyword `operation` begins the operation definition, followed by the name; here, `BitFlip`.</span></span>
<span data-ttu-id="f3ab7-117">Затем тип входных данных определяется ( `Qubit` ) вместе с именем, `target` для ссылки на входные данные в новой операции.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-117">Next, the type of input is defined (`Qubit`), along with a name, `target`, for referring to the input within the new operation.</span></span>
<span data-ttu-id="f3ab7-118">Наконец, `Unit` определяет, что выходные данные операции пусты.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-118">Lastly, `Unit` defines that the operation's output is empty.</span></span>
<span data-ttu-id="f3ab7-119">`Unit`используется аналогично `void` в C# и других императивных языках и эквивалентен `unit` в F # и других функциональных языках.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-119">`Unit` is used similarly to `void` in C# and other imperative languages and is equivalent to `unit` in F# and other functional languages.</span></span>

<span data-ttu-id="f3ab7-120">Операции также могут возвращать более интересные типы `Unit` , чем.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-120">Operations can also return more interesting types than `Unit`.</span></span>
<span data-ttu-id="f3ab7-121">Например, <xref:microsoft.quantum.intrinsic.m> операция возвращает выходные данные типа `Result` , представляющие выполнение измерения.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-121">For instance, the <xref:microsoft.quantum.intrinsic.m> operation returns an output of type `Result`, representing having performed a measurement.</span></span>  <span data-ttu-id="f3ab7-122">Его можно передать из операции в другую операцию или использовать с `let` ключевым словом для определения новой переменной.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-122">You can pass it from an operation to another operation or use it with the `let` keyword to define a new variable.</span></span>

<span data-ttu-id="f3ab7-123">Такой подход позволяет представить классические вычисления, взаимодействующие с операциями тактов на низком уровне, например в очень [плотной кодировке](https://github.com/microsoft/QuantumKatas/tree/master/SuperdenseCoding):</span><span class="sxs-lookup"><span data-stu-id="f3ab7-123">This approach allows for representing classical computation that interacts with quantum operations at a low level, such as in [superdense coding](https://github.com/microsoft/QuantumKatas/tree/master/SuperdenseCoding):</span></span>

```qsharp
operation DecodeSuperdense(here : Qubit, there : Qubit) : (Result, Result) {

    CNOT(there, here);
    H(there);

    let firstBit = M(there);
    let secondBit = M(here);

    return (firstBit, secondBit);
}
```

> [!NOTE]
> <span data-ttu-id="f3ab7-124">Каждая операция Q# принимает ровно один вход и возвращает ровно один выход.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-124">Each operation in Q# takes exactly one input and returns exactly one output.</span></span>
> <span data-ttu-id="f3ab7-125">Несколько входов и выходов представлены с помощью *кортежей*, которые собираются несколько значений вместе в одно значение.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-125">Multiple inputs and outputs are represented using *tuples*, which collect multiple values together into a single value.</span></span>
> <span data-ttu-id="f3ab7-126">В этом отношении Q# — это «кортеж-в кортеже».</span><span class="sxs-lookup"><span data-stu-id="f3ab7-126">In this regard, Q# is a "tuple-in tuple-out" language.</span></span>
> <span data-ttu-id="f3ab7-127">После этой концепции набор пустых круглых скобок, `()` должен считаться пустым кортежем, который имеет тип `Unit` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-127">Following this concept, a set of empty parentheses, `()`, should then be read as the "empty" tuple, which has the type `Unit`.</span></span>

## <a name="controlled-and-adjoint-operations"></a><span data-ttu-id="f3ab7-128">Контролируемые и смежные операции</span><span class="sxs-lookup"><span data-stu-id="f3ab7-128">Controlled and Adjoint Operations</span></span>

<span data-ttu-id="f3ab7-129">Если операция реализует единое преобразование, как в случае многих операций в Q# , то можно определить, как работает операция при *аджоинтед* или *управлении*.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-129">If an operation implements a unitary transformation, as is the case for many operations in Q#, then it is possible to define how the operation acts when *adjointed* or *controlled*.</span></span> <span data-ttu-id="f3ab7-130">В *примыкающей* специализации операции указывается, как действует "Инверсия" операции, а *управляемая* Специализация определяет, как работает операция, когда ее приложение записывается в состояние конкретного регистра такта.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-130">An *adjoint* specialization of an operation specifies how the "inverse" of the operation acts, while a *controlled* specialization specifies how an operation acts when its application is conditioned on the state of a particular quantum register.</span></span>

<span data-ttu-id="f3ab7-131">Аджоинтсие операций с тактами крайне важно для многих аспектов тактовых вычислений.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-131">Adjoints of quantum operations are crucial to many aspects of quantum computing.</span></span> <span data-ttu-id="f3ab7-132">Пример одной из таких ситуаций, обсуждаемой наряду с полезным Q# методом программирования, см. в разделе [лиц](#conjugations) в этой статье.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-132">For an example of one such situation discussed alongside a useful Q# programming technique, see [Conjugations](#conjugations) in this article.</span></span> 

<span data-ttu-id="f3ab7-133">Управляемая версия операции — это новая операция, которая фактически применяет базовую операцию только в том случае, если все элементы управления Кубитс находятся в указанном состоянии.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-133">The controlled version of an operation is a new operation that effectively applies the base operation only if all of the control qubits are in a specified state.</span></span>
<span data-ttu-id="f3ab7-134">Если элемент управления Кубитс в самом положении, то базовая операция применяется к соответствующей части детального размещения.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-134">If the control qubits are in superposition, then the base operation is applied coherently to the appropriate part of the superposition.</span></span>
<span data-ttu-id="f3ab7-135">Поэтому управляемые операции часто используются для создания замкнутые.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-135">Thus, controlled operations are often used to generate entanglement.</span></span>

<span data-ttu-id="f3ab7-136">Естественно, также может существовать *управляемая примыкающая* специализация, указывающая управляемое приложение для примыкающей операции.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-136">Naturally, a *controlled adjoint* specialization could exist as well, specifying the controlled application of an operation's adjoint.</span></span>

> [!NOTE]
> <span data-ttu-id="f3ab7-137">Если $U $ является единым преобразованием, реализованным операцией `U` , то `Adjoint U` представляет собой единое преобразование $U ^ \дагжер $, которое является комплексно-сопряженным преобразованием.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-137">If $U$ is the unitary transformation implemented by an operation `U`, then `Adjoint U` represents the unitary transformation $U^\dagger$, which is the complex conjugate transpose.</span></span>
> <span data-ttu-id="f3ab7-138">Успешное применение операции, а затем ее примыкающая к состоянию оставляет состояние без изменений, как показано на тот факт, что $UU ^ \дагжер = U ^ \дагжер U = \ид $, матрица Identity.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-138">Successively applying an operation and then its adjoint to a state leaves the state unchanged, as illustrated by the fact that $UU^\dagger = U^\dagger U = \id$, the identity matrix.</span></span>
> <span data-ttu-id="f3ab7-139">Единое представление управляемой операции немного сложнее, но дополнительные сведения см. в разделе [концепции тактовых вычислений: несколько Кубитс](xref:microsoft.quantum.concepts.multiple-qubits).</span><span class="sxs-lookup"><span data-stu-id="f3ab7-139">The unitary representation of a controlled operation is slightly more nuanced, but you can find more details at [Quantum computing concepts: multiple qubits](xref:microsoft.quantum.concepts.multiple-qubits).</span></span>

<span data-ttu-id="f3ab7-140">В следующем разделе описывается вызов этих различных специализаций в Q# коде и определение операций для их поддержки.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-140">The following section describes how to call these various specializations in your Q# code, and how to define operations to support them.</span></span>

### <a name="calling-operation-specializations"></a><span data-ttu-id="f3ab7-141">Действия при вызове специализаций операций</span><span class="sxs-lookup"><span data-stu-id="f3ab7-141">Calling operation specializations</span></span>

<span data-ttu-id="f3ab7-142">*Функтор* в Q# — это фабрика, которая определяет новую операцию на основе другой операции.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-142">A *functor* in Q# is a factory that defines a new operation from another operation.</span></span>
<span data-ttu-id="f3ab7-143">Два стандартных операторов в Q# — `Adjoint` и `Controlled` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-143">The two standard functors in Q# are `Adjoint` and `Controlled`.</span></span>

<span data-ttu-id="f3ab7-144">Операторов имеет доступ к реализации базовой операции при определении реализации новой операции.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-144">Functors have access to the implementation of the base operation when defining the implementation of the new operation.</span></span>
<span data-ttu-id="f3ab7-145">Таким же операторов может выполнять более сложные функции, чем традиционные функции более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-145">Thus, functors can perform more complex functions than traditional higher-level functions.</span></span> <span data-ttu-id="f3ab7-146">Операторов не имеют представления в Q# системе типов.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-146">Functors do not have a representation in the Q# type system.</span></span> <span data-ttu-id="f3ab7-147">Таким образом, сейчас невозможно привязать их к переменной или передать в качестве аргументов.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-147">It is thus currently not possible to bind them to a variable or pass them as arguments.</span></span> 

<span data-ttu-id="f3ab7-148">Используйте функтор, применив его к операции, которая возвращает новую операцию.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-148">Use a functor by applying it to an operation, which returns a new operation.</span></span>
<span data-ttu-id="f3ab7-149">Например, применение `Adjoint` функтор к `Y` операции возвращает новую операцию `Adjoint Y` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-149">For example, applying the `Adjoint` functor to the `Y` operation returns the new operation `Adjoint Y`.</span></span> <span data-ttu-id="f3ab7-150">Новую операцию можно вызвать, как и любые другие операции.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-150">You can invoke the new operation like any other operation.</span></span>
<span data-ttu-id="f3ab7-151">Чтобы операция поддерживала приложение `Adjoint` или `Controlled` операторов, ее тип возвращаемого значения обязательно должен быть `Unit` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-151">For an operation to support the application of the `Adjoint` or `Controlled` functors, its return type necessarily needs to be `Unit`.</span></span> 

#### <a name="adjoint-functor"></a><span data-ttu-id="f3ab7-152">`Adjoint`Функтор</span><span class="sxs-lookup"><span data-stu-id="f3ab7-152">`Adjoint` functor</span></span>

<span data-ttu-id="f3ab7-153">Таким же действие `Adjoint Y(q1)` применяет `Adjoint` функтор к `Y` операции для создания новой операции и применяет эту новую операцию к `q1` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-153">Thus, `Adjoint Y(q1)` applies the `Adjoint` functor to the `Y` operation to generate a new operation, and applies that new operation to `q1`.</span></span>
<span data-ttu-id="f3ab7-154">Новая операция имеет ту же сигнатуру и тип, что и базовая операция `Y` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-154">The new operation has the same signature and type as the base operation `Y`.</span></span>
<span data-ttu-id="f3ab7-155">В частности, новая операция также поддерживает и `Adjoint` поддерживает `Controlled` только в том случае, если базовая операция выполнена.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-155">In particular, the new operation also supports `Adjoint`, and supports `Controlled` if and only if the base operation did.</span></span>
<span data-ttu-id="f3ab7-156">`Adjoint`Функтор является собственным инверсией, то есть всегда совпадает с `Adjoint Adjoint Op` `Op` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-156">The `Adjoint` functor is its own inverse; that is, `Adjoint Adjoint Op` is always the same as `Op`.</span></span>

#### <a name="controlled-functor"></a><span data-ttu-id="f3ab7-157">`Controlled`Функтор</span><span class="sxs-lookup"><span data-stu-id="f3ab7-157">`Controlled` functor</span></span>

<span data-ttu-id="f3ab7-158">Аналогично, `Controlled X(controls, target)` применяет `Controlled` функтор к `X` операции для создания новой операции и применяет эту новую операцию к `controls` и `target` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-158">Similarly, `Controlled X(controls, target)` applies the `Controlled` functor to the `X` operation to generate a new operation, and applies that new operation to `controls` and `target`.</span></span>

> [!NOTE]
> <span data-ttu-id="f3ab7-159">В Q# контролируемые версии всегда принимают массив элементов управления Кубитс, и управление всегда основано на всех элементах управления Кубитс, находящихся в состоянии вычисления ( `PauliZ` ) `One` , $ \кет {1} $.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-159">In Q#, controlled versions always take an array of control qubits, and the controlling is always based on all of the control qubits being in the computational (`PauliZ`) `One` state, $\ket{1}$.</span></span>
> <span data-ttu-id="f3ab7-160">Управление на основе других состояний достигается путем применения соответствующей единой операции к элементу управления, Кубитс перед управляемой операцией, и последующего применения обратной операции после выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-160">Controlling based on other states is achieved by applying the appropriate unitary operation to the control qubits before the controlled operation, and then applying the inverses of the unitary operation after the controlled operation.</span></span>
> <span data-ttu-id="f3ab7-161">Например, применение `X` операции к элементу управления, кубит до и после управляемой операции, приводит к тому, что операция управляет `Zero` состоянием ($ \кет {0} $) для этого кубит; применение `H` операции до и после элементов управления в `PauliX` `One` состоянии, то есть-1 еиженвалуе Паули X, $ \кет {-} \масрел{: =} (\кет {0} -\кет {1} )/\скрт {2} $, а не `PauliZ` `One` состояния.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-161">For example, applying an `X` operation to a control qubit before and after a controlled operation causes the operation to control on the `Zero` state ($\ket{0}$) for that qubit; applying an `H` operation before and after controls on the `PauliX` `One` state, that is -1 eigenvalue of Pauli X, $\ket{-} \mathrel{:=} (\ket{0} - \ket{1}) / \sqrt{2}$ rather than the `PauliZ` `One` state.</span></span>

<span data-ttu-id="f3ab7-162">При наличии выражения операции можно сформировать новое выражение операции с помощью `Controlled` функтор.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-162">Given an operation expression, you can form a new operation expression by using the `Controlled` functor.</span></span>
<span data-ttu-id="f3ab7-163">Сигнатура новой операции основана на сигнатуре исходной операции.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-163">The signature of the new operation is based on the signature of the original operation.</span></span>
<span data-ttu-id="f3ab7-164">Тип результата такой же, но тип входных данных — это кортеж с массивом кубит, содержащий элемент управления кубит в качестве первого элемента и аргументы исходной операции в качестве второго элемента.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-164">The result type is the same, but the input type is a two-tuple with a qubit array that holds the control qubit(s) as the first element and the arguments of the original operation as the second element.</span></span>
<span data-ttu-id="f3ab7-165">Новая операция поддерживает и `Controlled` будет поддерживать `Adjoint` только в том случае, если была выполнена исходная операция.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-165">The new operation supports `Controlled`, and will support `Adjoint` if and only if the original operation did.</span></span>

<span data-ttu-id="f3ab7-166">Если исходная операция заняла только один аргумент, то здесь поступает [эквивалентность одноэлементного кортежа](xref:microsoft.quantum.guide.types) .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-166">If the original operation took only a single argument, then [singleton tuple equivalence](xref:microsoft.quantum.guide.types) comes into play here.</span></span>
<span data-ttu-id="f3ab7-167">Например, `Controlled X` является управляемой версией `X` операции.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-167">For instance, `Controlled X` is the controlled version of the `X` operation.</span></span> 
<span data-ttu-id="f3ab7-168">`X`имеет тип `(Qubit => Unit is Adj + Ctl)` , поэтому `Controlled X` имеет тип `((Qubit[], (Qubit)) => Unit is Adj + Ctl)` ; из-за равенства одноэлементных кортежей это то же самое, что `((Qubit[], Qubit) => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-168">`X` has type `(Qubit => Unit is Adj + Ctl)`, so `Controlled X` has type `((Qubit[], (Qubit)) => Unit is Adj + Ctl)`; because of singleton tuple equivalence, this is the same as `((Qubit[], Qubit) => Unit is Adj + Ctl)`.</span></span>

<span data-ttu-id="f3ab7-169">Если базовая операция заняла несколько аргументов, не забудьте заключить соответствующие аргументы управляемой версии операции в круглые скобки, чтобы преобразовать их в кортеж.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-169">If the base operation took several arguments, remember to enclose the corresponding arguments of the controlled version of the operation in parentheses to convert them into a tuple.</span></span>
<span data-ttu-id="f3ab7-170">Например, `Controlled Rz` является управляемой версией `Rz` операции.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-170">For instance, `Controlled Rz` is the controlled version of the `Rz` operation.</span></span> 
<span data-ttu-id="f3ab7-171">`Rz`имеет тип `((Double, Qubit) => Unit is Adj + Ctl)` , поэтому `Controlled Rz` имеет тип `((Qubit[], (Double, Qubit)) => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-171">`Rz` has type `((Double, Qubit) => Unit is Adj + Ctl)`, so `Controlled Rz` has type `((Qubit[], (Double, Qubit)) => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="f3ab7-172">Таким образом, будет `Controlled Rz(controls, (0.1, target))` допустимым вызовом `Controlled Rz` (Обратите внимание на круглые скобки `0.1, target` ).</span><span class="sxs-lookup"><span data-stu-id="f3ab7-172">Thus, `Controlled Rz(controls, (0.1, target))` would be a valid invocation of `Controlled Rz` (note the parentheses around `0.1, target`).</span></span>

<span data-ttu-id="f3ab7-173">В качестве другого примера `CNOT(control, target)` можно реализовать как `Controlled X([control], target)` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-173">As another example, `CNOT(control, target)` can be implemented as `Controlled X([control], target)`.</span></span> <span data-ttu-id="f3ab7-174">Если целевой объект должен управляться двумя элементами управления Кубитс (ККНОТ), используйте `Controlled X([control1, control2], target)` инструкцию.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-174">If a target should be controlled by two control qubits (CCNOT), use a `Controlled X([control1, control2], target)` statement.</span></span>

#### `Controlled Adjoint` 

<span data-ttu-id="f3ab7-175">`Controlled`И `Adjoint` операторов работы, поэтому нет никакой разницы между применением `Controlled Adjoint Op` или `Adjoint Controlled Op` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-175">The `Controlled` and `Adjoint` functors commute, so there is no difference between applying `Controlled Adjoint Op` or `Adjoint Controlled Op`.</span></span>


## <a name="defining-controlled-and-adjoint-implementations"></a><span data-ttu-id="f3ab7-176">Определение управляемых и смежных реализаций</span><span class="sxs-lookup"><span data-stu-id="f3ab7-176">Defining Controlled and Adjoint Implementations</span></span>

<span data-ttu-id="f3ab7-177">В объявлении первой операции в предыдущих примерах операции `BitFlip` и `DecodeSuperdense` были определены с помощью сигнатур `(Qubit => Unit)` и `((Qubit, Qubit) => (Result, Result))` соответственно.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-177">In the first operation declaration in the previous examples, the operations `BitFlip` and `DecodeSuperdense` were defined with signatures `(Qubit => Unit)` and `((Qubit, Qubit) => (Result, Result))`, respectively.</span></span>
<span data-ttu-id="f3ab7-178">Как `DecodeSuperdense` и в случае с измерениями, это не единая операция, поэтому не может существовать ни управляемая несмежная специализация (отозвать связанное требование, возвращаемое операцией `Unit` ).</span><span class="sxs-lookup"><span data-stu-id="f3ab7-178">As `DecodeSuperdense` includes measurements, it is not a unitary operation, and therefore neither controlled not adjoint specializations could exist (recall the related requirement that such an operation return `Unit`).</span></span>
<span data-ttu-id="f3ab7-179">Однако, как `BitFlip` просто выполняет единую <xref:microsoft.quantum.intrinsic.x> операцию, вы могли бы определить ее с обеими специализациями.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-179">However, as `BitFlip` simply performs the unitary <xref:microsoft.quantum.intrinsic.x> operation, you could have defined it with both specializations.</span></span>

<span data-ttu-id="f3ab7-180">В этом разделе подробно описано, как включить существование специализаций в Q# объявлениях операций, таким образом давая им возможность вызывать в сочетании с параметром `Adjoint` или `Controlled` операторов.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-180">This section details how to include the existence of specializations in your Q# operation declarations, hence giving them the ability to called in conjunction with the `Adjoint` or `Controlled` functors.</span></span>
<span data-ttu-id="f3ab7-181">Дополнительные сведения о некоторых ситуациях, в которых он является допустимым или недопустимым для объявления определенных специализаций, см. в разделе [условия для правильного определения специализаций](#circumstances-for-validly-defining-specializations) в этой статье.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-181">For more information about some of the situations in which it is either valid or not valid to declare certain specializations, see [Circumstances for validly defining specializations](#circumstances-for-validly-defining-specializations) in this article.</span></span>

<span data-ttu-id="f3ab7-182">Характеристики операции определяют типы операторов, которые можно применить к объявленной операции, и их воздействие.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-182">Operation characteristics define what kinds of functors you can apply to the declared operation, and what effect they have.</span></span> <span data-ttu-id="f3ab7-183">Существование этих специализаций можно объявить как часть сигнатуры операции, в частности через заметку с характеристиками операции: `is Adj` , `is Ctl` или `is Adj + Ctl` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-183">The existence of these specializations can be declared as part of the operation signature, specifically through an annotation with the operation characteristics: either `is Adj`, `is Ctl`, or `is Adj + Ctl`.</span></span>
<span data-ttu-id="f3ab7-184">Фактическая реализация каждой специализации *может быть либо явно,* либо *явно* определена.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-184">The actual implementation of each specialization can either be *implicitly* or *explicitly* defined.</span></span>

### <a name="implicitly-specifying-implementations"></a><span data-ttu-id="f3ab7-185">Неявное указание реализаций</span><span class="sxs-lookup"><span data-stu-id="f3ab7-185">Implicitly specifying implementations</span></span>

<span data-ttu-id="f3ab7-186">В этом случае тело объявления операции состоит только из реализации по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-186">In this case, the body of the operation declaration consists solely of the default implementation.</span></span> <span data-ttu-id="f3ab7-187">Пример:</span><span class="sxs-lookup"><span data-stu-id="f3ab7-187">For example:</span></span>

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit 
is Adj + Ctl { // implies the existence of an adjoint, a controlled, and a controlled adjoint specialization
    H(here);
    CNOT(here, there);
}
```
<span data-ttu-id="f3ab7-188">В этом случае соответствующая реализация для каждой такой неявно объявленной специализации автоматически создается компилятором, который будет выполняться при `Adjoint` использовании или `Controlled` операторов.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-188">Here, the corresponding implementation for each such implicitly declared specialization is automatically generated by the compiler, to be performed if the `Adjoint` or `Controlled` functors are used.</span></span>

<span data-ttu-id="f3ab7-189">Таким образом, вызов будет приводить к тому, что `Adjoint PrepareEntangledPair` компилятор реализует смежную часть `CNOT` , а затем прилегающая `H` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-189">So, a call of `Adjoint PrepareEntangledPair` would result in the compiler implementing the adjoint of `CNOT` and then the adjoint of `H`.</span></span>
<span data-ttu-id="f3ab7-190">Эти отдельные операции являются самостоятельными, поэтому итоговая `Adjoint PrepareEntangledPair` операция будет просто состоять из применения, `CNOT(here, there)` а затем `H(here)` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-190">These individual operations are both self-adjoint, so the resulting `Adjoint PrepareEntangledPair` operation would simply consist of applying `CNOT(here, there)` and then `H(here)`.</span></span>
<span data-ttu-id="f3ab7-191">Таким образом, вы можете использовать его для записи `DecodeSuperdense` в предыдущем примере более компактно, используя смежную часть `PrepareEntangledPair` для преобразования состояния запутанными обратно в унентанглед пару Кубитс:</span><span class="sxs-lookup"><span data-stu-id="f3ab7-191">Hence you can use this to write the `DecodeSuperdense` in the previous example more compactly, by using the adjoint of `PrepareEntangledPair` to transform the entangled state back into an unentangled pair of qubits:</span></span>

```qsharp
operation DecodeSuperdense(here : Qubit, there : Qubit) : (Result, Result) {
    Adjoint PrepareEntangledPair(there, here);

    let firstBit = M(there);
    let secondBit = M(here);

    return (firstBit, secondBit);
}
```

<span data-ttu-id="f3ab7-192">Заметка с характеристиками операций в объявлении полезна для того, чтобы компилятор создавал на основе реализации по умолчанию другие специализации.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-192">The annotation with the operation characteristics in the declaration is useful to ensure that the compiler auto-generates other specializations based on the default implementation.</span></span> 

<span data-ttu-id="f3ab7-193">При проектировании операций для использования с операторов необходимо учитывать ряд важных ограничений.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-193">There are several important limitations to consider when designing operations for use with functors.</span></span>
<span data-ttu-id="f3ab7-194">Как правило, специализации для операции, которая использует выходное значение любой другой операции, *не могут* быть созданы компилятором автоматически, так как это неоднозначно, как изменить порядок инструкций в такой операции, чтобы получить такой же результат.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-194">Most critically, specializations for an operation that uses the output value of any other operation *cannot* be auto-generated by the compiler, as it is ambiguous how to reorder the statements in such an operation to obtain the same effect.</span></span>

<span data-ttu-id="f3ab7-195">Таким образом, часто бывает полезно явно указывать различные реализации.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-195">Therefore, it is often useful to explicitly specify the various implementations.</span></span>

### <a name="explicitly-specifying-implementations"></a><span data-ttu-id="f3ab7-196">Явное указание реализаций</span><span class="sxs-lookup"><span data-stu-id="f3ab7-196">Explicitly specifying implementations</span></span>

<span data-ttu-id="f3ab7-197">Если компилятор не может создать реализацию, можно указать его явным образом.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-197">In the case where the compiler cannot generate the implementation, you can specify it explicitly.</span></span> <span data-ttu-id="f3ab7-198">Такие явные объявления специализации могут состоять из подходящей *директивы создания* или определяемой пользователем реализации.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-198">Such explicit specialization declarations can consist of a suitable *generation directive* or a user-defined implementation.</span></span>
<span data-ttu-id="f3ab7-199">Ниже приведен полный спектр возможностей, а также некоторые примеры явной специализации.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-199">Following are the full range of possibilities, with some examples of explicit specialization.</span></span> 


#### <a name="explicit-specialization-declarations"></a><span data-ttu-id="f3ab7-200">Явные объявления специализации</span><span class="sxs-lookup"><span data-stu-id="f3ab7-200">Explicit specialization declarations</span></span>

<span data-ttu-id="f3ab7-201">Q#операции могут содержать следующие явные объявления специализации:</span><span class="sxs-lookup"><span data-stu-id="f3ab7-201">Q# operations can contain the following explicit specialization declarations:</span></span>

- <span data-ttu-id="f3ab7-202">В `body` специализации указывается реализация операции без применения операторов.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-202">The `body` specialization specifies the implementation of the operation with no functors applied.</span></span>
- <span data-ttu-id="f3ab7-203">В `adjoint` специализации указывается реализация операции с `Adjoint` примененным функтор.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-203">The `adjoint` specialization specifies the implementation of the operation with the `Adjoint` functor applied.</span></span>
- <span data-ttu-id="f3ab7-204">В `controlled` специализации указывается реализация операции с `Controlled` примененным функтор.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-204">The `controlled` specialization specifies the implementation of the operation with the `Controlled` functor applied.</span></span>
- <span data-ttu-id="f3ab7-205">`controlled adjoint`Специализация задает реализацию операции с `Adjoint` `Controlled` примененными к и операторов.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-205">The `controlled adjoint` specialization specifies the implementation of the operation with both the `Adjoint` and `Controlled` functors applied.</span></span>
  <span data-ttu-id="f3ab7-206">Эту специализацию также можно присвоить имя `adjoint controlled` , так как две операторов работы.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-206">This specialization can also be named `adjoint controlled`, since the two functors commute.</span></span>


<span data-ttu-id="f3ab7-207">Специализация операции состоит из тега специализации (например, `body` или), `adjoint` за которым следует одно из следующих:</span><span class="sxs-lookup"><span data-stu-id="f3ab7-207">An operation specialization consists of the specialization tag (for example, `body` or `adjoint`) followed by one of:</span></span>

- <span data-ttu-id="f3ab7-208">Явное объявление, как описано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-208">An explicit declaration as described in the following.</span></span>
- <span data-ttu-id="f3ab7-209">*Директива* , сообщающая компилятору, *как* создать специализацию, одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="f3ab7-209">A *directive* that tells the compiler *how* to generate the specialization, one of:</span></span>
  - <span data-ttu-id="f3ab7-210">`intrinsic`, что указывает на то, что целевой компьютер предоставляет специализацию.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-210">`intrinsic`, which indicates that the target machine provides the specialization.</span></span>
  - <span data-ttu-id="f3ab7-211">`distribute`, используемый с `controlled` `controlled adjoint` специализациями и.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-211">`distribute`, used with the `controlled` and `controlled adjoint` specializations.</span></span>
    <span data-ttu-id="f3ab7-212">При использовании с параметр указывает на то `controlled` , что компилятор должен вычислить специализацию, применяя `Controlled` ко всем операциям в `body` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-212">When used with `controlled`, it indicates that the compiler should compute the specialization by applying `Controlled` to all of the operations in the `body`.</span></span>
    <span data-ttu-id="f3ab7-213">При использовании с параметр указывает на то `controlled adjoint` , что компилятор должен вычислить специализацию, применяя `Controlled` ко всем операциям в `adjoint` специализации.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-213">When used with `controlled adjoint`, it indicates that the compiler should compute the specialization by applying `Controlled` to all of the operations in the `adjoint` specialization.</span></span>
  - <span data-ttu-id="f3ab7-214">`invert`, который указывает, что компилятор должен вычислить `adjoint` специализацию путем инвертирования `body` , например для реверсирования порядка операций и применения прилегающих к каждому из них.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-214">`invert`, which indicates that the compiler should compute the `adjoint` specialization by inverting the `body`, for example, reversing the order of operations and applying the adjoint to each one.</span></span>
    <span data-ttu-id="f3ab7-215">Если используется с `adjoint controlled` , это означает, что компилятор должен вычислить специализацию путем инвертирования `controlled` специализации.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-215">When used with `adjoint controlled`, this indicates that the compiler should compute the specialization by inverting the `controlled` specialization.</span></span>
  - <span data-ttu-id="f3ab7-216">`self`, чтобы указать, что прилегающий специализации совпадает с `body` специализацией.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-216">`self`, to indicate that the adjoint specialization is the same as the `body` specialization.</span></span>
    <span data-ttu-id="f3ab7-217">Использование `self` является допустимым для `adjoint` `adjoint controlled` специализаций и.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-217">Using `self` is legal for the `adjoint` and `adjoint controlled` specializations.</span></span>
    <span data-ttu-id="f3ab7-218">Для `adjoint controlled` , `self` предполагает, что `adjoint controlled` специализация является той же, что и `controlled` специализация.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-218">For `adjoint controlled`, `self` implies that the `adjoint controlled` specialization is the same as the `controlled` specialization.</span></span>
  - <span data-ttu-id="f3ab7-219">`auto`, чтобы указать, что компилятор должен выбрать соответствующую директиву для применения.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-219">`auto`, to indicate that the compiler should select an appropriate directive to apply.</span></span>
    <span data-ttu-id="f3ab7-220">Нельзя использовать `auto` для `body` специализации.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-220">You cannot use`auto` for the `body` specialization.</span></span>

<span data-ttu-id="f3ab7-221">Для директив и `auto` ALL требуется закрывающая точка с запятой `;` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-221">The directives and `auto` all require a closing semi-colon `;`.</span></span>
<span data-ttu-id="f3ab7-222">`auto`Директива разрешается в следующую созданную директиву, если предоставлено явное объявление объекта `body` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-222">The `auto` directive resolves to the following generated directive if an explicit declaration of the `body` is provided:</span></span>

- <span data-ttu-id="f3ab7-223">`adjoint`Специализация создается в соответствии с директивой `invert` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-223">The `adjoint` specialization generates according to the directive `invert`.</span></span>
- <span data-ttu-id="f3ab7-224">`controlled`Специализация создается в соответствии с директивой `distribute` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-224">The `controlled` specialization generates according to the directive `distribute`.</span></span>
- <span data-ttu-id="f3ab7-225">`adjoint controlled`Специализация создается в соответствии с директивой `invert` , если явное объявление для задано `controlled` , но не для `adjoint` , и `distribute` в противном случае.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-225">The `adjoint controlled` specialization  generates according to the directive `invert` if an explicit declaration for `controlled` is given but not one for `adjoint`, and `distribute` otherwise.</span></span>

> [!TIP]   
> <span data-ttu-id="f3ab7-226">Если операция является самопримыкающей, явно укажите либо примыкающую, либо управляемую смежную специализацию с помощью директивы поколения, `self` чтобы компилятор использовал эту информацию в целях оптимизации.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-226">If an operation is self-adjoint, explicitly specify either the adjoint or the controlled adjoint specialization via the generation directive `self` to allow the compiler to make use of that information for optimization purposes.</span></span>

<span data-ttu-id="f3ab7-227">Объявление специализации, содержащее определяемую пользователем реализацию, состоит из кортежа аргументов, за которым следует блок операторов с Q# кодом, реализующим специализацию.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-227">A specialization declaration containing a user-defined implementation consists of an argument tuple followed by a statement block with the Q# code that implements the specialization.</span></span>
<span data-ttu-id="f3ab7-228">В списке arguments `...` используется для представления аргументов, объявленных для операции в целом.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-228">In the argument list, `...` is used to represent the arguments declared for the operation as a whole.</span></span>
<span data-ttu-id="f3ab7-229">Для `body` и `adjoint` список аргументов всегда должен иметь значение `(...)` ; для `controlled` и `adjoint controlled` список аргументов должен быть символом, представляющим массив элементов управления Кубитс, за которым следует `...` ключ, заключенный в круглые скобки, например `(controls,...)` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-229">For `body` and `adjoint`, the argument list should always be `(...)`; for `controlled` and `adjoint controlled`, the argument list should be a symbol that represents the array of control qubits, followed by `...`, enclosed in parentheses; for example, `(controls,...)`.</span></span>

### <a name="examples"></a><span data-ttu-id="f3ab7-230">Примеры</span><span class="sxs-lookup"><span data-stu-id="f3ab7-230">Examples</span></span>

<span data-ttu-id="f3ab7-231">Объявление операции может быть простым, как показано ниже, которое определяет операцию примитива Паули X:</span><span class="sxs-lookup"><span data-stu-id="f3ab7-231">An operation declaration might be as simple as the following, which defines the primitive Pauli X operation:</span></span>

```qsharp
operation X (qubit : Qubit) : Unit
is Adj + Ctl {
    body intrinsic;
    adjoint self;
}
```
<span data-ttu-id="f3ab7-232">Обратите внимание, что смежная операция Паули X определяется с помощью директивы, `self` так как по определению `X` является обратным.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-232">Note that the adjoint of the Pauli X operation is defined with the directive `self` because by definition `X` is its own inverse.</span></span>

<span data-ttu-id="f3ab7-233">В предыдущем `PrepareEntangledPair` примере код эквивалентен следующему коду, содержащему явные объявления специализации:</span><span class="sxs-lookup"><span data-stu-id="f3ab7-233">In the earlier `PrepareEntangledPair` example, the code is equivalent to the following code containing explicit specialization declarations:</span></span> 

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit 
is Ctl + Adj {
    body (...) { // default body specialization
        H(here);
        CNOT(here, there);
    }

    adjoint auto; // auto-generate adjoint specialization
    controlled auto; // auto-generate controlled specialization
    controlled adjoint auto; // auto-generate controlled adjoint specialization
}
```
<span data-ttu-id="f3ab7-234">Ключевое слово `auto` указывает, что компилятор должен определить, как создать реализацию специализации.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-234">The keyword `auto` indicates that the compiler should determine how to generate the specialization implementation.</span></span>

#### <a name="user-defined-specialization-implementation"></a><span data-ttu-id="f3ab7-235">Реализация пользовательской специализации</span><span class="sxs-lookup"><span data-stu-id="f3ab7-235">User-defined specialization implementation</span></span>

<span data-ttu-id="f3ab7-236">Если компилятор не может автоматически создать реализацию для определенной специализации или если может быть предоставлена более эффективная реализация, можно вручную определить реализацию.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-236">If the compiler cannot generate the implementation for a certain specialization automatically, or if a more efficient implementation can be given, then you can manually define the implementation.</span></span>

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit
is Ctl + Adj {
    body (...) { // default body specialization
        H(here);
        CNOT(here, there);
    }

    controlled (cs, ...) { // user-defined implementation for the controlled specialization
        Controlled H(cs, here);
        Controlled X(cs + [here], there);
    }

    adjoint invert; 
    controlled adjoint invert; 
}
```
<span data-ttu-id="f3ab7-237">В предыдущем примере `adjoint invert;` указывает, что примыкающая специализация должна быть создана путем инвертирования реализации тела, и `controlled adjoint invert;` указывает, что управляемая примыкающая специализация должна создаваться путем инвертирования заданной реализации управляемой специализации.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-237">In the previous example, `adjoint invert;` indicates that the adjoint specialization is to be generated by inverting the body implementation, and `controlled adjoint invert;` indicates that the controlled adjoint specialization is to be generated by inverting the given implementation of the controlled specialization.</span></span>

<span data-ttu-id="f3ab7-238">Если необходимо явно объявить одну или несколько специализаций, кроме тела по умолчанию, то реализация тела по умолчанию должна быть заключена в подходящее объявление специализации:</span><span class="sxs-lookup"><span data-stu-id="f3ab7-238">If one or more specializations besides the default body need to be explicitly declared, then the implementation for the default body needs to be wrapped into a suitable specialization declaration as well:</span></span>

```qsharp
operation CountOnes(qubits: Qubit[]) : Int {

    body (...) // default body specialization
    {
        mutable n = 0;
        for (qubit in qubits) {
            set n += M(q) == One ? 1 | 0;
        }
        return n;
    }

    ...
```

### <a name="circumstances-for-validly-defining-specializations"></a><span data-ttu-id="f3ab7-239">Условия для корректного определения специализаций</span><span class="sxs-lookup"><span data-stu-id="f3ab7-239">Circumstances for validly defining specializations</span></span>

#### <a name="operation-declarations-with-adjointcontrolled"></a><span data-ttu-id="f3ab7-240">Объявления операций с примыкающими и управляемыми данными</span><span class="sxs-lookup"><span data-stu-id="f3ab7-240">Operation declarations with adjoint/controlled</span></span>

<span data-ttu-id="f3ab7-241">Допускается указание операции без смежных или контролируемых версий.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-241">It is legal to specify an operation with no adjoint or controlled versions.</span></span> <span data-ttu-id="f3ab7-242">Например, операции измерения не имеют ни одного из них, так как они не являются обратимыми или управляемыми.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-242">For instance, measurement operations have neither because they are not invertible or controllable.</span></span>

<span data-ttu-id="f3ab7-243">Операция поддерживает `Adjoint` и операторов, `Controlled` если ее объявление содержит неявное или неявное объявление соответствующих специализаций.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-243">An operation supports the `Adjoint` and `Controlled` functors if its declaration contains an implicit or explicit declaration of the respective specializations.</span></span>

<span data-ttu-id="f3ab7-244">Явная объявленная специализация с прилегающая, управляемой, подразумевает наличие примыкающей или управляемой специализации.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-244">An explicitly declared adjoint/controlled specialization implies the existence of an adjoint/controlled specialization.</span></span> 

<span data-ttu-id="f3ab7-245">Для операции, текст которой содержит циклы повторения, инструкции SET, измерения, операторы Return или вызовы других операций, которые не поддерживают `Adjoint` функтор, автоматическое создание примыкающей специализации, следующей за `invert` директивой или, невозможно `auto` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-245">For an operation whose body contains repeat-until-success loops, set statements, measurements, return statements, or calls to other operations that do not support the `Adjoint` functor, auto-generating an adjoint specialization following the `invert` or `auto` directive is not possible.</span></span>

<span data-ttu-id="f3ab7-246">Для операции, текст которой содержит вызовы других операций, не поддерживающих `Controlled` функтор, автоматическое создание управляемой специализации, следующей за `distribute` директивой или, невозможно `auto` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-246">For an operation whose body contains calls to other operations that do not support the `Controlled` functor, auto-generating a controlled specialization following the `distribute` or `auto` directive is not possible.</span></span>

#### <a name="controlled-adjoint"></a><span data-ttu-id="f3ab7-247">Управляемый соседний</span><span class="sxs-lookup"><span data-stu-id="f3ab7-247">Controlled Adjoint</span></span>

<span data-ttu-id="f3ab7-248">Управляемая смежная версия операции указывает, как реализовать управляемую тактом версию примыкающей операции.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-248">The controlled adjoint version of an operation specifies how to implement a quantum-controlled version of the adjoint of the operation.</span></span>
<span data-ttu-id="f3ab7-249">Допускается указание операции без управляемой примыкающей версии; Например, операции измерения не имеют контролируемой версии, так как они не являются управляемыми и необратимыми.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-249">It is legal to specify an operation with no controlled adjoint version; for instance, measurement operations have no controlled adjoint version because they are neither controllable nor invertible.</span></span>

<span data-ttu-id="f3ab7-250">Управляемая примыкающая специализация для операции должна существовать только в том случае, если существует и смежная, и управляемая специализация.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-250">A controlled adjoint specialization for an operation needs to exist if and only if both an adjoint and a controlled specialization exist.</span></span> <span data-ttu-id="f3ab7-251">В этом случае определяется существование управляемой примыкающей специализации.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-251">In that case, the existence of the controlled adjoint specialization is inferred.</span></span> <span data-ttu-id="f3ab7-252">Если реализация не определена явно, то компиляция создает соответствующую специализацию.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-252">If no implementation is explicitly defined, the compile generates an appropriate specialization.</span></span>

<span data-ttu-id="f3ab7-253">Для операции, тело которой содержит вызовы других операций, не имеющих управляемой примыкающей версии, автоматическое создание примыкающей специализации, следующей за `invert` `distribute` директивой, или, невозможно `auto` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-253">For an operation whose body contains calls to other operations that do not have a controlled adjoint version, auto-generating an adjoint specialization following the `invert`, `distribute`, or `auto` directive is not possible.</span></span>


### <a name="type-compatibility"></a><span data-ttu-id="f3ab7-254">Совместимость типов</span><span class="sxs-lookup"><span data-stu-id="f3ab7-254">Type Compatibility</span></span>

<span data-ttu-id="f3ab7-255">Используйте операцию с дополнительным операторов в любом месте, где используется операция с меньшим числом операторов, но с одинаковой сигнатурой.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-255">Use an operation with additional functors supported anywhere you use an operation with fewer functors but the same signature.</span></span> <span data-ttu-id="f3ab7-256">Например, используйте операцию типа в `(Qubit => Unit is Adj)` любом месте, где используется операция типа `(Qubit => Unit)` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-256">For instance, use an operation of type `(Qubit => Unit is Adj)` anywhere you use an operation of type `(Qubit => Unit)`.</span></span>

<span data-ttu-id="f3ab7-257">Q#является *ковариантным* по отношению к вызываемым возвращаемым типам: вызываемый метод, возвращающий тип, `'A` совместим с вызываемым с тем же входным типом и типом результата, совместимым с `'A` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-257">Q# is *covariant* with respect to callable return types: a callable that returns a type `'A` is compatible with a callable with the same input type and a result type that is compatible with `'A` .</span></span>

<span data-ttu-id="f3ab7-258">Q#является *контравариантным* по отношению к типам входных данных: вызываемый тип, который принимает в `'A` качестве входных данных, совместим с вызываемым с тем же типом результата и типом входных данных, совместимым с `'A` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-258">Q# is *contravariant* with respect to input types: a callable that takes a type `'A` as input is compatible with a callable with the same result type and an input type that is compatible with `'A`.</span></span>

<span data-ttu-id="f3ab7-259">Это имеет значение, учитывая следующие определения:</span><span class="sxs-lookup"><span data-stu-id="f3ab7-259">That is, given the following definitions,</span></span>

```qsharp
operation Invert(qubits : Qubit[]) : Unit 
is Adj {...} 

operation ApplyUnitary(qubits : Qubit[]) : Unit 
is Adj + Ctl {...} 

function ConjugateInvertWith(
    inner : (Qubit[] => Unit is Adj),
    outer : (Qubit[] => Unit is Adj))
: (Qubit[] => Unit is Adj) {...}

function ConjugateUnitaryWith(
    inner : (Qubit[] => Unit is Adj + Ctl),
    outer : (Qubit[] => Unit is Adj))
: (Qubit[] => Unit is Adj + Ctl) {...}
```

<span data-ttu-id="f3ab7-260">Вы можете</span><span class="sxs-lookup"><span data-stu-id="f3ab7-260">you can</span></span>

- <span data-ttu-id="f3ab7-261">Вызовите функцию `ConjugateInvertWith` с `inner` аргументом либо `Invert` или `ApplyUnitary` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-261">Invoke the function `ConjugateInvertWith` with an `inner` argument of either `Invert` or `ApplyUnitary`.</span></span>
- <span data-ttu-id="f3ab7-262">Вызовите функцию `ConjugateUnitaryWith` с `inner` аргументом `ApplyUnitary` , но не `Invert` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-262">Invoke the function `ConjugateUnitaryWith` with an `inner` argument of `ApplyUnitary`, but not `Invert`.</span></span>
- <span data-ttu-id="f3ab7-263">Возврат значения типа `(Qubit[] => Unit is Adj + Ctl)` из `ConjugateInvertWith` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-263">Return a value of type `(Qubit[] => Unit is Adj + Ctl)` from `ConjugateInvertWith`.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f3ab7-264">Q#0,3 представил существенную разницу в поведении определяемых пользователем типов.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-264">Q# 0.3 introduced a significant difference in the behavior of user-defined types.</span></span>

<span data-ttu-id="f3ab7-265">Определяемые пользователем типы обрабатываются как упакованная версия базового типа, а не как подтип.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-265">User-defined types are treated as a wrapped version of the underlying type, rather than as a subtype.</span></span>
<span data-ttu-id="f3ab7-266">Это означает, что значение определяемого пользователем типа не может использоваться в тех случаях, когда предполагается, что значение базового типа равно.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-266">This means that a value of a user-defined type is not usable where you expect a value of the underlying type is.</span></span>


### <a name="conjugations"></a><span data-ttu-id="f3ab7-267">Лиц</span><span class="sxs-lookup"><span data-stu-id="f3ab7-267">Conjugations</span></span>

<span data-ttu-id="f3ab7-268">В отличие от классических битов освобождение памяти такта немного сложнее, так как в результате нежелательного сброса Кубитс может иметь нежелательные последствия для оставшихся вычислений, если Кубитс все еще запутанными.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-268">In contrast to classical bits, releasing quantum memory is slightly more involved since blindly resetting qubits can have undesired effects on the remaining computation if the qubits are still entangled.</span></span> <span data-ttu-id="f3ab7-269">Эти эффекты можно избежать, правильно выполнив вычисления перед освобождением памяти.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-269">These effects can be avoided by properly "undoing" performed computations prior to releasing the memory.</span></span> <span data-ttu-id="f3ab7-270">Общий шаблон в тактовых вычислениях, следовательно, является следующим:</span><span class="sxs-lookup"><span data-stu-id="f3ab7-270">A common pattern in quantum computing is hence the following:</span></span> 

```qsharp
operation ApplyWith<'T>(
    outerOperation : ('T => Unit is Adj), 
    innerOperation : ('T => Unit), 
    target : 'T) 
: Unit {

    outerOperation(target);
    innerOperation(target);
    Adjoint outerOperation(target);
}
```

<span data-ttu-id="f3ab7-271">Начиная с нашего выпуска 0,9, Q# поддерживает инструкцию конжугатион, которая реализует предыдущее преобразование.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-271">Starting with our 0.9 release, Q# supports a conjugation statement that implements the preceding transformation.</span></span> <span data-ttu-id="f3ab7-272">С помощью этой инструкции операция `ApplyWith` может быть реализована следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f3ab7-272">Using that statement, the operation `ApplyWith` can be implemented in the following way:</span></span>

```qsharp
operation ApplyWith<'T>(
    outerOperation : ('T => Unit is Adj), 
    innerOperation : ('T => Unit), 
    target : 'T) 
: Unit {

    within{ 
        outerOperation(target);
    }
    apply {
        innerOperation(target);
    }
}
```
<span data-ttu-id="f3ab7-273">Такой оператор конжугатион гораздо более полезен, если внешние и внутренние преобразования недоступны в качестве операций, а более удобны для описания блоком, состоящим из нескольких инструкций.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-273">Such a conjugation statement becomes far more useful if the outer and inner transformations are not readily available as operations but are instead more convenient to describe by a block consisting of several statements.</span></span> 

<span data-ttu-id="f3ab7-274">Обратное преобразование для инструкций, определенных в блоке внутри блока, автоматически создается компилятором и запускается после завершения блока Apply.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-274">The inverse transformation for the statements defined in the within-block is automatically generated by the compiler and run after the apply-block completes.</span></span>
<span data-ttu-id="f3ab7-275">Поскольку любые изменяемые переменные, используемые в качестве части блока in, не могут быть повторно привязаны в блоке применения, созданное преобразование гарантируется как прилегающие вычисления в блоке внутри блока.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-275">Since any mutable variables used as part of the within-block cannot be rebound in the apply-block, the generated transformation is guaranteed to be the adjoint of the computation in the within-block.</span></span> 


## <a name="defining-new-functions"></a><span data-ttu-id="f3ab7-276">Определение новых функций</span><span class="sxs-lookup"><span data-stu-id="f3ab7-276">Defining New Functions</span></span>

<span data-ttu-id="f3ab7-277">Функции являются исключительно детерминированными, классическими подпрограммыми в Q# , которые отличаются от операций тем, что они не могут иметь каких бы то ни было последствий, чем вычисление выходного значения.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-277">Functions are purely deterministic, classical routines in Q#, which are distinct from operations in that they are not allowed to have any effects beyond calculating an output value.</span></span>
<span data-ttu-id="f3ab7-278">В частности, функции не могут вызывать операции; Применяйте, выделяйте или позаимствование Кубитс; Примеры случайных чисел; или, в противном случае, зависит от состояния, превышающего входное значение функции.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-278">In particular, functions cannot call operations; act on, allocate, or borrow qubits; sample random numbers; or otherwise depend on state beyond the input value to a function.</span></span>
<span data-ttu-id="f3ab7-279">Как следствие, Q# функции являются *чисто*, в том, что они всегда сопоставляют одинаковые входные значения с одними и теми же выходными значениями.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-279">As a consequence, Q# functions are *pure*, in that they always map the same input values to the same output values.</span></span>
<span data-ttu-id="f3ab7-280">Такое поведение позволяет Q# компилятору безопасно изменять порядок и время вызова функций при создании специализаций операций.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-280">This behavior allows the Q# compiler to safely reorder how and when to call functions when generating operation specializations.</span></span>

<span data-ttu-id="f3ab7-281">Каждый Q# исходный файл может определять любое количество функций.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-281">Each Q# source file can define any number of functions.</span></span>
<span data-ttu-id="f3ab7-282">Имена функций должны быть уникальными в пределах пространства имен и не могут конфликтовать с именами операций или типов.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-282">Function names must be unique within a namespace and cannot conflict with operation or type names.</span></span>

<span data-ttu-id="f3ab7-283">Определение функции работает аналогично определению операции, за исключением того, что для функции нельзя определить ни прилегающие, ни контролируемые специализации.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-283">Defining a function works similarly to defining an operation, except that no adjoint or controlled specializations can be defined for a function.</span></span>
<span data-ttu-id="f3ab7-284">например</span><span class="sxs-lookup"><span data-stu-id="f3ab7-284">For instance:</span></span>

```qsharp
function Square(x : Double) : (Double) {
    return x * x;
}
```

<span data-ttu-id="f3ab7-285">or</span><span class="sxs-lookup"><span data-stu-id="f3ab7-285">or</span></span> 

```qsharp
function DotProduct(a : Double[], b : Double[]) : Double {
    if (Length(a) != Length(b)) {
        fail "Arrays are not compatible";
    }

    mutable accum = 0.0;
    for (i in 0..Length(a)-1) {
        set accum += a[i] * b[i];
    }
    return accum;
}
```

### <a name="classical-logic-in-functions--good"></a><span data-ttu-id="f3ab7-286">Классическая логика в функциях = = хорошее</span><span class="sxs-lookup"><span data-stu-id="f3ab7-286">Classical logic in functions == good</span></span>

<span data-ttu-id="f3ab7-287">Когда это возможно, полезно написать классическую логику с точки зрения функций, а не операций, чтобы операции могли использовать ее более эффективно.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-287">Whenever it is possible to do so, it is helpful to write out classical logic in terms of functions rather than operations so that operations can more readily use it.</span></span> <span data-ttu-id="f3ab7-288">Например, если вы написали предыдущее `Square` объявление в качестве *операции*, компилятор не сможет гарантировать, что его вызов с теми же входными данными получит одинаковые выходные данные.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-288">For example, if you had written the earlier `Square` declaration as an *operation*, then the compiler would not have been able to guarantee that calling it with the same input would consistently produce the same outputs.</span></span>

<span data-ttu-id="f3ab7-289">Чтобы подчеркнуть разницу между функциями и операциями, рассмотрим проблему классической выборки случайного числа в рамках Q# операции:</span><span class="sxs-lookup"><span data-stu-id="f3ab7-289">To underscore the difference between functions and operations, consider the problem of classically sampling a random number from within a Q# operation:</span></span>

```qsharp
operation U(target : Qubit) : Unit {

    let angle = RandomReal()
    Rz(angle, target)
}
```

<span data-ttu-id="f3ab7-290">Каждый раз `U` при вызове он имеет другое действие `target` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-290">Each time that `U` is called, it has a different action on `target`.</span></span>
<span data-ttu-id="f3ab7-291">В частности, компилятор не может гарантировать, что при добавлении `adjoint auto` объявления специализации в `U` , а затем `U(target); Adjoint U(target);` выступает в качестве удостоверения (т. е. без операции).</span><span class="sxs-lookup"><span data-stu-id="f3ab7-291">In particular, the compiler cannot guarantee that if you add an `adjoint auto` specialization declaration to `U`, then `U(target); Adjoint U(target);` acts as identity (that is, as a no-op).</span></span>
<span data-ttu-id="f3ab7-292">Это нарушает определение примыкающего, определенного в [векторах и матрицах](xref:microsoft.quantum.concepts.vectors), что позволяет компилятору автоматически формировать смежную специализацию в операции, при которой вызов операции <xref:microsoft.quantum.math.randomreal> приведет к нарушению гарантий, предоставляемых компилятором; <xref:microsoft.quantum.math.randomreal> — это операция, для которой не существует ни одной примыкающей или контролируемой версии.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-292">This violates the definition of the adjoint defined in [Vectors and Matrices](xref:microsoft.quantum.concepts.vectors), such that allowing the compiler to auto-generate an adjoint specialization in an operation where you call the operation <xref:microsoft.quantum.math.randomreal> would break the guarantees provided by the compiler; <xref:microsoft.quantum.math.randomreal> is an operation for which no adjoint or controlled version exists.</span></span>

<span data-ttu-id="f3ab7-293">С другой стороны, обеспечивая безопасность вызовов функций, таких как, `Square` и гарантирует, что компилятору нужно сохранить только входные данные, чтобы `Square` обеспечить стабильность его вывода.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-293">On the other hand, allowing function calls such as `Square` is safe, and assures the compiler that it only needs to preserve the input to `Square` to keep its output stable.</span></span>
<span data-ttu-id="f3ab7-294">Таким образом, изоляция максимально возможной логики функций позволяет легко повторно использовать эту логику в других функциях и операциях.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-294">Thus, isolating as much classical logic as possible into functions makes it easy to reuse that logic in other functions and operations alike.</span></span>


## <a name="generic-type-parameterized-callables"></a><span data-ttu-id="f3ab7-295">Универсальные вызываемые типы (параметризованные)</span><span class="sxs-lookup"><span data-stu-id="f3ab7-295">Generic (Type-Parameterized) Callables</span></span>

<span data-ttu-id="f3ab7-296">Многие функции и операции, которые вы можете определить, не сильно полагаются на типы входных данных, а только неявно используют их типы с помощью какой бы то ни было другой функции или операции.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-296">Many functions and operations that you might wish to define do not actually heavily rely on the types of their inputs, but rather only implicitly use their types via some other function or operation.</span></span>
<span data-ttu-id="f3ab7-297">Например, рассмотрим концепцию *Map* , общую для многих функциональных языков. При наличии функции $f (x) $ и коллекции значений $ \{ x_1, x_2, \дотс, x_n \} $, Map возвращает новую коллекцию $ \{ f (x_1), f (x_2), \дотс, f (x_n) \} $.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-297">For example, consider the *map* concept common to many functional languages; given a function $f(x)$ and a collection of values $\{x_1, x_2, \dots, x_n\}$, map returns a new collection $\{f(x_1), f(x_2), \dots, f(x_n)\}$.</span></span>
<span data-ttu-id="f3ab7-298">Чтобы реализовать это в Q# , воспользуйтесь преимуществами того факта, что функции являются первыми классами.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-298">To implement this in Q#, take advantage of the fact that functions are first class.</span></span>
<span data-ttu-id="f3ab7-299">Ниже приведен краткий пример `Map` использования `T` в качестве заполнителя для определения необходимых типов.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-299">Here is a quick example of `Map`, using `T` as a placeholder while you figure out what types you need.</span></span>

```qsharp
function Map(fn : (T -> T), values : T[]) : T[] {
    mutable mappedValues = new T[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

<span data-ttu-id="f3ab7-300">Обратите внимание, что эта функция выглядит почти так же, независимо от фактических типов, которые вы заменяете.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-300">Note that this function looks very much the same no matter what actual types you substitute in.</span></span>
<span data-ttu-id="f3ab7-301">, Например, карту из целых чисел в пол, похожа на карту из чисел с плавающей запятой в строки:</span><span class="sxs-lookup"><span data-stu-id="f3ab7-301">A map from integers to Paulis, for instance, looks much the same as a map from floating-point numbers to strings:</span></span>

```qsharp
function MapIntsToPaulis(fn : (Int -> Pauli), values : Int[]) : Pauli[] {
    mutable mappedValues = new Pauli[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}

function MapDoublesToStrings(fn : (Double -> String), values : Double[]) : String[] {
    mutable mappedValues = new String[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

<span data-ttu-id="f3ab7-302">В принципе, можно написать версию `Map` для каждой пары типов, которую вы сталкиваетесь, но в этом случае возникают некоторые сложности.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-302">In principle, you could write a version of `Map` for every pair of types that you encounter, but this introduces several difficulties.</span></span>
<span data-ttu-id="f3ab7-303">Например, если обнаружена ошибка в `Map` , необходимо обеспечить единообразное применение исправления во всех версиях `Map` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-303">For instance, if you find a bug in `Map`, then you must ensure that the fix is applied uniformly across all versions of `Map`.</span></span>
<span data-ttu-id="f3ab7-304">Более того, при создании нового кортежа или определяемого пользователем типа необходимо также создать новый объект `Map` для перехода с новым типом.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-304">Moreover, if you construct a new tuple or UDT, then you must now also construct a new `Map` to go along with the new type.</span></span>
<span data-ttu-id="f3ab7-305">Хотя это алгоритмизируемым для небольшого количества таких функций, поскольку вы соберете больше функций той же формы, что и `Map` , стоимость введения новых типов становится неоправданной в достаточно коротком порядке.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-305">While this is tractable for a small number of such functions, as you collect more and more functions of the same form as `Map`, the cost of introducing new types becomes unreasonably large in fairly short order.</span></span>

<span data-ttu-id="f3ab7-306">Тем не менее, значительная часть этой сложности возникает из-за того, что компилятор не предоставил сведения, необходимые для того, чтобы понять, как связаны разные версии `Map` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-306">However, much of this difficulty results from the fact that you have not given the compiler the information it needs to recognize how the different versions of `Map` are related.</span></span>
<span data-ttu-id="f3ab7-307">Фактически необходимо, чтобы компилятор рассматривал `Map` как часть математических функций от Q# *типов* до Q# функций.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-307">Effectively, you want the compiler to treat `Map` as some kind of mathematical function from Q# *types* to Q# functions.</span></span>

<span data-ttu-id="f3ab7-308">Q#Формализация этого понятия позволяет функциям и операциям иметь *Параметры типа*, а также их обычные параметры кортежа.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-308">Q# formalizes this notion by allowing functions and operations to have *type parameters*, as well as their ordinary tuple parameters.</span></span>
<span data-ttu-id="f3ab7-309">В предыдущих примерах вы хотели бы представить, `Map` что параметры типа имеют `Int, Pauli` в первом случае и во `Double, String` втором случае.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-309">In the previous examples, you wish to think of `Map` as having type parameters `Int, Pauli` in the first case and `Double, String` in the second case.</span></span>
<span data-ttu-id="f3ab7-310">В большинстве случаев используйте эти параметры типа, как если бы они были обычными типами.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-310">For the most part, use these type parameters as though they were ordinary types.</span></span> <span data-ttu-id="f3ab7-311">Используйте значения параметров типа, чтобы создать массивы и кортежи, вызывайте функции и операции и присвойте их обычным или изменяемым переменным.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-311">Use values of type parameters to make arrays and tuples, call functions and operations, and assign to ordinary or mutable variables.</span></span>

> [!NOTE]
> <span data-ttu-id="f3ab7-312">Самый крайний случай косвенной зависимости заключается в том, что Кубитс, где Q# программа не может напрямую полагаться на структуру `Qubit` типа, но **должна** передавать подобные типы другим операциям и функциям.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-312">The most extreme case of indirect dependence is that of qubits, where a Q# program cannot directly rely on the structure of the `Qubit` type but **must** pass such types to other operations and functions.</span></span>

<span data-ttu-id="f3ab7-313">Вернувшись к предыдущему примеру, вы увидите, что должны `Map` иметь параметры типа, один для представления входных данных `fn` и один для представления выходных данных `fn` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-313">Returning to the earlier example, then, you see that `Map` needs to have type parameters, one to represent the input to `fn` and one to represent the output from `fn`.</span></span>
<span data-ttu-id="f3ab7-314">В Q# это написано путем добавления угловых скобок (то есть `<>` не Бракетс $ \бракет {} $!) после имени функции или операции в ее объявлении, а также путем перечисления каждого параметра типа.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-314">In Q#, this is written by adding angle brackets (that's `<>`, not brakets $\braket{}$!) after the name of a function or operation in its declaration, and by listing each type parameter.</span></span>
<span data-ttu-id="f3ab7-315">Имя каждого параметра типа должно начинаться с такта `'` , что означает, что это параметр типа, а не обычный тип (также известен как *конкретный* тип).</span><span class="sxs-lookup"><span data-stu-id="f3ab7-315">The name of each type parameter must start with a tick `'`, indicating that it is a type parameter and not a ordinary type (also known as a *concrete* type).</span></span>
<span data-ttu-id="f3ab7-316">Таким образом, `Map` записывается:</span><span class="sxs-lookup"><span data-stu-id="f3ab7-316">Thus, `Map`, is written:</span></span>

```qsharp
function Map<'Input, 'Output>(fn : ('Input -> 'Output), values : 'Input[]) : 'Output[] {
    mutable mappedValues = new 'Output[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

<span data-ttu-id="f3ab7-317">Обратите внимание, что определение `Map<'Input, 'Output>` выглядит очень похоже на версии превиоиус.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-317">Note that the definition of `Map<'Input, 'Output>` looks extremely similar to the previoius versions.</span></span>
<span data-ttu-id="f3ab7-318">Единственное отличие заключается в том, что вы явным образом сообщили компилятору, что `Map` не зависит от того `'Input` , что и `'Output` есть, но работает для всех двух типов, напрямую используя их `fn` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-318">The only difference is that you have explicitly informed the compiler that `Map` doesn't directly depend on what `'Input` and `'Output` are, but works for any two types by using them indirectly through `fn`.</span></span>
<span data-ttu-id="f3ab7-319">Определив `Map<'Input, 'Output>` таким образом, вы можете вызвать его, как будто это обычная функция:</span><span class="sxs-lookup"><span data-stu-id="f3ab7-319">Once you have defined `Map<'Input, 'Output>` in this way, you can call it as though it was an ordinary function:</span></span>

```qsharp
// Represent Z₀ Z₁ X₂ Y₃ as a list of ints.
let ints = [3, 3, 1, 2];
// Here, assume IntToPauli : Int -> Pauli
// looks up PauliI by 0, PauliX by 1, so forth.
let paulis = Map(IntToPauli, ints);
```

> [!TIP]
> <span data-ttu-id="f3ab7-320">Написание универсальных функций и операций — это одно из мест, где «кортеж — в кортеже» — очень полезный способ подумать о Q# функциях и операциях.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-320">Writing generic functions and operations is one place where "tuple-in tuple-out" is a very useful way to think about Q# functions and operations.</span></span>
> <span data-ttu-id="f3ab7-321">Поскольку каждая функция принимает ровно один вход и возвращает ровно один выход, вход типа `'T -> 'U` соответствует *любой* Q# функции.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-321">Since every function takes exactly one input and returns exactly one output, an input of type `'T -> 'U` matches *any* Q# function whatsoever.</span></span>
> <span data-ttu-id="f3ab7-322">Аналогичным образом можно передать любую операцию в входные данные типа `'T => 'U` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-322">Similarly, you can pass any operation to an input of type `'T => 'U`.</span></span>

<span data-ttu-id="f3ab7-323">Во втором примере рассмотрим задачу написания функции, возвращающей композицию двух других функций:</span><span class="sxs-lookup"><span data-stu-id="f3ab7-323">As a second example, consider the challenge of writing a function that returns the composition of two other functions:</span></span>

```qsharp
function ComposeImpl(outerFn : (B -> C), innerFn : (A -> B), input : A) : C {
    return outerFn(innerFn(input));
}

function Compose(outerFn : (B -> C), innerFn : (A -> B)) : (A -> C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

<span data-ttu-id="f3ab7-324">Здесь необходимо точно указать, что, `A` `B` и, и `C` , следовательно, существенно ограничить служебную программу нашей новой `Compose` функции.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-324">Here, you must specify exactly what `A`, `B`, and `C` are, hence severely limiting the utility of our new `Compose` function.</span></span>
<span data-ttu-id="f3ab7-325">В конце концов, `Compose` только они зависят от `A` , `B` и `C` *через* `innerFn` и `outerFn` .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-325">After all, `Compose` only depends on `A`, `B`, and `C` *via* `innerFn` and `outerFn`.</span></span>
<span data-ttu-id="f3ab7-326">В качестве альтернативы можно добавить параметры типа к `Compose` , которые указывают, что он работает для *всех* `A` , `B` и `C` , пока эти параметры соответствуют ожидаемым `innerFn` и `outerFn` :</span><span class="sxs-lookup"><span data-stu-id="f3ab7-326">As an alternative, then, you can add type parameters to `Compose` that indicate that it works for *any* `A`, `B`, and `C`, so long as these parameters match those expected by `innerFn` and `outerFn`:</span></span>

```qsharp
function ComposeImpl<'A, 'B, 'C>(outerFn : ('B -> 'C), innerFn : ('A -> 'B), input : 'A) : 'C {
    return outerFn(innerFn(input));
}

function Compose<'A, 'B, 'C>(outerFn : ('B -> 'C), innerFn : ('A -> 'B)) : ('A -> 'C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

<span data-ttu-id="f3ab7-327">Q#Стандартные библиотеки предоставляют ряд таких операций и функций с параметризованными параметрами, которые упрощают выражать поток управления более высокого порядка.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-327">The Q# standard libraries provide a range of such type-parameterized operations and functions to make higher-order control flow easier to express.</span></span>
<span data-ttu-id="f3ab7-328">Они рассматриваются далее в [ Q# стандартном руководству по библиотеке](xref:microsoft.quantum.libraries.standard.intro).</span><span class="sxs-lookup"><span data-stu-id="f3ab7-328">These are discussed further in the [Q# standard library guide](xref:microsoft.quantum.libraries.standard.intro).</span></span>


## <a name="callables-as-first-class-values"></a><span data-ttu-id="f3ab7-329">Вызываемые как значения первого класса</span><span class="sxs-lookup"><span data-stu-id="f3ab7-329">Callables as First-Class Values</span></span>

<span data-ttu-id="f3ab7-330">Одной из важнейших методик для реализации потока управления и классической логики с помощью функций, а не операций является использование этих операций и функций в Q# — *первый класс*.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-330">One critical technique for reasoning about control flow and classical logic using functions rather than operations is to utilize that operations and functions in Q# are *first-class*.</span></span>
<span data-ttu-id="f3ab7-331">То есть все значения на языке имеют свое право.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-331">That is, they are each values in the language in their own right.</span></span>
<span data-ttu-id="f3ab7-332">Например, следующий код является вполне допустимым Q# , если немного косвенно:</span><span class="sxs-lookup"><span data-stu-id="f3ab7-332">For instance, the following is perfectly valid Q# code, if a little indirect:</span></span>

```qsharp
operation FirstClassExample(target : Qubit) : Unit {
    let ourH = H;
    ourH(target);
}
```

<span data-ttu-id="f3ab7-333">Значение переменной `ourH` в предыдущем фрагменте кода — это операция <xref:microsoft.quantum.intrinsic.h> , которая позволяет вызывать это значение, как любая другая операция.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-333">The value of the variable `ourH` in the previous snippet is then the operation <xref:microsoft.quantum.intrinsic.h>, such that you can call that value like any other operation.</span></span>
<span data-ttu-id="f3ab7-334">Благодаря этой возможности можно писать операции, которые принимают операции в качестве части их входных данных, формируя основные понятия потока управления более высокого порядка.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-334">With this ability, you can write operations that take operations as a part of their input, forming higher-order control flow concepts.</span></span>
<span data-ttu-id="f3ab7-335">Например, можно представить, что нужно «возкубит» операцию, применив ее дважды к той же цели.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-335">For instance, you could imagine wanting to "square" an operation by applying it twice to the same target qubit.</span></span>

```qsharp
operation ApplyTwice(op : (Qubit => Unit), target : Qubit) : Unit {
    op(target);
    op(target);
}
```

### <a name="returning-operations-from-a-function"></a><span data-ttu-id="f3ab7-336">Возвращение операций из функции</span><span class="sxs-lookup"><span data-stu-id="f3ab7-336">Returning operations from a function</span></span>

<span data-ttu-id="f3ab7-337">Важно подчеркнуть, что можно также возвращать операции как часть выходных данных, что позволяет изолировать некоторые виды классической условной логики в качестве классической функции, которая возвращает описание тактовой программы в форме операции.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-337">It's important to emphasize that you can also return operations as a part of outputs, such that you can isolate some kinds of classical conditional logic as a classical function, which returns a description of a quantum program in the form of an operation.</span></span>
<span data-ttu-id="f3ab7-338">В качестве простого примера рассмотрим пример использования телепередачи, в котором сторона, получающая 2-разрядное классическое сообщение, должна использовать сообщение для декодирования их кубит в соответствующее состояние в режиме «в Организации».</span><span class="sxs-lookup"><span data-stu-id="f3ab7-338">As a simple example, consider the teleportation example, in which the party receiving a two-bit classical message needs to use the message to decode their qubit into the proper teleported state.</span></span>
<span data-ttu-id="f3ab7-339">Это можно написать с точки зрения функции, которая принимает эти два классических битов и возвращает правильную операцию декодирования.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-339">You could write this in terms of a function that takes those two classical bits and returns the proper decoding operation.</span></span>

```qsharp
function TeleporationDecoderForMessage(hereBit : Result, thereBit : Result)
: (Qubit => Unit is Adj + Ctl) {

    if (hereBit == Zero && thereBit == Zero) {
        return I;
    } elif (hereBit == One && thereBit == Zero) {
        return X;
    } elif (hereBit == Zero && thereBit == One) {
        return Z;
    } else {
        return Y;
    }
}
```

<span data-ttu-id="f3ab7-340">Эта новая функция действительно является функцией. в этом случае, если вы вызываете ее с теми же значениями `hereBit` и `thereBit` , вы всегда получаете ту же операцию.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-340">This new function is indeed a function, in that if you call it with the same values of `hereBit` and `thereBit`, you always get back the same operation.</span></span>
<span data-ttu-id="f3ab7-341">Таким образом, декодер может безопасно выполняться внутри операций, не прибегая к попричине того, как логика декодирования взаимодействует с определениями различных специализаций операций.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-341">Thus, the decoder can safely run inside operations without having to reason about how the decoding logic interacts with the definitions of the different operation specializations.</span></span>
<span data-ttu-id="f3ab7-342">То есть классическая логика внутри функции изолирована, что гарантирует компилятору, что вызов функции может быть переупорядочен с помощью импунити, пока сохраняются входные данные.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-342">That is, the classical logic inside a function is isolated, guaranteeing to the compiler that the function call can be reordered with impunity so long as the input is preserved.</span></span>


## <a name="partial-application"></a><span data-ttu-id="f3ab7-343">Частичное приложение</span><span class="sxs-lookup"><span data-stu-id="f3ab7-343">Partial Application</span></span>

<span data-ttu-id="f3ab7-344">Вы можете значительно увеличить количество функций, возвращающих операции с помощью *частичного приложения*, в котором вы предоставляете одну или несколько частей входных данных функции или операции, не вызывая их фактически.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-344">You can do significantly more with functions that return operations by using *partial application*, in which you provide one or more parts of the input to a function or operation without actually calling it.</span></span> <span data-ttu-id="f3ab7-345">В приведенном выше `ApplyTwice` примере можно указать, что вы не хотите указывать, сразу же, к которому кубит входную операцию:</span><span class="sxs-lookup"><span data-stu-id="f3ab7-345">In the earlier `ApplyTwice` example, you can indicate that you don't want to specify, right away, to which qubit the input operation should apply:</span></span>

```qsharp
operation PartialApplicationExample(op : (Qubit => Unit), target : Qubit) : Unit {
    let twiceOp = ApplyTwice(op, _);
    twiceOp(target);
}
```

<span data-ttu-id="f3ab7-346">В этом случае локальная переменная `twiceOp` содержит операцию частичного применения `ApplyTwice(op, _)` , где `_` указывает части входных данных, которые еще не были указаны.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-346">In this case, the local variable `twiceOp` holds the partially applied operation `ApplyTwice(op, _)`, where `_` indicates parts of the input that have not yet been specified.</span></span>
<span data-ttu-id="f3ab7-347">При вызове `twiceOp` в следующей строке вы передаете в качестве входных данных частично примененную операцию все оставшиеся части входных данных в исходную операцию.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-347">When you call `twiceOp` in the next line, you pass as input to the partially applied operation all of the remaining parts of the input to the original operation.</span></span>
<span data-ttu-id="f3ab7-348">Таким образом, предыдущий фрагмент фактически аналогичен вызову `ApplyTwice(op, target)` напрямую, метод Save для того, что вы предоставили новую локальную переменную, чтобы можно было отложить вызов, предоставляя некоторые части входных данных.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-348">Thus, the previous snippet is effectively identical to having called `ApplyTwice(op, target)` directly, save for that you have introduced a new local variable so you can delay the call while providing some parts of the input.</span></span>

<span data-ttu-id="f3ab7-349">Так как операция, которая была частично применена, фактически не вызывается до тех пор, пока не будет предоставлен весь ввод, можно безопасно частично применить операции даже из функций.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-349">Since an operation that has been partially applied is not actually called until its entire input has been provided, you can safely partially apply operations even from within functions.</span></span>

```qsharp
function SquareOperation(op : (Qubit => Unit)) : (Qubit => Unit) {
    return ApplyTwice(op, _);
}
```

<span data-ttu-id="f3ab7-350">В принципе, классическая логика внутри `SquareOperation` может быть гораздо более сложной, но она по-прежнему изолирована от остальной части операции с помощью гарантий, что компилятор может предложить функции.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-350">In principle, the classical logic within `SquareOperation` could have been much more involved, but it is still isolated from the rest of an operation by the guarantees that the compiler can offer about functions.</span></span> <span data-ttu-id="f3ab7-351">Q#Стандартная библиотека использует этот подход для выражения классического потока управления так, чтобы можно было легко использовать его в качестве генератора.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-351">The Q# standard library uses this approach throughout for expressing classical control flow in a way that quantum programs can readily use.</span></span>


## <a name="recursion"></a><span data-ttu-id="f3ab7-352">Рекурсия</span><span class="sxs-lookup"><span data-stu-id="f3ab7-352">Recursion</span></span>

<span data-ttu-id="f3ab7-353">Q#вызываемые могут быть прямо или косвенно рекурсивными.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-353">Q# callables are allowed to be directly or indirectly recursive.</span></span>
<span data-ttu-id="f3ab7-354">Это значит, что операция или функция может вызвать саму себя или вызвать другой вызываемый метод, который напрямую или косвенно вызывает вызываемую операцию.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-354">That is, an operation or function can call itself, or it can call another callable that directly or indirectly calls the callable operation.</span></span>

<span data-ttu-id="f3ab7-355">Однако существует два важных комментария об использовании рекурсии.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-355">There are two important comments about the use of recursion, however:</span></span>

- <span data-ttu-id="f3ab7-356">Использование рекурсии в операциях, скорее всего, мешает некоторым оптимизациям.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-356">The use of recursion in operations is likely to interfere with certain optimizations.</span></span>
  <span data-ttu-id="f3ab7-357">Эти помехи могут оказать значительное влияние на время выполнения алгоритма.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-357">This interference can have a substantial impact on the execution time of the algorithm.</span></span>
- <span data-ttu-id="f3ab7-358">При запуске на фактическом устройстве-такте пространство стека может быть ограничено, так что глубокая рекурсия может привести к ошибке времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-358">When running on an actual quantum device, stack space might be limited, and so deep recursion can lead to a runtime error.</span></span>
  <span data-ttu-id="f3ab7-359">В частности, Q# компилятор и среда выполнения не выявляет и не оптимизируют заключительную рекурсию.</span><span class="sxs-lookup"><span data-stu-id="f3ab7-359">In particular, the Q# compiler and runtime do not identify and optimize tail recursion.</span></span>

## <a name="next-steps"></a><span data-ttu-id="f3ab7-360">Дальнейшие шаги</span><span class="sxs-lookup"><span data-stu-id="f3ab7-360">Next steps</span></span>

<span data-ttu-id="f3ab7-361">Сведения о [переменных](xref:microsoft.quantum.guide.variables) в Q# .</span><span class="sxs-lookup"><span data-stu-id="f3ab7-361">Learn about [Variables](xref:microsoft.quantum.guide.variables) in Q#.</span></span>