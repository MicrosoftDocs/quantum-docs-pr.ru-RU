---
uid: Microsoft.Quantum.MachineLearning.TrainSequentialClassifierAtModel
title: Операция Траинсекуентиалклассифиератмодел
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: TrainSequentialClassifierAtModel
qsharp.summary: Given the structure of a sequential classifier, trains the classifier on a given labeled training set, starting from a particular model.
ms.openlocfilehash: b9e30e4e5bc23f56d9119083045967caff28f13a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731073"
---
# <a name="trainsequentialclassifieratmodel-operation"></a><span data-ttu-id="4e7a2-102">Операция Траинсекуентиалклассифиератмодел</span><span class="sxs-lookup"><span data-stu-id="4e7a2-102">TrainSequentialClassifierAtModel operation</span></span>

<span data-ttu-id="4e7a2-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="4e7a2-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="4e7a2-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4e7a2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4e7a2-105">Используя структуру последовательного классификатора, обучить классификатор в заданном пометке обучающий набор, начиная с определенной модели.</span><span class="sxs-lookup"><span data-stu-id="4e7a2-105">Given the structure of a sequential classifier, trains the classifier on a given labeled training set, starting from a particular model.</span></span>

```qsharp
operation TrainSequentialClassifierAtModel (model : Microsoft.Quantum.MachineLearning.SequentialModel, samples : Microsoft.Quantum.MachineLearning.LabeledSample[], options : Microsoft.Quantum.MachineLearning.TrainingOptions, trainingSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, validationSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule) : (Microsoft.Quantum.MachineLearning.SequentialModel, Int)
```


## <a name="input"></a><span data-ttu-id="4e7a2-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="4e7a2-106">Input</span></span>

### <a name="model--sequentialmodel"></a><span data-ttu-id="4e7a2-107">модель: [секуентиалмодел](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="4e7a2-107">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>

<span data-ttu-id="4e7a2-108">Последовательная модель, которая будет использоваться в качестве отправной точки для обучения.</span><span class="sxs-lookup"><span data-stu-id="4e7a2-108">The sequential model to be used as a starting point for training.</span></span>


### <a name="samples--labeledsample"></a><span data-ttu-id="4e7a2-109">Примеры: [лабеледсампле](xref:Microsoft.Quantum.MachineLearning.LabeledSample)[]</span><span class="sxs-lookup"><span data-stu-id="4e7a2-109">samples : [LabeledSample](xref:Microsoft.Quantum.MachineLearning.LabeledSample)[]</span></span>

<span data-ttu-id="4e7a2-110">Набор обучающих данных с метками, которые будут использоваться для обучения.</span><span class="sxs-lookup"><span data-stu-id="4e7a2-110">A set of labeled training data that will be used to perform training.</span></span>


### <a name="options--trainingoptions"></a><span data-ttu-id="4e7a2-111">параметры: [траинингоптионс](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)</span><span class="sxs-lookup"><span data-stu-id="4e7a2-111">options : [TrainingOptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)</span></span>

<span data-ttu-id="4e7a2-112">Конфигурация, используемая при обучении; @"microsoft.quantum.machinelearning.trainingoptions" @"microsoft.quantum.machinelearning.defaulttrainingoptions" Дополнительные сведения см. в разделе и.</span><span class="sxs-lookup"><span data-stu-id="4e7a2-112">Configuration to be used when training; see @"microsoft.quantum.machinelearning.trainingoptions" and @"microsoft.quantum.machinelearning.defaulttrainingoptions" for more details.</span></span>


### <a name="trainingschedule--samplingschedule"></a><span data-ttu-id="4e7a2-113">Траинингсчедуле: [самплингсчедуле](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="4e7a2-113">trainingSchedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>

<span data-ttu-id="4e7a2-114">Расписание выборки, которое будет использоваться при выборе образцов из обучающих данных во время обучения.</span><span class="sxs-lookup"><span data-stu-id="4e7a2-114">A sampling schedule to use when selecting samples from the training data during training steps.</span></span>


### <a name="validationschedule--samplingschedule"></a><span data-ttu-id="4e7a2-115">Валидатионсчедуле: [самплингсчедуле](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="4e7a2-115">validationSchedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>

<span data-ttu-id="4e7a2-116">Расписание выборки, которое будет использоваться при выборе выборок из обучающих данных при выборе, какая начальная точка привела к наилучшему показателю классификатора.</span><span class="sxs-lookup"><span data-stu-id="4e7a2-116">A sampling schedule to use when selecting samples from the training data when selecting which start point resulted in the best classifier score.</span></span>



## <a name="output--sequentialmodelint"></a><span data-ttu-id="4e7a2-117">Выходные данные: ([секуентиалмодел](xref:Microsoft.Quantum.MachineLearning.SequentialModel),[int](xref:microsoft.quantum.lang-ref.int))</span><span class="sxs-lookup"><span data-stu-id="4e7a2-117">Output : ([SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel),[Int](xref:microsoft.quantum.lang-ref.int))</span></span>

- <span data-ttu-id="4e7a2-118">Параметризация заданного классификатора и сдвига между двумя классами, а также соответствующие результаты из каждой из заданных начальных точек.</span><span class="sxs-lookup"><span data-stu-id="4e7a2-118">A parameterization of the given classifier and a bias between the two classes, together corresponding to the best result from each of the given start points.</span></span>
- <span data-ttu-id="4e7a2-119">Число промахов, обнаруженных в наиболее подходящей модели-классификаторе.</span><span class="sxs-lookup"><span data-stu-id="4e7a2-119">The number of misses observed at the best classifier model.</span></span>

## <a name="see-also"></a><span data-ttu-id="4e7a2-120">См. также:</span><span class="sxs-lookup"><span data-stu-id="4e7a2-120">See Also</span></span>

- [<span data-ttu-id="4e7a2-121">Microsoft. тактов. MachineLearning. Траинсекуентиалклассифиер</span><span class="sxs-lookup"><span data-stu-id="4e7a2-121">Microsoft.Quantum.MachineLearning.TrainSequentialClassifier</span></span>](xref:Microsoft.Quantum.MachineLearning.TrainSequentialClassifier)
- [<span data-ttu-id="4e7a2-122">Microsoft. тактов. MachineLearning. Валидатесекуентиалклассифиер</span><span class="sxs-lookup"><span data-stu-id="4e7a2-122">Microsoft.Quantum.MachineLearning.ValidateSequentialClassifier</span></span>](xref:Microsoft.Quantum.MachineLearning.ValidateSequentialClassifier)