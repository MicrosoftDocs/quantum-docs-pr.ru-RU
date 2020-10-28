---
uid: Microsoft.Quantum.Core.RangeStep
title: Функция Ранжестеп
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeStep
qsharp.summary: Returns the integer that specifies how the next value of a range is calculated.
ms.openlocfilehash: f8e4c42330f2d6afdc1c0a9bdde36081ccab2f94
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713158"
---
# <a name="rangestep-function"></a>Функция Ранжестеп

Пространство имен: [Microsoft. тактов. Core](xref:Microsoft.Quantum.Core)

Пакеты [](https://nuget.org/packages/)


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