---
uid: Microsoft.Quantum.Arrays.EqualA
title: Функция EQUAL
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: EqualA
qsharp.summary: Given two arrays of the same type and a predicate that is defined for pairs of elements of the arrays, checks whether the arrays are equal.
ms.openlocfilehash: 24fd76aaeb66081d6d8f1eaa3056117f54b5a5e7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730296"
---
# <a name="equala-function"></a>Функция EQUAL

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакеты [](https://nuget.org/packages/)


При наличии двух массивов одного типа и предиката, определенного для пар элементов массивов, проверяет, равны ли массивы.

```qsharp
function EqualA<'T> (equal : (('T, 'T) -> Bool), array1 : 'T[], array2 : 'T[]) : Bool
```


## <a name="input"></a>Входные данные

### <a name="equal--tt---bool"></a>равно: ('T) — > [bool](xref:microsoft.quantum.lang-ref.bool)

Функция из кортежа `('T, 'T)` в `Bool` , используемая для проверки того, равны ли два элемента массивов.


### <a name="array1--t"></a>Массив1: 'T []

Первый сравниваемый массив.


### <a name="array2--t"></a>Массив2: 'T []

Второй сравниваемый массив.



## <a name="output--bool"></a>Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)

Значение, `true` если и только если `array1` и `array2` равны.
То есть, если оба массива имеют одинаковую длину, и все элементы равны, как определено в `equal` .

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип элементов каждого массива.

## <a name="remarks"></a>Remarks

Эта функция определена для универсальных типов; Например, если у нас есть два массива `'T[]` и функция `equal: ('T, 'T) -> Bool` , эта функция возвращает `Bool` значение, указывающее, равны ли массивы.
Чтобы два массива считались равными, они должны иметь одинаковую длину, а элементы в одинаковых позициях массивов должны быть равны.