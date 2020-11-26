---
uid: Microsoft.Quantum.Arrays.TupleArrayAsNestedArray
title: Функция Туплеаррайаснестедаррай
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: TupleArrayAsNestedArray
qsharp.summary: Turns a list of 2-tuples into a nested array.
ms.openlocfilehash: c898178b6385b27f753509f0748a8b666b5066bd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220082"
---
# <a name="tuplearrayasnestedarray-function"></a>Функция Туплеаррайаснестедаррай

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Включает список из двух кортежей в вложенный массив.

```qsharp
function TupleArrayAsNestedArray<'T> (tupleList : ('T, 'T)[]) : 'T[][]
```


## <a name="input"></a>Входные данные

### <a name="tuplelist--tt"></a>Туплелист: ('T) []

Список кортежей из двух элементов, которые должны быть преобразованы в вложенный массив.



## <a name="output--t"></a>Выходные данные: 'T [] []

Вложенный массив с длиной, соответствующей Туплелист.

## <a name="example"></a>Пример

```qsharp
// The following returns [[2, 3], [4, 5]]
TupleArrayAsNestedArray([(2, 3), (4, 5)]);
```

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

