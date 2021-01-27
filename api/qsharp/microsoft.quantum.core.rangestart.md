---
uid: Microsoft.Quantum.Core.RangeStart
title: RangeStart, функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeStart
qsharp.summary: Returns the defined start value of the given range.
ms.openlocfilehash: 5b04e8c860a4bd6af7b10b4dbf803b1eb69ef5d8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98831120"
---
# <a name="rangestart-function"></a>RangeStart, функция

Пространство имен: [Microsoft. тактов. Core](xref:Microsoft.Quantum.Core)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


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