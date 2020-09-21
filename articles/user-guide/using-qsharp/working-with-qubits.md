---
title: Работа с кубитами
description: Дополнительные сведения о работе с Кубитс в Q#
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.qubits
no-loc:
- Q#
- $$v
ms.openlocfilehash: aa942a61280553ae4e51cd5ddcc85c0df935dab1
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/21/2020
ms.locfileid: "90835865"
---
# <a name="working-with-qubits"></a><span data-ttu-id="cdae8-103">Работа с кубитами</span><span class="sxs-lookup"><span data-stu-id="cdae8-103">Working with qubits</span></span>

<span data-ttu-id="cdae8-104">Кубитс — это фундаментальный объект информации в тактовых вычислениях.</span><span class="sxs-lookup"><span data-stu-id="cdae8-104">Qubits are the fundamental object of information in quantum computing.</span></span> <span data-ttu-id="cdae8-105">Общие сведения о Кубитс см. в разделе [Общие сведения о тактовых вычислениях](xref:microsoft.quantum.overview.understanding), а также подробное описание их математического представления см. [в разделе кубит](xref:microsoft.quantum.concepts.qubit).</span><span class="sxs-lookup"><span data-stu-id="cdae8-105">For a general introduction to qubits, see [Understanding quantum computing](xref:microsoft.quantum.overview.understanding), and to dive deeper into their mathematical representation, see [The Qubit](xref:microsoft.quantum.concepts.qubit).</span></span> 

<span data-ttu-id="cdae8-106">В этой статье рассматривается использование и работа с Кубитс в Q# программе.</span><span class="sxs-lookup"><span data-stu-id="cdae8-106">This article explores how to use and work with qubits in a Q# program.</span></span> 

> [!IMPORTANT]
><span data-ttu-id="cdae8-107">Ни одна из инструкций, обсуждаемых в этой статье, не является допустимой в теле функции.</span><span class="sxs-lookup"><span data-stu-id="cdae8-107">None of the statements discussed in this article are valid within the body of a function.</span></span> <span data-ttu-id="cdae8-108">Они действительны только в пределах операций.</span><span class="sxs-lookup"><span data-stu-id="cdae8-108">They are only valid within operations.</span></span>

## <a name="allocating-qubits"></a><span data-ttu-id="cdae8-109">Выделение Кубитс</span><span class="sxs-lookup"><span data-stu-id="cdae8-109">Allocating Qubits</span></span>

<span data-ttu-id="cdae8-110">Поскольку физические Кубитс являются ценным ресурсом на такте, часть задания компилятора заключается в том, чтобы убедиться, что они используются как можно быстрее.</span><span class="sxs-lookup"><span data-stu-id="cdae8-110">Because physical qubits are a precious resource in a quantum computer, part of the compiler's job is to make sure they are being used as efficiently as possible.</span></span>
<span data-ttu-id="cdae8-111">Таким образом, необходимо сообщить Q# о *выделении* Кубитс для использования в определенном блоке инструкций.</span><span class="sxs-lookup"><span data-stu-id="cdae8-111">As such, you need to tell Q# to *allocate* qubits for use within a particular statement block.</span></span>
<span data-ttu-id="cdae8-112">Можно выделить Кубитс как один кубит или как массив Кубитс, известный как *регистр*.</span><span class="sxs-lookup"><span data-stu-id="cdae8-112">You can allocate qubits as a single qubit, or as an array of qubits, known as a *register*.</span></span> 

### <a name="clean-qubits"></a><span data-ttu-id="cdae8-113">Очистить Кубитс</span><span class="sxs-lookup"><span data-stu-id="cdae8-113">Clean qubits</span></span>

<span data-ttu-id="cdae8-114">Используйте `using` инструкцию для выделения нового Кубитс для использования в блоке инструкций.</span><span class="sxs-lookup"><span data-stu-id="cdae8-114">Use the `using` statement to allocate new qubits for use during a statement block.</span></span>

