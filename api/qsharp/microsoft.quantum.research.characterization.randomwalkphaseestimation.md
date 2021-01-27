---
uid: Microsoft.Quantum.Research.Characterization.RandomWalkPhaseEstimation
title: Операция Рандомвалкфасистиматион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Characterization
qsharp.name: RandomWalkPhaseEstimation
qsharp.summary: Performs iterative phase estimation using a random walk to approximate Bayesian inference on the classical measurement results from a given oracle and eigenstate.
ms.openlocfilehash: f9edafcce62c8b30a6bd52b7dbaa2df2c50c920d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846000"
---
# <a name="randomwalkphaseestimation-operation"></a>Операция Рандомвалкфасистиматион

Пространство имен: [Microsoft. тактов. Research. character](xref:Microsoft.Quantum.Research.Characterization)

Пакет: [Microsoft. тактов. Research. character](https://nuget.org/packages/Microsoft.Quantum.Research.Characterization)


Выполняет итеративную оценку этапа с помощью случайного прохода, чтобы приблизительно Байеса вывод на классический результат измерения из заданных Oracle и еиженстате.

```qsharp
operation RandomWalkPhaseEstimation (initialMean : Double, initialStdDev : Double, nMeasurements : Int, maxMeasurements : Int, unwind : Int, oracle : Microsoft.Quantum.Oracles.ContinuousOracle, targetState : Qubit[]) : Double
```


## <a name="input"></a>Входные данные

### <a name="initialmean--double"></a>Инитиалмеан: [Double](xref:microsoft.quantum.lang-ref.double)

Среднее первоначальное предварительное распределение по $ \фи $.


### <a name="initialstddev--double"></a>Инитиалстддев: [Double](xref:microsoft.quantum.lang-ref.double)

Стандартное отклонение начального нормального предварительного распространения по $ \фи $.


### <a name="nmeasurements--int"></a>Нмеасурементс: [int](xref:microsoft.quantum.lang-ref.int)

Количество измерений, которое должно быть принято в окончательной оценке апостериорные.


### <a name="maxmeasurements--int"></a>Максмеасурементс: [int](xref:microsoft.quantum.lang-ref.int)

Общее количество измерений, которое может быть выполнено до того, как операция будет считаться неудачной.


### <a name="unwind--int"></a>Очистка: [int](xref:microsoft.quantum.lang-ref.int)

Количество результатов, которое следует забывать при сбое проверок согласованности.


### <a name="oracle--continuousoracle"></a>Oracle: [континуаусоракле](xref:Microsoft.Quantum.Oracles.ContinuousOracle)

Операция, представляющая единое $U $ например, $U (t) \кет{\фи} = e ^ {i t \фи}\кет{\фи} $ для еиженстатес $ \кет{\фи} $ с неизвестным этапом $ \фи \ин \Масбб{р} ^ + $.


### <a name="targetstate--qubit"></a>Таржетстате: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистр, с которым работает $U $.



## <a name="output--double"></a>Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)

Окончательная оценка $ \хат{\фи} \масрел{: =} \експект [\фи] $, где ожидание на апостериорные задается всеми принятыми данными.

## <a name="remarks"></a>Remarks

### <a name="iterative-phase-estimation-and-eigenstates"></a>Оценка этапа итерации и Еиженстатес

В общем случае входной регистр `eigenstate` не должен быть еиженстате $ \кет{\фи} $ of $U $, но может быть частью еиженстатес. Предположим, что входное состояние предоставлено \бегин{алигн} \кет{\пси} & = \сум \_ {j} \алфа \_ j \кет{\фи \_ j}, \енд{алигн}, где $ \{ \алфа \_ j \} $ являются сложными коэффициентами, такими, что $ \сум \_ j | \алфа \_ j | ^ 2 = $1 и где $U \кет{\фи \_ j} = \Phi \_ j\ket {\ фи \_ j} $.

Затем выполнение итеративной оценки этапа будет в конечном итоге соединить один еиженстате, как описано в разделе " [рекомендации по разработке](xref:microsoft.quantum.libraries.characterization#iterative-phase-estimation-without-eigenstates)".

### <a name="experiment-design"></a>Проектирование экспериментов

Измерение времени $t $ и углов инверсии $ \сета $, переданных в, `oracle` выбирается в соответствии с *эвристическим эвристиком предположения*, \Бегин{алигн} \сета \сим \пр (\фи), \куад t \аппрокс \фрак {1} {\варианце{\фи}}.
\енд{алигн} этот эвристический подход оптимальен для уменьшения ожидаемой дисперсии апостериорные в итеративной оценке этапа в соответствии с предположением обычного ранее.

### <a name="optimality"></a>Оптимальность

Эта операция приближена к оптимальному средству оценки для этапа $ \фи $, как это было оценено с использованием квадратичной потери $L (\фи, \хат{\фи}) \масрел{: =} (\фи-\хат{\фи}) ^ 2 $.

Дополнительные сведения о статистике оценки этапа итерации см. в разделе [Оценка этапа Байеса](xref:microsoft.quantum.libraries.characterization#bayesian-phase-estimation) .

## <a name="references"></a>Ссылки

- Феррие *et al.* 2011 [ДОИ: 10/tfx](https://doi.org/10.1007/s11128-012-0407-6), [арксив: 1110.3067](https://arxiv.org/abs/1110.3067).
- Виебе *et al.* 2013 [ДОИ: 10/TF3](https://doi.org/10.1103/PhysRevLett.112.190501), [арксив: 1309.0876](https://arxiv.org/abs/1309.0876)
- Виебе и Гранаде 2018 *(в процессе подготовки)*.