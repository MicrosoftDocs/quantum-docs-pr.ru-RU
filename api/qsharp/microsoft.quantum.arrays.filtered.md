---
uid: Microsoft.Quantum.Arrays.Filtered
title: Отфильтрованная функция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Filtered
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, returns an array that consists of those elements that satisfy the predicate.
ms.openlocfilehash: fa8600f4d773daf6eabf8b9961ab46961155d1fd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221272"
---
# <a name="filtered-function"></a>Отфильтрованная функция

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии массива и предиката, определенного для элементов массива, возвращает массив, состоящий из элементов, которые соответствуют предикату.

```qsharp
function Filtered<'T> (predicate : ('T -> Bool), array : 'T[]) : 'T[]
```


## <a name="input"></a>Входные данные

### <a name="predicate--t---bool"></a>предикат: не> [bool](xref:microsoft.quantum.lang-ref.bool)

Функция из `'T` в логическое значение, используемое для фильтрации элементов.


### <a name="array--t"></a>массив: 'T []

Массив элементов `'T` .



## <a name="output--t"></a>Выходные данные: 'T []

Массив `'T[]` элементов, которые соответствуют предикату.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип `array` элементов.

## <a name="remarks"></a>Комментарии

Функция определена для универсальных типов, т. е. при наличии массива `'T[]` и предиката `'T -> Bool` можно фильтровать элементы.