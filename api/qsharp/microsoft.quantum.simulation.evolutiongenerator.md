---
uid: Microsoft.Quantum.Simulation.EvolutionGenerator
title: Определяемый пользователем тип Еволутионженератор
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EvolutionGenerator
qsharp.summary: >-
  Represents a dynamical generator as a set of simulatable gates and an expansion in terms of that basis.

  Last parameter for number of terms.
ms.openlocfilehash: be741216bf99305bf5f1d149c815e98aba36aad1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710637"
---
# <a name="evolutiongenerator-user-defined-type"></a><span data-ttu-id="1423e-102">Определяемый пользователем тип Еволутионженератор</span><span class="sxs-lookup"><span data-stu-id="1423e-102">EvolutionGenerator user defined type</span></span>

<span data-ttu-id="1423e-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="1423e-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="1423e-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1423e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1423e-105">Представляет динамический генератор в виде набора моделирующих шлюзов и расширения с точки зрения этого базиса.</span><span class="sxs-lookup"><span data-stu-id="1423e-105">Represents a dynamical generator as a set of simulatable gates and an expansion in terms of that basis.</span></span>

<span data-ttu-id="1423e-106">Последний параметр для числа терминов.</span><span class="sxs-lookup"><span data-stu-id="1423e-106">Last parameter for number of terms.</span></span>

```qsharp

newtype EvolutionGenerator = (Microsoft.Quantum.Simulation.EvolutionSet, Microsoft.Quantum.Simulation.GeneratorSystem);
```

