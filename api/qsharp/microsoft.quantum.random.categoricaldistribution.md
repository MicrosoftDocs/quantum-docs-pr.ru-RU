---
uid: Microsoft.Quantum.Random.CategoricalDistribution
title: Функция Категорикалдистрибутион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: CategoricalDistribution
qsharp.summary: Returns a discrete categorical distribution, in which the probability for each of a finite list of given outcomes is explicitly specified.
ms.openlocfilehash: 754ada71078bd5446f78885ace31d92dce6bf1a4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842350"
---
# <a name="categoricaldistribution-function"></a><span data-ttu-id="80523-102">Функция Категорикалдистрибутион</span><span class="sxs-lookup"><span data-stu-id="80523-102">CategoricalDistribution function</span></span>

<span data-ttu-id="80523-103">Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="80523-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="80523-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="80523-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="80523-105">Возвращает дискретное распределение по категориям, в котором явно задана вероятность для каждого конечного списка заданных результатов.</span><span class="sxs-lookup"><span data-stu-id="80523-105">Returns a discrete categorical distribution, in which the probability for each of a finite list of given outcomes is explicitly specified.</span></span>

```qsharp
function CategoricalDistribution (probs : Double[]) : Microsoft.Quantum.Random.DiscreteDistribution
```


## <a name="input"></a><span data-ttu-id="80523-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="80523-106">Input</span></span>

### <a name="probs--double"></a><span data-ttu-id="80523-107">пробс: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="80523-107">probs : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="80523-108">Вероятности для каждого результата из распределения по категориям.</span><span class="sxs-lookup"><span data-stu-id="80523-108">The probabilities for each outcome from the categorical distribution.</span></span>
<span data-ttu-id="80523-109">Эти вероятности не могут быть нормализованы, но должны быть не отрицательными.</span><span class="sxs-lookup"><span data-stu-id="80523-109">These probabilities may not be normalized, but must all be non-negative.</span></span>



## <a name="output--discretedistribution"></a><span data-ttu-id="80523-110">Выходные данные: [дискретедистрибутион](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span><span class="sxs-lookup"><span data-stu-id="80523-110">Output : [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span></span>

<span data-ttu-id="80523-111">Индекс `i` с вероятностью `probs[i] / sum` , где `sum` — Сумма, `probs` заданная параметром `Fold(PlusD, 0.0, probs)` .</span><span class="sxs-lookup"><span data-stu-id="80523-111">The index `i` with probability `probs[i] / sum`, where `sum` is the sum of `probs` given by `Fold(PlusD, 0.0, probs)`.</span></span>

## <a name="example"></a><span data-ttu-id="80523-112">Пример</span><span class="sxs-lookup"><span data-stu-id="80523-112">Example</span></span>

<span data-ttu-id="80523-113">В следующем коде Q # отображается 0 с вероятностью 30% и 1 с вероятностью 70%:</span><span class="sxs-lookup"><span data-stu-id="80523-113">The following Q# code will display 0 with probability 30% and 1 with probability 70%:</span></span>

```qsharp
let dist = CategoricalDistribution([0.3, 0.7]);
Message($"Got sample: {dist::Sample()}");
```