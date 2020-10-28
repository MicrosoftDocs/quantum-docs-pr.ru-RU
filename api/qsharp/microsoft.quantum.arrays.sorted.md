---
uid: Microsoft.Quantum.Arrays.Sorted
title: Функция сортировки
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Sorted
qsharp.summary: Given an array, returns the elements of that array sorted by a given comparison function.
ms.openlocfilehash: 14ac5325b81aec4ba0bf94a83cf00e086a075a7c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730025"
---
# <a name="sorted-function"></a>Функция сортировки

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакеты [](https://nuget.org/packages/)


При наличии массива возвращает элементы этого массива, отсортированные по заданной функции сравнения.

```qsharp
function Sorted<'T> (comparison : (('T, 'T) -> Bool), array : 'T[]) : 'T[]
```


## <a name="input"></a>Входные данные

### <a name="comparison--tt---bool"></a>Сравнение: ('T) — > [bool](xref:microsoft.quantum.lang-ref.bool)

Функция, которая сравнивает два элемента, которые `a` считаются меньше или равными, `b` Если `comparison(a, b)` имеет значение `true` .


### <a name="array--t"></a>массив: 'T []

Массив для сортировки.



## <a name="output--t"></a>Выходные данные: 'T []



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип каждого элемента `array` .

## <a name="remarks"></a>Remarks

`comparison`Предполагается, что функция является транзитивным, например, если `comparison(a, b)` `comparison(b, c)` `comparison(a, c)` предполагается и. Если это свойство не удерживает, выходные данные этой функции могут быть неправильными.

Так как это функция, результаты полностью детерминированные, даже если два элемента считаются равными по отношению к, `comparison` то есть когда `comparison(a, b)` и `comparison(b, a)` оба являются `true` .
В частности, сортировка, выполняемая этой функцией, гарантированно стабильной, поэтому если два элемента `a` и `b` выполняются в этом порядке в `array` и считаются равными в `comparison` , то `a` `b` в выходных данных также будет появляться.

Пример:

```Q#
function LastDigitLessThanOrEqual(left : Int, right : Int) : Bool {
    return LessThanOrEqualI(
        left % 10, right % 10
    );
}

function SortedByLastDigit() : Int[] {
    return Sorted(LastDigitLessThanOrEqual, [3, 37, 11, 17]);
}
// returns [11, 3, 37, 17].
```