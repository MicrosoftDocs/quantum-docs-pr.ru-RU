---
uid: Microsoft.Quantum.Core.RangeEnd
title: Функция RangeEnd
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeEnd
qsharp.summary: Returns the defined end value of the given range, which is not necessarily the last element in the sequence.
ms.openlocfilehash: 196fab0bd97a441a16976033dc0d660c54cdfd6a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98831368"
---
# <a name="rangeend-function"></a>Функция RangeEnd

Пространство имен: [Microsoft. тактов. Core](xref:Microsoft.Quantum.Core)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Возвращает определенное конечное значение заданного диапазона, которое не обязательно является последним элементом последовательности.

```qsharp
function RangeEnd (range : Range) : Int
```


## <a name="input"></a>Входные данные

### <a name="range--range"></a>диапазон: [диапазон](xref:microsoft.quantum.lang-ref.range)





## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)

Определенное конечное значение заданного диапазона.

## <a name="remarks"></a>Remarks

Первым элементом выражения диапазона является `start` , второй элемент —, `start+step` третий элемент — и `start+step+step` т. д., пока `end` не будет передан.

Обратите внимание, что определенное конечное значение диапазона может отличаться от последнего элемента последовательности, заданной диапазоном. Например, в диапазоне 0.. 2.. 5 последний элемент — 4, а конечное значение — 5.