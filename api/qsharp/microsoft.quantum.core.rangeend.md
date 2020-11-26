---
uid: Microsoft.Quantum.Core.RangeEnd
title: Функция RangeEnd
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeEnd
qsharp.summary: Returns the defined end value of the given range, which is not necessarily the last element in the sequence.
ms.openlocfilehash: 90a9e31bf5c4a5e92a35998ddaec8c9e9de9888e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224043"
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

## <a name="remarks"></a>Комментарии

Первым элементом выражения диапазона является `start` , второй элемент —, `start+step` третий элемент — и `start+step+step` т. д., пока `end` не будет передан.

Обратите внимание, что определенное конечное значение диапазона может отличаться от последнего элемента последовательности, заданной диапазоном. Например, в диапазоне 0.. 2.. 5 последний элемент — 4, а конечное значение — 5.