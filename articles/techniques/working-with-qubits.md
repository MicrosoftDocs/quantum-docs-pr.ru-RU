---
title: Работа с Кубитс | Документация Майкрософт
description: Работа с Кубитс
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.techniques.qubits
ms.openlocfilehash: d1a8ccc9423a9a04e12bc98e3783790232b2f5d8
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/26/2019
ms.locfileid: "73183477"
---
# <a name="working-with-qubits"></a><span data-ttu-id="ca054-103">Работа с Кубитс</span><span class="sxs-lookup"><span data-stu-id="ca054-103">Working with Qubits</span></span> #

<span data-ttu-id="ca054-104">Теперь, когда вы видели множество различных частей языка Q #, позвольте нам пробавиться от него и увидеть, как использовать сами Кубитс.</span><span class="sxs-lookup"><span data-stu-id="ca054-104">Having now seen a variety of different parts of the Q# language, let us get into the thick of it and see how to use qubits themselves.</span></span>

## <a name="allocating-qubits"></a><span data-ttu-id="ca054-105">Выделение Кубитс</span><span class="sxs-lookup"><span data-stu-id="ca054-105">Allocating Qubits</span></span> ##

<span data-ttu-id="ca054-106">Во-первых, чтобы получить кубит, которую можно использовать в Q #, мы *выделили* Кубитс в блоке `using`:</span><span class="sxs-lookup"><span data-stu-id="ca054-106">First, to obtain a qubit that we can use in Q#, we *allocate* qubits within a `using` block:</span></span>

```qsharp
using (register = Qubit[5]) {
    // Do stuff...
}
```

<span data-ttu-id="ca054-107">Все Кубитс, выделенные таким образом, запускаются в состоянии $ \кет{0}$. в приведенном выше примере `register` в состоянии $ \кет{00000} = \кет{0} \отимес \кет{0} \отимес \кдотс \отимес \кет{0}$.</span><span class="sxs-lookup"><span data-stu-id="ca054-107">Any qubits allocated in this way start off in the $\ket{0}$ state; in the example above, `register` is thus in the state $\ket{00000} = \ket{0} \otimes \ket{0} \otimes \cdots \otimes \ket{0}$.</span></span>
<span data-ttu-id="ca054-108">В конце блока `using` все Кубитс, выделенные этим блоком, немедленно освобождаются и не могут использоваться дальше.</span><span class="sxs-lookup"><span data-stu-id="ca054-108">At the end of the `using` block, any qubits allocated by that block are immediately deallocated and cannot be used further.</span></span>

> [!WARNING]
> <span data-ttu-id="ca054-109">Целевые компьютеры предполагают, что Кубитс находятся в состоянии $ \кет{0}$ немедленно перед освобождением, поэтому их можно повторно использовать и предлагать другим блокам `using` для выделения.</span><span class="sxs-lookup"><span data-stu-id="ca054-109">Target machines expect that qubits are in the $\ket{0}$ state immediately before deallocation, so that they can be reused and offered to other `using` blocks for allocation.</span></span>
> <span data-ttu-id="ca054-110">По возможности используйте единые операции для возврата всех выделенных Кубитс в $ \кет{0}$.</span><span class="sxs-lookup"><span data-stu-id="ca054-110">Whenever possible, use unitary operations to return any allocated qubits to $\ket{0}$.</span></span>
> <span data-ttu-id="ca054-111">При необходимости можно использовать операцию @"microsoft.quantum.intrinsic.reset" для измерения кубит, а также использовать этот результат измерения, чтобы гарантировать, что измеряемый кубит возвращается в $ \кет{0}$.</span><span class="sxs-lookup"><span data-stu-id="ca054-111">If need be, the @"microsoft.quantum.intrinsic.reset" operation can be used to measure a qubit instead, and to use that measurement result to ensure that the measured qubit is returned to $\ket{0}$.</span></span> <span data-ttu-id="ca054-112">Такое измерение приведет к уничтожению всех замкнутые с оставшимся Кубитс и может повлиять на вычисление.</span><span class="sxs-lookup"><span data-stu-id="ca054-112">Such a measurement will destroy any entanglement with the remaining qubits and can thus impact the computation.</span></span> 

## <a name="intrinsic-operations"></a><span data-ttu-id="ca054-113">Внутренние операции</span><span class="sxs-lookup"><span data-stu-id="ca054-113">Intrinsic Operations</span></span> ##

