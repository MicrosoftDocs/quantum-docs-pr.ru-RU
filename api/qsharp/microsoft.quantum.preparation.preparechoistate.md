---
uid: Microsoft.Quantum.Preparation.PrepareChoiState
title: Операция Препаречоистате
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareChoiState
qsharp.summary: Prepares the Choi–Jamiołkowski state for a given operation onto given reference and target registers.
ms.openlocfilehash: ced71c4278f42f577760acd54ae53e7f5e6dae4a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210579"
---
# <a name="preparechoistate-operation"></a><span data-ttu-id="8d855-102">Операция Препаречоистате</span><span class="sxs-lookup"><span data-stu-id="8d855-102">PrepareChoiState operation</span></span>

<span data-ttu-id="8d855-103">Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="8d855-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="8d855-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8d855-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8d855-105">Подготавливает состояние Чои – Жамиоłковски для данной операции к указанным ссылочным и целевым регистрам.</span><span class="sxs-lookup"><span data-stu-id="8d855-105">Prepares the Choi–Jamiołkowski state for a given operation onto given reference and target registers.</span></span>

```qsharp
operation PrepareChoiState (op : (Qubit[] => Unit), reference : Qubit[], target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="8d855-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="8d855-106">Input</span></span>

### <a name="op--qubit--unit"></a><span data-ttu-id="8d855-107">Op: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="8d855-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="8d855-108">Необходимо подготовить операцию $ \Ламбда $, Чои — Жамиоłковски State $J (\Ламбда)/2 ^ N $, где $N $ — это количество Кубитс, на которое `op` действует.</span><span class="sxs-lookup"><span data-stu-id="8d855-108">Operation $\Lambda$ whose Choi–Jamiołkowski state $J(\Lambda) / 2^N$ is to be prepared, where $N$ is the number of qubits on which `op` acts.</span></span>


### <a name="reference--qubit"></a><span data-ttu-id="8d855-109">Ссылка: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="8d855-109">reference : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="8d855-110">Регистр Кубитс, начиная с $ \ket{00\cdots 0} $, для использования в качестве ссылки на действие `op` .</span><span class="sxs-lookup"><span data-stu-id="8d855-110">A register of qubits starting in the $\ket{00\cdots 0}$ state to be used as a reference for the action of `op`.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="8d855-111">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="8d855-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="8d855-112">Регистр Кубитс изначально находится в состоянии $ \ket{00\cdots 0} $, `op` к которому применяется.</span><span class="sxs-lookup"><span data-stu-id="8d855-112">A register of qubits initially in the $\ket{00\cdots 0}$ state on which `op` is to be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8d855-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8d855-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="8d855-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8d855-114">Remarks</span></span>

<span data-ttu-id="8d855-115">Параметр Чои – Жамиłковски State $J (\Ламбда) $ для тактового процесса определяется как $ $ \бегин{алигн} J (\Ламбда) \масрел{: =} (\болдоне \отимес \Ламбда) (| \болдоне\рангле \! \rangle\langle \! \langle\boldone |), \end{align} $ $ WHERE $ | Кс\рангле \! \рангле $ — это *вектор* матрицы, $X $ в соглашении о стеке столбцов.</span><span class="sxs-lookup"><span data-stu-id="8d855-115">The Choi–Jamiłkowski state $J(\Lambda)$ of a quantum process is defined as $$ \begin{align} J(\Lambda) \mathrel{:=} (\boldone \otimes \Lambda) (|\boldone\rangle\!\rangle\langle\!\langle\boldone|), \end{align} $$ where $|X\rangle\!\rangle$ is the *vectorization* of a matrix $X$ in the column-stacking convention.</span></span> <span data-ttu-id="8d855-116">Изучение классического описания этого состояния предоставляет полную информацию о действии $ \Ламбда $, действующей на произвольные входные состояния, и формирует основу *тактового процесса томографи*.</span><span class="sxs-lookup"><span data-stu-id="8d855-116">Learning a classical description of this state provides full information about the effect of $\Lambda$ acting on arbitrary input states, and forms the foundation of *quantum process tomography*.</span></span>

## <a name="see-also"></a><span data-ttu-id="8d855-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="8d855-117">See Also</span></span>

- [<span data-ttu-id="8d855-118">Microsoft. тактов. подготовка. Препаречоистатеа</span><span class="sxs-lookup"><span data-stu-id="8d855-118">Microsoft.Quantum.Preparation.PrepareChoiStateA</span></span>](xref:Microsoft.Quantum.Preparation.PrepareChoiStateA)
- [<span data-ttu-id="8d855-119">Microsoft. тактов. подготовка. Препаречоистатек</span><span class="sxs-lookup"><span data-stu-id="8d855-119">Microsoft.Quantum.Preparation.PrepareChoiStateC</span></span>](xref:Microsoft.Quantum.Preparation.PrepareChoiStateC)
- [<span data-ttu-id="8d855-120">Microsoft. тактов. подготовка. Препаречоистатека</span><span class="sxs-lookup"><span data-stu-id="8d855-120">Microsoft.Quantum.Preparation.PrepareChoiStateCA</span></span>](xref:Microsoft.Quantum.Preparation.PrepareChoiStateCA)