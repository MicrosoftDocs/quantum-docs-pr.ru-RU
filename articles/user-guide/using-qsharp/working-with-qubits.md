---
title: Работа с кубитами
description: Описание заливки
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.qubits
ms.openlocfilehash: e89b9ccfe2a0796e01eedfc99f7ce71038d85f38
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2020
ms.locfileid: "83430940"
---
# <a name="working-with-qubits"></a><span data-ttu-id="8da08-103">Работа с кубитами</span><span class="sxs-lookup"><span data-stu-id="8da08-103">Working with qubits</span></span>

<span data-ttu-id="8da08-104">Теперь, когда вы видели множество различных частей языка Q #, позвольте нам пробавиться от него и увидеть, как использовать сами Кубитс.</span><span class="sxs-lookup"><span data-stu-id="8da08-104">Having now seen a variety of different parts of the Q# language, let us get into the thick of it and see how to use qubits themselves.</span></span>

<span data-ttu-id="8da08-105">Обратите внимание, что ни одна из этих инструкций не разрешена в теле функции.</span><span class="sxs-lookup"><span data-stu-id="8da08-105">Note that none of these statements are allowed within the body of a function.</span></span>
<span data-ttu-id="8da08-106">Они действительны только в пределах операций.</span><span class="sxs-lookup"><span data-stu-id="8da08-106">They are only valid within operations.</span></span>

## <a name="allocating-qubits"></a><span data-ttu-id="8da08-107">Выделение Кубитс</span><span class="sxs-lookup"><span data-stu-id="8da08-107">Allocating Qubits</span></span>

### <a name="clean-qubits"></a><span data-ttu-id="8da08-108">Очистить Кубитс</span><span class="sxs-lookup"><span data-stu-id="8da08-108">Clean qubits</span></span>

<span data-ttu-id="8da08-109">`using`Оператор используется для *выделения* нового Кубитс для использования в блоке инструкций.</span><span class="sxs-lookup"><span data-stu-id="8da08-109">The `using` statement is used to *allocate* new qubits for use during a statement block.</span></span>

<span data-ttu-id="8da08-110">Оператор состоит из ключевого слова `using` , открывающей скобки, `(` привязки, закрывающей скобки `)` и блока инструкций, в котором Кубитс будет доступен.</span><span class="sxs-lookup"><span data-stu-id="8da08-110">The statement consists of the keyword `using`, followed by an open parenthesis `(`, a binding, a close parenthesis `)`, and the statement block within which the qubits will be available.</span></span>
<span data-ttu-id="8da08-111">Привязка соответствует тому же шаблону, что и `let` инструкции: один символ или кортеж символов, за которым следует знак равенства `=` и одно значение или соответствующий кортеж *инициализаторов*.</span><span class="sxs-lookup"><span data-stu-id="8da08-111">The binding follows the same pattern as `let` statements: either a single symbol or a tuple of symbols, followed by an equals sign `=`, and either a single value or a matching tuple of *initializers*.</span></span>

<span data-ttu-id="8da08-112">Инициализаторы доступны для одного кубит, обозначенного как `Qubit()` , или массива Кубитс, `Qubit[n]` , где `n` является `Int` выражением.</span><span class="sxs-lookup"><span data-stu-id="8da08-112">Initializers are available either for a single qubit, indicated as `Qubit()`, or an array of qubits, `Qubit[n]`, where `n` is an `Int` expression.</span></span>
<span data-ttu-id="8da08-113">Например, примененная к объекту директива</span><span class="sxs-lookup"><span data-stu-id="8da08-113">For example,</span></span>

```qsharp
using (qubit = Qubit()) {
    // ...
}
using ((auxiliary, register) = (Qubit(), Qubit[5])) {
    // ...
}
```

