---
uid: Microsoft.Quantum.Bitwise.LeftShiftedI
title: Функция Лефтшифтеди
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: LeftShiftedI
qsharp.summary: Shifts the bitwise representation of a number left by a given number of bits.
ms.openlocfilehash: ce68311adf211169c2fb499bb189332370a6d6ac
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729880"
---
# <a name="leftshiftedi-function"></a>Функция Лефтшифтеди

Пространство имен: [Microsoft. тактов. побитовое](xref:Microsoft.Quantum.Bitwise)

Пакеты [](https://nuget.org/packages/)


Сдвигает побитовое представление числа влево на заданное число битов.

```qsharp
function LeftShiftedI (value : Int, amount : Int) : Int
```


## <a name="input"></a>Входные данные

### <a name="value--int"></a>значение: [int](xref:microsoft.quantum.lang-ref.int)

Число, битовое представление которого необходимо сдвинуть влево (более значимое значение).


### <a name="amount--int"></a>сумма: [int](xref:microsoft.quantum.lang-ref.int)

Число битов, на которое `value` будет перемещен влево.



## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)

Значение `value` , смещенное влево на `amount` биты.

## <a name="remarks"></a>Remarks

Следующие эквивалентны:

```Q#
let c = a <<< b;
let c = LeftShiftedI(a, b);
```