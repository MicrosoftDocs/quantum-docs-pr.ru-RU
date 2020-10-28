---
uid: Microsoft.Quantum.MachineLearning.InferredLabels
title: Функция Инферредлабелс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InferredLabels
qsharp.summary: Given an array of classification probabilities and a bias, returns the label inferred from each probability.
ms.openlocfilehash: 874d1a2f7cc6d67567e0d2baa70b0d26b639a029
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732352"
---
# <a name="inferredlabels-function"></a><span data-ttu-id="e93ab-102">Функция Инферредлабелс</span><span class="sxs-lookup"><span data-stu-id="e93ab-102">InferredLabels function</span></span>

<span data-ttu-id="e93ab-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="e93ab-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="e93ab-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e93ab-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e93ab-105">При наличии массива вероятностей классификации и смещения возвращает метку, выведенную из каждой вероятности.</span><span class="sxs-lookup"><span data-stu-id="e93ab-105">Given an array of classification probabilities and a bias, returns the label inferred from each probability.</span></span>

```qsharp
function InferredLabels (bias : Double, probabilities : Double[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="e93ab-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e93ab-106">Input</span></span>

### <a name="bias--double"></a><span data-ttu-id="e93ab-107">уровень смещения: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="e93ab-107">bias : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="e93ab-108">Сдвиг между двумя классами, как правило, результатом обучения классификатора.</span><span class="sxs-lookup"><span data-stu-id="e93ab-108">The bias between two classes, typically the result of training a classifier.</span></span>


### <a name="probabilities--double"></a><span data-ttu-id="e93ab-109">вероятности: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="e93ab-109">probabilities : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="e93ab-110">Массив вероятностей классификации для набора выборок, обычно в результате оценки частоты классификации.</span><span class="sxs-lookup"><span data-stu-id="e93ab-110">An array of classification probabilities for a set of samples, typically resulting from estimating classification frequencies.</span></span>



## <a name="output--int"></a><span data-ttu-id="e93ab-111">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="e93ab-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="e93ab-112">Метка выводится из каждой вероятности классификации.</span><span class="sxs-lookup"><span data-stu-id="e93ab-112">The label inferred from each classification probability.</span></span>