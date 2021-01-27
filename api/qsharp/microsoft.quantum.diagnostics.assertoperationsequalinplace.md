---
uid: Microsoft.Quantum.Diagnostics.AssertOperationsEqualInPlace
title: Операция Ассертоператионсекуалинплаце
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertOperationsEqualInPlace
qsharp.summary: >-
  Given two operations, asserts that they act identically for all input states.

  This assertion is implemented by checking the action of the operations on all states of the form $V_0 \otimes ... \otimes V_{n-1}$, where $V_k$ is one of the states $\ket{0}$, $\ket{1}$, $\ket{+}$ and $\ket{i}$ (+1 eigenstate of Pauli Y operator).

  This assertion uses $n$ qubits and requires multiple calls of the operations being compared.
ms.openlocfilehash: 7c330ebdc156e60713a734d39a3600ee1326563c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853484"
---
# <a name="assertoperationsequalinplace-operation"></a>Операция Ассертоператионсекуалинплаце

Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Учитывая две операции, утверждает, что они действуют одинаково для всех входных состояний.

Это утверждение реализуется путем проверки действия операций во всех состояниях формы $V _0 \отимес... \отимес V_ {n-1} $, где $V _k $ является одним из состояний $ \кет {0} $, $ \кет {1} $, $ \кет{+} $ и $ \кет{и} $ (+ 1 Еиженстате of Паули Y).

Это утверждение использует $n $ Кубитс и требует нескольких вызовов сравниваемых операций.

```qsharp
operation AssertOperationsEqualInPlace (nQubits : Int, givenU : (Qubit[] => Unit), expectedU : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a>Входные данные

### <a name="nqubits--int"></a>Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)

Число Кубитс $n $, с которыми работают операции `givenU` `expectedU` .


### <a name="givenu--qubit--unit"></a>Гивену: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit)> 

Операция с $n $ Кубитс будет проверена.


### <a name="expectedu--qubit--unit--is-adj"></a>Експектеду: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица измерения](xref:microsoft.quantum.lang-ref.unit) >

Операция ссылки на $n $ Кубитс `givenU` для сравнения с.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Ссылки

Основной частью состояний $ \кет {0} $, $ \кет {1} $, $ \кет{+} $ и $ \кет{и} $ является Chuang-Nielsen, описанный в [ *i. L. Чжуанский, M. A. Nielsen*](https://arxiv.org/abs/quant-ph/9610001).

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Diagnostics. Ассертоператионсекуалреференцед](xref:Microsoft.Quantum.Diagnostics.AssertOperationsEqualReferenced)