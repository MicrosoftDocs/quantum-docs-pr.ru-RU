---
uid: Microsoft.Quantum.Simulation.MultiplyGeneratorSystem
title: Функция Мултиплиженераторсистем
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: MultiplyGeneratorSystem
qsharp.summary: Multiplies the coefficient of all terms in a `GeneratorSystem`.
ms.openlocfilehash: effb9e3ca754f77bbe1ea0fb6ca30ae49e92d531
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229160"
---
# <a name="multiplygeneratorsystem-function"></a><span data-ttu-id="ff67b-102">Функция Мултиплиженераторсистем</span><span class="sxs-lookup"><span data-stu-id="ff67b-102">MultiplyGeneratorSystem function</span></span>

<span data-ttu-id="ff67b-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="ff67b-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="ff67b-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ff67b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ff67b-105">Умножает коэффициент всех терминов в `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="ff67b-105">Multiplies the coefficient of all terms in a `GeneratorSystem`.</span></span>

```qsharp
function MultiplyGeneratorSystem (multiplier : Double, generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="ff67b-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ff67b-106">Input</span></span>

### <a name="multiplier--double"></a><span data-ttu-id="ff67b-107">множитель: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ff67b-107">multiplier : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="ff67b-108">Коэффициент коэффициента.</span><span class="sxs-lookup"><span data-stu-id="ff67b-108">The multiplier on the coefficient.</span></span>


### <a name="generatorsystem--generatorsystem"></a><span data-ttu-id="ff67b-109">Женераторсистем: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="ff67b-109">generatorSystem : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="ff67b-110">Умножаемый `GeneratorSystem`.</span><span class="sxs-lookup"><span data-stu-id="ff67b-110">The `GeneratorSystem` to be multiplied.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="ff67b-111">Выходные данные: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="ff67b-111">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="ff67b-112">Объект, `GeneratorSystem` представляющий систему с коэффициентами `multiplier` увеличения.</span><span class="sxs-lookup"><span data-stu-id="ff67b-112">A `GeneratorSystem` representing a system with coefficients a factor `multiplier` larger.</span></span>

## <a name="see-also"></a><span data-ttu-id="ff67b-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="ff67b-113">See Also</span></span>

- [<span data-ttu-id="ff67b-114">Microsoft. тактов. моделирование. Женераторсистем</span><span class="sxs-lookup"><span data-stu-id="ff67b-114">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)