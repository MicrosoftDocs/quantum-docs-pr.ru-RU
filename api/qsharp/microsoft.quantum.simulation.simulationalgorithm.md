---
uid: Microsoft.Quantum.Simulation.SimulationAlgorithm
title: Определяемый пользователем тип Симулатионалгорисм
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: SimulationAlgorithm
qsharp.summary: >-
  Represents a time-independent simulation algorithm.

  A time-independent simulation technique converts an <xref:microsoft.quantum.simulation.evolutiongenerator> to unitary time evolution for some time-interval.
ms.openlocfilehash: 9127a936bbf7a212e712645eabdf49fefc7a97d0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92734113"
---
# <a name="simulationalgorithm-user-defined-type"></a><span data-ttu-id="88624-102">Определяемый пользователем тип Симулатионалгорисм</span><span class="sxs-lookup"><span data-stu-id="88624-102">SimulationAlgorithm user defined type</span></span>

<span data-ttu-id="88624-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="88624-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="88624-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="88624-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="88624-105">Представляет алгоритм моделирования, не зависящий от времени.</span><span class="sxs-lookup"><span data-stu-id="88624-105">Represents a time-independent simulation algorithm.</span></span>

<span data-ttu-id="88624-106">Метод моделирования, не зависящий от времени, преобразует <xref:microsoft.quantum.simulation.evolutiongenerator></span><span class="sxs-lookup"><span data-stu-id="88624-106">A time-independent simulation technique converts an <xref:microsoft.quantum.simulation.evolutiongenerator></span></span>
<span data-ttu-id="88624-107">на единое время развития в течение некоторого интервала времени.</span><span class="sxs-lookup"><span data-stu-id="88624-107">to unitary time evolution for some time-interval.</span></span>

```qsharp

newtype SimulationAlgorithm = (((Double, Microsoft.Quantum.Simulation.EvolutionGenerator, Qubit[]) => Unit is Adj + Ctl));
```

