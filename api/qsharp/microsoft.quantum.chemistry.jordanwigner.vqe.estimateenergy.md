---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.EstimateEnergy
title: Операция Естиматинерги
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: EstimateEnergy
qsharp.summary: Estimates the energy of the molecule by summing the energy contributed by the individual Jordan-Wigner terms.
ms.openlocfilehash: 52e527a68818c80f93bc177d3563064fd0f2aea3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713746"
---
# <a name="estimateenergy-operation"></a><span data-ttu-id="6c503-102">Операция Естиматинерги</span><span class="sxs-lookup"><span data-stu-id="6c503-102">EstimateEnergy operation</span></span>

<span data-ttu-id="6c503-103">Пространство имен: [Microsoft. тактов. химия. жорданвигнер. вке](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="6c503-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="6c503-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6c503-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6c503-105">Оценивает энергию молекулы, суммируя энергию за отдельные условия Jordan-Wigner.</span><span class="sxs-lookup"><span data-stu-id="6c503-105">Estimates the energy of the molecule by summing the energy contributed by the individual Jordan-Wigner terms.</span></span>

```qsharp
operation EstimateEnergy (jwHamiltonian : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData, nSamples : Int) : Double
```


## <a name="description"></a><span data-ttu-id="6c503-106">Описание</span><span class="sxs-lookup"><span data-stu-id="6c503-106">Description</span></span>

<span data-ttu-id="6c503-107">Эта операция неявным образом зависит от соглашения об индексировании со счетчиком.</span><span class="sxs-lookup"><span data-stu-id="6c503-107">This operation implicitly relies on the spin up-down indexing convention.</span></span>

## <a name="input"></a><span data-ttu-id="6c503-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="6c503-108">Input</span></span>

### <a name="jwhamiltonian--jordanwignerencodingdata"></a><span data-ttu-id="6c503-109">Жвхамилтониан: [жорданвигнеренкодингдата](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)</span><span class="sxs-lookup"><span data-stu-id="6c503-109">jwHamiltonian : [JordanWignerEncodingData](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)</span></span>

<span data-ttu-id="6c503-110">Jordan-Wigner Хамилтониан.</span><span class="sxs-lookup"><span data-stu-id="6c503-110">The Jordan-Wigner Hamiltonian.</span></span>


### <a name="nsamples--int"></a><span data-ttu-id="6c503-111">Нсамплес: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6c503-111">nSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6c503-112">Число выборок, используемых для оценки ожидаемых терминов.</span><span class="sxs-lookup"><span data-stu-id="6c503-112">The number of samples to use for the estimation of the term expectations.</span></span>



## <a name="output--double"></a><span data-ttu-id="6c503-113">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="6c503-113">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="6c503-114">Предполагаемое энергопотребление молекулы</span><span class="sxs-lookup"><span data-stu-id="6c503-114">The estimated energy of the molecule</span></span>