<span data-ttu-id="ca054-114">После выделения кубит можно передать в функции и операции.</span><span class="sxs-lookup"><span data-stu-id="ca054-114">Once allocated, a qubit can then be passed to functions and operations.</span></span>
<span data-ttu-id="ca054-115">В некоторых случаях это все, что программа Q # может делать с кубит, так как действия, которые могут быть выполнены, определяются как операции.</span><span class="sxs-lookup"><span data-stu-id="ca054-115">In some sense, this is all that a Q# program can do with a qubit, as the actions that can be taken are all defined as operations.</span></span>
<span data-ttu-id="ca054-116">Мы более подробно рассмотрим эти операции в [подставляемых операциях и функциях](xref:microsoft.quantum.libraries.standard.prelude), но сейчас мы упомянули несколько полезных операций, которые можно использовать для взаимодействия с Кубитс.</span><span class="sxs-lookup"><span data-stu-id="ca054-116">We will see these operations in more detail in [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude), but for now, we mention a few useful operations that can be used to interact with qubits.</span></span>

<span data-ttu-id="ca054-117">Во-первых, операторы Single-кубит Паули $X $, $Y $ и $Z $ представлены в Q # встроенными операциями `X`, `Y`и `Z`, каждый из которых имеет тип `(Qubit => Unit is Adj + Ctl)`.</span><span class="sxs-lookup"><span data-stu-id="ca054-117">First, the single-qubit Pauli operators $X$, $Y$, and $Z$ are represented in Q# by the intrinsic operations `X`, `Y`, and `Z`, each of which has type `(Qubit => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="ca054-118">Как описано в [подставляемых операциях и функциях](xref:microsoft.quantum.libraries.standard.prelude), можно представить $X $ и, следовательно, `X` как операцию побитового отражения или не шлюз.</span><span class="sxs-lookup"><span data-stu-id="ca054-118">As described in [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude), we can think of $X$ and hence of `X` as a bit-flip operation or NOT gate.</span></span>
<span data-ttu-id="ca054-119">Это позволяет нам подготовить состояния вида $ \ket{s_0 s_1 \дотс s_n} $ для некоторых классических битовых строк $s $:</span><span class="sxs-lookup"><span data-stu-id="ca054-119">This lets us prepare states of the form $\ket{s_0 s_1 \dots s_n}$ for some classical bit string $s$:</span></span>

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

