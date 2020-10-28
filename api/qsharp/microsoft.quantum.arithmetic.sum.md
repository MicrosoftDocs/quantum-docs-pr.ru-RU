---
uid: Microsoft.Quantum.Arithmetic.Sum
title: Операция суммирования
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: Sum
qsharp.summary: Implements a reversible sum gate. Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2`.
ms.openlocfilehash: b31d8ab39676ee6723e5fc053eba9e0af3ac2b2f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730440"
---
# <a name="sum-operation"></a>Операция суммирования

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакеты [](https://nuget.org/packages/)


Реализует шлюз обратимой суммы. Учитывая поразрядность, закодированную в кубит `carryIn` и два бита слагаемому, закодированные в `summand1` и `summand2` , выполняет побитовую операцию XOR `carryIn` `summand1` и `summand2` в кубит `summand2` .

```qsharp
operation Sum (carryIn : Qubit, summand1 : Qubit, summand2 : Qubit) : Unit
```


## <a name="input"></a>Входные данные

### <a name="carryin--qubit"></a>выполнение: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Кубит.


### <a name="summand1--qubit"></a>summand1: [кубит](xref:microsoft.quantum.lang-ref.qubit)

First слагаемому кубит.


### <a name="summand2--qubit"></a>summand2: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Второй слагаемому кубит заменяется нижним битом суммы `summand1` и `summand2` .



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

В отличие от `Carry` операции, это не приводит к вычислению бита выполнения.