---
uid: Microsoft.Quantum.Simulation.GeneratorIndex
title: Определяемый пользователем тип Женераториндекс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GeneratorIndex
qsharp.summary: >-
  Represents a single primitive term in the set of all dynamical generators, e.g. Hermitian operators, for which there exists a map from that generator to time-evolution by that generator, through `EvolutionSet`.

  The first element (Int[], Double[]) is indexes that single term -- For instance, the Pauli string XXY with coefficient 0.5 would be indexed by ([1,1,2], [0.5]). Alternatively, Hamiltonians parameterized by a continuous variable, such as X cos φ + Y sin φ, might for instance be represented by ([], [φ]). The second element indexes the subsystem on which the generator acts on.
ms.openlocfilehash: 8d36f74fbf122469e9e829b950e4ed9a6e3a35a7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733161"
---
# <a name="generatorindex-user-defined-type"></a><span data-ttu-id="dc084-102">Определяемый пользователем тип Женераториндекс</span><span class="sxs-lookup"><span data-stu-id="dc084-102">GeneratorIndex user defined type</span></span>

<span data-ttu-id="dc084-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="dc084-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="dc084-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="dc084-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="dc084-105">Представляет один примитивный термин в наборе всех динамических генераторов, например операторы Хермитиан, для которых существует соответствие от этого генератора до времени развития этого генератора с помощью `EvolutionSet` .</span><span class="sxs-lookup"><span data-stu-id="dc084-105">Represents a single primitive term in the set of all dynamical generators, e.g. Hermitian operators, for which there exists a map from that generator to time-evolution by that generator, through `EvolutionSet`.</span></span>

<span data-ttu-id="dc084-106">Первый элемент (int [], double []) — это индексы, в которых один термин — например, Паули строка КСКСИ с коэффициентом 0,5 будет индексироваться по ([1, 1, 2], [0,5]).</span><span class="sxs-lookup"><span data-stu-id="dc084-106">The first element (Int[], Double[]) is indexes that single term -- For instance, the Pauli string XXY with coefficient 0.5 would be indexed by ([1,1,2], [0.5]).</span></span> <span data-ttu-id="dc084-107">Кроме того, Хамилтонианс, параметризованный с помощью непрерывной переменной, например X cos φ + Y Sin φ, может представлять экземпляр ([], [φ]).</span><span class="sxs-lookup"><span data-stu-id="dc084-107">Alternatively, Hamiltonians parameterized by a continuous variable, such as X cos φ + Y sin φ, might for instance be represented by ([], [φ]).</span></span> <span data-ttu-id="dc084-108">Второй элемент индексирует подсистему, в которой работает генератор.</span><span class="sxs-lookup"><span data-stu-id="dc084-108">The second element indexes the subsystem on which the generator acts on.</span></span>

```qsharp

newtype GeneratorIndex = ((Int[], Double[]), Int[]);
```



## <a name="remarks"></a><span data-ttu-id="dc084-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="dc084-109">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="dc084-110">Интерпретация `GeneratorIndex` не определена, за исключением ссылки на конкретный набор генераторов.</span><span class="sxs-lookup"><span data-stu-id="dc084-110">The interpretation of an `GeneratorIndex` is not defined except with reference to a particular set of generators.</span></span>

## <a name="see-also"></a><span data-ttu-id="dc084-111">См. также:</span><span class="sxs-lookup"><span data-stu-id="dc084-111">See Also</span></span>

- [<span data-ttu-id="dc084-112">Microsoft. тактов. моделирование. эволюционный</span><span class="sxs-lookup"><span data-stu-id="dc084-112">Microsoft.Quantum.Simulation.EvolutionSet</span></span>](xref:Microsoft.Quantum.Simulation.EvolutionSet)
- [<span data-ttu-id="dc084-113">Microsoft. тактов. моделирование. Паулиеволутионсет</span><span class="sxs-lookup"><span data-stu-id="dc084-113">Microsoft.Quantum.Simulation.PauliEvolutionSet</span></span>](xref:Microsoft.Quantum.Simulation.PauliEvolutionSet)