operation Example() : Unit {

    using (register = Qubit[8]) {
        PrepareBitString(
            [true, true, false, false, true, false, false, true],
            register
        );
        // At this point, register now has the state |11001001〉.
    }
}
```

> [!TIP]
> <span data-ttu-id="ca054-120">Позже мы увидим более компактные способы записи этой операции, не требующие управления потоком вручную.</span><span class="sxs-lookup"><span data-stu-id="ca054-120">Later, we will see more compact ways of writing this operation that do not require manual flow control.</span></span>

<span data-ttu-id="ca054-121">Также можно подготовить такие состояния, как $ \кет{+} = \лефт (\кет{0} + \кет{1}\ригхт)/\скрт{2}$ и $ \кет{-} = \лефт (\кет{0}-\кет{1}\ригхт)/\скрт{2}$ с помощью преобразования Хадамард $H $ , который представлен в Q # встроенной операцией `H : (Qubit => Unit is Adj + Ctl)`:</span><span class="sxs-lookup"><span data-stu-id="ca054-121">We can also prepare states such as $\ket{+} = \left(\ket{0} + \ket{1}\right) / \sqrt{2}$ and $\ket{-} = \left(\ket{0} - \ket{1}\right) / \sqrt{2}$ by using the Hadamard transform $H$, which is represented in Q# by the intrinsic operation `H : (Qubit => Unit is Adj + Ctl)`:</span></span>

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

## <a name="measurements"></a><span data-ttu-id="ca054-122">Измерения</span><span class="sxs-lookup"><span data-stu-id="ca054-122">Measurements</span></span> ##

<span data-ttu-id="ca054-123">С помощью операции `Measure`, которая является встроенной встроенной операцией, можно извлечь классическую информацию из объекта типа `Qubit` и присвоить классический результат, который имеет зарезервированный тип `Result`, указывая, что результатом является No более длительное состояние такта.</span><span class="sxs-lookup"><span data-stu-id="ca054-123">Using the `Measure` operation, which is a built in intrinsic non-unitary operation, we can extract classical information from an object of type `Qubit` and assign a classical value as a result, which has a reserved type `Result`, indicating that the result is no longer a quantum state.</span></span> <span data-ttu-id="ca054-124">Входные данные для `Measure` — это Паули ось в блочной сфере, представленная объектом типа `Pauli` (например, для экземпляра `PauliX`) и объектом типа `Qubit`.</span><span class="sxs-lookup"><span data-stu-id="ca054-124">The input to `Measure` is a Pauli axis on the Bloch sphere, represented by an object of type `Pauli` (i.e., for instance `PauliX`) and an object of type `Qubit`.</span></span> 

<span data-ttu-id="ca054-125">Простой пример — это следующая операция, которая создает один кубит в{0}\кет, а затем применяет к ней ``H`` шлюз Хадамард, а затем вычисляет результат на основе `PauliZ`.</span><span class="sxs-lookup"><span data-stu-id="ca054-125">A simple example is the following operation which creates one qubit in the $\ket{0}$ state, then applies a Hadamard gate ``H`` to it and then measures the result in the `PauliZ` basis.</span></span> 

```qsharp
operation MeasurementOneQubit () : Result {

    // The following using block creates a fresh qubit and initializes it 
    // in the |0〉 state.
    using (qubit = Qubit()) {
        // We apply a Hadamard operation H to the state, thereby creating the 
        // state 1/sqrt(2)(|0〉+|1〉). 
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

<span data-ttu-id="ca054-126">Чуть более сложный пример определяется следующей операцией, возвращающей логическое значение `true` если все Кубитс в регистре типа `Qubit[]` находятся в нулевом состоянии, при измерении в заданной Паулиной базе и `false` иным образом.</span><span class="sxs-lookup"><span data-stu-id="ca054-126">A slightly more complicated example is given by the following operation which returns the Boolean value `true` if all qubits in a register of type `Qubit[]` are in the state zero, when measured in a specified Pauli basis and `false` otherwise.</span></span> 

```qsharp
operation AllMeasurementsZero (qs : Qubit[], pauli : Pauli) : Bool {

    mutable value = true;
    for (q in qs) {
        if ( Measure([pauli], [q]) == One ) {
            set value = false;
        }
    }
    return value;
}
```

<span data-ttu-id="ca054-127">Язык Q # позволяет применять зависимости классического потока управления к результатам измерения Кубитс.</span><span class="sxs-lookup"><span data-stu-id="ca054-127">The Q# language allows dependencies of classical control flow on measurement results of qubits.</span></span> <span data-ttu-id="ca054-128">Это, в свою очередь, позволяет реализовать мощные мини-приложения вероятностная, которые могут снизить затраты вычислительных ресурсов для реализации унитариес.</span><span class="sxs-lookup"><span data-stu-id="ca054-128">This in turn enables to implement powerful probabilistic gadgets that can reduce the computational cost for implementing unitaries.</span></span> <span data-ttu-id="ca054-129">В качестве примера можно легко реализовать так называемое *повторение до успешного выполнения* в Q #, представляющие собой вероятностнаяные цепи *с низкой* стоимостью в терминах простейших шлюзов, но для которых реальная стоимость зависит от фактического выполнения и фактического покидает различные возможные ветви.</span><span class="sxs-lookup"><span data-stu-id="ca054-129">As an example, it is easy to implement so-called *Repeat-Until-Success* in Q# which are probabilistic circuits that have an *expected* low cost in terms of elementary gates, but for which the true cost depends on an actual run and an actual interleaving of various possible branchings.</span></span> 

<span data-ttu-id="ca054-130">Чтобы упростить шаблоны повторения до успешного завершения (RUS), Q # поддерживает конструкцию</span><span class="sxs-lookup"><span data-stu-id="ca054-130">To facilitate Repeat-Until-Success (RUS) patterns, Q# supports the construct</span></span>
```qsharp
repeat {
    statementBlock1 
}
until (expression)
fixup {
    statementBlock2
}
```
<span data-ttu-id="ca054-131">где `statementBlock1` и `statementBlock2` — ноль или более инструкций Q # и `expression` любое допустимое выражение, результатом вычисления которого является значение типа `Bool`.</span><span class="sxs-lookup"><span data-stu-id="ca054-131">where `statementBlock1` and `statementBlock2` are zero or more Q# statements, and `expression` any valid expression that evaluates to a value of type `Bool`.</span></span> <span data-ttu-id="ca054-132">В типичном варианте использования в следующей цепи реализуется поворот вокруг иррациональная оси $ (I + 2i Z)/\скрт{5}$ в БЛОЧ Sphere.</span><span class="sxs-lookup"><span data-stu-id="ca054-132">In a typical use case, the following circuit implements a rotation around an irrational axis of $(I + 2i Z)/\sqrt{5}$ on the Bloch sphere.</span></span> <span data-ttu-id="ca054-133">Это достигается с помощью известного шаблона RUS:</span><span class="sxs-lookup"><span data-stu-id="ca054-133">This is accomplished by using a known RUS pattern:</span></span> 

```qsharp
operation RUScircuit (qubit : Qubit) : Unit {

    using(ancillas = Qubit[2]) {
        ApplyToEachA(H, ancillas);
        mutable finished = false;
        repeat {
            Controlled X(ancillas, qubit);
            S(qubit);
            Controlled X(ancillas, qubit);
            Z(qubit);
        }
        until(finished)
        fixup {
            if AllMeasurementsZero(ancillas, Xpauli) {
                set finished = true;
            }
        }
    }
}
```

<span data-ttu-id="ca054-134">В этом примере показано использование изменяемой переменной `finished`, которая находится в области действия всего цикла Repeat-Until-unадресной привязки и инициализируется перед циклом и обновляется на шаге исправления.</span><span class="sxs-lookup"><span data-stu-id="ca054-134">This example shows the use of a mutable variable `finished` which is in scope of the entire repeat-until-fixup loop and which gets initialized before the loop and updated in the fixup step.</span></span>

<span data-ttu-id="ca054-135">Наконец, мы покажем пример шаблона RUS для подготовки состояния такта $ \фрак{1}{\скрт{3}} \лефт (\скрт{2}\кет{0}+ \кет{1}\ригхт) $, начиная с $ \кет{+} $ State.</span><span class="sxs-lookup"><span data-stu-id="ca054-135">Finally, we show an example of a RUS pattern to prepare a quantum state $\frac{1}{\sqrt{3}}\left(\sqrt{2}\ket{0}+\ket{1}\right)$, starting from the $\ket{+}$ state.</span></span> <span data-ttu-id="ca054-136">См. также [Пример модульного тестирования, поставляемый со стандартной библиотекой](https://github.com/Microsoft/Quantum/blob/master/Samples/src/UnitTesting/RepeatUntilSuccessCircuits.qs):</span><span class="sxs-lookup"><span data-stu-id="ca054-136">See also the [unit testing sample provided with the standard library](https://github.com/Microsoft/Quantum/blob/master/Samples/src/UnitTesting/RepeatUntilSuccessCircuits.qs):</span></span> 

```qsharp
operation RepeatUntilSuccessStatePreparation( target : Qubit ) : Unit {

    using( ancilla = Qubit() ) {
        H(ancilla);
        repeat {
            // We expect target and ancilla qubit to be in |+⟩ state.
            AssertProb( 
                [PauliX], [target], Zero, 1.0, 
                "target qubit should be in the |+⟩ state", 1e-10 );
            AssertProb( 
                [PauliX], [ancilla], Zero, 1.0,
                "ancilla qubit should be in the |+⟩ state", 1e-10 );
                
            Adjoint T(ancilla);
            CNOT(target, ancilla);
            T(ancilla);

            // The probability of measuring |+⟩ state on ancilla is 3/4.
            AssertProb( 
                [PauliX], [ancilla], Zero, 3. / 4., 
                "Error: the probability to measure |+⟩ in the first 
                ancilla must be 3/4",
                1e-10);

            // If we get measurement outcome Zero, we prepare the required state 
            let outcome = Measure([PauliX], [ancilla]);
        }
        until( outcome == Zero )
        fixup {
            // Bring ancilla and target back to |+⟩ state
            if( outcome == One ) {
                Z(ancilla);
                X(target);
                H(target);
            }
        }
        // Return ancilla back to Zero state
        H(ancilla);
    }
}
```
 
<span data-ttu-id="ca054-137">Важные программные функции, показанные в этой операции, являются более сложными `fixup` части цикла, которая включает в себя операции обработки тактов, и использование `AssertProb` инструкций для определения вероятности измерения состояния такта в определенных точках программу.</span><span class="sxs-lookup"><span data-stu-id="ca054-137">Notable programmatic features shown in this operation are a more complex `fixup` part of the loop which involves quantum operations, and the use of `AssertProb` statements to ascertain the probability of measuring the quantum state at certain specified points in the program.</span></span> <span data-ttu-id="ca054-138">Дополнительные сведения о `Assert` и инструкциях `AssertProb` см. в разделе [тестирование и отладка](xref:microsoft.quantum.techniques.testing-and-debugging) .</span><span class="sxs-lookup"><span data-stu-id="ca054-138">See also [Testing and debugging](xref:microsoft.quantum.techniques.testing-and-debugging) for more information about `Assert` and `AssertProb` statements.</span></span> 
