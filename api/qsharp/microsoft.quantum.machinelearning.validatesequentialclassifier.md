---
uid: Microsoft.Quantum.MachineLearning.ValidateSequentialClassifier
title: Операция Валидатесекуентиалклассифиер
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ValidateSequentialClassifier
qsharp.summary: Validates a given sequential classifier against a given set of pre-labeled samples.
ms.openlocfilehash: 802f1045ea4086bd371d68018a481182cb75b209
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731065"
---
# <a name="validatesequentialclassifier-operation"></a><span data-ttu-id="d73c8-102">Операция Валидатесекуентиалклассифиер</span><span class="sxs-lookup"><span data-stu-id="d73c8-102">ValidateSequentialClassifier operation</span></span>

<span data-ttu-id="d73c8-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="d73c8-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="d73c8-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d73c8-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d73c8-105">Проверяет заданный последовательный классификатор на соответствие заданному набору предварительно помеченных образцов.</span><span class="sxs-lookup"><span data-stu-id="d73c8-105">Validates a given sequential classifier against a given set of pre-labeled samples.</span></span>

```qsharp
operation ValidateSequentialClassifier (model : Microsoft.Quantum.MachineLearning.SequentialModel, samples : Microsoft.Quantum.MachineLearning.LabeledSample[], tolerance : Double, nMeasurements : Int, validationSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule) : Microsoft.Quantum.MachineLearning.ValidationResults
```


## <a name="input"></a><span data-ttu-id="d73c8-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d73c8-106">Input</span></span>

### <a name="model--sequentialmodel"></a><span data-ttu-id="d73c8-107">модель: [секуентиалмодел](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="d73c8-107">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>

<span data-ttu-id="d73c8-108">Последовательная модель для проверки.</span><span class="sxs-lookup"><span data-stu-id="d73c8-108">The sequential model to be validated.</span></span>


### <a name="samples--labeledsample"></a><span data-ttu-id="d73c8-109">Примеры: [лабеледсампле](xref:Microsoft.Quantum.MachineLearning.LabeledSample)[]</span><span class="sxs-lookup"><span data-stu-id="d73c8-109">samples : [LabeledSample](xref:Microsoft.Quantum.MachineLearning.LabeledSample)[]</span></span>

<span data-ttu-id="d73c8-110">Примеры, используемые для проверки данной модели.</span><span class="sxs-lookup"><span data-stu-id="d73c8-110">The samples to be used to validate the given model.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="d73c8-111">Допуск: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d73c8-111">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="d73c8-112">Погрешность аппроксимации, используемая при кодировании каждого образца в качестве входных данных для последовательного классификатора.</span><span class="sxs-lookup"><span data-stu-id="d73c8-112">The approximation tolerance to use in encoding each sample as an input to the sequential classifier.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="d73c8-113">Нмеасурементс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d73c8-113">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d73c8-114">Количество измерений, используемых при классификации каждого образца.</span><span class="sxs-lookup"><span data-stu-id="d73c8-114">The number of measurements to use in classifying each sample.</span></span>


### <a name="validationschedule--samplingschedule"></a><span data-ttu-id="d73c8-115">Валидатионсчедуле: [самплингсчедуле](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="d73c8-115">validationSchedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>

<span data-ttu-id="d73c8-116">Расписание, по которому образцы должны быть выведены из набора проверки.</span><span class="sxs-lookup"><span data-stu-id="d73c8-116">The schedule by which samples should be drawn from the validation set.</span></span>



## <a name="output--validationresults"></a><span data-ttu-id="d73c8-117">Выходные данные: [валидатионресултс](xref:Microsoft.Quantum.MachineLearning.ValidationResults)</span><span class="sxs-lookup"><span data-stu-id="d73c8-117">Output : [ValidationResults](xref:Microsoft.Quantum.MachineLearning.ValidationResults)</span></span>

<span data-ttu-id="d73c8-118">Результаты данной проверки.</span><span class="sxs-lookup"><span data-stu-id="d73c8-118">The results of the given validation.</span></span>