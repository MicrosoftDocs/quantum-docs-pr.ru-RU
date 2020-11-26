---
uid: Microsoft.Quantum.Preparation.PrepareEntangledState
title: Операция Препаринтангледстате
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareEntangledState
qsharp.summary: >-
  Pairwise entangles two qubit registers.

  That is, given two registers, prepares the maximally entangled state $\frac{1}{\sqrt{2}} \left(\ket{00} + \ket{11} \right)$ between each pair of qubits on the respective registers, assuming that each register starts in the $\ket{0\cdots 0}$ state.
ms.openlocfilehash: 5f6e3ea1e7638d3bc446f21ace2968cf8284353a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210477"
---
# <a name="prepareentangledstate-operation"></a>Операция Препаринтангледстате

Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Парные ентанглес два регистра кубит.

Это значит, что при наличии двух регистров подготавливается максимальное запутанными State $ \фрак {1} {\скрт {2} } \лефт (\кет {00} + \кет {11} \ригхт) $ между каждой парой Кубитс в соответствующих регистрах, предполагая, что каждый регистр начинается в состоянии $ \ket{0\cdots 0} $.

```qsharp
operation PrepareEntangledState (left : Qubit[], right : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="left--qubit"></a>Left: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Массив кубит в состоянии $ \ket{0\cdots 0} $


### <a name="right--qubit"></a>Right: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Массив кубит в состоянии $ \ket{0\cdots 0} $



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

