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
# <a name="_runsingletrainingepoch-operation"></a><span data-ttu-id="d4a15-102">_RunSingleTrainingEpoch операция</span><span class="sxs-lookup"><span data-stu-id="d4a15-102">_RunSingleTrainingEpoch operation</span></span>

<span data-ttu-id="d4a15-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="d4a15-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="d4a15-104">Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="d4a15-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="d4a15-105">Выполнение одного эпохи последовательного обучения классификатора на подмножестве образцов данных.</span><span class="sxs-lookup"><span data-stu-id="d4a15-105">Perform one epoch of sequential classifier training on a subset of data samples.</span></span>

```qsharp
operation _RunSingleTrainingEpoch (encodedSamples : (Microsoft.Quantum.MachineLearning.LabeledSample, Microsoft.Quantum.MachineLearning.StateGenerator)[], schedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, periodScore : Int, options : Microsoft.Quantum.MachineLearning.TrainingOptions, model : Microsoft.Quantum.MachineLearning.SequentialModel, nPreviousBestMisses : Int) : (Int, Microsoft.Quantum.MachineLearning.SequentialModel)
```


## <a name="input"></a><span data-ttu-id="d4a15-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d4a15-106">Input</span></span>

### <a name="encodedsamples--labeledsamplestategenerator"></a><span data-ttu-id="d4a15-107">Енкодедсамплес: ([лабеледсампле](xref:Microsoft.Quantum.MachineLearning.LabeledSample),[статеженератор](xref:Microsoft.Quantum.MachineLearning.StateGenerator)) []</span><span class="sxs-lookup"><span data-stu-id="d4a15-107">encodedSamples : ([LabeledSample](xref:Microsoft.Quantum.MachineLearning.LabeledSample),[StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator))[]</span></span>




### <a name="schedule--samplingschedule"></a><span data-ttu-id="d4a15-108">Расписание: [самплингсчедуле](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="d4a15-108">schedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>




### <a name="periodscore--int"></a><span data-ttu-id="d4a15-109">Периодскоре: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d4a15-109">periodScore : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d4a15-110">Число шагов градиента, которые должны быть взяты между точками оценки.</span><span class="sxs-lookup"><span data-stu-id="d4a15-110">The number of gradient steps to be taken between scoring points.</span></span>
<span data-ttu-id="d4a15-111">Для лучшей точности установите значение 1.</span><span class="sxs-lookup"><span data-stu-id="d4a15-111">For best accuracy, set to 1.</span></span>


### <a name="options--trainingoptions"></a><span data-ttu-id="d4a15-112">параметры: [траинингоптионс](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)</span><span class="sxs-lookup"><span data-stu-id="d4a15-112">options : [TrainingOptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)</span></span>

<span data-ttu-id="d4a15-113">Параметры, используемые при обучении.</span><span class="sxs-lookup"><span data-stu-id="d4a15-113">Options to be used in training.</span></span>


### <a name="model--sequentialmodel"></a><span data-ttu-id="d4a15-114">модель: [секуентиалмодел](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="d4a15-114">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>

<span data-ttu-id="d4a15-115">Последовательная модель для обучения.</span><span class="sxs-lookup"><span data-stu-id="d4a15-115">The sequential model to be trained.</span></span>


### <a name="npreviousbestmisses--int"></a><span data-ttu-id="d4a15-116">Нпревиаусбестмиссес: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d4a15-116">nPreviousBestMisses : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d4a15-117">Лучшее число ошибок классификации, произошедших в предыдущих эпохах.</span><span class="sxs-lookup"><span data-stu-id="d4a15-117">The best number of misclassifications observed in previous epochs.</span></span>



## <a name="output--intsequentialmodel"></a><span data-ttu-id="d4a15-118">Выходные данные: ([int](xref:microsoft.quantum.lang-ref.int),[секуентиалмодел](xref:Microsoft.Quantum.MachineLearning.SequentialModel))</span><span class="sxs-lookup"><span data-stu-id="d4a15-118">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel))</span></span>

- <span data-ttu-id="d4a15-119">Наименьшее число неправильной классификации, наблюдаемое в этом эпохе.</span><span class="sxs-lookup"><span data-stu-id="d4a15-119">The smallest number of misclassifications observed through to this epoch.</span></span>
- <span data-ttu-id="d4a15-120">Найдена новая Лучшая последовательность модели.</span><span class="sxs-lookup"><span data-stu-id="d4a15-120">The new best sequential model found.</span></span>