---
title: 'Q # операции и функции'
description: 'Сведения об операциях и функциях Q #, а также о том, как они применяются в тактовой программе.'
uid: microsoft.quantum.techniques.opsandfunctions
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 43f0cf2da192a607e514d0c7de57a9bdd067faf7
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907670"
---
# <a name="q-operations-and-functions"></a><span data-ttu-id="94175-103">Q # операции и функции</span><span class="sxs-lookup"><span data-stu-id="94175-103">Q# Operations and Functions</span></span>

<span data-ttu-id="94175-104">Программы Q # состоят из одной или нескольких *операций* , описывающих побочные эффекты, которые могут иметь тактовые операции, и одну или несколько *функций* , которые позволяют вносить изменения в классические данные.</span><span class="sxs-lookup"><span data-stu-id="94175-104">Q# programs consist of one or more *operations* that describe side effects quantum operations can have on quantum data, and one or more *functions* that allow modifications to classical data.</span></span> <span data-ttu-id="94175-105">В отличие от операций, функции используются для описания чистого поведения и не имеют каких либо эффектов, помимо вычисления классических выходных значений.</span><span class="sxs-lookup"><span data-stu-id="94175-105">In contrast to operations, functions are used to describe purely classical behavior and do not have any effects besides computing classical output values.</span></span>

<span data-ttu-id="94175-106">Каждая операция, определенная в Q #, может затем вызывать любое количество других операций, включая встроенные внутренние операции, определенные в языке.</span><span class="sxs-lookup"><span data-stu-id="94175-106">Each operation defined in Q# may then call any number of other operations, including the built-in intrinsic operations defined by the language.</span></span> <span data-ttu-id="94175-107">Конкретный способ определения этих внутренних операций зависит от целевого компьютера.</span><span class="sxs-lookup"><span data-stu-id="94175-107">The particular way in which these intrinsic operations are defined depends on the target machine.</span></span> <span data-ttu-id="94175-108">При компиляции каждая операция представляется как тип класса .NET, который можно предоставить целевым компьютерам.</span><span class="sxs-lookup"><span data-stu-id="94175-108">When compiled, each operation is represented as a .NET class type that can be provided to target machines.</span></span>

## <a name="defining-new-operations"></a><span data-ttu-id="94175-109">Определение новых операций</span><span class="sxs-lookup"><span data-stu-id="94175-109">Defining New Operations</span></span>

<span data-ttu-id="94175-110">Как описано выше, самый простой стандартный блок тактовой программы, написанный на Q #, — это *Операция*, которую можно вызывать из классических приложений .NET, например, с помощью симулятора или других операций в Q #.</span><span class="sxs-lookup"><span data-stu-id="94175-110">As described above, the most basic building block of a quantum program written in Q# is an *operation*, which can either be called from classical .NET applications, e.g., using a simulator, or by other operations within Q#.</span></span>
<span data-ttu-id="94175-111">Каждая операция принимает входные данные, создает выход и задает реализацию для одной или нескольких специализаций операций.</span><span class="sxs-lookup"><span data-stu-id="94175-111">Each operation takes an input, produces an output, and specifies the implementation for one or more operation specializations.</span></span>
<span data-ttu-id="94175-112">Например, следующая операция определяет только специализацию тела по умолчанию и принимает один кубит в качестве входных данных, а затем вызывает встроенную операцию `X` для этих входных данных:</span><span class="sxs-lookup"><span data-stu-id="94175-112">For instance, the following operation defines only a default body specialization and takes a single qubit as its input, then calls the built-in `X` operation on that input:</span></span>

```qsharp
operation BitFlip(target : Qubit) : Unit {
    X(target);
}
```

<span data-ttu-id="94175-113">Ключевое слово `operation` начинает определение операции, за которым следует имя; Здесь `BitFlip`.</span><span class="sxs-lookup"><span data-stu-id="94175-113">The keyword `operation` begins the operation definition, and is followed by the name; here, `BitFlip`.</span></span>
<span data-ttu-id="94175-114">Далее тип входных данных определяется как `Qubit`, а также имя `target` для ссылки на входные данные в новой операции.</span><span class="sxs-lookup"><span data-stu-id="94175-114">Next, the type of the input is defined as `Qubit`, along with a name `target` for referring to the input within the new operation.</span></span>
<span data-ttu-id="94175-115">Аналогичным образом `Unit` определяет, что выходные данные операции пусты.</span><span class="sxs-lookup"><span data-stu-id="94175-115">Similarly, the `Unit` defines that the operation's output is empty.</span></span>
<span data-ttu-id="94175-116">Он используется аналогично `void` в C# и других императивных языках и эквивалентен `unit` в F# и других функциональных языках.</span><span class="sxs-lookup"><span data-stu-id="94175-116">This is used similarly to `void` in C# and other imperative languages, and is equivalent to `unit` in F# and other functional languages.</span></span>

