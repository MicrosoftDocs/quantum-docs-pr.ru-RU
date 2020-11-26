---
uid: Microsoft.Quantum.Arrays.Any
title: Любая функция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Any
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, checks if at least one element of the array satisfies the predicate.
ms.openlocfilehash: 717ab9ebcbb864a6faf1c14cd36125e589849f2e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221663"
---
# <a name="any-function"></a>Любая функция

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии массива и предиката, определенного для элементов массива, проверяет, удовлетворяет ли предикату хотя бы один элемент массива.

```qsharp
function Any<'T> (predicate : ('T -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a>Входные данные

### <a name="predicate--t---bool"></a>предикат: не> [bool](xref:microsoft.quantum.lang-ref.bool)

Функция из `'T` в `Bool` , используемая для проверки элементов.


### <a name="array--t"></a>массив: 'T []

Массив элементов `'T` .



## <a name="output--bool"></a>Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)

`Bool`Значение функции или предиката, применяемого ко всем элементам.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип `array` элементов.

## <a name="remarks"></a>Комментарии

Функция определена для универсальных типов, т. е. при наличии массива `'T[]` и функции `predicate: 'T -> Bool` мы можем получить `Bool` значение, которое указывает, удовлетворяет ли какой-либо элемент `predicate` .