---
uid: Microsoft.Quantum.Characterization.RobustPhaseEstimation
title: Операция Робустфасистиматион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: RobustPhaseEstimation
qsharp.summary: Performs the robust non-iterative quantum phase estimation algorithm for a given oracle `U` and eigenstate, and provides a single real-valued estimate of the phase with variance scaling at the Heisenberg limit.
ms.openlocfilehash: d04ee578c0e6f916e9a4da451075b79e0630c70a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714936"
---
# <a name="robustphaseestimation-operation"></a>Операция Робустфасистиматион

Пространство имен: [Microsoft. тактов. charactering](xref:Microsoft.Quantum.Characterization)

Пакеты [](https://nuget.org/packages/)


Выполняет устойчивый алгоритм оценки неитеративного тактового этапа для заданных Oracle `U` и еиженстате и предоставляет единую оценку этапа с масштабированием в пределах Гейзенбега.

```qsharp
operation RobustPhaseEstimation (bitsPrecision : Int, oracle : Microsoft.Quantum.Oracles.DiscreteOracle, targetState : Qubit[]) : Double
```


## <a name="input"></a>Входные данные

### <a name="bitsprecision--int"></a>БитспреЦисион: [int](xref:microsoft.quantum.lang-ref.int)

Это дает оценку $ \фи $ со стандартным отклонением $ \сигма \ле 2 \ PI/2 ^ \Текст{битспреЦисион} $ с помощью такого количества запросов, как $ \сигма \ле 10,7 \пи/\текст{# запросов} $.


### <a name="oracle--discreteoracle"></a>Oracle: [дискретеоракле](xref:Microsoft.Quantum.Oracles.DiscreteOracle)

Операция, реализующая $U ^ m $ для заданного целого числа, включает $m $.


### <a name="targetstate--qubit"></a>Таржетстате: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистр такта, в котором $U $ действует. Если в нем хранится еиженстате $ \кет{\фи} $ of $U $, то $U \кет{\фи} = e ^ {и\фи} \кет{\фи} $ for $ \фи\ин (-\пи, \пи] $ Неизвестный этап.



## <a name="output--double"></a>Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)



## <a name="remarks"></a>Remarks

В ограничении большого количества запросов Cramer-Rao нижние границы для стандартного отклонения от оценки $ \фи $ удовлетворяет $ \сигма \же 2 \пи/\текст{# запросов} $.

## <a name="references"></a>Ссылки

- Надежная калибровка универсального Single-Qubit Gate-Set с помощью надежной оценки этапа Шелби Киммел, Guang Хао Low, текста книги J. Йодер https://arxiv.org/abs/1502.02677