> [!NOTE]
> <span data-ttu-id="94175-117">Мы рассмотрим это более подробно, но каждая операция в Q # принимает ровно один вход и возвращает ровно один выход.</span><span class="sxs-lookup"><span data-stu-id="94175-117">We will explore this in more detail below, but each operation in Q# takes exactly one input and returns exactly one output.</span></span>
> <span data-ttu-id="94175-118">После этого несколько входов и выходов представляются с помощью *кортежей*, которые собираются несколько значений вместе в одно значение.</span><span class="sxs-lookup"><span data-stu-id="94175-118">Multiple inputs and outputs are then represented using *tuples*, which collect multiple values together into a single value.</span></span>
> <span data-ttu-id="94175-119">В неформальном случае мы говорим, что Q # — это «кортеж в кортеже».</span><span class="sxs-lookup"><span data-stu-id="94175-119">Informally, we say that Q# is a "tuple-in tuple-out" language.</span></span>
> <span data-ttu-id="94175-120">После этой концепции `()` следует считать "пустым" кортежом, который имеет тип `Unit`.</span><span class="sxs-lookup"><span data-stu-id="94175-120">Following this concept, `()` should then be read as the "empty" tuple, which has the type `Unit`.</span></span>

<span data-ttu-id="94175-121">В новой операции реализация может быть указана непосредственно в объявлении, если только реализация специализации тела по умолчанию должна быть указана явно.</span><span class="sxs-lookup"><span data-stu-id="94175-121">Within the new operation, the implementation can be specified directly within the declaration if only the implementation of the default body specialization needs to be specified explicitly.</span></span> <span data-ttu-id="94175-122">Кроме того, можно определить реализации, например одну или несколько операций `functor`, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="94175-122">Additionally, it is possible to define the implementations of, for example, one or more `functor` operations, as elaborated below.</span></span> <span data-ttu-id="94175-123">В приведенном выше примере единственным оператором является вызов встроенной операции Q # <xref:microsoft.quantum.intrinsic.x>.</span><span class="sxs-lookup"><span data-stu-id="94175-123">In the example above, the only statement is to call the built-in Q# operation <xref:microsoft.quantum.intrinsic.x>.</span></span>

<span data-ttu-id="94175-124">Операции могут также возвращать более интересные типы, чем `Unit`.</span><span class="sxs-lookup"><span data-stu-id="94175-124">Operations can also return more interesting types than `Unit`.</span></span>
<span data-ttu-id="94175-125">Например, операция <xref:microsoft.quantum.intrinsic.m> возвращает выходные данные типа `Result`, представляющие выполнение измерения.</span><span class="sxs-lookup"><span data-stu-id="94175-125">For instance, the <xref:microsoft.quantum.intrinsic.m> operation returns an output of type `Result`, representing having performed a measurement.</span></span> <span data-ttu-id="94175-126">Можно либо передать выходные данные операции в другую операцию, либо использовать ее с ключевым словом `let`, чтобы определить новую переменную.</span><span class="sxs-lookup"><span data-stu-id="94175-126">We can either pass the output from an operation to another operation, or can use it with the `let` keyword to define a new variable.</span></span>
<!-- Link to UID for superdense conceptual and example documentation. -->
<span data-ttu-id="94175-127">Это позволяет представить классические вычисления, взаимодействующие с операциями тактов на низком уровне, например в очень плотной кодировке:</span><span class="sxs-lookup"><span data-stu-id="94175-127">This allows for representing classical computation that interacts with quantum operations at a low level, such as in superdense coding:</span></span>

