---
uid: Microsoft.Quantum.Random.DrawRandomInt
title: Операция Драврандоминт
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomInt
qsharp.summary: Draws a random integer in a given inclusive range.
ms.openlocfilehash: d9d8d9fbb25587ac5ccbd4edf0e555649380375f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733593"
---
# <a name="drawrandomint-operation"></a><span data-ttu-id="86b6c-102">Операция Драврандоминт</span><span class="sxs-lookup"><span data-stu-id="86b6c-102">DrawRandomInt operation</span></span>

<span data-ttu-id="86b6c-103">Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="86b6c-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="86b6c-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="86b6c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="86b6c-105">Рисует случайное целое число в заданном инклюзивном диапазоне.</span><span class="sxs-lookup"><span data-stu-id="86b6c-105">Draws a random integer in a given inclusive range.</span></span>

```qsharp
operation DrawRandomInt (min : Int, max : Int) : Int
```


## <a name="input"></a><span data-ttu-id="86b6c-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="86b6c-106">Input</span></span>

### <a name="min--int"></a><span data-ttu-id="86b6c-107">min: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="86b6c-107">min : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="86b6c-108">Наименьшее целое число для рисования.</span><span class="sxs-lookup"><span data-stu-id="86b6c-108">The smallest integer to be drawn.</span></span>


### <a name="max--int"></a><span data-ttu-id="86b6c-109">Max: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="86b6c-109">max : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="86b6c-110">Максимальное отображаемое целое число.</span><span class="sxs-lookup"><span data-stu-id="86b6c-110">The largest integer to be drawn.</span></span>



## <a name="output--int"></a><span data-ttu-id="86b6c-111">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="86b6c-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="86b6c-112">Целое число в инклюзивном диапазоне от `min` до `max` с равномерным значением вероятности.</span><span class="sxs-lookup"><span data-stu-id="86b6c-112">An integer in the inclusive range from `min` to `max` with uniform probability.</span></span>

## <a name="remarks"></a><span data-ttu-id="86b6c-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="86b6c-113">Remarks</span></span>

<span data-ttu-id="86b6c-114">Завершается ошибкой `max <= min` , если.</span><span class="sxs-lookup"><span data-stu-id="86b6c-114">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="86b6c-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="86b6c-115">See Also</span></span>

- [<span data-ttu-id="86b6c-116">Microsoft. тактов. Дискретеуниформдистрибутион</span><span class="sxs-lookup"><span data-stu-id="86b6c-116">Microsoft.Quantum.DiscreteUniformDistribution</span></span>](xref:Microsoft.Quantum.DiscreteUniformDistribution)