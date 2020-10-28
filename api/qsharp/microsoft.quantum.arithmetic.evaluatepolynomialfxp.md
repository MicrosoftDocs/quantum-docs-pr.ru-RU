---
uid: Microsoft.Quantum.Arithmetic.EvaluatePolynomialFxP
title: Операция Евалуатеполиномиалфксп
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: EvaluatePolynomialFxP
qsharp.summary: Evaluates a polynomial in a fixed-point representation.
ms.openlocfilehash: 3903bf69d5b0a6e57530f2c6a44e1d351c8a605f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731560"
---
# <a name="evaluatepolynomialfxp-operation"></a><span data-ttu-id="62f6b-102">Операция Евалуатеполиномиалфксп</span><span class="sxs-lookup"><span data-stu-id="62f6b-102">EvaluatePolynomialFxP operation</span></span>

<span data-ttu-id="62f6b-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="62f6b-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="62f6b-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="62f6b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="62f6b-105">Вычисляет значение полинома в представлении с фиксированной запятой.</span><span class="sxs-lookup"><span data-stu-id="62f6b-105">Evaluates a polynomial in a fixed-point representation.</span></span>

```qsharp
operation EvaluatePolynomialFxP (coefficients : Double[], fpx : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit
```


## <a name="input"></a><span data-ttu-id="62f6b-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="62f6b-106">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="62f6b-107">коэффициенты: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="62f6b-107">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="62f6b-108">Коэффициенты полинома в виде массива Double, т. е. массива $ [a_0, a_1,..., a_d] $ для полиномного $P (x) = a_0 + a_1 x + \кдотс + a_d x ^ d $.</span><span class="sxs-lookup"><span data-stu-id="62f6b-108">Coefficients of the polynomial as a double array, i.e., the array $[a_0, a_1, ..., a_d]$ for the polynomial $P(x) = a_0 + a_1 x + \cdots + a_d x^d$.</span></span>


### <a name="fpx--fixedpoint"></a><span data-ttu-id="62f6b-109">ФПКС: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="62f6b-109">fpx : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="62f6b-110">Входное число с фиксированной запятой, для которого вычисляется степень полинома.</span><span class="sxs-lookup"><span data-stu-id="62f6b-110">Input fixed-point number for which to evaluate the polynomial.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="62f6b-111">результат: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="62f6b-111">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="62f6b-112">Выходное число с фиксированной запятой, которое будет содержать $P (x) $.</span><span class="sxs-lookup"><span data-stu-id="62f6b-112">Output fixed-point number which will hold $P(x)$.</span></span> <span data-ttu-id="62f6b-113">Должно быть в состоянии $ \кет {0} $ изначально.</span><span class="sxs-lookup"><span data-stu-id="62f6b-113">Must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="62f6b-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="62f6b-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

