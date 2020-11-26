---
uid: Microsoft.Quantum.MachineLearning.ValidateSequentialClassifier
title: Операция Валидатесекуентиалклассифиер
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ValidateSequentialClassifier
qsharp.summary: Validates a given sequential classifier against a given set of pre-labeled samples.
ms.openlocfilehash: 5174085edbfd846e8f6649f33e325fd1979ae6a2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196112"
---
# <a name="validatesequentialclassifier-operation"></a>Операция Валидатесекуентиалклассифиер

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Проверяет заданный последовательный классификатор на соответствие заданному набору предварительно помеченных образцов.

```qsharp
operation ValidateSequentialClassifier (model : Microsoft.Quantum.MachineLearning.SequentialModel, samples : Microsoft.Quantum.MachineLearning.LabeledSample[], tolerance : Double, nMeasurements : Int, validationSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule) : Microsoft.Quantum.MachineLearning.ValidationResults
```


## <a name="input"></a>Входные данные

### <a name="model--sequentialmodel"></a>модель: [секуентиалмодел](xref:Microsoft.Quantum.MachineLearning.SequentialModel)

Последовательная модель для проверки.


### <a name="samples--labeledsample"></a>Примеры: [лабеледсампле](xref:Microsoft.Quantum.MachineLearning.LabeledSample)[]

Примеры, используемые для проверки данной модели.


### <a name="tolerance--double"></a>Допуск: [Double](xref:microsoft.quantum.lang-ref.double)

Погрешность аппроксимации, используемая при кодировании каждого образца в качестве входных данных для последовательного классификатора.


### <a name="nmeasurements--int"></a>Нмеасурементс: [int](xref:microsoft.quantum.lang-ref.int)

Количество измерений, используемых при классификации каждого образца.


### <a name="validationschedule--samplingschedule"></a>Валидатионсчедуле: [самплингсчедуле](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)

Расписание, по которому образцы должны быть выведены из набора проверки.



## <a name="output--validationresults"></a>Выходные данные: [валидатионресултс](xref:Microsoft.Quantum.MachineLearning.ValidationResults)

Результаты данной проверки.