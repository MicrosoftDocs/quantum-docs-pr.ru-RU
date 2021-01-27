---
uid: Microsoft.Quantum.Arithmetic.Carry
title: Выполнение операции
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: Carry
qsharp.summary: Implements a reversible carry gate. Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2` and the carry-out is xored to the qubit `carryOut`.
ms.openlocfilehash: dfb08a9a9c805c0b611ab993c9b1eb949810a7da
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843356"
---
# <a name="carry-operation"></a>Выполнение операции

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Реализует обратимый вентиль. Учитывая поразрядность, закодированную в кубит `carryIn` и два слагаемому бит, закодированные в `summand1` и `summand2` , вычисляют побитовое исключающее XOR `carryIn` , `summand1` а `summand2` в кубит, `summand2` а также ксоред в кубит `carryOut` .

```qsharp
operation Carry (carryIn : Qubit, summand1 : Qubit, summand2 : Qubit, carryOut : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="carryin--qubit"></a>выполнение: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Кубит.


### <a name="summand1--qubit"></a>summand1: [кубит](xref:microsoft.quantum.lang-ref.qubit)

First слагаемому кубит.


### <a name="summand2--qubit"></a>summand2: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Второй слагаемому кубит заменяется нижним битом суммы `summand1` и `summand2` .


### <a name="carryout--qubit"></a>выполнение: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Кубит для выполнения, будет ксоред с более высоким битом суммы.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

