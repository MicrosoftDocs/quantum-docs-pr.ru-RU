---
uid: Microsoft.Quantum.Canon.ApplyAnd
title: Операция нажимаем
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyAnd
qsharp.summary: Inverts a given target qubit if and only if both control qubits are in the 1 state, using measurement to perform the adjoint operation.
ms.openlocfilehash: 5a4e18cb0361708e1fc00e8d62c0a6c2415d6bed
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729744"
---
# <a name="applyand-operation"></a><span data-ttu-id="0a6e9-102">Операция нажимаем</span><span class="sxs-lookup"><span data-stu-id="0a6e9-102">ApplyAnd operation</span></span>

<span data-ttu-id="0a6e9-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="0a6e9-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="0a6e9-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0a6e9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0a6e9-105">Инвертирует заданный целевой объект кубит только в том случае, если оба элемента управления Кубитс находятся в состоянии 1, с помощью измерения для выполнения примыкающей операции.</span><span class="sxs-lookup"><span data-stu-id="0a6e9-105">Inverts a given target qubit if and only if both control qubits are in the 1 state, using measurement to perform the adjoint operation.</span></span>

```qsharp
operation ApplyAnd (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="0a6e9-106">Описание</span><span class="sxs-lookup"><span data-stu-id="0a6e9-106">Description</span></span>

<span data-ttu-id="0a6e9-107">Инвертирует `target` , если оба элемента управления равны 1, но предполагает, что `target` находится в состоянии 0.</span><span class="sxs-lookup"><span data-stu-id="0a6e9-107">Inverts `target` if and only if both controls are 1, but assumes that `target` is in state 0.</span></span>  <span data-ttu-id="0a6e9-108">Операция имеет T-Count 4, T-Depth 2 и не требует вспомогательных кубит и, следовательно, может быть предпочтительней для операции ККНОТ, если `target` известно как 0.</span><span class="sxs-lookup"><span data-stu-id="0a6e9-108">The operation has T-count 4, T-depth 2 and requires no helper qubit, and may therefore be preferable to a CCNOT operation, if `target` is known to be 0.</span></span>  <span data-ttu-id="0a6e9-109">Смежная операция основана на измерении и не требует T-шлюзов.</span><span class="sxs-lookup"><span data-stu-id="0a6e9-109">The adjoint of this operation is measurement based and requires no T gates.</span></span>

<span data-ttu-id="0a6e9-110">Для управляемого приложения этой операции не требуются вспомогательные кубит, `2^c` `Rz` шлюзы и не оптимизированы для глубины, где `c` — это число общего Кубитс управления, включая два элемента управления из `ApplyAnd` операции.</span><span class="sxs-lookup"><span data-stu-id="0a6e9-110">The controlled application of this operation requires no helper qubit, `2^c` `Rz` gates and is not optimized for depth, where `c` is the number of overall control qubits including the two controls from the `ApplyAnd` operation.</span></span>  <span data-ttu-id="0a6e9-111">Для приложения, контролируемого соседним контролем `2^c - 1` `Rz` , требуются шлюзы (с углом, равным вдвое меньше размера несмежной операции), вспомогательный кубит не оптимизирован и не оптимизируется для глубины.</span><span class="sxs-lookup"><span data-stu-id="0a6e9-111">The adjoint controlled application requires `2^c - 1` `Rz` gates (with an angle twice the size of the non-adjoint operation), no helper qubit and is not optimized for depth.</span></span>

## <a name="input"></a><span data-ttu-id="0a6e9-112">Входные данные</span><span class="sxs-lookup"><span data-stu-id="0a6e9-112">Input</span></span>

### <a name="control1--qubit"></a><span data-ttu-id="0a6e9-113">Control1: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="0a6e9-113">control1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="0a6e9-114">Первый элемент управления кубит</span><span class="sxs-lookup"><span data-stu-id="0a6e9-114">First control qubit</span></span>


### <a name="control2--qubit"></a><span data-ttu-id="0a6e9-115">control2: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="0a6e9-115">control2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="0a6e9-116">Второй элемент управления кубит</span><span class="sxs-lookup"><span data-stu-id="0a6e9-116">Second control qubit</span></span>


### <a name="target--qubit"></a><span data-ttu-id="0a6e9-117">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="0a6e9-117">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="0a6e9-118">Целевой вспомогательный кубит; должно находиться в состоянии 0</span><span class="sxs-lookup"><span data-stu-id="0a6e9-118">Target auxiliary qubit; must be in state 0</span></span>



## <a name="output--unit"></a><span data-ttu-id="0a6e9-119">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0a6e9-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="0a6e9-120">Ссылки</span><span class="sxs-lookup"><span data-stu-id="0a6e9-120">References</span></span>

- <span data-ttu-id="0a6e9-121">Коди Jones: "романские конструкции для отказоустойчивого Тоффоли шлюза", инвентаризационная. Rev. A 87, 022328, 2013 [арксив: 1212.5069](https://arxiv.org/abs/1212.5069) ДОИ: 10.1103/фисрева. 87.022328</span><span class="sxs-lookup"><span data-stu-id="0a6e9-121">Cody Jones: "Novel constructions for the fault-tolerant Toffoli gate", Phys. Rev. A 87, 022328, 2013 [arXiv:1212.5069](https://arxiv.org/abs/1212.5069) doi:10.1103/PhysRevA.87.022328</span></span>
- <span data-ttu-id="0a6e9-122">Крейг Гиднэй: "сократить затраты на сложение тактов", такт 2, страница 74, 2018 [арксив: 1709.06648](https://arxiv.org/abs/1709.06648) ДОИ: 10.1103/фисрева. 85.044302</span><span class="sxs-lookup"><span data-stu-id="0a6e9-122">Craig Gidney: "Halving the cost of quantum addition", Quantum 2, page 74, 2018 [arXiv:1709.06648](https://arxiv.org/abs/1709.06648) doi:10.1103/PhysRevA.85.044302</span></span>
- <span data-ttu-id="0a6e9-123">Матиас Соекен: "каналы Oracle для тактов и шаблон дерева Рождества", [статья блога 19 декабря 2019](https://msoeken.github.io/blog_qac.html) (Примечание: объясняется многоуправляемая конструкция).</span><span class="sxs-lookup"><span data-stu-id="0a6e9-123">Mathias Soeken: "Quantum Oracle Circuits and the Christmas Tree Pattern", [Blog article from December 19, 2019](https://msoeken.github.io/blog_qac.html) (note: explains the multiple controlled construction)</span></span>