---
uid: Microsoft.Quantum.Simulation.TrotterStepImpl
title: Операция Троттерстепимпл
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TrotterStepImpl
qsharp.summary: Implements time-evolution by a term contained in a `GeneratorSystem`.
ms.openlocfilehash: bc6c3c6656da319fce9c7c48824dbc4ad75ccc83
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203422"
---
# <a name="trotterstepimpl-operation"></a>Операция Троттерстепимпл

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Реализует развитие времени с помощью термина, содержащегося в `GeneratorSystem` .

```qsharp
operation TrotterStepImpl (evolutionGenerator : Microsoft.Quantum.Simulation.EvolutionGenerator, idx : Int, stepsize : Double, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="evolutiongenerator--evolutiongenerator"></a>Еволутионженератор: [еволутионженератор](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)

Полное описание системы для имитации.


### <a name="idx--int"></a>IDX: [int](xref:microsoft.quantum.lang-ref.int)

Целочисленный индекс для термина в описанной системе.


### <a name="stepsize--double"></a>степсизе: [Double](xref:microsoft.quantum.lang-ref.double)

Множитель в течение времени — развитие по условию, индексированное по `idx` .


### <a name="qubits--qubit"></a>Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Кубитс в соответствии с эмуляцией.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

