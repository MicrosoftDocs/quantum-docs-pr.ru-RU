---
uid: Microsoft.Quantum.Simulation.EvolutionSet
title: Определяемый пользователем тип эволюционных данных
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EvolutionSet
qsharp.summary: >-
  Represents a set of gates that can be readily implemented and used to implement simulation algorithms.

  Elements in the set are indexed by a  <xref:microsoft.quantum.simulation.generatorindex>, and each set is described by a function from `GeneratorIndex` to  <xref:microsoft.quantum.simulation.evolutionunitary>, which are operations parameterized by a real number representing time
ms.openlocfilehash: 35c0b24da284a5871fd11b6d624102b853b89d19
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856072"
---
# <a name="evolutionset-user-defined-type"></a>Определяемый пользователем тип эволюционных данных

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Представляет набор шлюзов, которые можно легко реализовать и использовать для реализации алгоритмов моделирования.

Элементы в наборе индексируются по  <xref:microsoft.quantum.simulation.generatorindex> , а каждый набор описывается функцией из `GeneratorIndex` в  <xref:microsoft.quantum.simulation.evolutionunitary> , что представляет собой операции, параметризованные вещественным числом, представляющим время.

```qsharp

newtype EvolutionSet = ((Microsoft.Quantum.Simulation.GeneratorIndex -> Microsoft.Quantum.Simulation.EvolutionUnitary));
```

