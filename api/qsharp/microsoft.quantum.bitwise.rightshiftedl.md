---
uid: Microsoft.Quantum.Bitwise.RightShiftedL
title: Функция Ригхтшифтедл
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: RightShiftedL
qsharp.summary: Shifts the bitwise representation of a number right by a given number of bits.
ms.openlocfilehash: 3d941e1a0bcd96fe54ab01019293d883f11547a1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219521"
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

## <a name="remarks"></a>Комментарии

Следующие эквивалентны:

```Q#
let c = a >>> b;
let c = RightShiftedL(a, b);
```