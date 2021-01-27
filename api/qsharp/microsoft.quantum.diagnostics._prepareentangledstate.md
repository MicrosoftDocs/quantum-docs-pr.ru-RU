---
uid: Microsoft.Quantum.Diagnostics._prepareEntangledState
title: _prepareEntangledState операция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _prepareEntangledState
qsharp.summary: >-
  Given two registers, prepares the maximally entangled state between each pair of qubits on the respective registers. All qubits must start in the |0⟩ state.

  The result is that corresponding pairs of qubits from each register are in the $\bra{\beta_{00}}\ket{\beta_{00}}$.
ms.openlocfilehash: 5a74978a536a92dafae0b532805bd8e8ae1c888e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830970"
---
# <a name="_prepareentangledstate-operation"></a>_prepareEntangledState операция

Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


При наличии двух регистров подготавливает запутанными состояние между каждой парой Кубитс в соответствующих регистрах.
Все Кубитс должны начинаться в состоянии ⟩ | 0.

Результат заключается в том, что соответствующие пары Кубитс из каждой ККМ находятся в \кет{\ beta_ \бра{\ {00} {00} } $ beta_} $.

```qsharp
operation _prepareEntangledState (left : Qubit[], right : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="left--qubit"></a>Left: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Массив кубит в состоянии $ \ket{0\cdots 0} $


### <a name="right--qubit"></a>Right: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Массив кубит в состоянии $ \ket{0\cdots 0} $



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

