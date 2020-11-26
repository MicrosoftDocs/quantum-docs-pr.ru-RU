---
uid: Microsoft.Quantum.Random.ContinuousUniformDistribution
title: Функция Континуаусуниформдистрибутион
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: ContinuousUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive interval.
ms.openlocfilehash: a3911fe9962ce18daa239de0272c53d83344134a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193086"
---
# <a name="continuousuniformdistribution-function"></a><span data-ttu-id="de7d8-102">Функция Континуаусуниформдистрибутион</span><span class="sxs-lookup"><span data-stu-id="de7d8-102">ContinuousUniformDistribution function</span></span>

<span data-ttu-id="de7d8-103">Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="de7d8-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="de7d8-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="de7d8-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="de7d8-105">Возвращает равномерное распределение по заданному инклюзивному интервалу.</span><span class="sxs-lookup"><span data-stu-id="de7d8-105">Returns a uniform distribution over a given inclusive interval.</span></span>

```qsharp
function ContinuousUniformDistribution (min : Double, max : Double) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a><span data-ttu-id="de7d8-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="de7d8-106">Input</span></span>

### <a name="min--double"></a><span data-ttu-id="de7d8-107">min: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="de7d8-107">min : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="de7d8-108">Наименьшее вещественное число для рисования.</span><span class="sxs-lookup"><span data-stu-id="de7d8-108">The smallest real number to be drawn.</span></span>


### <a name="max--double"></a><span data-ttu-id="de7d8-109">Max: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="de7d8-109">max : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="de7d8-110">Максимальное вещественное число для рисования.</span><span class="sxs-lookup"><span data-stu-id="de7d8-110">The largest real number to be drawn.</span></span>



## <a name="output--continuousdistribution"></a><span data-ttu-id="de7d8-111">Выходные данные: [континуаусдистрибутион](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="de7d8-111">Output : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>

<span data-ttu-id="de7d8-112">Распределение, случайные вариатес которых являются реальными числами в инклюзивном интервале от `min` до `max` с равномерным значением вероятности.</span><span class="sxs-lookup"><span data-stu-id="de7d8-112">A distribution whose random variates are real numbers in the inclusive interval from `min` to `max` with uniform probability.</span></span>

## <a name="remarks"></a><span data-ttu-id="de7d8-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="de7d8-113">Remarks</span></span>

<span data-ttu-id="de7d8-114">Завершается ошибкой `max <= min` , если.</span><span class="sxs-lookup"><span data-stu-id="de7d8-114">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="de7d8-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="de7d8-115">See Also</span></span>

- [<span data-ttu-id="de7d8-116">Microsoft. тактов. Драврандомдаубле</span><span class="sxs-lookup"><span data-stu-id="de7d8-116">Microsoft.Quantum.DrawRandomDouble</span></span>](xref:Microsoft.Quantum.DrawRandomDouble)