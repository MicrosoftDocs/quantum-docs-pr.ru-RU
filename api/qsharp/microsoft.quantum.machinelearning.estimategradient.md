---
uid: Microsoft.Quantum.MachineLearning.EstimateGradient
title: Операция Естиматеградиент
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: EstimateGradient
qsharp.summary: Estimates the training gradient for a sequential classifier at a particular model and for a given encoded input.
ms.openlocfilehash: 79f4abdf131509d4948a3c114e631118329f88d8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211854"
---
# <a name="estimategradient-operation"></a>Операция Естиматеградиент

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Оценивает градиентное обучение для последовательного классификатора в определенной модели и для заданных закодированных входных данных.

```qsharp
operation EstimateGradient (model : Microsoft.Quantum.MachineLearning.SequentialModel, encodedInput : Microsoft.Quantum.MachineLearning.StateGenerator, nMeasurements : Int) : Double[]
```


## <a name="input"></a>Входные данные

### <a name="model--sequentialmodel"></a>модель: [секуентиалмодел](xref:Microsoft.Quantum.MachineLearning.SequentialModel)

Последовательная модель, градиент которой должен быть оценен.


### <a name="encodedinput--stategenerator"></a>Енкодединпут: [статеженератор](xref:Microsoft.Quantum.MachineLearning.StateGenerator)

Входные данные для последовательного классификатора, закодированные в операцию подготовки состояния.


### <a name="nmeasurements--int"></a>Нмеасурементс: [int](xref:microsoft.quantum.lang-ref.int)

Количество измерений, используемых при оценке градиента.



## <a name="output--double"></a>Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)[]

Оценка оценочного градиента на заданном входе и параметрах модели.

## <a name="remarks"></a>Комментарии

Для оценки градиента эта операция использует Хадамард тест и метод сдвига параметров.