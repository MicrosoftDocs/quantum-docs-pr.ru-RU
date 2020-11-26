---
uid: Microsoft.Quantum.MachineLearning.Misclassifications
title: Функция ошибок классификации
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Misclassifications
qsharp.summary: Given a set of inferred labels and a set of correct labels, returns indices for where each set of labels differs.
ms.openlocfilehash: e13a9b9b65931678d5d87878e81fa172329a28ea
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211684"
---
# <a name="misclassifications-function"></a><span data-ttu-id="ce0a0-102">Функция ошибок классификации</span><span class="sxs-lookup"><span data-stu-id="ce0a0-102">Misclassifications function</span></span>

<span data-ttu-id="ce0a0-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="ce0a0-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="ce0a0-104">Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="ce0a0-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="ce0a0-105">При наличии набора выводимых меток и набора правильных меток возвращает индексы, где каждый набор меток отличается.</span><span class="sxs-lookup"><span data-stu-id="ce0a0-105">Given a set of inferred labels and a set of correct labels, returns indices for where each set of labels differs.</span></span>

```qsharp
function Misclassifications (inferredLabels : Int[], actualLabels : Int[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="ce0a0-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ce0a0-106">Input</span></span>

### <a name="inferredlabels--int"></a><span data-ttu-id="ce0a0-107">Инферредлабелс: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="ce0a0-107">inferredLabels : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="ce0a0-108">Метки, выводимые для заданного обучения или набора проверки.</span><span class="sxs-lookup"><span data-stu-id="ce0a0-108">The labels inferred for a given training or validation set.</span></span>


### <a name="actuallabels--int"></a><span data-ttu-id="ce0a0-109">Актуаллабелс: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="ce0a0-109">actualLabels : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="ce0a0-110">Истинные метки для заданного обучения или набора проверки.</span><span class="sxs-lookup"><span data-stu-id="ce0a0-110">The true labels for a given training or validation set.</span></span>



## <a name="output--int"></a><span data-ttu-id="ce0a0-111">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="ce0a0-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="ce0a0-112">Массив индексов `idx` таким, что `inferredLabels[idx] != actualLabels[idx]` .</span><span class="sxs-lookup"><span data-stu-id="ce0a0-112">An array of indices `idx` such that `inferredLabels[idx] != actualLabels[idx]`.</span></span>