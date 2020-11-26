---
uid: Microsoft.Quantum.Arrays.Enumerated
title: Функция Enumerate
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Enumerated
qsharp.summary: Given an array, returns a new array containing elements of the original array along with the indices of each element.
ms.openlocfilehash: 94e8fdb7288bc43ed84d10a3292819b455a2be31
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221425"
---
# <a name="enumerated-function"></a>Функция Enumerate

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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