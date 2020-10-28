---
uid: Microsoft.Quantum.Arithmetic.EvaluateEvenPolynomialFxP
title: Операция Евалуативенполиномиалфксп
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: EvaluateEvenPolynomialFxP
qsharp.summary: Evaluates an even polynomial in a fixed-point representation.
ms.openlocfilehash: e49a6d47553a60766b561525e8cfa37e95fda9e8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731569"
---
# <a name="evaluateevenpolynomialfxp-operation"></a><span data-ttu-id="2c1b5-102">Операция Евалуативенполиномиалфксп</span><span class="sxs-lookup"><span data-stu-id="2c1b5-102">EvaluateEvenPolynomialFxP operation</span></span>

<span data-ttu-id="2c1b5-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="2c1b5-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="2c1b5-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2c1b5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2c1b5-105">Вычисляет четность в представлении с фиксированной запятой.</span><span class="sxs-lookup"><span data-stu-id="2c1b5-105">Evaluates an even polynomial in a fixed-point representation.</span></span>

```qsharp
operation EvaluateEvenPolynomialFxP (coefficients : Double[], fpx : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit
```


## <a name="input"></a><span data-ttu-id="2c1b5-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2c1b5-106">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="2c1b5-107">коэффициенты: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="2c1b5-107">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="2c1b5-108">Коэффициенты равномерности в виде массива типа Double, т. е. массива $ [a_0, a_1,..., a_k] $ для четного $P (x) = a_0 + a_1 x ^ 2 + \кдотс + a_k x ^ {2000} $.</span><span class="sxs-lookup"><span data-stu-id="2c1b5-108">Coefficients of the even polynomial as a double array, i.e., the array $[a_0, a_1, ..., a_k]$ for the even polynomial $P(x) = a_0 + a_1 x^2 + \cdots + a_k x^{2k}$.</span></span>


### <a name="fpx--fixedpoint"></a><span data-ttu-id="2c1b5-109">ФПКС: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="2c1b5-109">fpx : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="2c1b5-110">Входное число с фиксированной запятой, для которого вычисляется степень полинома.</span><span class="sxs-lookup"><span data-stu-id="2c1b5-110">Input fixed-point number for which to evaluate the polynomial.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="2c1b5-111">результат: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="2c1b5-111">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="2c1b5-112">Выходное число с фиксированной запятой, которое будет содержать $P (x) $.</span><span class="sxs-lookup"><span data-stu-id="2c1b5-112">Output fixed-point number which will hold $P(x)$.</span></span> <span data-ttu-id="2c1b5-113">Должно быть в состоянии $ \кет {0} $ изначально.</span><span class="sxs-lookup"><span data-stu-id="2c1b5-113">Must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2c1b5-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2c1b5-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

