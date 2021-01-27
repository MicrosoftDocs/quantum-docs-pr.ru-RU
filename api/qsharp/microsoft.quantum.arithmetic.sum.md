---
uid: Microsoft.Quantum.Arithmetic.Sum
title: Операция суммирования
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: Sum
qsharp.summary: Implements a reversible sum gate. Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2`.
ms.openlocfilehash: e659c77a876e10df75f28ca1798fb0335e1bfb22
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847755"
---
# <a name="sum-operation"></a>Операция суммирования

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Реализует шлюз обратимой суммы. Учитывая поразрядность, закодированную в кубит `carryIn` и два бита слагаемому, закодированные в `summand1` и `summand2` , выполняет побитовую операцию XOR `carryIn` `summand1` и `summand2` в кубит `summand2` .

```qsharp
operation Sum (carryIn : Qubit, summand1 : Qubit, summand2 : Qubit) : Unit is Adj + Ctl
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