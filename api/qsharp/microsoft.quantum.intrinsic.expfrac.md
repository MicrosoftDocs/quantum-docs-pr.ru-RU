---
uid: Microsoft.Quantum.Intrinsic.ExpFrac
title: Операция Експфрак
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: ExpFrac
qsharp.summary: >-
  Applies the exponential of a multi-qubit Pauli operator with an argument given by a dyadic fraction.

  \begin{align} e^{i \pi k [P_0 \otimes P_1 \cdots P_{N-1}] / 2^n}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.
ms.openlocfilehash: d11912a272387b087098f59e7ac071534b01c054
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711491"
---
# <a name="expfrac-operation"></a>Операция Експфрак

Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)

Пакеты [](https://nuget.org/packages/)


Применяет экспоненту оператора Multi-кубит Паули с аргументом, заданным в дробной части ДЯДИК.

\бегин{алигн} e ^ {i \пи k [P_0 \отимес P_1 \кдотс P_ {N-1}]/2 ^ N}, \енд{алигн}, где $P _i $ — это $i $ th элемента `paulis` , где $N = $ `Length(paulis)` .

```qsharp
operation ExpFrac (paulis : Pauli[], numerator : Int, power : Int, qubits : Qubit[]) : Unit
```


## <a name="input"></a>Входные данные

### <a name="paulis--pauli"></a>Пол: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]

Массив значений Single-кубит Паули, указывающих факторы продукта тензорные для каждого кубит.


### <a name="numerator--int"></a>Числитель: [int](xref:microsoft.quantum.lang-ref.int)

Числитель ($k $) в дробном представлении ДЯДИК угла, на которое будет поворачиваться регистр кубит.


### <a name="power--int"></a>степень: [int](xref:microsoft.quantum.lang-ref.int)

Степень двух ($n $), указывающая знаменатель угла, на который будет повернут регистр кубит.


### <a name="qubits--qubit"></a>Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Зарегистрируйтесь, чтобы применить заданный поворот к.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

