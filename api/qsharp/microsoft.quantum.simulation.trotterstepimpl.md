---
uid: Microsoft.Quantum.Simulation.TrotterStepImpl
title: Операция Троттерстепимпл
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TrotterStepImpl
qsharp.summary: Implements time-evolution by a term contained in a `GeneratorSystem`.
ms.openlocfilehash: bc6c3c6656da319fce9c7c48824dbc4ad75ccc83
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203422"
---
# <a name="trotterstepimpl-operation"></a><span data-ttu-id="df3a0-102">Операция Троттерстепимпл</span><span class="sxs-lookup"><span data-stu-id="df3a0-102">TrotterStepImpl operation</span></span>

<span data-ttu-id="df3a0-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="df3a0-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="df3a0-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="df3a0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="df3a0-105">Реализует развитие времени с помощью термина, содержащегося в `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="df3a0-105">Implements time-evolution by a term contained in a `GeneratorSystem`.</span></span>

```qsharp
operation TrotterStepImpl (evolutionGenerator : Microsoft.Quantum.Simulation.EvolutionGenerator, idx : Int, stepsize : Double, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="df3a0-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="df3a0-106">Input</span></span>

### <a name="evolutiongenerator--evolutiongenerator"></a><span data-ttu-id="df3a0-107">Еволутионженератор: [еволутионженератор](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span><span class="sxs-lookup"><span data-stu-id="df3a0-107">evolutionGenerator : [EvolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span></span>

<span data-ttu-id="df3a0-108">Полное описание системы для имитации.</span><span class="sxs-lookup"><span data-stu-id="df3a0-108">A complete description of the system to be simulated.</span></span>


### <a name="idx--int"></a><span data-ttu-id="df3a0-109">IDX: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="df3a0-109">idx : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="df3a0-110">Целочисленный индекс для термина в описанной системе.</span><span class="sxs-lookup"><span data-stu-id="df3a0-110">Integer index to a term in the described system.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="df3a0-111">степсизе: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="df3a0-111">stepsize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="df3a0-112">Множитель в течение времени — развитие по условию, индексированное по `idx` .</span><span class="sxs-lookup"><span data-stu-id="df3a0-112">Multiplier on duration of time-evolution by term indexed by `idx`.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="df3a0-113">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="df3a0-113">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="df3a0-114">Кубитс в соответствии с эмуляцией.</span><span class="sxs-lookup"><span data-stu-id="df3a0-114">Qubits acted on by simulation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="df3a0-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="df3a0-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

