---
uid: Microsoft.Quantum.MachineLearning.TrainingOptions
title: Определяемый пользователем тип Траинингоптионс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: TrainingOptions
qsharp.summary: A collection of options to be used in training quantum classifiers.
ms.openlocfilehash: 762d6853910832c6d4cda522c0c5df706d1ed195
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842779"
---
# <a name="trainingoptions-user-defined-type"></a>Определяемый пользователем тип Траинингоптионс

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Коллекция параметров, используемых в классификаторах тактов для обучения.

```qsharp

newtype TrainingOptions = (LearningRate : Double, Tolerance : Double, MinibatchSize : Int, NMeasurements : Int, MaxEpochs : Int, MaxStalls : Int, StochasticRescaleFactor : Double, ScoringPeriod : Int, VerboseMessage : (String -> Unit));
```



## <a name="named-items"></a>Именованные элементы

### <a name="learningrate--double"></a>Леарнинграте: [Double](xref:microsoft.quantum.lang-ref.double)

Скорость обучения, с которой следует масштабировать градиенты при обновлении параметров модели во время обучения.
### <a name="tolerance--double"></a>Допуск: [Double](xref:microsoft.quantum.lang-ref.double)

Погрешность приближения, используемая при подготовке образцов в качестве состояний тактов.
### <a name="minibatchsize--int"></a>Минибатчсизе: [int](xref:microsoft.quantum.lang-ref.int)

Число выборок, используемых в каждом обучающем уменьшив.
### <a name="nmeasurements--int"></a>Нмеасурементс: [int](xref:microsoft.quantum.lang-ref.int)

Количество попыток измерения результатов классификации для оценки вероятности классификации.
### <a name="maxepochs--int"></a>Максепочс: [int](xref:microsoft.quantum.lang-ref.int)

Максимальное число эпох для обучения каждой модели.
### <a name="maxstalls--int"></a>Макссталлс: [int](xref:microsoft.quantum.lang-ref.int)

Максимальное число попыток остановки учебного эпохи (примерно ноль градиента) до сбоя.
### <a name="stochasticrescalefactor--double"></a>Сточастикрескалефактор: [Double](xref:microsoft.quantum.lang-ref.double)

Величина перемасштабирования остановленных моделей до повторной попытки обновления.
### <a name="scoringperiod--int"></a>Скорингпериод: [int](xref:microsoft.quantum.lang-ref.int)

Число шагов градиента, которые должны быть взяты между точками оценки.
Для лучшей точности установите значение 1.
### <a name="verbosemessage--string---unit"></a>Вербосемессаже: [](xref:microsoft.quantum.lang-ref.string) -> [единица](xref:microsoft.quantum.lang-ref.unit) строки

Функция, которая может использоваться для получения подробной обратной связи.

## <a name="remarks"></a>Remarks

Этот определяемый пользователем тип не должен создаваться напрямую, а должен задаваться вызовом @"microsoft.quantum.machinelearning.defaulttrainingoptions" , а затем с помощью `w/` оператора переопределять различные значения по умолчанию.

Например, чтобы использовать измерения 100 000 и максимум 8 обучающих эпох:

```qsharp
let options = DefaultTrainingOptions()
              w/ NMeasurements <- 100000
              w/ MaxEpochs <- 8;
```

## <a name="references"></a>Ссылки

- [Арксив: 1804.00633](https://arxiv.org/abs/1804.00633)