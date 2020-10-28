---
uid: Microsoft.Quantum.Canon.ApplyLowDepthAnd
title: Операция Апплиловдепсанд
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyLowDepthAnd
qsharp.summary: Inverts a given target qubit if and only if both control qubits are in the 1 state, with T-depth 1, using measurement to perform the adjoint operation.
ms.openlocfilehash: 092a350e42d8d90942de13530fefd761b5187e1d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717987"
---
# <a name="applylowdepthand-operation"></a><span data-ttu-id="5493b-102">Операция Апплиловдепсанд</span><span class="sxs-lookup"><span data-stu-id="5493b-102">ApplyLowDepthAnd operation</span></span>

<span data-ttu-id="5493b-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5493b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5493b-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5493b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5493b-105">Инвертирует заданный целевой объект кубит только в том случае, если оба элемента управления Кубитс находятся в состоянии 1 с T-Depth 1, с помощью измерения для выполнения примыкающей операции.</span><span class="sxs-lookup"><span data-stu-id="5493b-105">Inverts a given target qubit if and only if both control qubits are in the 1 state, with T-depth 1, using measurement to perform the adjoint operation.</span></span>

```qsharp
operation ApplyLowDepthAnd (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="5493b-106">Описание</span><span class="sxs-lookup"><span data-stu-id="5493b-106">Description</span></span>

<span data-ttu-id="5493b-107">Инвертирует `target` , если оба элемента управления равны 1, но предполагает, что `target` находится в состоянии 0.</span><span class="sxs-lookup"><span data-stu-id="5493b-107">Inverts `target` if and only if both controls are 1, but assumes that `target` is in state 0.</span></span>  <span data-ttu-id="5493b-108">Операция имеет T-Count 4, T-Depth 1 и требует одного вспомогательного кубит и, следовательно, может быть предпочтительнее операции ККНОТ, если `target` известно как 0.</span><span class="sxs-lookup"><span data-stu-id="5493b-108">The operation has T-count 4, T-depth 1 and requires one helper qubit, and may therefore be preferable to a CCNOT operation, if `target` is known to be 0.</span></span>  <span data-ttu-id="5493b-109">Смежная часть этой операции основана на измерении и не требует T-шлюзов и не имеет вспомогательного кубит.</span><span class="sxs-lookup"><span data-stu-id="5493b-109">The adjoint of this operation is measurement based and requires no T gates, and no helper qubit.</span></span>

## <a name="input"></a><span data-ttu-id="5493b-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5493b-110">Input</span></span>

### <a name="control1--qubit"></a><span data-ttu-id="5493b-111">Control1: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="5493b-111">control1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="5493b-112">Первый элемент управления кубит</span><span class="sxs-lookup"><span data-stu-id="5493b-112">First control qubit</span></span>


### <a name="control2--qubit"></a><span data-ttu-id="5493b-113">control2: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="5493b-113">control2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="5493b-114">Второй элемент управления кубит</span><span class="sxs-lookup"><span data-stu-id="5493b-114">Second control qubit</span></span>


### <a name="target--qubit"></a><span data-ttu-id="5493b-115">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="5493b-115">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="5493b-116">Целевой вспомогательный кубит; должно находиться в состоянии 0</span><span class="sxs-lookup"><span data-stu-id="5493b-116">Target auxiliary qubit; must be in state 0</span></span>



## <a name="output--unit"></a><span data-ttu-id="5493b-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5493b-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="5493b-118">Ссылки</span><span class="sxs-lookup"><span data-stu-id="5493b-118">References</span></span>

- <span data-ttu-id="5493b-119">Коди Jones: "романские конструкции для отказоустойчивого Тоффоли шлюза", инвентаризационная. Rev. A 87, 022328, 2013 [арксив: 1212.5069](https://arxiv.org/abs/1212.5069) ДОИ: 10.1103/фисрева. 87.022328</span><span class="sxs-lookup"><span data-stu-id="5493b-119">Cody Jones: "Novel constructions for the fault-tolerant Toffoli gate", Phys. Rev. A 87, 022328, 2013 [arXiv:1212.5069](https://arxiv.org/abs/1212.5069) doi:10.1103/PhysRevA.87.022328</span></span>
- <span data-ttu-id="5493b-120">Питер Селинжер: "тактовые цепи T-Depth 1", инвентаризационная. Rev. A 87, 042302, 2013 [арксив: 1210.0974](https://arxiv.org/abs/1210.0974) ДОИ: 10.1103/фисрева. 87.042302</span><span class="sxs-lookup"><span data-stu-id="5493b-120">Peter Selinger: "Quantum circuits of T-depth one", Phys. Rev. A 87, 042302, 2013 [arXiv:1210.0974](https://arxiv.org/abs/1210.0974) doi:10.1103/PhysRevA.87.042302</span></span>