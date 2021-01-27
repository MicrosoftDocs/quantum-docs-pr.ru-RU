---
uid: Microsoft.Quantum.Arrays.IndexRange
title: Функция Индексранже
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexRange
qsharp.summary: Given an array, returns a range over the indices of that array, suitable for use in a for loop.
ms.openlocfilehash: 043b56a1ac3cbe5cd59cdd45d3725f301d81a6ee
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845779"
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

## <a name="example"></a>Пример

Следующие `for` циклы эквивалентны:

```qsharp
for (idx in IndexRange(array)) { ... }
for (idx in IndexRange(array)) { ... }
```