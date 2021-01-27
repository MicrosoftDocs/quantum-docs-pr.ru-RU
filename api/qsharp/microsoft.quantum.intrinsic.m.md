---
uid: Microsoft.Quantum.Intrinsic.M
title: Операция M
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: M
qsharp.summary: >-
  Performs a measurement of a single qubit in the Pauli $Z$ basis.

  The output result is given by the distribution \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \braket{\psi | 0} \braket{0 | \psi}. \end{align}
ms.openlocfilehash: 0037d7f5ad060857c6ca2c863b1d24aca3e338cf
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98818873"
---
# <a name="m-operation"></a>Операция M

Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Выполняет измерение отдельного кубита в Паули $Z $.

Результат вывода задается параметром Distribution \бегин{алигн} \Пр (\Тексттт{зеро} | \кет{\пси}) = \бракет{\пси | 0} \braket{0 | \пси}.
\енд{алигн}

```qsharp
operation M (qubit : Qubit) : Result
```


## <a name="input"></a>Входные данные

### <a name="qubit--qubit"></a>Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Кубит.



## <a name="output--__invalidresult__"></a>Выходные данные __: <Result> Недопустимый__

`Zero` Если обнаружено значение $ + $1 еиженвалуе, а `One` также значение $-$1 еиженвалуе.

## <a name="remarks"></a>Remarks

Эквивалентно:

```qsharp
Measure([PauliZ], [qubit]);
```