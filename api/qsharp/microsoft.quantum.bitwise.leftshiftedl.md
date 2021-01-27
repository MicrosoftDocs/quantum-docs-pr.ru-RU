---
uid: Microsoft.Quantum.Bitwise.LeftShiftedL
title: Функция Лефтшифтедл
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: LeftShiftedL
qsharp.summary: Shifts the bitwise representation of a number left by a given number of bits.
ms.openlocfilehash: 014653011574d0fabb4b9aa04cedf58b87ddf798
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842140"
---
# <a name="leftshiftedl-function"></a>Функция Лефтшифтедл

Пространство имен: [Microsoft. тактов. побитовое](xref:Microsoft.Quantum.Bitwise)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Сдвигает побитовое представление числа влево на заданное число битов.

```qsharp
function LeftShiftedL (value : BigInt, amount : Int) : BigInt
```


## <a name="input"></a>Входные данные

### <a name="value--bigint"></a>значение: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Число, битовое представление которого необходимо сдвинуть влево (более значимое значение).


### <a name="amount--int"></a>сумма: [int](xref:microsoft.quantum.lang-ref.int)

Число битов, на которое `value` будет перемещен влево.



## <a name="output--bigint"></a>Выходные данные: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Значение `value` , смещенное влево на `amount` биты.

## <a name="remarks"></a>Remarks

Следующие эквивалентны:

```qsharp
let c = a <<< b;
let c = LeftShiftedL(a, b);
```