---
uid: Microsoft.Quantum.MachineLearning.InferredLabel
title: Функция Инферредлабел
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InferredLabel
qsharp.summary: Given a of classification probability and a bias, returns the label inferred from that probability.
ms.openlocfilehash: 46b24c283a01e6ac1c959ee4a6899591ee708ff7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848419"
---
# <a name="inferredlabel-function"></a><span data-ttu-id="fc889-102">Функция Инферредлабел</span><span class="sxs-lookup"><span data-stu-id="fc889-102">InferredLabel function</span></span>

<span data-ttu-id="fc889-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="fc889-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="fc889-104">Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="fc889-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="fc889-105">При наличии вероятности классификации и смещения возвращает метку, выведенную из этой вероятности.</span><span class="sxs-lookup"><span data-stu-id="fc889-105">Given a of classification probability and a bias, returns the label inferred from that probability.</span></span>

```qsharp
function InferredLabel (bias : Double, probability : Double) : Int
```


## <a name="input"></a><span data-ttu-id="fc889-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="fc889-106">Input</span></span>

### <a name="bias--double"></a><span data-ttu-id="fc889-107">уровень смещения: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="fc889-107">bias : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="fc889-108">Сдвиг между двумя классами, как правило, результатом обучения классификатора.</span><span class="sxs-lookup"><span data-stu-id="fc889-108">The bias between two classes, typically the result of training a classifier.</span></span>


### <a name="probability--double"></a><span data-ttu-id="fc889-109">вероятность: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="fc889-109">probability : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="fc889-110">Вероятности классификации для конкретного примера, которые обычно являются результатом оценки частоты классификации.</span><span class="sxs-lookup"><span data-stu-id="fc889-110">A classification probabilities for a particular sample, typically resulting from estimating its classification frequency.</span></span>



## <a name="output--int"></a><span data-ttu-id="fc889-111">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="fc889-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="fc889-112">Метка, выводимая из данной вероятности классификации.</span><span class="sxs-lookup"><span data-stu-id="fc889-112">The label inferred from the given classification probability.</span></span>