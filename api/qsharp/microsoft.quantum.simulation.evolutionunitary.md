---
uid: Microsoft.Quantum.Simulation.EvolutionUnitary
title: Определяемый пользователем тип Еволутионунитари
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EvolutionUnitary
qsharp.summary: >-
  Represents a unitary time-evolution operator.

  The first parameter is is duration of time-evolution, and the second parameter is the qubit register acted upon by the unitary.
ms.openlocfilehash: ea160bb9a0a8bb5106c3e37a6a16155bad71dd25
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856044"
---
# <a name="evolutionunitary-user-defined-type"></a><span data-ttu-id="59acc-102">Определяемый пользователем тип Еволутионунитари</span><span class="sxs-lookup"><span data-stu-id="59acc-102">EvolutionUnitary user defined type</span></span>

<span data-ttu-id="59acc-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="59acc-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="59acc-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="59acc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="59acc-105">Представляет отдельный оператор времени развития.</span><span class="sxs-lookup"><span data-stu-id="59acc-105">Represents a unitary time-evolution operator.</span></span>

<span data-ttu-id="59acc-106">Первый параметр — это длительность развития времени, а второй параметр — кубит регистр, который зависит от единой.</span><span class="sxs-lookup"><span data-stu-id="59acc-106">The first parameter is is duration of time-evolution, and the second parameter is the qubit register acted upon by the unitary.</span></span>

```qsharp

newtype EvolutionUnitary = (((Double, Qubit[]) => Unit is Adj + Ctl));
```

