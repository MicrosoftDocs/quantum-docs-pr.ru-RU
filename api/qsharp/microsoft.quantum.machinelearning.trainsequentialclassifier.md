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
# <a name="trainsequentialclassifier-operation"></a><span data-ttu-id="19de9-102">Операция Траинсекуентиалклассифиер</span><span class="sxs-lookup"><span data-stu-id="19de9-102">TrainSequentialClassifier operation</span></span>

<span data-ttu-id="19de9-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="19de9-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="19de9-104">Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="19de9-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="19de9-105">Используя структуру последовательного классификатора, обучить классификатор по заданному пометке обучающий набор.</span><span class="sxs-lookup"><span data-stu-id="19de9-105">Given the structure of a sequential classifier, trains the classifier on a given labeled training set.</span></span>

```qsharp
operation TrainSequentialClassifier (models : Microsoft.Quantum.MachineLearning.SequentialModel[], samples : Microsoft.Quantum.MachineLearning.LabeledSample[], options : Microsoft.Quantum.MachineLearning.TrainingOptions, trainingSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, validationSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule) : (Microsoft.Quantum.MachineLearning.SequentialModel, Int)
```


## <a name="input"></a><span data-ttu-id="19de9-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="19de9-106">Input</span></span>

### <a name="models--sequentialmodel"></a><span data-ttu-id="19de9-107">модели: [секуентиалмодел](xref:Microsoft.Quantum.MachineLearning.SequentialModel)[]</span><span class="sxs-lookup"><span data-stu-id="19de9-107">models : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)[]</span></span>

<span data-ttu-id="19de9-108">Массив моделей, используемых в качестве начальных точек во время обучения.</span><span class="sxs-lookup"><span data-stu-id="19de9-108">An array of models to be used as starting points during training.</span></span>


### <a name="samples--labeledsample"></a><span data-ttu-id="19de9-109">Примеры: [лабеледсампле](xref:Microsoft.Quantum.MachineLearning.LabeledSample)[]</span><span class="sxs-lookup"><span data-stu-id="19de9-109">samples : [LabeledSample](xref:Microsoft.Quantum.MachineLearning.LabeledSample)[]</span></span>

<span data-ttu-id="19de9-110">Набор обучающих данных с метками, которые будут использоваться для обучения.</span><span class="sxs-lookup"><span data-stu-id="19de9-110">A set of labeled training data that will be used to perform training.</span></span>


### <a name="options--trainingoptions"></a><span data-ttu-id="19de9-111">параметры: [траинингоптионс](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)</span><span class="sxs-lookup"><span data-stu-id="19de9-111">options : [TrainingOptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)</span></span>

<span data-ttu-id="19de9-112">Конфигурация, используемая при обучении; @"microsoft.quantum.machinelearning.trainingoptions" @"microsoft.quantum.machinelearning.defaulttrainingoptions" Дополнительные сведения см. в разделе и.</span><span class="sxs-lookup"><span data-stu-id="19de9-112">Configuration to be used when training; see @"microsoft.quantum.machinelearning.trainingoptions" and @"microsoft.quantum.machinelearning.defaulttrainingoptions" for more details.</span></span>


### <a name="trainingschedule--samplingschedule"></a><span data-ttu-id="19de9-113">Траинингсчедуле: [самплингсчедуле](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="19de9-113">trainingSchedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>

<span data-ttu-id="19de9-114">Расписание выборки, которое будет использоваться при выборе образцов из обучающих данных во время обучения.</span><span class="sxs-lookup"><span data-stu-id="19de9-114">A sampling schedule to use when selecting samples from the training data during training steps.</span></span>


### <a name="validationschedule--samplingschedule"></a><span data-ttu-id="19de9-115">Валидатионсчедуле: [самплингсчедуле](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="19de9-115">validationSchedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>

<span data-ttu-id="19de9-116">Расписание выборки, которое будет использоваться при выборе выборок из обучающих данных при выборе, какая начальная точка привела к наилучшему показателю классификатора.</span><span class="sxs-lookup"><span data-stu-id="19de9-116">A sampling schedule to use when selecting samples from the training data when selecting which start point resulted in the best classifier score.</span></span>



## <a name="output--sequentialmodelint"></a><span data-ttu-id="19de9-117">Выходные данные: ([секуентиалмодел](xref:Microsoft.Quantum.MachineLearning.SequentialModel),[int](xref:microsoft.quantum.lang-ref.int))</span><span class="sxs-lookup"><span data-stu-id="19de9-117">Output : ([SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel),[Int](xref:microsoft.quantum.lang-ref.int))</span></span>

- <span data-ttu-id="19de9-118">Параметризация заданного классификатора и сдвига между двумя классами, а также соответствующие результаты из каждой из заданных начальных точек.</span><span class="sxs-lookup"><span data-stu-id="19de9-118">A parameterization of the given classifier and a bias between the two classes, together corresponding to the best result from each of the given start points.</span></span>
- <span data-ttu-id="19de9-119">Число промахов, обнаруженных в наиболее подходящей модели-классификаторе.</span><span class="sxs-lookup"><span data-stu-id="19de9-119">The number of misses observed at the best classifier model.</span></span>

## <a name="see-also"></a><span data-ttu-id="19de9-120">См. также:</span><span class="sxs-lookup"><span data-stu-id="19de9-120">See Also</span></span>

- [<span data-ttu-id="19de9-121">Microsoft. тактов. MachineLearning. Траинсекуентиалклассифиератмодел</span><span class="sxs-lookup"><span data-stu-id="19de9-121">Microsoft.Quantum.MachineLearning.TrainSequentialClassifierAtModel</span></span>](xref:Microsoft.Quantum.MachineLearning.TrainSequentialClassifierAtModel)
- [<span data-ttu-id="19de9-122">Microsoft. тактов. MachineLearning. Валидатесекуентиалклассифиер</span><span class="sxs-lookup"><span data-stu-id="19de9-122">Microsoft.Quantum.MachineLearning.ValidateSequentialClassifier</span></span>](xref:Microsoft.Quantum.MachineLearning.ValidateSequentialClassifier)