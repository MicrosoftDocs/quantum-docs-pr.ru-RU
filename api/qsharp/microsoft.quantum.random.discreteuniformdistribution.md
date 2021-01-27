---
uid: Microsoft.Quantum.Random.DiscreteUniformDistribution
title: Функция Дискретеуниформдистрибутион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DiscreteUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive range.
ms.openlocfilehash: f909e7def5439ec0feef4ca4dc0cf8ed12374dfe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853718"
---
# <a name="discreteuniformdistribution-function"></a><span data-ttu-id="3ac95-102">Функция Дискретеуниформдистрибутион</span><span class="sxs-lookup"><span data-stu-id="3ac95-102">DiscreteUniformDistribution function</span></span>

<span data-ttu-id="3ac95-103">Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="3ac95-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="3ac95-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="3ac95-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="3ac95-105">Возвращает равномерное распределение по заданному инклюзивному диапазону.</span><span class="sxs-lookup"><span data-stu-id="3ac95-105">Returns a uniform distribution over a given inclusive range.</span></span>

```qsharp
function DiscreteUniformDistribution (min : Int, max : Int) : Microsoft.Quantum.Random.DiscreteDistribution
```


## <a name="input"></a><span data-ttu-id="3ac95-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="3ac95-106">Input</span></span>

### <a name="min--int"></a><span data-ttu-id="3ac95-107">min: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3ac95-107">min : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3ac95-108">Наименьшее целое число для рисования.</span><span class="sxs-lookup"><span data-stu-id="3ac95-108">The smallest integer to be drawn.</span></span>


### <a name="max--int"></a><span data-ttu-id="3ac95-109">Max: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3ac95-109">max : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3ac95-110">Максимальное отображаемое целое число.</span><span class="sxs-lookup"><span data-stu-id="3ac95-110">The largest integer to be drawn.</span></span>



## <a name="output--discretedistribution"></a><span data-ttu-id="3ac95-111">Выходные данные: [дискретедистрибутион](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span><span class="sxs-lookup"><span data-stu-id="3ac95-111">Output : [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span></span>

<span data-ttu-id="3ac95-112">Распределение, случайные вариатес которых являются целыми числами в диапазоне от `min` до `max` с равномерным значением вероятности.</span><span class="sxs-lookup"><span data-stu-id="3ac95-112">A distribution whose random variates are integers in the inclusive range from `min` to `max` with uniform probability.</span></span>

## <a name="example"></a><span data-ttu-id="3ac95-113">Пример</span><span class="sxs-lookup"><span data-stu-id="3ac95-113">Example</span></span>

<span data-ttu-id="3ac95-114">Следующий фрагмент Q # случайным образом выполняет откат шести костей:</span><span class="sxs-lookup"><span data-stu-id="3ac95-114">The following Q# snippet randomly rolls a six-sided die:</span></span>

```qsharp
let dieDistribution = DiscreteUniformDistribution(1, 6);
let dieRoll = dieDistribution::Sample();
```

## <a name="remarks"></a><span data-ttu-id="3ac95-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="3ac95-115">Remarks</span></span>

<span data-ttu-id="3ac95-116">Завершается ошибкой `max <= min` , если.</span><span class="sxs-lookup"><span data-stu-id="3ac95-116">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="3ac95-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="3ac95-117">See Also</span></span>

- [<span data-ttu-id="3ac95-118">Microsoft. тактов. Драврандомдаубле</span><span class="sxs-lookup"><span data-stu-id="3ac95-118">Microsoft.Quantum.DrawRandomDouble</span></span>](xref:Microsoft.Quantum.DrawRandomDouble)