---
uid: Microsoft.Quantum.Simulation.TrotterSimulationAlgorithm
title: Функция Троттерсимулатионалгорисм
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TrotterSimulationAlgorithm
qsharp.summary: '`SimulationAlgorithm` function that uses a Trotter–Suzuki decomposition to approximate the time-evolution operator _exp(-iHt)_.'
ms.openlocfilehash: b2cc9c29cbb40809540d143fcefd7cb0838bfea7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847786"
---
# <a name="trottersimulationalgorithm-function"></a><span data-ttu-id="5d67a-102">Функция Троттерсимулатионалгорисм</span><span class="sxs-lookup"><span data-stu-id="5d67a-102">TrotterSimulationAlgorithm function</span></span>

<span data-ttu-id="5d67a-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="5d67a-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="5d67a-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5d67a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5d67a-105">`SimulationAlgorithm` функция, использующая декомпозицию Троттер – Сузуки для приближения оператора времени _(-ИХТ)_.</span><span class="sxs-lookup"><span data-stu-id="5d67a-105">`SimulationAlgorithm` function that uses a Trotter–Suzuki decomposition to approximate the time-evolution operator _exp(-iHt)_.</span></span>

```qsharp
function TrotterSimulationAlgorithm (trotterStepSize : Double, trotterOrder : Int) : Microsoft.Quantum.Simulation.SimulationAlgorithm
```


## <a name="input"></a><span data-ttu-id="5d67a-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5d67a-106">Input</span></span>

### <a name="trotterstepsize--double"></a><span data-ttu-id="5d67a-107">Троттерстепсизе: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5d67a-107">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="5d67a-108">Продолжительность имитации времени — развитие в одном Троттер шаге.</span><span class="sxs-lookup"><span data-stu-id="5d67a-108">Duration of simulated time-evolution in single Trotter step.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="5d67a-109">Троттерордер: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5d67a-109">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5d67a-110">Порядок Троттер интегратора.</span><span class="sxs-lookup"><span data-stu-id="5d67a-110">Order of Trotter integrator.</span></span> <span data-ttu-id="5d67a-111">Это должно быть либо 1, либо четное число.</span><span class="sxs-lookup"><span data-stu-id="5d67a-111">This must be either 1 or an even number.</span></span>



## <a name="output--simulationalgorithm"></a><span data-ttu-id="5d67a-112">Выходные данные: [симулатионалгорисм](xref:Microsoft.Quantum.Simulation.SimulationAlgorithm)</span><span class="sxs-lookup"><span data-stu-id="5d67a-112">Output : [SimulationAlgorithm](xref:Microsoft.Quantum.Simulation.SimulationAlgorithm)</span></span>

<span data-ttu-id="5d67a-113">Тип `SimulationAlgorithm`.</span><span class="sxs-lookup"><span data-stu-id="5d67a-113">A `SimulationAlgorithm` type.</span></span>