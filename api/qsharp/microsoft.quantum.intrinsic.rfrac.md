---
uid: Microsoft.Quantum.Intrinsic.RFrac
title: Операция Рфрак
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: RFrac
qsharp.summary: >-
  Applies a rotation about the given Pauli axis by an angle specified as a dyadic fraction.

  \begin{align} R_{\mu}(n, k) \mathrel{:=} e^{i \pi n \sigma_{\mu} / 2^k}, \end{align} where $\mu \in \{I, X, Y, Z\}$.

  > [!WARNING] > This operation uses the **opposite** sign convention from > @"microsoft.quantum.intrinsic.r".
ms.openlocfilehash: c80bb2b394e83c1133ed6ddc1640a3d88563ca6e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98818478"
---
# <a name="rfrac-operation"></a>Операция Рфрак

Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Применяет поворот к заданной оси Паули на угол, заданный как дробь ДЯДИК.

\бегин{алигн} R_ {\му} (n, k) \масрел{: =} e ^ {i \пи n \ sigma_ {\му}/2 ^ k}, \енд{алигн}, где $ \му \ин \{ i, X, Y, Z \} $.

> [!WARNING]
> В этой операции используется **противоположное** соглашение о знаках из @"microsoft.quantum.intrinsic.r" .

```qsharp
operation RFrac (pauli : Pauli, numerator : Int, power : Int, qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="pauli--pauli"></a>Паули: [Паули](xref:microsoft.quantum.lang-ref.pauli)

Паули оператор возведен для образования вращения.


### <a name="numerator--int"></a>Числитель: [int](xref:microsoft.quantum.lang-ref.int)

Числитель в ДЯДИК дробное представление угла, на которое поворачивается кубит.


### <a name="power--int"></a>степень: [int](xref:microsoft.quantum.lang-ref.int)

Степень 2, указывающая знаменатель угла, на который будет поворачиваться кубит.


### <a name="qubit--qubit"></a>Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Кубит, к которому должен быть применен шлюз.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

Эквивалентно:

```qsharp
// PI() is a Q# function that returns an approximation of π.
R(pauli, -PI() * IntAsDouble(numerator) / IntAsDouble(2 ^ (power - 1)), qubit);
```