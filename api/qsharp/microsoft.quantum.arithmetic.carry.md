---
uid: Microsoft.Quantum.Arithmetic.Carry
title: Выполнение операции
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: Carry
qsharp.summary: Implements a reversible carry gate. Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2` and the carry-out is xored to the qubit `carryOut`.
ms.openlocfilehash: 2b977151861fb01be7d7dbad6e0a7b803fded880
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731641"
---
# <a name="carry-operation"></a>Выполнение операции

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакеты [](https://nuget.org/packages/)


Реализует обратимый вентиль. Учитывая поразрядность, закодированную в кубит `carryIn` и два слагаемому бит, закодированные в `summand1` и `summand2` , вычисляют побитовое исключающее XOR `carryIn` , `summand1` а `summand2` в кубит, `summand2` а также ксоред в кубит `carryOut` .

```qsharp
operation Carry (carryIn : Qubit, summand1 : Qubit, summand2 : Qubit, carryOut : Qubit) : Unit
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

