---
uid: Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition
title: Операция Апплипермутатионусингдекомпоситион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyPermutationUsingDecomposition
qsharp.summary: Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.
ms.openlocfilehash: 40b51807da155c57c3fa8d740eff28ceef0a0ffc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733969"
---
# <a name="applypermutationusingdecomposition-operation"></a><span data-ttu-id="5b19e-102">Операция Апплипермутатионусингдекомпоситион</span><span class="sxs-lookup"><span data-stu-id="5b19e-102">ApplyPermutationUsingDecomposition operation</span></span>

<span data-ttu-id="5b19e-103">Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="5b19e-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="5b19e-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5b19e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5b19e-105">Пермутес амплитуды в состоянии такта, учитывая перестановку с помощью синтеза на основе декомпозиции.</span><span class="sxs-lookup"><span data-stu-id="5b19e-105">Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.</span></span>

```qsharp
operation ApplyPermutationUsingDecomposition (perm : Int[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="5b19e-106">Описание</span><span class="sxs-lookup"><span data-stu-id="5b19e-106">Description</span></span>

<span data-ttu-id="5b19e-107">Эта процедура реализует метод синтеза на основе декомпозиции.</span><span class="sxs-lookup"><span data-stu-id="5b19e-107">This procedure implements the decomposition based synthesis approach.</span></span>  <span data-ttu-id="5b19e-108">Входные данные представляют собой перестановку $ \пи $ over $2 ^ n $ Elements $ \{ 0, \дотс, 2 ^ n-1 \} $, который представляет переменную $n $-Variable обратимую логическую функцию.</span><span class="sxs-lookup"><span data-stu-id="5b19e-108">The input is a permutation $\pi$ over $2^n$ elements $\{0, \dots, 2^n-1\}$, which represents an $n$-variable reversible Boolean function.</span></span>
<span data-ttu-id="5b19e-109">Алгоритм последовательно выполняет следующие действия для каждого индекса переменной $i $:</span><span class="sxs-lookup"><span data-stu-id="5b19e-109">The algorithm iteratively performs the following steps for each variable index $i$:</span></span>

1. <span data-ttu-id="5b19e-110">Compute $ ((\ pi_l, \ pi_r), \пи ') $ таким, что изображения $ \ pi_l $ и $ \ pi_r $ не изменяют биты в своих элементах в индексах, отличных от $i $, а изображения $ \пи ' $ не изменяют бит $i $ в своих элементах.</span><span class="sxs-lookup"><span data-stu-id="5b19e-110">Compute $((\pi_l, \pi_r), \pi')$ such that the images of $\pi_l$ and $\pi_r$ do not change bits in their elements at indexes other than $i$ and images of $\pi'$ do not change bit $i$ in their elements.</span></span>
2. <span data-ttu-id="5b19e-111">Задайте $ \пи \лефтарров \пи "$" и производные таблицы истинности от $ \ pi_l $ и $ \ pi_r $ на основе элементов, которые не являются фиксированными точками.</span><span class="sxs-lookup"><span data-stu-id="5b19e-111">Set $\pi \leftarrow \pi'$, and derive truth tables from $\pi_l$ and $\pi_r$ based on elements that are not fixed-points.</span></span>

<span data-ttu-id="5b19e-112">После применения этих шагов для всех переменных индексов оставшаяся перестановка $ \пи $ будет являться удостоверением, и на основе собранных таблиц и индексов истинности можно применить операции, контролируемые истинной таблицей, @"microsoft.quantum.intrinsic.x" с помощью @"microsoft.quantum.synthesis.applyxcontrolledontruthtable" операции.</span><span class="sxs-lookup"><span data-stu-id="5b19e-112">After applying these steps for all variable indexes, the remaining permutation $\pi$ will be the identity, and based on the collected truth tables and indexes, one can apply truth-table controlled @"microsoft.quantum.intrinsic.x" operations using the @"microsoft.quantum.synthesis.applyxcontrolledontruthtable" operation.</span></span>

<span data-ttu-id="5b19e-113">Порядок переменных — $0, \дотс, n-$1.</span><span class="sxs-lookup"><span data-stu-id="5b19e-113">The variable order is $0, \dots, n - 1$.</span></span>  <span data-ttu-id="5b19e-114">В операции можно указать пользовательский порядок переменных @"microsoft.quantum.synthesis.applypermutationusingdecompositionwithvariableorder" .</span><span class="sxs-lookup"><span data-stu-id="5b19e-114">A custom variable order can be specified in the operation @"microsoft.quantum.synthesis.applypermutationusingdecompositionwithvariableorder".</span></span>

## <a name="input"></a><span data-ttu-id="5b19e-115">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5b19e-115">Input</span></span>

### <a name="perm--int"></a><span data-ttu-id="5b19e-116">разрешение: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="5b19e-116">perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="5b19e-117">Перестановка элементов $2 ^ n $, начиная с 0.</span><span class="sxs-lookup"><span data-stu-id="5b19e-117">A permutation of $2^n$ elements starting from 0.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="5b19e-118">Кубитс: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="5b19e-118">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="5b19e-119">Список $n $ Кубитс, к которому применяется перестановка.</span><span class="sxs-lookup"><span data-stu-id="5b19e-119">A list of $n$ qubits to which the permutation is applied to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5b19e-120">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5b19e-120">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="5b19e-121">Ссылки</span><span class="sxs-lookup"><span data-stu-id="5b19e-121">References</span></span>

- [<span data-ttu-id="5b19e-122">*Алексис de вос* , *Иван Van рентержем* , rebys. of Dataport. 2 (2), 2008, PP. 183--200</span><span class="sxs-lookup"><span data-stu-id="5b19e-122">*Alexis De Vos* , *Yvan Van Rentergem* , Adv. in Math. of Comm. 2(2), 2008, pp. 183--200</span></span>](http://www.aimsciences.org/article/doi/10.3934/amc.2008.2.183)
- [<span data-ttu-id="5b19e-123">*Матиас соекен* , *Мария Тагуе* , *жерхард W. дуекк* , *ролф дречслер* , журнал символьных вычислений 73 (2016), PP. 1--26</span><span class="sxs-lookup"><span data-stu-id="5b19e-123">*Mathias Soeken* , *Laura Tague* , *Gerhard W. Dueck* , *Rolf Drechsler* , Journal of Symbolic Computation 73 (2016), pp. 1--26</span></span>](https://www.sciencedirect.com/science/article/pii/S0747717115000188?via%3Dihub)

## <a name="see-also"></a><span data-ttu-id="5b19e-124">См. также:</span><span class="sxs-lookup"><span data-stu-id="5b19e-124">See Also</span></span>

- [<span data-ttu-id="5b19e-125">Microsoft. тактов. синтез. Апплипермутатионусингдекомпоситионвисвариаблеордер</span><span class="sxs-lookup"><span data-stu-id="5b19e-125">Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecompositionWithVariableOrder</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecompositionWithVariableOrder)
- [<span data-ttu-id="5b19e-126">Microsoft. тактов. синтез. Апплипермутатионусингтрансформатион</span><span class="sxs-lookup"><span data-stu-id="5b19e-126">Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation)