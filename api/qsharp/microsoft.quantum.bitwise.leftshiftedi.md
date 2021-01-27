---
uid: Microsoft.Quantum.Bitwise.LeftShiftedI
title: Функция Лефтшифтеди
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: LeftShiftedI
qsharp.summary: Shifts the bitwise representation of a number left by a given number of bits.
ms.openlocfilehash: 3f551bdba5c8e2a1456838769e4cee0660d0f969
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845307"
---
# <a name="leftshiftedi-function"></a>Функция Лефтшифтеди

Пространство имен: [Microsoft. тактов. побитовое](xref:Microsoft.Quantum.Bitwise)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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

```qsharp
let c = a <<< b;
let c = LeftShiftedI(a, b);
```