---
uid: Microsoft.Quantum.Characterization.EstimateImagOverlapBetweenStates
title: Операция Естиматеимаговерлапбетвинстатес
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateImagOverlapBetweenStates
qsharp.summary: Given two operations which each prepare copies of a state, estimates the imaginary part of the overlap between the states prepared by each operation.
ms.openlocfilehash: b192abc4ba37d126bf46f94c66cb87fe3bbec4c8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216206"
---
# <a name="estimateimagoverlapbetweenstates-operation"></a><span data-ttu-id="611fa-102">Операция Естиматеимаговерлапбетвинстатес</span><span class="sxs-lookup"><span data-stu-id="611fa-102">EstimateImagOverlapBetweenStates operation</span></span>

<span data-ttu-id="611fa-103">Пространство имен: [Microsoft. тактов. charactering](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="611fa-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="611fa-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="611fa-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="611fa-105">При наличии двух операций, каждый из которых подготавливает копии состояния, оценивает мнимую часть перекрытия между состояниями, подготовленными каждой операцией.</span><span class="sxs-lookup"><span data-stu-id="611fa-105">Given two operations which each prepare copies of a state, estimates the imaginary part of the overlap between the states prepared by each operation.</span></span>

```qsharp
operation EstimateImagOverlapBetweenStates (commonPreparation : (Qubit[] => Unit is Adj), preparation1 : (Qubit[] => Unit is Adj + Ctl), preparation2 : (Qubit[] => Unit is Adj + Ctl), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a><span data-ttu-id="611fa-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="611fa-106">Input</span></span>

### <a name="commonpreparation--qubit--unit--is-adj"></a><span data-ttu-id="611fa-107">Коммонпрепаратион: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица измерения](xref:microsoft.quantum.lang-ref.unit) ></span><span class="sxs-lookup"><span data-stu-id="611fa-107">commonPreparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="611fa-108">Операция, которая подготавливает фиксированное состояние ввода.</span><span class="sxs-lookup"><span data-stu-id="611fa-108">An operation that prepares a fixed input state.</span></span>


### <a name="preparation1--qubit--unit--is-adj--ctl"></a><span data-ttu-id="611fa-109">preparation1: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="611fa-109">preparation1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="611fa-110">Первая из двух операций подготовки состояния для сравнения.</span><span class="sxs-lookup"><span data-stu-id="611fa-110">The first of the two state preparation operations to be compared.</span></span>


### <a name="preparation2--qubit--unit--is-adj--ctl"></a><span data-ttu-id="611fa-111">preparation2: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="611fa-111">preparation2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="611fa-112">Вторая из двух операций подготовки состояния для сравнения.</span><span class="sxs-lookup"><span data-stu-id="611fa-112">The second of the two state preparation operations to be compared.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="611fa-113">Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="611fa-113">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="611fa-114">Число Кубитс, для которых `commonPreparation` действует, `preparation1` и `preparation2` .</span><span class="sxs-lookup"><span data-stu-id="611fa-114">The number of qubits on which `commonPreparation`, `preparation1`, and `preparation2` all act.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="611fa-115">Нмеасурементс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="611fa-115">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="611fa-116">Количество измерений, используемых для оценки перекрытия.</span><span class="sxs-lookup"><span data-stu-id="611fa-116">The number of measurements to use in estimating the overlap.</span></span>



## <a name="output--double"></a><span data-ttu-id="611fa-117">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="611fa-117">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="611fa-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="611fa-118">Remarks</span></span>

<span data-ttu-id="611fa-119">Эта операция использует тест Хадамард для поиска мнимой части $ $ \бегин{алигн} \бракет{\пси | V ^ {\дагжер} U | \пси} \енд{алигн} $ $, где $ \кет{\пси} $ — это состояние, подготовленное `commonPreparation` , $U $ является единым представлением действия `preparation1` , а $V $ соответствует `preparation2` .</span><span class="sxs-lookup"><span data-stu-id="611fa-119">This operation uses the Hadamard test to find the imaginary part of $$ \begin{align} \braket{\psi | V^{\dagger} U | \psi} \end{align} $$ where $\ket{\psi}$ is the state prepared by `commonPreparation`, $U$ is the unitary representation of the action of `preparation1`, and where $V$ corresponds to `preparation2`.</span></span>

## <a name="references"></a><span data-ttu-id="611fa-120">Ссылки</span><span class="sxs-lookup"><span data-stu-id="611fa-120">References</span></span>

- <span data-ttu-id="611fa-121">Ахаронов *et al.* [Куант-pH/0511096](https://arxiv.org/abs/quant-ph/0511096).</span><span class="sxs-lookup"><span data-stu-id="611fa-121">Aharonov *et al.* [quant-ph/0511096](https://arxiv.org/abs/quant-ph/0511096).</span></span>

## <a name="see-also"></a><span data-ttu-id="611fa-122">См. также:</span><span class="sxs-lookup"><span data-stu-id="611fa-122">See Also</span></span>

- [<span data-ttu-id="611fa-123">Microsoft. тактов. characters. Естиматереаловерлапбетвинстатес</span><span class="sxs-lookup"><span data-stu-id="611fa-123">Microsoft.Quantum.Characterization.EstimateRealOverlapBetweenStates</span></span>](xref:Microsoft.Quantum.Characterization.EstimateRealOverlapBetweenStates)
- [<span data-ttu-id="611fa-124">Microsoft. тактов. characters. Естиматеоверлапбетвинстатес</span><span class="sxs-lookup"><span data-stu-id="611fa-124">Microsoft.Quantum.Characterization.EstimateOverlapBetweenStates</span></span>](xref:Microsoft.Quantum.Characterization.EstimateOverlapBetweenStates)