---
uid: Microsoft.Quantum.MachineLearning.ValidationResults
title: Определяемый пользователем тип Валидатионресултс
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ValidationResults
qsharp.summary: The results from having validated a classifier against a set of samples.
ms.openlocfilehash: 42bfab7fd1f9372d9394f2eaf2d698b39b4307e1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211497"
---
# <a name="validationresults-user-defined-type"></a><span data-ttu-id="5f678-102">Определяемый пользователем тип Валидатионресултс</span><span class="sxs-lookup"><span data-stu-id="5f678-102">ValidationResults user defined type</span></span>

<span data-ttu-id="5f678-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="5f678-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="5f678-104">Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="5f678-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="5f678-105">Результаты проверки классификатора на соответствие набору примеров.</span><span class="sxs-lookup"><span data-stu-id="5f678-105">The results from having validated a classifier against a set of samples.</span></span>

```qsharp

newtype ValidationResults = (NMisclassifications : Int, NValidationSamples : Int);
```



## <a name="named-items"></a><span data-ttu-id="5f678-106">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="5f678-106">Named Items</span></span>

### <a name="nmisclassifications--int"></a><span data-ttu-id="5f678-107">Нмисклассификатионс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5f678-107">NMisclassifications : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5f678-108">Число ошибок классификации, наблюдаемых во время проверки.</span><span class="sxs-lookup"><span data-stu-id="5f678-108">The number of misclassifications observed during validation.</span></span>
### <a name="nvalidationsamples--int"></a><span data-ttu-id="5f678-109">Нвалидатионсамплес: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5f678-109">NValidationSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

