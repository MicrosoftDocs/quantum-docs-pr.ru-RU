---
uid: Microsoft.Quantum.Diagnostics._flipToBasis
title: _flipToBasis операция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _flipToBasis
qsharp.summary: >-
  Applies unitaries that map $\ket{0}\otimes\cdots\ket{0}$ to $\ket{\psi_0} \otimes \ket{\psi_{n - 1}}$, where $\ket{\psi_k}$ depends on `basis[k]`.

  The correspondence between value of `basis[k]` and $\ket{\psi_k}$ is the following:

  - `basis[k]=0` $\rightarrow \ket{0}$. - `basis[k]=1` $\rightarrow \ket{1}$. - `basis[k]=2` $\rightarrow \ket{+}$. - `basis[k]=3` $\rightarrow \ket{i}$ ( +1 eigenstate of Pauli Y ).
ms.openlocfilehash: 1581a1267902ceee81d6f01348f4ee718e49ee47
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223992"
---
# <a name="_fliptobasis-operation"></a>_flipToBasis операция

Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Применяет унитариес, который сопоставляет $ \кет {0} \отимес\кдотс\кет {0} $ с $ \кет{\ psi_0} \отимес \кет{\ psi_ {n-1}} $, где $ \кет{\ psi_k} $ зависит от `basis[k]` .

Соответствие значения `basis[k]` и $ \кет{\ psi_k} $ является следующим:

- `basis[k]=0` $ \ригхтарров \кет {0} $.
- `basis[k]=1` $ \ригхтарров \кет {1} $.
- `basis[k]=2` $ \ригхтарров \кет{+} $.
- `basis[k]=3` $ \ригхтарров \кет{и} $ (+ 1 еиженстате Паули Y).

```qsharp
operation _flipToBasis (basis : Int[], qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="basis--int"></a>Базис: [int](xref:microsoft.quantum.lang-ref.int)[]

Массив идентификаторов однокубитного состояния (0 <= ID <= 3), по одному для каждого элемента Кубитс.


### <a name="qubits--qubit"></a>Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Кубит.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

