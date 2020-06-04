---
title: Работа с кубитами
description: Описание заливки
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.qubits
ms.openlocfilehash: 0deb0729a88c49798f32a22a943b935d383c570b
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327549"
---
# <a name="working-with-qubits"></a>Работа с кубитами

Теперь, когда вы видели множество различных частей языка Q #, позвольте нам пробавиться от него и увидеть, как использовать сами Кубитс.

Обратите внимание, что ни одна из этих инструкций не разрешена в теле функции.
Они действительны только в пределах операций.

## <a name="allocating-qubits"></a>Выделение Кубитс

### <a name="clean-qubits"></a>Очистить Кубитс

`using`Оператор используется для *выделения* нового Кубитс для использования в блоке инструкций.

Оператор состоит из ключевого слова `using` , открывающей скобки, `(` привязки, закрывающей скобки `)` и блока инструкций, в котором Кубитс будет доступен.
Привязка соответствует тому же шаблону, что и `let` инструкции: один символ или кортеж символов, за которым следует знак равенства `=` и одно значение или соответствующий кортеж *инициализаторов*.

Инициализаторы доступны для одного кубит, обозначенного как `Qubit()` , или массива Кубитс, `Qubit[n]` , где `n` является `Int` выражением.
Например,

```qsharp
using (qubit = Qubit()) {
    // ...
}
using ((auxiliary, register) = (Qubit(), Qubit[5])) {
    // ...
}
```

Все Кубитс, выделенные таким образом, запускаются в $ \кет {0} $ State; в приведенном выше примере `register` — в состоянии $ \кет {00000} = \кет {0} \отимес \кет {0} \отимес \кдотс \отимес \кет {0} $.
В конце `using` блока все Кубитс, выделенные этим блоком, немедленно освобождаются и не могут использоваться дальше.

> [!WARNING]
> Целевые компьютеры предполагают, что Кубитс находятся в состоянии $ \кет {0} $ непосредственно перед освобождением, чтобы их можно было повторно использовать и предоставлять другим `using` блокам для выделения.
> По возможности используйте единые операции для возврата всех выделенных Кубитс в $ \кет {0} $.
> При необходимости @"microsoft.quantum.intrinsic.reset" можно использовать операцию для измерения кубит и использовать этот результат измерения, чтобы гарантировать, что измеряемый кубит возвращается в $ \кет {0} $. Такое измерение приведет к уничтожению всех замкнутые с оставшимся Кубитс и может повлиять на вычисление.


### <a name="borrowed-qubits"></a>Заимствованный Кубитс

`borrowing`Оператор используется, чтобы сделать Кубитс доступным для временного использования, который не должен находиться в определенном состоянии.

Механизм заимствования займов позволяет выделить Кубитс, который можно использовать в качестве вспомогательного пространства во время вычисления.
Обычно эти Кубитс не находятся в чистом состоянии, т. е. они не обязательно инициализируются в известном состоянии, например $ \кет {0} $.
Они часто называются «грязными» Кубитс, так как их состояние неизвестно и даже может быть запутанными с другими частями памяти компьютера-такта.

Привязка соответствует тому же шаблону и правилам, что и в `using` операторе.
Например,
```qsharp
borrowing (qubit = Qubit()) {
    // ...
}
borrowing ((auxiliary, register) = (Qubit(), Qubit[5])) {
    // ...
}
```
Заимствованные Кубитс находятся в неизвестном состоянии и выходят за пределы области действия в конце блока инструкций.
Он фиксируется, чтобы покинуть Кубитс в том состоянии, в котором они находились в момент заимствования, т. е. состояние в начале и в конце блока инструкции должны совпадать.
Это состояние в частности не всегда является классическим состоянием, поэтому в большинстве случаев области действия не должны содержать измерений. 

При заимствовании Кубитс система сначала пытается заполнить запрос от Кубитс, который используется, но к нему не обращаются в теле `borrowing` инструкции.
Если такой Кубитс не хватает, он выделит новый Кубитс для выполнения запроса.


