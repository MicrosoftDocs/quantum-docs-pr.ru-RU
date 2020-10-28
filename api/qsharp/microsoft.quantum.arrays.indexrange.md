---
uid: Microsoft.Quantum.Arrays.IndexRange
title: Функция Индексранже
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexRange
qsharp.summary: Given an array, returns a range over the indices of that array, suitable for use in a for loop.
ms.openlocfilehash: 7f9779acd4a781c50388217aa780710bd0b99ff3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730201"
---
# <a name="indexrange-function"></a>Функция Индексранже

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакеты [](https://nuget.org/packages/)


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