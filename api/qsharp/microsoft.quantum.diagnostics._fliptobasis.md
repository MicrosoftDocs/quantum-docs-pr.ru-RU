---
uid: Microsoft.Quantum.Diagnostics._flipToBasis
title: _flipToBasis операция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _flipToBasis
qsharp.summary: >-
  Applies unitaries that map $\ket{0}\otimes\cdots\ket{0}$ to $\ket{\psi_0} \otimes \ket{\psi_{n - 1}}$, where $\ket{\psi_k}$ depends on `basis[k]`.

  The correspondence between value of `basis[k]` and $\ket{\psi_k}$ is the following:

  - `basis[k]=0` $\rightarrow \ket{0}$. - `basis[k]=1` $\rightarrow \ket{1}$. - `basis[k]=2` $\rightarrow \ket{+}$. - `basis[k]=3` $\rightarrow \ket{i}$ ( +1 eigenstate of Pauli Y ).
ms.openlocfilehash: e074ed2ae259f6aef49a8d327ce518a9e2caebfa
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713144"
---
# <a name="_fliptobasis-operation"></a>_flipToBasis операция

Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Пакеты [](https://nuget.org/packages/)


Применяет унитариес, который сопоставляет $ \кет {0} \отимес\кдотс\кет {0} $ с $ \кет{\ psi_0} \отимес \кет{\ psi_ {n-1}} $, где $ \кет{\ psi_k} $ зависит от `basis[k]` .

Соответствие значения `basis[k]` и $ \кет{\ psi_k} $ является следующим:

- `basis[k]=0` $ \ригхтарров \кет {0} $.
- `basis[k]=1` $ \ригхтарров \кет {1} $.
- `basis[k]=2` $ \ригхтарров \кет{+} $.
- `basis[k]=3` $ \ригхтарров \кет{и} $ (+ 1 еиженстате Паули Y).

```qsharp
operation _flipToBasis (basis : Int[], qubits : Qubit[]) : Unit
```


## <a name="input"></a>Входные данные

### <a name="basis--int"></a>Базис: [int](xref:microsoft.quantum.lang-ref.int)[]

Массив идентификаторов однокубитного состояния (0 <= ID <= 3), по одному для каждого элемента Кубитс.


### <a name="qubits--qubit"></a>Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Кубит.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

