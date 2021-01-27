---
uid: Microsoft.Quantum.Intrinsic.R1Frac
title: Операция R1Frac
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: R1Frac
qsharp.summary: >-
  Applies a rotation about the $\ket{1}$ state by an angle specified as a dyadic fraction.

  \begin{align} R_1(n, k) \mathrel{:=} \operatorname{diag}(1, e^{i \pi k / 2^n}). \end{align}

  > [!WARNING] > This operation uses the **opposite** sign convention from > @"microsoft.quantum.intrinsic.r", and does not include the > factor of $1/ 2$ included by @"microsoft.quantum.intrinsic.r1".
ms.openlocfilehash: bfae01d11524f64ceebd53aa8544d7ea48c40f31
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98818692"
---
# <a name="r1frac-operation"></a>Операция R1Frac

Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Применяет поворот к {1} состоянию $ \кет $ на угол, заданный как дробь ДЯДИК.

\бегин{алигн} R_1 (n, k) \масрел{: =} \операторнаме{диаг} (1, e ^ {i \пи k/2 ^ n}).
\енд{алигн}

> [!WARNING]
> Эта операция использует **противоположное** соглашение о знаках из @"microsoft.quantum.intrinsic.r" и не включает фактор $1/2 $, включенный в @"microsoft.quantum.intrinsic.r1" .

```qsharp
operation R1Frac (numerator : Int, power : Int, qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

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
RFrac(PauliZ, -numerator, denominator + 1, qubit);
RFrac(PauliI, numerator, denominator + 1, qubit);
```