---
uid: Microsoft.Quantum.MachineLearning.InferredLabels
title: Функция Инферредлабелс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InferredLabels
qsharp.summary: Given an array of classification probabilities and a bias, returns the label inferred from each probability.
ms.openlocfilehash: 576b4b1f11fc21476bbb019d4b0326981294528c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848397"
---
# <a name="inferredlabels-function"></a><span data-ttu-id="ed5e1-102">Функция Инферредлабелс</span><span class="sxs-lookup"><span data-stu-id="ed5e1-102">InferredLabels function</span></span>

<span data-ttu-id="ed5e1-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="ed5e1-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="ed5e1-104">Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="ed5e1-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="ed5e1-105">При наличии массива вероятностей классификации и смещения возвращает метку, выведенную из каждой вероятности.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-105">Given an array of classification probabilities and a bias, returns the label inferred from each probability.</span></span>

```qsharp
function InferredLabels (bias : Double, probabilities : Double[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="ed5e1-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ed5e1-106">Input</span></span>

### <a name="bias--double"></a><span data-ttu-id="ed5e1-107">уровень смещения: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ed5e1-107">bias : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="ed5e1-108">Сдвиг между двумя классами, как правило, результатом обучения классификатора.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-108">The bias between two classes, typically the result of training a classifier.</span></span>


### <a name="probabilities--double"></a><span data-ttu-id="ed5e1-109">вероятности: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="ed5e1-109">probabilities : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="ed5e1-110">Массив вероятностей классификации для набора выборок, обычно в результате оценки частоты классификации.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-110">An array of classification probabilities for a set of samples, typically resulting from estimating classification frequencies.</span></span>



## <a name="output--int"></a><span data-ttu-id="ed5e1-111">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="ed5e1-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="ed5e1-112">Метка выводится из каждой вероятности классификации.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-112">The label inferred from each classification probability.</span></span>