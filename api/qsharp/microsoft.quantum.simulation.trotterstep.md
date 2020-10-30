---
uid: Microsoft.Quantum.Simulation.TrotterStep
title: Функция Троттерстеп
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TrotterStep
qsharp.summary: Implements a single time-step of time-evolution by the system described in an `EvolutionGenerator` using a Trotter–Suzuki decomposition.
ms.openlocfilehash: 7a1a27ba4dc4b8b7bbc4da6a378d4a1494bc9415
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733992"
---
# <a name="trotterstep-function"></a><span data-ttu-id="51e11-102">Функция Троттерстеп</span><span class="sxs-lookup"><span data-stu-id="51e11-102">TrotterStep function</span></span>

<span data-ttu-id="51e11-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="51e11-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="51e11-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="51e11-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="51e11-105">Реализует однократный шаг за пределом времени с помощью системы, описанной в `EvolutionGenerator` с использованием декомпозиции Троттер – Сузуки.</span><span class="sxs-lookup"><span data-stu-id="51e11-105">Implements a single time-step of time-evolution by the system described in an `EvolutionGenerator` using a Trotter–Suzuki decomposition.</span></span>

```qsharp
function TrotterStep (evolutionGenerator : Microsoft.Quantum.Simulation.EvolutionGenerator, trotterOrder : Int, trotterStepSize : Double) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="51e11-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="51e11-106">Input</span></span>

### <a name="evolutiongenerator--evolutiongenerator"></a><span data-ttu-id="51e11-107">Еволутионженератор: [еволутионженератор](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span><span class="sxs-lookup"><span data-stu-id="51e11-107">evolutionGenerator : [EvolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span></span>

<span data-ttu-id="51e11-108">Полное описание системы для имитации.</span><span class="sxs-lookup"><span data-stu-id="51e11-108">A complete description of the system to be simulated.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="51e11-109">Троттерордер: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="51e11-109">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="51e11-110">Порядок Троттер интегратора.</span><span class="sxs-lookup"><span data-stu-id="51e11-110">Order of Trotter integrator.</span></span> <span data-ttu-id="51e11-111">Это должно быть либо 1, либо четное число.</span><span class="sxs-lookup"><span data-stu-id="51e11-111">This must be either 1 or an even number.</span></span>


### <a name="trotterstepsize--double"></a><span data-ttu-id="51e11-112">Троттерстепсизе: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="51e11-112">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="51e11-113">Продолжительность имитации времени — развитие в одном Троттер шаге.</span><span class="sxs-lookup"><span data-stu-id="51e11-113">Duration of simulated time-evolution in single Trotter step.</span></span>



## <a name="output--qubit--unit-adj--ctl"></a><span data-ttu-id="51e11-114">Выходные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] => [единицы измерения](xref:microsoft.quantum.lang-ref.unit) + CTL</span><span class="sxs-lookup"><span data-stu-id="51e11-114">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="51e11-115">Единая операция, которая приблизительно составляет один шаг времени — развитие длительности `trotterStepSize` .</span><span class="sxs-lookup"><span data-stu-id="51e11-115">Unitary operation that approximates a single step of time-evolution for duration `trotterStepSize`.</span></span>

## <a name="remarks"></a><span data-ttu-id="51e11-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="51e11-116">Remarks</span></span>

<span data-ttu-id="51e11-117">Дополнительные сведения о декомпозиции Троттер – Сузуки см. в разделе [упорядочение по времени](/quantum/libraries/control-flow#time-ordered-composition).</span><span class="sxs-lookup"><span data-stu-id="51e11-117">For more on the Trotter–Suzuki decomposition, see [Time-Ordered Composition](/quantum/libraries/control-flow#time-ordered-composition).</span></span>