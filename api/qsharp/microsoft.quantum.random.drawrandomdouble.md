---
uid: Microsoft.Quantum.Random.DrawRandomDouble
title: Операция Драврандомдаубле
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomDouble
qsharp.summary: Draws a random real number in a given inclusive interval.
ms.openlocfilehash: 6c0558ded2bd018afad84c42c2d15fc029ac0d44
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733209"
---
# <a name="drawrandomdouble-operation"></a><span data-ttu-id="41eb9-102">Операция Драврандомдаубле</span><span class="sxs-lookup"><span data-stu-id="41eb9-102">DrawRandomDouble operation</span></span>

<span data-ttu-id="41eb9-103">Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="41eb9-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="41eb9-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="41eb9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="41eb9-105">Рисует случайное вещественное число в заданном инклюзивном интервале.</span><span class="sxs-lookup"><span data-stu-id="41eb9-105">Draws a random real number in a given inclusive interval.</span></span>

```qsharp
operation DrawRandomDouble (min : Double, max : Double) : Double
```


## <a name="input"></a><span data-ttu-id="41eb9-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="41eb9-106">Input</span></span>

### <a name="min--double"></a><span data-ttu-id="41eb9-107">min: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="41eb9-107">min : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="41eb9-108">Наименьшее вещественное число для рисования.</span><span class="sxs-lookup"><span data-stu-id="41eb9-108">The smallest real number to be drawn.</span></span>


### <a name="max--double"></a><span data-ttu-id="41eb9-109">Max: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="41eb9-109">max : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="41eb9-110">Максимальное вещественное число для рисования.</span><span class="sxs-lookup"><span data-stu-id="41eb9-110">The largest real number to be drawn.</span></span>



## <a name="output--double"></a><span data-ttu-id="41eb9-111">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="41eb9-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="41eb9-112">Случайное вещественное число в инклюзивном интервале от `min` до `max` с равномерным вероятностью.</span><span class="sxs-lookup"><span data-stu-id="41eb9-112">A random real number in the inclusive interval from `min` to `max` with uniform probability.</span></span>

## <a name="remarks"></a><span data-ttu-id="41eb9-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="41eb9-113">Remarks</span></span>

<span data-ttu-id="41eb9-114">Завершается ошибкой `max <= min` , если.</span><span class="sxs-lookup"><span data-stu-id="41eb9-114">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="41eb9-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="41eb9-115">See Also</span></span>

- [<span data-ttu-id="41eb9-116">Microsoft. тактов. Континуаусуниформдистрибутион</span><span class="sxs-lookup"><span data-stu-id="41eb9-116">Microsoft.Quantum.ContinuousUniformDistribution</span></span>](xref:Microsoft.Quantum.ContinuousUniformDistribution)