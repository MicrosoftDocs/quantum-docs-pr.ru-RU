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
# <a name="_fliptobasis-operation"></a><span data-ttu-id="19b25-102">_flipToBasis операция</span><span class="sxs-lookup"><span data-stu-id="19b25-102">_flipToBasis operation</span></span>

<span data-ttu-id="19b25-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="19b25-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="19b25-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="19b25-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="19b25-105">Применяет унитариес, который сопоставляет $ \кет {0} \отимес\кдотс\кет {0} $ с $ \кет{\ psi_0} \отимес \кет{\ psi_ {n-1}} $, где $ \кет{\ psi_k} $ зависит от `basis[k]` .</span><span class="sxs-lookup"><span data-stu-id="19b25-105">Applies unitaries that map $\ket{0}\otimes\cdots\ket{0}$ to $\ket{\psi_0} \otimes \ket{\psi_{n - 1}}$, where $\ket{\psi_k}$ depends on `basis[k]`.</span></span>

<span data-ttu-id="19b25-106">Соответствие значения `basis[k]` и $ \кет{\ psi_k} $ является следующим:</span><span class="sxs-lookup"><span data-stu-id="19b25-106">The correspondence between value of `basis[k]` and $\ket{\psi_k}$ is the following:</span></span>

- <span data-ttu-id="19b25-107">`basis[k]=0` $ \ригхтарров \кет {0} $.</span><span class="sxs-lookup"><span data-stu-id="19b25-107">`basis[k]=0` $\rightarrow \ket{0}$.</span></span>
- <span data-ttu-id="19b25-108">`basis[k]=1` $ \ригхтарров \кет {1} $.</span><span class="sxs-lookup"><span data-stu-id="19b25-108">`basis[k]=1` $\rightarrow \ket{1}$.</span></span>
- <span data-ttu-id="19b25-109">`basis[k]=2` $ \ригхтарров \кет{+} $.</span><span class="sxs-lookup"><span data-stu-id="19b25-109">`basis[k]=2` $\rightarrow \ket{+}$.</span></span>
- <span data-ttu-id="19b25-110">`basis[k]=3` $ \ригхтарров \кет{и} $ (+ 1 еиженстате Паули Y).</span><span class="sxs-lookup"><span data-stu-id="19b25-110">`basis[k]=3` $\rightarrow \ket{i}$ ( +1 eigenstate of Pauli Y ).</span></span>

```qsharp
operation _flipToBasis (basis : Int[], qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="19b25-111">Входные данные</span><span class="sxs-lookup"><span data-stu-id="19b25-111">Input</span></span>

### <a name="basis--int"></a><span data-ttu-id="19b25-112">Базис: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="19b25-112">basis : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="19b25-113">Массив идентификаторов однокубитного состояния (0 <= ID <= 3), по одному для каждого элемента Кубитс.</span><span class="sxs-lookup"><span data-stu-id="19b25-113">Array of single-qubit basis state IDs (0 <= id <= 3), one for each element of qubits.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="19b25-114">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="19b25-114">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="19b25-115">Кубит.</span><span class="sxs-lookup"><span data-stu-id="19b25-115">Qubit to be operated on.</span></span>



## <a name="output--unit"></a><span data-ttu-id="19b25-116">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="19b25-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

