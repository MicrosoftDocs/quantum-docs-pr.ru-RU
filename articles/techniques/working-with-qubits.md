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
# <a name="working-with-qubits"></a>Работа с Кубитс

Теперь, когда вы видели множество различных частей языка Q #, позвольте нам пробавиться от него и увидеть, как использовать сами Кубитс.

## <a name="allocating-qubits"></a>Выделение Кубитс

Во-первых, чтобы получить кубит, которую можно использовать в Q #, мы *выделили* Кубитс в блоке `using`:

```qsharp
using (register = Qubit[5]) {
    // Do stuff...
}
```

Все Кубитс, выделенные таким образом, запускаются в состоянии $ \кет{0}$. в приведенном выше примере `register` в состоянии $ \кет{00000} = \кет{0} \отимес \кет{0} \отимес \кдотс \отимес \кет{0}$.
В конце блока `using` все Кубитс, выделенные этим блоком, немедленно освобождаются и не могут использоваться дальше.

> [!WARNING]
> Целевые компьютеры предполагают, что Кубитс находятся в состоянии $ \кет{0}$ немедленно перед освобождением, поэтому их можно повторно использовать и предлагать другим блокам `using` для выделения.
> По возможности используйте единые операции для возврата всех выделенных Кубитс в $ \кет{0}$.
> При необходимости можно использовать операцию @"microsoft.quantum.intrinsic.reset" для измерения кубит, а также использовать этот результат измерения, чтобы гарантировать, что измеряемый кубит возвращается в $ \кет{0}$. Такое измерение приведет к уничтожению всех замкнутые с оставшимся Кубитс и может повлиять на вычисление.

## <a name="intrinsic-operations"></a>Внутренние операции

После выделения кубит можно передать в функции и операции.
В некоторых случаях это все, что программа Q # может делать с кубит, так как действия, которые могут быть выполнены, определяются как операции.
Мы более подробно рассмотрим эти операции в [подставляемых операциях и функциях](xref:microsoft.quantum.libraries.standard.prelude), но сейчас мы упомянули несколько полезных операций, которые можно использовать для взаимодействия с Кубитс.

Во-первых, операторы Single-кубит Паули $X $, $Y $ и $Z $ представлены в Q # встроенными операциями `X`, `Y`и `Z`, каждый из которых имеет тип `(Qubit => Unit is Adj + Ctl)`.
Как описано в [подставляемых операциях и функциях](xref:microsoft.quantum.libraries.standard.prelude), можно представить $X $ и, следовательно, `X` как операцию побитового отражения или не шлюз.
`X` операция позволяет нам подготовить состояния формы $ \кет{s_0 s_1 \дотс s_n} $ для некоторых классических битовых строк $s $:

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
> Позже мы увидим более компактные способы записи этой операции, не требующие управления потоком вручную.

Также можно подготовить такие состояния, как $ \кет{+} = \лефт (\кет{0} + \кет{1}\ригхт)/\скрт{2}$ и $ \кет{-} = \лефт (\кет{0}-\кет{1}\ригхт)/\скрт{2}$ с помощью Хадамард Transform $H $, которое представлено в Q # встроенной операцией `H : (Qubit => Unit is Adj + Ctl)`:

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

## <a name="measurements"></a>Измерения

Используя операцию `Measure`, встроенную в неединую операцию, можно извлечь классическую информацию из объекта типа `Qubit` и присвоить классический результат, имеющий зарезервированный тип `Result`, указывающий, что результат больше не является состоянием такта.
Входные данные для `Measure` — это Паули ось в блочной сфере, представленная значением типа `Pauli` (для экземпляра `PauliX`) и значением типа `Qubit`.

В качестве простого примера можно привести следующую операцию, которая выделяет один кубит в $ \кет{0}$ State, затем применяет операцию Хадамард `H` к ней и измеряет результат на `PauliZ`ной основе.

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

Чуть более сложный пример определяется следующей операцией, возвращающей логическое значение `true` если все Кубитс в регистре типа `Qubit[]` находятся в нулевом состоянии при измерении в заданной Паулиной базе и возвращают `false` в противном случае.

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

Язык Q # позволяет классического потока управления зависеть от результатов измерения Кубитс.
Эта возможность, в свою очередь, позволяет реализовать мощные мини-приложения вероятностная, которые могут снизить вычислительные затраты для реализации унитариес.
В качестве примера можно легко реализовать так называемые шаблоны *повторения до успешного выполнения* (RUS) в Q #.
Эти шаблоны RUS являются вероятностная программами, которые имеют *ожидаемую* низкую стоимость в терминах простейших шлюзов, но для которых реальная стоимость зависит от фактического запуска и фактического перехода различных вариантов ветвления.

Чтобы упростить шаблоны повторения до успешного завершения (RUS), Q # поддерживает конструкцию

```qsharp
repeat {
    statementBlock1
}
until (expression)
fixup {
    statementBlock2
}
```

где `statementBlock1` и `statementBlock2` — ноль или более инструкций Q # и `expression` любое допустимое выражение, результатом вычисления которого является значение типа `Bool`.
В типичном варианте использования следующая операция Q # реализует поворот вокруг иррациональная оси $ (I + 2i Z)/\скрт{5}$ в сфере БЛОЧ. Это достигается с помощью известного шаблона RUS:

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

В этом примере показано использование изменяемой переменной `finished`, которая находится в области действия всего цикла Repeat-Until-unадресной привязки и инициализируется перед циклом и обновляется на шаге исправления.

Наконец, мы покажем пример шаблона RUS для подготовки состояния такта $ \фрак{1}{\скрт{3}} \лефт (\скрт{2}\кет{0}+ \кет{1}\ригхт) $, начиная с $ \кет{+} $ State.
См. также [Пример модульного тестирования, поставляемый со стандартной библиотекой](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):

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

Важные программные функции, показанные в этой операции, являются более сложными `fixup` части цикла, которая включает в себя операции обработки тактов, и использование `AssertProb` инструкций для определения вероятности измерения состояния такта в определенных точках программы.
Дополнительные сведения об операциях [`Assert`](xref:microsoft.quantum.intrinsic.assert) и [`AssertProb`](xref:microsoft.quantum.intrinsic.assertprob) см. в разделе [тестирование и отладка](xref:microsoft.quantum.techniques.testing-and-debugging) .
