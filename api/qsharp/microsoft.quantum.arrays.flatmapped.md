---
uid: Microsoft.Quantum.Arrays.FlatMapped
title: Функция Флатмаппед
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: FlatMapped
qsharp.summary: Given an array and a function that maps an array element to some output array, returns the concatenated output arrays for each array element.
ms.openlocfilehash: 3e75c7703471a2986812df660c2f9328f1536d22
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730272"
---
# <a name="flatmapped-function"></a>Функция Флатмаппед

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакеты [](https://nuget.org/packages/)


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