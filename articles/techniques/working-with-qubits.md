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
# <a name="working-with-qubits"></a>Работа с Кубитс #

Теперь, когда вы видели множество различных частей языка Q #, позвольте нам пробавиться от него и увидеть, как использовать сами Кубитс.

## <a name="allocating-qubits"></a>Выделение Кубитс ##

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

## <a name="intrinsic-operations"></a>Внутренние операции ##

После выделения кубит можно передать в функции и операции.
В некоторых случаях это все, что программа Q # может делать с кубит, так как действия, которые могут быть выполнены, определяются как операции.
Мы более подробно рассмотрим эти операции в [подставляемых операциях и функциях](xref:microsoft.quantum.libraries.standard.prelude), но сейчас мы упомянули несколько полезных операций, которые можно использовать для взаимодействия с Кубитс.

Во-первых, операторы Single-кубит Паули $X $, $Y $ и $Z $ представлены в Q # встроенными операциями `X`, `Y`и `Z`, каждый из которых имеет тип `(Qubit => Unit is Adj + Ctl)`.
Как описано в [подставляемых операциях и функциях](xref:microsoft.quantum.libraries.standard.prelude), можно представить $X $ и, следовательно, `X` как операцию побитового отражения или не шлюз.
Это позволяет нам подготовить состояния вида $ \ket{s_0 s_1 \дотс s_n} $ для некоторых классических битовых строк $s $:

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
> Позже мы увидим более компактные способы записи этой операции, не требующие управления потоком вручную.

Также можно подготовить такие состояния, как $ \кет{+} = \лефт (\кет{0} + \кет{1}\ригхт)/\скрт{2}$ и $ \кет{-} = \лефт (\кет{0}-\кет{1}\ригхт)/\скрт{2}$ с помощью преобразования Хадамард $H $ , который представлен в Q # встроенной операцией `H : (Qubit => Unit is Adj + Ctl)`:

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

## <a name="measurements"></a>Измерения ##

С помощью операции `Measure`, которая является встроенной встроенной операцией, можно извлечь классическую информацию из объекта типа `Qubit` и присвоить классический результат, который имеет зарезервированный тип `Result`, указывая, что результатом является No более длительное состояние такта. Входные данные для `Measure` — это Паули ось в блочной сфере, представленная объектом типа `Pauli` (например, для экземпляра `PauliX`) и объектом типа `Qubit`. 

Простой пример — это следующая операция, которая создает один кубит в{0}\кет, а затем применяет к ней ``H`` шлюз Хадамард, а затем вычисляет результат на основе `PauliZ`. 

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

Чуть более сложный пример определяется следующей операцией, возвращающей логическое значение `true` если все Кубитс в регистре типа `Qubit[]` находятся в нулевом состоянии, при измерении в заданной Паулиной базе и `false` иным образом. 

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

Язык Q # позволяет применять зависимости классического потока управления к результатам измерения Кубитс. Это, в свою очередь, позволяет реализовать мощные мини-приложения вероятностная, которые могут снизить затраты вычислительных ресурсов для реализации унитариес. В качестве примера можно легко реализовать так называемое *повторение до успешного выполнения* в Q #, представляющие собой вероятностнаяные цепи *с низкой* стоимостью в терминах простейших шлюзов, но для которых реальная стоимость зависит от фактического выполнения и фактического покидает различные возможные ветви. 

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
где `statementBlock1` и `statementBlock2` — ноль или более инструкций Q # и `expression` любое допустимое выражение, результатом вычисления которого является значение типа `Bool`. В типичном варианте использования в следующей цепи реализуется поворот вокруг иррациональная оси $ (I + 2i Z)/\скрт{5}$ в БЛОЧ Sphere. Это достигается с помощью известного шаблона RUS: 

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

В этом примере показано использование изменяемой переменной `finished`, которая находится в области действия всего цикла Repeat-Until-unадресной привязки и инициализируется перед циклом и обновляется на шаге исправления.

Наконец, мы покажем пример шаблона RUS для подготовки состояния такта $ \фрак{1}{\скрт{3}} \лефт (\скрт{2}\кет{0}+ \кет{1}\ригхт) $, начиная с $ \кет{+} $ State. См. также [Пример модульного тестирования, поставляемый со стандартной библиотекой](https://github.com/Microsoft/Quantum/blob/master/Samples/src/UnitTesting/RepeatUntilSuccessCircuits.qs): 

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
 
Важные программные функции, показанные в этой операции, являются более сложными `fixup` части цикла, которая включает в себя операции обработки тактов, и использование `AssertProb` инструкций для определения вероятности измерения состояния такта в определенных точках программу. Дополнительные сведения о `Assert` и инструкциях `AssertProb` см. в разделе [тестирование и отладка](xref:microsoft.quantum.techniques.testing-and-debugging) . 
