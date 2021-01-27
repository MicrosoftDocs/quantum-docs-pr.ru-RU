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

