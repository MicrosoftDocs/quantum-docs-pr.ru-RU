---
uid: Microsoft.Quantum.Simulation.TimeDependentTrotterSimulationAlgorithmImpl
title: Операция Тимедепенденттроттерсимулатионалгорисмимпл
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TimeDependentTrotterSimulationAlgorithmImpl
qsharp.summary: Implementation of multiple Trotter steps to approximate a unitary operator that solves the time-dependent Schrödinger equation.
ms.openlocfilehash: c6d1c976d29c69d3ac14d9a2be09826602c8cc1d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730673"
---
# <a name="timedependenttrottersimulationalgorithmimpl-operation"></a><span data-ttu-id="1698c-102">Операция Тимедепенденттроттерсимулатионалгорисмимпл</span><span class="sxs-lookup"><span data-stu-id="1698c-102">TimeDependentTrotterSimulationAlgorithmImpl operation</span></span>

<span data-ttu-id="1698c-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="1698c-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="1698c-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1698c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1698c-105">Реализация нескольких Троттер шагов для приблизительного оператора, который решает Шредингер формулу, зависящую от времени.</span><span class="sxs-lookup"><span data-stu-id="1698c-105">Implementation of multiple Trotter steps to approximate a unitary operator that solves the time-dependent Schrödinger equation.</span></span>

```qsharp
operation TimeDependentTrotterSimulationAlgorithmImpl (trotterStepSize : Double, trotterOrder : Int, maxTime : Double, evolutionSchedule : Microsoft.Quantum.Simulation.EvolutionSchedule, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="1698c-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="1698c-106">Input</span></span>

### <a name="trotterstepsize--double"></a><span data-ttu-id="1698c-107">Троттерстепсизе: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="1698c-107">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="1698c-108">Продолжительность имитации времени — развитие в одном Троттер шаге.</span><span class="sxs-lookup"><span data-stu-id="1698c-108">Duration of simulated time-evolution in single Trotter step.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="1698c-109">Троттерордер: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1698c-109">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="1698c-110">Порядок Троттер интегратора.</span><span class="sxs-lookup"><span data-stu-id="1698c-110">Order of Trotter integrator.</span></span> <span data-ttu-id="1698c-111">Это должно быть либо 1, либо четное число.</span><span class="sxs-lookup"><span data-stu-id="1698c-111">This must be either 1 or an even number.</span></span>


### <a name="maxtime--double"></a><span data-ttu-id="1698c-112">Макстиме: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="1698c-112">maxTime : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="1698c-113">Общая продолжительность имитации $t $.</span><span class="sxs-lookup"><span data-stu-id="1698c-113">Total duration of simulation $t$.</span></span>


### <a name="evolutionschedule--evolutionschedule"></a><span data-ttu-id="1698c-114">Еволутионсчедуле: [еволутионсчедуле](xref:Microsoft.Quantum.Simulation.EvolutionSchedule)</span><span class="sxs-lookup"><span data-stu-id="1698c-114">evolutionSchedule : [EvolutionSchedule](xref:Microsoft.Quantum.Simulation.EvolutionSchedule)</span></span>

<span data-ttu-id="1698c-115">Полное описание зависящей от времени системы для имитации.</span><span class="sxs-lookup"><span data-stu-id="1698c-115">A complete description of the time-dependent system to be simulated.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="1698c-116">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="1698c-116">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="1698c-117">Кубитс в соответствии с эмуляцией.</span><span class="sxs-lookup"><span data-stu-id="1698c-117">Qubits acted on by simulation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1698c-118">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1698c-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