<span data-ttu-id="cdae8-115">Оператор состоит из ключевого слова `using` , за которым следует привязка, заключенная в круглые скобки, `( )` и блок операторов, в рамках которого доступны Кубитс.</span><span class="sxs-lookup"><span data-stu-id="cdae8-115">The statement consists of the keyword `using`, followed by a binding enclosed in parentheses `( )` and the statement block within which the qubits are available.</span></span>
<span data-ttu-id="cdae8-116">Привязка соответствует тому же шаблону, что и `let` инструкции: один символ или кортеж символов, за которым следует знак равенства `=` и одно значение или соответствующий кортеж *инициализаторов*.</span><span class="sxs-lookup"><span data-stu-id="cdae8-116">The binding follows the same pattern as `let` statements: either a single symbol or a tuple of symbols, followed by an equals sign `=`, and either a single value or a matching tuple of *initializers*.</span></span>

<span data-ttu-id="cdae8-117">Инициализаторы доступны для одного кубит, обозначенного как `Qubit()` , или массива Кубитс, `Qubit[n]` , где `n` является `Int` выражением.</span><span class="sxs-lookup"><span data-stu-id="cdae8-117">Initializers are available either for a single qubit, indicated as `Qubit()`, or an array of qubits, `Qubit[n]`, where `n` is an `Int` expression.</span></span>
<span data-ttu-id="cdae8-118">Например, примененная к объекту директива</span><span class="sxs-lookup"><span data-stu-id="cdae8-118">For example,</span></span>

```qsharp
using (qubit = Qubit()) {
    // ...
}
using ((auxiliary, register) = (Qubit(), Qubit[5])) {
    // ...
}
```

<span data-ttu-id="cdae8-119">Все Кубитс, выделенные таким образом, запускаются в состоянии $ \кет {0} $.</span><span class="sxs-lookup"><span data-stu-id="cdae8-119">Any qubits allocated in this way start off in the $\ket{0}$ state.</span></span> <span data-ttu-id="cdae8-120">Таким образом, в предыдущем примере `auxiliary` — это один кубит в состоянии $ \кет {0} $, который `register` находится в пяти кубит State $ \кет {00000} = \кет {0} \отимес \кет {0} \отимес \кдотс \отимес \кет {0} $.</span><span class="sxs-lookup"><span data-stu-id="cdae8-120">Thus in the previous example, `auxiliary` is a single qubit in the state $\ket{0}$, and `register` is in the five-qubit state $\ket{00000} = \ket{0} \otimes \ket{0} \otimes \cdots \otimes \ket{0}$.</span></span>
<span data-ttu-id="cdae8-121">В конце `using` блока все Кубитс, выделенные этим блоком, немедленно освобождаются и не могут использоваться дальше.</span><span class="sxs-lookup"><span data-stu-id="cdae8-121">At the end of the `using` block, any qubits allocated by that block are immediately deallocated and cannot be used further.</span></span>

> [!WARNING]
> <span data-ttu-id="cdae8-122">Целевые компьютеры могут повторно использовать освобожденные Кубитс и предлагать их другим `using` блокам для выделения.</span><span class="sxs-lookup"><span data-stu-id="cdae8-122">Target machines can reuse deallocated qubits and offer them to other `using` blocks for allocation.</span></span> <span data-ttu-id="cdae8-123">Таким образом, целевой компьютер ждет, что Кубитс находятся в состоянии $ \кет {0} $ непосредственно перед освобождением.</span><span class="sxs-lookup"><span data-stu-id="cdae8-123">As such, the target machine expects that qubits are in the $\ket{0}$ state immediately before deallocation.</span></span>
> <span data-ttu-id="cdae8-124">По возможности используйте единые операции для возврата всех выделенных Кубитс в $ \кет {0} $.</span><span class="sxs-lookup"><span data-stu-id="cdae8-124">Whenever possible, use unitary operations to return any allocated qubits to $\ket{0}$.</span></span>
> <span data-ttu-id="cdae8-125">При необходимости можно использовать @"microsoft.quantum.intrinsic.reset" операцию, которая возвращает кубит в $ \кет {0} $, измеряя ее и условно выполняя операцию на основе результата.</span><span class="sxs-lookup"><span data-stu-id="cdae8-125">If need be, you can use the @"microsoft.quantum.intrinsic.reset" operation, which returns the qubit to $\ket{0}$ by measuring it and conditionally performing an operation based on the result.</span></span> <span data-ttu-id="cdae8-126">Такое измерение уничтожает любые замкнутые с оставшимся Кубитс и может повлиять на вычисление.</span><span class="sxs-lookup"><span data-stu-id="cdae8-126">Such a measurement destroys any entanglement with the remaining qubits and can thus impact the computation.</span></span>