```qsharp
operation Superdense(here : Qubit, there : Qubit) : (Result, Result) {

    CNOT(there, here);
    H(there);

    let firstBit = M(there);
    let secondBit = M(here);

    return (firstBit, secondBit);
}
```
### <a name="functors-adjoint-and-controlled"></a><span data-ttu-id="94175-128">Операторов, прилегающий и управляемый</span><span class="sxs-lookup"><span data-stu-id="94175-128">Functors, adjoint and controlled</span></span>
<span data-ttu-id="94175-129">Если операция реализует единое преобразование, можно определить, как работает операция при *аджоинтед* или *управлении*.</span><span class="sxs-lookup"><span data-stu-id="94175-129">If an operation implements a unitary transformation, then it is possible to define how the operation acts when *adjointed* or *controlled*.</span></span> <span data-ttu-id="94175-130">В примыкающей специализации операции указывается, как она действует при выполнении в обратную, в то время как управляемая специализация указывает, как работает операция при условии, что оно применено к состоянию регистра такта.</span><span class="sxs-lookup"><span data-stu-id="94175-130">An adjoint specialization of an operation specifies how it acts when run in reverse, while a controlled specialization specifies how an operation acts when applied conditioned on the state of a quantum register.</span></span>
<span data-ttu-id="94175-131">Существование этих специализаций можно объявить как часть сигнатуры операции: `is Adj + Ctl` в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="94175-131">The existence of these specializations can be declared as part of the operation signature: `is Adj + Ctl` in the following example.</span></span> <span data-ttu-id="94175-132">Затем соответствующая реализация для каждой такой неявно объявленной специализации создается компилятором.</span><span class="sxs-lookup"><span data-stu-id="94175-132">The corresponding implementation for each such implicitly declared specialization is then generated by the compiler.</span></span> 

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit
is Adj + Ctl { // implies the existence of an adjoint, a controlled, and a controlled adjoint specialization
    H(here);
    CNOT(here, there);
}
```

> [!NOTE]
> <span data-ttu-id="94175-133">Многие операции в Q # представляют единые шлюзы.</span><span class="sxs-lookup"><span data-stu-id="94175-133">Many operations in Q# represent unitary gates.</span></span>
> <span data-ttu-id="94175-134">Если $U $ является единым шлюзом, представленным `U`операции, то `Adjoint U` представляет единую вентиль $U ^ \дагжер $.</span><span class="sxs-lookup"><span data-stu-id="94175-134">If $U$ is the unitary gate represented by an operation `U`, then `Adjoint U` represents the unitary gate $U^\dagger$.</span></span>

<span data-ttu-id="94175-135">В случае, если реализация не может быть создана компилятором, ее можно указать явно.</span><span class="sxs-lookup"><span data-stu-id="94175-135">In the case where the implementation cannot be generated by the compiler, it can be explicitly specified.</span></span> <span data-ttu-id="94175-136">Такие явные объявления специализации могут состоять из подходящей директивы создания или пользовательской реализации.</span><span class="sxs-lookup"><span data-stu-id="94175-136">Such explicit specialization declarations can consist of a suitable generation directive or a user defined implementation.</span></span> <span data-ttu-id="94175-137">Код в `PrepareEntangledPair` выше, например, эквивалентен приведенному ниже коду, содержащему явные объявления специализации:</span><span class="sxs-lookup"><span data-stu-id="94175-137">The code in `PrepareEntangledPair` above for example is equivalent to the code below containing explicit specialization declarations:</span></span> 

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit {
    body (...) { // default body specialization
        H(here);
        CNOT(here, there);
    }

    adjoint auto; // auto-generate adjoint specialization
    controlled auto; // auto-generate controlled specialization
    controlled adjoint auto; // auto-generate controlled adjoint specialization
}
```
<span data-ttu-id="94175-138">Ключевое слово `auto` указывает, что компилятор должен определить способ создания реализации специализации.</span><span class="sxs-lookup"><span data-stu-id="94175-138">The keyword `auto` indicates that the compiler should determine how to generate the specialization implementation.</span></span>
<span data-ttu-id="94175-139">Если компилятор не может автоматически создать реализацию для определенной специализации или если может быть предоставлена более эффективная реализация, то реализация может быть также определена вручную.</span><span class="sxs-lookup"><span data-stu-id="94175-139">If the compiler cannot generate the implementation for a certain specialization automatically, or if a more efficient implementation can be given, then the implementation may also be manually defined.</span></span>

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
<span data-ttu-id="94175-140">В приведенном выше примере `adjoint invert;` указывает, что примыкающая специализация должна быть создана путем инвертирования реализации тела, а `controlled adjoint invert;` указывает, что управляемая примыкающая специализация должна быть создана путем инвертирования заданной реализации управляемой специализации.</span><span class="sxs-lookup"><span data-stu-id="94175-140">In the example above, `adjoint invert;` indicates that the adjoint specialization is to be generated by inverting the body implementation, and `controlled adjoint invert;` indicates that the controlled adjoint specialization is to be generated by inverting the given implementation of the controlled specialization.</span></span>

<span data-ttu-id="94175-141">В [потоке управления более высокого порядка](xref:microsoft.quantum.concepts.control-flow)будут рассмотрены дополнительные примеры.</span><span class="sxs-lookup"><span data-stu-id="94175-141">We will see more examples of this in [Higher-Order Control Flow](xref:microsoft.quantum.concepts.control-flow).</span></span>

