---
uid: Microsoft.Quantum.MachineLearning.ValidationResults
title: Определяемый пользователем тип Валидатионресултс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ValidationResults
qsharp.summary: The results from having validated a classifier against a set of samples.
ms.openlocfilehash: 923fd80333b6bf77daeaac2bf205db620e61cfd0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846095"
---
# <a name="validationresults-user-defined-type"></a><span data-ttu-id="7faee-102">Определяемый пользователем тип Валидатионресултс</span><span class="sxs-lookup"><span data-stu-id="7faee-102">ValidationResults user defined type</span></span>

<span data-ttu-id="7faee-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="7faee-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="7faee-104">Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="7faee-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="7faee-105">Результаты проверки классификатора на соответствие набору примеров.</span><span class="sxs-lookup"><span data-stu-id="7faee-105">The results from having validated a classifier against a set of samples.</span></span>

```qsharp

newtype ValidationResults = (NMisclassifications : Int, NValidationSamples : Int);
```



## <a name="named-items"></a><span data-ttu-id="7faee-106">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="7faee-106">Named Items</span></span>

### <a name="nmisclassifications--int"></a><span data-ttu-id="7faee-107">Нмисклассификатионс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7faee-107">NMisclassifications : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7faee-108">Число ошибок классификации, наблюдаемых во время проверки.</span><span class="sxs-lookup"><span data-stu-id="7faee-108">The number of misclassifications observed during validation.</span></span>
### <a name="nvalidationsamples--int"></a><span data-ttu-id="7faee-109">Нвалидатионсамплес: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7faee-109">NValidationSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

