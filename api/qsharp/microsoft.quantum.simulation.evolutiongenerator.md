---
uid: Microsoft.Quantum.Simulation.EvolutionGenerator
title: Определяемый пользователем тип Еволутионженератор
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EvolutionGenerator
qsharp.summary: >-
  Represents a dynamical generator as a set of simulatable gates and an expansion in terms of that basis.

  Last parameter for number of terms.
ms.openlocfilehash: 9e0fc5a232070c238aad943ab73f064999237c15
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229449"
---
# <a name="evolutiongenerator-user-defined-type"></a><span data-ttu-id="6e8e9-102">Определяемый пользователем тип Еволутионженератор</span><span class="sxs-lookup"><span data-stu-id="6e8e9-102">EvolutionGenerator user defined type</span></span>

<span data-ttu-id="6e8e9-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="6e8e9-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="6e8e9-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6e8e9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6e8e9-105">Представляет динамический генератор в виде набора моделирующих шлюзов и расширения с точки зрения этого базиса.</span><span class="sxs-lookup"><span data-stu-id="6e8e9-105">Represents a dynamical generator as a set of simulatable gates and an expansion in terms of that basis.</span></span>

<span data-ttu-id="6e8e9-106">Последний параметр для числа терминов.</span><span class="sxs-lookup"><span data-stu-id="6e8e9-106">Last parameter for number of terms.</span></span>

```qsharp

newtype EvolutionGenerator = (Microsoft.Quantum.Simulation.EvolutionSet, Microsoft.Quantum.Simulation.GeneratorSystem);
```

