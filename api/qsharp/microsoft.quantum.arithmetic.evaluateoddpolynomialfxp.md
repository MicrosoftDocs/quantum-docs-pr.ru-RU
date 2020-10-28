---
uid: Microsoft.Quantum.Arithmetic.EvaluateOddPolynomialFxP
title: Операция Евалуатеоддполиномиалфксп
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: EvaluateOddPolynomialFxP
qsharp.summary: Evaluates an odd polynomial in a fixed-point representation.
ms.openlocfilehash: d52da4092f16d43ab9d08b03f798a4d6789c7348
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731568"
---
# <a name="evaluateoddpolynomialfxp-operation"></a><span data-ttu-id="637f9-102">Операция Евалуатеоддполиномиалфксп</span><span class="sxs-lookup"><span data-stu-id="637f9-102">EvaluateOddPolynomialFxP operation</span></span>

<span data-ttu-id="637f9-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="637f9-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="637f9-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="637f9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="637f9-105">Вычисляет нечетный полином в представлении с фиксированной запятой.</span><span class="sxs-lookup"><span data-stu-id="637f9-105">Evaluates an odd polynomial in a fixed-point representation.</span></span>

```qsharp
operation EvaluateOddPolynomialFxP (coefficients : Double[], fpx : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit
```


## <a name="input"></a><span data-ttu-id="637f9-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="637f9-106">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="637f9-107">коэффициенты: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="637f9-107">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="637f9-108">Коэффициенты нечетнымго полинома в виде двойного массива, т. е. массива $ [a_0, a_1,..., a_k] $ для нечетного $P (x) = a_0 x + a_1 x ^ 3 + \кдотс + a_k x ^ {2000 + 1} $.</span><span class="sxs-lookup"><span data-stu-id="637f9-108">Coefficients of the odd polynomial as a double array, i.e., the array $[a_0, a_1, ..., a_k]$ for the odd polynomial $P(x) = a_0 x + a_1 x^3 + \cdots + a_k x^{2k+1}$.</span></span>


### <a name="fpx--fixedpoint"></a><span data-ttu-id="637f9-109">ФПКС: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="637f9-109">fpx : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="637f9-110">Входное число с фиксированной запятой, для которого вычисляется степень полинома.</span><span class="sxs-lookup"><span data-stu-id="637f9-110">Input fixed-point number for which to evaluate the polynomial.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="637f9-111">результат: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="637f9-111">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="637f9-112">Выходное число с фиксированной запятой, которое будет содержать P (x).</span><span class="sxs-lookup"><span data-stu-id="637f9-112">Output fixed-point number which will hold P(x).</span></span> <span data-ttu-id="637f9-113">Должно быть в состоянии $ \кет {0} $ изначально.</span><span class="sxs-lookup"><span data-stu-id="637f9-113">Must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="637f9-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="637f9-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

