---
uid: Microsoft.Quantum.Characterization.QuantumPhaseEstimation
title: Операция Куантумфасистиматион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: QuantumPhaseEstimation
qsharp.summary: Performs the quantum phase estimation algorithm for a given oracle `U` and `targetState`, reading the phase into a big-endian quantum register.
ms.openlocfilehash: 4bdf3de9dab20fa97ba47f15efec4b41a10709f3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839659"
---
# <a name="quantumphaseestimation-operation"></a>Операция Куантумфасистиматион

Пространство имен: [Microsoft. тактов. charactering](xref:Microsoft.Quantum.Characterization)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Выполняет алгоритм оценки тактовой фазы для заданного Oracle `U` и `targetState` считывает его в реестр такта с обратным порядком байтов.

```qsharp
operation QuantumPhaseEstimation (oracle : Microsoft.Quantum.Oracles.DiscreteOracle, targetState : Qubit[], controlRegister : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="oracle--discreteoracle"></a>Oracle: [дискретеоракле](xref:Microsoft.Quantum.Oracles.DiscreteOracle)

Операция, реализующая $U ^ m $ для данного целого числа степеней m.


### <a name="targetstate--qubit"></a>Таржетстате: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистр такта, представляющий состояние $ \кет{\фи} $ в соответствии с $U $. Если $ \кет{\фи} $ является еиженстате $U $, $U \кет{\фи} = e ^ {и\фи} \кет{\фи} $ for $ \фи \ин [0, 2 \ PI) $ Неизвестный этап.


### <a name="controlregister--bigendian"></a>Контролрегистер: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian)

Регистр целых чисел с обратным порядком байтов, который может использоваться для управления предоставленной базой данных Oracle и будет содержать представление $ \фи $ после применения этой операции. Предполагается, что Контролрегистер начинается в начальном состоянии $ \ket{00\cdots 0} $, где длина регистра указывает требуемую точность.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

