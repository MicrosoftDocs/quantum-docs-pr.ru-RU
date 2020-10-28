---
uid: Microsoft.Quantum.Random.ContinuousUniformDistribution
title: Функция Континуаусуниформдистрибутион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: ContinuousUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive interval.
ms.openlocfilehash: 74300efb10ba7b5aa006f0b1b6aafde0da840f00
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709433"
---
# <a name="continuousuniformdistribution-function"></a><span data-ttu-id="4f3cb-102">Функция Континуаусуниформдистрибутион</span><span class="sxs-lookup"><span data-stu-id="4f3cb-102">ContinuousUniformDistribution function</span></span>

<span data-ttu-id="4f3cb-103">Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="4f3cb-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="4f3cb-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4f3cb-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4f3cb-105">Возвращает равномерное распределение по заданному инклюзивному интервалу.</span><span class="sxs-lookup"><span data-stu-id="4f3cb-105">Returns a uniform distribution over a given inclusive interval.</span></span>

```qsharp
function ContinuousUniformDistribution (min : Double, max : Double) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a><span data-ttu-id="4f3cb-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="4f3cb-106">Input</span></span>

### <a name="min--double"></a><span data-ttu-id="4f3cb-107">min: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="4f3cb-107">min : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="4f3cb-108">Наименьшее вещественное число для рисования.</span><span class="sxs-lookup"><span data-stu-id="4f3cb-108">The smallest real number to be drawn.</span></span>


### <a name="max--double"></a><span data-ttu-id="4f3cb-109">Max: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="4f3cb-109">max : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="4f3cb-110">Максимальное вещественное число для рисования.</span><span class="sxs-lookup"><span data-stu-id="4f3cb-110">The largest real number to be drawn.</span></span>



## <a name="output--continuousdistribution"></a><span data-ttu-id="4f3cb-111">Выходные данные: [континуаусдистрибутион](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="4f3cb-111">Output : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>

<span data-ttu-id="4f3cb-112">Распределение, случайные вариатес которых являются реальными числами в инклюзивном интервале от `min` до `max` с равномерным значением вероятности.</span><span class="sxs-lookup"><span data-stu-id="4f3cb-112">A distribution whose random variates are real numbers in the inclusive interval from `min` to `max` with uniform probability.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f3cb-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="4f3cb-113">Remarks</span></span>

<span data-ttu-id="4f3cb-114">Завершается ошибкой `max <= min` , если.</span><span class="sxs-lookup"><span data-stu-id="4f3cb-114">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="4f3cb-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="4f3cb-115">See Also</span></span>

- [<span data-ttu-id="4f3cb-116">Microsoft. тактов. Драврандомдаубле</span><span class="sxs-lookup"><span data-stu-id="4f3cb-116">Microsoft.Quantum.DrawRandomDouble</span></span>](xref:Microsoft.Quantum.DrawRandomDouble)