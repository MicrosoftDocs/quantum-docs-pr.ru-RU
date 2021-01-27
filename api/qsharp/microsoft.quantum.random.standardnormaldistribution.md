---
uid: Microsoft.Quantum.Random.StandardNormalDistribution
title: Функция Стандарднормалдистрибутион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: StandardNormalDistribution
qsharp.summary: Returns a normal distribution with mean 0 and variance 1.
ms.openlocfilehash: e1776339655c33516f7b3d156f1b377a0c74d250
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857797"
---
# <a name="standardnormaldistribution-function"></a><span data-ttu-id="23924-102">Функция Стандарднормалдистрибутион</span><span class="sxs-lookup"><span data-stu-id="23924-102">StandardNormalDistribution function</span></span>

<span data-ttu-id="23924-103">Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="23924-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="23924-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="23924-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="23924-105">Возвращает нормальное распределение с средним 0 и дисперсией 1.</span><span class="sxs-lookup"><span data-stu-id="23924-105">Returns a normal distribution with mean 0 and variance 1.</span></span>

```qsharp
function StandardNormalDistribution () : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="output--continuousdistribution"></a><span data-ttu-id="23924-106">Выходные данные: [континуаусдистрибутион](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="23924-106">Output : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>



## <a name="example"></a><span data-ttu-id="23924-107">Пример</span><span class="sxs-lookup"><span data-stu-id="23924-107">Example</span></span>

<span data-ttu-id="23924-108">Далее выводятся 10 примеров из стандартного нормального распределения.</span><span class="sxs-lookup"><span data-stu-id="23924-108">The following draws 10 samples from the standard normal distribution:</span></span>

```qsharp
let samples = DrawMany((StandardNormalDistribution())::Sample, 10, ());
```

## <a name="see-also"></a><span data-ttu-id="23924-109">См. также:</span><span class="sxs-lookup"><span data-stu-id="23924-109">See Also</span></span>

- [<span data-ttu-id="23924-110">Microsoft. тактов. Random. Нормалдистрибутион</span><span class="sxs-lookup"><span data-stu-id="23924-110">Microsoft.Quantum.Random.NormalDistribution</span></span>](xref:Microsoft.Quantum.Random.NormalDistribution)