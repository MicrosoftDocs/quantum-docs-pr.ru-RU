---
uid: Microsoft.Quantum.MachineLearning.EstimateClassificationProbability
title: Операция Естиматеклассификатионпробабилити
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: EstimateClassificationProbability
qsharp.summary: Given a sample and a sequential classifier, estimates the classification probability for that sample by repeatedly measuring the output of the classifier on the given sample.
ms.openlocfilehash: c2b74bc55ad9005a8f52d05796e856f4f2fb62ba
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853940"
---
# <a name="estimateclassificationprobability-operation"></a>Операция Естиматеклассификатионпробабилити

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


При наличии образца и последовательного классификатора оценивает вероятность классификации для этого образца путем многократного измерения выходных данных классификатора в заданном примере.

```qsharp
operation EstimateClassificationProbability (tolerance : Double, model : Microsoft.Quantum.MachineLearning.SequentialModel, sample : Double[], nMeasurements : Int) : Double
```


## <a name="input"></a>Входные данные

### <a name="tolerance--double"></a>Допуск: [Double](xref:microsoft.quantum.lang-ref.double)

Допуск, позволяющий кодировать образец в операцию подготовки состояния.


### <a name="model--sequentialmodel"></a>модель: [секуентиалмодел](xref:Microsoft.Quantum.MachineLearning.SequentialModel)

Последовательная модель, используемая для оценки вероятности классификации для данного образца.


### <a name="sample--double"></a>Пример: [Double](xref:microsoft.quantum.lang-ref.double)[]

Вектор признаков для примера, который необходимо классифицировать.


### <a name="nmeasurements--int"></a>Нмеасурементс: [int](xref:microsoft.quantum.lang-ref.int)

Количество измерений, используемых для оценки вероятности классификации.



## <a name="output--double"></a>Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)

Оценка вероятности классификации для данного образца.