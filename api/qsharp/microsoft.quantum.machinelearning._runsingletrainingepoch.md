---
uid: Microsoft.Quantum.MachineLearning._RunSingleTrainingEpoch
title: _RunSingleTrainingEpoch операция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: _RunSingleTrainingEpoch
qsharp.summary: Perform one epoch of sequential classifier training on a subset of data samples.
ms.openlocfilehash: 71780645a025972f11f32f8ba8fd94d098604f9e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196758"
---
# <a name="_runsingletrainingepoch-operation"></a>_RunSingleTrainingEpoch операция

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Выполнение одного эпохи последовательного обучения классификатора на подмножестве образцов данных.

```qsharp
operation _RunSingleTrainingEpoch (encodedSamples : (Microsoft.Quantum.MachineLearning.LabeledSample, Microsoft.Quantum.MachineLearning.StateGenerator)[], schedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, periodScore : Int, options : Microsoft.Quantum.MachineLearning.TrainingOptions, model : Microsoft.Quantum.MachineLearning.SequentialModel, nPreviousBestMisses : Int) : (Int, Microsoft.Quantum.MachineLearning.SequentialModel)
```


## <a name="input"></a>Входные данные

### <a name="encodedsamples--labeledsamplestategenerator"></a>Енкодедсамплес: ([лабеледсампле](xref:Microsoft.Quantum.MachineLearning.LabeledSample),[статеженератор](xref:Microsoft.Quantum.MachineLearning.StateGenerator)) []




### <a name="schedule--samplingschedule"></a>Расписание: [самплингсчедуле](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)




### <a name="periodscore--int"></a>Периодскоре: [int](xref:microsoft.quantum.lang-ref.int)

Число шагов градиента, которые должны быть взяты между точками оценки.
Для лучшей точности установите значение 1.


### <a name="options--trainingoptions"></a>параметры: [траинингоптионс](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)

Параметры, используемые при обучении.


### <a name="model--sequentialmodel"></a>модель: [секуентиалмодел](xref:Microsoft.Quantum.MachineLearning.SequentialModel)

Последовательная модель для обучения.


### <a name="npreviousbestmisses--int"></a>Нпревиаусбестмиссес: [int](xref:microsoft.quantum.lang-ref.int)

Лучшее число ошибок классификации, произошедших в предыдущих эпохах.



## <a name="output--intsequentialmodel"></a>Выходные данные: ([int](xref:microsoft.quantum.lang-ref.int),[секуентиалмодел](xref:Microsoft.Quantum.MachineLearning.SequentialModel))

- Наименьшее число неправильной классификации, наблюдаемое в этом эпохе.
- Найдена новая Лучшая последовательность модели.