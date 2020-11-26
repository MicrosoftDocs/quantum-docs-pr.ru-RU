---
uid: Microsoft.Quantum.Characterization.DiscretePhaseEstimationIteration
title: Операция Дискретефасистиматионитератион
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: DiscretePhaseEstimationIteration
qsharp.summary: Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using integer powers of a unitary oracle.
ms.openlocfilehash: 8ce1e1a2bda6507285f055c87619a8760c891082
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204391"
---
# <a name="discretephaseestimationiteration-operation"></a>Операция Дискретефасистиматионитератион

Пространство имен: [Microsoft. тактов. charactering](xref:Microsoft.Quantum.Characterization)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Выполняет одну итерацию итеративного (классического) алгоритма оценки фазы с помощью целочисленных степеней единой Oracle.

```qsharp
operation DiscretePhaseEstimationIteration (oracle : Microsoft.Quantum.Oracles.DiscreteOracle, power : Int, theta : Double, targetState : Qubit[], controlQubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="oracle--discreteoracle"></a>Oracle: [дискретеоракле](xref:Microsoft.Quantum.Oracles.DiscreteOracle)

Операция, выполняемая над целым числом и регистром, например $U ^ m $ применяется к заданному регистру, где $U $ — это единое целое, этап которого должен быть оценен, а $m $ — целочисленная мощность, заданная Oracle


### <a name="power--int"></a>степень: [int](xref:microsoft.quantum.lang-ref.int)

Количество раз, когда применяется заданная Единая база данных Oracle.


### <a name="theta--double"></a>тета: [двойной](xref:microsoft.quantum.lang-ref.double)

Угол, на который следует обратить фазу на элементе управления кубит до того, как он будет действовать в целевом состоянии.


### <a name="targetstate--qubit"></a>Таржетстате: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистрация состояния в зависимости от заданного единого объекта Oracle.


### <a name="controlqubit--qubit"></a>Контролкубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Вспомогательная кубит, используемая для управления приложением данного Oracle.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

