---
uid: Microsoft.Quantum.Arrays.MappedOverRange
title: Функция Маппедоверранже
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedOverRange
qsharp.summary: Given a range and a function that takes an integer as input, returns a new array that consists of the images of the range values under the function.
ms.openlocfilehash: b1d73c2503e63ed09a3d6a56421760ca29eb0c3f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220694"
---
# <a name="mappedoverrange-function"></a>Функция Маппедоверранже

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии диапазона и функции, принимающей в качестве входных данных целое число, возвращает новый массив, состоящий из изображений значений диапазона в функции.

```qsharp
function MappedOverRange<'T> (mapper : (Int -> 'T), range : Range) : 'T[]
```


## <a name="input"></a>Входные данные

### <a name="mapper--int---t"></a>сопоставитель: [int](xref:microsoft.quantum.lang-ref.int) ->

Функция из `Int` в `'T` , используемая для отображения значений диапазона.


### <a name="range--range"></a>диапазон: [диапазон](xref:microsoft.quantum.lang-ref.range)

Диапазон целых чисел.



## <a name="output--t"></a>Выходные данные: 'T []

Массив `'T[]` элементов, сопоставленных с `mapper` функцией.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип результата `mapper` функции.

## <a name="remarks"></a>Комментарии

Функция определена для универсальных типов, т. е. каждый раз, когда у нас есть функция, `mapper: Int -> 'T` можно сопоставлять значения диапазона и создавать массив типа `'T[]` .

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Arrays. сопоставить](xref:Microsoft.Quantum.Arrays.Mapped)