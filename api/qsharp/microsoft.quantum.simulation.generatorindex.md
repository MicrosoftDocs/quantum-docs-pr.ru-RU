---
uid: Microsoft.Quantum.Simulation.GeneratorIndex
title: Определяемый пользователем тип Женераториндекс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GeneratorIndex
qsharp.summary: >-
  Represents a single primitive term in the set of all dynamical generators, e.g. Hermitian operators, for which there exists a map from that generator to time-evolution by that generator, through `EvolutionSet`.

  The first element (Int[], Double[]) is indexes that single term -- For instance, the Pauli string XXY with coefficient 0.5 would be indexed by ([1,1,2], [0.5]). Alternatively, Hamiltonians parameterized by a continuous variable, such as X cos φ + Y sin φ, might for instance be represented by ([], [φ]). The second element indexes the subsystem on which the generator acts on.
ms.openlocfilehash: 762dac81ea0963443f0338cea1b879856c84b0ff
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858379"
---
# <a name="generatorindex-user-defined-type"></a><span data-ttu-id="d6795-102">Определяемый пользователем тип Женераториндекс</span><span class="sxs-lookup"><span data-stu-id="d6795-102">GeneratorIndex user defined type</span></span>

<span data-ttu-id="d6795-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="d6795-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="d6795-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d6795-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d6795-105">Представляет один примитивный термин в наборе всех динамических генераторов, например операторы Хермитиан, для которых существует соответствие от этого генератора до времени развития этого генератора с помощью `EvolutionSet` .</span><span class="sxs-lookup"><span data-stu-id="d6795-105">Represents a single primitive term in the set of all dynamical generators, e.g. Hermitian operators, for which there exists a map from that generator to time-evolution by that generator, through `EvolutionSet`.</span></span>

<span data-ttu-id="d6795-106">Первый элемент (int [], double []) — это индексы, в которых один термин — например, Паули строка КСКСИ с коэффициентом 0,5 будет индексироваться по ([1, 1, 2], [0,5]).</span><span class="sxs-lookup"><span data-stu-id="d6795-106">The first element (Int[], Double[]) is indexes that single term -- For instance, the Pauli string XXY with coefficient 0.5 would be indexed by ([1,1,2], [0.5]).</span></span> <span data-ttu-id="d6795-107">Кроме того, Хамилтонианс, параметризованный с помощью непрерывной переменной, например X cos φ + Y Sin φ, может представлять экземпляр ([], [φ]).</span><span class="sxs-lookup"><span data-stu-id="d6795-107">Alternatively, Hamiltonians parameterized by a continuous variable, such as X cos φ + Y sin φ, might for instance be represented by ([], [φ]).</span></span> <span data-ttu-id="d6795-108">Второй элемент индексирует подсистему, в которой работает генератор.</span><span class="sxs-lookup"><span data-stu-id="d6795-108">The second element indexes the subsystem on which the generator acts on.</span></span>

```qsharp

newtype GeneratorIndex = ((Int[], Double[]), Int[]);
```



## <a name="example"></a><span data-ttu-id="d6795-109">Пример</span><span class="sxs-lookup"><span data-stu-id="d6795-109">Example</span></span>

<span data-ttu-id="d6795-110">С помощью  <xref:microsoft.quantum.simulation.paulievolutionset> оператор $ \пи X_2 X_5 Y_9 $ представляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d6795-110">Using  <xref:microsoft.quantum.simulation.paulievolutionset>, the operator $\pi X_2 X_5 Y_9$ is represented as:</span></span>

```qsharp
let index = GeneratorIndex(([1, 1, 2], [PI()]), [2, 5, 9]);
```

## <a name="remarks"></a><span data-ttu-id="d6795-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="d6795-111">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="d6795-112">Интерпретация `GeneratorIndex` не определена, за исключением ссылки на конкретный набор генераторов.</span><span class="sxs-lookup"><span data-stu-id="d6795-112">The interpretation of an `GeneratorIndex` is not defined except with reference to a particular set of generators.</span></span>

## <a name="see-also"></a><span data-ttu-id="d6795-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="d6795-113">See Also</span></span>

- [<span data-ttu-id="d6795-114">Microsoft. тактов. моделирование. эволюционный</span><span class="sxs-lookup"><span data-stu-id="d6795-114">Microsoft.Quantum.Simulation.EvolutionSet</span></span>](xref:Microsoft.Quantum.Simulation.EvolutionSet)
- [<span data-ttu-id="d6795-115">Microsoft. тактов. моделирование. Паулиеволутионсет</span><span class="sxs-lookup"><span data-stu-id="d6795-115">Microsoft.Quantum.Simulation.PauliEvolutionSet</span></span>](xref:Microsoft.Quantum.Simulation.PauliEvolutionSet)