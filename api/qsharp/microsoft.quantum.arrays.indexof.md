---
uid: Microsoft.Quantum.Arrays.IndexOf
title: IndexOf, функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexOf
qsharp.summary: Returns the first index of the first element in an array that satisfies a given predicate. If no such element exists, returns -1.
ms.openlocfilehash: 64db55e831078a7130a3ced6a30bfbd2299c392d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848528"
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



## <a name="example"></a>Пример

Предположим, что `IsEven : Int -> Bool` это функция, которая возвращает значение, `true` только если входные данные являются четными. Затем это можно использовать с `IndexOf` для поиска первого четного элемента в массиве:

```qsharp
let items = [1, 3, 17, 2, 21];
let idx = IndexOf(IsEven, items); // returns 3
```