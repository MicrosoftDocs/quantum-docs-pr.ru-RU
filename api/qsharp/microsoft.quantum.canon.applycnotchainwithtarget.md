---
uid: Microsoft.Quantum.Canon.ApplyCNOTChainWithTarget
title: Операция Аппликнотчаинвистаржет
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCNOTChainWithTarget
qsharp.summary: Computes the parity of an array of qubits into a target qubit.
ms.openlocfilehash: 8ec85ce5805b3bbd1e1f7c739f27de3a861bc79e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219113"
---
# <a name="applycnotchainwithtarget-operation"></a><span data-ttu-id="31a6c-102">Операция Аппликнотчаинвистаржет</span><span class="sxs-lookup"><span data-stu-id="31a6c-102">ApplyCNOTChainWithTarget operation</span></span>

<span data-ttu-id="31a6c-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="31a6c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="31a6c-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="31a6c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="31a6c-105">Выполняет подсчет четности массива Кубитс в целевом кубит.</span><span class="sxs-lookup"><span data-stu-id="31a6c-105">Computes the parity of an array of qubits into a target qubit.</span></span>

```qsharp
operation ApplyCNOTChainWithTarget (qubits : Qubit[], targetQubit : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="31a6c-106">Описание</span><span class="sxs-lookup"><span data-stu-id="31a6c-106">Description</span></span>

<span data-ttu-id="31a6c-107">Если изначально массив находится в состоянии $ \кет{q_0} \кет{q_1} \кдотс \кет{q_ {\текст{таржет}}} $, конечное состояние присваивается с помощью $ \кет{q_0} \кет{q_1 \оплус q_0} \кдотс \кет{q_ {n-1} \оплус \кдотс \oplus q_0 \oplus q_ {\Text{Target}}} $.</span><span class="sxs-lookup"><span data-stu-id="31a6c-107">If the array is initially in the state $\ket{q_0} \ket{q_1} \cdots \ket{q_{\text{target}}}$, the final state is given by $\ket{q_0} \ket{q_1 \oplus q_0} \cdots \ket{q_{n - 1} \oplus \cdots \oplus q_0 \oplus q_{\text{target}}}$.</span></span>

## <a name="input"></a><span data-ttu-id="31a6c-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="31a6c-108">Input</span></span>

### <a name="qubits--qubit"></a><span data-ttu-id="31a6c-109">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="31a6c-109">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="31a6c-110">Массив Кубитс, для которого вычислена четность.</span><span class="sxs-lookup"><span data-stu-id="31a6c-110">Array of qubits on which the parity is computed.</span></span>


### <a name="targetqubit--qubit"></a><span data-ttu-id="31a6c-111">Таржеткубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="31a6c-111">targetQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="31a6c-112">Окончательный кубит, в котором четностью Кубитс является Ксоред.</span><span class="sxs-lookup"><span data-stu-id="31a6c-112">Final qubit into which the parity of 'qubits' is XORed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="31a6c-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="31a6c-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="31a6c-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="31a6c-114">Remarks</span></span>

<span data-ttu-id="31a6c-115">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="31a6c-115">The following are equivalent:</span></span>

```qsharp
ApplyCNOTChainWithTarget(Most(qs), Last(qs));
```

<span data-ttu-id="31a6c-116">и</span><span class="sxs-lookup"><span data-stu-id="31a6c-116">and</span></span>

```qsharp
ApplyCNOTChain(qs);
```