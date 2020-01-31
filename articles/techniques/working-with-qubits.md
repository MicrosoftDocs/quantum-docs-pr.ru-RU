---
title: Работа с Кубитс
description: 'Работа с методами Кубитс-Q #'
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.techniques.qubits
ms.openlocfilehash: dc6db93dadc37534aece9624fe516125d919f8cd
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820000"
---
# <a name="working-with-qubits"></a><span data-ttu-id="6fb2f-103">Работа с Кубитс</span><span class="sxs-lookup"><span data-stu-id="6fb2f-103">Working with Qubits</span></span>

<span data-ttu-id="6fb2f-104">Теперь, когда вы видели множество различных частей языка Q #, позвольте нам пробавиться от него и увидеть, как использовать сами Кубитс.</span><span class="sxs-lookup"><span data-stu-id="6fb2f-104">Having now seen a variety of different parts of the Q# language, let us get into the thick of it and see how to use qubits themselves.</span></span>

## <a name="allocating-qubits"></a><span data-ttu-id="6fb2f-105">Выделение Кубитс</span><span class="sxs-lookup"><span data-stu-id="6fb2f-105">Allocating Qubits</span></span>

<span data-ttu-id="6fb2f-106">Во-первых, чтобы получить кубит, которую можно использовать в Q #, мы *выделили* Кубитс в блоке `using`:</span><span class="sxs-lookup"><span data-stu-id="6fb2f-106">First, to obtain a qubit that we can use in Q#, we *allocate* qubits within a `using` block:</span></span>

```qsharp
using (register = Qubit[5]) {
    // Do stuff...
}
```

<span data-ttu-id="6fb2f-107">Все Кубитс, выделенные таким образом, запускаются в состоянии $ \кет{0}$. в приведенном выше примере `register` в состоянии $ \кет{00000} = \кет{0} \отимес \кет{0} \отимес \кдотс \отимес \кет{0}$.</span><span class="sxs-lookup"><span data-stu-id="6fb2f-107">Any qubits allocated in this way start off in the $\ket{0}$ state; in the example above, `register` is thus in the state $\ket{00000} = \ket{0} \otimes \ket{0} \otimes \cdots \otimes \ket{0}$.</span></span>
<span data-ttu-id="6fb2f-108">В конце блока `using` все Кубитс, выделенные этим блоком, немедленно освобождаются и не могут использоваться дальше.</span><span class="sxs-lookup"><span data-stu-id="6fb2f-108">At the end of the `using` block, any qubits allocated by that block are immediately deallocated and cannot be used further.</span></span>

> [!WARNING]
> <span data-ttu-id="6fb2f-109">Целевые компьютеры предполагают, что Кубитс находятся в состоянии $ \кет{0}$ немедленно перед освобождением, поэтому их можно повторно использовать и предлагать другим блокам `using` для выделения.</span><span class="sxs-lookup"><span data-stu-id="6fb2f-109">Target machines expect that qubits are in the $\ket{0}$ state immediately before deallocation, so that they can be reused and offered to other `using` blocks for allocation.</span></span>
> <span data-ttu-id="6fb2f-110">По возможности используйте единые операции для возврата всех выделенных Кубитс в $ \кет{0}$.</span><span class="sxs-lookup"><span data-stu-id="6fb2f-110">Whenever possible, use unitary operations to return any allocated qubits to $\ket{0}$.</span></span>
> <span data-ttu-id="6fb2f-111">При необходимости можно использовать операцию @"microsoft.quantum.intrinsic.reset" для измерения кубит, а также использовать этот результат измерения, чтобы гарантировать, что измеряемый кубит возвращается в $ \кет{0}$.</span><span class="sxs-lookup"><span data-stu-id="6fb2f-111">If need be, the @"microsoft.quantum.intrinsic.reset" operation can be used to measure a qubit instead, and to use that measurement result to ensure that the measured qubit is returned to $\ket{0}$.</span></span> <span data-ttu-id="6fb2f-112">Такое измерение приведет к уничтожению всех замкнутые с оставшимся Кубитс и может повлиять на вычисление.</span><span class="sxs-lookup"><span data-stu-id="6fb2f-112">Such a measurement will destroy any entanglement with the remaining qubits and can thus impact the computation.</span></span>

## <a name="intrinsic-operations"></a><span data-ttu-id="6fb2f-113">Внутренние операции</span><span class="sxs-lookup"><span data-stu-id="6fb2f-113">Intrinsic Operations</span></span>