<span data-ttu-id="8da08-114">Все Кубитс, выделенные таким образом, запускаются в $ \кет {0} $ State; в приведенном выше примере `register` — в состоянии $ \кет {00000} = \кет {0} \отимес \кет {0} \отимес \кдотс \отимес \кет {0} $.</span><span class="sxs-lookup"><span data-stu-id="8da08-114">Any qubits allocated in this way start off in the $\ket{0}$ state; in the example above, `register` is thus in the state $\ket{00000} = \ket{0} \otimes \ket{0} \otimes \cdots \otimes \ket{0}$.</span></span>
<span data-ttu-id="8da08-115">В конце `using` блока все Кубитс, выделенные этим блоком, немедленно освобождаются и не могут использоваться дальше.</span><span class="sxs-lookup"><span data-stu-id="8da08-115">At the end of the `using` block, any qubits allocated by that block are immediately deallocated and cannot be used further.</span></span>

> [!WARNING]
> <span data-ttu-id="8da08-116">Целевые компьютеры предполагают, что Кубитс находятся в состоянии $ \кет {0} $ непосредственно перед освобождением, чтобы их можно было повторно использовать и предоставлять другим `using` блокам для выделения.</span><span class="sxs-lookup"><span data-stu-id="8da08-116">Target machines expect that qubits are in the $\ket{0}$ state immediately before deallocation, so that they can be reused and offered to other `using` blocks for allocation.</span></span>
> <span data-ttu-id="8da08-117">По возможности используйте единые операции для возврата всех выделенных Кубитс в $ \кет {0} $.</span><span class="sxs-lookup"><span data-stu-id="8da08-117">Whenever possible, use unitary operations to return any allocated qubits to $\ket{0}$.</span></span>
> <span data-ttu-id="8da08-118">При необходимости @"microsoft.quantum.intrinsic.reset" можно использовать операцию для измерения кубит и использовать этот результат измерения, чтобы гарантировать, что измеряемый кубит возвращается в $ \кет {0} $.</span><span class="sxs-lookup"><span data-stu-id="8da08-118">If need be, the @"microsoft.quantum.intrinsic.reset" operation can be used to measure a qubit instead, and to use that measurement result to ensure that the measured qubit is returned to $\ket{0}$.</span></span> <span data-ttu-id="8da08-119">Такое измерение приведет к уничтожению всех замкнутые с оставшимся Кубитс и может повлиять на вычисление.</span><span class="sxs-lookup"><span data-stu-id="8da08-119">Such a measurement will destroy any entanglement with the remaining qubits and can thus impact the computation.</span></span>


### <a name="borrowed-qubits"></a><span data-ttu-id="8da08-120">Заимствованный Кубитс</span><span class="sxs-lookup"><span data-stu-id="8da08-120">Borrowed Qubits</span></span>

<span data-ttu-id="8da08-121">`borrowing`Оператор используется, чтобы сделать Кубитс доступным для временного использования, который не должен находиться в определенном состоянии.</span><span class="sxs-lookup"><span data-stu-id="8da08-121">The `borrowing` statement is used to make qubits available for temporary use, which do not need be in a specific state.</span></span>

<span data-ttu-id="8da08-122">Механизм заимствования займов позволяет выделить Кубитс, который можно использовать в качестве вспомогательного пространства во время вычисления.</span><span class="sxs-lookup"><span data-stu-id="8da08-122">The borrowing mechanism allows the allocation of qubits that can be used as scratch space during a computation.</span></span>
<span data-ttu-id="8da08-123">Обычно эти Кубитс не находятся в чистом состоянии, т. е. они не обязательно инициализируются в известном состоянии, например $ \кет {0} $.</span><span class="sxs-lookup"><span data-stu-id="8da08-123">These qubits are generally not in a clean state, i.e., they are not necessarily initialized in a known state such as $\ket{0}$.</span></span>
<span data-ttu-id="8da08-124">Они часто называются «грязными» Кубитс, так как их состояние неизвестно и даже может быть запутанными с другими частями памяти компьютера-такта.</span><span class="sxs-lookup"><span data-stu-id="8da08-124">These are often referred to as "dirty" qubits because their state is unknown and can even be entangled with other parts of the quantum computer's memory.</span></span>

