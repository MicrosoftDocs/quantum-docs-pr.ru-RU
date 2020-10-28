---
uid: Microsoft.Quantum.Intrinsic.M
title: Операция M
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: M
qsharp.summary: >-
  Performs a measurement of a single qubit in the Pauli $Z$ basis.

  The output result is given by the distribution \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \braket{\psi | 0} \braket{0 | \psi}. \end{align}
ms.openlocfilehash: 8d4b120385bfc7086a7cb0e3f77034c760d78d92
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731393"
---
# <a name="m-operation"></a>Операция M

Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)

Пакеты [](https://nuget.org/packages/)


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