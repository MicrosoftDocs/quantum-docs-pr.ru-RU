---
uid: Microsoft.Quantum.Math.PNormalized
title: Функция Пнормализед
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PNormalized
qsharp.summary: >-
  Normalizes a vector of `Double`s in the `L(p)` norm.

  That is, given an array $x$ of type `Double[]`, this returns an array where all elements are divided by the $p$-norm $\|x\|_p$.
ms.openlocfilehash: 6f9dfebe83f52cbf486cd8e6874d3699f5e6b8ab
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732240"
---
# <a name="pnormalized-function"></a><span data-ttu-id="e0973-102">Функция Пнормализед</span><span class="sxs-lookup"><span data-stu-id="e0973-102">PNormalized function</span></span>

<span data-ttu-id="e0973-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="e0973-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="e0973-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e0973-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e0973-105">Нормализация вектора `Double` s в `L(p)` норме.</span><span class="sxs-lookup"><span data-stu-id="e0973-105">Normalizes a vector of `Double`s in the `L(p)` norm.</span></span>

<span data-ttu-id="e0973-106">То есть при наличии массива, $x $ типа `Double[]` , возвращается массив, в котором все элементы делятся на $p $-норму $ \| x \| _p $.</span><span class="sxs-lookup"><span data-stu-id="e0973-106">That is, given an array $x$ of type `Double[]`, this returns an array where all elements are divided by the $p$-norm $\|x\|_p$.</span></span>

```qsharp
function PNormalized (p : Double, array : Double[]) : Double[]
```


## <a name="input"></a><span data-ttu-id="e0973-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e0973-107">Input</span></span>

### <a name="p--double"></a><span data-ttu-id="e0973-108">p: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="e0973-108">p : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="e0973-109">Экспонента $p $ в $p $-норме.</span><span class="sxs-lookup"><span data-stu-id="e0973-109">The exponent $p$ in the $p$-norm.</span></span>


### <a name="array--double"></a><span data-ttu-id="e0973-110">массив: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="e0973-110">array : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>





## <a name="output--double"></a><span data-ttu-id="e0973-111">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="e0973-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="e0973-112">Массив $x $ нормализован $p $-нормой $ \| x \| _p $.</span><span class="sxs-lookup"><span data-stu-id="e0973-112">The array $x$ normalized by the $p$-norm $\|x\|_p$.</span></span>

## <a name="see-also"></a><span data-ttu-id="e0973-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="e0973-113">See Also</span></span>

- [<span data-ttu-id="e0973-114">Microsoft. тактов. Math. Пнорм</span><span class="sxs-lookup"><span data-stu-id="e0973-114">Microsoft.Quantum.Math.PNorm</span></span>](xref:Microsoft.Quantum.Math.PNorm)