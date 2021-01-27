---
uid: Microsoft.Quantum.MachineLearning.EstimateGradient
title: Операция Естиматеградиент
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: EstimateGradient
qsharp.summary: Estimates the training gradient for a sequential classifier at a particular model and for a given encoded input.
ms.openlocfilehash: 38edcb67e7dcc5d2e971fb507a792937774a702c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844382"
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

## <a name="remarks"></a>Remarks

Для оценки градиента эта операция использует Хадамард тест и метод сдвига параметров.