<span data-ttu-id="94175-142">Чтобы вызвать специализацию операции, используйте ключевые слова `Adjoint` или `Controlled`.</span><span class="sxs-lookup"><span data-stu-id="94175-142">To call a specialization of an operation, use the `Adjoint` or `Controlled` keywords.</span></span>
<span data-ttu-id="94175-143">Например, приведенный выше пример кода можно написать более компактно, используя смежную часть `PrepareEntangledPair` для преобразования запутанными состояния обратно в унентанглед пару Кубитс:</span><span class="sxs-lookup"><span data-stu-id="94175-143">For example, the superdense coding example above can be written more compactly by using the adjoint of `PrepareEntangledPair` to transform the entangled state back into an unentangled pair of qubits:</span></span>

```qsharp
operation Superdense(here : Qubit, there : Qubit) : (Result, Result) {
    Adjoint PrepareEntangledPair(there, here);

    let firstBit = M(there);
    let secondBit = M(here);

    return (firstBit, secondBit);
}
```

<span data-ttu-id="94175-144">При проектировании операций для использования с операторов необходимо учитывать ряд важных ограничений.</span><span class="sxs-lookup"><span data-stu-id="94175-144">There are a number of important limitations to consider when designing operations for use with functors.</span></span>
<span data-ttu-id="94175-145">Как правило, специализации для операции, которая использует выходное значение любой другой операции, не могут быть созданы компилятором автоматически, так как это неоднозначно, как изменить порядок инструкций в такой операции, чтобы получить такой же результат.</span><span class="sxs-lookup"><span data-stu-id="94175-145">Most critically, specializations for an operation that uses the output value of any other operation cannot be auto-generated by the compiler, as it is ambiguous how to reorder the statements in such an operation to obtain the same effect.</span></span>


## <a name="defining-new-functions"></a><span data-ttu-id="94175-146">Определение новых функций</span><span class="sxs-lookup"><span data-stu-id="94175-146">Defining New Functions</span></span>

<span data-ttu-id="94175-147">Q # также позволяет определять *функции*, которые отличаются от операций тем, что они не могут иметь каких бы то ни было последствий, чем вычисление выходного значения.</span><span class="sxs-lookup"><span data-stu-id="94175-147">Q# also allows for defining *functions*, which are distinct from operations in that they are not allowed to have any effects beyond calculating an output value.</span></span>
<span data-ttu-id="94175-148">В частности, функции не могут вызывать операции, действовать для Кубитс, примеры случайных чисел или иным образом зависят от состояния, превышающего входное значение функции.</span><span class="sxs-lookup"><span data-stu-id="94175-148">In particular, functions cannot call operations, act on qubits, sample random numbers, or otherwise depend on state beyond the input value to a function.</span></span>
<span data-ttu-id="94175-149">Как следствие, функции Q # являются *чисто*, в том, что они всегда сопоставляют одинаковые входные значения с одними и теми же выходными значениями.</span><span class="sxs-lookup"><span data-stu-id="94175-149">As a consequence, Q# functions are *pure*, in that they always map the same input values to the same output values.</span></span>
<span data-ttu-id="94175-150">Это позволяет компилятору Q # безопасно изменять порядок и время вызова функций при создании специализаций операций.</span><span class="sxs-lookup"><span data-stu-id="94175-150">This allows the Q# compiler to safely reorder how and when functions are called when generating operation specializations.</span></span>

<span data-ttu-id="94175-151">Определение функции работает аналогично определению операции, за исключением того, что для функции нельзя определить ни прилегающие, ни контролируемые специализации.</span><span class="sxs-lookup"><span data-stu-id="94175-151">Defining a function works similarly to defining an operation, except that no adjoint or controlled specializations can be defined for a function.</span></span>
<span data-ttu-id="94175-152">например</span><span class="sxs-lookup"><span data-stu-id="94175-152">For instance:</span></span>

```qsharp
function Square(x : Double) : (Double) {
    return x * x;
}
```
<span data-ttu-id="94175-153">Когда это возможно, полезно писать классическую логику с точки зрения функций, а не операций, чтобы его можно было использовать в рамках операций.</span><span class="sxs-lookup"><span data-stu-id="94175-153">Whenever it is possible to do so, it is helpful to write out classical logic in terms of functions rather than operations, so that it can be more readily used from within operations.</span></span>
<span data-ttu-id="94175-154">Например, если бы в качестве операции было написано `Square`, компилятор не сможет гарантировать, что его вызов с теми же входными данными получит одинаковые выходные данные.</span><span class="sxs-lookup"><span data-stu-id="94175-154">If we had written `Square` as an operation, for example, then the compiler would not have been able to guarantee that calling it with the same input would consistently produce the same outputs.</span></span>

<span data-ttu-id="94175-155">Чтобы подчеркнуть разницу между функциями и операциями, рассмотрим проблему с классической выборкой случайного числа в операции Q #:</span><span class="sxs-lookup"><span data-stu-id="94175-155">To underscore the difference between functions and operations, consider the problem of classically sampling a random number from within a Q# operation:</span></span>

