---
uid: Microsoft.Quantum.MachineLearning.TrainSequentialClassifierAtModel
title: Операция Траинсекуентиалклассифиератмодел
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: TrainSequentialClassifierAtModel
qsharp.summary: Given the structure of a sequential classifier, trains the classifier on a given labeled training set, starting from a particular model.
ms.openlocfilehash: 4164c190cb19b6d3ea74d9803a77d2b19607279b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857161"
---
# <a name="trainsequentialclassifieratmodel-operation"></a>Операция Траинсекуентиалклассифиератмодел

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Используя структуру последовательного классификатора, обучить классификатор в заданном пометке обучающий набор, начиная с определенной модели.

```qsharp
operation TrainSequentialClassifierAtModel (model : Microsoft.Quantum.MachineLearning.SequentialModel, samples : Microsoft.Quantum.MachineLearning.LabeledSample[], options : Microsoft.Quantum.MachineLearning.TrainingOptions, trainingSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, validationSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule) : (Microsoft.Quantum.MachineLearning.SequentialModel, Int)
```


## <a name="input"></a>Входные данные

### <a name="model--sequentialmodel"></a>модель: [секуентиалмодел](xref:Microsoft.Quantum.MachineLearning.SequentialModel)

Последовательная модель, которая будет использоваться в качестве отправной точки для обучения.


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

- [Microsoft. тактов. MachineLearning. Траинсекуентиалклассифиер](xref:Microsoft.Quantum.MachineLearning.TrainSequentialClassifier)
- [Microsoft. тактов. MachineLearning. Валидатесекуентиалклассифиер](xref:Microsoft.Quantum.MachineLearning.ValidateSequentialClassifier)