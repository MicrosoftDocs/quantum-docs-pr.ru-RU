---
uid: Microsoft.Quantum.MachineLearning.TrainSequentialClassifier
title: Операция Траинсекуентиалклассифиер
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: TrainSequentialClassifier
qsharp.summary: Given the structure of a sequential classifier, trains the classifier on a given labeled training set.
ms.openlocfilehash: 12c4df59941b682d9de798e6585b59d1c34924dc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711309"
---
# <a name="trainsequentialclassifier-operation"></a>Операция Траинсекуентиалклассифиер

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакеты [](https://nuget.org/packages/)


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