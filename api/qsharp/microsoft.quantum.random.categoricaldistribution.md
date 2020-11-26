---
uid: Microsoft.Quantum.Random.CategoricalDistribution
title: Функция Категорикалдистрибутион
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: CategoricalDistribution
qsharp.summary: Returns a discrete categorical distribution, in which the probability for each of a finite list of given outcomes is explicitly specified.
ms.openlocfilehash: 2e3d9b17939d5a9a5bc5e7d89a843e0ff5a848ba
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210256"
---
# <a name="categoricaldistribution-function"></a><span data-ttu-id="ba7cf-102">Функция Категорикалдистрибутион</span><span class="sxs-lookup"><span data-stu-id="ba7cf-102">CategoricalDistribution function</span></span>

<span data-ttu-id="ba7cf-103">Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="ba7cf-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="ba7cf-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="ba7cf-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="ba7cf-105">Возвращает дискретное распределение по категориям, в котором явно задана вероятность для каждого конечного списка заданных результатов.</span><span class="sxs-lookup"><span data-stu-id="ba7cf-105">Returns a discrete categorical distribution, in which the probability for each of a finite list of given outcomes is explicitly specified.</span></span>

```qsharp
function CategoricalDistribution (probs : Double[]) : Microsoft.Quantum.Random.DiscreteDistribution
```


## <a name="input"></a><span data-ttu-id="ba7cf-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ba7cf-106">Input</span></span>

### <a name="probs--double"></a><span data-ttu-id="ba7cf-107">пробс: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="ba7cf-107">probs : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="ba7cf-108">Вероятности для каждого результата из распределения по категориям.</span><span class="sxs-lookup"><span data-stu-id="ba7cf-108">The probabilities for each outcome from the categorical distribution.</span></span>
<span data-ttu-id="ba7cf-109">Эти вероятности не могут быть нормализованы, но должны быть не отрицательными.</span><span class="sxs-lookup"><span data-stu-id="ba7cf-109">These probabilities may not be normalized, but must all be non-negative.</span></span>



## <a name="output--discretedistribution"></a><span data-ttu-id="ba7cf-110">Выходные данные: [дискретедистрибутион](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span><span class="sxs-lookup"><span data-stu-id="ba7cf-110">Output : [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span></span>

<span data-ttu-id="ba7cf-111">Индекс `i` с вероятностью `probs[i] / sum` , где `sum` — Сумма, `probs` заданная параметром `Fold(PlusD, 0.0, probs)` .</span><span class="sxs-lookup"><span data-stu-id="ba7cf-111">The index `i` with probability `probs[i] / sum`, where `sum` is the sum of `probs` given by `Fold(PlusD, 0.0, probs)`.</span></span>