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
# <a name="estimateclassificationprobabilities-operation"></a>Операция Естиматеклассификатионпробабилитиес

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


При наличии набора примеров и последовательного классификатора оценивает вероятность классификации для этих образцов путем повторного измерения выходных данных классификатора в каждом примере.

```qsharp
operation EstimateClassificationProbabilities (tolerance : Double, model : Microsoft.Quantum.MachineLearning.SequentialModel, samples : Double[][], nMeasurements : Int) : Double[]
```


## <a name="input"></a>Входные данные

### <a name="tolerance--double"></a>Допуск: [Double](xref:microsoft.quantum.lang-ref.double)

Допуск, позволяющий кодировать образец в операцию подготовки состояния.


### <a name="model--sequentialmodel"></a>модель: [секуентиалмодел](xref:Microsoft.Quantum.MachineLearning.SequentialModel)

Последовательная модель, используемая для оценки вероятностей классификации для заданных образцов.


### <a name="samples--double"></a>Примеры: [Double](xref:microsoft.quantum.lang-ref.double)[] []

Массив векторов признаков для каждой классифицированной выборки.


### <a name="nmeasurements--int"></a>Нмеасурементс: [int](xref:microsoft.quantum.lang-ref.int)

Количество измерений, используемых для оценки вероятности классификации.



## <a name="output--double"></a>Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)[]

Массив оценок вероятности классификации для каждого заданного образца.