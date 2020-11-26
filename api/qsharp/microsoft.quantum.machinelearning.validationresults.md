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
# <a name="validationresults-user-defined-type"></a>Определяемый пользователем тип Валидатионресултс

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Результаты проверки классификатора на соответствие набору примеров.

```qsharp

newtype ValidationResults = (NMisclassifications : Int, NValidationSamples : Int);
```



## <a name="named-items"></a>Именованные элементы

### <a name="nmisclassifications--int"></a>Нмисклассификатионс: [int](xref:microsoft.quantum.lang-ref.int)

Число ошибок классификации, наблюдаемых во время проверки.
### <a name="nvalidationsamples--int"></a>Нвалидатионсамплес: [int](xref:microsoft.quantum.lang-ref.int)

