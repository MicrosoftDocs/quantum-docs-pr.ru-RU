---
uid: Microsoft.Quantum.Arrays.MappedOverRange
title: Функция Маппедоверранже
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedOverRange
qsharp.summary: Given a range and a function that takes an integer as input, returns a new array that consists of the images of the range values under the function.
ms.openlocfilehash: 7093043e2a290e6132774b8fe154d3627a254f27
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845655"
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

## <a name="example"></a>Пример

В этом примере добавляется 1 к диапазону четных чисел:

```qsharp
let numbers = MappedOverRange(PlusI(1, _), 0..2..10);
// numbers = [1, 3, 5, 7, 9, 11]
```

## <a name="remarks"></a>Remarks

Функция определена для универсальных типов, т. е. каждый раз, когда у нас есть функция, `mapper: Int -> 'T` можно сопоставлять значения диапазона и создавать массив типа `'T[]` .

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Arrays. сопоставить](xref:Microsoft.Quantum.Arrays.Mapped)