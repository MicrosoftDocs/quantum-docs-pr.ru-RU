---
title: 'Поток управления в Q #'
description: Циклы, условные выражения и т. д.
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.controlflow
ms.openlocfilehash: 0cf62a128170bd0c28ff77f00fc23414567b1ea4
ms.sourcegitcommit: af10179284967bd7a72a52ae7e1c4da65c7d128d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "85415309"
---
# <a name="control-flow-in-q"></a>Поток управления в Q #

Внутри операции или функции каждая инструкция выполняется по порядку, аналогично другим общим императивным классическим языкам.
Однако поток управления можно изменить тремя разными способами:

* `if`инструкции
* `for`бираются
* `repeat-until-success`бираются

`if` `for` Конструкции потока управления и имеют привычный смысл для большинства классических языков программирования. [`Repeat-until-success`](#repeat-until-success-loop)циклы обсуждаются далее в этой статье.

Важно `for` ! циклы и `if` инструкции можно использовать в операциях, для которых создаются [специализации](xref:microsoft.quantum.guide.operationsfunctions) автоматически. В этом сценарии смежная часть `for` цикла обращается к направлению и принимает смежную часть каждой итерации.
Это действие следует принципу "обувь-and-Socks": Если вы хотите отменить размещение по протоколу SOCKS, а затем обувь, необходимо отменить размещение обувь, а затем отменить последующую операцию по протоколу SOCKS. 

## <a name="if-else-if-else"></a>If, else — if, else

`if`Оператор поддерживает условное выполнение.
Он состоит из ключевого слова `if` , логического выражения в круглых скобках и блока операторов (блок _then_ ).
При необходимости может следовать любое количество других предложений else-if, каждое из которых состоит из ключевого слова `elif` , логического выражения в круглых скобках и блока операторов ( _Else-If_ ).
Наконец, оператор может при необходимости завершиться предложением else, которое состоит из ключевого слова, `else` за которым следует другой блок операторов (блок _else_ ).

`if`Условие вычисляется, и, если оно равно *true*, выполняется блок *then* .
Если условие имеет *значение false*, то проверяется первое условие else-if; Если это так, то выполняется блок *Else-If* .
В противном случае второй блок-If вычисляет, а затем третий и т. д. до тех пор, пока не будет обнаружено предложение с истинным условием или отсутствуют другие предложения Else-If.
Если исходное условие *If* и все предложения Else-If имеют *значение false*, выполняется блок *else* , если он указан.

Обратите внимание, что любой блок выполняется в отдельной области.
Привязки, сделанные внутри `if` `elif` блока, или, `else` не видны после завершения блока.

Например,

```qsharp
if (result == One) {
    X(target);
    let n = 1;
    // n is bound
} 
// n is not bound
```
или
```qsharp
if (i == 1) {
    X(target);
    let n = 1;
} elif (i == 2) {
    Y(target);
    let m = n + 1; // would cause an error, because n is no longer bound
} else {
    Z(target);
}
```

## <a name="for-loop"></a>Цикл For

`for`Инструкция поддерживает итерацию по диапазону целых чисел или массиву.
Оператор состоит из ключевого слова `for` , за которым следует символ или кортеж символов, ключевое слово `in` , а также выражение типа `Range` или массива, все в круглых скобках и блок инструкций.

Блок операторов (тело цикла) выполняется повторно с определенным символом (переменной цикла), привязанным к каждому значению в диапазоне или массиве.
Обратите внимание, что если выражение диапазона принимает пустой диапазон или массив, тело не выполняется вообще.
Выражение полностью вычисляется перед входом в цикл и не изменяется во время выполнения цикла.

Переменная цикла привязывается к каждому входу в тело цикла и не привязана к концу тела.
Переменная цикла не привязана после завершения цикла for.
Привязка переменной цикла является неизменяемой и соответствует тем же правилам, что и другие привязки переменных. 

В этих примерах `qubits` используется регистр Кубитс (т. е. типа `Qubit[]` ), 

```qsharp
// ...
for (qubit in qubits) {  // iterate over each qubit value in the array qubits
    H(qubit);
}
// 'qubit' is no longer bound

mutable results = new (Int, Results)[Length(qubits)];
for (index in 0 .. Length(qubits) - 1) {  // iterates over the integers in the Range 0 .. (Length(qubits) - 1)
    set results w/= index <- (index, M(qubits[index])); // measure each qubit, updates the tuple value in the results array that at index 
}

mutable accumulated = 0;
for ((index, measured) in results) { // iterates over the tuple values in results
    if (measured == One) {
        set accumulated += 1 <<< index;
    }
}
```

Обратите внимание, что в конце мы использовали бинарный оператор арифметического сдвига влево `<<<` . Дополнительные сведения см. в разделе [числовые выражения](xref:microsoft.quantum.guide.expressions#numeric-expressions).

## <a name="repeat-until-success-loop"></a>Цикл "повторить" до "успешно"

Язык Q # позволяет классического потока управления зависеть от результатов измерения Кубитс.
Эта возможность, в свою очередь, позволяет реализовать мощные мини-приложения вероятностная, которые могут снизить вычислительные затраты для реализации унитариес.
Примерами являются шаблоны *повторение до успешного* завершения (RUS) в Q #.
Эти шаблоны RUS *представляют собой вероятностная программы с низкой* стоимостью в терминах простейших шлюзов. Стоимость полагается на фактическое выполнение и за несколько возможных ветвлений.

Чтобы упростить шаблоны повторения до успешного завершения (RUS), Q # поддерживает конструкции

```qsharp
repeat {
    // do stuff
}
until (expression)
fixup {
    // do other stuff
}
```

где `expression` — любое допустимое выражение, результатом вычисления которого является значение типа `Bool` .
Выполняется тело цикла, после чего вычисляется условие.
Если условие истинно, инструкция завершается; в противном случае запускается адресная привязка и инструкция запускается снова, начиная с тела цикла.

Все три части цикла RUS (текст, тест и адресная привязка) обрабатываются как единая область *для каждого повторения*, поэтому символы, привязанные к телу, доступны как в тесте, так и в адресной привязке.
Однако завершение выполнения адресной привязки завершает область действия инструкции, чтобы привязки символов, сделанные во время тела или исправления, были недоступны при последующих повторах.

Кроме того, `fixup` оператор часто полезен, но не всегда нужен.
В случаях, когда это не требуется, конструкция

```qsharp
repeat {
    // do stuff
}
until (expression);
```

также является допустимым шаблоном RUS.

Дополнительные примеры и подробные сведения см. в разделе [примеры повторения до успешного выполнения](#repeat-until-success-examples) в этой статье.

> [!TIP]   
> Избегайте использования циклов повторения до успешного выполнения в функциях. Используйте циклы *while* , чтобы обеспечить соответствующую функциональность внутри функций. 

## <a name="while-loop"></a>Цикл while

Шаблоны Repeat-Until-Success имеют очень много времени. Они широко используются в определенных классах алгоритмов такта, поэтому выделенная конструкция языка в Q #. Однако циклы, которые нарушаются в зависимости от условия и длина выполнения которого, таким способом, неизвестны во время компиляции, обрабатываются с определенной осторожностью в среде выполнения такта. Однако их использование в функциях не является проблемой, так как эти циклы содержат только код, который выполняется на обычном (не такте) оборудовании. 

Таким образом, Q # поддерживает использование циклов while только внутри функций. `while`Оператор состоит из ключевого слова `while` , логического выражения в круглых скобках и блока операторов.
Блок операторов (тело цикла) выполняется до тех пор, пока условие принимает значение `true` .

```qsharp
// ...
mutable (item, index) = (-1, 0);
while (index < Length(arr) && item < 0) { 
    set item = arr[index];
    set index += 1;
}
```

## <a name="return-statement"></a>Оператор Return

Оператор Return завершает выполнение операции или функции и возвращает значение вызывающему объекту.
Он состоит из ключевого слова `return` , за которым следует выражение соответствующего типа и завершающая точка с запятой.

Например,
```qsharp
return 1;
```
или
```qsharp
return (results, qubits);
```

* Вызываемый метод, возвращающий пустой кортеж, не `()` требует наличия оператора return.
* Чтобы указать ранний выход из операции или функции, используйте `return ();` .
Для вызова, возвращающего любой другой тип, требуется завершающий оператор return.
* В операции отсутствует максимальное число инструкций Return.
Компилятор может выдать предупреждение, если операторы следуют за оператором Return в блоке.

   
## <a name="fail-statement"></a>Оператор Fail

Оператор Fail завершает выполнение операции и возвращает вызывающему объекту значение ошибки.
Он состоит из ключевого слова `fail` , за которым следует строка и завершающая точка с запятой.
Инструкция возвращает строку в классический драйвер в качестве сообщения об ошибке.

Количество инструкций Fail в операции не ограничено.
Компилятор может выдать предупреждение, если операторы следуют за оператором Fail в блоке.

Например,

```qsharp
fail $"Impossible state reached";
```
или с помощью [интерполяции строк](xref:microsoft.quantum.guide.expressions#interpolated-strings),
```qsharp
fail $"Syndrome {syn} is incorrect";
```

## <a name="repeat-until-success-examples"></a>Примеры повторения до успешного выполнения

### <a name="rus-pattern-for-single-qubit-rotation-about-an-irrational-axis"></a>Шаблон RUS для однокубитного вращения по оси иррациональная 

В типичном варианте использования следующая операция Q # реализует поворот вокруг оси иррациональная $ (I + 2i Z)/\скрт {5} $ в БЛОЧ Sphere. В реализации используется известный шаблон RUS:

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

### <a name="rus-loop-with-a-mutable-variable-in-scope"></a>RUS-цикл с изменяемой переменной в области видимости

В этом примере показано использование изменяемой переменной, `finished` которая находится в области действия всего цикла повторения до и после цикла, которая инициализируется перед циклом и обновляется в шаге исправления.

```qsharp
mutable iter = 1;
repeat {
    ProbabilisticCircuit(qubits);
    let success = ComputeSuccessIndicator(qubits);
}
until (success || iter > maxIter)
fixup {
    iter += 1;
    ComputeCorrection(qubits);
}
```

### <a name="rus-without-fixup"></a>RUS без`fixup`

В этом примере показан цикл RUS без шага исправления. Код представляет собой цепь вероятностная, которая реализует важный шлюз ротации $V _3 = (\болдоне + 2 i Z)/\скрт {5} $ с использованием `H` `T` шлюзов и.
Цикл завершается в среднем на $ \фрак {8} {5} $.
Дополнительные сведения см. в разделе [*Повтор-Until-Success: недетерминированная декомпозиция одного кубит унитариес*](https://arxiv.org/abs/1311.1074) (Паетзникк и своре, 2014).

```qsharp
using (qubit = Qubit()) {
    repeat {
        H(qubit);
        T(qubit);
        CNOT(target, qubit);
        H(qubit);
        Adjoint T(qubit);
        H(qubit);
        T(qubit);
        H(qubit);
        CNOT(target, qubit);
        T(qubit);
        Z(target);
        H(qubit);
        let result = M(qubit);
    } until (result == Zero);
}
```

### <a name="rus-to-prepare-a-quantum-state"></a>RUS для подготовки состояния такта

Наконец, ниже приведен пример шаблона RUS для подготовки состояния такта $ \фрак {1} {\скрт {3} } \лефт (\скрт {2} \кет {0} + \кет {1} \ригхт) $, начиная с $ \кет{+} $ State.

В этой операции показаны следующие важные программные функции.

* Более сложная `fixup` часть цикла, включающая в себя операции обработки тактов. 
* Использование `AssertProb` инструкций для определения вероятности измерения состояния такта в некоторых указанных точках программы.

Дополнительные сведения об [`Assert`](xref:microsoft.quantum.intrinsic.assert) [`AssertProb`](xref:microsoft.quantum.intrinsic.assertprob) операциях и см. в разделе [тестирование и отладка](xref:microsoft.quantum.guide.testingdebugging).

```qsharp
operation PrepareStateUsingRUS(target : Qubit) : Unit {
    using (auxiliary = Qubit()) {
        H(auxiliary);
        repeat {
            // We expect the target and auxiliary qubits to each be in
            // the |+> state.
            AssertProb(
                [PauliX], [target], Zero, 1.0,
                "target qubit should be in the |+> state", 1e-10 );
            AssertProb(
                [PauliX], [auxiliary], Zero, 1.0,
                "auxiliary qubit should be in the |+> state", 1e-10 );

            Adjoint T(auxiliary);
            CNOT(target, auxiliary);
            T(auxiliary);

            // The probability of measuring |+> state on the auxiliary qubit
            // is 3/4.
            AssertProb(
                [PauliX], [auxiliary], Zero, 3. / 4.,
                "Error: the probability to measure |+> in the first
                auxiliary must be 3/4",
                1e-10);

            // If we get the measurement outcome Zero, we prepare the
            // required state.
            let outcome = Measure([PauliX], [auxiliary]);
        }
        until (outcome == Zero)
        fixup {
            // Bring the auxiliary and target qubits back to |+> state.
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

Дополнительные сведения см. [в разделе Пример модульного тестирования, предоставленный в стандартной библиотеке](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):

## <a name="next-steps"></a>Следующие шаги

Сведения о [тестировании и отладке](xref:microsoft.quantum.guide.testingdebugging) в Q #.
