---
title: 'Переменные в Q #'
description: Описание заливки
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.variables
ms.openlocfilehash: 407b4ff3570816eb7bdc323a5c5b77dac2d951af
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2020
ms.locfileid: "83430906"
---
# <a name="variables-in-q"></a>Переменные в Q #

В Q # различаются изменяемые и неизменяемые символы, а также "переменные", которые связаны с выражениями или назначаются им.
Как правило, использование неизменяемых символов рекомендуется, поскольку оно позволяет компилятору выполнять более оптимизацию.

Левая часть привязки состоит из кортежа символов, а также с правой стороны выражения.

## <a name="immutable-variables"></a>Неизменяемые переменные

Значение любого типа в Q # можно присвоить переменной для повторного использования в операции или функции с помощью `let` ключевого слова.

Неизменяемая Привязка состоит из ключевого слова `let` , за которым следует символ или кортеж символов, знак равенства `=` , выражение для привязки символов к и завершающая точка с запятой.

например

```qsharp
let measurementOperator = [PauliX, PauliZ, PauliZ, PauliX, PauliI];
```

Это назначает определенный массив операторов Паули имени переменной (или символу) `measurementOperator` .

> [!NOTE]
> Нам не нужно явно указывать тип нашей новой переменной, так как выражение в правой части `let` оператора является неоднозначным и тип выводится компилятором. 

Переменные, определенные с помощью, `let` являются *неизменяемыми*. Это означает, что после определения она больше не может быть изменена каким бы то ни было.
Это обеспечивает несколько выгодных оптимизаций, включая оптимизацию классической логики, действующей на переменные, для изменения порядка применения `Adjoint` варианта операции.

## <a name="mutable-variables"></a>Изменяемые переменные

В качестве альтернативы созданию переменной с помощью `let` `mutable` ключевого слова будет создана изменяемая переменная, которая *может* быть повторно привязана после первоначального создания с использованием `set` ключевого слова.

Символы, объявленные и привязанные как часть `mutable` инструкции, могут быть повторно привязаны к другому значению позже в коде. Если символ повторно привязан позже в коде, его тип не изменится, а вновь привязанное значение должно быть совместимо с этим типом.

### <a name="rebinding-of-mutable-symbols"></a>Повторная привязка изменяемых символов

Изменяемую переменную можно повторно привязать с помощью `set` инструкции.
Такая повторная привязка состоит из ключевого слова `set` , за которым следует символ или кортеж символов, знак равенства `=` , выражение для повторной привязки символов к и завершающая точка с запятой.

Ниже приведены некоторые возможные примеры методов повторной привязки.

### <a name="apply-and-reassign-statements"></a>Операторы применения и повторного назначения

Определенный тип оператора, `set` который мы называем оператором *Apply-and-reassignя* , предоставляет удобный способ объединения, если правая часть состоит из приложения бинарного оператора, и результат должен быть повторно привязан к оператору в левом аргументе. Например, примененная к объекту директива
```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter += 1;
    // ...
}
```
увеличивает значение счетчика `counter` в каждой итерации `for` цикла. Приведенный выше код эквивалентен 
```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter = counter + 1;
    // ...
}
```

Аналогичные операторы доступны для всех бинарных операторов, в которых тип левой стороны соответствует типу выражения. Это предоставляет пример удобного способа накопления значений.

Например, допустим `qubits` является регситером Кубитс:
```qsharp
mutable results = new Result[0];   // results is an empty array of type Result[]
for (q in qubits) {
    set results += [M(q)];         // concatenate the outcome from measuring q to the existing array
    // ...
}
...                                // results contains the measurement outcomes from the whole register
```

### <a name="update-and-reassign-statements"></a>Операторы обновления и повторного назначения

Аналогичное объединение существует для [выражений копирования и обновления](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions) в правой части.
Соответственно, операторы *Update и reassignя* существуют для *именованных элементов* в определяемых пользователем типах, а также для *элементов массива*.  

```qsharp
newtype Complex = (Re : Double, Im : Double);

function ComplexSum(reals : Double[], ims : Double[]) : Complex[] {
    mutable res = Complex(0.,0.);

    for (r in reals) {
        set res w/= Re <- res::Re + r; // update-and-reassign statement
    }
    for (i in ims) {
        set res w/= Im <- res::Im + i; // update-and-reassign statement
    }
    return res;
}
```

В случае массивов [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) в стандартных библиотеках предоставляются необходимые средства для многих общих задач инициализации массива и управления ими, что позволяет избежать необходимости обновлять элементы массива в первую очередь. 

Инструкции обновления и повторного назначения предоставляют альтернативный вариант при необходимости:

