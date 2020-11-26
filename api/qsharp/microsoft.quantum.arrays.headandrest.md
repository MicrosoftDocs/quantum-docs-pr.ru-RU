---
uid: Microsoft.Quantum.Arrays.HeadAndRest
title: Функция Хеадандрест
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: HeadAndRest
qsharp.summary: Returns a tuple of first and all remaining elements of the array.
ms.openlocfilehash: 1144e00227df1cd7d96bc76b118b0b556adbaa96
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221085"
---
# <a name="headandrest-function"></a>Функция Хеадандрест

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает кортеж из первого и всех остальных элементов массива.

```qsharp
function HeadAndRest<'A> (array : 'A[]) : ('A, 'A[])
```


## <a name="input"></a>Входные данные

### <a name="array--a"></a>массив: ' A []

Массив, содержащий по крайней мере один элемент.



## <a name="output--aa"></a>Выходные данные: (' а, ' A [])

Кортеж из первого и всех остальных элементов массива.

## <a name="type-parameters"></a>Параметры типа

### <a name="a"></a>' A

Тип элементов массива.