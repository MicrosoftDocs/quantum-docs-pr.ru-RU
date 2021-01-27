---
uid: Microsoft.Quantum.Simulation.InterpolatedEvolution
title: Функция Интерполатедеволутион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: InterpolatedEvolution
qsharp.summary: Interpolates between two generators with a uniform schedule, returning an operation that applies simulated evolution under the resulting time-dependent generator to a qubit register.
ms.openlocfilehash: 4d2e04513c96c6e5f41e85f1df685e91e2973098
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858094"
---
# <a name="interpolatedevolution-function"></a><span data-ttu-id="49989-102">Функция Интерполатедеволутион</span><span class="sxs-lookup"><span data-stu-id="49989-102">InterpolatedEvolution function</span></span>

<span data-ttu-id="49989-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="49989-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="49989-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="49989-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="49989-105">Выполняет интерполяцию между двумя генераторами с единым расписанием, возвращая операцию, которая применяет смоделированное развитие в рамках генератора, зависящего от времени, к кубит регистру.</span><span class="sxs-lookup"><span data-stu-id="49989-105">Interpolates between two generators with a uniform schedule, returning an operation that applies simulated evolution under the resulting time-dependent generator to a qubit register.</span></span>

```qsharp
function InterpolatedEvolution (interpolationTime : Double, evolutionGeneratorStart : Microsoft.Quantum.Simulation.EvolutionGenerator, evolutionGeneratorEnd : Microsoft.Quantum.Simulation.EvolutionGenerator, timeDependentSimulationAlgorithm : Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="49989-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="49989-106">Input</span></span>

### <a name="interpolationtime--double"></a><span data-ttu-id="49989-107">Интерполатионтиме: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="49989-107">interpolationTime : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="49989-108">Время для выполнения интерполяции.</span><span class="sxs-lookup"><span data-stu-id="49989-108">Time to perform the interpolation over.</span></span>


### <a name="evolutiongeneratorstart--evolutiongenerator"></a><span data-ttu-id="49989-109">Еволутионженераторстарт: [еволутионженератор](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span><span class="sxs-lookup"><span data-stu-id="49989-109">evolutionGeneratorStart : [EvolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span></span>

<span data-ttu-id="49989-110">Начальный генератор для моделирования развития.</span><span class="sxs-lookup"><span data-stu-id="49989-110">Initial generator to simulate evolution under.</span></span>


### <a name="evolutiongeneratorend--evolutiongenerator"></a><span data-ttu-id="49989-111">Еволутионженераторенд: [еволутионженератор](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span><span class="sxs-lookup"><span data-stu-id="49989-111">evolutionGeneratorEnd : [EvolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span></span>

<span data-ttu-id="49989-112">Окончательный генератор для моделирования развития.</span><span class="sxs-lookup"><span data-stu-id="49989-112">Final generator to simulate evolution under.</span></span>


### <a name="timedependentsimulationalgorithm--timedependentsimulationalgorithm"></a><span data-ttu-id="49989-113">Тимедепендентсимулатионалгорисм: [тимедепендентсимулатионалгорисм](xref:Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm)</span><span class="sxs-lookup"><span data-stu-id="49989-113">timeDependentSimulationAlgorithm : [TimeDependentSimulationAlgorithm](xref:Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm)</span></span>

<span data-ttu-id="49989-114">Алгоритм моделирования, зависящий от времени, который будет использоваться для моделирования развития во время единообразия расписания интерполяции.</span><span class="sxs-lookup"><span data-stu-id="49989-114">A time-dependent simulation algorithm that will be used to simulate evolution during the uniform interpolation schedule.</span></span>



## <a name="output--qubit--unit--is-adj--ctl"></a><span data-ttu-id="49989-115">Выходные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица измерения](xref:microsoft.quantum.lang-ref.unit)  ">" + CTL</span><span class="sxs-lookup"><span data-stu-id="49989-115">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>



## <a name="remarks"></a><span data-ttu-id="49989-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="49989-116">Remarks</span></span>

<span data-ttu-id="49989-117">Если время интерполяции выбрано в соответствии с условиями адиабатик, эта функция возвращает операцию, которая выполняет подготовку адиабатик State для финального динамического генератора.</span><span class="sxs-lookup"><span data-stu-id="49989-117">If the interpolation time is chosen to meet the adiabatic conditions, then this function returns an operation which performs adiabatic state preparation for the final dynamical generator.</span></span>