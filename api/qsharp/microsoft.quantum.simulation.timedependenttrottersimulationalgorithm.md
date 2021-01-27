---
uid: Microsoft.Quantum.Simulation.TimeDependentTrotterSimulationAlgorithm
title: Функция Тимедепенденттроттерсимулатионалгорисм
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TimeDependentTrotterSimulationAlgorithm
qsharp.summary: '`TimeDependentSimulationAlgorithm` function that uses a Trotter–Suzuki decomposition to approximate a unitary operator that solves the time-dependent Schrodinger equation.'
ms.openlocfilehash: c827dd79af6f4b745adf8903ed2664d9e8255785
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858359"
---
# <a name="timedependenttrottersimulationalgorithm-function"></a><span data-ttu-id="c53b1-102">Функция Тимедепенденттроттерсимулатионалгорисм</span><span class="sxs-lookup"><span data-stu-id="c53b1-102">TimeDependentTrotterSimulationAlgorithm function</span></span>

<span data-ttu-id="c53b1-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="c53b1-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="c53b1-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c53b1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c53b1-105">`TimeDependentSimulationAlgorithm` функция, использующая декомпозицию Троттер – Сузуки для приближения единого оператора, который решает, зависящее от времени Счродинжер уравнение.</span><span class="sxs-lookup"><span data-stu-id="c53b1-105">`TimeDependentSimulationAlgorithm` function that uses a Trotter–Suzuki decomposition to approximate a unitary operator that solves the time-dependent Schrodinger equation.</span></span>

```qsharp
function TimeDependentTrotterSimulationAlgorithm (trotterStepSize : Double, trotterOrder : Int) : Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm
```


## <a name="input"></a><span data-ttu-id="c53b1-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c53b1-106">Input</span></span>

### <a name="trotterstepsize--double"></a><span data-ttu-id="c53b1-107">Троттерстепсизе: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="c53b1-107">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="c53b1-108">Продолжительность имитации времени — развитие в одном Троттер шаге.</span><span class="sxs-lookup"><span data-stu-id="c53b1-108">Duration of simulated time-evolution in single Trotter step.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="c53b1-109">Троттерордер: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c53b1-109">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c53b1-110">Порядок Троттер интегратора.</span><span class="sxs-lookup"><span data-stu-id="c53b1-110">Order of Trotter integrator.</span></span> <span data-ttu-id="c53b1-111">Это должно быть либо 1, либо четное число.</span><span class="sxs-lookup"><span data-stu-id="c53b1-111">This must be either 1 or an even number.</span></span>



## <a name="output--timedependentsimulationalgorithm"></a><span data-ttu-id="c53b1-112">Выходные данные: [тимедепендентсимулатионалгорисм](xref:Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm)</span><span class="sxs-lookup"><span data-stu-id="c53b1-112">Output : [TimeDependentSimulationAlgorithm](xref:Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm)</span></span>

<span data-ttu-id="c53b1-113">Тип `TimeDependentSimulationAlgorithm`.</span><span class="sxs-lookup"><span data-stu-id="c53b1-113">A `TimeDependentSimulationAlgorithm` type.</span></span>