---
uid: Microsoft.Quantum.MachineLearning.ValidationResults
title: Определяемый пользователем тип Валидатионресултс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ValidationResults
qsharp.summary: The results from having validated a classifier against a set of samples.
ms.openlocfilehash: 1e54a5a086035f5f8d36d777badb306156d99600
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731056"
---
# <a name="validationresults-user-defined-type"></a><span data-ttu-id="bfff7-102">Определяемый пользователем тип Валидатионресултс</span><span class="sxs-lookup"><span data-stu-id="bfff7-102">ValidationResults user defined type</span></span>

<span data-ttu-id="bfff7-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="bfff7-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="bfff7-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="bfff7-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="bfff7-105">Результаты проверки классификатора на соответствие набору примеров.</span><span class="sxs-lookup"><span data-stu-id="bfff7-105">The results from having validated a classifier against a set of samples.</span></span>

```qsharp

newtype ValidationResults = (NMisclassifications : Int, NValidationSamples : Int);
```



## <a name="named-items"></a><span data-ttu-id="bfff7-106">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="bfff7-106">Named Items</span></span>

### <a name="nmisclassifications--int"></a><span data-ttu-id="bfff7-107">Нмисклассификатионс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="bfff7-107">NMisclassifications : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="bfff7-108">Число ошибок классификации, наблюдаемых во время проверки.</span><span class="sxs-lookup"><span data-stu-id="bfff7-108">The number of misclassifications observed during validation.</span></span>
### <a name="nvalidationsamples--int"></a><span data-ttu-id="bfff7-109">Нвалидатионсамплес: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="bfff7-109">NValidationSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>
