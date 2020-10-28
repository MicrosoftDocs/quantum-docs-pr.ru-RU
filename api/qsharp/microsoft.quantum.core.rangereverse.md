---
uid: Microsoft.Quantum.Core.RangeReverse
title: Функция Ранжереверсе
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeReverse
qsharp.summary: Returns a new range which is the reverse of the input range.
ms.openlocfilehash: d4e612d2f175015b7193634aeec12f9df12df7d3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713228"
---
# <a name="rangereverse-function"></a>Функция Ранжереверсе

Пространство имен: [Microsoft. тактов. Core](xref:Microsoft.Quantum.Core)

Пакеты [](https://nuget.org/packages/)


Возвращает новый диапазон, являющийся обратным по отношению к входному диапазону.

```qsharp
function RangeReverse (r : Range) : Range
```


## <a name="input"></a>Входные данные

### <a name="r--range"></a>r: [диапазон](xref:microsoft.quantum.lang-ref.range)

Входной диапазон.



## <a name="output--range"></a>Выходные данные: [диапазон](xref:microsoft.quantum.lang-ref.range)

Новый диапазон, являющийся обратным по отношению к заданному диапазону.

## <a name="remarks"></a>Remarks

Обратите внимание, что обратная часть диапазона не просто `end` .. `-step` .. `start` , поскольку фактический последний элемент диапазона может не совпадать с `end` .