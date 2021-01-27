---
uid: Microsoft.Quantum.Random.DrawCategorical
title: Операция Дравкатегорикал
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawCategorical
qsharp.summary: Draws a random sample from a categorical distribution specified by a list of probablities.
ms.openlocfilehash: a9fe1b08e80abc65a5c4b803f0cb8a5e7a62759c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851153"
---
# <a name="drawcategorical-operation"></a><span data-ttu-id="cf4e8-102">Операция Дравкатегорикал</span><span class="sxs-lookup"><span data-stu-id="cf4e8-102">DrawCategorical operation</span></span>

<span data-ttu-id="cf4e8-103">Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="cf4e8-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="cf4e8-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="cf4e8-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="cf4e8-105">Рисует случайную выборку из распределения по категориям, заданному списком пробаблитиес.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-105">Draws a random sample from a categorical distribution specified by a list of probablities.</span></span>

```qsharp
operation DrawCategorical (probs : Double[]) : Int
```


## <a name="description"></a><span data-ttu-id="cf4e8-106">Описание</span><span class="sxs-lookup"><span data-stu-id="cf4e8-106">Description</span></span>

<span data-ttu-id="cf4e8-107">Вероятность выбора определенного индекса пропорциональна значению элемента массива в этом индексе.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-107">The probability of selecting a specific index is proportional to the value of the array element at that index.</span></span>
<span data-ttu-id="cf4e8-108">Элементы массива, равные нулю, игнорируются, и их индексы никогда не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-108">Array elements that are equal to zero are ignored and their indices are never returned.</span></span> <span data-ttu-id="cf4e8-109">Если какой-либо элемент массива меньше нуля или если ни один элемент массива больше нуля, операция завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-109">If any array element is less than zero, or if no array element is greater than zero, then the operation fails.</span></span>

## <a name="input"></a><span data-ttu-id="cf4e8-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="cf4e8-110">Input</span></span>

### <a name="probs--double"></a><span data-ttu-id="cf4e8-111">пробс: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="cf4e8-111">probs : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="cf4e8-112">Массив чисел с плавающей запятой пропорционально вероятности выбора каждого индекса.</span><span class="sxs-lookup"><span data-stu-id="cf4e8-112">An array of floating-point numbers proportional to the probability of selecting each index.</span></span>



## <a name="output--int"></a><span data-ttu-id="cf4e8-113">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="cf4e8-113">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="cf4e8-114">Целое число $i $ с вероятностью $ \Пр (i) = p_i/\ sum_i p_i $, где $p _i $ — это $i $ TH элемент `probs` .</span><span class="sxs-lookup"><span data-stu-id="cf4e8-114">An integer $i$ with probability $\Pr(i) = p_i / \sum_i p_i$, where $p_i$ is the $i$th element of `probs`.</span></span>

## <a name="see-also"></a><span data-ttu-id="cf4e8-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="cf4e8-115">See Also</span></span>

- [<span data-ttu-id="cf4e8-116">Microsoft. тактов. Random. Категорикалдистрибутион</span><span class="sxs-lookup"><span data-stu-id="cf4e8-116">Microsoft.Quantum.Random.CategoricalDistribution</span></span>](xref:Microsoft.Quantum.Random.CategoricalDistribution)