### <a name="borrowed-qubits"></a><span data-ttu-id="cdae8-127">Заимствованный Кубитс</span><span class="sxs-lookup"><span data-stu-id="cdae8-127">Borrowed Qubits</span></span>

<span data-ttu-id="cdae8-128">Используйте `borrowing` инструкцию для выделения Кубитс для временного использования, который не должен находиться в определенном состоянии.</span><span class="sxs-lookup"><span data-stu-id="cdae8-128">Use the `borrowing` statement to allocate qubits for temporary use, which do not need to be in a specific state.</span></span>

<span data-ttu-id="cdae8-129">Во время вычисления можно использовать заимствованный Кубитс в качестве вспомогательного пространства.</span><span class="sxs-lookup"><span data-stu-id="cdae8-129">You can use borrowed qubits as scratch space during a computation.</span></span>
<span data-ttu-id="cdae8-130">Обычно эти Кубитс не находятся в чистом состоянии, т. е. они не обязательно инициализируются в известном состоянии, например $ \кет {0} $.</span><span class="sxs-lookup"><span data-stu-id="cdae8-130">These qubits are generally not in a clean state, that is, they are not necessarily initialized in a known state such as $\ket{0}$.</span></span>
<span data-ttu-id="cdae8-131">Они часто называются «грязными» Кубитс, так как их состояние неизвестно и даже может быть запутанными с другими частями памяти компьютера-такта.</span><span class="sxs-lookup"><span data-stu-id="cdae8-131">These are often referred to as "dirty" qubits because their state is unknown and can even be entangled with other parts of the quantum computer's memory.</span></span>

<span data-ttu-id="cdae8-132">Привязка соответствует тому же шаблону и правилам, что и `using` оператор.</span><span class="sxs-lookup"><span data-stu-id="cdae8-132">The binding follows the same pattern and rules as the `using` statement.</span></span>
<span data-ttu-id="cdae8-133">Например, примененная к объекту директива</span><span class="sxs-lookup"><span data-stu-id="cdae8-133">For example,</span></span>
```qsharp
borrowing (qubit = Qubit()) {
    // ...
}
borrowing ((auxiliary, register) = (Qubit(), Qubit[5])) {
    // ...
}
```
<span data-ttu-id="cdae8-134">Заимствованные Кубитс находятся в неизвестном состоянии и выходят за пределы области действия в конце блока инструкций.</span><span class="sxs-lookup"><span data-stu-id="cdae8-134">The borrowed qubits are in an unknown state and go out of scope at the end of the statement block.</span></span>
<span data-ttu-id="cdae8-135">Он фиксируется, чтобы выйти из Кубитс в том состоянии, в котором они были в момент их позаимствования. Это значит, что их состояние в начале и в конце блока инструкций должно быть одинаковым.</span><span class="sxs-lookup"><span data-stu-id="cdae8-135">The borrower commits to leaving the qubits in the same state they were in when they borrowed them; that is, their state at the beginning and the end of the statement block should be the same.</span></span>
<span data-ttu-id="cdae8-136">Так как это состояние не обязательно является классическим состоянием, в большинстве случаев области действия не должны содержать измерений.</span><span class="sxs-lookup"><span data-stu-id="cdae8-136">Because this state is not necessarily a classical state, in most cases borrowing scopes should not contain measurements.</span></span> 