<span data-ttu-id="8da08-125">Привязка соответствует тому же шаблону и правилам, что и в `using` операторе.</span><span class="sxs-lookup"><span data-stu-id="8da08-125">The binding follows the same pattern and rules as the one in a `using` statement.</span></span>
<span data-ttu-id="8da08-126">Например, примененная к объекту директива</span><span class="sxs-lookup"><span data-stu-id="8da08-126">For example,</span></span>
```qsharp
borrowing (qubit = Qubit()) {
    // ...
}
borrowing ((auxiliary, register) = (Qubit(), Qubit[5])) {
    // ...
}
```
<span data-ttu-id="8da08-127">Заимствованные Кубитс находятся в неизвестном состоянии и выходят за пределы области действия в конце блока инструкций.</span><span class="sxs-lookup"><span data-stu-id="8da08-127">The borrowed qubits are in an unknown state and go out of scope at the end of the statement block.</span></span>
<span data-ttu-id="8da08-128">Он фиксируется, чтобы покинуть Кубитс в том состоянии, в котором они находились в момент заимствования, т. е. состояние в начале и в конце блока инструкции должны совпадать.</span><span class="sxs-lookup"><span data-stu-id="8da08-128">The borrower commits to leaving the qubits in the same state they were in when they were borrowed,  i.e. their state at the beginning and at the end of the statement block is expected to be the same.</span></span>
<span data-ttu-id="8da08-129">Это состояние в частности не всегда является классическим состоянием, поэтому в большинстве случаев области действия не должны содержать измерений.</span><span class="sxs-lookup"><span data-stu-id="8da08-129">This state in particular is not necessarily a classical state, such that in most cases, borrowing scopes should not contain measurements.</span></span> 

<span data-ttu-id="8da08-130">При заимствовании Кубитс система сначала пытается заполнить запрос от Кубитс, который используется, но к нему не обращаются в теле `borrowing` инструкции.</span><span class="sxs-lookup"><span data-stu-id="8da08-130">When borrowing qubits, the system will first try to fill the request from qubits that are in use but that are not accessed during the body of the `borrowing` statement.</span></span>
<span data-ttu-id="8da08-131">Если такой Кубитс не хватает, он выделит новый Кубитс для выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="8da08-131">If there aren't enough such qubits, then it will allocate new qubits to complete the request.</span></span>


<span data-ttu-id="8da08-132">Между известными случаями использования «грязных» Кубитс являются реализации многофункциональных кнот шлюзов, требующие лишь очень мало Кубитс и реализации инкрементов.</span><span class="sxs-lookup"><span data-stu-id="8da08-132">Among the known use cases of dirty qubits are implementations of multi-controlled CNOT gates that require only very few qubits and implementation of incrementers.</span></span>
<span data-ttu-id="8da08-133">Примеры использования в Q #, а также использование [*2N + 2 Кубитс с модульным умножением на основе Тоффоли*](https://arxiv.org/abs/1611.07995) (Ханер, Роеттелер и своре 2017) для алгоритма, использующего заимствованные Кубитс, см. в приведенном ниже [примере заимствования Кубитс](#borrowing-qubits-example) .</span><span class="sxs-lookup"><span data-stu-id="8da08-133">See the [Borrowing Qubits Example](#borrowing-qubits-example) below to see an example of their use in Q#, or the paper [*Factoring using 2n+2 qubits with Toffoli based modular multiplication*](https://arxiv.org/abs/1611.07995) (Haner, Roetteler, and Svore 2017) for an algorithm which utilizes borrowed qubits.</span></span>


## <a name="intrinsic-operations"></a><span data-ttu-id="8da08-134">Внутренние операции</span><span class="sxs-lookup"><span data-stu-id="8da08-134">Intrinsic Operations</span></span>

<span data-ttu-id="8da08-135">После выделения кубит можно передать в функции и операции.</span><span class="sxs-lookup"><span data-stu-id="8da08-135">Once allocated, a qubit can then be passed to functions and operations.</span></span>
<span data-ttu-id="8da08-136">В некоторых случаях это все, что программа Q # может делать с кубит, так как действия, которые могут быть выполнены, определяются как операции.</span><span class="sxs-lookup"><span data-stu-id="8da08-136">In some sense, this is all that a Q# program can do with a qubit, as the actions that can be taken are all defined as operations.</span></span>
<span data-ttu-id="8da08-137">Мы более подробно рассмотрим эти операции в [подставляемых операциях и функциях](xref:microsoft.quantum.libraries.standard.prelude), но сейчас мы упомянули несколько полезных операций, которые можно использовать для взаимодействия с Кубитс.</span><span class="sxs-lookup"><span data-stu-id="8da08-137">We will see these operations in more detail in [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude), but for now, we mention a few useful operations that can be used to interact with qubits.</span></span>

