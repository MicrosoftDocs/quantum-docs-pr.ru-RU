---
uid: Microsoft.Quantum.Arrays.Unique
title: Уникальная функция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Unique
qsharp.summary: Returns a new array that has no equal adjacent elements.
ms.openlocfilehash: 7964d5d41eb68cb05f9414164d69496c1f76eb08
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220014"
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

## <a name="remarks"></a>Комментарии

Если существует несколько элементов, которые равны, но не расположены рядом друг с другом, в выходном массиве будет несколько вхождений.  Используйте эту функцию вместе с `Sorted` для получения массива с общими уникальными элементами.