---
uid: Microsoft.Quantum.Arrays.FlatMapped
title: Функция Флатмаппед
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: FlatMapped
qsharp.summary: Given an array and a function that maps an array element to some output array, returns the concatenated output arrays for each array element.
ms.openlocfilehash: e851e8503b3afcb4572f09fe39079247518c22c4
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221255"
---
# <a name="flatmapped-function"></a>Функция Флатмаппед

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии массива и функции, которая сопоставляет элемент массива с каким-либо выходным массивом, возвращает объединенные выходные массивы для каждого элемента массива.

```qsharp
function FlatMapped<'TInput, 'TOutput> (mapper : ('TInput -> 'TOutput[]), array : 'TInput[]) : 'TOutput[]
```


## <a name="input"></a>Входные данные

### <a name="mapper--tinput---toutput"></a>сопоставитель: ' Тинпут-> ' Таутпут []

Функция из `'TInput` в `'TOutput[]` , используемая для отображения элементов массива.


### <a name="array--tinput"></a>массив: ' Тинпут []

Массив элементов.



## <a name="output--toutput"></a>Выходные данные: ' Таутпут []

Массив `'TOutput[]` , который является объединением всех массивов, созданных функцией сопоставления.

## <a name="type-parameters"></a>Параметры типа

### <a name="tinput"></a>' Тинпут

Тип `array` элементов.
### <a name="toutput"></a>' Таутпут

`mapper`Функция возвращает массивы этого типа.