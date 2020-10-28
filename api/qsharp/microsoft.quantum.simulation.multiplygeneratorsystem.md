---
uid: Microsoft.Quantum.Simulation.MultiplyGeneratorSystem
title: Функция Мултиплиженераторсистем
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: MultiplyGeneratorSystem
qsharp.summary: Multiplies the coefficient of all terms in a `GeneratorSystem`.
ms.openlocfilehash: 1d28de99dab3f7aca4bf3706fe98f5ef7c5286a7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730928"
---
# <a name="multiplygeneratorsystem-function"></a><span data-ttu-id="18a69-102">Функция Мултиплиженераторсистем</span><span class="sxs-lookup"><span data-stu-id="18a69-102">MultiplyGeneratorSystem function</span></span>

<span data-ttu-id="18a69-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="18a69-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="18a69-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="18a69-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="18a69-105">Умножает коэффициент всех терминов в `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="18a69-105">Multiplies the coefficient of all terms in a `GeneratorSystem`.</span></span>

```qsharp
function MultiplyGeneratorSystem (multiplier : Double, generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="18a69-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="18a69-106">Input</span></span>

### <a name="multiplier--double"></a><span data-ttu-id="18a69-107">множитель: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="18a69-107">multiplier : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="18a69-108">Коэффициент коэффициента.</span><span class="sxs-lookup"><span data-stu-id="18a69-108">The multiplier on the coefficient.</span></span>


### <a name="generatorsystem--generatorsystem"></a><span data-ttu-id="18a69-109">Женераторсистем: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="18a69-109">generatorSystem : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="18a69-110">Умножаемый `GeneratorSystem`.</span><span class="sxs-lookup"><span data-stu-id="18a69-110">The `GeneratorSystem` to be multiplied.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="18a69-111">Выходные данные: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="18a69-111">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="18a69-112">Объект, `GeneratorSystem` представляющий систему с коэффициентами `multiplier` увеличения.</span><span class="sxs-lookup"><span data-stu-id="18a69-112">A `GeneratorSystem` representing a system with coefficients a factor `multiplier` larger.</span></span>

## <a name="see-also"></a><span data-ttu-id="18a69-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="18a69-113">See Also</span></span>

- [<span data-ttu-id="18a69-114">Microsoft. тактов. моделирование. Женераторсистем</span><span class="sxs-lookup"><span data-stu-id="18a69-114">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)