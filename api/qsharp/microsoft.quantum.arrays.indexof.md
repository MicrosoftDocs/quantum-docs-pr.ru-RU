---
uid: Microsoft.Quantum.Arrays.IndexOf
title: IndexOf, функция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexOf
qsharp.summary: Returns the first index of the first element in an array that satisfies a given predicate. If no such element exists, returns -1.
ms.openlocfilehash: d63b204334611f8f2c3860f9ee1d756f637780e2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221017"
---
# <a name="indexof-function"></a>IndexOf, функция

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает первый индекс первого элемента в массиве, удовлетворяющего заданному предикату. Если такого элемента не существует, возвращает значение-1.

```qsharp
function IndexOf<'T> (predicate : ('T -> Bool), arr : 'T[]) : Int
```


## <a name="input"></a>Входные данные

### <a name="predicate--t---bool"></a>предикат: не> [bool](xref:microsoft.quantum.lang-ref.bool)

Функция предиката, действующая на элементы массива.


### <a name="arr--t"></a>ARR: 'T []

Массив для поиска с использованием заданного предиката.



## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)

Наименьший индекс, `idx` такой как `predicate(arr[idx])` true, или-1, если такого элемента не существует.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

