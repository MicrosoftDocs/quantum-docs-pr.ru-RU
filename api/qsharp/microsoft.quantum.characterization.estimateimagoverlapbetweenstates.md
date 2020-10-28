---
uid: Microsoft.Quantum.Characterization.EstimateImagOverlapBetweenStates
title: Операция Естиматеимаговерлапбетвинстатес
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateImagOverlapBetweenStates
qsharp.summary: Given two operations which each prepare copies of a state, estimates the imaginary part of the overlap between the states prepared by each operation.
ms.openlocfilehash: 8b73115c3243c594897ac4b309ec52d5e9863d26
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715047"
---
# <a name="estimateimagoverlapbetweenstates-operation"></a><span data-ttu-id="c6db8-102">Операция Естиматеимаговерлапбетвинстатес</span><span class="sxs-lookup"><span data-stu-id="c6db8-102">EstimateImagOverlapBetweenStates operation</span></span>

<span data-ttu-id="c6db8-103">Пространство имен: [Microsoft. тактов. charactering](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="c6db8-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="c6db8-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c6db8-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c6db8-105">При наличии двух операций, каждый из которых подготавливает копии состояния, оценивает мнимую часть перекрытия между состояниями, подготовленными каждой операцией.</span><span class="sxs-lookup"><span data-stu-id="c6db8-105">Given two operations which each prepare copies of a state, estimates the imaginary part of the overlap between the states prepared by each operation.</span></span>

```qsharp
operation EstimateImagOverlapBetweenStates (commonPreparation : (Qubit[] => Unit is Adj), preparation1 : (Qubit[] => Unit is Adj + Ctl), preparation2 : (Qubit[] => Unit is Adj + Ctl), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a><span data-ttu-id="c6db8-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c6db8-106">Input</span></span>

### <a name="commonpreparation--qubit--unit-adj"></a><span data-ttu-id="c6db8-107">Коммонпрепаратион: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] [=>ная](xref:microsoft.quantum.lang-ref.unit) прогода</span><span class="sxs-lookup"><span data-stu-id="c6db8-107">commonPreparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="c6db8-108">Операция, которая подготавливает фиксированное состояние ввода.</span><span class="sxs-lookup"><span data-stu-id="c6db8-108">An operation that prepares a fixed input state.</span></span>


### <a name="preparation1--qubit--unit-adj--ctl"></a><span data-ttu-id="c6db8-109">preparation1: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] => [единицы измерения](xref:microsoft.quantum.lang-ref.unit) + CTL</span><span class="sxs-lookup"><span data-stu-id="c6db8-109">preparation1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="c6db8-110">Первая из двух операций подготовки состояния для сравнения.</span><span class="sxs-lookup"><span data-stu-id="c6db8-110">The first of the two state preparation operations to be compared.</span></span>


### <a name="preparation2--qubit--unit-adj--ctl"></a><span data-ttu-id="c6db8-111">preparation2: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] => [единицы измерения](xref:microsoft.quantum.lang-ref.unit) + CTL</span><span class="sxs-lookup"><span data-stu-id="c6db8-111">preparation2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="c6db8-112">Вторая из двух операций подготовки состояния для сравнения.</span><span class="sxs-lookup"><span data-stu-id="c6db8-112">The second of the two state preparation operations to be compared.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="c6db8-113">Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c6db8-113">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c6db8-114">Число Кубитс, для которых `commonPreparation` действует, `preparation1` и `preparation2` .</span><span class="sxs-lookup"><span data-stu-id="c6db8-114">The number of qubits on which `commonPreparation`, `preparation1`, and `preparation2` all act.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="c6db8-115">Нмеасурементс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c6db8-115">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c6db8-116">Количество измерений, используемых для оценки перекрытия.</span><span class="sxs-lookup"><span data-stu-id="c6db8-116">The number of measurements to use in estimating the overlap.</span></span>



## <a name="output--double"></a><span data-ttu-id="c6db8-117">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="c6db8-117">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="c6db8-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="c6db8-118">Remarks</span></span>

<span data-ttu-id="c6db8-119">Эта операция использует тест Хадамард для поиска мнимой части $ $ \бегин{алигн} \бракет{\пси | V ^ {\дагжер} U | \пси} \енд{алигн} $ $, где $ \кет{\пси} $ — это состояние, подготовленное `commonPreparation` , $U $ является единым представлением действия `preparation1` , а $V $ соответствует `preparation2` .</span><span class="sxs-lookup"><span data-stu-id="c6db8-119">This operation uses the Hadamard test to find the imaginary part of $$ \begin{align} \braket{\psi | V^{\dagger} U | \psi} \end{align} $$ where $\ket{\psi}$ is the state prepared by `commonPreparation`, $U$ is the unitary representation of the action of `preparation1`, and where $V$ corresponds to `preparation2`.</span></span>

## <a name="references"></a><span data-ttu-id="c6db8-120">Ссылки</span><span class="sxs-lookup"><span data-stu-id="c6db8-120">References</span></span>

- <span data-ttu-id="c6db8-121">Ахаронов *et al.* [Куант-pH/0511096](https://arxiv.org/abs/quant-ph/0511096).</span><span class="sxs-lookup"><span data-stu-id="c6db8-121">Aharonov *et al.* [quant-ph/0511096](https://arxiv.org/abs/quant-ph/0511096).</span></span>

## <a name="see-also"></a><span data-ttu-id="c6db8-122">См. также:</span><span class="sxs-lookup"><span data-stu-id="c6db8-122">See Also</span></span>

- [<span data-ttu-id="c6db8-123">Microsoft. тактов. characters. Естиматереаловерлапбетвинстатес</span><span class="sxs-lookup"><span data-stu-id="c6db8-123">Microsoft.Quantum.Characterization.EstimateRealOverlapBetweenStates</span></span>](xref:Microsoft.Quantum.Characterization.EstimateRealOverlapBetweenStates)
- [<span data-ttu-id="c6db8-124">Microsoft. тактов. characters. Естиматеоверлапбетвинстатес</span><span class="sxs-lookup"><span data-stu-id="c6db8-124">Microsoft.Quantum.Characterization.EstimateOverlapBetweenStates</span></span>](xref:Microsoft.Quantum.Characterization.EstimateOverlapBetweenStates)