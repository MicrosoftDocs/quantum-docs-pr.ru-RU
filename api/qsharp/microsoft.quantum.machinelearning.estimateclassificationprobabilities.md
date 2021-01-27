---
uid: Microsoft.Quantum.MachineLearning.EstimateClassificationProbabilities
title: Операция Естиматеклассификатионпробабилитиес
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: EstimateClassificationProbabilities
qsharp.summary: Given a set of samples and a sequential classifier, estimates the classification probability for those samples by repeatedly measuring the output of the classifier on each sample.
ms.openlocfilehash: eea503d042d6ffc241186c117a7c02ee72983b09
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847722"
---
# <a name="estimateclassificationprobabilities-operation"></a><span data-ttu-id="43fcd-102">Операция Естиматеклассификатионпробабилитиес</span><span class="sxs-lookup"><span data-stu-id="43fcd-102">EstimateClassificationProbabilities operation</span></span>

<span data-ttu-id="43fcd-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="43fcd-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="43fcd-104">Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="43fcd-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="43fcd-105">При наличии набора примеров и последовательного классификатора оценивает вероятность классификации для этих образцов путем повторного измерения выходных данных классификатора в каждом примере.</span><span class="sxs-lookup"><span data-stu-id="43fcd-105">Given a set of samples and a sequential classifier, estimates the classification probability for those samples by repeatedly measuring the output of the classifier on each sample.</span></span>

```qsharp
operation EstimateClassificationProbabilities (tolerance : Double, model : Microsoft.Quantum.MachineLearning.SequentialModel, samples : Double[][], nMeasurements : Int) : Double[]
```


## <a name="input"></a><span data-ttu-id="43fcd-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="43fcd-106">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="43fcd-107">Допуск: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="43fcd-107">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="43fcd-108">Допуск, позволяющий кодировать образец в операцию подготовки состояния.</span><span class="sxs-lookup"><span data-stu-id="43fcd-108">The tolerance to allow in encoding the sample into a state preparation operation.</span></span>


### <a name="model--sequentialmodel"></a><span data-ttu-id="43fcd-109">модель: [секуентиалмодел](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="43fcd-109">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>

<span data-ttu-id="43fcd-110">Последовательная модель, используемая для оценки вероятностей классификации для заданных образцов.</span><span class="sxs-lookup"><span data-stu-id="43fcd-110">The sequential model to be used to estimate the classification probabilities for the given samples.</span></span>


### <a name="samples--double"></a><span data-ttu-id="43fcd-111">Примеры: [Double](xref:microsoft.quantum.lang-ref.double)[] []</span><span class="sxs-lookup"><span data-stu-id="43fcd-111">samples : [Double](xref:microsoft.quantum.lang-ref.double)[][]</span></span>

<span data-ttu-id="43fcd-112">Массив векторов признаков для каждой классифицированной выборки.</span><span class="sxs-lookup"><span data-stu-id="43fcd-112">An array of feature vectors for each sample to be classified.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="43fcd-113">Нмеасурементс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="43fcd-113">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="43fcd-114">Количество измерений, используемых для оценки вероятности классификации.</span><span class="sxs-lookup"><span data-stu-id="43fcd-114">The number of measurements to use in estimating the classification probability.</span></span>



## <a name="output--double"></a><span data-ttu-id="43fcd-115">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="43fcd-115">Output : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="43fcd-116">Массив оценок вероятности классификации для каждого заданного образца.</span><span class="sxs-lookup"><span data-stu-id="43fcd-116">An array of estimates of the classification probability for each given sample.</span></span>