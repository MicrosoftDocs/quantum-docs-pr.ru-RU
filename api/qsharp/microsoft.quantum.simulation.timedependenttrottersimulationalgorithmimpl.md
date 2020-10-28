---
uid: Microsoft.Quantum.Simulation.TimeDependentTrotterSimulationAlgorithmImpl
title: Операция Тимедепенденттроттерсимулатионалгорисмимпл
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TimeDependentTrotterSimulationAlgorithmImpl
qsharp.summary: Implementation of multiple Trotter steps to approximate a unitary operator that solves the time-dependent Schrödinger equation.
ms.openlocfilehash: c6d1c976d29c69d3ac14d9a2be09826602c8cc1d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730673"
---
# <a name="timedependenttrottersimulationalgorithmimpl-operation"></a>Операция Тимедепенденттроттерсимулатионалгорисмимпл

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакеты [](https://nuget.org/packages/)


Реализация нескольких Троттер шагов для приблизительного оператора, который решает Шредингер формулу, зависящую от времени.

```qsharp
operation TimeDependentTrotterSimulationAlgorithmImpl (trotterStepSize : Double, trotterOrder : Int, maxTime : Double, evolutionSchedule : Microsoft.Quantum.Simulation.EvolutionSchedule, qubits : Qubit[]) : Unit
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

