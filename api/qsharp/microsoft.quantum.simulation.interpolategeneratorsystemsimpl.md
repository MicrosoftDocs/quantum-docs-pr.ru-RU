---
uid: Microsoft.Quantum.Simulation.InterpolateGeneratorSystemsImpl
title: Функция Интерполатеженераторсистемсимпл
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: InterpolateGeneratorSystemsImpl
qsharp.summary: Linearly interpolates between two `GeneratorSystems` according to a schedule parameter `s` between 0 and 1 (inclusive).
ms.openlocfilehash: 212ed4c473fab3572f73ea250061057ad13e393f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709434"
---
# <a name="interpolategeneratorsystemsimpl-function"></a><span data-ttu-id="488c7-102">Функция Интерполатеженераторсистемсимпл</span><span class="sxs-lookup"><span data-stu-id="488c7-102">InterpolateGeneratorSystemsImpl function</span></span>

<span data-ttu-id="488c7-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="488c7-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="488c7-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="488c7-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="488c7-105">Линейная интерполяция между двумя в `GeneratorSystems` соответствии с параметром расписания `s` от 0 до 1 (включительно).</span><span class="sxs-lookup"><span data-stu-id="488c7-105">Linearly interpolates between two `GeneratorSystems` according to a schedule parameter `s` between 0 and 1 (inclusive).</span></span>

```qsharp
function InterpolateGeneratorSystemsImpl (schedule : Double, generatorSystemStart : Microsoft.Quantum.Simulation.GeneratorSystem, generatorSystemEnd : Microsoft.Quantum.Simulation.GeneratorSystem) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="488c7-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="488c7-106">Input</span></span>

### <a name="schedule--double"></a><span data-ttu-id="488c7-107">Расписание: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="488c7-107">schedule : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="488c7-108">Параметр расписания $s \ин [0, 1] $.</span><span class="sxs-lookup"><span data-stu-id="488c7-108">A schedule parameter $s\in[0,1]$.</span></span>


### <a name="generatorsystemstart--generatorsystem"></a><span data-ttu-id="488c7-109">Женераторсистемстарт: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="488c7-109">generatorSystemStart : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="488c7-110">Начало `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="488c7-110">The start `GeneratorSystem`.</span></span>


### <a name="generatorsystemend--generatorsystem"></a><span data-ttu-id="488c7-111">Женераторсистеменд: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="488c7-111">generatorSystemEnd : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="488c7-112">Конец `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="488c7-112">The end `GeneratorSystem`.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="488c7-113">Выходные данные: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="488c7-113">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="488c7-114">Объект, `GeneratorSystem` представляющий систему, которая является суммой систем генератора входных данных с весовым коэффициентом $ (1-s) $ ON `generatorSystemStart` и весом $s $ On `generatorSystemEnd` .</span><span class="sxs-lookup"><span data-stu-id="488c7-114">A `GeneratorSystem` representing a system that is the sum of the input generator systems, with weight $(1-s)$ on `generatorSystemStart` and weight $s$ on `generatorSystemEnd`.</span></span>

## <a name="see-also"></a><span data-ttu-id="488c7-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="488c7-115">See Also</span></span>

- [<span data-ttu-id="488c7-116">Microsoft. тактов. моделирование. Женераторсистем</span><span class="sxs-lookup"><span data-stu-id="488c7-116">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)