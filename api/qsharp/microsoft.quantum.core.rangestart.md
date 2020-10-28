---
uid: Microsoft.Quantum.Core.RangeStart
title: RangeStart, функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeStart
qsharp.summary: Returns the defined start value of the given range.
ms.openlocfilehash: 3e4b0cebe34b4c98cb1d582a9cd11b46ff778517
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713171"
---
# <a name="rangestart-function"></a>RangeStart, функция

Пространство имен: [Microsoft. тактов. Core](xref:Microsoft.Quantum.Core)

Пакеты [](https://nuget.org/packages/)


Возвращает заданное начальное значение заданного диапазона.

```qsharp
function RangeStart (range : Range) : Int
```


## <a name="input"></a>Входные данные

### <a name="range--range"></a>диапазон: [диапазон](xref:microsoft.quantum.lang-ref.range)





## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)

Заданное начальное значение заданного диапазона.

## <a name="remarks"></a>Remarks

Первым элементом выражения диапазона является `start` , второй элемент —, `start+step` третий элемент — и `start+step+step` т. д., пока `end` не будет передан.

Обратите внимание, что определенное начальное значение диапазона совпадает с первым элементом последовательности, если диапазон не задает пустую последовательность (например, 2.. 1).