<span data-ttu-id="8da08-138">Во-первых, операторы Single-кубит Паули $X $, $Y $ и $Z $ представлены в Q # встроенными операциями `X` , `Y` и `Z` , каждый из которых имеет тип `(Qubit => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="8da08-138">First, the single-qubit Pauli operators $X$, $Y$, and $Z$ are represented in Q# by the intrinsic operations `X`, `Y`, and `Z`, each of which has type `(Qubit => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="8da08-139">Как описано в [подставляемых операциях и функциях](xref:microsoft.quantum.libraries.standard.prelude), можно представить $X $ и, следовательно, `X` как операцию побитового отражения или не вентиль.</span><span class="sxs-lookup"><span data-stu-id="8da08-139">As described in [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude), we can think of $X$ and hence of `X` as a bit-flip operation or NOT gate.</span></span>
<span data-ttu-id="8da08-140">Эта `X` операция позволяет нам подготовить состояние вида $ \кет{s_0 s_1 \дотс s_n} $ для некоторых классических битовых строк $s $:</span><span class="sxs-lookup"><span data-stu-id="8da08-140">The `X` operation lets us prepare states of the form $\ket{s_0 s_1 \dots s_n}$ for some classical bit string $s$:</span></span>

```qsharp
operation PrepareBitString(bitstring : Bool[], register : Qubit[]) : Unit
is Adj + Ctl {
    let nQubits = Length(register);
    for (idxQubit in 0..nQubits - 1) {
        if (bitstring[idxQubit]) {
            X(register[idxQubit]);
        }
    }
}

operation RunExample() : Unit {
    using (register = Qubit[8]) {
        PrepareBitString(
            [true, true, false, false, true, false, false, true],
            register
        );
        // At this point, register now has the state |11001001〉.
        // Resetting the qubits will allow us to deallocate them properly.
        ResetAll(register);
    }
}
```

> [!TIP]
> <span data-ttu-id="8da08-141">Позже мы увидим более компактные способы записи этой операции, не требующие управления потоком вручную.</span><span class="sxs-lookup"><span data-stu-id="8da08-141">Later, we will see more compact ways of writing this operation that do not require manual flow control.</span></span>

<span data-ttu-id="8da08-142">Также можно подготовить такие состояния, как $ \кет{+} = \лефт (\кет {0} + \кет {1} \ригхт)/\скрт {2} $ и $ \кет {-} = \лефт (\кет {0} -\кет {1} \ригхт)/\скрт {2} $, с помощью хадамард Transform $H $, которое представлено в Q # встроенной операцией `H : (Qubit => Unit is Adj + Ctl)` :</span><span class="sxs-lookup"><span data-stu-id="8da08-142">We can also prepare states such as $\ket{+} = \left(\ket{0} + \ket{1}\right) / \sqrt{2}$ and $\ket{-} = \left(\ket{0} - \ket{1}\right) / \sqrt{2}$ by using the Hadamard transform $H$, which is represented in Q# by the intrinsic operation `H : (Qubit => Unit is Adj + Ctl)`:</span></span>

```qsharp
operation PreparePlusMinusState(bitstring : Bool[], register : Qubit[]) : Unit {
    // First, get a computational basis state of the form
    // |s_0 s_1 ... s_n〉 by using PrepareBitString, above.
    PrepareBitString(bitstring, register);
    // Next, we use that |+〉 = H|0〉 and |-〉 = H|1〉 to
    // prepare the state we want.
    for (idxQubit in IndexRange(register)) {
        H(register[idxQubit]);
    }
}
```

