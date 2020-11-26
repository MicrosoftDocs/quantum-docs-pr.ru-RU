---
uid: Microsoft.Quantum.Random.DrawRandomInt
title: Операция Драврандоминт
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomInt
qsharp.summary: Draws a random integer in a given inclusive range.
ms.openlocfilehash: f7b6cb75f761e4c45295245ed4bd4fb82c592809
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192916"
---
# <a name="drawrandomint-operation"></a><span data-ttu-id="2945b-102">Операция Драврандоминт</span><span class="sxs-lookup"><span data-stu-id="2945b-102">DrawRandomInt operation</span></span>

<span data-ttu-id="2945b-103">Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="2945b-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="2945b-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="2945b-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="2945b-105">Рисует случайное целое число в заданном инклюзивном диапазоне.</span><span class="sxs-lookup"><span data-stu-id="2945b-105">Draws a random integer in a given inclusive range.</span></span>

```qsharp
operation DrawRandomInt (min : Int, max : Int) : Int
```


## <a name="input"></a><span data-ttu-id="2945b-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2945b-106">Input</span></span>

### <a name="min--int"></a><span data-ttu-id="2945b-107">min: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2945b-107">min : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2945b-108">Наименьшее целое число для рисования.</span><span class="sxs-lookup"><span data-stu-id="2945b-108">The smallest integer to be drawn.</span></span>


### <a name="max--int"></a><span data-ttu-id="2945b-109">Max: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2945b-109">max : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2945b-110">Максимальное отображаемое целое число.</span><span class="sxs-lookup"><span data-stu-id="2945b-110">The largest integer to be drawn.</span></span>



## <a name="output--int"></a><span data-ttu-id="2945b-111">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2945b-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2945b-112">Целое число в инклюзивном диапазоне от `min` до `max` с равномерным значением вероятности.</span><span class="sxs-lookup"><span data-stu-id="2945b-112">An integer in the inclusive range from `min` to `max` with uniform probability.</span></span>

## <a name="remarks"></a><span data-ttu-id="2945b-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2945b-113">Remarks</span></span>

<span data-ttu-id="2945b-114">Завершается ошибкой `max <= min` , если.</span><span class="sxs-lookup"><span data-stu-id="2945b-114">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="2945b-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="2945b-115">See Also</span></span>

- [<span data-ttu-id="2945b-116">Microsoft. тактов. Дискретеуниформдистрибутион</span><span class="sxs-lookup"><span data-stu-id="2945b-116">Microsoft.Quantum.DiscreteUniformDistribution</span></span>](xref:Microsoft.Quantum.DiscreteUniformDistribution)