---
uid: Microsoft.Quantum.Simulation.TimeDependentTrotterSimulationAlgorithmImpl
title: Операция Тимедепенденттроттерсимулатионалгорисмимпл
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TimeDependentTrotterSimulationAlgorithmImpl
qsharp.summary: Implementation of multiple Trotter steps to approximate a unitary operator that solves the time-dependent Schrödinger equation.
ms.openlocfilehash: f4f8a9265dc25305819da5ae1002f02b7efd1952
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203456"
---
# <a name="timedependenttrottersimulationalgorithmimpl-operation"></a>Операция Тимедепенденттроттерсимулатионалгорисмимпл

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Реализация нескольких Троттер шагов для приблизительного оператора, который решает Шредингер формулу, зависящую от времени.

```qsharp
operation TimeDependentTrotterSimulationAlgorithmImpl (trotterStepSize : Double, trotterOrder : Int, maxTime : Double, evolutionSchedule : Microsoft.Quantum.Simulation.EvolutionSchedule, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="trotterstepsize--double"></a>Троттерстепсизе: [Double](xref:microsoft.quantum.lang-ref.double)

Продолжительность имитации времени — развитие в одном Троттер шаге.


### <a name="trotterorder--int"></a>Троттерордер: [int](xref:microsoft.quantum.lang-ref.int)

Порядок Троттер интегратора. Это должно быть либо 1, либо четное число.


### <a name="maxtime--double"></a>Макстиме: [Double](xref:microsoft.quantum.lang-ref.double)

Общая продолжительность имитации $t $.


### <a name="evolutionschedule--evolutionschedule"></a>Еволутионсчедуле: [еволутионсчедуле](xref:Microsoft.Quantum.Simulation.EvolutionSchedule)

Полное описание зависящей от времени системы для имитации.


### <a name="qubits--qubit"></a>Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Кубитс в соответствии с эмуляцией.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

