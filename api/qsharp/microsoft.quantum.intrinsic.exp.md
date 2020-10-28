---
uid: Microsoft.Quantum.Intrinsic.Exp
title: Операция exp
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Exp
qsharp.summary: >-
  Applies the exponential of a multi-qubit Pauli operator.

  \begin{align} e^{i \theta [P_0 \otimes P_1 \cdots P_{N-1}]}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.
ms.openlocfilehash: b923374a954f90aba2deaead79dd419fbf67fea3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711520"
---
# <a name="exp-operation"></a>Операция exp

Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)

Пакеты [](https://nuget.org/packages/)


Применяет экспоненту оператора Multi-кубит Паули.

\бегин{алигн} e ^ {i \сета [P_0 \отимес P_1 \кдотс P_ {N-1}]}, \енд{алигн}, где $P _i $ — это $i $ TH элемент `paulis` , а $N = $ `Length(paulis)` .

```qsharp
operation Exp (paulis : Pauli[], theta : Double, qubits : Qubit[]) : Unit
```


## <a name="input"></a>Входные данные

### <a name="paulis--pauli"></a>Пол: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]

Массив значений Single-кубит Паули, указывающих факторы продукта тензорные для каждого кубит.


### <a name="theta--double"></a>тета: [двойной](xref:microsoft.quantum.lang-ref.double)

Угол для данного оператора Multi-кубит Паули, на который будет повернут целевой регистр.


### <a name="qubits--qubit"></a>Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Зарегистрируйтесь, чтобы применить заданный поворот к.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

