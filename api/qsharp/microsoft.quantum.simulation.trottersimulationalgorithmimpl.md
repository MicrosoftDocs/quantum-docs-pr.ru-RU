---
uid: Microsoft.Quantum.Simulation.TrotterSimulationAlgorithmImpl
title: Операция Троттерсимулатионалгорисмимпл
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TrotterSimulationAlgorithmImpl
qsharp.summary: Makes repeated calls to `TrotterStep` to approximate the time-evolution operator exp(_-iHt_).
ms.openlocfilehash: 5b796245e2a4434228260a229cb61be66f3e38d6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203406"
---
# <a name="trottersimulationalgorithmimpl-operation"></a><span data-ttu-id="31534-102">Операция Троттерсимулатионалгорисмимпл</span><span class="sxs-lookup"><span data-stu-id="31534-102">TrotterSimulationAlgorithmImpl operation</span></span>

<span data-ttu-id="31534-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="31534-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="31534-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="31534-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="31534-105">Выполняет повторяющиеся вызовы для `TrotterStep` приблизительного оператора времени ожидания (_-ИХТ_).</span><span class="sxs-lookup"><span data-stu-id="31534-105">Makes repeated calls to `TrotterStep` to approximate the time-evolution operator exp(_-iHt_).</span></span>

```qsharp
operation TrotterSimulationAlgorithmImpl (trotterStepSize : Double, trotterOrder : Int, maxTime : Double, evolutionGenerator : Microsoft.Quantum.Simulation.EvolutionGenerator, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="31534-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="31534-106">Input</span></span>

### <a name="trotterstepsize--double"></a><span data-ttu-id="31534-107">Троттерстепсизе: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="31534-107">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="31534-108">Продолжительность имитации времени — развитие в одном Троттер шаге.</span><span class="sxs-lookup"><span data-stu-id="31534-108">Duration of simulated time-evolution in single Trotter step.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="31534-109">Троттерордер: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="31534-109">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="31534-110">Порядок Троттер интегратора.</span><span class="sxs-lookup"><span data-stu-id="31534-110">Order of Trotter integrator.</span></span> <span data-ttu-id="31534-111">Это должно быть либо 1, либо четное число.</span><span class="sxs-lookup"><span data-stu-id="31534-111">This must be either 1 or an even number.</span></span>


### <a name="maxtime--double"></a><span data-ttu-id="31534-112">Макстиме: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="31534-112">maxTime : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="31534-113">Общая продолжительность имитации $t $.</span><span class="sxs-lookup"><span data-stu-id="31534-113">Total duration of simulation $t$.</span></span>


### <a name="evolutiongenerator--evolutiongenerator"></a><span data-ttu-id="31534-114">Еволутионженератор: [еволутионженератор](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span><span class="sxs-lookup"><span data-stu-id="31534-114">evolutionGenerator : [EvolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span></span>

<span data-ttu-id="31534-115">Полное описание системы для имитации.</span><span class="sxs-lookup"><span data-stu-id="31534-115">A complete description of the system to be simulated.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="31534-116">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="31534-116">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="31534-117">Кубитс в соответствии с эмуляцией.</span><span class="sxs-lookup"><span data-stu-id="31534-117">Qubits acted on by simulation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="31534-118">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="31534-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

