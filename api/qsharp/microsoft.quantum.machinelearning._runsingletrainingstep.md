---
uid: Microsoft.Quantum.MachineLearning._RunSingleTrainingStep
title: _RunSingleTrainingStep операция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: _RunSingleTrainingStep
qsharp.summary: attempts a single parameter update in the direction of mini batch gradient
ms.openlocfilehash: c40bf6f1ceecef2cb196846b4f5a1c49023f1f74
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731185"
---
# <a name="_runsingletrainingstep-operation"></a><span data-ttu-id="a8e08-102">_RunSingleTrainingStep операция</span><span class="sxs-lookup"><span data-stu-id="a8e08-102">_RunSingleTrainingStep operation</span></span>

<span data-ttu-id="a8e08-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="a8e08-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="a8e08-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a8e08-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a8e08-105">предпринимает попытку обновления одного параметра в направлении мини-градиента пакета</span><span class="sxs-lookup"><span data-stu-id="a8e08-105">attempts a single parameter update in the direction of mini batch gradient</span></span>

```qsharp
operation _RunSingleTrainingStep (miniBatch : (Microsoft.Quantum.MachineLearning.LabeledSample, Microsoft.Quantum.MachineLearning.StateGenerator)[], options : Microsoft.Quantum.MachineLearning.TrainingOptions, model : Microsoft.Quantum.MachineLearning.SequentialModel) : (Double, Microsoft.Quantum.MachineLearning.SequentialModel)
```


## <a name="input"></a><span data-ttu-id="a8e08-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a8e08-106">Input</span></span>

### <a name="minibatch--labeledsamplestategenerator"></a><span data-ttu-id="a8e08-107">Уменьшив: ([лабеледсампле](xref:Microsoft.Quantum.MachineLearning.LabeledSample),[статеженератор](xref:Microsoft.Quantum.MachineLearning.StateGenerator)) []</span><span class="sxs-lookup"><span data-stu-id="a8e08-107">miniBatch : ([LabeledSample](xref:Microsoft.Quantum.MachineLearning.LabeledSample),[StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator))[]</span></span>

<span data-ttu-id="a8e08-108">контейнер помеченных образцов в мини-пакете</span><span class="sxs-lookup"><span data-stu-id="a8e08-108">container of labeled samples in the mini batch</span></span>


### <a name="options--trainingoptions"></a><span data-ttu-id="a8e08-109">параметры: [траинингоптионс](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)</span><span class="sxs-lookup"><span data-stu-id="a8e08-109">options : [TrainingOptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)</span></span>




### <a name="model--sequentialmodel"></a><span data-ttu-id="a8e08-110">модель: [секуентиалмодел](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="a8e08-110">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>





## <a name="output--doublesequentialmodel"></a><span data-ttu-id="a8e08-111">Выходные данные: ([Double](xref:microsoft.quantum.lang-ref.double),[секуентиалмодел](xref:Microsoft.Quantum.MachineLearning.SequentialModel))</span><span class="sxs-lookup"><span data-stu-id="a8e08-111">Output : ([Double](xref:microsoft.quantum.lang-ref.double),[SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel))</span></span>

<span data-ttu-id="a8e08-112">(служебная программа, (новое) параметры) пара</span><span class="sxs-lookup"><span data-stu-id="a8e08-112">(utility, (new)parameters) pair</span></span>