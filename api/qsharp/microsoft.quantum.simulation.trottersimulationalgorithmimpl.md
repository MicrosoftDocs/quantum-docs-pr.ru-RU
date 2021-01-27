---
uid: Microsoft.Quantum.Simulation.TrotterSimulationAlgorithmImpl
title: Операция Троттерсимулатионалгорисмимпл
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TrotterSimulationAlgorithmImpl
qsharp.summary: Makes repeated calls to `TrotterStep` to approximate the time-evolution operator exp(_-iHt_).
ms.openlocfilehash: b2411950b90eb676b1da53bd06bde648099e2db4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858888"
---
# <a name="trottersimulationalgorithmimpl-operation"></a><span data-ttu-id="61654-102">Операция Троттерсимулатионалгорисмимпл</span><span class="sxs-lookup"><span data-stu-id="61654-102">TrotterSimulationAlgorithmImpl operation</span></span>

<span data-ttu-id="61654-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="61654-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="61654-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="61654-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="61654-105">Выполняет повторяющиеся вызовы для `TrotterStep` приблизительного оператора времени ожидания (_-ИХТ_).</span><span class="sxs-lookup"><span data-stu-id="61654-105">Makes repeated calls to `TrotterStep` to approximate the time-evolution operator exp(_-iHt_).</span></span>

```qsharp
operation TrotterSimulationAlgorithmImpl (trotterStepSize : Double, trotterOrder : Int, maxTime : Double, evolutionGenerator : Microsoft.Quantum.Simulation.EvolutionGenerator, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="61654-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="61654-106">Input</span></span>

### <a name="trotterstepsize--double"></a><span data-ttu-id="61654-107">Троттерстепсизе: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="61654-107">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="61654-108">Продолжительность имитации времени — развитие в одном Троттер шаге.</span><span class="sxs-lookup"><span data-stu-id="61654-108">Duration of simulated time-evolution in single Trotter step.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="61654-109">Троттерордер: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="61654-109">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="61654-110">Порядок Троттер интегратора.</span><span class="sxs-lookup"><span data-stu-id="61654-110">Order of Trotter integrator.</span></span> <span data-ttu-id="61654-111">Это должно быть либо 1, либо четное число.</span><span class="sxs-lookup"><span data-stu-id="61654-111">This must be either 1 or an even number.</span></span>


### <a name="maxtime--double"></a><span data-ttu-id="61654-112">Макстиме: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="61654-112">maxTime : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="61654-113">Общая продолжительность имитации $t $.</span><span class="sxs-lookup"><span data-stu-id="61654-113">Total duration of simulation $t$.</span></span>


### <a name="evolutiongenerator--evolutiongenerator"></a><span data-ttu-id="61654-114">Еволутионженератор: [еволутионженератор](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span><span class="sxs-lookup"><span data-stu-id="61654-114">evolutionGenerator : [EvolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span></span>

<span data-ttu-id="61654-115">Полное описание системы для имитации.</span><span class="sxs-lookup"><span data-stu-id="61654-115">A complete description of the system to be simulated.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="61654-116">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="61654-116">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="61654-117">Кубитс в соответствии с эмуляцией.</span><span class="sxs-lookup"><span data-stu-id="61654-117">Qubits acted on by simulation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="61654-118">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="61654-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

