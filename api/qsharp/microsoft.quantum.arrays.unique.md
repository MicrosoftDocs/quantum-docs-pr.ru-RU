---
uid: Microsoft.Quantum.Arrays.Unique
title: Уникальная функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Unique
qsharp.summary: Returns a new array that has no equal adjacent elements.
ms.openlocfilehash: b3aa03d20195bdd8bb64783a9b68cafac29e68f6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850922"
---
# <a name="unique-function"></a>Уникальная функция

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает новый массив, у которого нет равных смежных элементов.

```qsharp
function Unique<'T> (equal : (('T, 'T) -> Bool), array : 'T[]) : 'T[]
```


## <a name="description"></a>Описание

При наличии массива элементов и функции для проверки равенства эта функция возвращает новый массив, в котором сохраняется относительный порядок элементов, но все смежные элементы, которые равны, фильтруются только в один элемент.

## <a name="input"></a>Входные данные

### <a name="equal--tt---bool"></a>равно: ('T) — > [bool](xref:microsoft.quantum.lang-ref.bool)

Функция, которая сравнивает два элемента, которые `a` считаются равными, `b` Если `equal(a, b)` имеет значение `true` .


### <a name="array--t"></a>массив: 'T []

Массив для фильтрации уникальных элементов.



## <a name="output--t"></a>Выходные данные: 'T []

Массив без равных смежных элементов.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип каждого элемента `array` .

## <a name="example"></a>Пример

```qsharp
let unique1 = Unique(EqualI, [1, 1, 3, 3, 2, 5, 5, 5, 7]);
// same as [1, 3, 2, 5, 7]
let unique2 = Unique(EqualI, [2, 2, 1, 1, 2, 2, 1, 1]);
// same as [2, 1, 2, 1];
let unique3 = Unique(EqualI, Sorted(LessThanOrEqualI, [2, 2, 1, 1, 2, 2, 1, 1]));
// same as [1, 2];
```

## <a name="remarks"></a>Remarks

Если существует несколько элементов, которые равны, но не расположены рядом друг с другом, в выходном массиве будет несколько вхождений.  Используйте эту функцию вместе с `Sorted` для получения массива с общими уникальными элементами.