---
uid: Microsoft.Quantum.Random.DrawRandomDouble
title: Операция Драврандомдаубле
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomDouble
qsharp.summary: Draws a random real number in a given inclusive interval.
ms.openlocfilehash: 792e9c714b761b48618aec2091e167a359c2b522
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847621"
---
# <a name="drawrandomdouble-operation"></a><span data-ttu-id="07707-102">Операция Драврандомдаубле</span><span class="sxs-lookup"><span data-stu-id="07707-102">DrawRandomDouble operation</span></span>

<span data-ttu-id="07707-103">Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="07707-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="07707-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="07707-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="07707-105">Рисует случайное вещественное число в заданном инклюзивном интервале.</span><span class="sxs-lookup"><span data-stu-id="07707-105">Draws a random real number in a given inclusive interval.</span></span>

```qsharp
operation DrawRandomDouble (min : Double, max : Double) : Double
```


## <a name="input"></a><span data-ttu-id="07707-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="07707-106">Input</span></span>

### <a name="min--double"></a><span data-ttu-id="07707-107">min: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="07707-107">min : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="07707-108">Наименьшее вещественное число для рисования.</span><span class="sxs-lookup"><span data-stu-id="07707-108">The smallest real number to be drawn.</span></span>


### <a name="max--double"></a><span data-ttu-id="07707-109">Max: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="07707-109">max : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="07707-110">Максимальное вещественное число для рисования.</span><span class="sxs-lookup"><span data-stu-id="07707-110">The largest real number to be drawn.</span></span>



## <a name="output--double"></a><span data-ttu-id="07707-111">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="07707-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="07707-112">Случайное вещественное число в инклюзивном интервале от `min` до `max` с равномерным вероятностью.</span><span class="sxs-lookup"><span data-stu-id="07707-112">A random real number in the inclusive interval from `min` to `max` with uniform probability.</span></span>

## <a name="example"></a><span data-ttu-id="07707-113">Пример</span><span class="sxs-lookup"><span data-stu-id="07707-113">Example</span></span>

<span data-ttu-id="07707-114">Следующий фрагмент Q # случайным образом рисует угол между $0 $ и $2 \пи $:</span><span class="sxs-lookup"><span data-stu-id="07707-114">The following Q# snippet randomly draws an angle between $0$ and $2 \pi$:</span></span>

```qsharp
let angle = DrawRandomDouble(0.0, 2.0 * PI());
```

## <a name="remarks"></a><span data-ttu-id="07707-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="07707-115">Remarks</span></span>

<span data-ttu-id="07707-116">Завершается ошибкой `max <= min` , если.</span><span class="sxs-lookup"><span data-stu-id="07707-116">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="07707-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="07707-117">See Also</span></span>

- [<span data-ttu-id="07707-118">Microsoft. тактов. Континуаусуниформдистрибутион</span><span class="sxs-lookup"><span data-stu-id="07707-118">Microsoft.Quantum.ContinuousUniformDistribution</span></span>](xref:Microsoft.Quantum.ContinuousUniformDistribution)