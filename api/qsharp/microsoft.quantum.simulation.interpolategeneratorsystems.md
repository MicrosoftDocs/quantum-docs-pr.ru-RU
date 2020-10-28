---
uid: Microsoft.Quantum.Simulation.InterpolateGeneratorSystems
title: Функция Интерполатеженераторсистемс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: InterpolateGeneratorSystems
qsharp.summary: Returns a `TimeDependentGeneratorSystem` representing the linear interpolation between two `GeneratorSystem`s.
ms.openlocfilehash: 9881c27577023dafff0bfc6d961877db44fec0eb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710567"
---
# <a name="interpolategeneratorsystems-function"></a><span data-ttu-id="0faf6-102">Функция Интерполатеженераторсистемс</span><span class="sxs-lookup"><span data-stu-id="0faf6-102">InterpolateGeneratorSystems function</span></span>

<span data-ttu-id="0faf6-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="0faf6-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="0faf6-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0faf6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0faf6-105">Возвращает значение, `TimeDependentGeneratorSystem` представляющее линейную интерполяцию между двумя `GeneratorSystem` s.</span><span class="sxs-lookup"><span data-stu-id="0faf6-105">Returns a `TimeDependentGeneratorSystem` representing the linear interpolation between two `GeneratorSystem`s.</span></span>

```qsharp
function InterpolateGeneratorSystems (generatorSystemStart : Microsoft.Quantum.Simulation.GeneratorSystem, generatorSystemEnd : Microsoft.Quantum.Simulation.GeneratorSystem) : Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem
```


## <a name="input"></a><span data-ttu-id="0faf6-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="0faf6-106">Input</span></span>

### <a name="generatorsystemstart--generatorsystem"></a><span data-ttu-id="0faf6-107">Женераторсистемстарт: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="0faf6-107">generatorSystemStart : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="0faf6-108">Начало `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="0faf6-108">The start `GeneratorSystem`.</span></span>


### <a name="generatorsystemend--generatorsystem"></a><span data-ttu-id="0faf6-109">Женераторсистеменд: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="0faf6-109">generatorSystemEnd : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="0faf6-110">Конец `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="0faf6-110">The end `GeneratorSystem`.</span></span>



## <a name="output--timedependentgeneratorsystem"></a><span data-ttu-id="0faf6-111">Выходные данные: [тимедепендентженераторсистем](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="0faf6-111">Output : [TimeDependentGeneratorSystem](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)</span></span>

<span data-ttu-id="0faf6-112">Объект, `TimeDependentGeneratorSystem` представляющий систему, которая является суммой систем генератора входных данных с весовым коэффициентом $ (1-s) $ ON `generatorSystemStart` и весом $s $ On `generatorSystemEnd` .</span><span class="sxs-lookup"><span data-stu-id="0faf6-112">A `TimeDependentGeneratorSystem` representing a system that is the sum of the input generator systems, with weight $(1-s)$ on `generatorSystemStart` and weight $s$ on `generatorSystemEnd`.</span></span>

## <a name="see-also"></a><span data-ttu-id="0faf6-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="0faf6-113">See Also</span></span>

- [<span data-ttu-id="0faf6-114">Microsoft. тактов. моделирование. Женераторсистем</span><span class="sxs-lookup"><span data-stu-id="0faf6-114">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)
- [<span data-ttu-id="0faf6-115">Microsoft. тактов. моделирование. Тимедепендентженераторсистем</span><span class="sxs-lookup"><span data-stu-id="0faf6-115">Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)