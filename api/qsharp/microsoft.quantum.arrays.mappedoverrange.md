---
uid: Microsoft.Quantum.Arrays.MappedOverRange
title: Функция Маппедоверранже
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedOverRange
qsharp.summary: Given a range and a function that takes an integer as input, returns a new array that consists of the images of the range values under the function.
ms.openlocfilehash: e527a3ca1fd7571836f4f79bb453581f53d1db2b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730129"
---
# <a name="mappedoverrange-function"></a>Функция Маппедоверранже

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакеты [](https://nuget.org/packages/)


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

## <a name="remarks"></a>Remarks

Функция определена для универсальных типов, т. е. каждый раз, когда у нас есть функция, `mapper: Int -> 'T` можно сопоставлять значения диапазона и создавать массив типа `'T[]` .

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Arrays. сопоставить](xref:Microsoft.Quantum.Arrays.Mapped)