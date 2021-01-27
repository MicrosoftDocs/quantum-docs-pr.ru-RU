---
uid: Microsoft.Quantum.Arrays.FlatMapped
title: Функция Флатмаппед
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: FlatMapped
qsharp.summary: Given an array and a function that maps an array element to some output array, returns the concatenated output arrays for each array element.
ms.openlocfilehash: bee7002c5a1e80cee7907ff9cb4ebaaedf8e9923
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848642"
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

## <a name="example"></a>Пример

```qsharp
let Numbers = SequenceI(1, _); // generates numbers starting from 1
let values = FlatMapped(Numbers, [1, 2, 3]);
// values = [1, 1, 2, 1, 2, 3]
```