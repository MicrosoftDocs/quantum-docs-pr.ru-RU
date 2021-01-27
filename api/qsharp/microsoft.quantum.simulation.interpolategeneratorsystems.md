---
uid: Microsoft.Quantum.Simulation.InterpolateGeneratorSystems
title: Функция Интерполатеженераторсистемс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: InterpolateGeneratorSystems
qsharp.summary: Returns a `TimeDependentGeneratorSystem` representing the linear interpolation between two `GeneratorSystem`s.
ms.openlocfilehash: c56f1eaf13afb649777c0d9368e97d85996cc67b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842260"
---
# <a name="interpolategeneratorsystems-function"></a><span data-ttu-id="7e8a7-102">Функция Интерполатеженераторсистемс</span><span class="sxs-lookup"><span data-stu-id="7e8a7-102">InterpolateGeneratorSystems function</span></span>

<span data-ttu-id="7e8a7-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="7e8a7-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="7e8a7-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7e8a7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7e8a7-105">Возвращает значение, `TimeDependentGeneratorSystem` представляющее линейную интерполяцию между двумя `GeneratorSystem` s.</span><span class="sxs-lookup"><span data-stu-id="7e8a7-105">Returns a `TimeDependentGeneratorSystem` representing the linear interpolation between two `GeneratorSystem`s.</span></span>

```qsharp
function InterpolateGeneratorSystems (generatorSystemStart : Microsoft.Quantum.Simulation.GeneratorSystem, generatorSystemEnd : Microsoft.Quantum.Simulation.GeneratorSystem) : Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem
```


## <a name="input"></a><span data-ttu-id="7e8a7-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7e8a7-106">Input</span></span>

### <a name="generatorsystemstart--generatorsystem"></a><span data-ttu-id="7e8a7-107">Женераторсистемстарт: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="7e8a7-107">generatorSystemStart : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="7e8a7-108">Начало `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="7e8a7-108">The start `GeneratorSystem`.</span></span>


### <a name="generatorsystemend--generatorsystem"></a><span data-ttu-id="7e8a7-109">Женераторсистеменд: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="7e8a7-109">generatorSystemEnd : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="7e8a7-110">Конец `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="7e8a7-110">The end `GeneratorSystem`.</span></span>



## <a name="output--timedependentgeneratorsystem"></a><span data-ttu-id="7e8a7-111">Выходные данные: [тимедепендентженераторсистем](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="7e8a7-111">Output : [TimeDependentGeneratorSystem](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)</span></span>

<span data-ttu-id="7e8a7-112">Объект, `TimeDependentGeneratorSystem` представляющий систему, которая является суммой систем генератора входных данных с весовым коэффициентом $ (1-s) $ ON `generatorSystemStart` и весом $s $ On `generatorSystemEnd` .</span><span class="sxs-lookup"><span data-stu-id="7e8a7-112">A `TimeDependentGeneratorSystem` representing a system that is the sum of the input generator systems, with weight $(1-s)$ on `generatorSystemStart` and weight $s$ on `generatorSystemEnd`.</span></span>

## <a name="see-also"></a><span data-ttu-id="7e8a7-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="7e8a7-113">See Also</span></span>

- [<span data-ttu-id="7e8a7-114">Microsoft. тактов. моделирование. Женераторсистем</span><span class="sxs-lookup"><span data-stu-id="7e8a7-114">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)
- [<span data-ttu-id="7e8a7-115">Microsoft. тактов. моделирование. Тимедепендентженераторсистем</span><span class="sxs-lookup"><span data-stu-id="7e8a7-115">Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)