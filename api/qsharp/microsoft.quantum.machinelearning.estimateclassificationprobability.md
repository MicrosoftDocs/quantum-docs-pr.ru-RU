---
uid: Microsoft.Quantum.MachineLearning.EstimateClassificationProbability
title: Операция Естиматеклассификатионпробабилити
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: EstimateClassificationProbability
qsharp.summary: Given a sample and a sequential classifier, estimates the classification probability for that sample by repeatedly measuring the output of the classifier on the given sample.
ms.openlocfilehash: 79e40bc4bc0954dc6742307122609950bf22ec71
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709770"
---
# <a name="estimateclassificationprobability-operation"></a><span data-ttu-id="0ab53-102">Операция Естиматеклассификатионпробабилити</span><span class="sxs-lookup"><span data-stu-id="0ab53-102">EstimateClassificationProbability operation</span></span>

<span data-ttu-id="0ab53-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="0ab53-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="0ab53-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0ab53-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0ab53-105">При наличии образца и последовательного классификатора оценивает вероятность классификации для этого образца путем многократного измерения выходных данных классификатора в заданном примере.</span><span class="sxs-lookup"><span data-stu-id="0ab53-105">Given a sample and a sequential classifier, estimates the classification probability for that sample by repeatedly measuring the output of the classifier on the given sample.</span></span>

```qsharp
operation EstimateClassificationProbability (tolerance : Double, model : Microsoft.Quantum.MachineLearning.SequentialModel, sample : Double[], nMeasurements : Int) : Double
```


## <a name="input"></a><span data-ttu-id="0ab53-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="0ab53-106">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="0ab53-107">Допуск: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="0ab53-107">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="0ab53-108">Допуск, позволяющий кодировать образец в операцию подготовки состояния.</span><span class="sxs-lookup"><span data-stu-id="0ab53-108">The tolerance to allow in encoding the sample into a state preparation operation.</span></span>


### <a name="model--sequentialmodel"></a><span data-ttu-id="0ab53-109">модель: [секуентиалмодел](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="0ab53-109">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>

<span data-ttu-id="0ab53-110">Последовательная модель, используемая для оценки вероятности классификации для данного образца.</span><span class="sxs-lookup"><span data-stu-id="0ab53-110">The sequential model to be used to estimate the classification probability for the given sample.</span></span>


### <a name="sample--double"></a><span data-ttu-id="0ab53-111">Пример: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="0ab53-111">sample : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="0ab53-112">Вектор признаков для примера, который необходимо классифицировать.</span><span class="sxs-lookup"><span data-stu-id="0ab53-112">The feature vector for the sample to be classified.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="0ab53-113">Нмеасурементс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0ab53-113">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0ab53-114">Количество измерений, используемых для оценки вероятности классификации.</span><span class="sxs-lookup"><span data-stu-id="0ab53-114">The number of measurements to use in estimating the classification probability.</span></span>



## <a name="output--double"></a><span data-ttu-id="0ab53-115">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="0ab53-115">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="0ab53-116">Оценка вероятности классификации для данного образца.</span><span class="sxs-lookup"><span data-stu-id="0ab53-116">An estimate of the classification probability for the given sample.</span></span>