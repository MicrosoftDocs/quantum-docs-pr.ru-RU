---
uid: Microsoft.Quantum.Bitwise.RightShiftedI
title: Функция Ригхтшифтеди
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: RightShiftedI
qsharp.summary: Shifts the bitwise representation of a number right by a given number of bits.
ms.openlocfilehash: b20a4a8c281a470af9a4828f8a5ca905a7918723
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209780"
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

## <a name="remarks"></a>Комментарии

Следующие эквивалентны:

```Q#
let c = a >>> b;
let c = RightShiftedI(a, b);
```