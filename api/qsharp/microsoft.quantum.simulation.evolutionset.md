---
uid: Microsoft.Quantum.Simulation.EvolutionSet
title: Определяемый пользователем тип эволюционных данных
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EvolutionSet
qsharp.summary: >-
  Represents a set of gates that can be readily implemented and used to implement simulation algorithms.

  Elements in the set are indexed by a  <xref:microsoft.quantum.simulation.generatorindex>, and each set is described by a function from `GeneratorIndex` to  <xref:microsoft.quantum.simulation.evolutionunitary>, which are operations parameterized by a real number representing time
ms.openlocfilehash: 41504837b281b1021a2d09ef75acc10315b4fd07
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710610"
---
# <a name="evolutionset-user-defined-type"></a>Определяемый пользователем тип эволюционных данных

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакеты [](https://nuget.org/packages/)


Представляет набор шлюзов, которые можно легко реализовать и использовать для реализации алгоритмов моделирования.

Элементы в наборе индексируются по  <xref:microsoft.quantum.simulation.generatorindex> , а каждый набор описывается функцией из `GeneratorIndex` в  <xref:microsoft.quantum.simulation.evolutionunitary> , что представляет собой операции, параметризованные вещественным числом, представляющим время.

```qsharp

newtype EvolutionSet = ((Microsoft.Quantum.Simulation.GeneratorIndex -> Microsoft.Quantum.Simulation.EvolutionUnitary));
```

