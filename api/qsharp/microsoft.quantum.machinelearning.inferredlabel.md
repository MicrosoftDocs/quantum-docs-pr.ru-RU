---
uid: Microsoft.Quantum.MachineLearning.InferredLabel
title: Функция Инферредлабел
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InferredLabel
qsharp.summary: Given a of classification probability and a bias, returns the label inferred from that probability.
ms.openlocfilehash: 1d6edec94f731fe96da797f0c3d77e6eba565149
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732369"
---
# <a name="inferredlabel-function"></a><span data-ttu-id="7758f-102">Функция Инферредлабел</span><span class="sxs-lookup"><span data-stu-id="7758f-102">InferredLabel function</span></span>

<span data-ttu-id="7758f-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="7758f-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="7758f-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7758f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7758f-105">При наличии вероятности классификации и смещения возвращает метку, выведенную из этой вероятности.</span><span class="sxs-lookup"><span data-stu-id="7758f-105">Given a of classification probability and a bias, returns the label inferred from that probability.</span></span>

```qsharp
function InferredLabel (bias : Double, probability : Double) : Int
```


## <a name="input"></a><span data-ttu-id="7758f-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7758f-106">Input</span></span>

### <a name="bias--double"></a><span data-ttu-id="7758f-107">уровень смещения: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="7758f-107">bias : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="7758f-108">Сдвиг между двумя классами, как правило, результатом обучения классификатора.</span><span class="sxs-lookup"><span data-stu-id="7758f-108">The bias between two classes, typically the result of training a classifier.</span></span>


### <a name="probability--double"></a><span data-ttu-id="7758f-109">вероятность: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="7758f-109">probability : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="7758f-110">Вероятности классификации для конкретного примера, которые обычно являются результатом оценки частоты классификации.</span><span class="sxs-lookup"><span data-stu-id="7758f-110">A classification probabilities for a particular sample, typically resulting from estimating its classification frequency.</span></span>



## <a name="output--int"></a><span data-ttu-id="7758f-111">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7758f-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7758f-112">Метка, выводимая из данной вероятности классификации.</span><span class="sxs-lookup"><span data-stu-id="7758f-112">The label inferred from the given classification probability.</span></span>