---
title: Работа с кубитами
description: Описание заливки
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.qubits
no-loc:
- Q#
- $$v
ms.openlocfilehash: 6808a852ee0de7d3a38ea44e9637eeaa6bea382a
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2020
ms.locfileid: "87867868"
---
# <a name="working-with-qubits"></a>Работа с кубитами

Кубитс — это фундаментальный объект информации в тактовых вычислениях. Общие сведения о Кубитс см. в разделе [Общие сведения о тактовых вычислениях](xref:microsoft.quantum.overview.understanding), а также подробное описание их математического представления см. [в разделе кубит](xref:microsoft.quantum.concepts.qubit). 

В этой статье рассматривается использование и работа с Кубитс в Q# программе. 

> [!IMPORTANT]
>Ни одна из инструкций, обсуждаемых в этой статье, не является допустимой в теле функции. Они действительны только в пределах операций.

## <a name="allocating-qubits"></a>Выделение Кубитс

Поскольку физические Кубитс являются ценным ресурсом на такте, часть задания компилятора заключается в том, чтобы убедиться, что они используются как можно быстрее.
Таким образом, необходимо сообщить Q# о *выделении* Кубитс для использования в определенном блоке инструкций.
Можно выделить Кубитс как один кубит или как массив Кубитс, известный как *регистр*. 

### <a name="clean-qubits"></a>Очистить Кубитс

Используйте `using` инструкцию для выделения нового Кубитс для использования в блоке инструкций.

Оператор состоит из ключевого слова `using` , за которым следует привязка, заключенная в круглые скобки, `( )` и блок операторов, в рамках которого доступны Кубитс.
Привязка соответствует тому же шаблону, что и `let` инструкции: один символ или кортеж символов, за которым следует знак равенства `=` и одно значение или соответствующий кортеж *инициализаторов*.

Инициализаторы доступны для одного кубит, обозначенного как `Qubit()` , или массива Кубитс, `Qubit[n]` , где `n` является `Int` выражением.
например следующие.

```qsharp
using (qubit = Qubit()) {
    // ...
}
using ((auxiliary, register) = (Qubit(), Qubit[5])) {
    // ...
}
```

Все Кубитс, выделенные таким образом, запускаются в состоянии $ \кет {0} $. Таким образом, в предыдущем примере `auxiliary` — это один кубит в состоянии $ \кет {0} $, который `register` находится в пяти кубит State $ \кет {00000} = \кет {0} \отимес \кет {0} \отимес \кдотс \отимес \кет {0} $.
В конце `using` блока все Кубитс, выделенные этим блоком, немедленно освобождаются и не могут использоваться дальше.

> [!WARNING]
> Целевые компьютеры могут повторно использовать освобожденные Кубитс и предлагать их другим `using` блокам для выделения. Таким образом, целевой компьютер ждет, что Кубитс находятся в состоянии $ \кет {0} $ непосредственно перед освобождением.
> По возможности используйте единые операции для возврата всех выделенных Кубитс в $ \кет {0} $.
> При необходимости можно использовать @"microsoft.quantum.intrinsic.reset" операцию, которая возвращает кубит в $ \кет {0} $, измеряя ее и условно выполняя операцию на основе результата. Такое измерение уничтожает любые замкнутые с оставшимся Кубитс и может повлиять на вычисление.


### <a name="borrowed-qubits"></a>Заимствованный Кубитс

Используйте `borrowing` инструкцию для выделения Кубитс для временного использования, который не должен находиться в определенном состоянии.

Во время вычисления можно использовать заимствованный Кубитс в качестве вспомогательного пространства.
Обычно эти Кубитс не находятся в чистом состоянии, т. е. они не обязательно инициализируются в известном состоянии, например $ \кет {0} $.
Они часто называются «грязными» Кубитс, так как их состояние неизвестно и даже может быть запутанными с другими частями памяти компьютера-такта.

Привязка соответствует тому же шаблону и правилам, что и `using` оператор.
например следующие.
```qsharp
borrowing (qubit = Qubit()) {
    // ...
}
borrowing ((auxiliary, register) = (Qubit(), Qubit[5])) {
    // ...
}
```
Заимствованные Кубитс находятся в неизвестном состоянии и выходят за пределы области действия в конце блока инструкций.
Он фиксируется, чтобы выйти из Кубитс в том состоянии, в котором они были в момент их позаимствования. Это значит, что их состояние в начале и в конце блока инструкций должно быть одинаковым.
Так как это состояние не обязательно является классическим состоянием, в большинстве случаев области действия не должны содержать измерений. 

При заимствовании Кубитс система сначала пытается заполнить запрос от Кубитс, который используется, но недоступен в теле `borrowing` инструкции.
Если такой Кубитс не хватает, он выделяет новый Кубитс для выполнения запроса.

Между известными случаями использования «грязных» Кубитс являются реализации многофункциональных кнот шлюзов, требующие лишь очень мало Кубитс и реализации инкрементов.
Пример использования в см Q# . в статьях о [заимствовании Кубитс](#borrowing-qubits-example) в этой статье или в документе [*с использованием 2N + 2 Кубитс с Тоффоли модульного умножения*](https://arxiv.org/abs/1611.07995) (ханер, роеттелер и своре 2017) для алгоритма, использующего заимствованные Кубитс.

