---
uid: Microsoft.Quantum.Arithmetic.EvaluateOddPolynomialFxP
title: Операция Евалуатеоддполиномиалфксп
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: EvaluateOddPolynomialFxP
qsharp.summary: Evaluates an odd polynomial in a fixed-point representation.
ms.openlocfilehash: 852e986cd09c3b2e31263f53e381d9da73298415
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846669"
---
# <a name="evaluateoddpolynomialfxp-operation"></a><span data-ttu-id="89206-102">Операция Евалуатеоддполиномиалфксп</span><span class="sxs-lookup"><span data-stu-id="89206-102">EvaluateOddPolynomialFxP operation</span></span>

<span data-ttu-id="89206-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="89206-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="89206-104">Пакет: [Microsoft. тактов. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="89206-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="89206-105">Вычисляет нечетный полином в представлении с фиксированной запятой.</span><span class="sxs-lookup"><span data-stu-id="89206-105">Evaluates an odd polynomial in a fixed-point representation.</span></span>

```qsharp
operation EvaluateOddPolynomialFxP (coefficients : Double[], fpx : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="89206-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="89206-106">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="89206-107">коэффициенты: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="89206-107">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="89206-108">Коэффициенты нечетнымго полинома в виде двойного массива, т. е. массива $ [a_0, a_1,..., a_k] $ для нечетного $P (x) = a_0 x + a_1 x ^ 3 + \кдотс + a_k x ^ {2000 + 1} $.</span><span class="sxs-lookup"><span data-stu-id="89206-108">Coefficients of the odd polynomial as a double array, i.e., the array $[a_0, a_1, ..., a_k]$ for the odd polynomial $P(x) = a_0 x + a_1 x^3 + \cdots + a_k x^{2k+1}$.</span></span>


### <a name="fpx--fixedpoint"></a><span data-ttu-id="89206-109">ФПКС: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="89206-109">fpx : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="89206-110">Входное число с фиксированной запятой, для которого вычисляется степень полинома.</span><span class="sxs-lookup"><span data-stu-id="89206-110">Input fixed-point number for which to evaluate the polynomial.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="89206-111">результат: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="89206-111">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="89206-112">Выходное число с фиксированной запятой, которое будет содержать P (x).</span><span class="sxs-lookup"><span data-stu-id="89206-112">Output fixed-point number which will hold P(x).</span></span> <span data-ttu-id="89206-113">Должно быть в состоянии $ \кет {0} $ изначально.</span><span class="sxs-lookup"><span data-stu-id="89206-113">Must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="89206-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="89206-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

