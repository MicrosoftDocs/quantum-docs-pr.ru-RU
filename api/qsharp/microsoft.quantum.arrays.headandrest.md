---
uid: Microsoft.Quantum.Arrays.HeadAndRest
title: Функция Хеадандрест
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: HeadAndRest
qsharp.summary: Returns a tuple of first and all remaining elements of the array.
ms.openlocfilehash: 9af4ba48a21d3cdf932b2f702051a70a6108db1b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730224"
---
# <a name="headandrest-function"></a>Функция Хеадандрест

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакеты [](https://nuget.org/packages/)


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