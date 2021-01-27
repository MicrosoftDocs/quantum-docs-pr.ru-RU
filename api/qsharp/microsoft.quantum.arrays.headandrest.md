---
uid: Microsoft.Quantum.Arrays.HeadAndRest
title: Функция Хеадандрест
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: HeadAndRest
qsharp.summary: Returns a tuple of first and all remaining elements of the array.
ms.openlocfilehash: c082e0a917343c18e5f511f065b2e78f1e217ecc
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848548"
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