```qsharp
operation GenerateRandomInts(max : Int, nSamples : Int) : Int[] {
    mutable samples = new Double[0];
    for (i in 1 .. nSamples) {
        set samples += [RandomInt(max)];
    }
    return samples;
}

operation SampleUniformDistrbution(nSamples : Int, nSteps : Int) : Double[] {
    let normalization = 1. / IntAsDouble(nSteps);
    mutable samples = GenerateRandomInts(nSteps, nSamples);
    
    for (i in IndexRange(samples) {
        let value = IntAsDouble(samples[i]);
        set samples w/= i <- normalization * value; // update-and-reassign statement
    }
}

```

Используя средства библиотеки для массивов, предоставляемых [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) , мы можем, например, легко определить функцию, возвращающую массив пола, где Паули по индексу `i` принимает заданное значение, а все остальные записи являются идентификатором.

Ниже приведены два определения такой функции, второй из которых использует средства в нашем выбытии.

```qsharp
function PauliEmbedding(pauli : Pauli, length : Int, location : Int) : Pauli[] {
    mutable pauliArray = new Pauli[length];             // initialize pauliArray of given length
    for (index in 0 .. length - 1) {                    // iterate over the integers in the length range
        set pauliArray w/= index <-                     // change the value at index to input pauli or PauliI
            index == location ? pauli | PauliI;         // cond. expression evaluating to pauli or PauliI dep. on whether index==location
    }    
    return pauliArray;
}
```

Вместо перебора по каждому индексу в массиве и условного присвоения ему значения `PauliI` или `Pauli` , мы можем использовать `ConstantArray` FROM [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) для создания массива `PauliI` , а затем просто возвращая выражение копирования и обновления, в котором мы изменили значение спеЦифк в индексе `location` :

```qsharp
function PauliEmbedding(pauli : Pauli, length : Int, location : Int) : Pauli[] {
    return ConstantArray(length, PauliI) w/ location <- pauli;
}
```

## <a name="tuple-deconstruction"></a>Деконструкция кортежа

Помимо присвоения одной переменной, `let` `mutable` Ключевые слова и---или на самом деле любые другие конструкции привязки, например `set` (описанные ниже)---также позволяют распаковать содержимое [типа кортежа](xref:microsoft.quantum.guide.types#tuple-types).
Назначение этой формы называется *деконструированием* элементов этого кортежа.

Если правая часть привязки является кортежем, то этот кортеж можно деконструировать после назначения.
Такие деконструкции могут содержать вложенные кортежи, а любая полная или частичная деконструкция является допустимой, если форма кортежа в правой части совместима с формой кортежа символов.

Пример:

```qsharp
let (i, f) = (5, 0.1); // i is bound to 5 and f to 0.1
mutable (a, (_, b)) = (1, (2, 3)); // a is bound to 1, b is bound to 3
mutable (x, y) = ((1, 2), [3, 4]); // x is bound to (1,2), y is bound to [3,4]
set (x, _, y) = ((5, 6), 7, [8]);  // x is rebound to (5,6), y is rebound to [8]
let (r1, r2) = MeasureTwice(q1, PauliX, q2, PauliY);
```

## <a name="binding-scopes"></a>Области привязки

Как правило, привязки к символам выходят за пределы области действия и становятся неработоспособными в конце блока операторов, в котором они встречаются.
Существует два исключения из этого правила:

- Привязка переменной цикла `for` цикла находится в области видимости тела цикла for, но не после конца цикла.
- Все три части `repeat` / `until` цикла (текст, тест и адресная привязка) обрабатываются как одна область, поэтому символы, привязанные к тексту, доступны в тесте и в адресной привязке.

Для обоих типов циклов каждый проход по циклу выполняется в своей собственной области, поэтому привязки из предыдущего прохода не будут доступны на более позднем этапе.
Подробные сведения об этих циклах можно найти в [потоке управления](xref:microsoft.quantum.guide.controlflow).

Привязки символов из внешних блоков наследуются внутренними блоками.
Символ может быть привязан только один раз для каждого блока; нельзя определить символ с тем же именем, что и у другого символа, находящихся в пределах области (без "тени").
Следующие последовательности будут допустимыми:

```qsharp
if (a == b) {
    ...
    let n = 5;
    ...             // n is 5
}
let n = 8;
...                 // n is 8
```

и

```qsharp
if (a == b) {
    ...
    let n = 5;
    ...             // n is 5
} else {
    ...
    let n = 8;
    ...             // n is 8
}
...                 // n is not bound to a value
```

Но это недопустимо:

```qsharp
let n = 5;
...                 // n is 5
let n = 8;          // Error!!
...
```

как:

```qsharp
let n = 8;
if (a == b) {
    ...             // n is 8
    let n = 5;      // Error!
    ...
}
...
```

## <a name="whats-next"></a>Дальнейшая работа
Дополнительные сведения о [работе с Кубитс](xref:microsoft.quantum.guide.qubits) в Q #.