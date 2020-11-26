---
uid: Microsoft.Quantum.Arrays.IndexRange
title: Функция Индексранже
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexRange
qsharp.summary: Given an array, returns a range over the indices of that array, suitable for use in a for loop.
ms.openlocfilehash: 5afd4cc260ac3e384d2736bf7b43d941afd9ef73
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220949"
---
# <a name="indexrange-function"></a>Функция Индексранже

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


При наличии массива возвращает диапазон по индексам этого массива, который подходит для использования в цикле for.

```qsharp
function IndexRange<'TElement> (array : 'TElement[]) : Range
```


## <a name="input"></a>Входные данные

### <a name="array--telement"></a>массив: ' TElement []

Массив, для которого должен быть возвращен диапазон индексов.



## <a name="output--range"></a>Выходные данные: [диапазон](xref:microsoft.quantum.lang-ref.range)

Диапазон для всех индексов массива.

## <a name="type-parameters"></a>Параметры типа

### <a name="telement"></a>' TElement

Тип элементов массива.