<span data-ttu-id="6fb2f-114">После выделения кубит можно передать в функции и операции.</span><span class="sxs-lookup"><span data-stu-id="6fb2f-114">Once allocated, a qubit can then be passed to functions and operations.</span></span>
<span data-ttu-id="6fb2f-115">В некоторых случаях это все, что программа Q # может делать с кубит, так как действия, которые могут быть выполнены, определяются как операции.</span><span class="sxs-lookup"><span data-stu-id="6fb2f-115">In some sense, this is all that a Q# program can do with a qubit, as the actions that can be taken are all defined as operations.</span></span>
<span data-ttu-id="6fb2f-116">Мы более подробно рассмотрим эти операции в [подставляемых операциях и функциях](xref:microsoft.quantum.libraries.standard.prelude), но сейчас мы упомянули несколько полезных операций, которые можно использовать для взаимодействия с Кубитс.</span><span class="sxs-lookup"><span data-stu-id="6fb2f-116">We will see these operations in more detail in [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude), but for now, we mention a few useful operations that can be used to interact with qubits.</span></span>

<span data-ttu-id="6fb2f-117">Во-первых, операторы Single-кубит Паули $X $, $Y $ и $Z $ представлены в Q # встроенными операциями `X`, `Y`и `Z`, каждый из которых имеет тип `(Qubit => Unit is Adj + Ctl)`.</span><span class="sxs-lookup"><span data-stu-id="6fb2f-117">First, the single-qubit Pauli operators $X$, $Y$, and $Z$ are represented in Q# by the intrinsic operations `X`, `Y`, and `Z`, each of which has type `(Qubit => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="6fb2f-118">Как описано в [подставляемых операциях и функциях](xref:microsoft.quantum.libraries.standard.prelude), можно представить $X $ и, следовательно, `X` как операцию побитового отражения или не шлюз.</span><span class="sxs-lookup"><span data-stu-id="6fb2f-118">As described in [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude), we can think of $X$ and hence of `X` as a bit-flip operation or NOT gate.</span></span>
<span data-ttu-id="6fb2f-119">`X` операция позволяет нам подготовить состояния формы $ \кет{s_0 s_1 \дотс s_n} $ для некоторых классических битовых строк $s $:</span><span class="sxs-lookup"><span data-stu-id="6fb2f-119">The `X` operation lets us prepare states of the form $\ket{s_0 s_1 \dots s_n}$ for some classical bit string $s$:</span></span>

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
> <span data-ttu-id="6fb2f-120">Позже мы увидим более компактные способы записи этой операции, не требующие управления потоком вручную.</span><span class="sxs-lookup"><span data-stu-id="6fb2f-120">Later, we will see more compact ways of writing this operation that do not require manual flow control.</span></span>

<span data-ttu-id="6fb2f-121">Также можно подготовить такие состояния, как $ \кет{+} = \лефт (\кет{0} + \кет{1}\ригхт)/\скрт{2}$ и $ \кет{-} = \лефт (\кет{0}-\кет{1}\ригхт)/\скрт{2}$ с помощью Хадамард Transform $H $, которое представлено в Q # встроенной операцией `H : (Qubit => Unit is Adj + Ctl)`:</span><span class="sxs-lookup"><span data-stu-id="6fb2f-121">We can also prepare states such as $\ket{+} = \left(\ket{0} + \ket{1}\right) / \sqrt{2}$ and $\ket{-} = \left(\ket{0} - \ket{1}\right) / \sqrt{2}$ by using the Hadamard transform $H$, which is represented in Q# by the intrinsic operation `H : (Qubit => Unit is Adj + Ctl)`:</span></span>

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

## <a name="measurements"></a><span data-ttu-id="6fb2f-122">Измерения</span><span class="sxs-lookup"><span data-stu-id="6fb2f-122">Measurements</span></span>

<span data-ttu-id="6fb2f-123">Используя операцию `Measure`, встроенную в неединую операцию, можно извлечь классическую информацию из объекта типа `Qubit` и присвоить классический результат, имеющий зарезервированный тип `Result`, указывающий, что результат больше не является состоянием такта.</span><span class="sxs-lookup"><span data-stu-id="6fb2f-123">Using the `Measure` operation, which is a built-in intrinsic non-unitary operation, we can extract classical information from an object of type `Qubit` and assign a classical value as a result, which has a reserved type `Result`, indicating that the result is no longer a quantum state.</span></span>
<span data-ttu-id="6fb2f-124">Входные данные для `Measure` — это Паули ось в блочной сфере, представленная значением типа `Pauli` (для экземпляра `PauliX`) и значением типа `Qubit`.</span><span class="sxs-lookup"><span data-stu-id="6fb2f-124">The input to `Measure` is a Pauli axis on the Bloch sphere, represented by a value of type `Pauli` (for instance `PauliX`) and an value of type `Qubit`.</span></span>

