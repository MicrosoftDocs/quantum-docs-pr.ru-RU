---
uid: Microsoft.Quantum.Simulation.TrotterSimulationAlgorithmImpl
title: Операция Троттерсимулатионалгорисмимпл
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TrotterSimulationAlgorithmImpl
qsharp.summary: Makes repeated calls to `TrotterStep` to approximate the time-evolution operator exp(_-iHt_).
ms.openlocfilehash: 2af68532d700a1fb5b037707ce4650696cbe1a64
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733993"
---
# <a name="trottersimulationalgorithmimpl-operation"></a><span data-ttu-id="0555b-102">Операция Троттерсимулатионалгорисмимпл</span><span class="sxs-lookup"><span data-stu-id="0555b-102">TrotterSimulationAlgorithmImpl operation</span></span>

<span data-ttu-id="0555b-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="0555b-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="0555b-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0555b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0555b-105">Выполняет повторяющиеся вызовы для `TrotterStep` приблизительного оператора времени ожидания ( _-ИХТ_ ).</span><span class="sxs-lookup"><span data-stu-id="0555b-105">Makes repeated calls to `TrotterStep` to approximate the time-evolution operator exp( _-iHt_ ).</span></span>

```qsharp
operation TrotterSimulationAlgorithmImpl (trotterStepSize : Double, trotterOrder : Int, maxTime : Double, evolutionGenerator : Microsoft.Quantum.Simulation.EvolutionGenerator, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="0555b-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="0555b-106">Input</span></span>

### <a name="trotterstepsize--double"></a><span data-ttu-id="0555b-107">Троттерстепсизе: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="0555b-107">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="0555b-108">Продолжительность имитации времени — развитие в одном Троттер шаге.</span><span class="sxs-lookup"><span data-stu-id="0555b-108">Duration of simulated time-evolution in single Trotter step.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="0555b-109">Троттерордер: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0555b-109">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0555b-110">Порядок Троттер интегратора.</span><span class="sxs-lookup"><span data-stu-id="0555b-110">Order of Trotter integrator.</span></span> <span data-ttu-id="0555b-111">Это должно быть либо 1, либо четное число.</span><span class="sxs-lookup"><span data-stu-id="0555b-111">This must be either 1 or an even number.</span></span>


### <a name="maxtime--double"></a><span data-ttu-id="0555b-112">Макстиме: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="0555b-112">maxTime : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="0555b-113">Общая продолжительность имитации $t $.</span><span class="sxs-lookup"><span data-stu-id="0555b-113">Total duration of simulation $t$.</span></span>


### <a name="evolutiongenerator--evolutiongenerator"></a><span data-ttu-id="0555b-114">Еволутионженератор: [еволутионженератор](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span><span class="sxs-lookup"><span data-stu-id="0555b-114">evolutionGenerator : [EvolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span></span>

<span data-ttu-id="0555b-115">Полное описание системы для имитации.</span><span class="sxs-lookup"><span data-stu-id="0555b-115">A complete description of the system to be simulated.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="0555b-116">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="0555b-116">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="0555b-117">Кубитс в соответствии с эмуляцией.</span><span class="sxs-lookup"><span data-stu-id="0555b-117">Qubits acted on by simulation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0555b-118">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0555b-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

