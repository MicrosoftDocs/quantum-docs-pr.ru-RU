---
uid: Microsoft.Quantum.Arrays.Enumerated
title: Функция Enumerate
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Enumerated
qsharp.summary: Given an array, returns a new array containing elements of the original array along with the indices of each element.
ms.openlocfilehash: 0a591025a4eef79e08b47527c0bdb556f5645334
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730305"
---
# <a name="enumerated-function"></a>Функция Enumerate

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакеты [](https://nuget.org/packages/)


При наличии массива возвращает новый массив, содержащий элементы исходного массива вместе с индексами каждого элемента.

```qsharp
function Enumerated<'TElement> (array : 'TElement[]) : (Int, 'TElement)[]
```


## <a name="input"></a>Входные данные

### <a name="array--telement"></a>массив: ' TElement []

Массив, элементы которого необходимо перечислить.



## <a name="output--inttelement"></a>Выходные данные: ([int](xref:microsoft.quantum.lang-ref.int), ' TElement ') []

Новый массив, содержащий элементы исходного массива вместе с их индексами.

## <a name="type-parameters"></a>Параметры типа

### <a name="telement"></a>' TElement

Тип элементов массива.