<span data-ttu-id="6fb2f-125">В качестве простого примера можно привести следующую операцию, которая выделяет один кубит в $ \кет{0}$ State, затем применяет операцию Хадамард `H` к ней и измеряет результат на `PauliZ`ной основе.</span><span class="sxs-lookup"><span data-stu-id="6fb2f-125">A simple example is the following operation, which allocates one qubit in the $\ket{0}$ state, then applies a Hadamard operation `H` to it and measures the result in the `PauliZ` basis.</span></span>

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

<span data-ttu-id="6fb2f-126">Чуть более сложный пример определяется следующей операцией, возвращающей логическое значение `true` если все Кубитс в регистре типа `Qubit[]` находятся в нулевом состоянии при измерении в заданной Паулиной базе и возвращают `false` в противном случае.</span><span class="sxs-lookup"><span data-stu-id="6fb2f-126">A slightly more complicated example is given by the following operation, which returns the Boolean value `true` if all qubits in a register of type `Qubit[]` are in the state zero when measured in a specified Pauli basis, and which returns `false` otherwise.</span></span>

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

<span data-ttu-id="6fb2f-127">Язык Q # позволяет классического потока управления зависеть от результатов измерения Кубитс.</span><span class="sxs-lookup"><span data-stu-id="6fb2f-127">The Q# language allows classical control flow to depend on the results of measuring qubits.</span></span>
<span data-ttu-id="6fb2f-128">Эта возможность, в свою очередь, позволяет реализовать мощные мини-приложения вероятностная, которые могут снизить вычислительные затраты для реализации унитариес.</span><span class="sxs-lookup"><span data-stu-id="6fb2f-128">This capability in turn enables implementing powerful probabilistic gadgets that can reduce the computational cost for implementing unitaries.</span></span>
<span data-ttu-id="6fb2f-129">В качестве примера можно легко реализовать так называемые шаблоны *повторения до успешного выполнения* (RUS) в Q #.</span><span class="sxs-lookup"><span data-stu-id="6fb2f-129">As an example, it is easy to implement so-called *Repeat-Until-Success* (RUS) patterns in Q#.</span></span>
<span data-ttu-id="6fb2f-130">Эти шаблоны RUS являются вероятностная программами, которые имеют *ожидаемую* низкую стоимость в терминах простейших шлюзов, но для которых реальная стоимость зависит от фактического запуска и фактического перехода различных вариантов ветвления.</span><span class="sxs-lookup"><span data-stu-id="6fb2f-130">These RUS patterns are probabilistic programs that have an *expected* low cost in terms of elementary gates, but for which the true cost depends on an actual run and an actual interleaving of various possible branchings.</span></span>

<span data-ttu-id="6fb2f-131">Чтобы упростить шаблоны повторения до успешного завершения (RUS), Q # поддерживает конструкцию</span><span class="sxs-lookup"><span data-stu-id="6fb2f-131">To facilitate Repeat-Until-Success (RUS) patterns, Q# supports the construct</span></span>

```qsharp
repeat {
    statementBlock1
}
until (expression)
fixup {
    statementBlock2
}
```

<span data-ttu-id="6fb2f-132">где `statementBlock1` и `statementBlock2` — ноль или более инструкций Q # и `expression` любое допустимое выражение, результатом вычисления которого является значение типа `Bool`.</span><span class="sxs-lookup"><span data-stu-id="6fb2f-132">where `statementBlock1` and `statementBlock2` are zero or more Q# statements, and `expression` any valid expression that evaluates to a value of type `Bool`.</span></span>
<span data-ttu-id="6fb2f-133">В типичном варианте использования следующая операция Q # реализует поворот вокруг иррациональная оси $ (I + 2i Z)/\скрт{5}$ в сфере БЛОЧ.</span><span class="sxs-lookup"><span data-stu-id="6fb2f-133">In a typical use case, the following Q# operation implements a rotation around an irrational axis of $(I + 2i Z)/\sqrt{5}$ on the Bloch sphere.</span></span> <span data-ttu-id="6fb2f-134">Это достигается с помощью известного шаблона RUS:</span><span class="sxs-lookup"><span data-stu-id="6fb2f-134">This is accomplished by using a known RUS pattern:</span></span>

