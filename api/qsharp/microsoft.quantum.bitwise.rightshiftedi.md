---
uid: Microsoft.Quantum.Bitwise.RightShiftedI
title: Функция Ригхтшифтеди
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: RightShiftedI
qsharp.summary: Shifts the bitwise representation of a number right by a given number of bits.
ms.openlocfilehash: 5c3106eb73178554184cbfb37333c027805c69f3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845255"
---
# <a name="rightshiftedi-function"></a>Функция Ригхтшифтеди

Пространство имен: [Microsoft. тактов. побитовое](xref:Microsoft.Quantum.Bitwise)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Сдвигает побитовое представление числа вправо на заданное число битов.

```qsharp
function RightShiftedI (value : Int, amount : Int) : Int
```


## <a name="input"></a>Входные данные

### <a name="value--int"></a>значение: [int](xref:microsoft.quantum.lang-ref.int)

Число, побитовое представление которого должно быть смещено вправо (менее значимое).


### <a name="amount--int"></a>сумма: [int](xref:microsoft.quantum.lang-ref.int)

Число битов, на которое `value` будет перемещено право.



## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)

Значение `value` , перемещенное вправо по `amount` битам.

## <a name="remarks"></a>Remarks

Следующие эквивалентны:

```qsharp
let c = a >>> b;
let c = RightShiftedI(a, b);
```