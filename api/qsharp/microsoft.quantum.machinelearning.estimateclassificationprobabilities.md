---
uid: Microsoft.Quantum.MachineLearning.EstimateClassificationProbabilities
title: Операция Естиматеклассификатионпробабилитиес
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: EstimateClassificationProbabilities
qsharp.summary: Given a set of samples and a sequential classifier, estimates the classification probability for those samples by repeatedly measuring the output of the classifier on each sample.
ms.openlocfilehash: 2b7845d39256f718cc3e415207b8a47b24620bdb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709784"
---
# <a name="estimateclassificationprobabilities-operation"></a>Операция Естиматеклассификатионпробабилитиес

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакеты [](https://nuget.org/packages/)


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