## <a name="measurements"></a><span data-ttu-id="8da08-143">Измерения</span><span class="sxs-lookup"><span data-stu-id="8da08-143">Measurements</span></span>

<span data-ttu-id="8da08-144">Используя `Measure` операцию, встроенную в неединую операцию, можно извлечь классическую информацию из объекта типа `Qubit` и присвоить классический результат, имеющий зарезервированный тип `Result` , указывающий на то, что результат больше не является состоянием такта.</span><span class="sxs-lookup"><span data-stu-id="8da08-144">Using the `Measure` operation, which is a built-in intrinsic non-unitary operation, we can extract classical information from an object of type `Qubit` and assign a classical value as a result, which has a reserved type `Result`, indicating that the result is no longer a quantum state.</span></span>
<span data-ttu-id="8da08-145">Входные данные для `Measure` — это Паули ось в блочной сфере, представленной значением типа `Pauli` (например), `PauliX` и значением типа `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="8da08-145">The input to `Measure` is a Pauli axis on the Bloch sphere, represented by a value of type `Pauli` (for instance `PauliX`) and an value of type `Qubit`.</span></span>

<span data-ttu-id="8da08-146">Простой пример — следующая операция, которая выделяет один кубит в состоянии $ \кет {0} $, затем применяет `H` к ней операцию хадамард и измеряет результат на `PauliZ` основе.</span><span class="sxs-lookup"><span data-stu-id="8da08-146">A simple example is the following operation, which allocates one qubit in the $\ket{0}$ state, then applies a Hadamard operation `H` to it and measures the result in the `PauliZ` basis.</span></span>

```qsharp
operation MeasureOneQubit() : Result {
    // The following using block creates a fresh qubit and initializes it
    // in the |0〉 state.
    using (qubit = Qubit()) {
        // We apply a Hadamard operation H to the state, thereby preparing the
        // state 1 / sqrt(2) (|0〉 + |1〉).
        H(qubit);
        // Now we measure the qubit in Z-basis.
        let result = M(qubit);
        // As the qubit is now in an eigenstate of the measurement operator,
        // we reset the qubit before releasing it.
        if (result == One) { X(qubit); }
        // Finally, we return the result of the measurement.
        return result;
    }
}
```

<span data-ttu-id="8da08-147">Чуть более сложный пример определяется следующей операцией, возвращающей логическое значение, `true` Если все Кубитс в регистре типа `Qubit[]` находятся в нулевом состоянии при измерении в указанной Паули базе, и в `false` противном случае возвращает.</span><span class="sxs-lookup"><span data-stu-id="8da08-147">A slightly more complicated example is given by the following operation, which returns the Boolean value `true` if all qubits in a register of type `Qubit[]` are in the state zero when measured in a specified Pauli basis, and which returns `false` otherwise.</span></span>

```qsharp
operation MeasureIfAllQubitsAreZero(qubits : Qubit[], pauli : Pauli) : Bool {
    mutable value = true;
    for (qubit in qubits) {
        if (Measure([pauli], [qubit]) == One) {
            set value = false;
        }
    }
    return value;
}
```

## <a name="borrowing-qubits-example"></a><span data-ttu-id="8da08-148">Пример заимствования Кубитс</span><span class="sxs-lookup"><span data-stu-id="8da08-148">Borrowing Qubits Example</span></span>

<span data-ttu-id="8da08-149">В Canon есть примеры, в которых используется `borrowing` ключевое слово, например `MultiControlledXBorrow` определенная ниже функция.</span><span class="sxs-lookup"><span data-stu-id="8da08-149">In the canon there are examples that use the `borrowing` keyword, for instance the function `MultiControlledXBorrow` defined below.</span></span>
<span data-ttu-id="8da08-150">Если `controls` обозначает элемент управления Кубитс, который должен быть добавлен к `X` операции, то в `Length(controls)-2` этой реализации будет добавлена Общая часть "грязного" анЦиллас.</span><span class="sxs-lookup"><span data-stu-id="8da08-150">If `controls` denotes the control qubits that should be added to an `X` operation, then an overall of `Length(controls)-2` many dirty ancillas will be added by this implementation.</span></span>

```qsharp
operation MultiControlledXBorrow ( controls : Qubit[] , target : Qubit ) : Unit
is Adj + Ctl {

    body (...) {
        ... // skipping some case handling here
        let numberOfDirtyQubits = numberOfControls - 2;
        borrowing( dirtyQubits = Qubit[ numberOfDirtyQubits ] ) {

            let allQubits = [ target ] + dirtyQubits + controls;
            let lastDirtyQubit = numberOfDirtyQubits;
            let totalNumberOfQubits = Length(allQubits);

            let outerOperation1 = 
                CCNOTByIndexLadder(
                    numberOfDirtyQubits + 1, 1, 0, numberOfDirtyQubits , _ );
            
            let innerOperation = 
                CCNOTByIndex(
                    totalNumberOfQubits - 1, totalNumberOfQubits - 2, lastDirtyQubit, _ );
            
            WithA(outerOperation1, innerOperation, allQubits);
            
            let outerOperation2 = 
                CCNOTByIndexLadder(
                    numberOfDirtyQubits + 2, 2, 1, numberOfDirtyQubits - 1 , _ );
            
            WithA(outerOperation2, innerOperation, allQubits);
        }
    }

    controlled(extraControls, ...) {
        MultiControlledXBorrow( extraControls + controls, target );
    }
}
```

<span data-ttu-id="8da08-151">Обратите внимание, что широкое использование `With` ---объединения в своей форме, которое применимо для операций, поддерживающих прилегающие, т. е. `WithA` ---был сделан в этом примере.</span><span class="sxs-lookup"><span data-stu-id="8da08-151">Note that extensive use of the `With` combinator---in its form that is applicable for operations that support adjoint, i.e., `WithA`---was made in this example.</span></span>
<span data-ttu-id="8da08-152">Это хороший стиль программирования, поскольку добавление элементов управления в структуры, включающие `With` Управление, распространяется только на внутреннюю операцию.</span><span class="sxs-lookup"><span data-stu-id="8da08-152">This is good programming style, because adding control to structures involving `With` propagates control only to the inner operation.</span></span>
<span data-ttu-id="8da08-153">Кроме того, обратите внимание, что в дополнение к `body` операции, реализация `controlled` тела операции была явно предоставлена, вместо того чтобы прибегнуть к `controlled auto` оператору.</span><span class="sxs-lookup"><span data-stu-id="8da08-153">Further, note that here in addition to the `body` of the operation, an implementation of the `controlled` body of the operation was explicitly provided, rather than resorting to a `controlled auto` statement.</span></span>
<span data-ttu-id="8da08-154">Причина этого заключается в том, что мы понимаем, что из структуры канала можно легко добавить дополнительные элементы управления, которые полезны по сравнению с добавлением элемента управления в каждый отдельный шлюз в `body` .</span><span class="sxs-lookup"><span data-stu-id="8da08-154">The reason for this is that we know from the structure of the circuit how to easily add further controls which is beneficial compared to adding control to each and every individual gate in the `body`.</span></span> 

<span data-ttu-id="8da08-155">Рекомендуется сравнить этот код с другой функцией Canon `MultiControlledXClean` , которая достигает той же цели реализации `X` операции, управляемой операцией умножения, но и использует несколько чистых Кубитс с помощью `using` механизма.</span><span class="sxs-lookup"><span data-stu-id="8da08-155">It is instructive to compare this code with another canon function `MultiControlledXClean` which achieves the same goal of implementing a multiply-controlled `X` operation, however, which uses several clean qubits using the `using` mechanism.</span></span> 

## <a name="whats-next"></a><span data-ttu-id="8da08-156">Дальнейшая работа</span><span class="sxs-lookup"><span data-stu-id="8da08-156">What's Next?</span></span>
<span data-ttu-id="8da08-157">Дополнительные сведения о [потоке управления](xref:microsoft.quantum.guide.controlflow) в Q #.</span><span class="sxs-lookup"><span data-stu-id="8da08-157">Learn about [Control Flow](xref:microsoft.quantum.guide.controlflow) in Q#.</span></span>