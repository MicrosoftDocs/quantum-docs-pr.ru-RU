---
uid: Microsoft.Quantum.MachineLearning.TrainSequentialClassifier
title: Операция Траинсекуентиалклассифиер
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: TrainSequentialClassifier
qsharp.summary: Given the structure of a sequential classifier, trains the classifier on a given labeled training set.
ms.openlocfilehash: d0b0587ffa93141739bcd6f39324571ffc28dacc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96228667"
---
# <a name="trainsequentialclassifier-operation"></a>Операция Траинсекуентиалклассифиер

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Используя структуру последовательного классификатора, обучить классификатор по заданному пометке обучающий набор.

```qsharp
operation TrainSequentialClassifier (models : Microsoft.Quantum.MachineLearning.SequentialModel[], samples : Microsoft.Quantum.MachineLearning.LabeledSample[], options : Microsoft.Quantum.MachineLearning.TrainingOptions, trainingSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, validationSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule) : (Microsoft.Quantum.MachineLearning.SequentialModel, Int)
```


## <a name="input"></a>Входные данные

### <a name="models--sequentialmodel"></a>модели: [секуентиалмодел](xref:Microsoft.Quantum.MachineLearning.SequentialModel)[]

Массив моделей, используемых в качестве начальных точек во время обучения.


### <a name="samples--labeledsample"></a>Примеры: [лабеледсампле](xref:Microsoft.Quantum.MachineLearning.LabeledSample)[]

Набор обучающих данных с метками, которые будут использоваться для обучения.


### <a name="options--trainingoptions"></a>параметры: [траинингоптионс](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)

Конфигурация, используемая при обучении; @"microsoft.quantum.machinelearning.trainingoptions" @"microsoft.quantum.machinelearning.defaulttrainingoptions" Дополнительные сведения см. в разделе и.


### <a name="trainingschedule--samplingschedule"></a>Траинингсчедуле: [самплингсчедуле](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)

Расписание выборки, которое будет использоваться при выборе образцов из обучающих данных во время обучения.


### <a name="validationschedule--samplingschedule"></a>Валидатионсчедуле: [самплингсчедуле](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)

Расписание выборки, которое будет использоваться при выборе выборок из обучающих данных при выборе, какая начальная точка привела к наилучшему показателю классификатора.



## <a name="output--sequentialmodelint"></a>Выходные данные: ([секуентиалмодел](xref:Microsoft.Quantum.MachineLearning.SequentialModel),[int](xref:microsoft.quantum.lang-ref.int))

- Параметризация заданного классификатора и сдвига между двумя классами, а также соответствующие результаты из каждой из заданных начальных точек.
- Число промахов, обнаруженных в наиболее подходящей модели-классификаторе.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. MachineLearning. Траинсекуентиалклассифиератмодел](xref:Microsoft.Quantum.MachineLearning.TrainSequentialClassifierAtModel)
- [Microsoft. тактов. MachineLearning. Валидатесекуентиалклассифиер](xref:Microsoft.Quantum.MachineLearning.ValidateSequentialClassifier)