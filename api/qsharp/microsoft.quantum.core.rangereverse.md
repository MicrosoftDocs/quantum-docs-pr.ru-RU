---
uid: Microsoft.Quantum.Core.RangeReverse
title: Функция Ранжереверсе
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeReverse
qsharp.summary: Returns a new range which is the reverse of the input range.
ms.openlocfilehash: f3b94d3c6fa6350a2c337f8bc8d889d24d87a85b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853657"
---
# <a name="rangereverse-function"></a>Функция Ранжереверсе

Пространство имен: [Microsoft. тактов. Core](xref:Microsoft.Quantum.Core)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


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