<span data-ttu-id="cdae8-137">При заимствовании Кубитс система сначала пытается заполнить запрос от Кубитс, который используется, но недоступен в теле `borrowing` инструкции.</span><span class="sxs-lookup"><span data-stu-id="cdae8-137">When borrowing qubits, the system first tries to fill the request from qubits that are in use but not accessed during the body of the `borrowing` statement.</span></span>
<span data-ttu-id="cdae8-138">Если такой Кубитс не хватает, он выделяет новый Кубитс для выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="cdae8-138">If there aren't enough such qubits, then it allocates new qubits to complete the request.</span></span>

<span data-ttu-id="cdae8-139">Между известными случаями использования «грязных» Кубитс являются реализации многофункциональных кнот шлюзов, требующие лишь очень мало Кубитс и реализации инкрементов.</span><span class="sxs-lookup"><span data-stu-id="cdae8-139">Among the known use cases of dirty qubits are implementations of multi-controlled CNOT gates that require only very few qubits and implementation of incrementers.</span></span>
<span data-ttu-id="cdae8-140">Пример использования в см Q# . в статьях о [заимствовании Кубитс](#borrowing-qubits-example) в этой статье или в документе [*с использованием 2N + 2 Кубитс с Тоффоли модульного умножения*](https://arxiv.org/abs/1611.07995) (ханер, роеттелер и своре 2017) для алгоритма, использующего заимствованные Кубитс.</span><span class="sxs-lookup"><span data-stu-id="cdae8-140">For an example of their use in Q#, see [Borrowing Qubits Example](#borrowing-qubits-example) in this article, or the paper [*Factoring using 2n+2 qubits with Toffoli based modular multiplication*](https://arxiv.org/abs/1611.07995) (Haner, Roetteler, and Svore 2017) for an algorithm which utilizes borrowed qubits.</span></span>

## <a name="intrinsic-operations"></a><span data-ttu-id="cdae8-141">Внутренние операции</span><span class="sxs-lookup"><span data-stu-id="cdae8-141">Intrinsic Operations</span></span>

<span data-ttu-id="cdae8-142">После выделения можно передать кубит в функции и операции.</span><span class="sxs-lookup"><span data-stu-id="cdae8-142">Once allocated, you can pass a qubit to functions and operations.</span></span>
<span data-ttu-id="cdae8-143">В некоторых случаях это все, что Q# программа может делать с кубит, так как действия, которые могут быть выполнены, определяются как операции.</span><span class="sxs-lookup"><span data-stu-id="cdae8-143">In some sense, this is all that a Q# program can do with a qubit, as the actions that can be taken are all defined as operations.</span></span>

<span data-ttu-id="cdae8-144">В этой статье рассматриваются некоторые полезные Q# операции, которые можно использовать для взаимодействия с Кубитс.</span><span class="sxs-lookup"><span data-stu-id="cdae8-144">This article discusses a few useful Q# operations that you can use to interact with qubits.</span></span>
<span data-ttu-id="cdae8-145">Дополнительные сведения об этих и других функциях см. в разделе [встроенные операции и функции](xref:microsoft.quantum.libraries.standard.prelude).</span><span class="sxs-lookup"><span data-stu-id="cdae8-145">For more detail about these and others, see [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude).</span></span> 

<span data-ttu-id="cdae8-146">Во-первых, операторы Single-кубит Паули $X $, $Y $ и $Z $ представлены Q# встроенными операциями [`X`](xref:microsoft.quantum.intrinsic.x) , [`Y`](xref:microsoft.quantum.intrinsic.y) и [`Z`](xref:microsoft.quantum.intrinsic.z) , каждый из которых имеет тип `(Qubit => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="cdae8-146">First, the single-qubit Pauli operators $X$, $Y$, and $Z$ are represented in Q# by the intrinsic operations [`X`](xref:microsoft.quantum.intrinsic.x), [`Y`](xref:microsoft.quantum.intrinsic.y), and [`Z`](xref:microsoft.quantum.intrinsic.z), each of which has type `(Qubit => Unit is Adj + Ctl)`.</span></span>

