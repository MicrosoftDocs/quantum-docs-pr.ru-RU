---
uid: Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm
title: Определяемый пользователем тип Тимедепендентсимулатионалгорисм
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TimeDependentSimulationAlgorithm
qsharp.summary: >-
  Represents a time-dependent simulation algorithm.

  A time-dependent simulation technique converts an <xref:microsoft.quantum.simulation.evolutionschedule> to unitary time-evolution for some time-interval.
ms.openlocfilehash: 9d2a1a853005495b5a9df60ac1f0dcbfbdf7637f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92734217"
---
# <a name="timedependentsimulationalgorithm-user-defined-type"></a><span data-ttu-id="ae356-102">Определяемый пользователем тип Тимедепендентсимулатионалгорисм</span><span class="sxs-lookup"><span data-stu-id="ae356-102">TimeDependentSimulationAlgorithm user defined type</span></span>

<span data-ttu-id="ae356-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="ae356-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="ae356-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ae356-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ae356-105">Представляет алгоритм моделирования, зависящий от времени.</span><span class="sxs-lookup"><span data-stu-id="ae356-105">Represents a time-dependent simulation algorithm.</span></span>

<span data-ttu-id="ae356-106">Метод моделирования, зависящий от времени, преобразует <xref:microsoft.quantum.simulation.evolutionschedule></span><span class="sxs-lookup"><span data-stu-id="ae356-106">A time-dependent simulation technique converts an <xref:microsoft.quantum.simulation.evolutionschedule></span></span>
<span data-ttu-id="ae356-107">на единое время – развитие времени в течение некоторого интервала времени.</span><span class="sxs-lookup"><span data-stu-id="ae356-107">to unitary time-evolution for some time-interval.</span></span>

```qsharp

newtype TimeDependentSimulationAlgorithm = (((Double, Microsoft.Quantum.Simulation.EvolutionSchedule, Qubit[]) => Unit is Adj + Ctl));
```

