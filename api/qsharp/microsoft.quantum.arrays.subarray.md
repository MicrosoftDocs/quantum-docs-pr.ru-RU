---
uid: Microsoft.Quantum.Arrays.Subarray
title: Функция подмассивов
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Subarray
qsharp.summary: Takes an array and a list of locations and produces a new array formed from the elements of the original array that match the given locations.
ms.openlocfilehash: be7b6ee1a396d67ebc311d8d97f4bd751a32d171
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730000"
---
# <a name="subarray-function"></a>Функция подмассивов

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакеты [](https://nuget.org/packages/)


Принимает массив и список расположений и создает новый массив, сформированный из элементов исходного массива, которые соответствуют заданным местам.

```qsharp
function Subarray<'T> (indices : Int[], array : 'T[]) : 'T[]
```


## <a name="input"></a>Входные данные

### <a name="indices--int"></a>индексы: [int](xref:microsoft.quantum.lang-ref.int)[]

Список целых чисел, используемый для определения подмассива.


### <a name="array--t"></a>массив: 'T []

Массив элементов `'T` .



## <a name="output--t"></a>Выходные данные: 'T []

Массив `out` элементов, индексы которых соответствуют подмассиву `out[idx] == array[indices[idx]]` .

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип `array` элементов.

## <a name="remarks"></a>Remarks

Функция определена для универсальных типов, т. е. при наличии массива `'T[]` и списка расположений, `Int[]` определяющих этот подмассив.
Построение подмассива основано на создании новой глубокой копии заданного массива, а не на обслуживании ссылок.

Если значение равно `Length(indices) < Length(array)` , эта функция вернет подмножество `array` . С другой стороны, если `indices` содержит повторяющиеся элементы, соответствующие элементы `array` будут также повторяться.
Если `indices` и `array` имеют одинаковую длину, эта функция предоставляет перестановки `array` .