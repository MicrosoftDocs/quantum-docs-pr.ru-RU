---
uid: Microsoft.Quantum.MachineLearning.Misclassifications
title: Функция ошибок классификации
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Misclassifications
qsharp.summary: Given a set of inferred labels and a set of correct labels, returns indices for where each set of labels differs.
ms.openlocfilehash: 500c2910f7c5616c88ff6c70ab3cc16680e199fb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732977"
---
# <a name="misclassifications-function"></a><span data-ttu-id="87a19-102">Функция ошибок классификации</span><span class="sxs-lookup"><span data-stu-id="87a19-102">Misclassifications function</span></span>

<span data-ttu-id="87a19-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="87a19-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="87a19-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="87a19-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="87a19-105">При наличии набора выводимых меток и набора правильных меток возвращает индексы, где каждый набор меток отличается.</span><span class="sxs-lookup"><span data-stu-id="87a19-105">Given a set of inferred labels and a set of correct labels, returns indices for where each set of labels differs.</span></span>

```qsharp
function Misclassifications (inferredLabels : Int[], actualLabels : Int[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="87a19-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="87a19-106">Input</span></span>

### <a name="inferredlabels--int"></a><span data-ttu-id="87a19-107">Инферредлабелс: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="87a19-107">inferredLabels : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="87a19-108">Метки, выводимые для заданного обучения или набора проверки.</span><span class="sxs-lookup"><span data-stu-id="87a19-108">The labels inferred for a given training or validation set.</span></span>


### <a name="actuallabels--int"></a><span data-ttu-id="87a19-109">Актуаллабелс: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="87a19-109">actualLabels : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="87a19-110">Истинные метки для заданного обучения или набора проверки.</span><span class="sxs-lookup"><span data-stu-id="87a19-110">The true labels for a given training or validation set.</span></span>



## <a name="output--int"></a><span data-ttu-id="87a19-111">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="87a19-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="87a19-112">Массив индексов `idx` таким, что `inferredLabels[idx] != actualLabels[idx]` .</span><span class="sxs-lookup"><span data-stu-id="87a19-112">An array of indices `idx` such that `inferredLabels[idx] != actualLabels[idx]`.</span></span>