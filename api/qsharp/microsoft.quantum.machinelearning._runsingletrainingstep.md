---
uid: Microsoft.Quantum.MachineLearning._RunSingleTrainingStep
title: _RunSingleTrainingStep операция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: _RunSingleTrainingStep
qsharp.summary: attempts a single parameter update in the direction of mini batch gradient
ms.openlocfilehash: 2ee6dbbf26e8514ad59d156da12e0bcaca4ad7ae
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96212109"
---
# <a name="_runsingletrainingstep-operation"></a>_RunSingleTrainingStep операция

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


предпринимает попытку обновления одного параметра в направлении мини-градиента пакета

```qsharp
operation _RunSingleTrainingStep (miniBatch : (Microsoft.Quantum.MachineLearning.LabeledSample, Microsoft.Quantum.MachineLearning.StateGenerator)[], options : Microsoft.Quantum.MachineLearning.TrainingOptions, model : Microsoft.Quantum.MachineLearning.SequentialModel) : (Double, Microsoft.Quantum.MachineLearning.SequentialModel)
```


## <a name="input"></a>Входные данные

### <a name="minibatch--labeledsamplestategenerator"></a>Уменьшив: ([лабеледсампле](xref:Microsoft.Quantum.MachineLearning.LabeledSample),[статеженератор](xref:Microsoft.Quantum.MachineLearning.StateGenerator)) []

контейнер помеченных образцов в мини-пакете


### <a name="options--trainingoptions"></a>параметры: [траинингоптионс](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)




### <a name="model--sequentialmodel"></a>модель: [секуентиалмодел](xref:Microsoft.Quantum.MachineLearning.SequentialModel)





## <a name="output--doublesequentialmodel"></a>Выходные данные: ([Double](xref:microsoft.quantum.lang-ref.double),[секуентиалмодел](xref:Microsoft.Quantum.MachineLearning.SequentialModel))

(служебная программа, (новое) параметры) пара