---
uid: Microsoft.Quantum.Characterization.RobustPhaseEstimation
title: Операция Робустфасистиматион
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: RobustPhaseEstimation
qsharp.summary: Performs the robust non-iterative quantum phase estimation algorithm for a given oracle `U` and eigenstate, and provides a single real-valued estimate of the phase with variance scaling at the Heisenberg limit.
ms.openlocfilehash: 3e6774e2fe348668840cdc08fe3a070ec3d82a6d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216087"
---
# <a name="robustphaseestimation-operation"></a>Операция Робустфасистиматион

Пространство имен: [Microsoft. тактов. charactering](xref:Microsoft.Quantum.Characterization)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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



## <a name="remarks"></a>Комментарии

В ограничении большого количества запросов Cramer-Rao нижние границы для стандартного отклонения от оценки $ \фи $ удовлетворяет $ \сигма \же 2 \пи/\текст{# запросов} $.

## <a name="references"></a>Ссылки

- Надежная калибровка универсального Single-Qubit Gate-Set с помощью надежной оценки этапа Шелби Киммел, Guang Хао Low, текста книги J. Йодер https://arxiv.org/abs/1502.02677