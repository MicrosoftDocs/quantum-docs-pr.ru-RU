---
uid: Microsoft.Quantum.Bitwise.RightShiftedL
title: Функция Ригхтшифтедл
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: RightShiftedL
qsharp.summary: Shifts the bitwise representation of a number right by a given number of bits.
ms.openlocfilehash: 03ed69c7151e62b91c4a036e301f99b45ce5ab62
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842097"
---
# <a name="rightshiftedl-function"></a>Функция Ригхтшифтедл

Пространство имен: [Microsoft. тактов. побитовое](xref:Microsoft.Quantum.Bitwise)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Сдвигает побитовое представление числа вправо на заданное число битов.

```qsharp
function RightShiftedL (value : BigInt, amount : Int) : BigInt
```


## <a name="input"></a>Входные данные

### <a name="value--bigint"></a>значение: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Число, побитовое представление которого должно быть смещено вправо (менее значимое).


### <a name="amount--int"></a>сумма: [int](xref:microsoft.quantum.lang-ref.int)

Число битов, на которое `value` будет перемещено право.



## <a name="output--bigint"></a>Выходные данные: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Значение `value` , перемещенное вправо по `amount` битам.

## <a name="remarks"></a>Remarks

Следующие эквивалентны:

```qsharp
let c = a >>> b;
let c = RightShiftedL(a, b);
```