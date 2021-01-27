---
uid: Microsoft.Quantum.Core.RangeStep
title: Функция Ранжестеп
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeStep
qsharp.summary: Returns the integer that specifies how the next value of a range is calculated.
ms.openlocfilehash: 667b579337eec28d6b75de61668bd79de176883e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853601"
---
# <a name="rangestep-function"></a>Функция Ранжестеп

Пространство имен: [Microsoft. тактов. Core](xref:Microsoft.Quantum.Core)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Возвращает целое число, указывающее, как вычисляется следующее значение диапазона.

```qsharp
function RangeStep (range : Range) : Int
```


## <a name="input"></a>Входные данные

### <a name="range--range"></a>диапазон: [диапазон](xref:microsoft.quantum.lang-ref.range)





## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)

Заданное значение шага данного диапазона.

## <a name="remarks"></a>Remarks

Первым элементом выражения диапазона является `start` , второй элемент —, `start+step` третий элемент — и `start+step+step` т. д., пока `end` не будет передан.