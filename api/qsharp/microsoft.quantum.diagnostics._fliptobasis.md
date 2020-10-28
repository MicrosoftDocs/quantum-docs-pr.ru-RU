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
# <a name="_fliptobasis-operation"></a><span data-ttu-id="64495-102">_flipToBasis операция</span><span class="sxs-lookup"><span data-stu-id="64495-102">_flipToBasis operation</span></span>

<span data-ttu-id="64495-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="64495-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="64495-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="64495-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="64495-105">Применяет унитариес, который сопоставляет $ \кет {0} \отимес\кдотс\кет {0} $ с $ \кет{\ psi_0} \отимес \кет{\ psi_ {n-1}} $, где $ \кет{\ psi_k} $ зависит от `basis[k]` .</span><span class="sxs-lookup"><span data-stu-id="64495-105">Applies unitaries that map $\ket{0}\otimes\cdots\ket{0}$ to $\ket{\psi_0} \otimes \ket{\psi_{n - 1}}$, where $\ket{\psi_k}$ depends on `basis[k]`.</span></span>

<span data-ttu-id="64495-106">Соответствие значения `basis[k]` и $ \кет{\ psi_k} $ является следующим:</span><span class="sxs-lookup"><span data-stu-id="64495-106">The correspondence between value of `basis[k]` and $\ket{\psi_k}$ is the following:</span></span>

- <span data-ttu-id="64495-107">`basis[k]=0` $ \ригхтарров \кет {0} $.</span><span class="sxs-lookup"><span data-stu-id="64495-107">`basis[k]=0` $\rightarrow \ket{0}$.</span></span>
- <span data-ttu-id="64495-108">`basis[k]=1` $ \ригхтарров \кет {1} $.</span><span class="sxs-lookup"><span data-stu-id="64495-108">`basis[k]=1` $\rightarrow \ket{1}$.</span></span>
- <span data-ttu-id="64495-109">`basis[k]=2` $ \ригхтарров \кет{+} $.</span><span class="sxs-lookup"><span data-stu-id="64495-109">`basis[k]=2` $\rightarrow \ket{+}$.</span></span>
- <span data-ttu-id="64495-110">`basis[k]=3` $ \ригхтарров \кет{и} $ (+ 1 еиженстате Паули Y).</span><span class="sxs-lookup"><span data-stu-id="64495-110">`basis[k]=3` $\rightarrow \ket{i}$ ( +1 eigenstate of Pauli Y ).</span></span>

```qsharp
operation _flipToBasis (basis : Int[], qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="64495-111">Входные данные</span><span class="sxs-lookup"><span data-stu-id="64495-111">Input</span></span>

### <a name="basis--int"></a><span data-ttu-id="64495-112">Базис: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="64495-112">basis : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="64495-113">Массив идентификаторов однокубитного состояния (0 <= ID <= 3), по одному для каждого элемента Кубитс.</span><span class="sxs-lookup"><span data-stu-id="64495-113">Array of single-qubit basis state IDs (0 <= id <= 3), one for each element of qubits.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="64495-114">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="64495-114">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="64495-115">Кубит.</span><span class="sxs-lookup"><span data-stu-id="64495-115">Qubit to be operated on.</span></span>



## <a name="output--unit"></a><span data-ttu-id="64495-116">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="64495-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

