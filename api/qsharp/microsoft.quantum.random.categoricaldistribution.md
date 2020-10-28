---
uid: Microsoft.Quantum.Random.CategoricalDistribution
title: Функция Категорикалдистрибутион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: CategoricalDistribution
qsharp.summary: Returns a discrete categorical distribution, in which the probability for each of a finite list of given outcomes is explicitly specified.
ms.openlocfilehash: 756e9e95cac5554ab8f885dab7c47ac1b174c0f3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732544"
---
# <a name="categoricaldistribution-function"></a><span data-ttu-id="f8472-102">Функция Категорикалдистрибутион</span><span class="sxs-lookup"><span data-stu-id="f8472-102">CategoricalDistribution function</span></span>

<span data-ttu-id="f8472-103">Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="f8472-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="f8472-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f8472-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f8472-105">Возвращает дискретное распределение по категориям, в котором явно задана вероятность для каждого конечного списка заданных результатов.</span><span class="sxs-lookup"><span data-stu-id="f8472-105">Returns a discrete categorical distribution, in which the probability for each of a finite list of given outcomes is explicitly specified.</span></span>

```qsharp
function CategoricalDistribution (probs : Double[]) : Microsoft.Quantum.Random.DiscreteDistribution
```


## <a name="input"></a><span data-ttu-id="f8472-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f8472-106">Input</span></span>

### <a name="probs--double"></a><span data-ttu-id="f8472-107">пробс: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="f8472-107">probs : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="f8472-108">Вероятности для каждого результата из распределения по категориям.</span><span class="sxs-lookup"><span data-stu-id="f8472-108">The probabilities for each outcome from the categorical distribution.</span></span>
<span data-ttu-id="f8472-109">Эти вероятности не могут быть нормализованы, но должны быть не отрицательными.</span><span class="sxs-lookup"><span data-stu-id="f8472-109">These probabilities may not be normalized, but must all be non-negative.</span></span>



## <a name="output--discretedistribution"></a><span data-ttu-id="f8472-110">Выходные данные: [дискретедистрибутион](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span><span class="sxs-lookup"><span data-stu-id="f8472-110">Output : [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span></span>

<span data-ttu-id="f8472-111">Индекс `i` с вероятностью `probs[i] / sum` , где `sum` — Сумма, `probs` заданная параметром `Fold(PlusD, 0.0, probs)` .</span><span class="sxs-lookup"><span data-stu-id="f8472-111">The index `i` with probability `probs[i] / sum`, where `sum` is the sum of `probs` given by `Fold(PlusD, 0.0, probs)`.</span></span>