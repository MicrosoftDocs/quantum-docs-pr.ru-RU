---
uid: Microsoft.Quantum.Characterization.ContinuousPhaseEstimationIteration
title: Операция Континуаусфасистиматионитератион
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: ContinuousPhaseEstimationIteration
qsharp.summary: Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using arbitrary real powers of a unitary oracle.
ms.openlocfilehash: 3c0f6cf084311598346b25dd7028e290946cd87f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216291"
---
# <a name="continuousphaseestimationiteration-operation"></a>Операция Континуаусфасистиматионитератион

Пространство имен: [Microsoft. тактов. charactering](xref:Microsoft.Quantum.Characterization)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Выполняет одну итерацию итеративного (классического) алгоритма оценки фазы с использованием произвольных реальных степеней единой системы Oracle.

```qsharp
operation ContinuousPhaseEstimationIteration (oracle : Microsoft.Quantum.Oracles.ContinuousOracle, time : Double, theta : Double, targetState : Qubit[], controlQubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="oracle--continuousoracle"></a>Oracle: [континуаусоракле](xref:Microsoft.Quantum.Oracles.ContinuousOracle)

Операция, работающая с двойным $t $ и регистром, таким, что $U ^ t $ применяется к заданному регистру, где $U $ является единым этапом, который должен быть оценен, а $t $ — целочисленной мощностью, заданной для Oracle


### <a name="time--double"></a>время: [Double](xref:microsoft.quantum.lang-ref.double)

Количество раз, когда применяется заданная Единая база данных Oracle.


### <a name="theta--double"></a>тета: [двойной](xref:microsoft.quantum.lang-ref.double)

Угол, на который следует обратить фазу на элементе управления кубит до того, как он будет действовать в целевом состоянии.


### <a name="targetstate--qubit"></a>Таржетстате: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистрация состояния в зависимости от заданного единого объекта Oracle.


### <a name="controlqubit--qubit"></a>Контролкубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)





## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

