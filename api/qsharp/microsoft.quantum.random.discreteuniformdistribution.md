---
uid: Microsoft.Quantum.Random.DiscreteUniformDistribution
title: Функция Дискретеуниформдистрибутион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DiscreteUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive range.
ms.openlocfilehash: 5e93c66d891d9b6aec548c0cf266df35e6090c92
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730968"
---
# <a name="discreteuniformdistribution-function"></a><span data-ttu-id="d63c0-102">Функция Дискретеуниформдистрибутион</span><span class="sxs-lookup"><span data-stu-id="d63c0-102">DiscreteUniformDistribution function</span></span>

<span data-ttu-id="d63c0-103">Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="d63c0-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="d63c0-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d63c0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d63c0-105">Возвращает равномерное распределение по заданному инклюзивному диапазону.</span><span class="sxs-lookup"><span data-stu-id="d63c0-105">Returns a uniform distribution over a given inclusive range.</span></span>

```qsharp
function DiscreteUniformDistribution (min : Int, max : Int) : Microsoft.Quantum.Random.DiscreteDistribution
```


## <a name="input"></a><span data-ttu-id="d63c0-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d63c0-106">Input</span></span>

### <a name="min--int"></a><span data-ttu-id="d63c0-107">min: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d63c0-107">min : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d63c0-108">Наименьшее целое число для рисования.</span><span class="sxs-lookup"><span data-stu-id="d63c0-108">The smallest integer to be drawn.</span></span>


### <a name="max--int"></a><span data-ttu-id="d63c0-109">Max: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d63c0-109">max : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d63c0-110">Максимальное отображаемое целое число.</span><span class="sxs-lookup"><span data-stu-id="d63c0-110">The largest integer to be drawn.</span></span>



## <a name="output--discretedistribution"></a><span data-ttu-id="d63c0-111">Выходные данные: [дискретедистрибутион](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span><span class="sxs-lookup"><span data-stu-id="d63c0-111">Output : [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span></span>

<span data-ttu-id="d63c0-112">Распределение, случайные вариатес которых являются целыми числами в диапазоне от `min` до `max` с равномерным значением вероятности.</span><span class="sxs-lookup"><span data-stu-id="d63c0-112">A distribution whose random variates are integers in the inclusive range from `min` to `max` with uniform probability.</span></span>

## <a name="remarks"></a><span data-ttu-id="d63c0-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="d63c0-113">Remarks</span></span>

<span data-ttu-id="d63c0-114">Завершается ошибкой `max <= min` , если.</span><span class="sxs-lookup"><span data-stu-id="d63c0-114">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="d63c0-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="d63c0-115">See Also</span></span>

- [<span data-ttu-id="d63c0-116">Microsoft. тактов. Драврандомдаубле</span><span class="sxs-lookup"><span data-stu-id="d63c0-116">Microsoft.Quantum.DrawRandomDouble</span></span>](xref:Microsoft.Quantum.DrawRandomDouble)