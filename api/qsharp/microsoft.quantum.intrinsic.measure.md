---
uid: Microsoft.Quantum.Intrinsic.Measure
title: Операция измерения
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Measure
qsharp.summary: >-
  Performs a joint measurement of one or more qubits in the specified Pauli bases.

  The output result is given by the distribution: \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \frac12 \braket{ \psi \mid| \left( \boldone + P_0 \otimes P_1 \otimes \cdots \otimes P_{N-1} \right) \mid| \psi }, \end{align} where $P_i$ is the $i$th element of `bases`, and where $N = \texttt{Length}(\texttt{bases})$. That is, measurement returns a `Result` $d$ such that the eigenvalue of the observed measurement effect is $(-1)^d$.
ms.openlocfilehash: bf0a606b1bfc8c4762245422450ec26907ec1946
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98818773"
---
# <a name="measure-operation"></a>Операция измерения

Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Выполняет совместное измерение одного или нескольких Кубитс в указанных базовых базах Паули.

Результат получается в результате распределения: \бегин{алигн} \Пр (\Тексттт{зеро} | \кет{\пси}) = \frac12 \бракет{\пси \мид | \лефт (\болдоне + P_0 \отимес P_1 \otimes \cdots \otimes P_ {N-1} \right) \mid | \psi}, \end{align}, где $P _i $ — это $i $ TH `bases` , и where $N = \texttt{Length} (\texttt{bases}) $.
То есть измерение возвращает `Result` $d $ таким, что еиженвалуе наблюдаемый результат измерения равен $ (-1) ^ d $.

```qsharp
operation Measure (bases : Pauli[], qubits : Qubit[]) : Result
```


## <a name="input"></a>Входные данные

### <a name="bases--pauli"></a>базовые базы: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]

Массив значений Single-кубит Паули, указывающих факторы продукта тензорные для каждого кубит.


### <a name="qubits--qubit"></a>Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистрация Кубитс для измерения.



## <a name="output--__invalidresult__"></a>Выходные данные __: <Result> Недопустимый__

`Zero` Если обнаружено значение $ + $1 еиженвалуе, а `One` также значение $-$1 еиженвалуе.

## <a name="remarks"></a>Remarks

Если базовый массив и массив кубит имеют разную длину, операция завершится ошибкой.