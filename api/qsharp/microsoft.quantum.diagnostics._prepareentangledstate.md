---
uid: Microsoft.Quantum.Diagnostics._prepareEntangledState
title: _prepareEntangledState операция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _prepareEntangledState
qsharp.summary: >-
  Given two registers, prepares the maximally entangled state between each pair of qubits on the respective registers. All qubits must start in the |0⟩ state.

  The result is that corresponding pairs of qubits from each register are in the $\bra{\beta_{00}}\ket{\beta_{00}}$.
ms.openlocfilehash: 97a55b4bb85095c7d8e8432dfcd1c6d6f7e93cdc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223941"
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

