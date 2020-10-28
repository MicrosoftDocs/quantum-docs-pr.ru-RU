---
uid: Microsoft.Quantum.Arrays.TupleArrayAsNestedArray
title: Функция Туплеаррайаснестедаррай
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: TupleArrayAsNestedArray
qsharp.summary: Turns a list of 2-tuples into a nested array.
ms.openlocfilehash: 917f35db949790ab3ae6e7a2184bcfcf5ed50be6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729976"
---
# <a name="tuplearrayasnestedarray-function"></a>Функция Туплеаррайаснестедаррай

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакеты [](https://nuget.org/packages/)


Включает список из двух кортежей в вложенный массив.

```qsharp
function TupleArrayAsNestedArray<'T> (tupleList : ('T, 'T)[]) : 'T[][]
```


## <a name="input"></a>Входные данные

### <a name="tuplelist--tt"></a>Туплелист: ('T) []

Список кортежей из двух элементов, которые должны быть преобразованы в вложенный массив.



## <a name="output--t"></a>Выходные данные: 'T [] []

Вложенный массив с длиной, соответствующей Туплелист.

## <a name="example"></a>Например, .

```qsharp
// The following returns [[2, 3], [4, 5]]
TupleArrayAsNestedArray([(2, 3), (4, 5)]);
```

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

