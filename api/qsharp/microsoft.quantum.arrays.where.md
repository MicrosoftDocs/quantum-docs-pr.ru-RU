---
uid: Microsoft.Quantum.Arrays.Where
title: WHERE, функция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Where
qsharp.summary: Given a predicate and an array, returns the indices of that array where the predicate is true.
ms.openlocfilehash: 97598aa25d2d085aaab94f3d60ee64db9e2b89d6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219929"
---
# <a name="where-function"></a>WHERE, функция

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии предиката и массива возвращает индексы этого массива, где предикат имеет значение true.

```qsharp
function Where<'T> (predicate : ('T -> Bool), array : 'T[]) : Int[]
```


## <a name="input"></a>Входные данные

### <a name="predicate--t---bool"></a>предикат: не> [bool](xref:microsoft.quantum.lang-ref.bool)

Функция из `'T` в логическое значение, используемое для фильтрации элементов.


### <a name="array--t"></a>массив: 'T []

Массив элементов `'T` .



## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)[]

Массив индексов, где `predicate` имеет значение true.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип `array` элементов.