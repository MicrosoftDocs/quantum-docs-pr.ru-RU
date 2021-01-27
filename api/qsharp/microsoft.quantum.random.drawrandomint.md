---
uid: Microsoft.Quantum.Random.DrawRandomInt
title: Операция Драврандоминт
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomInt
qsharp.summary: Draws a random integer in a given inclusive range.
ms.openlocfilehash: ebed7f52b7c4a8c538ed9d718c486b5aa94a0327
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851136"
---
# <a name="drawrandomint-operation"></a><span data-ttu-id="73e80-102">Операция Драврандоминт</span><span class="sxs-lookup"><span data-stu-id="73e80-102">DrawRandomInt operation</span></span>

<span data-ttu-id="73e80-103">Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="73e80-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="73e80-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="73e80-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="73e80-105">Рисует случайное целое число в заданном инклюзивном диапазоне.</span><span class="sxs-lookup"><span data-stu-id="73e80-105">Draws a random integer in a given inclusive range.</span></span>

```qsharp
operation DrawRandomInt (min : Int, max : Int) : Int
```


## <a name="input"></a><span data-ttu-id="73e80-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="73e80-106">Input</span></span>

### <a name="min--int"></a><span data-ttu-id="73e80-107">min: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="73e80-107">min : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="73e80-108">Наименьшее целое число для рисования.</span><span class="sxs-lookup"><span data-stu-id="73e80-108">The smallest integer to be drawn.</span></span>


### <a name="max--int"></a><span data-ttu-id="73e80-109">Max: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="73e80-109">max : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="73e80-110">Максимальное отображаемое целое число.</span><span class="sxs-lookup"><span data-stu-id="73e80-110">The largest integer to be drawn.</span></span>



## <a name="output--int"></a><span data-ttu-id="73e80-111">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="73e80-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="73e80-112">Целое число в инклюзивном диапазоне от `min` до `max` с равномерным значением вероятности.</span><span class="sxs-lookup"><span data-stu-id="73e80-112">An integer in the inclusive range from `min` to `max` with uniform probability.</span></span>

## <a name="example"></a><span data-ttu-id="73e80-113">Пример</span><span class="sxs-lookup"><span data-stu-id="73e80-113">Example</span></span>

<span data-ttu-id="73e80-114">Следующий фрагмент Q # случайным образом выполняет откат шести костей:</span><span class="sxs-lookup"><span data-stu-id="73e80-114">The following Q# snippet randomly rolls a six-sided die:</span></span>

```qsharp
let roll = DrawRandomInt(1, 6);
```

## <a name="remarks"></a><span data-ttu-id="73e80-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="73e80-115">Remarks</span></span>

<span data-ttu-id="73e80-116">Завершается ошибкой `max <= min` , если.</span><span class="sxs-lookup"><span data-stu-id="73e80-116">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="73e80-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="73e80-117">See Also</span></span>

- [<span data-ttu-id="73e80-118">Microsoft. тактов. Дискретеуниформдистрибутион</span><span class="sxs-lookup"><span data-stu-id="73e80-118">Microsoft.Quantum.DiscreteUniformDistribution</span></span>](xref:Microsoft.Quantum.DiscreteUniformDistribution)