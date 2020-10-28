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
# <a name="validationresults-user-defined-type"></a>Определяемый пользователем тип Валидатионресултс

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакеты [](https://nuget.org/packages/)


Результаты проверки классификатора на соответствие набору примеров.

```qsharp

newtype ValidationResults = (NMisclassifications : Int, NValidationSamples : Int);
```



## <a name="named-items"></a>Именованные элементы

### <a name="nmisclassifications--int"></a>Нмисклассификатионс: [int](xref:microsoft.quantum.lang-ref.int)

Число ошибок классификации, наблюдаемых во время проверки.
### <a name="nvalidationsamples--int"></a>Нвалидатионсамплес: [int](xref:microsoft.quantum.lang-ref.int)

