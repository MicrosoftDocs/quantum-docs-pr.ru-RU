---
uid: Microsoft.Quantum.Arrays.Subarray
title: Функция подмассивов
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Subarray
qsharp.summary: Takes an array and a list of locations and produces a new array formed from the elements of the original array that match the given locations.
ms.openlocfilehash: ccc041da0213d1f5dc5c8b4ff7a03b8b01ad107d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845419"
---
# <a name="subarray-function"></a>Функция подмассивов

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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