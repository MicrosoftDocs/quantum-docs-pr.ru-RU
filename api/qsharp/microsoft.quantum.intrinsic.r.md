---
uid: Microsoft.Quantum.Intrinsic.R
title: Операция R
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: R
qsharp.summary: >-
  Applies a rotation about the given Pauli axis.

  \begin{align} R_{\mu}(\theta) \mathrel{:=} e^{-i \theta \sigma_{\mu} / 2}, \end{align} where $\mu \in \{I, X, Y, Z\}$.
ms.openlocfilehash: 1df4b1197e885e479339e542e8c1ffaeb392543d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98818713"
---
# <a name="r-operation"></a>Операция R

Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Применяет поворот к заданной оси Паули.

\бегин{алигн} R_ {\му} (\сета) \масрел{: =} e ^ {-i \сета \ sigma_ {\му}/2}, \енд{алигн}, где $ \му \ин \{ i, X, Y, Z \} $.

```qsharp
operation R (pauli : Pauli, theta : Double, qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="pauli--pauli"></a>Паули: [Паули](xref:microsoft.quantum.lang-ref.pauli)

Паули оператор ($ \му $) в возведен для образования вращения.


### <a name="theta--double"></a>тета: [двойной](xref:microsoft.quantum.lang-ref.double)

Угол поворота кубит.


### <a name="qubit--qubit"></a>Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Кубит, к которому должен быть применен шлюз.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

При вызове с `pauli = PauliI` Эта операция применяет *глобальный этап*. Этот этап может быть важен при использовании с `Controlled` функтор.