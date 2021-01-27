---
uid: Microsoft.Quantum.Simulation.MultiplyGeneratorIndex
title: Функция Мултиплиженераториндекс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: MultiplyGeneratorIndex
qsharp.summary: Multiplies the coefficient in a `GeneratorIndex`.
ms.openlocfilehash: b53a483a0c2b8c99b733c9c87289fb212b5ffc89
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848035"
---
# <a name="multiplygeneratorindex-function"></a><span data-ttu-id="bb647-102">Функция Мултиплиженераториндекс</span><span class="sxs-lookup"><span data-stu-id="bb647-102">MultiplyGeneratorIndex function</span></span>

<span data-ttu-id="bb647-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="bb647-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="bb647-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bb647-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bb647-105">Умножает коэффициент в `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="bb647-105">Multiplies the coefficient in a `GeneratorIndex`.</span></span>

```qsharp
function MultiplyGeneratorIndex (multiplier : Double, generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a><span data-ttu-id="bb647-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="bb647-106">Input</span></span>

### <a name="multiplier--double"></a><span data-ttu-id="bb647-107">множитель: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="bb647-107">multiplier : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="bb647-108">Коэффициент коэффициента.</span><span class="sxs-lookup"><span data-stu-id="bb647-108">The multiplier on the coefficient.</span></span>


### <a name="generatorindex--generatorindex"></a><span data-ttu-id="bb647-109">Женераториндекс: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="bb647-109">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="bb647-110">Умножаемый `GeneratorIndex`.</span><span class="sxs-lookup"><span data-stu-id="bb647-110">The `GeneratorIndex` to be multiplied.</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="bb647-111">Выходные данные: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="bb647-111">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="bb647-112">Объект, `GeneratorIndex` представляющий термин с коэффициентом, который `multiplier` больше.</span><span class="sxs-lookup"><span data-stu-id="bb647-112">A `GeneratorIndex` representing a term with coefficient a factor `multiplier` larger.</span></span>

## <a name="example"></a><span data-ttu-id="bb647-113">Пример</span><span class="sxs-lookup"><span data-stu-id="bb647-113">Example</span></span>

```qsharp
let gen = GeneratorIndex(([1,2,3],[coeff]),[1,2,3]);
let ((idxPaulis, idxDoubles), idxQubits) = MultiplyGeneratorIndex(multiplier, gen);
// idxDoubles[0] == multiplier * coeff;
```

## <a name="see-also"></a><span data-ttu-id="bb647-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="bb647-114">See Also</span></span>

- [<span data-ttu-id="bb647-115">Microsoft. тактов. моделирование. Женераториндекс</span><span class="sxs-lookup"><span data-stu-id="bb647-115">Microsoft.Quantum.Simulation.GeneratorIndex</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorIndex)