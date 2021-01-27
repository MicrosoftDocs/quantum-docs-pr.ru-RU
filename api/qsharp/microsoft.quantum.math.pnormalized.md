---
uid: Microsoft.Quantum.Math.PNormalized
title: Функция Пнормализед
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PNormalized
qsharp.summary: >-
  Normalizes a vector of `Double`s in the `L(p)` norm.

  That is, given an array $x$ of type `Double[]`, this returns an array where all elements are divided by the $p$-norm $\|x\|_p$.
ms.openlocfilehash: ea6a88d07d3b246f666b793f0b10ab6598ea4ff6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854846"
---
# <a name="pnormalized-function"></a><span data-ttu-id="17df9-102">Функция Пнормализед</span><span class="sxs-lookup"><span data-stu-id="17df9-102">PNormalized function</span></span>

<span data-ttu-id="17df9-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="17df9-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="17df9-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="17df9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="17df9-105">Нормализация вектора `Double` s в `L(p)` норме.</span><span class="sxs-lookup"><span data-stu-id="17df9-105">Normalizes a vector of `Double`s in the `L(p)` norm.</span></span>

<span data-ttu-id="17df9-106">То есть при наличии массива, $x $ типа `Double[]` , возвращается массив, в котором все элементы делятся на $p $-норму $ \| x \| _p $.</span><span class="sxs-lookup"><span data-stu-id="17df9-106">That is, given an array $x$ of type `Double[]`, this returns an array where all elements are divided by the $p$-norm $\|x\|_p$.</span></span>

```qsharp
function PNormalized (p : Double, array : Double[]) : Double[]
```


## <a name="input"></a><span data-ttu-id="17df9-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="17df9-107">Input</span></span>

### <a name="p--double"></a><span data-ttu-id="17df9-108">p: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="17df9-108">p : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="17df9-109">Экспонента $p $ в $p $-норме.</span><span class="sxs-lookup"><span data-stu-id="17df9-109">The exponent $p$ in the $p$-norm.</span></span>


### <a name="array--double"></a><span data-ttu-id="17df9-110">массив: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="17df9-110">array : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>





## <a name="output--double"></a><span data-ttu-id="17df9-111">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="17df9-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="17df9-112">Массив $x $ нормализован $p $-нормой $ \| x \| _p $.</span><span class="sxs-lookup"><span data-stu-id="17df9-112">The array $x$ normalized by the $p$-norm $\|x\|_p$.</span></span>

## <a name="see-also"></a><span data-ttu-id="17df9-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="17df9-113">See Also</span></span>

- [<span data-ttu-id="17df9-114">Microsoft. тактов. Math. Пнорм</span><span class="sxs-lookup"><span data-stu-id="17df9-114">Microsoft.Quantum.Math.PNorm</span></span>](xref:Microsoft.Quantum.Math.PNorm)