---
uid: Microsoft.Quantum.Simulation.TimeDependentTrotterSimulationAlgorithm
title: Функция Тимедепенденттроттерсимулатионалгорисм
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TimeDependentTrotterSimulationAlgorithm
qsharp.summary: '`TimeDependentSimulationAlgorithm` function that uses a Trotter–Suzuki decomposition to approximate a unitary operator that solves the time-dependent Schrodinger equation.'
ms.openlocfilehash: 94bc606fdc46d77e8beb1470c78102a63e6d4e81
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192780"
---
# <a name="timedependenttrottersimulationalgorithm-function"></a><span data-ttu-id="45de5-102">Функция Тимедепенденттроттерсимулатионалгорисм</span><span class="sxs-lookup"><span data-stu-id="45de5-102">TimeDependentTrotterSimulationAlgorithm function</span></span>

<span data-ttu-id="45de5-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="45de5-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="45de5-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="45de5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="45de5-105">`TimeDependentSimulationAlgorithm` функция, использующая декомпозицию Троттер – Сузуки для приближения единого оператора, который решает, зависящее от времени Счродинжер уравнение.</span><span class="sxs-lookup"><span data-stu-id="45de5-105">`TimeDependentSimulationAlgorithm` function that uses a Trotter–Suzuki decomposition to approximate a unitary operator that solves the time-dependent Schrodinger equation.</span></span>

```qsharp
function TimeDependentTrotterSimulationAlgorithm (trotterStepSize : Double, trotterOrder : Int) : Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm
```


## <a name="input"></a><span data-ttu-id="45de5-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="45de5-106">Input</span></span>

### <a name="trotterstepsize--double"></a><span data-ttu-id="45de5-107">Троттерстепсизе: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="45de5-107">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="45de5-108">Продолжительность имитации времени — развитие в одном Троттер шаге.</span><span class="sxs-lookup"><span data-stu-id="45de5-108">Duration of simulated time-evolution in single Trotter step.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="45de5-109">Троттерордер: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="45de5-109">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="45de5-110">Порядок Троттер интегратора.</span><span class="sxs-lookup"><span data-stu-id="45de5-110">Order of Trotter integrator.</span></span> <span data-ttu-id="45de5-111">Это должно быть либо 1, либо четное число.</span><span class="sxs-lookup"><span data-stu-id="45de5-111">This must be either 1 or an even number.</span></span>



## <a name="output--timedependentsimulationalgorithm"></a><span data-ttu-id="45de5-112">Выходные данные: [тимедепендентсимулатионалгорисм](xref:Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm)</span><span class="sxs-lookup"><span data-stu-id="45de5-112">Output : [TimeDependentSimulationAlgorithm](xref:Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm)</span></span>

<span data-ttu-id="45de5-113">Тип `TimeDependentSimulationAlgorithm`.</span><span class="sxs-lookup"><span data-stu-id="45de5-113">A `TimeDependentSimulationAlgorithm` type.</span></span>