```qsharp
operation ApplyVRotationUsingRUS(qubit : Qubit) : Unit {
    using (controls = Qubit[2]) {
        ApplyToEachA(H, controls);
        mutable finished = false;
        repeat {
            Controlled X(controls, qubit);
            S(qubit);
            Controlled X(controls, qubit);
            Z(qubit);
        }
        until (finished)
        fixup {
            if (MeasureIfAllQubitsAreZero(controls, PauliX)) {
                set finished = true;
            }
        }
    }
}
```

<span data-ttu-id="6fb2f-135">В этом примере показано использование изменяемой переменной `finished`, которая находится в области действия всего цикла Repeat-Until-unадресной привязки и инициализируется перед циклом и обновляется на шаге исправления.</span><span class="sxs-lookup"><span data-stu-id="6fb2f-135">This example shows the use of a mutable variable `finished` which is in scope of the entire repeat-until-fixup loop and which gets initialized before the loop and updated in the fixup step.</span></span>

<span data-ttu-id="6fb2f-136">Наконец, мы покажем пример шаблона RUS для подготовки состояния такта $ \фрак{1}{\скрт{3}} \лефт (\скрт{2}\кет{0}+ \кет{1}\ригхт) $, начиная с $ \кет{+} $ State.</span><span class="sxs-lookup"><span data-stu-id="6fb2f-136">Finally, we show an example of a RUS pattern to prepare a quantum state $\frac{1}{\sqrt{3}}\left(\sqrt{2}\ket{0}+\ket{1}\right)$, starting from the $\ket{+}$ state.</span></span>
<span data-ttu-id="6fb2f-137">См. также [Пример модульного тестирования, поставляемый со стандартной библиотекой](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):</span><span class="sxs-lookup"><span data-stu-id="6fb2f-137">See also the [unit testing sample provided with the standard library](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):</span></span>

```qsharp
operation PrepareStateUsingRUS(target : Qubit) : Unit {
    using (auxiliary = Qubit()) {
        H(auxiliary);
        repeat {
            // We expect the target and auxiliary qubits to each be in
            // the |+⟩ state.
            AssertProb(
                [PauliX], [target], Zero, 1.0,
                "target qubit should be in the |+⟩ state", 1e-10 );
            AssertProb(
                [PauliX], [auxiliary], Zero, 1.0,
                "auxiliary qubit should be in the |+⟩ state", 1e-10 );

            Adjoint T(auxiliary);
            CNOT(target, auxiliary);
            T(auxiliary);

            // The probability of measuring |+⟩ state on the auxiliary qubit
            // is 3/4.
            AssertProb(
                [PauliX], [auxiliary], Zero, 3. / 4.,
                "Error: the probability to measure |+⟩ in the first
                auxiliary must be 3/4",
                1e-10);

            // If we get the measurement outcome Zero, we prepare the
            // required state.
            let outcome = Measure([PauliX], [auxiliary]);
        }
        until (outcome == Zero)
        fixup {
            // Bring the auxiliary and target qubits back to |+⟩ state.
            if (outcome == One) {
                Z(auxiliary);
                X(target);
                H(target);
            }
        }
        // Return the auxiliary qubit back to the Zero state.
        H(auxiliary);
    }
}
```

<span data-ttu-id="6fb2f-138">Важные программные функции, показанные в этой операции, являются более сложными `fixup` части цикла, которая включает в себя операции обработки тактов, и использование `AssertProb` инструкций для определения вероятности измерения состояния такта в определенных точках программы.</span><span class="sxs-lookup"><span data-stu-id="6fb2f-138">Notable programmatic features shown in this operation are a more complex `fixup` part of the loop, which involves quantum operations, and the use of `AssertProb` statements to ascertain the probability of measuring the quantum state at certain specified points in the program.</span></span>
<span data-ttu-id="6fb2f-139">Дополнительные сведения об операциях [`Assert`](xref:microsoft.quantum.intrinsic.assert) и [`AssertProb`](xref:microsoft.quantum.intrinsic.assertprob) см. в разделе [тестирование и отладка](xref:microsoft.quantum.techniques.testing-and-debugging) .</span><span class="sxs-lookup"><span data-stu-id="6fb2f-139">See also [Testing and debugging](xref:microsoft.quantum.techniques.testing-and-debugging) for more information about the [`Assert`](xref:microsoft.quantum.intrinsic.assert) and [`AssertProb`](xref:microsoft.quantum.intrinsic.assertprob) operations.</span></span>
