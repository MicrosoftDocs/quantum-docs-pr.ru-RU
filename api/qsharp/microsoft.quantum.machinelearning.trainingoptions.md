---
uid: Microsoft.Quantum.MachineLearning.TrainingOptions
title: Определяемый пользователем тип Траинингоптионс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: TrainingOptions
qsharp.summary: A collection of options to be used in training quantum classifiers.
ms.openlocfilehash: 5ecc2b5175a4e8db78f72311ac1d5ff964bae811
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732289"
---
# <a name="trainingoptions-user-defined-type"></a><span data-ttu-id="f4ed2-102">Определяемый пользователем тип Траинингоптионс</span><span class="sxs-lookup"><span data-stu-id="f4ed2-102">TrainingOptions user defined type</span></span>

<span data-ttu-id="f4ed2-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="f4ed2-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="f4ed2-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f4ed2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f4ed2-105">Коллекция параметров, используемых в классификаторах тактов для обучения.</span><span class="sxs-lookup"><span data-stu-id="f4ed2-105">A collection of options to be used in training quantum classifiers.</span></span>

```qsharp

newtype TrainingOptions = (LearningRate : Double, Tolerance : Double, MinibatchSize : Int, NMeasurements : Int, MaxEpochs : Int, MaxStalls : Int, StochasticRescaleFactor : Double, ScoringPeriod : Int, VerboseMessage : (String -> Unit));
```



## <a name="named-items"></a><span data-ttu-id="f4ed2-106">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="f4ed2-106">Named Items</span></span>

### <a name="learningrate--double"></a><span data-ttu-id="f4ed2-107">Леарнинграте: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f4ed2-107">LearningRate : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="f4ed2-108">Скорость обучения, с которой следует масштабировать градиенты при обновлении параметров модели во время обучения.</span><span class="sxs-lookup"><span data-stu-id="f4ed2-108">The learning rate by which gradients should be rescaled when updating model parameters during training steps.</span></span>
### <a name="tolerance--double"></a><span data-ttu-id="f4ed2-109">Допуск: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f4ed2-109">Tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="f4ed2-110">Погрешность приближения, используемая при подготовке образцов в качестве состояний тактов.</span><span class="sxs-lookup"><span data-stu-id="f4ed2-110">The approximation tolerance to use when preparing samples as quantum states.</span></span>
### <a name="minibatchsize--int"></a><span data-ttu-id="f4ed2-111">Минибатчсизе: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f4ed2-111">MinibatchSize : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f4ed2-112">Число выборок, используемых в каждом обучающем уменьшив.</span><span class="sxs-lookup"><span data-stu-id="f4ed2-112">The number of samples to use in each training minibatch.</span></span>
### <a name="nmeasurements--int"></a><span data-ttu-id="f4ed2-113">Нмеасурементс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f4ed2-113">NMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f4ed2-114">Количество попыток измерения результатов классификации для оценки вероятности классификации.</span><span class="sxs-lookup"><span data-stu-id="f4ed2-114">The number of times to measure each classification result in order to estimate the classification probability.</span></span>
### <a name="maxepochs--int"></a><span data-ttu-id="f4ed2-115">Максепочс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f4ed2-115">MaxEpochs : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f4ed2-116">Максимальное число эпох для обучения каждой модели.</span><span class="sxs-lookup"><span data-stu-id="f4ed2-116">The maximum number of epochs to train each model for.</span></span>
### <a name="maxstalls--int"></a><span data-ttu-id="f4ed2-117">Макссталлс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f4ed2-117">MaxStalls : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f4ed2-118">Максимальное число попыток остановки учебного эпохи (примерно ноль градиента) до сбоя.</span><span class="sxs-lookup"><span data-stu-id="f4ed2-118">The maximum number of times a training epoch is allowed to stall (approximately zero gradient) before failing.</span></span>
### <a name="stochasticrescalefactor--double"></a><span data-ttu-id="f4ed2-119">Сточастикрескалефактор: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f4ed2-119">StochasticRescaleFactor : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="f4ed2-120">Величина перемасштабирования остановленных моделей до повторной попытки обновления.</span><span class="sxs-lookup"><span data-stu-id="f4ed2-120">The amount to rescale stalled models by before retrying an update.</span></span>
### <a name="scoringperiod--int"></a><span data-ttu-id="f4ed2-121">Скорингпериод: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f4ed2-121">ScoringPeriod : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f4ed2-122">Число шагов градиента, которые должны быть взяты между точками оценки.</span><span class="sxs-lookup"><span data-stu-id="f4ed2-122">The number of gradient steps to be taken between scoring points.</span></span>
<span data-ttu-id="f4ed2-123">Для лучшей точности установите значение 1.</span><span class="sxs-lookup"><span data-stu-id="f4ed2-123">For best accuracy, set to 1.</span></span>
### <a name="verbosemessage--string---unit"></a><span data-ttu-id="f4ed2-124">Вербосемессаже: [String](xref:microsoft.quantum.lang-ref.string) -> [единица](xref:microsoft.quantum.lang-ref.unit) строки</span><span class="sxs-lookup"><span data-stu-id="f4ed2-124">VerboseMessage : [String](xref:microsoft.quantum.lang-ref.string) -> [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="f4ed2-125">Функция, которая может использоваться для получения подробной обратной связи.</span><span class="sxs-lookup"><span data-stu-id="f4ed2-125">A function that can be used to provide verbose feedback.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4ed2-126">Remarks</span><span class="sxs-lookup"><span data-stu-id="f4ed2-126">Remarks</span></span>

<span data-ttu-id="f4ed2-127">Этот определяемый пользователем тип не должен создаваться напрямую, а должен задаваться вызовом @"microsoft.quantum.machinelearning.defaulttrainingoptions" , а затем с помощью `w/` оператора переопределять различные значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f4ed2-127">This UDT should not be created directly, but rather should be specified by calling @"microsoft.quantum.machinelearning.defaulttrainingoptions" and then using the `w/` operator to override different defaults.</span></span>

<span data-ttu-id="f4ed2-128">Например, чтобы использовать измерения 100 000 и максимум 8 обучающих эпох:</span><span class="sxs-lookup"><span data-stu-id="f4ed2-128">For example, to use 100,000 measurements and at most 8 training epochs:</span></span>

```Q#
let options = DefaultTrainingOptions()
              w/ NMeasurements <- 100000
              w/ MaxEpochs <- 8;
```

## <a name="references"></a><span data-ttu-id="f4ed2-129">Ссылки</span><span class="sxs-lookup"><span data-stu-id="f4ed2-129">References</span></span>

- [<span data-ttu-id="f4ed2-130">Арксив: 1804.00633</span><span class="sxs-lookup"><span data-stu-id="f4ed2-130">arXiv:1804.00633</span></span>](https://arxiv.org/abs/1804.00633)