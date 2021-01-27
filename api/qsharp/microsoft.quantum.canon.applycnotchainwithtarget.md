---
uid: Microsoft.Quantum.Canon.ApplyCNOTChainWithTarget
title: Операция Аппликнотчаинвистаржет
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCNOTChainWithTarget
qsharp.summary: Computes the parity of an array of qubits into a target qubit.
ms.openlocfilehash: ba1a4e99c411a4718b5a09fdcd57a7239eb4dbd6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845119"
---
# <a name="applycnotchainwithtarget-operation"></a><span data-ttu-id="efcbd-102">Операция Аппликнотчаинвистаржет</span><span class="sxs-lookup"><span data-stu-id="efcbd-102">ApplyCNOTChainWithTarget operation</span></span>

<span data-ttu-id="efcbd-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="efcbd-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="efcbd-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="efcbd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="efcbd-105">Выполняет подсчет четности массива Кубитс в целевом кубит.</span><span class="sxs-lookup"><span data-stu-id="efcbd-105">Computes the parity of an array of qubits into a target qubit.</span></span>

```qsharp
operation ApplyCNOTChainWithTarget (qubits : Qubit[], targetQubit : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="efcbd-106">Описание</span><span class="sxs-lookup"><span data-stu-id="efcbd-106">Description</span></span>

<span data-ttu-id="efcbd-107">Если изначально массив находится в состоянии $ \кет{q_0} \кет{q_1} \кдотс \кет{q_ {\текст{таржет}}} $, конечное состояние присваивается с помощью $ \кет{q_0} \кет{q_1 \оплус q_0} \кдотс \кет{q_ {n-1} \оплус \кдотс \oplus q_0 \oplus q_ {\Text{Target}}} $.</span><span class="sxs-lookup"><span data-stu-id="efcbd-107">If the array is initially in the state $\ket{q_0} \ket{q_1} \cdots \ket{q_{\text{target}}}$, the final state is given by $\ket{q_0} \ket{q_1 \oplus q_0} \cdots \ket{q_{n - 1} \oplus \cdots \oplus q_0 \oplus q_{\text{target}}}$.</span></span>

## <a name="input"></a><span data-ttu-id="efcbd-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="efcbd-108">Input</span></span>

### <a name="qubits--qubit"></a><span data-ttu-id="efcbd-109">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="efcbd-109">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="efcbd-110">Массив Кубитс, для которого вычислена четность.</span><span class="sxs-lookup"><span data-stu-id="efcbd-110">Array of qubits on which the parity is computed.</span></span>


### <a name="targetqubit--qubit"></a><span data-ttu-id="efcbd-111">Таржеткубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="efcbd-111">targetQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="efcbd-112">Окончательный кубит, в котором четностью Кубитс является Ксоред.</span><span class="sxs-lookup"><span data-stu-id="efcbd-112">Final qubit into which the parity of 'qubits' is XORed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="efcbd-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="efcbd-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="efcbd-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="efcbd-114">Remarks</span></span>

<span data-ttu-id="efcbd-115">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="efcbd-115">The following are equivalent:</span></span>

```qsharp
ApplyCNOTChainWithTarget(Most(qs), Last(qs));
```

<span data-ttu-id="efcbd-116">и</span><span class="sxs-lookup"><span data-stu-id="efcbd-116">and</span></span>

```qsharp
ApplyCNOTChain(qs);
```