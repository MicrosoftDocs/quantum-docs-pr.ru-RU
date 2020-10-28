---
uid: Microsoft.Quantum.Characterization.EstimateOverlapBetweenStates
title: Операция Естиматеоверлапбетвинстатес
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateOverlapBetweenStates
qsharp.summary: Given two operations which each prepare copies of a state, estimates the squared overlap between the states prepared by each operation.
ms.openlocfilehash: 58a367c7ff7d13ac5c1eb1588fb8dac66414776c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714992"
---
# <a name="estimateoverlapbetweenstates-operation"></a><span data-ttu-id="afb64-102">Операция Естиматеоверлапбетвинстатес</span><span class="sxs-lookup"><span data-stu-id="afb64-102">EstimateOverlapBetweenStates operation</span></span>

<span data-ttu-id="afb64-103">Пространство имен: [Microsoft. тактов. charactering](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="afb64-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="afb64-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="afb64-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="afb64-105">При наличии двух операций, каждый из которых подготавливает копии состояния, вычисляет квадрат перекрытия между состояниями, подготовленными каждой операцией.</span><span class="sxs-lookup"><span data-stu-id="afb64-105">Given two operations which each prepare copies of a state, estimates the squared overlap between the states prepared by each operation.</span></span>

```qsharp
operation EstimateOverlapBetweenStates (preparation1 : (Qubit[] => Unit is Adj), preparation2 : (Qubit[] => Unit is Adj), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a><span data-ttu-id="afb64-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="afb64-106">Input</span></span>

### <a name="preparation1--qubit--unit-adj"></a><span data-ttu-id="afb64-107">preparation1: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] [=>ная](xref:microsoft.quantum.lang-ref.unit) прогода</span><span class="sxs-lookup"><span data-stu-id="afb64-107">preparation1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="afb64-108">Первая из двух операций подготовки состояния для сравнения.</span><span class="sxs-lookup"><span data-stu-id="afb64-108">The first of the two state preparation operations to be compared.</span></span>


### <a name="preparation2--qubit--unit-adj"></a><span data-ttu-id="afb64-109">preparation2: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] [=>ная](xref:microsoft.quantum.lang-ref.unit) прогода</span><span class="sxs-lookup"><span data-stu-id="afb64-109">preparation2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="afb64-110">Вторая из двух операций подготовки состояния для сравнения.</span><span class="sxs-lookup"><span data-stu-id="afb64-110">The second of the two state preparation operations to be compared.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="afb64-111">Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="afb64-111">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="afb64-112">Число Кубитс, для которых `commonPreparation` действует, `preparation1` и `preparation2` .</span><span class="sxs-lookup"><span data-stu-id="afb64-112">The number of qubits on which `commonPreparation`, `preparation1`, and `preparation2` all act.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="afb64-113">Нмеасурементс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="afb64-113">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="afb64-114">Количество измерений, используемых для оценки перекрытия.</span><span class="sxs-lookup"><span data-stu-id="afb64-114">The number of measurements to use in estimating the overlap.</span></span>



## <a name="output--double"></a><span data-ttu-id="afb64-115">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="afb64-115">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="afb64-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="afb64-116">Remarks</span></span>

<span data-ttu-id="afb64-117">Эта операция использует тест подкачки для поиска $ $ \бегин{алигн} \лефт | \braket{00\cdots 0 | V ^ {\дагжер} U | 00 \ кдотс 0} \ригхт | ^ 2 \енд{алигн} $ $ WHERE $U $ является единым представлением действия `preparation1` , а $V $ соответствует `preparation2` .</span><span class="sxs-lookup"><span data-stu-id="afb64-117">This operation uses the SWAP test to find $$ \begin{align} \left| \braket{00\cdots 0 | V^{\dagger} U | 00\cdots 0} \right|^2 \end{align} $$ where $U$ is the unitary representation of the action of `preparation1`, and where $V$ corresponds to `preparation2`.</span></span>

## <a name="see-also"></a><span data-ttu-id="afb64-118">См. также:</span><span class="sxs-lookup"><span data-stu-id="afb64-118">See Also</span></span>

- [<span data-ttu-id="afb64-119">Microsoft. тактов. characters. Естиматереаловерлапбетвинстатес</span><span class="sxs-lookup"><span data-stu-id="afb64-119">Microsoft.Quantum.Characterization.EstimateRealOverlapBetweenStates</span></span>](xref:Microsoft.Quantum.Characterization.EstimateRealOverlapBetweenStates)
- [<span data-ttu-id="afb64-120">Microsoft. тактов. characters. Естиматеимаговерлапбетвинстатес</span><span class="sxs-lookup"><span data-stu-id="afb64-120">Microsoft.Quantum.Characterization.EstimateImagOverlapBetweenStates</span></span>](xref:Microsoft.Quantum.Characterization.EstimateImagOverlapBetweenStates)