```qsharp
operation U(target : Qubit) : Unit {

    let angle = RandomReal()
    Rz(angle, target)
}
```

<span data-ttu-id="94175-156">Каждый раз, когда вызывается `U`, он будет иметь другое действие в `target`.</span><span class="sxs-lookup"><span data-stu-id="94175-156">Each time that `U` is called, it will have a different action on `target`.</span></span>
<span data-ttu-id="94175-157">В частности, компилятор не может гарантировать, что если мы добавили объявление специализации `adjoint auto` для `U`, `U(target); Adjoint U(target);` будет выступать в качестве удостоверения (т. е. без операции).</span><span class="sxs-lookup"><span data-stu-id="94175-157">In particular, the compiler cannot guarantee that if we added an `adjoint auto` specialization declaration to `U`, then `U(target); Adjoint U(target);` acts as identity (that is, as a no-op).</span></span>
<span data-ttu-id="94175-158">Это нарушает определение примыкающего, которое мы видели в [векторах и матрицах](xref:microsoft.quantum.concepts.vectors), что позволяет автоматически формировать смежную специализацию в операции, в которой мы вызвали операцию <xref:microsoft.quantum.math.randomreal> нарушают гарантии, предоставляемые компилятором. <xref:microsoft.quantum.math.randomreal> — это операция, для которой не существует ни одной примыкающей или контролируемой версии.</span><span class="sxs-lookup"><span data-stu-id="94175-158">This violates the definition of the adjoint that we saw in [Vectors and Matrices](xref:microsoft.quantum.concepts.vectors), such that allowing to auto-generate an adjoint specialization in an operation where we have called the operation <xref:microsoft.quantum.math.randomreal> would break the guarantees provided by the compiler; <xref:microsoft.quantum.math.randomreal> is an operation for which no adjoint or controlled version exists.</span></span>

<span data-ttu-id="94175-159">С другой стороны, разрешение вызовов функций, таких как `Square`, является надежным, в том, что компилятор может быть уверенным в том, что необходимо сохранить входные данные для `Square`, чтобы обеспечить стабильную работу.</span><span class="sxs-lookup"><span data-stu-id="94175-159">On the other hand, allowing function calls such as `Square` is safe, in that the compiler can be assured that it only needs to preserve the input to `Square` in order to keep its output stable.</span></span>
<span data-ttu-id="94175-160">Таким образом, изоляция максимально возможной логики функций позволяет легко повторно использовать эту логику в других функциях и операциях.</span><span class="sxs-lookup"><span data-stu-id="94175-160">Thus, isolating as much classical logic as possible into functions makes it easy to reuse that logic in other functions and operations alike.</span></span>

## <a name="control-flow"></a><span data-ttu-id="94175-161">Поток управления</span><span class="sxs-lookup"><span data-stu-id="94175-161">Control Flow</span></span>

<span data-ttu-id="94175-162">Внутри операции или функции каждая инструкция выполняется по порядку, аналогично наиболее распространенным императивным классическим языкам.</span><span class="sxs-lookup"><span data-stu-id="94175-162">Within an operation or function, each statement executes in order, similar to most common imperative classical languages.</span></span>
<span data-ttu-id="94175-163">Однако этот поток управления можно изменить тремя разными способами:</span><span class="sxs-lookup"><span data-stu-id="94175-163">This flow of control can be modified, however, in three distinct ways:</span></span>

- <span data-ttu-id="94175-164">Операторы `if`</span><span class="sxs-lookup"><span data-stu-id="94175-164">`if` Statements</span></span>
- <span data-ttu-id="94175-165">Циклы `for`</span><span class="sxs-lookup"><span data-stu-id="94175-165">`for` Loops</span></span>
- <span data-ttu-id="94175-166">Циклы `until` -`repeat`</span><span class="sxs-lookup"><span data-stu-id="94175-166">`repeat`-`until` Loops</span></span>

