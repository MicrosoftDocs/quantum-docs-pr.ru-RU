---
uid: Microsoft.Quantum.Simulation.InterpolateGeneratorSystemsImpl
title: Функция Интерполатеженераторсистемсимпл
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: InterpolateGeneratorSystemsImpl
qsharp.summary: Linearly interpolates between two `GeneratorSystems` according to a schedule parameter `s` between 0 and 1 (inclusive).
ms.openlocfilehash: a902a93968d221349f9a6fa977bbc1706971fcfd
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855767"
---
# <a name="interpolategeneratorsystemsimpl-function"></a><span data-ttu-id="544f2-102">Функция Интерполатеженераторсистемсимпл</span><span class="sxs-lookup"><span data-stu-id="544f2-102">InterpolateGeneratorSystemsImpl function</span></span>

<span data-ttu-id="544f2-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="544f2-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="544f2-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="544f2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="544f2-105">Линейная интерполяция между двумя в `GeneratorSystems` соответствии с параметром расписания `s` от 0 до 1 (включительно).</span><span class="sxs-lookup"><span data-stu-id="544f2-105">Linearly interpolates between two `GeneratorSystems` according to a schedule parameter `s` between 0 and 1 (inclusive).</span></span>

```qsharp
function InterpolateGeneratorSystemsImpl (schedule : Double, generatorSystemStart : Microsoft.Quantum.Simulation.GeneratorSystem, generatorSystemEnd : Microsoft.Quantum.Simulation.GeneratorSystem) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="544f2-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="544f2-106">Input</span></span>

### <a name="schedule--double"></a><span data-ttu-id="544f2-107">Расписание: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="544f2-107">schedule : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="544f2-108">Параметр расписания $s \ин [0, 1] $.</span><span class="sxs-lookup"><span data-stu-id="544f2-108">A schedule parameter $s\in[0,1]$.</span></span>


### <a name="generatorsystemstart--generatorsystem"></a><span data-ttu-id="544f2-109">Женераторсистемстарт: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="544f2-109">generatorSystemStart : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="544f2-110">Начало `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="544f2-110">The start `GeneratorSystem`.</span></span>


### <a name="generatorsystemend--generatorsystem"></a><span data-ttu-id="544f2-111">Женераторсистеменд: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="544f2-111">generatorSystemEnd : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="544f2-112">Конец `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="544f2-112">The end `GeneratorSystem`.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="544f2-113">Выходные данные: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="544f2-113">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="544f2-114">Объект, `GeneratorSystem` представляющий систему, которая является суммой систем генератора входных данных с весовым коэффициентом $ (1-s) $ ON `generatorSystemStart` и весом $s $ On `generatorSystemEnd` .</span><span class="sxs-lookup"><span data-stu-id="544f2-114">A `GeneratorSystem` representing a system that is the sum of the input generator systems, with weight $(1-s)$ on `generatorSystemStart` and weight $s$ on `generatorSystemEnd`.</span></span>

## <a name="see-also"></a><span data-ttu-id="544f2-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="544f2-115">See Also</span></span>

- [<span data-ttu-id="544f2-116">Microsoft. тактов. моделирование. Женераторсистем</span><span class="sxs-lookup"><span data-stu-id="544f2-116">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)