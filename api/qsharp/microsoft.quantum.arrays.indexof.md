---
uid: Microsoft.Quantum.Arrays.IndexOf
title: IndexOf, функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexOf
qsharp.summary: Returns the first index of the first element in an array that satisfies a given predicate. If no such element exists, returns -1.
ms.openlocfilehash: 7ff80f13f432a18f216b2dee4bd65b1e82034fa5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730217"
---
# <a name="indexof-function"></a>IndexOf, функция

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакеты [](https://nuget.org/packages/)


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

