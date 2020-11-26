---
uid: Microsoft.Quantum.Arrays.All
title: ALL, функция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: All
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, and checks if all elements of the array satisfy the predicate.
ms.openlocfilehash: a7c83e38c3c101b712215eb664486fe29863a52b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221697"
---
# <a name="all-function"></a>ALL, функция

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии массива и предиката, определенного для элементов массива, и проверяет, удовлетворяет ли предикату все элементы массива.

```qsharp
function All<'T> (predicate : ('T -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a>Входные данные

### <a name="predicate--t---bool"></a>предикат: не> [bool](xref:microsoft.quantum.lang-ref.bool)

Функция из `'T` в `Bool` , используемая для проверки элементов.


### <a name="array--t"></a>массив: 'T []

Массив элементов `'T` .



## <a name="output--bool"></a>Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)

`Bool`Значение функции и предиката, применяемого ко всем элементам.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип `array` элементов.

## <a name="remarks"></a>Комментарии

Функция определена для универсальных типов, т. е. при наличии массива `'T[]` и функции `predicate: 'T -> Bool` мы можем получить `Bool` значение, которое указывает, соответствуют ли все элементы `predicate` .