<span data-ttu-id="cdae8-147">Как описано в [подставляемых операциях и функциях](xref:microsoft.quantum.libraries.standard.prelude), представьте $X $ и, следовательно, `X` как операцию побитового отражения или не является шлюзом.</span><span class="sxs-lookup"><span data-stu-id="cdae8-147">As described in [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude), think of $X$ and hence of `X` as a bit-flip operation or NOT gate.</span></span>
<span data-ttu-id="cdae8-148">Вы можете использовать `X` операцию для подготовки состояний вида $ \кет{s_0 s_1 \дотс s_n} $ для некоторых классических битовых строк $s $:</span><span class="sxs-lookup"><span data-stu-id="cdae8-148">You can use the `X` operation to prepare states of the form $\ket{s_0 s_1 \dots s_n}$ for some classical bit string $s$:</span></span>

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
        // Remember to reset the qubits before deallocation:
        ResetAll(register);
    }
}
```

> [!TIP]
> <span data-ttu-id="cdae8-149">Позже вы увидите более компактные способы записи этой операции, которые не нуждаются в ручном потоке управления.</span><span class="sxs-lookup"><span data-stu-id="cdae8-149">Later, you will see more compact ways of writing this operation that do not require manual control flow.</span></span>

<span data-ttu-id="cdae8-150">Кроме того, можно подготовить такие состояния, как $ \кет{+} = \лефт (\кет {0} + \кет {1} \ригхт)/\скрт {2} $ и $ \кет {-} = \лефт (\кет {0} -\кет {1} \ригхт)/\скрт {2} $, с помощью хадамард Transform $H $, которое представлено Q# встроенной операцией [`H`](xref:microsoft.quantum.intrinsic.h) (также типа (кубит => единица "года + CTL)"):</span><span class="sxs-lookup"><span data-stu-id="cdae8-150">You can also prepare states such as $\ket{+} = \left(\ket{0} + \ket{1}\right) / \sqrt{2}$ and $\ket{-} = \left(\ket{0} - \ket{1}\right) / \sqrt{2}$ by using the Hadamard transform $H$, which is represented in Q# by the intrinsic operation [`H`](xref:microsoft.quantum.intrinsic.h) (also of type (Qubit => Unit is Adj + Ctl)\`):</span></span>

```qsharp
operation PreparePlusMinusState(bitstring : Bool[], register : Qubit[]) : Unit {
    // First, get a computational basis state of the form
    // |s_0 s_1 ... s_n〉 by using PrepareBitString in the earlier example.
    PrepareBitString(bitstring, register);
    // Next, use that |+〉 = H|0〉 and |-〉 = H|1〉 to
    // prepare the desired state.
    for (idxQubit in IndexRange(register)) {
        H(register[idxQubit]);
    }
}
```

## <a name="measurements"></a><span data-ttu-id="cdae8-151">Измерения</span><span class="sxs-lookup"><span data-stu-id="cdae8-151">Measurements</span></span>

<span data-ttu-id="cdae8-152">Измерения отдельных Кубитс можно выполнять в разных базах данных, каждый из которых представлен осью Паули в [БЛОЧ Sphere](xref:microsoft.quantum.glossary#bloch-sphere).</span><span class="sxs-lookup"><span data-stu-id="cdae8-152">Measurements of individual qubits can be performed in different bases, each represented by a Pauli axis on the [Bloch sphere](xref:microsoft.quantum.glossary#bloch-sphere).</span></span>
<span data-ttu-id="cdae8-153">*Вычислительная базис* — это `PauliZ` базис, который является наиболее распространенным основанием для измерения.</span><span class="sxs-lookup"><span data-stu-id="cdae8-153">The *computational basis* refers to the `PauliZ` basis, and is the most common basis used for measurement.</span></span>

### <a name="measure-a-single-qubit-in-the-pauliz-basis"></a><span data-ttu-id="cdae8-154">Измерение отдельного кубита в `PauliZ` основе</span><span class="sxs-lookup"><span data-stu-id="cdae8-154">Measure a single qubit in the `PauliZ` basis</span></span>

<span data-ttu-id="cdae8-155">Используйте [`M`](xref:microsoft.quantum.intrinsic.m) операцию, встроенную в неединую операцию, для измерения отдельного кубита на `PauliZ` основе и присвойте результату классический.</span><span class="sxs-lookup"><span data-stu-id="cdae8-155">Use the [`M`](xref:microsoft.quantum.intrinsic.m) operation, which is a built-in intrinsic non-unitary operation, to measure a single qubit in the `PauliZ` basis and assign a classical value to the result.</span></span>
<span data-ttu-id="cdae8-156">`M` имеет зарезервированный возвращаемый тип, `Result` который может принимать только значения `Zero` или `One` соответствующие измеряемым состояниям $ \кет {0} $ или $ \кет {1} $ — указывает, что результат больше не является состоянием такта.</span><span class="sxs-lookup"><span data-stu-id="cdae8-156">`M` has a reserved return type, `Result`, which can only take values `Zero` or `One` corresponding to the measured states $\ket{0}$ or $\ket{1}$ - indicating that the result is no longer a quantum state.</span></span>

<span data-ttu-id="cdae8-157">Простой пример — следующая операция, которая выделяет один кубит в состоянии $ \кет {0} $, затем применяет `H` к ней операцию хадамард и измеряет результат на `PauliZ` основе.</span><span class="sxs-lookup"><span data-stu-id="cdae8-157">A simple example is the following operation, which allocates one qubit in the $\ket{0}$ state, then applies a Hadamard operation `H` to it and measures the result in the `PauliZ` basis.</span></span>

```qsharp
operation MeasureOneQubit() : Result {
    // The following using block creates a fresh qubit and initializes it
    // in the |0〉 state.
    using (qubit = Qubit()) {
        // Apply a Hadamard operation H to the state, thereby preparing the
        // state 1 / sqrt(2) (|0〉 + |1〉).
        H(qubit);
        // Now measure the qubit in Z-basis.
        let result = M(qubit);
        // As the qubit is now in an eigenstate of the measurement operator,
        // reset the qubit before releasing it.
        if (result == One) { X(qubit); }
        // Finally, return the result of the measurement.
        return result;
    }
}
```

### <a name="measure-one-or-more-qubits-in-specific-bases"></a><span data-ttu-id="cdae8-158">Измерение одного или нескольких Кубитс в конкретных базовых базах</span><span class="sxs-lookup"><span data-stu-id="cdae8-158">Measure one or more qubits in specific bases</span></span>

<span data-ttu-id="cdae8-159">Для измерения массива из одного или нескольких Кубитс в конкретных базах данных можно использовать [`Measure`](xref:microsoft.quantum.intrinsic.measure) операцию.</span><span class="sxs-lookup"><span data-stu-id="cdae8-159">To measure an array of one or more qubits in specific bases, you can use the [`Measure`](xref:microsoft.quantum.intrinsic.measure) operation.</span></span>

<span data-ttu-id="cdae8-160">Входные данные для `Measure` являются массивом `Pauli` типов (например, `[PauliX, PauliZ, PauliZ]` ) и массивом Кубитс.</span><span class="sxs-lookup"><span data-stu-id="cdae8-160">The inputs to `Measure` are an array of `Pauli` types (for example, `[PauliX, PauliZ, PauliZ]`) and an array of qubits.</span></span>

<span data-ttu-id="cdae8-161">Чуть более сложный пример определяется следующей операцией, возвращающей логическое значение, `true` Если все Кубитс в регистре типа `Qubit[]` находятся в нулевом состоянии при измерении в указанной Паули базе, и в `false` противном случае возвращает.</span><span class="sxs-lookup"><span data-stu-id="cdae8-161">A slightly more complicated example is given by the following operation, which returns the Boolean value `true` if all qubits in a register of type `Qubit[]` are in the state zero when measured in a specified Pauli basis, and which returns `false` otherwise.</span></span>

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

<span data-ttu-id="cdae8-162">Обратите внимание, что этот пример по-прежнему выполняется только `Measure` для отдельных Кубитс по одному, но операция может быть расширена до совместного измерения на нескольких Кубитс.</span><span class="sxs-lookup"><span data-stu-id="cdae8-162">Note that this example still only performs `Measure` on individual qubits one at a time, but the operation can be extended to joint measurements on multiple qubits.</span></span>

## <a name="borrowing-qubits-example"></a><span data-ttu-id="cdae8-163">Пример заимствования Кубитс</span><span class="sxs-lookup"><span data-stu-id="cdae8-163">Borrowing Qubits Example</span></span>

<span data-ttu-id="cdae8-164">В Canon есть примеры, использующие `borrowing` ключевое слово, например следующую функцию `MultiControlledXBorrow` .</span><span class="sxs-lookup"><span data-stu-id="cdae8-164">There are examples in the canon that use the `borrowing` keyword, such as the following function `MultiControlledXBorrow`.</span></span> <span data-ttu-id="cdae8-165">Если `controls` обозначает элемент управления Кубитс для добавления в `X` операцию, то число "грязных" [анЦиллас](xref:microsoft.quantum.glossary#ancilla) , добавленное этой реализацией, — `Length(controls)-2` .</span><span class="sxs-lookup"><span data-stu-id="cdae8-165">If `controls` denotes the control qubits to add to an `X` operation, then the number of dirty [ancillas](xref:microsoft.quantum.glossary#ancilla) added by this implementation is `Length(controls)-2`.</span></span>

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

<span data-ttu-id="cdae8-166">Обратите внимание, что в этом примере используется широкое использование `With` объединения, в его форме, которая применима для операций, поддерживающих смежные, например `WithA` .</span><span class="sxs-lookup"><span data-stu-id="cdae8-166">Note that this example used extensive use of the `With` combinator, in its form that is applicable for operations that support adjoint, for example, `WithA`.</span></span>
<span data-ttu-id="cdae8-167">Это хороший стиль программирования, поскольку добавление элементов управления в структуры, включающие `With` Управление, распространяется только на внутреннюю операцию.</span><span class="sxs-lookup"><span data-stu-id="cdae8-167">This is good programming style, because adding control to structures involving `With` propagates control only to the inner operation.</span></span>
<span data-ttu-id="cdae8-168">Кроме того, обратите внимание, что в дополнение к `body` операции `controlled` была предоставлена явная реализация тела операции, а не `controlled auto` инструкция.</span><span class="sxs-lookup"><span data-stu-id="cdae8-168">Also note that, in addition to the `body` of the operation, an implementation of the `controlled` body of the operation was explicitly provided, rather than resorting to a `controlled auto` statement.</span></span>
<span data-ttu-id="cdae8-169">Причиной этого является то, что из-за структуры канала можно легко добавить дополнительные элементы управления, что полезно по сравнению с добавлением элемента управления в каждый шлюз в `body` .</span><span class="sxs-lookup"><span data-stu-id="cdae8-169">The reason for this is that, because of the structure of the circuit, it is easy to add further controls, which is beneficial compared to adding control to each gate in the `body`.</span></span> 

<span data-ttu-id="cdae8-170">Рекомендуется сравнить этот код с другой функцией Canon `MultiControlledXClean` , которая достигает той же цели реализации `X` операции, управляемой операцией умножения, но и использует несколько чистых Кубитс с помощью `using` механизма.</span><span class="sxs-lookup"><span data-stu-id="cdae8-170">It is instructive to compare this code with another canon function `MultiControlledXClean` which achieves the same goal of implementing a multiply-controlled `X` operation, however, which uses several clean qubits using the `using` mechanism.</span></span> 

## <a name="next-steps"></a><span data-ttu-id="cdae8-171">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="cdae8-171">Next steps</span></span>

<span data-ttu-id="cdae8-172">Дополнительные сведения о [потоке управления](xref:microsoft.quantum.guide.controlflow) в Q# .</span><span class="sxs-lookup"><span data-stu-id="cdae8-172">Learn about [Control Flow](xref:microsoft.quantum.guide.controlflow) in Q#.</span></span>