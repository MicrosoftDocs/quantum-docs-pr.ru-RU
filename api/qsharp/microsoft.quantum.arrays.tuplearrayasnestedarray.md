---
uid: Microsoft.Quantum.Arrays.TupleArrayAsNestedArray
title: Функция Туплеаррайаснестедаррай
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: TupleArrayAsNestedArray
qsharp.summary: Turns a list of 2-tuples into a nested array.
ms.openlocfilehash: 51a35555080d1d2475fc1aa9e48e84c7c6f92c51
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845394"
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