<span data-ttu-id="94175-167">Мы относимся к рассказу о втором, пока не будем обсуждать каналы [повторения](xref:microsoft.quantum.techniques.qubits#measurements) .</span><span class="sxs-lookup"><span data-stu-id="94175-167">We defer discussion of the latter until we discuss [Repeat Until Success (RUS)](xref:microsoft.quantum.techniques.qubits#measurements) circuits.</span></span>
<span data-ttu-id="94175-168">Однако конструкции потока управления `if` и `for` имеют привычный смысл для большинства классических языков программирования.</span><span class="sxs-lookup"><span data-stu-id="94175-168">The `if` and `for` control flow constructs, however, proceed in a familiar sense to most classical programming languages.</span></span>
<span data-ttu-id="94175-169">В частности, оператор `if` может принять условие, за которым может следовать одна или несколько `elif`ных инструкций и может заканчиваться `else`:</span><span class="sxs-lookup"><span data-stu-id="94175-169">In particular, an `if` statement can take a condition, may be followed by one or more `elif` statements, and may end with an `else`:</span></span>

```qsharp
if (pauli == PauliX) {
    X(qubit);
} elif (pauli == PauliY) {
    Y(qubit);
} elif (pauli == PauliZ) {
    Z(qubit);
} else {
    fail "Cannot use PauliI here.";
}
```

<span data-ttu-id="94175-170">Аналогичным образом `for` циклы указывают на итерацию для диапазона целых чисел или элементов массива.</span><span class="sxs-lookup"><span data-stu-id="94175-170">Similarly, `for` loops indicate iteration over a range of integers or over the elements of an array:</span></span>

```qsharp
for (idxQubit in 0..nQubits - 1) {
    // Do something to idxQubit...
}
```

<span data-ttu-id="94175-171">Что важнее, `for` циклы и операторы `if` можно использовать даже в операциях, для которых автоматически создаются специализации.</span><span class="sxs-lookup"><span data-stu-id="94175-171">Importantly, `for` loops and `if` statements can even be used in operations for which specializations are auto-generated.</span></span> <span data-ttu-id="94175-172">В этом случае смежная часть цикла `for` меняет направление на противоположное и принимает смежную часть каждой итерации.</span><span class="sxs-lookup"><span data-stu-id="94175-172">In that case the adjoint of a `for` loop reverses the direction and takes the adjoint of each iteration.</span></span>
<span data-ttu-id="94175-173">Это соответствует принципу "обувь-and-Socks": Если вы хотите отменить размещение по протоколу SOCKS, а затем обувь, необходимо отменить помещение обувь, а затем отменить последующую операцию по протоколу SOCKS.</span><span class="sxs-lookup"><span data-stu-id="94175-173">This follows the "shoes-and-socks" principle: if you wish to undo putting on socks and then shoes, you must undo putting on shoes and then undo putting on socks.</span></span>
<span data-ttu-id="94175-174">Это решение работает менее эффективно, и вы можете использовать протокол Socks, пока вы по-прежнему людьмие обувь!</span><span class="sxs-lookup"><span data-stu-id="94175-174">It works decidedly less well to try and take your socks off while you're still wearing your shoes!</span></span>

## <a name="operations-and-functions-as-first-class-values"></a><span data-ttu-id="94175-175">Операции и функции в качестве значений первого класса</span><span class="sxs-lookup"><span data-stu-id="94175-175">Operations and Functions as First-Class Values</span></span>

<span data-ttu-id="94175-176">Одной из важнейших методик для реализации потока управления и классической логики с помощью функций, а не операций является использование этих операций и функций в Q # — *первый класс*.</span><span class="sxs-lookup"><span data-stu-id="94175-176">One critical technique for reasoning about control flow and classical logic using functions rather than operations is to utilize that operations and functions in Q# are *first-class*.</span></span>
<span data-ttu-id="94175-177">То есть все значения на языке имеют свое право.</span><span class="sxs-lookup"><span data-stu-id="94175-177">That is, they are each values in the language in their own right.</span></span>
<span data-ttu-id="94175-178">Например, ниже приведен правильный код Q #, если немного косвенно:</span><span class="sxs-lookup"><span data-stu-id="94175-178">For instance, the following is perfectly valid Q# code, if a little indirect:</span></span>

```qsharp
operation FirstClassExample(target : Qubit) : Unit {
    let ourH = H;
    ourH(target);
}
```

<span data-ttu-id="94175-179">Значение переменной, `ourH` в приведенном выше фрагменте, — это операция, <xref:microsoft.quantum.intrinsic.h>, так что мы можем вызвать это значение, как любую другую операцию.</span><span class="sxs-lookup"><span data-stu-id="94175-179">The value of the variable `ourH` in the snippet above is then the operation <xref:microsoft.quantum.intrinsic.h>, such that we can call that value like any other operation.</span></span>
<span data-ttu-id="94175-180">Это позволяет нам писать операции, которые принимают операции в качестве части их входных данных, формируя основные понятия потока управления более высокого порядка.</span><span class="sxs-lookup"><span data-stu-id="94175-180">This allows us to write operations that take operations as a part of their input, forming higher-order control flow concepts.</span></span>
<span data-ttu-id="94175-181">Например, мы могли бы представить, что нужно "возкубит" операцию, применив ее дважды к той же цели.</span><span class="sxs-lookup"><span data-stu-id="94175-181">For instance, we could imagine wanting to "square" an operation by applying it twice to the same target qubit.</span></span>

```qsharp
operation ApplyTwice(op : (Qubit => Unit), target : Qubit) : Unit {
    op(target);
    op(target);
}
```

<span data-ttu-id="94175-182">В этом примере стрелка `=>`, которая отображается в `(Qubit => Unit)` типа, означает, что поле ввода `op` является операцией, которая принимает в качестве входных данных тип `Qubit` и создает в качестве выходных данных пустой кортеж.</span><span class="sxs-lookup"><span data-stu-id="94175-182">In this example, the `=>` arrow that appears in the type `(Qubit => Unit)` denotes that the input field `op` is an operation which takes as its input the type `Qubit` and produces an empty tuple as its output.</span></span>
<span data-ttu-id="94175-183">Кроме того, мы указываем характеристики типа операции, которые содержат сведения о поддерживаемых операторов.</span><span class="sxs-lookup"><span data-stu-id="94175-183">Additionally we specify the characteristics of that operation type, which contain the information about which functors are supported.</span></span>
<span data-ttu-id="94175-184">Операция типа `(Qubit => Unit)` не поддерживает ни `Adjoint`, ни `Controlled` функтор.</span><span class="sxs-lookup"><span data-stu-id="94175-184">An operation of type `(Qubit => Unit)` supports neither the `Adjoint` nor the `Controlled` functor.</span></span> <span data-ttu-id="94175-185">Если нам нужно указать, что операция этого типа должна поддерживать, например `Adjoint` функтор, нам нужно объявить ее как аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="94175-185">If we want to indicate that an operation of that type has to support e.g. the `Adjoint` functor, we have to declare it as being adjointable.</span></span> <span data-ttu-id="94175-186">Это делается с помощью аннотации, `is Adj` типу.</span><span class="sxs-lookup"><span data-stu-id="94175-186">This is done by using the annotation `is Adj` to the type.</span></span> <span data-ttu-id="94175-187">Аналогичным образом `(Qubit => Unit is Ctl)` указывает, что операция этого типа поддерживает `Controlled` функтор.</span><span class="sxs-lookup"><span data-stu-id="94175-187">Similarly, `(Qubit => Unit is Ctl)` denotes that an operation of that type supports the `Controlled` functor.</span></span> <span data-ttu-id="94175-188">Мы рассмотрим это Подробнее, когда мы обсудим [типы в разделе вопросы и ответы](xref:microsoft.quantum.language.type-model) .</span><span class="sxs-lookup"><span data-stu-id="94175-188">We will explore this further when we discuss [types in Q#](xref:microsoft.quantum.language.type-model) more generally.</span></span>

<span data-ttu-id="94175-189">Сейчас мы Подчеркните, что мы можем также возвращать операции как часть выходных данных, что позволяет изолировать некоторые виды классической условной логики в качестве классической функции, возвращающей описание тактовой программы в форме операции.</span><span class="sxs-lookup"><span data-stu-id="94175-189">For now, we emphasize that we can also return operations as a part of outputs, such that we can isolate some kinds of classical conditional logic as a classical function which returns a description of a quantum program in the form of an operation.</span></span>
<span data-ttu-id="94175-190">В качестве простого примера рассмотрим пример использования телепередачи, в котором сторона, получающая 2-разрядное классическое сообщение, должна использовать сообщение для декодирования их кубит в соответствующее состояние в режиме «в Организации».</span><span class="sxs-lookup"><span data-stu-id="94175-190">As a simple example, consider the teleportation example, in which the party receiving a two-bit classical message needs to use the message to decode their qubit into the proper teleported state.</span></span>
<span data-ttu-id="94175-191">Мы можем написать это с точки зрения функции, которая принимает эти два классических битов и возвращает правильную операцию декодирования.</span><span class="sxs-lookup"><span data-stu-id="94175-191">We could write this in terms of a function that takes those two classical bits and returns the proper decoding operation.</span></span>

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

<span data-ttu-id="94175-192">Эта новая функция действительно является функцией. в этом случае, если мы вызываем ее с теми же значениями `hereBit` и `thereBit`, мы всегда вернемся к той же операции.</span><span class="sxs-lookup"><span data-stu-id="94175-192">This new function is indeed a function, in that if we call it with the same values of `hereBit` and `thereBit`, we will always get back the same operation.</span></span>
<span data-ttu-id="94175-193">Таким образом, декодер можно безопасно запускать внутри операций, не прибегая к причине того, как логика декодирования взаимодействует с определениями различных специализаций операций.</span><span class="sxs-lookup"><span data-stu-id="94175-193">Thus, the decoder can be safely run inside operations without having to reason about how the decoding logic interacts with the definitions of the different operation specializations.</span></span>
<span data-ttu-id="94175-194">То есть, мы разимпунити классическую логику внутри функции, гарантируя компилятору, что вызов функции может быть переупорядочен с помощью, пока сохраняются входные данные.</span><span class="sxs-lookup"><span data-stu-id="94175-194">That is, we have isolated the classical logic inside a function, guaranteeing to the compiler that the function call can be reordered with impunity so long as the input is preserved.</span></span>

<span data-ttu-id="94175-195">Мы также можем рассматривать функции как значения первого класса, так как мы увидим более подробное описание [операций и типов функций](#operations-and-functions-as-first-class-values).</span><span class="sxs-lookup"><span data-stu-id="94175-195">We can also treat functions as first-class values, as we will see in more detail when we discuss [operations and function types](#operations-and-functions-as-first-class-values).</span></span>

## <a name="partially-applying-operations-and-functions"></a><span data-ttu-id="94175-196">Частичное применение операций и функций</span><span class="sxs-lookup"><span data-stu-id="94175-196">Partially Applying Operations and Functions</span></span>

<span data-ttu-id="94175-197">Мы можем значительно повысить эффективность работы функций, возвращающих операции с помощью *частичного приложения*, в котором мы можем предоставить одну или несколько частей входных данных функции или операции без фактического их вызова.</span><span class="sxs-lookup"><span data-stu-id="94175-197">We can do significantly more with functions that return operations by using *partial application*, in which we can provide one or more parts of the input to a function or operation without actually calling it.</span></span> <span data-ttu-id="94175-198">Например, при повторном вызове приведенного выше примера `ApplyTwice` мы можем указать, что мы не хотим указывать, что нужно, чтобы кубит входную операцию:</span><span class="sxs-lookup"><span data-stu-id="94175-198">For example, recalling the `ApplyTwice` example above, we can indicate that we don't want to specify, right away, to which qubit the input operation should apply:</span></span>

```qsharp
operation PartialApplicationExample(op : (Qubit => Unit), target : Qubit) : Unit {
    let twiceOp = ApplyTwice(op, _);
    twiceOp(target);
}
```

<span data-ttu-id="94175-199">В этом случае локальная переменная `twiceOp` содержит частично примененную операцию `ApplyTwice(op, _)`, где части входных данных, которые еще не были указаны, обозначаются `_`.</span><span class="sxs-lookup"><span data-stu-id="94175-199">In this case, the local variable `twiceOp` holds the partially applied operation `ApplyTwice(op, _)`, where parts of the input that have not yet been specified are indicated by `_`.</span></span>
<span data-ttu-id="94175-200">Когда мы вызываем `twiceOp` в следующей строке, мы передаем в качестве входных данных частично примененную операцию все оставшиеся части входных данных в исходную операцию.</span><span class="sxs-lookup"><span data-stu-id="94175-200">When we actually call `twiceOp` in the next line, we pass as input to the partially applied operation all of the remaining parts of the input to the original operation.</span></span>
<span data-ttu-id="94175-201">Таким образом, приведенный выше фрагмент кода фактически идентичен вызову `ApplyTwice(op, target)` напрямую, сохранить для того, что мы предоставили новую локальную переменную, которая позволяет отложить вызов, предоставляя некоторые части входных данных.</span><span class="sxs-lookup"><span data-stu-id="94175-201">Thus, the above snippet is effectively identical to having called `ApplyTwice(op, target)` directly, save for that we have introduced a new local variable that allows us to delay the call while providing some parts of the input.</span></span>

<span data-ttu-id="94175-202">Так как операция, которая была частично применена, фактически не вызывается до тех пор, пока не будет предоставлен весь ввод, можно безопасно частично применить операции даже в рамках функций.</span><span class="sxs-lookup"><span data-stu-id="94175-202">Since an operation that has been partially applied is not actually called until its entire input has been provided, we can safely partially apply operations even from within functions.</span></span>

```qsharp
function SquareOperation(op : (Qubit => Unit)) : (Qubit => Unit) {
    return ApplyTwice(op, _);
}
```

<span data-ttu-id="94175-203">В принципе, классическая логика в `SquareOperation` может быть гораздо более сложной, но она по-прежнему изолирована от остальной части операции с помощью гарантий, что компилятор может предложить функции.</span><span class="sxs-lookup"><span data-stu-id="94175-203">In principle, the classical logic within `SquareOperation` could have been much more involved, but it is still isolated from the rest of an operation by the guarantees that the compiler can offer about functions.</span></span>
<span data-ttu-id="94175-204">Этот подход будет использоваться в стандартной библиотеке Q # для выражения классического потока управления способом, который можно легко использовать в тактовых программах.</span><span class="sxs-lookup"><span data-stu-id="94175-204">This approach will be used throughout the Q# standard library for expressing classical control flow in a way that can be readily used within quantum programs.</span></span>
