---
uid: Microsoft.Quantum.Random.DrawRandomDouble
title: Операция Драврандомдаубле
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomDouble
qsharp.summary: Draws a random real number in a given inclusive interval.
ms.openlocfilehash: d62416f4a222716edb9393fe4f43731d0e8aa9d3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192950"
---
# <a name="drawrandomdouble-operation"></a><span data-ttu-id="7cb64-102">Операция Драврандомдаубле</span><span class="sxs-lookup"><span data-stu-id="7cb64-102">DrawRandomDouble operation</span></span>

<span data-ttu-id="7cb64-103">Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="7cb64-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="7cb64-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="7cb64-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="7cb64-105">Рисует случайное вещественное число в заданном инклюзивном интервале.</span><span class="sxs-lookup"><span data-stu-id="7cb64-105">Draws a random real number in a given inclusive interval.</span></span>

```qsharp
operation DrawRandomDouble (min : Double, max : Double) : Double
```


## <a name="input"></a><span data-ttu-id="7cb64-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7cb64-106">Input</span></span>

### <a name="min--double"></a><span data-ttu-id="7cb64-107">min: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="7cb64-107">min : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="7cb64-108">Наименьшее вещественное число для рисования.</span><span class="sxs-lookup"><span data-stu-id="7cb64-108">The smallest real number to be drawn.</span></span>


### <a name="max--double"></a><span data-ttu-id="7cb64-109">Max: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="7cb64-109">max : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="7cb64-110">Максимальное вещественное число для рисования.</span><span class="sxs-lookup"><span data-stu-id="7cb64-110">The largest real number to be drawn.</span></span>



## <a name="output--double"></a><span data-ttu-id="7cb64-111">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="7cb64-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="7cb64-112">Случайное вещественное число в инклюзивном интервале от `min` до `max` с равномерным вероятностью.</span><span class="sxs-lookup"><span data-stu-id="7cb64-112">A random real number in the inclusive interval from `min` to `max` with uniform probability.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cb64-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7cb64-113">Remarks</span></span>

<span data-ttu-id="7cb64-114">Завершается ошибкой `max <= min` , если.</span><span class="sxs-lookup"><span data-stu-id="7cb64-114">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="7cb64-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="7cb64-115">See Also</span></span>

- [<span data-ttu-id="7cb64-116">Microsoft. тактов. Континуаусуниформдистрибутион</span><span class="sxs-lookup"><span data-stu-id="7cb64-116">Microsoft.Quantum.ContinuousUniformDistribution</span></span>](xref:Microsoft.Quantum.ContinuousUniformDistribution)