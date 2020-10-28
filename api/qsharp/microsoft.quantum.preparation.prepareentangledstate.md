---
uid: Microsoft.Quantum.Preparation.PrepareEntangledState
title: Операция Препаринтангледстате
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareEntangledState
qsharp.summary: >-
  Pairwise entangles two qubit registers.

  That is, given two registers, prepares the maximally entangled state $\frac{1}{\sqrt{2}} \left(\ket{00} + \ket{11} \right)$ between each pair of qubits on the respective registers, assuming that each register starts in the $\ket{0\cdots 0}$ state.
ms.openlocfilehash: 299d586f7581acdecf22da2f6bbfbb8d45f372f3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732176"
---
# <a name="prepareentangledstate-operation"></a>Операция Препаринтангледстате

Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)

Пакеты [](https://nuget.org/packages/)


Парные ентанглес два регистра кубит.

Это значит, что при наличии двух регистров подготавливается максимальное запутанными State $ \фрак {1} {\скрт {2} } \лефт (\кет {00} + \кет {11} \ригхт) $ между каждой парой Кубитс в соответствующих регистрах, предполагая, что каждый регистр начинается в состоянии $ \ket{0\cdots 0} $.

```qsharp
operation PrepareEntangledState (left : Qubit[], right : Qubit[]) : Unit
```


## <a name="input"></a>Входные данные

### <a name="left--qubit"></a>Left: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Массив кубит в состоянии $ \ket{0\cdots 0} $


### <a name="right--qubit"></a>Right: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Массив кубит в состоянии $ \ket{0\cdots 0} $



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

