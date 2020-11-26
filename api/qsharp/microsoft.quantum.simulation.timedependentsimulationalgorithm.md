---
uid: Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm
title: Определяемый пользователем тип Тимедепендентсимулатионалгорисм
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TimeDependentSimulationAlgorithm
qsharp.summary: >-
  Represents a time-dependent simulation algorithm.

  A time-dependent simulation technique converts an <xref:microsoft.quantum.simulation.evolutionschedule> to unitary time-evolution for some time-interval.
ms.openlocfilehash: b495a9fd96c78872f84e8f8183105f6290f70655
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192525"
---
# <a name="timedependentsimulationalgorithm-user-defined-type"></a>Определяемый пользователем тип Тимедепендентсимулатионалгорисм

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Представляет алгоритм моделирования, зависящий от времени.

Метод моделирования, зависящий от времени, преобразует <xref:microsoft.quantum.simulation.evolutionschedule>
на единое время – развитие времени в течение некоторого интервала времени.

```qsharp

newtype TimeDependentSimulationAlgorithm = (((Double, Microsoft.Quantum.Simulation.EvolutionSchedule, Qubit[]) => Unit is Adj + Ctl));
```