Между известными случаями использования «грязных» Кубитс являются реализации многофункциональных кнот шлюзов, требующие лишь очень мало Кубитс и реализации инкрементов.
Примеры использования в Q #, а также использование [*2N + 2 Кубитс с модульным умножением на основе Тоффоли*](https://arxiv.org/abs/1611.07995) (Ханер, Роеттелер и своре 2017) для алгоритма, использующего заимствованные Кубитс, см. в приведенном ниже [примере заимствования Кубитс](#borrowing-qubits-example) .


## <a name="intrinsic-operations"></a>Внутренние операции

После выделения кубит можно передать в функции и операции.
В некоторых случаях это все, что программа Q # может делать с кубит, так как действия, которые могут быть выполнены, определяются как операции.
Мы более подробно рассмотрим эти операции в [подставляемых операциях и функциях](xref:microsoft.quantum.libraries.standard.prelude), но сейчас мы упомянули несколько полезных операций, которые можно использовать для взаимодействия с Кубитс.

Во-первых, операторы Single-кубит Паули $X $, $Y $ и $Z $ представлены в Q # встроенными операциями `X` , `Y` и `Z` , каждый из которых имеет тип `(Qubit => Unit is Adj + Ctl)` .
Как описано в [подставляемых операциях и функциях](xref:microsoft.quantum.libraries.standard.prelude), можно представить $X $ и, следовательно, `X` как операцию побитового отражения или не вентиль.
Эта `X` операция позволяет нам подготовить состояние вида $ \кет{s_0 s_1 \дотс s_n} $ для некоторых классических битовых строк $s $:

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

Также можно подготовить такие состояния, как $ \кет{+} = \лефт (\кет {0} + \кет {1} \ригхт)/\скрт {2} $ и $ \кет {-} = \лефт (\кет {0} -\кет {1} \ригхт)/\скрт {2} $, с помощью хадамард Transform $H $, которое представлено в Q # встроенной операцией `H : (Qubit => Unit is Adj + Ctl)` :

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

Используя `Measure` операцию, встроенную в неединую операцию, можно извлечь классическую информацию из объекта типа `Qubit` и присвоить классический результат, имеющий зарезервированный тип `Result` , указывающий на то, что результат больше не является состоянием такта.
Входные данные для `Measure` — это Паули ось в блочной сфере, представленной значением типа `Pauli` (например), `PauliX` и значением типа `Qubit` .

Простой пример — следующая операция, которая выделяет один кубит в состоянии $ \кет {0} $, затем применяет `H` к ней операцию хадамард и измеряет результат на `PauliZ` основе.

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

## <a name="borrowing-qubits-example"></a>Пример заимствования Кубитс

В Canon есть примеры, в которых используется `borrowing` ключевое слово, например `MultiControlledXBorrow` определенная ниже функция.
Если `controls` обозначает элемент управления Кубитс, который должен быть добавлен к `X` операции, то в `Length(controls)-2` этой реализации будет добавлена Общая часть "грязного" анЦиллас.

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

Обратите внимание, что широкое использование `With` ---объединения в своей форме, которое применимо для операций, поддерживающих прилегающие, т. е. `WithA` ---был сделан в этом примере.
Это хороший стиль программирования, поскольку добавление элементов управления в структуры, включающие `With` Управление, распространяется только на внутреннюю операцию.
Кроме того, обратите внимание, что в дополнение к `body` операции, реализация `controlled` тела операции была явно предоставлена, вместо того чтобы прибегнуть к `controlled auto` оператору.
Причина этого заключается в том, что мы понимаем, что из структуры канала можно легко добавить дополнительные элементы управления, которые полезны по сравнению с добавлением элемента управления в каждый отдельный шлюз в `body` . 

Рекомендуется сравнить этот код с другой функцией Canon `MultiControlledXClean` , которая достигает той же цели реализации `X` операции, управляемой операцией умножения, но и использует несколько чистых Кубитс с помощью `using` механизма. 

## <a name="next-steps"></a>Дальнейшие действия

Дополнительные сведения о [потоке управления](xref:microsoft.quantum.guide.controlflow) в Q #.