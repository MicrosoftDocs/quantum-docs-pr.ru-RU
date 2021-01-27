---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.EstimateEnergy
title: Операция Естиматинерги
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: EstimateEnergy
qsharp.summary: Estimates the energy of the molecule by summing the energy contributed by the individual Jordan-Wigner terms.
ms.openlocfilehash: a64ac3970e3e67568f91b4e67775d834a80c04a1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98835729"
---
# <a name="estimateenergy-operation"></a><span data-ttu-id="c5abb-102">Операция Естиматинерги</span><span class="sxs-lookup"><span data-stu-id="c5abb-102">EstimateEnergy operation</span></span>

<span data-ttu-id="c5abb-103">Пространство имен: [Microsoft. тактов. химия. жорданвигнер. вке](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="c5abb-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="c5abb-104">Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="c5abb-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="c5abb-105">Оценивает энергию молекулы, суммируя энергию за отдельные условия Jordan-Wigner.</span><span class="sxs-lookup"><span data-stu-id="c5abb-105">Estimates the energy of the molecule by summing the energy contributed by the individual Jordan-Wigner terms.</span></span>

```qsharp
operation EstimateEnergy (jwHamiltonian : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData, nSamples : Int) : Double
```


## <a name="description"></a><span data-ttu-id="c5abb-106">Описание</span><span class="sxs-lookup"><span data-stu-id="c5abb-106">Description</span></span>

<span data-ttu-id="c5abb-107">Эта операция неявным образом зависит от соглашения об индексировании со счетчиком.</span><span class="sxs-lookup"><span data-stu-id="c5abb-107">This operation implicitly relies on the spin up-down indexing convention.</span></span>

## <a name="input"></a><span data-ttu-id="c5abb-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c5abb-108">Input</span></span>

### <a name="jwhamiltonian--jordanwignerencodingdata"></a><span data-ttu-id="c5abb-109">Жвхамилтониан: [жорданвигнеренкодингдата](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)</span><span class="sxs-lookup"><span data-stu-id="c5abb-109">jwHamiltonian : [JordanWignerEncodingData](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)</span></span>

<span data-ttu-id="c5abb-110">Jordan-Wigner Хамилтониан.</span><span class="sxs-lookup"><span data-stu-id="c5abb-110">The Jordan-Wigner Hamiltonian.</span></span>


### <a name="nsamples--int"></a><span data-ttu-id="c5abb-111">Нсамплес: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c5abb-111">nSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c5abb-112">Число выборок, используемых для оценки ожидаемых терминов.</span><span class="sxs-lookup"><span data-stu-id="c5abb-112">The number of samples to use for the estimation of the term expectations.</span></span>



## <a name="output--double"></a><span data-ttu-id="c5abb-113">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="c5abb-113">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="c5abb-114">Предполагаемое энергопотребление молекулы</span><span class="sxs-lookup"><span data-stu-id="c5abb-114">The estimated energy of the molecule</span></span>