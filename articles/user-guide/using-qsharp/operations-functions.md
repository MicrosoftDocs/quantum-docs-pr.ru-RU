---
title: 'Операции и функции в Q #'
description: Определение и вызов операций и функций, а также управляемых и примыкающих специализаций операций.
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.operationsfunctions
ms.openlocfilehash: bc9695b85b68807801225ccbc903a4622b450768
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2020
ms.locfileid: "83431076"
---
# <a name="operations-and-functions-in-q"></a><span data-ttu-id="0be70-103">Операции и функции в Q #</span><span class="sxs-lookup"><span data-stu-id="0be70-103">Operations and Functions in Q#</span></span>

## <a name="defining-new-operations"></a><span data-ttu-id="0be70-104">Определение новых операций</span><span class="sxs-lookup"><span data-stu-id="0be70-104">Defining New Operations</span></span>

<span data-ttu-id="0be70-105">Операции — это ядро Q #.</span><span class="sxs-lookup"><span data-stu-id="0be70-105">Operations are the core of Q#.</span></span>
<span data-ttu-id="0be70-106">После объявления их можно вызывать из классических приложений .NET, например, с помощью симулятора или других операций в Q #.</span><span class="sxs-lookup"><span data-stu-id="0be70-106">Once declared, they can either be called from classical .NET applications, e.g., using a simulator, or by other operations within Q#.</span></span>
<span data-ttu-id="0be70-107">Каждая операция, определенная в Q #, может затем вызывать любое количество других операций, включая встроенные внутренние операции, определенные в языке.</span><span class="sxs-lookup"><span data-stu-id="0be70-107">Each operation defined in Q# may then call any number of other operations, including the built-in intrinsic operations defined by the language.</span></span> <span data-ttu-id="0be70-108">Конкретный способ определения этих внутренних операций зависит от целевого компьютера.</span><span class="sxs-lookup"><span data-stu-id="0be70-108">The particular way in which these intrinsic operations are defined depends on the target machine.</span></span>
<span data-ttu-id="0be70-109">При компиляции каждая операция представляется как тип класса .NET, который можно предоставить целевым компьютерам.</span><span class="sxs-lookup"><span data-stu-id="0be70-109">When compiled, each operation is represented as a .NET class type that can be provided to target machines.</span></span>

<span data-ttu-id="0be70-110">Каждый исходный файл Q # может определять любое количество операций.</span><span class="sxs-lookup"><span data-stu-id="0be70-110">Each Q# source file may define any number of operations.</span></span>
<span data-ttu-id="0be70-111">Имена операций должны быть уникальными в пределах пространства имен и могут не конфликтовать с именами типа или функции.</span><span class="sxs-lookup"><span data-stu-id="0be70-111">Operation names must be unique within a namespace and may not conflict with type or function names.</span></span>

<span data-ttu-id="0be70-112">Объявление операции состоит из ключевого слова `operation` , за которым следует символ, который представляет собой имя операции, кортеж типизированного идентификатора, определяющий аргументы для операции, двоеточие `:` , аннотацию типа, которая описывает тип результата операции, при необходимости заметку с характеристиками операции, открывающую фигурную скобку `{` , текст объявления операции и окончательную закрывающую фигурную скобку `}` .</span><span class="sxs-lookup"><span data-stu-id="0be70-112">An operation declaration consists of the keyword `operation`, followed by the symbol that is the operation's name, a typed identifier tuple that defines the arguments to the operation, a colon `:`, a type annotation that describes the operation's result type, optionally an annotation with the operation characteristics, an open brace `{`, the body of the operation declaration, and a final closing brace `}`.</span></span>

<span data-ttu-id="0be70-113">Каждая операция принимает входные данные, создает выход и задает реализацию для одной или нескольких специализаций операций.</span><span class="sxs-lookup"><span data-stu-id="0be70-113">Each operation takes an input, produces an output, and specifies the implementation for one or more operation specializations.</span></span>
<span data-ttu-id="0be70-114">Ниже описаны возможные специализации и способы их определения и вызова.</span><span class="sxs-lookup"><span data-stu-id="0be70-114">The possible specializations, and how to define/call them, are detailed further below.</span></span>
<span data-ttu-id="0be70-115">Сейчас рассмотрим следующую операцию, которая определяет только специализацию тела по умолчанию и принимает одну кубит в качестве входных данных, а затем вызывает встроенную <xref:microsoft.quantum.intrinsic.x> операцию над этими входными данными:</span><span class="sxs-lookup"><span data-stu-id="0be70-115">For now, consider the following operation, which defines only a default body specialization and takes a single qubit as its input, then calls the built-in <xref:microsoft.quantum.intrinsic.x> operation on that input:</span></span>

```qsharp
operation BitFlip(target : Qubit) : Unit {
    X(target);
}
```

<span data-ttu-id="0be70-116">Ключевое слово `operation` начинается с определения операции, за которым следует имя; здесь, `BitFlip` .</span><span class="sxs-lookup"><span data-stu-id="0be70-116">The keyword `operation` begins the operation definition, and is followed by the name; here, `BitFlip`.</span></span>
<span data-ttu-id="0be70-117">Далее тип входных данных определяется как `Qubit` , вместе с именем `target` для ссылки на входные данные в новой операции.</span><span class="sxs-lookup"><span data-stu-id="0be70-117">Next, the type of the input is defined as `Qubit`, along with a name `target` for referring to the input within the new operation.</span></span>
<span data-ttu-id="0be70-118">Аналогично, `Unit` определяет, что выходные данные операции пусты.</span><span class="sxs-lookup"><span data-stu-id="0be70-118">Similarly, the `Unit` defines that the operation's output is empty.</span></span>
<span data-ttu-id="0be70-119">Он используется аналогично `void` в C# и других императивных языках и эквивалентен `unit` в F # и других функциональных языках.</span><span class="sxs-lookup"><span data-stu-id="0be70-119">This is used similarly to `void` in C# and other imperative languages, and is equivalent to `unit` in F# and other functional languages.</span></span>

<span data-ttu-id="0be70-120">Операции также могут возвращать более интересные типы `Unit` , чем.</span><span class="sxs-lookup"><span data-stu-id="0be70-120">Operations can also return more interesting types than `Unit`.</span></span>
<span data-ttu-id="0be70-121">Например, <xref:microsoft.quantum.intrinsic.m> операция возвращает выходные данные типа `Result` , представляющие выполнение измерения.</span><span class="sxs-lookup"><span data-stu-id="0be70-121">For instance, the <xref:microsoft.quantum.intrinsic.m> operation returns an output of type `Result`, representing having performed a measurement.</span></span> <span data-ttu-id="0be70-122">Можно либо передать выходные данные операции в другую операцию, либо использовать ее с `let` ключевым словом для определения новой переменной.</span><span class="sxs-lookup"><span data-stu-id="0be70-122">We can either pass the output from an operation to another operation, or can use it with the `let` keyword to define a new variable.</span></span>

<span data-ttu-id="0be70-123">Это позволяет представить классические вычисления, взаимодействующие с операциями тактов на низком уровне, например в очень [плотной кодировке](https://github.com/microsoft/QuantumKatas/tree/master/SuperdenseCoding):</span><span class="sxs-lookup"><span data-stu-id="0be70-123">This allows for representing classical computation that interacts with quantum operations at a low level, such as in [superdense coding](https://github.com/microsoft/QuantumKatas/tree/master/SuperdenseCoding):</span></span>

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
> <span data-ttu-id="0be70-124">Каждая операция в Q # принимает ровно один вход и возвращает ровно один выход.</span><span class="sxs-lookup"><span data-stu-id="0be70-124">Each operation in Q# takes exactly one input and returns exactly one output.</span></span>
> <span data-ttu-id="0be70-125">После этого несколько входов и выходов представляются с помощью *кортежей*, которые собираются несколько значений вместе в одно значение.</span><span class="sxs-lookup"><span data-stu-id="0be70-125">Multiple inputs and outputs are then represented using *tuples*, which collect multiple values together into a single value.</span></span>
> <span data-ttu-id="0be70-126">В неформальном случае мы говорим, что Q # — это «кортеж в кортеже».</span><span class="sxs-lookup"><span data-stu-id="0be70-126">Informally, we say that Q# is a "tuple-in tuple-out" language.</span></span>
> <span data-ttu-id="0be70-127">После этого `()` следует считать "пустой" кортеж с типом `Unit` .</span><span class="sxs-lookup"><span data-stu-id="0be70-127">Following this concept, `()` should then be read as the "empty" tuple, which has the type `Unit`.</span></span>


## <a name="controlled-and-adjoint-operations"></a><span data-ttu-id="0be70-128">Контролируемые и смежные операции</span><span class="sxs-lookup"><span data-stu-id="0be70-128">Controlled and Adjoint Operations</span></span>

<span data-ttu-id="0be70-129">Если операция реализует единое преобразование, как в случае с множеством операций в Q #, то можно определить, как работает операция при *аджоинтед* или *управлении*.</span><span class="sxs-lookup"><span data-stu-id="0be70-129">If an operation implements a unitary transformation, as is the case for many operations in Q#, then it is possible to define how the operation acts when *adjointed* or *controlled*.</span></span> <span data-ttu-id="0be70-130">В *примыкающей* специализации операции указывается, как действует "Инверсия" операции, а *управляемая* Специализация определяет, как работает операция, когда ее приложение записывается в состояние конкретного регистра такта.</span><span class="sxs-lookup"><span data-stu-id="0be70-130">An *adjoint* specialization of an operation specifies how the "inverse" of the operation acts, while a *controlled* specialization specifies how an operation acts when its application is conditioned on the state of a particular quantum register.</span></span>

<span data-ttu-id="0be70-131">Аджоинтсие операций с тактами крайне важно для многих аспектов тактовых вычислений.</span><span class="sxs-lookup"><span data-stu-id="0be70-131">Adjoints of quantum operations are crucial to many aspects of quantum computing.</span></span> <span data-ttu-id="0be70-132">Далее, в разделе [лиц](#conjugations) , вы найдете одну из таких ситуаций, обсуждаемую вместе с полезным приемом программирования Q #.</span><span class="sxs-lookup"><span data-stu-id="0be70-132">Further below, in the [Conjugations](#conjugations) section, you will find one such situation discussed alongside a useful Q# programming technique.</span></span>

<span data-ttu-id="0be70-133">Управляемая версия операции — это новая операция, которая фактически применяет базовую операцию только в том случае, если все элементы управления Кубитс находятся в указанном состоянии.</span><span class="sxs-lookup"><span data-stu-id="0be70-133">The controlled version of an operation is a new operation that effectively applies the base operation only if all of the control qubits are in a specified state.</span></span>
<span data-ttu-id="0be70-134">Если элемент управления Кубитс в самом положении, то базовая операция применяется к соответствующей части детального размещения.</span><span class="sxs-lookup"><span data-stu-id="0be70-134">If the control qubits are in superposition, then the base operation is applied coherently to the appropriate part of the superposition.</span></span>
<span data-ttu-id="0be70-135">Поэтому управляемые операции часто используются для создания замкнутые.</span><span class="sxs-lookup"><span data-stu-id="0be70-135">Thus, controlled operations are often used to generate entanglement.</span></span>

<span data-ttu-id="0be70-136">Естественно, также может существовать *управляемая примыкающая* специализация, указывающая управляемое приложение для примыкающей операции.</span><span class="sxs-lookup"><span data-stu-id="0be70-136">Naturally, a *controlled adjoint* specialization could exist as well, specifying the controlled application of an operation's adjoint.</span></span>

> [!NOTE]
> <span data-ttu-id="0be70-137">Если $U $ является единым преобразованием, реализованным операцией `U` , то `Adjoint U` представляет собой единое преобразование $U ^ \дагжер $, которое является комплексно-сопряженным преобразованием.</span><span class="sxs-lookup"><span data-stu-id="0be70-137">If $U$ is the unitary transformation implemented by an operation `U`, then `Adjoint U` represents the unitary transformation $U^\dagger$, which is the complex conjugate transpose.</span></span>
> <span data-ttu-id="0be70-138">Успешное применение операции, а затем ее примыкающая к состоянию оставляет состояние без изменений, как показано на тот факт, что $UU ^ \дагжер = U ^ \дагжер U = \ид $, матрица Identity.</span><span class="sxs-lookup"><span data-stu-id="0be70-138">Successively applying an operation and then its adjoint to a state leaves the state unchanged, as illustrated by the fact that $UU^\dagger = U^\dagger U = \id$, the identity matrix.</span></span>
> <span data-ttu-id="0be70-139">Единое представление управляемой операции немного сложнее, но дополнительные сведения см. в разделе [концепции тактовых вычислений: несколько Кубитс](xref:microsoft.quantum.concepts.multiple-qubits).</span><span class="sxs-lookup"><span data-stu-id="0be70-139">The unitary representation of a controlled operation is slightly more nuanced, but you can find more details at [Quantum computing concepts: multiple qubits](xref:microsoft.quantum.concepts.multiple-qubits).</span></span>

<span data-ttu-id="0be70-140">В следующем разделе описывается, как вызывать эти различные специализации в коде Q #.</span><span class="sxs-lookup"><span data-stu-id="0be70-140">The following section describes how to call these various specializations in your Q# code.</span></span>
<span data-ttu-id="0be70-141">Ниже мы подробно расскажу, как определить операции для их поддержки.</span><span class="sxs-lookup"><span data-stu-id="0be70-141">Below, we detail how to define operations to support them.</span></span>

### <a name="calling-operation-specializations"></a><span data-ttu-id="0be70-142">Действия при вызове специализаций операций</span><span class="sxs-lookup"><span data-stu-id="0be70-142">Calling operation specializations</span></span>

<span data-ttu-id="0be70-143">*Функтор* в Q # — это фабрика, которая определяет новую операцию на основе другой операции.</span><span class="sxs-lookup"><span data-stu-id="0be70-143">A *functor* in Q# is a factory that defines a new operation from another operation.</span></span>
<span data-ttu-id="0be70-144">Два стандартных операторов в Q # — `Adjoint` и `Controlled` .</span><span class="sxs-lookup"><span data-stu-id="0be70-144">The two standard functors in Q# are `Adjoint` and `Controlled`.</span></span>

<span data-ttu-id="0be70-145">Операторов имеет доступ к реализации базовой операции при определении реализации новой операции.</span><span class="sxs-lookup"><span data-stu-id="0be70-145">Functors have access to the implementation of the base operation when defining the implementation of the new operation.</span></span>
<span data-ttu-id="0be70-146">Таким же операторов может выполнять более сложные функции, чем традиционные функции более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="0be70-146">Thus, functors can perform more complex functions than traditional higher-level functions.</span></span> <span data-ttu-id="0be70-147">Операторов не имеют представления в системе типов Q #.</span><span class="sxs-lookup"><span data-stu-id="0be70-147">Functors do not have a representation in the Q# type system.</span></span> <span data-ttu-id="0be70-148">Таким образом, сейчас невозможно привязать их к переменной или передать в качестве аргументов.</span><span class="sxs-lookup"><span data-stu-id="0be70-148">It is thus currently not possible to bind them to a variable or pass them as arguments.</span></span> 

<span data-ttu-id="0be70-149">Функтор используется, применяя его к операции, возвращая новую операцию.</span><span class="sxs-lookup"><span data-stu-id="0be70-149">A functor is used by applying it to an operation, returning a new operation.</span></span>
<span data-ttu-id="0be70-150">Например, операция, полученная в результате применения `Adjoint` функтор к операции, `Y` записывается как `Adjoint Y` .</span><span class="sxs-lookup"><span data-stu-id="0be70-150">For example, the operation that results from applying the `Adjoint` functor to the `Y` operation is written as `Adjoint Y`.</span></span>
<span data-ttu-id="0be70-151">Новая операция может быть затем вызвана как любая другая операция.</span><span class="sxs-lookup"><span data-stu-id="0be70-151">The new operation may then be invoked like any other operation.</span></span>
<span data-ttu-id="0be70-152">Чтобы операция поддерживала приложение `Adjoint` и (или) `Controlled` операторов, ее тип возвращаемого значения обязательно должен быть `Unit` .</span><span class="sxs-lookup"><span data-stu-id="0be70-152">For an operation to support application of the `Adjoint` and/or `Controlled` functors, its return type necessarily needs to be `Unit`.</span></span> 

#### <a name="adjoint-functor"></a><span data-ttu-id="0be70-153">`Adjoint`Функтор</span><span class="sxs-lookup"><span data-stu-id="0be70-153">`Adjoint` functor</span></span>

<span data-ttu-id="0be70-154">Поэтому `Adjoint Y(q1)` применяет к операции смежный функтор `Y` для создания новой операции и применяет эту новую операцию к `q1` .</span><span class="sxs-lookup"><span data-stu-id="0be70-154">Thus, `Adjoint Y(q1)` applies the Adjoint functor to the `Y` operation to generate a new operation, and applies that new operation to `q1`.</span></span>
<span data-ttu-id="0be70-155">Новая операция имеет ту же сигнатуру и тип, что и базовая операция `Y` .</span><span class="sxs-lookup"><span data-stu-id="0be70-155">The new operation has the same signature and type as the base operation `Y`.</span></span>
<span data-ttu-id="0be70-156">В частности, новая операция позволяет также `Adjoint` Разрешить и `Controlled` только в том случае, если базовая операция была выполнена.</span><span class="sxs-lookup"><span data-stu-id="0be70-156">In particular, the new operation also allows `Adjoint`, and will allow `Controlled` if and only if the base operation did.</span></span>
<span data-ttu-id="0be70-157">Прилегающий функтор является собственным инверсией; то есть всегда совпадает с `Adjoint Adjoint Op` `Op` .</span><span class="sxs-lookup"><span data-stu-id="0be70-157">The Adjoint functor is its own inverse; that is, `Adjoint Adjoint Op` is always the same as `Op`.</span></span>

#### <a name="controlled-functor"></a><span data-ttu-id="0be70-158">`Controlled`Функтор</span><span class="sxs-lookup"><span data-stu-id="0be70-158">`Controlled` functor</span></span>

<span data-ttu-id="0be70-159">Аналогично, `Controlled X(controls, target)` применяет контролируемый функтор к `X` операции для создания новой операции и применяет эту новую операцию к `controls` и `target` .</span><span class="sxs-lookup"><span data-stu-id="0be70-159">Similarly, `Controlled X(controls, target)` applies the Controlled functor to the `X` operation to generate a new operation, and applies that new operation to `controls` and `target`.</span></span>

> [!NOTE]
> <span data-ttu-id="0be70-160">В Q # управляемые версии всегда принимают массив элементов управления Кубитс, а заданное состояние всегда используется для всех Кубитс элементов управления в состоянии вычисления ( `PauliZ` ) `One` , $ \кет {1} $.</span><span class="sxs-lookup"><span data-stu-id="0be70-160">In Q#, controlled versions always take an array of control qubits, and the specified state is always for all of the control qubits to be in the computational (`PauliZ`) `One` state, $\ket{1}$.</span></span>
> <span data-ttu-id="0be70-161">Управление, основанное на других состояниях, можно получить, применив соответствующую единую операцию к элементу управления, Кубитс до управляемой операции, а затем применяя обратную операцию единой операции после управляемой операции.</span><span class="sxs-lookup"><span data-stu-id="0be70-161">Controlling based on other states may be achieved by applying the appropriate unitary operation to the control qubits before the controlled operation, and then applying the inverses of the unitary operation after the controlled operation.</span></span>
> <span data-ttu-id="0be70-162">Например, применение `X` операции к элементу управления, кубит до и после управляемой операции, приведет к тому, что операция будет управлять `Zero` состоянием ($ \кет {0} $) для этого кубит; применение `H` операции до и после будет контролировать `PauliX` `One` состояние, то есть-1 еиженвалуе Паули X, $ \кет {-} \масрел{: =} (\кет {0} -\кет {1} )/\скрт {2} $, а не `PauliZ` `One` состояние.</span><span class="sxs-lookup"><span data-stu-id="0be70-162">For example, applying an `X` operation to a control qubit before and after a controlled operation will cause the operation to control on the `Zero` state ($\ket{0}$) for that qubit; applying an `H` operation before and after will control on the `PauliX` `One` state, that is -1 eigenvalue of Pauli X, $\ket{-} \mathrel{:=} (\ket{0} - \ket{1}) / \sqrt{2}$ rather than the `PauliZ` `One` state.</span></span>

<span data-ttu-id="0be70-163">При наличии выражения операции новое выражение операции может быть сформировано с помощью `Controlled` функтор.</span><span class="sxs-lookup"><span data-stu-id="0be70-163">Given an operation expression, a new operation expression may be formed using the `Controlled` functor.</span></span>
<span data-ttu-id="0be70-164">Сигнатура новой операции основана на сигнатуре исходной операции.</span><span class="sxs-lookup"><span data-stu-id="0be70-164">The signature of the new operation is based on the signature of the original operation.</span></span>
<span data-ttu-id="0be70-165">Тип результата такой же, но тип входных данных — это кортеж с массивом кубит, содержащий элемент управления кубит в качестве первого элемента и аргументы исходной операции в качестве второго элемента.</span><span class="sxs-lookup"><span data-stu-id="0be70-165">The result type is the same, but the input type is a two-tuple with a qubit array that holds the control qubit(s) as the first element and the arguments of the original operation as the second element.</span></span>
<span data-ttu-id="0be70-166">Новая операция поддерживает и `Controlled` будет поддерживать `Adjoint` только в том случае, если была выполнена исходная операция.</span><span class="sxs-lookup"><span data-stu-id="0be70-166">The new operation supports `Controlled`, and will support `Adjoint` if and only if the original operation did.</span></span>

<span data-ttu-id="0be70-167">Если исходная операция заняла только один аргумент, здесь будет прилагаться эквивалентность одноэлементного кортежа.</span><span class="sxs-lookup"><span data-stu-id="0be70-167">If the original operation took only a single argument, then singleton tuple equivalence will come into play here.</span></span>
<span data-ttu-id="0be70-168">Например, `Controlled X` является управляемой версией `X` операции.</span><span class="sxs-lookup"><span data-stu-id="0be70-168">For instance, `Controlled X` is the controlled version of the `X` operation.</span></span> 
<span data-ttu-id="0be70-169">`X`имеет тип `(Qubit => Unit is Adj + Ctl)` , поэтому `Controlled X` имеет тип `((Qubit[], (Qubit)) => Unit is Adj + Ctl)` ; из-за равенства одноэлементных кортежей это то же самое, что `((Qubit[], Qubit) => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="0be70-169">`X` has type `(Qubit => Unit is Adj + Ctl)`, so `Controlled X` has type `((Qubit[], (Qubit)) => Unit is Adj + Ctl)`; because of singleton tuple equivalence, this is the same as `((Qubit[], Qubit) => Unit is Adj + Ctl)`.</span></span>

<span data-ttu-id="0be70-170">Если базовая операция заняла несколько аргументов, не забудьте заключить соответствующие аргументы управляемой версии операции в круглые скобки, чтобы преобразовать их в кортеж.</span><span class="sxs-lookup"><span data-stu-id="0be70-170">If the base operation took several arguments, remember to enclose the corresponding arguments of the controlled version of the operation in parentheses to convert them into a tuple.</span></span>
<span data-ttu-id="0be70-171">Например, `Controlled Rz` является управляемой версией `Rz` операции.</span><span class="sxs-lookup"><span data-stu-id="0be70-171">For instance, `Controlled Rz` is the controlled version of the `Rz` operation.</span></span> 
<span data-ttu-id="0be70-172">`Rz`имеет тип `((Double, Qubit) => Unit is Adj + Ctl)` , поэтому `Controlled Rz` имеет тип `((Qubit[], (Double, Qubit)) => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="0be70-172">`Rz` has type `((Double, Qubit) => Unit is Adj + Ctl)`, so `Controlled Rz` has type `((Qubit[], (Double, Qubit)) => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="0be70-173">Таким образом, будет `Controlled Rz(controls, (0.1, target))` допустимым вызовом `Controlled Rz` (Обратите внимание на круглые скобки `0.1, target` ).</span><span class="sxs-lookup"><span data-stu-id="0be70-173">Thus, `Controlled Rz(controls, (0.1, target))` would be a valid invocation of `Controlled Rz` (note the parentheses around `0.1, target`).</span></span>

<span data-ttu-id="0be70-174">В качестве другого примера `CNOT(control, target)` можно реализовать как `Controlled X([control], target)` .</span><span class="sxs-lookup"><span data-stu-id="0be70-174">As another example, `CNOT(control, target)` can be implemented as `Controlled X([control], target)`.</span></span> <span data-ttu-id="0be70-175">Если целевой объект должен управляться 2 Control Кубитс (ККНОТ), можно использовать `Controlled X([control1, control2], target)` инструкцию.</span><span class="sxs-lookup"><span data-stu-id="0be70-175">If a target should be controlled by 2 control qubits (CCNOT), we can use `Controlled X([control1, control2], target)` statement.</span></span>

#### `Controlled Adjoint` 

<span data-ttu-id="0be70-176">`Controlled`И `Adjoint` операторов работы, поэтому нет никакой разницы между применением `Controlled Adjoint Op` или `Adjoint Controlled Op` .</span><span class="sxs-lookup"><span data-stu-id="0be70-176">The `Controlled` and `Adjoint` functors commute, so there is no difference between applying `Controlled Adjoint Op` or `Adjoint Controlled Op`.</span></span>


## <a name="defining-controlled-and-adjoint-implementations"></a><span data-ttu-id="0be70-177">Определение управляемых и смежных реализаций</span><span class="sxs-lookup"><span data-stu-id="0be70-177">Defining Controlled and Adjoint Implementations</span></span>

<span data-ttu-id="0be70-178">В приведенных выше примерах объявлений первой операции операции `BitFlip` и `DecodeSuperdense` были определены с помощью сигнатур `(Qubit => Unit)` и `((Qubit, Qubit) => (Result, Result))` соответственно.</span><span class="sxs-lookup"><span data-stu-id="0be70-178">In the first operation declaration examples above, the operations `BitFlip` and `DecodeSuperdense` were defined with signatures `(Qubit => Unit)` and `((Qubit, Qubit) => (Result, Result))`, respectively.</span></span>
<span data-ttu-id="0be70-179">Как `DecodeSuperdense` и в случае с измерениями, это не единая операция, поэтому не может существовать ни управляемая несмежная специализация (отозвать связанное требование, возвращаемое операцией `Unit` ).</span><span class="sxs-lookup"><span data-stu-id="0be70-179">As `DecodeSuperdense` includes measurements, it is not a unitary operation, and therefore neither controlled not adjoint specializations could exist (recall the related requirement that such an operation return `Unit`).</span></span>
<span data-ttu-id="0be70-180">Однако, так как `BitFlip` просто выполняет единую <xref:microsoft.quantum.intrinsic.x> операцию, мы могли бы определить ее с обеими специализациями.</span><span class="sxs-lookup"><span data-stu-id="0be70-180">However, as `BitFlip` simply performs the unitary <xref:microsoft.quantum.intrinsic.x> operation, we could have defined it with both specializations.</span></span>

<span data-ttu-id="0be70-181">Здесь мы подробно расскажу о том, как включить существование специализаций в объявлениях операций Q #, таким образом предоставив им возможность вызова в сочетании с `Adjoint` и/или `Controlled` операторов.</span><span class="sxs-lookup"><span data-stu-id="0be70-181">Here, we detail how to include the existence of specializations in your Q# operation declarations, hence giving them the ability to called in conjunction with the `Adjoint` and/or `Controlled` functors.</span></span>
<span data-ttu-id="0be70-182">Далее мы рассмотрим некоторые [ситуации, в](#circumstances-for-validly-defining-specializations)которых он является допустимым или недопустимым для объявления определенных специализаций.</span><span class="sxs-lookup"><span data-stu-id="0be70-182">Further [below](#circumstances-for-validly-defining-specializations), we describe some of the situations in which it is either valid or not valid to declare certain specializations.</span></span>

<span data-ttu-id="0be70-183">Характеристики операции определяют типы операторов, которые могут быть применены к объявленной операции, и их воздействие.</span><span class="sxs-lookup"><span data-stu-id="0be70-183">Operation characteristics define what kinds of functors can be applied to the declared operation, and what effect they have.</span></span> <span data-ttu-id="0be70-184">Существование этих специализаций можно объявить как часть сигнатуры операции, в частности через заметку с характеристиками операции: `is Adj` , `is Ctl` или `is Adj + Ctl` .</span><span class="sxs-lookup"><span data-stu-id="0be70-184">The existence of these specializations can be declared as part of the operation signature, specifically through an annotation with the operation characteristics: either `is Adj`, `is Ctl`, or `is Adj + Ctl`.</span></span>
<span data-ttu-id="0be70-185">Фактическая реализация каждой специализации *может быть либо явно,* либо *явно* определена.</span><span class="sxs-lookup"><span data-stu-id="0be70-185">The actual implementation of each specialization can either be *implicitly* or *explicitly* defined.</span></span>

### <a name="implicitly-specifying-implementations"></a><span data-ttu-id="0be70-186">Неявное указание реализаций</span><span class="sxs-lookup"><span data-stu-id="0be70-186">Implicitly specifying implementations</span></span>

<span data-ttu-id="0be70-187">В этом случае тело объявления операции состоит только из реализации по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0be70-187">In this case, the body of the operation declaration consists solely of the default implementation.</span></span> <span data-ttu-id="0be70-188">Пример:</span><span class="sxs-lookup"><span data-stu-id="0be70-188">For example:</span></span>

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit 
is Adj + Ctl { // implies the existence of an adjoint, a controlled, and a controlled adjoint specialization
    H(here);
    CNOT(here, there);
}
```
<span data-ttu-id="0be70-189">В этом случае соответствующая реализация для каждой такой неявно объявленной специализации автоматически создается компилятором, который будет выполняться при `Adjoint` использовании или `Controlled` операторов.</span><span class="sxs-lookup"><span data-stu-id="0be70-189">Here, the corresponding implementation for each such implicitly declared specialization is automatically generated by the compiler, to be performed if the `Adjoint` or `Controlled` functors are used.</span></span>

<span data-ttu-id="0be70-190">Таким образом, вызов будет приводить к тому, что `Adjoint PrepareEntangledPair` компилятор реализует смежную часть `CNOT` , а затем прилегающая `H` .</span><span class="sxs-lookup"><span data-stu-id="0be70-190">So, a call of `Adjoint PrepareEntangledPair` would result in the compiler implementing the adjoint of `CNOT` and then the adjoint of `H`.</span></span>
<span data-ttu-id="0be70-191">Эти отдельные операции являются самостоятельными, поэтому итоговая `Adjoint PrepareEntangledPair` операция будет просто состоять из применения, `CNOT(here, there)` а затем `H(here)` .</span><span class="sxs-lookup"><span data-stu-id="0be70-191">These individual operations are both self-adjoint, so the resulting `Adjoint PrepareEntangledPair` operation would simply consist of applying `CNOT(here, there)` and then `H(here)`.</span></span>
<span data-ttu-id="0be70-192">Поэтому мы можем использовать этот `DecodeSuperdense` пример для более компактного написания приведенного выше примера, используя смежную часть `PrepareEntangledPair` для преобразования состояния запутанными обратно в унентанглед пару Кубитс:</span><span class="sxs-lookup"><span data-stu-id="0be70-192">Hence we can use this to write the `DecodeSuperdense` example above more compactly, by using the adjoint of `PrepareEntangledPair` to transform the entangled state back into an unentangled pair of qubits:</span></span>

```qsharp
operation DecodeSuperdense(here : Qubit, there : Qubit) : (Result, Result) {
    Adjoint PrepareEntangledPair(there, here);

    let firstBit = M(there);
    let secondBit = M(here);

    return (firstBit, secondBit);
}
```

<span data-ttu-id="0be70-193">Заметка с характеристиками операций в объявлении полезна для того, чтобы компилятор создавал на основе реализации по умолчанию другие специализации.</span><span class="sxs-lookup"><span data-stu-id="0be70-193">The annotation with the operation characteristics in the declaration is useful to ensure that the compiler auto-generates other specializations based on the default implementation.</span></span> 

<span data-ttu-id="0be70-194">При проектировании операций для использования с операторов необходимо учитывать ряд важных ограничений.</span><span class="sxs-lookup"><span data-stu-id="0be70-194">There are a number of important limitations to consider when designing operations for use with functors.</span></span>
<span data-ttu-id="0be70-195">Как правило, специализации для операции, которая использует выходное значение любой другой операции, *не могут* быть созданы компилятором автоматически, так как это неоднозначно, как изменить порядок инструкций в такой операции, чтобы получить такой же результат.</span><span class="sxs-lookup"><span data-stu-id="0be70-195">Most critically, specializations for an operation that uses the output value of any other operation *cannot* be auto-generated by the compiler, as it is ambiguous how to reorder the statements in such an operation to obtain the same effect.</span></span>

<span data-ttu-id="0be70-196">Таким образом, часто бывает полезно явно указывать различные реализации.</span><span class="sxs-lookup"><span data-stu-id="0be70-196">Therefore, it is often useful to explicitly specify the various implementations.</span></span>

### <a name="explicitly-specifying-implementations"></a><span data-ttu-id="0be70-197">Явное указание реализаций</span><span class="sxs-lookup"><span data-stu-id="0be70-197">Explicitly specifying implementations</span></span>

<span data-ttu-id="0be70-198">В случае, если реализация не может быть создана компилятором, ее можно указать явно.</span><span class="sxs-lookup"><span data-stu-id="0be70-198">In the case where the implementation cannot be generated by the compiler, it can be explicitly specified.</span></span> <span data-ttu-id="0be70-199">Такие явные объявления специализации могут состоять из подходящей *директивы создания* или определяемой пользователем реализации.</span><span class="sxs-lookup"><span data-stu-id="0be70-199">Such explicit specialization declarations can consist of a suitable *generation directive* or a user-defined implementation.</span></span>
<span data-ttu-id="0be70-200">Здесь мы предоставляем полный спектр возможностей с примерами ниже.</span><span class="sxs-lookup"><span data-stu-id="0be70-200">Here we provide the full range of possibilities, with examples following below.</span></span>


#### <a name="explicit-specialization-declarations"></a><span data-ttu-id="0be70-201">Явные объявления специализации</span><span class="sxs-lookup"><span data-stu-id="0be70-201">Explicit specialization declarations</span></span>

<span data-ttu-id="0be70-202">Операции Q # могут содержать следующие явные объявления специализаций:</span><span class="sxs-lookup"><span data-stu-id="0be70-202">Q# operations may contain the following explicit specialization declarations:</span></span>

- <span data-ttu-id="0be70-203">В `body` специализации указывается реализация операции без применения операторов.</span><span class="sxs-lookup"><span data-stu-id="0be70-203">The `body` specialization specifies the implementation of the operation with no functors applied.</span></span>
- <span data-ttu-id="0be70-204">В `adjoint` специализации указывается реализация операции с `Adjoint` примененным функтор.</span><span class="sxs-lookup"><span data-stu-id="0be70-204">The `adjoint` specialization specifies the implementation of the operation with the `Adjoint` functor applied.</span></span>
- <span data-ttu-id="0be70-205">В `controlled` специализации указывается реализация операции с `Controlled` примененным функтор.</span><span class="sxs-lookup"><span data-stu-id="0be70-205">The `controlled` specialization specifies the implementation of the operation with the `Controlled` functor applied.</span></span>
- <span data-ttu-id="0be70-206">`controlled adjoint`Специализация задает реализацию операции с `Adjoint` `Controlled` примененными к и операторов.</span><span class="sxs-lookup"><span data-stu-id="0be70-206">The `controlled adjoint` specialization specifies the implementation of the operation with both the `Adjoint` and `Controlled` functors applied.</span></span>
  <span data-ttu-id="0be70-207">Эту специализацию также можно присвоить имя `adjoint controlled` , так как две операторов работы.</span><span class="sxs-lookup"><span data-stu-id="0be70-207">This specialization can also be named `adjoint controlled`, since the two functors commute.</span></span>


<span data-ttu-id="0be70-208">Специализация операции состоит из тега специализации (например `body` , или и `adjoint` т. д.), за которым следует одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="0be70-208">An operation specialization consists of the specialization tag (e.g. `body`, or `adjoint`, etc.) followed by one of:</span></span>

- <span data-ttu-id="0be70-209">Явное объявление, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="0be70-209">An explicit declaration as described below.</span></span>
- <span data-ttu-id="0be70-210">*Директива* , сообщающая компилятору, *как* создать специализацию, одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="0be70-210">A *directive* that tells the compiler *how* to generate the specialization, one of:</span></span>
  - <span data-ttu-id="0be70-211">`intrinsic`, который указывает, что специализация предоставляется целевым компьютером.</span><span class="sxs-lookup"><span data-stu-id="0be70-211">`intrinsic`, which indicates that the specialization is provided by the target machine.</span></span>
  - <span data-ttu-id="0be70-212">`distribute`, который может использоваться с `controlled` `controlled adjoint` специализациями и.</span><span class="sxs-lookup"><span data-stu-id="0be70-212">`distribute`, which may be used with the `controlled` and `controlled adjoint` specializations.</span></span>
    <span data-ttu-id="0be70-213">При использовании с параметр указывает на то `controlled` , что компилятор должен вычислить специализацию, применяя `Controlled` ко всем операциям в `body` .</span><span class="sxs-lookup"><span data-stu-id="0be70-213">When used with `controlled`, it indicates that the compiler should compute the specialization by applying `Controlled` to all of the operations in the `body`.</span></span>
    <span data-ttu-id="0be70-214">При использовании с параметр указывает на то `controlled adjoint` , что компилятор должен вычислить специализацию, применяя `Controlled` ко всем операциям в `adjoint` специализации.</span><span class="sxs-lookup"><span data-stu-id="0be70-214">When used with `controlled adjoint`, it indicates that the compiler should compute the specialization by applying `Controlled` to all of the operations in the `adjoint` specialization.</span></span>
  - <span data-ttu-id="0be70-215">`invert`, который указывает, что компилятор должен вычислить `adjoint` специализацию путем инвертирования `body` , т. е. Порядок операций и применение прилегающих к каждому из них.</span><span class="sxs-lookup"><span data-stu-id="0be70-215">`invert`, which indicates that the compiler should compute the `adjoint` specialization by inverting the `body`, i.e. reversing the order of operations and applying the adjoint to each one.</span></span>
    <span data-ttu-id="0be70-216">Если используется с `adjoint controlled` , это означает, что компилятор должен вычислить специализацию путем инвертирования `controlled` специализации.</span><span class="sxs-lookup"><span data-stu-id="0be70-216">When used with `adjoint controlled`, this indicates that the compiler should compute the specialization by inverting the `controlled` specialization.</span></span>
  - <span data-ttu-id="0be70-217">`self`, чтобы указать, что прилегающий специализации совпадает с `body` специализацией.</span><span class="sxs-lookup"><span data-stu-id="0be70-217">`self`, to indicate that the adjoint specialization is the the same as the `body` specialization.</span></span>
    <span data-ttu-id="0be70-218">Это допустимо для `adjoint` `adjoint controlled` специализаций и.</span><span class="sxs-lookup"><span data-stu-id="0be70-218">This is legal for the `adjoint` and `adjoint controlled` specializations.</span></span>
    <span data-ttu-id="0be70-219">Для `adjoint controlled` , `self` предполагает, что `adjoint controlled` специализация является той же, что и `controlled` специализация.</span><span class="sxs-lookup"><span data-stu-id="0be70-219">For `adjoint controlled`, `self` implies that the `adjoint controlled` specialization is the same as the `controlled` specialization.</span></span>
  - <span data-ttu-id="0be70-220">`auto`, чтобы указать, что компилятор должен выбрать соответствующую директиву для применения.</span><span class="sxs-lookup"><span data-stu-id="0be70-220">`auto`, to indicate that the compiler should select an appropriate directive to apply.</span></span>
    <span data-ttu-id="0be70-221">`auto`не может использоваться для `body` специализации.</span><span class="sxs-lookup"><span data-stu-id="0be70-221">`auto` may not be used for the `body` specialization.</span></span>

<span data-ttu-id="0be70-222">Для директив и `auto` ALL требуется закрывающая точка с запятой `;` .</span><span class="sxs-lookup"><span data-stu-id="0be70-222">The directives and `auto` all require a closing semi-colon `;`.</span></span>
<span data-ttu-id="0be70-223">`auto`Директива разрешается в следующую директиву поколения, если предоставлено явное объявление объекта `body` .</span><span class="sxs-lookup"><span data-stu-id="0be70-223">The `auto` directive resolves to the following generation directive if an explicit declaration of the `body` is provided:</span></span>

- <span data-ttu-id="0be70-224">`adjoint`Специализация создается в соответствии с директивой `invert` .</span><span class="sxs-lookup"><span data-stu-id="0be70-224">The `adjoint` specialization is generated according to the directive `invert`.</span></span>
- <span data-ttu-id="0be70-225">`controlled`Специализация создается в соответствии с директивой `distribute` .</span><span class="sxs-lookup"><span data-stu-id="0be70-225">The `controlled` specialization is generated according to the directive `distribute`.</span></span>
- <span data-ttu-id="0be70-226">`adjoint controlled`Специализация создается в соответствии с директивой `invert` , если явное объявление для задано `controlled` , но не для `adjoint` , и `distribute` в противном случае.</span><span class="sxs-lookup"><span data-stu-id="0be70-226">The `adjoint controlled` specialization is generated according to the directive `invert` if an explicit declaration for `controlled` is given but not one for `adjoint`, and `distribute` otherwise.</span></span>

> [!TIP]   
> <span data-ttu-id="0be70-227">Если операция является самопримыкающей, явно укажите либо примыкающую, либо управляемую смежную специализацию с помощью директивы поколения, `self` чтобы компилятор использовал эту информацию в целях оптимизации.</span><span class="sxs-lookup"><span data-stu-id="0be70-227">If an operation is self-adjoint, explicitly specify either the adjoint or the controlled adjoint specialization via the generation directive `self` to allow the compiler to make use of that information for optimization purposes.</span></span>

<span data-ttu-id="0be70-228">Объявление специализации, содержащее определенную пользователем реализацию, состоит из кортежа аргументов, за которым следует блок операторов с кодом Q #, реализующим специализацию.</span><span class="sxs-lookup"><span data-stu-id="0be70-228">A specialization declaration containing a user defined implementation consists of an argument tuple followed by a statement block with the Q# code that implements the specialization.</span></span>
<span data-ttu-id="0be70-229">В списке arguments `...` используется для представления аргументов, объявленных для операции в целом.</span><span class="sxs-lookup"><span data-stu-id="0be70-229">In the argument list, `...` is used to represent the arguments declared for the operation as a whole.</span></span>
<span data-ttu-id="0be70-230">Для `body` и `adjoint` список аргументов всегда должен иметь значение `(...)` ; для `controlled` и `adjoint controlled` список аргументов должен быть символом, представляющим массив элементов управления Кубитс, за которым следует `...` ключ, заключенный в круглые скобки, например `(controls,...)` .</span><span class="sxs-lookup"><span data-stu-id="0be70-230">For `body` and `adjoint`, the argument list should always be `(...)`; for `controlled` and `adjoint controlled`, the argument list should be a symbol that represents the array of control qubits, followed by `...`, enclosed in parentheses; for example, `(controls,...)`.</span></span>

### <a name="examples"></a><span data-ttu-id="0be70-231">Примеры</span><span class="sxs-lookup"><span data-stu-id="0be70-231">Examples</span></span>

<span data-ttu-id="0be70-232">Объявление операции может быть простым, как показано ниже, которое определяет операцию примитива Паули X:</span><span class="sxs-lookup"><span data-stu-id="0be70-232">An operation declaration might be as simple as the following, which defines the primitive Pauli X operation:</span></span>

```qsharp
operation X (qubit : Qubit) : Unit
is Adj + Ctl {
    body intrinsic;
    adjoint self;
}
```
<span data-ttu-id="0be70-233">Обратите внимание, что смежная операция Паули X определяется с помощью директивы, `self` так как по определению `X` является обратным.</span><span class="sxs-lookup"><span data-stu-id="0be70-233">Note that the adjoint of the Pauli X operation is defined with the directive `self` because by definition `X` is its own inverse.</span></span>

<span data-ttu-id="0be70-234">Приведенный `PrepareEntangledPair` выше код для примера эквивалентен приведенному ниже коду, содержащему явные объявления специализации:</span><span class="sxs-lookup"><span data-stu-id="0be70-234">The code in `PrepareEntangledPair` above for example is equivalent to the code below containing explicit specialization declarations:</span></span> 

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
<span data-ttu-id="0be70-235">Ключевое слово `auto` указывает, что компилятор должен определить, как создать реализацию специализации.</span><span class="sxs-lookup"><span data-stu-id="0be70-235">The keyword `auto` indicates that the compiler should determine how to generate the specialization implementation.</span></span>

#### <a name="user-defined-specialization-implementation"></a><span data-ttu-id="0be70-236">Реализация пользовательской специализации</span><span class="sxs-lookup"><span data-stu-id="0be70-236">User-defined specialization implementation</span></span>

<span data-ttu-id="0be70-237">Если компилятор не может автоматически создать реализацию для определенной специализации или если может быть предоставлена более эффективная реализация, то реализация может быть также определена вручную.</span><span class="sxs-lookup"><span data-stu-id="0be70-237">If the compiler cannot generate the implementation for a certain specialization automatically, or if a more efficient implementation can be given, then the implementation may also be manually defined.</span></span>

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit
is Ctl + Adj {
    body (...) { // default body specialization
        H(here);
        CNOT(here, there);
    }

    controlled (cs, ...) { // user defined implementation for the controlled specialization
        Controlled H(cs, here);
        Controlled X(cs + [here], there);
    }

    adjoint invert; 
    controlled adjoint invert; 
}
```
<span data-ttu-id="0be70-238">В приведенном выше примере `adjoint invert;` указывает, что примыкающая специализация должна быть создана путем инвертирования реализации тела, и `controlled adjoint invert;` указывает, что управляемая примыкающая специализация должна создаваться путем инвертирования заданной реализации управляемой специализации.</span><span class="sxs-lookup"><span data-stu-id="0be70-238">In the example above, `adjoint invert;` indicates that the adjoint specialization is to be generated by inverting the body implementation, and `controlled adjoint invert;` indicates that the controlled adjoint specialization is to be generated by inverting the given implementation of the controlled specialization.</span></span>

<span data-ttu-id="0be70-239">Если необходимо явно объявить одну или несколько специализаций, кроме тела по умолчанию, то реализация тела по умолчанию должна быть заключена в подходящее объявление специализации:</span><span class="sxs-lookup"><span data-stu-id="0be70-239">If one or more specializations besides the default body need to be explicitly declared, then the implementation for the default body needs to be wrapped into a suitable specialization declaration as well:</span></span>

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

### <a name="circumstances-for-validly-defining-specializations"></a><span data-ttu-id="0be70-240">Условия для корректного определения специализаций</span><span class="sxs-lookup"><span data-stu-id="0be70-240">Circumstances for validly defining specializations</span></span>

#### <a name="operation-declarations-with-adjointcontrolled"></a><span data-ttu-id="0be70-241">Объявления операций с примыкающими и управляемыми данными</span><span class="sxs-lookup"><span data-stu-id="0be70-241">Operation declarations with adjoint/controlled</span></span>

<span data-ttu-id="0be70-242">Допускается указание операции без смежных или контролируемых версий.</span><span class="sxs-lookup"><span data-stu-id="0be70-242">It is legal to specify an operation with no adjoint or controlled versions.</span></span> <span data-ttu-id="0be70-243">Например, операции измерения не имеют ни одного, так как они не являются обратимыми или управляемыми.</span><span class="sxs-lookup"><span data-stu-id="0be70-243">For instance, measurement operations have neither, because they are not invertible or controllable.</span></span>

<span data-ttu-id="0be70-244">Операция поддерживает `Adjoint` и/или операторов, `Controlled` если ее объявление содержит неявное или неявное объявление соответствующих специализаций.</span><span class="sxs-lookup"><span data-stu-id="0be70-244">An operation supports the `Adjoint` and/or `Controlled` functors if its declaration contains an implicit or explicit declaration of the respective specializations.</span></span>

<span data-ttu-id="0be70-245">Явная объявленная специализация с прилегающая, управляемой, подразумевает наличие примыкающей или управляемой специализации.</span><span class="sxs-lookup"><span data-stu-id="0be70-245">An explicitly declared adjoint/controlled specialization implies the existence of an adjoint/controlled specialization.</span></span> 

<span data-ttu-id="0be70-246">Для операции, текст которой содержит циклы повторения, инструкции SET, измерения, операторы Return или вызовы других операций, которые не поддерживают `Adjoint` функтор, автоматическое создание примыкающей специализации, следующей за `invert` директивой или, невозможно `auto` .</span><span class="sxs-lookup"><span data-stu-id="0be70-246">For an operation whose body contains repeat-until-success loops, set statements, measurements, return statements, or calls to other operations that do not support the `Adjoint` functor, auto-generating an adjoint specialization following the `invert` or `auto` directive is not possible.</span></span>

<span data-ttu-id="0be70-247">Для операции, текст которой содержит вызовы других операций, не поддерживающих `Controlled` функтор, автоматическое создание управляемой специализации, следующей за `distribute` директивой или, невозможно `auto` .</span><span class="sxs-lookup"><span data-stu-id="0be70-247">For an operation whose body contains calls to other operations that does not support the `Controlled` functor, auto-generating a controlled specialization following the `distribute` or `auto` directive is not possible.</span></span>

#### <a name="controlled-adjoint"></a><span data-ttu-id="0be70-248">Управляемый соседний</span><span class="sxs-lookup"><span data-stu-id="0be70-248">Controlled Adjoint</span></span>

<span data-ttu-id="0be70-249">Управляемая смежная версия операции указывает, как реализуется зависящая от такта версия смежной операции.</span><span class="sxs-lookup"><span data-stu-id="0be70-249">The controlled adjoint version of an operation specifies how a quantum-controlled version of the adjoint of the operation is implemented.</span></span>
<span data-ttu-id="0be70-250">Допускается указание операции без управляемой примыкающей версии; Например, операции измерения не имеют контролируемой версии, так как они не являются управляемыми и необратимыми.</span><span class="sxs-lookup"><span data-stu-id="0be70-250">It is legal to specify an operation with no controlled adjoint version; for instance, measurement operations have no controlled adjoint version because they are neither controllable nor invertible.</span></span>

<span data-ttu-id="0be70-251">Управляемая примыкающая специализация для операции должна существовать только в том случае, если существует и смежная, и управляемая специализация.</span><span class="sxs-lookup"><span data-stu-id="0be70-251">A controlled adjoint specialization for an operation needs to exist if and only if both an adjoint and a controlled specialization exist.</span></span> <span data-ttu-id="0be70-252">В этом случае определяется существование управляемой примыкающей специализации, и компилятор создает соответствующую специализацию, если реализация не определена явным образом.</span><span class="sxs-lookup"><span data-stu-id="0be70-252">In that case, the existence of the controlled adjoint specialization is inferred and an appropriate specialization is generated by the compiler if no implementation has been defined explicitly.</span></span> 

<span data-ttu-id="0be70-253">Для операции, тело которой содержит вызовы других операций, не имеющих управляемой примыкающей версии, автоматическое создание примыкающей специализации после `invert` `distribute` `auto` директивы или невозможно.</span><span class="sxs-lookup"><span data-stu-id="0be70-253">For an operation whose body contains calls to other operations that do not have a controlled adjoint version, auto-generating an adjoint specialization following the `invert`, `distribute` or `auto` directive is not possible.</span></span>


### <a name="type-compatibility"></a><span data-ttu-id="0be70-254">Совместимость типов</span><span class="sxs-lookup"><span data-stu-id="0be70-254">Type Compatibility</span></span>

<span data-ttu-id="0be70-255">Операция с поддержкой дополнительного операторов может использоваться в любом месте, где выполняется операция с меньшим числом операторов, но ожидается та же сигнатура.</span><span class="sxs-lookup"><span data-stu-id="0be70-255">An operation with additional functors supported may be used anywhere an operation with fewer functors but the same signature is expected.</span></span>
<span data-ttu-id="0be70-256">Например, операция типа `(Qubit => Unit is Adj)` может использоваться в любом месте, где ожидается операция с типом `(Qubit => Unit)` .</span><span class="sxs-lookup"><span data-stu-id="0be70-256">For instance, an operation of type `(Qubit => Unit is Adj)` may be used anywhere an operation of type `(Qubit => Unit)` is expected.</span></span>

<span data-ttu-id="0be70-257">Q # является *ковариантным* по отношению к вызываемым типам возвращаемых данных: вызываемый метод, возвращающий тип, `'A` совместим с вызываемым с тем же входным типом и типом результата, `'A` совместимым с.</span><span class="sxs-lookup"><span data-stu-id="0be70-257">Q# is *covariant* with respect to callable return types: a callable that returns a type `'A` is compatible with a callable with the same input type and a result type that `'A` is compatible with.</span></span>

<span data-ttu-id="0be70-258">Q # является *контравариантным* по отношению к входным типам: вызываемый тип в `'A` качестве входных данных совместим с вызываемым с тем же типом результата и типом ввода, совместимым с `'A` .</span><span class="sxs-lookup"><span data-stu-id="0be70-258">Q# is *contravariant* with respect to input types: a callable that takes a type `'A` as input is compatible with a callable with the same result type and an input type that is compatible with `'A`.</span></span>

<span data-ttu-id="0be70-259">Это происходит при наличии следующих определений:</span><span class="sxs-lookup"><span data-stu-id="0be70-259">That is, given the following definitions:</span></span>

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

<span data-ttu-id="0be70-260">выполняются следующие условия.</span><span class="sxs-lookup"><span data-stu-id="0be70-260">the following are true:</span></span>

- <span data-ttu-id="0be70-261">Функцию `ConjugateInvertWith` можно вызвать с `inner` аргументом либо `Invert` или `ApplyUnitary` .</span><span class="sxs-lookup"><span data-stu-id="0be70-261">The function `ConjugateInvertWith` may be invoked with an `inner` argument of either `Invert` or `ApplyUnitary`.</span></span>
- <span data-ttu-id="0be70-262">Функция `ConjugateUnitaryWith` может быть вызвана с `inner` аргументом `ApplyUnitary` , но не `Invert` .</span><span class="sxs-lookup"><span data-stu-id="0be70-262">The function `ConjugateUnitaryWith` may be invoked with an `inner` argument of `ApplyUnitary`, but not `Invert`.</span></span>
- <span data-ttu-id="0be70-263">Значение типа `(Qubit[] => Unit is Adj + Ctl)` может быть возвращено из `ConjugateInvertWith` .</span><span class="sxs-lookup"><span data-stu-id="0be70-263">A value of type `(Qubit[] => Unit is Adj + Ctl)` may be returned from `ConjugateInvertWith`.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0be70-264">В Q # 0,3 введена существенная разница в работе определяемых пользователем типов.</span><span class="sxs-lookup"><span data-stu-id="0be70-264">Q# 0.3 introduced a significant difference in the behavior of user-defined types.</span></span>

<span data-ttu-id="0be70-265">Определяемые пользователем типы обрабатываются как упакованная версия базового типа, а не как подтип.</span><span class="sxs-lookup"><span data-stu-id="0be70-265">User-defined types are treated as a wrapped version of the underlying type, rather than as a subtype.</span></span>
<span data-ttu-id="0be70-266">Это означает, что значение определяемого пользователем типа не может использоваться, если ожидается значение базового типа.</span><span class="sxs-lookup"><span data-stu-id="0be70-266">This means that a value of a user-defined type is not usable where a value of the underlying type is expected.</span></span>


### <a name="conjugations"></a><span data-ttu-id="0be70-267">Лиц</span><span class="sxs-lookup"><span data-stu-id="0be70-267">Conjugations</span></span>

<span data-ttu-id="0be70-268">В отличие от классических битов освобождение памяти такта немного сложнее, так как в результате нежелательного сброса Кубитс может иметь нежелательные последствия для оставшихся вычислений, если Кубитс все еще запутанными.</span><span class="sxs-lookup"><span data-stu-id="0be70-268">In contrast to classical bits, releasing quantum memory is slightly more involved since blindly resetting qubits can have undesired effects on the remaining computation if the qubits are still entangled.</span></span> <span data-ttu-id="0be70-269">Это можно избежать, правильно выполнив вычисления перед освобождением памяти.</span><span class="sxs-lookup"><span data-stu-id="0be70-269">This can be avoided by properly "undoing" performed computations prior to releasing the memory.</span></span> <span data-ttu-id="0be70-270">Общий шаблон в тактовых вычислениях, следовательно, является следующим:</span><span class="sxs-lookup"><span data-stu-id="0be70-270">A common pattern in quantum computing is hence the following:</span></span> 

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

<span data-ttu-id="0be70-271">Начиная с нашего выпуска 0,9 мы поддерживаем инструкцию конжугатион, которая реализует преобразование выше.</span><span class="sxs-lookup"><span data-stu-id="0be70-271">Starting with our 0.9 release, we support a conjugation statement that implements the transformation above.</span></span> <span data-ttu-id="0be70-272">С помощью этой инструкции операция `ApplyWith` может быть реализована следующим образом:</span><span class="sxs-lookup"><span data-stu-id="0be70-272">Using that statement, the operation `ApplyWith` can be implemented in the following way:</span></span>

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
<span data-ttu-id="0be70-273">Очевидно, что такой оператор конжугатион гораздо полезнее, если внешнее и внутреннее преобразование недоступно в качестве операций, но вместо этого более удобно описывать блоком, состоящим из нескольких инструкций.</span><span class="sxs-lookup"><span data-stu-id="0be70-273">Such a conjugation statement obviously becomes far more useful if the outer and inner transformation are not readily available as operations but are instead more convenient to describe by a block consisting of several statements.</span></span> 

<span data-ttu-id="0be70-274">Обратное преобразование для инструкций, определенных в блоке внутри блока, автоматически создается компилятором и выполняется после завершения блока Apply.</span><span class="sxs-lookup"><span data-stu-id="0be70-274">The inverse transformation for the statements defined in the within-block is automatically generated by the compiler and executed after the apply-block completes.</span></span>
<span data-ttu-id="0be70-275">Поскольку любые изменяемые переменные, используемые в качестве части блока in, не могут быть повторно привязаны в блоке применения, созданное преобразование гарантируется как прилегающие вычисления в блоке внутри блока.</span><span class="sxs-lookup"><span data-stu-id="0be70-275">Since any mutable variables used as part of the within-block cannot be rebound in the apply-block, the generated transformation is guaranteed to be the adjoint of the computation in the within-block.</span></span> 


## <a name="defining-new-functions"></a><span data-ttu-id="0be70-276">Определение новых функций</span><span class="sxs-lookup"><span data-stu-id="0be70-276">Defining New Functions</span></span>

<span data-ttu-id="0be70-277">Функции являются исключительно детерминированными, классическими подпрограммами в Q #, которые отличаются от операций тем, что они не могут иметь никаких эффектов, Кроме вычисления выходного значения.</span><span class="sxs-lookup"><span data-stu-id="0be70-277">Functions are purely deterministic, classical routines in Q#, which are distinct from operations in that they are not allowed to have any effects beyond calculating an output value.</span></span>
<span data-ttu-id="0be70-278">В частности, функции не могут вызывать операции; Применяйте, выделяйте или позаимствование Кубитс; Примеры случайных чисел; или, в противном случае, зависит от состояния, превышающего входное значение функции.</span><span class="sxs-lookup"><span data-stu-id="0be70-278">In particular, functions cannot call operations; act on, allocate, or borrow qubits; sample random numbers; or otherwise depend on state beyond the input value to a function.</span></span>
<span data-ttu-id="0be70-279">Как следствие, функции Q # являются *чисто*, в том, что они всегда сопоставляют одинаковые входные значения с одними и теми же выходными значениями.</span><span class="sxs-lookup"><span data-stu-id="0be70-279">As a consequence, Q# functions are *pure*, in that they always map the same input values to the same output values.</span></span>
<span data-ttu-id="0be70-280">Это позволяет компилятору Q # безопасно изменять порядок и время вызова функций при создании специализаций операций.</span><span class="sxs-lookup"><span data-stu-id="0be70-280">This allows the Q# compiler to safely reorder how and when functions are called when generating operation specializations.</span></span>

<span data-ttu-id="0be70-281">Каждый исходный файл Q # может определять любое количество функций.</span><span class="sxs-lookup"><span data-stu-id="0be70-281">Each Q# source file may define any number of functions.</span></span>
<span data-ttu-id="0be70-282">Имена функций должны быть уникальными в пределах пространства имен и не могут конфликтовать с именами операций или типов.</span><span class="sxs-lookup"><span data-stu-id="0be70-282">Function names must be unique within a namespace and may not conflict with operation or type names.</span></span>

<span data-ttu-id="0be70-283">Определение функции работает аналогично определению операции, за исключением того, что для функции нельзя определить ни прилегающие, ни контролируемые специализации.</span><span class="sxs-lookup"><span data-stu-id="0be70-283">Defining a function works similarly to defining an operation, except that no adjoint or controlled specializations can be defined for a function.</span></span>
<span data-ttu-id="0be70-284">например</span><span class="sxs-lookup"><span data-stu-id="0be70-284">For instance:</span></span>

```qsharp
function Square(x : Double) : (Double) {
    return x * x;
}
```

<span data-ttu-id="0be70-285">or</span><span class="sxs-lookup"><span data-stu-id="0be70-285">or</span></span> 

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

### <a name="classical-logic-in-functions--good"></a><span data-ttu-id="0be70-286">Классическая логика в функциях = = хорошее</span><span class="sxs-lookup"><span data-stu-id="0be70-286">Classical logic in functions == good</span></span>

<span data-ttu-id="0be70-287">Когда это возможно, полезно писать классическую логику с точки зрения функций, а не операций, чтобы его можно было использовать в рамках операций.</span><span class="sxs-lookup"><span data-stu-id="0be70-287">Whenever it is possible to do so, it is helpful to write out classical logic in terms of functions rather than operations, so that it can be more readily used from within operations.</span></span>
<span data-ttu-id="0be70-288">Например, если мы написали `Square` объявление выше в качестве *операции*, компилятор не сможет гарантировать, что его вызов с теми же входными данными получит одинаковые выходные данные.</span><span class="sxs-lookup"><span data-stu-id="0be70-288">For example, if we had written the `Square` declaration above as an *operation*, then the compiler would not have been able to guarantee that calling it with the same input would consistently produce the same outputs.</span></span>

<span data-ttu-id="0be70-289">Чтобы подчеркнуть разницу между функциями и операциями, рассмотрим проблему с классической выборкой случайного числа в операции Q #:</span><span class="sxs-lookup"><span data-stu-id="0be70-289">To underscore the difference between functions and operations, consider the problem of classically sampling a random number from within a Q# operation:</span></span>

```qsharp
operation U(target : Qubit) : Unit {

    let angle = RandomReal()
    Rz(angle, target)
}
```

<span data-ttu-id="0be70-290">Каждый раз `U` при вызове он будет иметь другое действие `target` .</span><span class="sxs-lookup"><span data-stu-id="0be70-290">Each time that `U` is called, it will have a different action on `target`.</span></span>
<span data-ttu-id="0be70-291">В частности, компилятор не может гарантировать, что если мы добавили `adjoint auto` объявление специализации в, то будет выступать в `U` `U(target); Adjoint U(target);` качестве удостоверения (т. е. без операции).</span><span class="sxs-lookup"><span data-stu-id="0be70-291">In particular, the compiler cannot guarantee that if we added an `adjoint auto` specialization declaration to `U`, then `U(target); Adjoint U(target);` acts as identity (that is, as a no-op).</span></span>
<span data-ttu-id="0be70-292">Это нарушает определение примыкающего, которое мы видели в [векторах и матрицах](xref:microsoft.quantum.concepts.vectors), что позволяет автоматически формировать примыкающую специализацию в операции, в которой мы вызвали эту операцию, <xref:microsoft.quantum.math.randomreal> приведет к нарушению гарантий, предоставляемых компилятором; <xref:microsoft.quantum.math.randomreal> — это операция, для которой не существует ни одной соседней или контролируемой версии.</span><span class="sxs-lookup"><span data-stu-id="0be70-292">This violates the definition of the adjoint that we saw in [Vectors and Matrices](xref:microsoft.quantum.concepts.vectors), such that allowing to auto-generate an adjoint specialization in an operation where we have called the operation <xref:microsoft.quantum.math.randomreal> would break the guarantees provided by the compiler; <xref:microsoft.quantum.math.randomreal> is an operation for which no adjoint or controlled version exists.</span></span>

<span data-ttu-id="0be70-293">С другой стороны, разрешение на вызовы функций, например, `Square` является типобезопасным, в том, что компилятор может быть уверенным в том, что для `Square` обеспечения стабильной работы его выходных данных необходимо сохранить только входные данные.</span><span class="sxs-lookup"><span data-stu-id="0be70-293">On the other hand, allowing function calls such as `Square` is safe, in that the compiler can be assured that it only needs to preserve the input to `Square` in order to keep its output stable.</span></span>
<span data-ttu-id="0be70-294">Таким образом, изоляция максимально возможной логики функций позволяет легко повторно использовать эту логику в других функциях и операциях.</span><span class="sxs-lookup"><span data-stu-id="0be70-294">Thus, isolating as much classical logic as possible into functions makes it easy to reuse that logic in other functions and operations alike.</span></span>


## <a name="generic-type-parameterized-callables"></a><span data-ttu-id="0be70-295">Универсальные вызываемые типы (параметризованные)</span><span class="sxs-lookup"><span data-stu-id="0be70-295">Generic (Type-Parameterized) Callables</span></span>

<span data-ttu-id="0be70-296">Многие функции и операции, которые мы хотим определить, не сильно полагаются на типы входных данных, а только неявно используют их типы с помощью какой бы то ни было другой функции или операции.</span><span class="sxs-lookup"><span data-stu-id="0be70-296">Many functions and operations that we might wish to define do not actually heavily rely on the types of their inputs, but rather only implicitly use their types via some other function or operation.</span></span>
<span data-ttu-id="0be70-297">Например, рассмотрим концепцию *Map* , общую для многих функциональных языков. При наличии функции $f (x) $ и коллекции значений $ \{ x_1, x_2, \дотс, x_n \} $, Map возвращает новую коллекцию $ \{ f (x_1), f (x_2), \дотс, f (x_n) \} $.</span><span class="sxs-lookup"><span data-stu-id="0be70-297">For example, consider the *map* concept common to many functional languages; given a function $f(x)$ and a collection of values $\{x_1, x_2, \dots, x_n\}$, map returns a new collection $\{f(x_1), f(x_2), \dots, f(x_n)\}$.</span></span>
<span data-ttu-id="0be70-298">Чтобы реализовать это в Q #, мы можем воспользоваться преимуществами функций, которые являются первыми классами.</span><span class="sxs-lookup"><span data-stu-id="0be70-298">To implement this in Q#, we can take advantage of that functions are first class.</span></span>
<span data-ttu-id="0be70-299">Давайте запишем краткий пример `Map` , используя ★ в качестве заполнителя, пока мы выберем, какие типы нам нужны.</span><span class="sxs-lookup"><span data-stu-id="0be70-299">Let's write out a quick example of `Map`, using ★ as a placeholder while we figure out what types we need.</span></span>

```qsharp
function Map(fn : (★ -> ★), values : ★[]) : ★[] {
    mutable mappedValues = new ★[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

<span data-ttu-id="0be70-300">Обратите внимание, что эта функция выглядит почти так же, независимо от фактических типов, которые мы заменяем.</span><span class="sxs-lookup"><span data-stu-id="0be70-300">Note this function looks very much the same no matter what actual types we substitute in.</span></span>
<span data-ttu-id="0be70-301">, Например, карту из целых чисел в пол, похожа на карту из чисел с плавающей запятой в строки:</span><span class="sxs-lookup"><span data-stu-id="0be70-301">A map from integers to Paulis, for instance, looks much the same as a map from floating-point numbers to strings:</span></span>

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

<span data-ttu-id="0be70-302">В принципе, мы могли бы написать версию `Map` для каждой пары типов, которую мы столкнулись, но это порождает ряд трудностей.</span><span class="sxs-lookup"><span data-stu-id="0be70-302">In principle, we could write a version of `Map` for every pair of types that we encounter, but this introduces a number of difficulties.</span></span>
<span data-ttu-id="0be70-303">Например, если обнаружена ошибка в `Map` , необходимо обеспечить единообразное применение исправления ко всем версиям `Map` .</span><span class="sxs-lookup"><span data-stu-id="0be70-303">For instance, if we find a bug in `Map`, then we must ensure that the fix is applied uniformly across all versions of `Map`.</span></span>
<span data-ttu-id="0be70-304">Более того, если мы создаем новый кортеж или определяемый пользователем тип, то теперь необходимо создать новый объект `Map` для перехода с новым типом.</span><span class="sxs-lookup"><span data-stu-id="0be70-304">Moreover, if we construct a new tuple or UDT, then we must now also construct a new `Map` to go along with the new type.</span></span>
<span data-ttu-id="0be70-305">Хотя это алгоритмизируемым для небольшого количества таких функций, так как мы соберем больше функций той же формы, что и `Map` , стоимость введения новых типов становится неоправданной в достаточно коротком порядке.</span><span class="sxs-lookup"><span data-stu-id="0be70-305">While this is tractable for a small number of such functions, as we collect more and more functions of the same form as `Map`, the cost of introducing new types becomes unreasonably large in fairly short order.</span></span>

<span data-ttu-id="0be70-306">Однако значительная часть этой сложности в том, что мы не предоставили компилятору сведения, необходимые для того, чтобы понять, как связаны разные версии `Map` .</span><span class="sxs-lookup"><span data-stu-id="0be70-306">Much of this difficulty results, however, from that the we have not given the compiler the information it needs to recognize how the different versions of `Map` are related.</span></span>
<span data-ttu-id="0be70-307">Фактически мы хотим, чтобы компилятор рассматривал `Map` как некоторую математическую функцию от q # *типов* до q # функций.</span><span class="sxs-lookup"><span data-stu-id="0be70-307">Effectively, we want the compiler to treat `Map` as some kind of mathematical function from Q# *types* to Q# functions.</span></span>

<span data-ttu-id="0be70-308">Это понятие формально позволяет функциям и операциям иметь *Параметры типа*, а также их обычные параметры кортежа.</span><span class="sxs-lookup"><span data-stu-id="0be70-308">This notion is formalized by allowing functions and operations to have *type parameters*, as well as their ordinary tuple parameters.</span></span>
<span data-ttu-id="0be70-309">В приведенных выше примерах мы будем рассматривать `Map` как параметры типа `Int, Pauli` в первом случае и `Double, String` во втором случае.</span><span class="sxs-lookup"><span data-stu-id="0be70-309">In the examples above, we wish to think of `Map` as having type parameters `Int, Pauli` in the first case and `Double, String` in the second case.</span></span>
<span data-ttu-id="0be70-310">В большинстве случаев эти параметры типа можно использовать, как будто они являются обычными типами: мы используем значения параметров типа для создания массивов и кортежей, вызова функций и операций и присваивания обычным или изменяемым переменным.</span><span class="sxs-lookup"><span data-stu-id="0be70-310">For the most part, these type parameters can then be used as though they were ordinary types: we use values of type parameters to make arrays and tuples, call functions and operations, and assign to ordinary or mutable variables.</span></span>

> [!NOTE]
> <span data-ttu-id="0be70-311">Самый крайний случай косвенной зависимости заключается в том, что Кубитс, где программа Q # не может напрямую полагаться на структуру `Qubit` типа, но **должна** передавать подобные типы другим операциям и функциям.</span><span class="sxs-lookup"><span data-stu-id="0be70-311">The most extreme case of indirect dependence is that of qubits, where a Q# program cannot directly rely on the structure of the `Qubit` type, but **must** pass such types to other operations and functions.</span></span>

<span data-ttu-id="0be70-312">Вернувшись к приведенному выше примеру, можно увидеть, что нам нужно `Map` иметь параметры типа, один для представления входных данных `fn` и один для представления выходных данных `fn` .</span><span class="sxs-lookup"><span data-stu-id="0be70-312">Returning to the example above, then, we can see that we need `Map` to have type parameters, one to represent the input to `fn` and one to represent the output from `fn`.</span></span>
<span data-ttu-id="0be70-313">В Q # это написано путем добавления угловых скобок (то есть `<>` не Бракетс $ \бракет {} $!) после имени функции или операции в ее объявлении, а также путем перечисления каждого параметра типа.</span><span class="sxs-lookup"><span data-stu-id="0be70-313">In Q#, this is written by adding angle brackets (that's `<>`, not brakets $\braket{}$!) after the name of a function or operation in its declaration, and by listing each type parameter.</span></span>
<span data-ttu-id="0be70-314">Имя каждого параметра типа должно начинаться с такта `'` , что означает, что это параметр типа, а не обычный тип (также известен как *конкретный* тип).</span><span class="sxs-lookup"><span data-stu-id="0be70-314">The name of each type parameter must start with a tick `'`, indicating that it is a type parameter and not a ordinary type (also known as a *concrete* type).</span></span>
<span data-ttu-id="0be70-315">Для `Map` , таким образом, мы пишем следующее:</span><span class="sxs-lookup"><span data-stu-id="0be70-315">For `Map`, we thus write:</span></span>

```qsharp
function Map<'Input, 'Output>(fn : ('Input -> 'Output), values : 'Input[]) : 'Output[] {
    mutable mappedValues = new 'Output[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

<span data-ttu-id="0be70-316">Обратите внимание, что определение `Map<'Input, 'Output>` выглядит очень похоже на версии, которые мы написали ранее.</span><span class="sxs-lookup"><span data-stu-id="0be70-316">Note that the definition of `Map<'Input, 'Output>` looks extremely similar to the versions we wrote out before.</span></span>
<span data-ttu-id="0be70-317">Единственное отличие заключается в том, что мы явно осведомлены о компиляторе, который `Map` напрямую не зависит от того `'Input` , что и `'Output` есть, но работает для любых двух типов, используя их косвенно с помощью `fn` .</span><span class="sxs-lookup"><span data-stu-id="0be70-317">The only difference is that we have explicitly informed the compiler that `Map` doesn't directly depend on what `'Input` and `'Output` are, but works for any two types by using them indirectly through `fn`.</span></span>
<span data-ttu-id="0be70-318">Как только мы определили `Map<'Input, 'Output>` этот способ, мы можем вызвать его, как будто это обычная функция:</span><span class="sxs-lookup"><span data-stu-id="0be70-318">Once we have defined `Map<'Input, 'Output>` in this way, we can call it as though it was an ordinary function:</span></span>

```qsharp
// Represent Z₀ Z₁ X₂ Y₃ as a list of ints.
let ints = [3, 3, 1, 2];
// Here, we assume IntToPauli : Int -> Pauli
// looks up PauliI by 0, PauliX by 1, so forth.
let paulis = Map(IntToPauli, ints);
```

> [!TIP]
> <span data-ttu-id="0be70-319">Написание универсальных функций и операций — это одно из мест, где «кортеж-в кортеже» — очень полезный способ подумать о функциях и операциях Q #.</span><span class="sxs-lookup"><span data-stu-id="0be70-319">Writing generic functions and operations is one place where "tuple-in tuple-out" is a very useful way to think about Q# functions and operations.</span></span>
> <span data-ttu-id="0be70-320">Поскольку каждая функция принимает ровно один вход и возвращает ровно один выход, входные данные типа `'T -> 'U` совпадают с *любыми* функциями Q #.</span><span class="sxs-lookup"><span data-stu-id="0be70-320">Since every function takes exactly one input and returns exactly one output, an input of type `'T -> 'U` matches *any* Q# function whatsoever.</span></span>
> <span data-ttu-id="0be70-321">Аналогичным образом любая операция может быть передана в входные данные типа `'T => 'U` .</span><span class="sxs-lookup"><span data-stu-id="0be70-321">Similarly, any operation can be passed to an input of type `'T => 'U`.</span></span>

<span data-ttu-id="0be70-322">Во втором примере рассмотрим задачу написания функции, возвращающей композицию двух других функций:</span><span class="sxs-lookup"><span data-stu-id="0be70-322">As a second example, consider the challenge of writing a function that returns the composition of two other functions:</span></span>

```qsharp
function ComposeImpl(outerFn : (B -> C), innerFn : (A -> B), input : A) : C {
    return outerFn(innerFn(input));
}

function Compose(outerFn : (B -> C), innerFn : (A -> B)) : (A -> C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

<span data-ttu-id="0be70-323">Здесь мы должны точно указать, что `A` `B` и, и `C` , следовательно, значительно ограничивать служебную программу нашей новой `Compose` функции.</span><span class="sxs-lookup"><span data-stu-id="0be70-323">Here, we must specify exactly what `A`, `B`, and `C` are, hence severely limiting the utility of our new `Compose` function.</span></span>
<span data-ttu-id="0be70-324">В конце концов, `Compose` только они зависят от `A` , `B` и `C` *через* `innerFn` и `outerFn` .</span><span class="sxs-lookup"><span data-stu-id="0be70-324">After all, `Compose` only depends on `A`, `B`, and `C` *via* `innerFn` and `outerFn`.</span></span>
<span data-ttu-id="0be70-325">В качестве альтернативы можно добавить параметры типа к `Compose` , которые указывают, что он работает для *всех* `A` , `B` и `C` , пока эти параметры соответствуют ожидаемым `innerFn` и `outerFn` :</span><span class="sxs-lookup"><span data-stu-id="0be70-325">As an alternative, then, we can add type parameters to `Compose` that indicate that it works for *any* `A`, `B`, and `C`, so long as these parameters match those expected by `innerFn` and `outerFn`:</span></span>

```qsharp
function ComposeImpl<'A, 'B, 'C>(outerFn : ('B -> 'C), innerFn : ('A -> 'B), input : 'A) : 'C {
    return outerFn(innerFn(input));
}

function Compose<'A, 'B, 'C>(outerFn : ('B -> 'C), innerFn : ('A -> 'B)) : ('A -> 'C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

<span data-ttu-id="0be70-326">Стандартные библиотеки Q # предоставляют ряд таких операций и функций с параметрами, которые позволяют более быстро выражать поток управления с более высоким порядком.</span><span class="sxs-lookup"><span data-stu-id="0be70-326">The Q# standard libraries provide a range of such type-parameterized operations and functions to make higher-order control flow easier to express.</span></span>
<span data-ttu-id="0be70-327">Они описаны далее в статье [рекомендации по стандартной библиотеке Q #](xref:microsoft.quantum.libraries.standard.intro).</span><span class="sxs-lookup"><span data-stu-id="0be70-327">These are discussed further in the [Q# standard library guide](xref:microsoft.quantum.libraries.standard.intro).</span></span>


## <a name="callables-as-first-class-values"></a><span data-ttu-id="0be70-328">Вызываемые как значения первого класса</span><span class="sxs-lookup"><span data-stu-id="0be70-328">Callables as First-Class Values</span></span>

<span data-ttu-id="0be70-329">Одной из важнейших методик для реализации потока управления и классической логики с помощью функций, а не операций является использование этих операций и функций в Q # — *первый класс*.</span><span class="sxs-lookup"><span data-stu-id="0be70-329">One critical technique for reasoning about control flow and classical logic using functions rather than operations is to utilize that operations and functions in Q# are *first-class*.</span></span>
<span data-ttu-id="0be70-330">То есть все значения на языке имеют свое право.</span><span class="sxs-lookup"><span data-stu-id="0be70-330">That is, they are each values in the language in their own right.</span></span>
<span data-ttu-id="0be70-331">Например, ниже приведен правильный код Q #, если немного косвенно:</span><span class="sxs-lookup"><span data-stu-id="0be70-331">For instance, the following is perfectly valid Q# code, if a little indirect:</span></span>

```qsharp
operation FirstClassExample(target : Qubit) : Unit {
    let ourH = H;
    ourH(target);
}
```

<span data-ttu-id="0be70-332">Значением переменной `ourH` в приведенном выше фрагменте является операция <xref:microsoft.quantum.intrinsic.h> , так что мы можем вызвать это значение, как любую другую операцию.</span><span class="sxs-lookup"><span data-stu-id="0be70-332">The value of the variable `ourH` in the snippet above is then the operation <xref:microsoft.quantum.intrinsic.h>, such that we can call that value like any other operation.</span></span>
<span data-ttu-id="0be70-333">Это позволяет нам писать операции, которые принимают операции в качестве части их входных данных, формируя основные понятия потока управления более высокого порядка.</span><span class="sxs-lookup"><span data-stu-id="0be70-333">This allows us to write operations that take operations as a part of their input, forming higher-order control flow concepts.</span></span>
<span data-ttu-id="0be70-334">Например, мы могли бы представить, что нужно "возкубит" операцию, применив ее дважды к той же цели.</span><span class="sxs-lookup"><span data-stu-id="0be70-334">For instance, we could imagine wanting to "square" an operation by applying it twice to the same target qubit.</span></span>

```qsharp
operation ApplyTwice(op : (Qubit => Unit), target : Qubit) : Unit {
    op(target);
    op(target);
}
```

### <a name="returning-operations-from-a-function"></a><span data-ttu-id="0be70-335">Возвращение операций из функции</span><span class="sxs-lookup"><span data-stu-id="0be70-335">Returning operations from a function</span></span>

<span data-ttu-id="0be70-336">Мы Подчеркните, что мы можем также возвращать операции как часть выходных данных, что позволяет изолировать некоторые виды классической условной логики в качестве классической функции, возвращающей описание тактовой программы в форме операции.</span><span class="sxs-lookup"><span data-stu-id="0be70-336">We emphasize that we can also return operations as a part of outputs, such that we can isolate some kinds of classical conditional logic as a classical function which returns a description of a quantum program in the form of an operation.</span></span>
<span data-ttu-id="0be70-337">В качестве простого примера рассмотрим пример использования телепередачи, в котором сторона, получающая 2-разрядное классическое сообщение, должна использовать сообщение для декодирования их кубит в соответствующее состояние в режиме «в Организации».</span><span class="sxs-lookup"><span data-stu-id="0be70-337">As a simple example, consider the teleportation example, in which the party receiving a two-bit classical message needs to use the message to decode their qubit into the proper teleported state.</span></span>
<span data-ttu-id="0be70-338">Мы можем написать это с точки зрения функции, которая принимает эти два классических битов и возвращает правильную операцию декодирования.</span><span class="sxs-lookup"><span data-stu-id="0be70-338">We could write this in terms of a function that takes those two classical bits and returns the proper decoding operation.</span></span>

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

<span data-ttu-id="0be70-339">Эта новая функция действительно является функцией. в этом случае, если мы вызываем ее с теми же значениями `hereBit` и `thereBit` , мы всегда вернемся к той же операции.</span><span class="sxs-lookup"><span data-stu-id="0be70-339">This new function is indeed a function, in that if we call it with the same values of `hereBit` and `thereBit`, we will always get back the same operation.</span></span>
<span data-ttu-id="0be70-340">Таким образом, декодер можно безопасно запускать внутри операций, не прибегая к причине того, как логика декодирования взаимодействует с определениями различных специализаций операций.</span><span class="sxs-lookup"><span data-stu-id="0be70-340">Thus, the decoder can be safely run inside operations without having to reason about how the decoding logic interacts with the definitions of the different operation specializations.</span></span>
<span data-ttu-id="0be70-341">То есть, мы разимпунити классическую логику внутри функции, гарантируя компилятору, что вызов функции может быть переупорядочен с помощью, пока сохраняются входные данные.</span><span class="sxs-lookup"><span data-stu-id="0be70-341">That is, we have isolated the classical logic inside a function, guaranteeing to the compiler that the function call can be reordered with impunity so long as the input is preserved.</span></span>


## <a name="partial-application"></a><span data-ttu-id="0be70-342">Частичное приложение</span><span class="sxs-lookup"><span data-stu-id="0be70-342">Partial Application</span></span>

<span data-ttu-id="0be70-343">Мы можем значительно повысить эффективность работы функций, возвращающих операции с помощью *частичного приложения*, в котором мы можем предоставить одну или несколько частей входных данных функции или операции без фактического их вызова.</span><span class="sxs-lookup"><span data-stu-id="0be70-343">We can do significantly more with functions that return operations by using *partial application*, in which we can provide one or more parts of the input to a function or operation without actually calling it.</span></span> <span data-ttu-id="0be70-344">Например, при повторном вызове приведенного `ApplyTwice` выше примера мы можем указать, что мы не хотим указывать, что нужно, чтобы кубит входную операцию:</span><span class="sxs-lookup"><span data-stu-id="0be70-344">For example, recalling the `ApplyTwice` example above, we can indicate that we don't want to specify, right away, to which qubit the input operation should apply:</span></span>

```qsharp
operation PartialApplicationExample(op : (Qubit => Unit), target : Qubit) : Unit {
    let twiceOp = ApplyTwice(op, _);
    twiceOp(target);
}
```

<span data-ttu-id="0be70-345">В этом случае локальная переменная `twiceOp` содержит операцию частичного применения `ApplyTwice(op, _)` , где части входных данных, которые еще не были указаны, обозначаются `_` .</span><span class="sxs-lookup"><span data-stu-id="0be70-345">In this case, the local variable `twiceOp` holds the partially applied operation `ApplyTwice(op, _)`, where parts of the input that have not yet been specified are indicated by `_`.</span></span>
<span data-ttu-id="0be70-346">Когда мы фактически вызываем `twiceOp` в следующей строке, мы передаем в качестве входных данных частично примененную операцию все оставшиеся части входных данных в исходную операцию.</span><span class="sxs-lookup"><span data-stu-id="0be70-346">When we actually call `twiceOp` in the next line, we pass as input to the partially applied operation all of the remaining parts of the input to the original operation.</span></span>
<span data-ttu-id="0be70-347">Таким образом, приведенный выше фрагмент кода фактически идентичен вызову `ApplyTwice(op, target)` напрямую, методу Save для этого мы предоставили новую локальную переменную, которая позволяет отложить вызов, в то же время предоставляя некоторые части входных данных.</span><span class="sxs-lookup"><span data-stu-id="0be70-347">Thus, the above snippet is effectively identical to having called `ApplyTwice(op, target)` directly, save for that we have introduced a new local variable that allows us to delay the call while providing some parts of the input.</span></span>

<span data-ttu-id="0be70-348">Так как операция, которая была частично применена, фактически не вызывается до тех пор, пока не будет предоставлен весь ввод, можно безопасно частично применить операции даже в рамках функций.</span><span class="sxs-lookup"><span data-stu-id="0be70-348">Since an operation that has been partially applied is not actually called until its entire input has been provided, we can safely partially apply operations even from within functions.</span></span>

```qsharp
function SquareOperation(op : (Qubit => Unit)) : (Qubit => Unit) {
    return ApplyTwice(op, _);
}
```

<span data-ttu-id="0be70-349">В принципе, классическая логика внутри `SquareOperation` может быть гораздо более сложной, но она по-прежнему изолирована от остальной части операции с помощью гарантий, что компилятор может предложить функции.</span><span class="sxs-lookup"><span data-stu-id="0be70-349">In principle, the classical logic within `SquareOperation` could have been much more involved, but it is still isolated from the rest of an operation by the guarantees that the compiler can offer about functions.</span></span>
<span data-ttu-id="0be70-350">Этот подход будет использоваться в стандартной библиотеке Q # для выражения классического потока управления способом, который можно легко использовать в тактовых программах.</span><span class="sxs-lookup"><span data-stu-id="0be70-350">This approach will be used throughout the Q# standard library for expressing classical control flow in a way that can be readily used within quantum programs.</span></span>


## <a name="recursion"></a><span data-ttu-id="0be70-351">Рекурсия</span><span class="sxs-lookup"><span data-stu-id="0be70-351">Recursion</span></span>

<span data-ttu-id="0be70-352">Возможность вызовов Q # может быть прямо или косвенно рекурсивной.</span><span class="sxs-lookup"><span data-stu-id="0be70-352">Q# callables are allowed to be directly or indirectly recursive.</span></span>
<span data-ttu-id="0be70-353">Это значит, что операция или функция может вызвать саму себя или вызвать другой вызываемый метод, который напрямую или косвенно вызывает вызываемую операцию.</span><span class="sxs-lookup"><span data-stu-id="0be70-353">That is, an operation or function may call itself, or it may call another callable that directly or indirectly calls the callable operation.</span></span>

<span data-ttu-id="0be70-354">Однако существует два важных комментария об использовании рекурсии.</span><span class="sxs-lookup"><span data-stu-id="0be70-354">There are two important comments about the use of recursion, however:</span></span>

- <span data-ttu-id="0be70-355">Использование рекурсии в операциях, скорее всего, мешает некоторым оптимизациям.</span><span class="sxs-lookup"><span data-stu-id="0be70-355">The use of recursion in operations is likely to interfere with certain optimizations.</span></span>
  <span data-ttu-id="0be70-356">Это может оказать значительное влияние на время выполнения алгоритма.</span><span class="sxs-lookup"><span data-stu-id="0be70-356">This may have a substantial impact on the execution time of the algorithm.</span></span>
- <span data-ttu-id="0be70-357">При выполнении на фактическом устройстве-такте пространство стека может быть ограничено, так что глубокая рекурсия может привести к ошибке времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="0be70-357">When executing on an actual quantum device, stack space may be limited, and so deep recursion may lead to a runtime error.</span></span>
  <span data-ttu-id="0be70-358">В частности, компилятор Q # и среда выполнения не выявляет и не оптимизируют заключительную рекурсию.</span><span class="sxs-lookup"><span data-stu-id="0be70-358">In particular, the Q# compiler and runtime do not identify and optimize tail recursion.</span></span>

## <a name="whats-next"></a><span data-ttu-id="0be70-359">Дальнейшая работа</span><span class="sxs-lookup"><span data-stu-id="0be70-359">What's Next?</span></span>
<span data-ttu-id="0be70-360">Сведения о [переменных](xref:microsoft.quantum.guide.variables) в Q #.</span><span class="sxs-lookup"><span data-stu-id="0be70-360">Learn about [Variables](xref:microsoft.quantum.guide.variables) in Q#.</span></span>