## <a name="intrinsic-operations"></a>Внутренние операции

После выделения можно передать кубит в функции и операции.
В некоторых случаях это все, что Q# программа может делать с кубит, так как действия, которые могут быть выполнены, определяются как операции.

В этой статье рассматриваются некоторые полезные Q# операции, которые можно использовать для взаимодействия с Кубитс.
Дополнительные сведения об этих и других функциях см. в разделе [встроенные операции и функции](xref:microsoft.quantum.libraries.standard.prelude). 

Во-первых, операторы Single-кубит Паули $X $, $Y $ и $Z $ представлены Q# встроенными операциями [`X`](xref:microsoft.quantum.intrinsic.x) , [`Y`](xref:microsoft.quantum.intrinsic.y) и [`Z`](xref:microsoft.quantum.intrinsic.z) , каждый из которых имеет тип `(Qubit => Unit is Adj + Ctl)` .

Как описано в [подставляемых операциях и функциях](xref:microsoft.quantum.libraries.standard.prelude), представьте $X $ и, следовательно, `X` как операцию побитового отражения или не является шлюзом.
Вы можете использовать `X` операцию для подготовки состояний вида $ \кет{s_0 s_1 \дотс s_n} $ для некоторых классических битовых строк $s $:

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
> Позже вы увидите более компактные способы записи этой операции, которые не нуждаются в ручном потоке управления.

Кроме того, можно подготовить такие состояния, как $ \кет{+} = \лефт (\кет {0} + \кет {1} \ригхт)/\скрт {2} $ и $ \кет {-} = \лефт (\кет {0} -\кет {1} \ригхт)/\скрт {2} $, с помощью хадамард Transform $H $, которое представлено Q# встроенной операцией [`H`](xref:microsoft.quantum.intrinsic.h) (также типа (кубит => единица "года + CTL)"):

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

## <a name="measurements"></a>Измерения

Измерения отдельных Кубитс можно выполнять в разных базах данных, каждый из которых представлен осью Паули в [БЛОЧ Sphere](xref:microsoft.quantum.glossary#bloch-sphere).
*Вычислительная базис* — это `PauliZ` базис, который является наиболее распространенным основанием для измерения.

### <a name="measure-a-single-qubit-in-the-pauliz-basis"></a>Измерение отдельного кубита в `PauliZ` основе

Используйте [`M`](xref:microsoft.quantum.intrinsic.m) операцию, встроенную в неединую операцию, для измерения отдельного кубита на `PauliZ` основе и присвойте результату классический.
`M`имеет зарезервированный возвращаемый тип, `Result` который может принимать только значения `Zero` или `One` соответствующие измеряемым состояниям $ \кет {0} $ или $ \кет {1} $ — указывает, что результат больше не является состоянием такта.

Простой пример — следующая операция, которая выделяет один кубит в состоянии $ \кет {0} $, затем применяет `H` к ней операцию хадамард и измеряет результат на `PauliZ` основе.

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

### <a name="measure-one-or-more-qubits-in-specific-bases"></a>Измерение одного или нескольких Кубитс в конкретных базовых базах

Для измерения массива из одного или нескольких Кубитс в конкретных базах данных можно использовать [`Measure`](xref:microsoft.quantum.intrinsic.measure) операцию.

Входные данные для `Measure` являются массивом `Pauli` типов (например, `[PauliX, PauliZ, PauliZ]` ) и массивом Кубитс.

Чуть более сложный пример определяется следующей операцией, возвращающей логическое значение, `true` Если все Кубитс в регистре типа `Qubit[]` находятся в нулевом состоянии при измерении в указанной Паули базе, и в `false` противном случае возвращает.

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

Обратите внимание, что этот пример по-прежнему выполняется только `Measure` для отдельных Кубитс по одному, но операция может быть расширена до совместного измерения на нескольких Кубитс.

## <a name="borrowing-qubits-example"></a>Пример заимствования Кубитс

В Canon есть примеры, использующие `borrowing` ключевое слово, например следующую функцию `MultiControlledXBorrow` . Если `controls` обозначает элемент управления Кубитс для добавления в `X` операцию, то число "грязных" [анЦиллас](xref:microsoft.quantum.glossary#ancilla) , добавленное этой реализацией, — `Length(controls)-2` .

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

Обратите внимание, что в этом примере используется широкое использование `With` объединения, в его форме, которая применима для операций, поддерживающих смежные, например `WithA` .
Это хороший стиль программирования, поскольку добавление элементов управления в структуры, включающие `With` Управление, распространяется только на внутреннюю операцию.
Кроме того, обратите внимание, что в дополнение к `body` операции `controlled` была предоставлена явная реализация тела операции, а не `controlled auto` инструкция.
Причиной этого является то, что из-за структуры канала можно легко добавить дополнительные элементы управления, что полезно по сравнению с добавлением элемента управления в каждый шлюз в `body` . 

Рекомендуется сравнить этот код с другой функцией Canon `MultiControlledXClean` , которая достигает той же цели реализации `X` операции, управляемой операцией умножения, но и использует несколько чистых Кубитс с помощью `using` механизма. 

## <a name="next-steps"></a>Дальнейшие шаги

Дополнительные сведения о [потоке управления](xref:microsoft.quantum.guide.controlflow) в Q# .