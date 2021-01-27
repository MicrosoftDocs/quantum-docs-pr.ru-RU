---
uid: Microsoft.Quantum.Arithmetic.EvaluatePolynomialFxP
title: Операция Евалуатеполиномиалфксп
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: EvaluatePolynomialFxP
qsharp.summary: Evaluates a polynomial in a fixed-point representation.
ms.openlocfilehash: d88f9002f4ce39b6a16091837c76168fb3a2f086
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843221"
---
# <a name="evaluatepolynomialfxp-operation"></a><span data-ttu-id="adfdf-102">Операция Евалуатеполиномиалфксп</span><span class="sxs-lookup"><span data-stu-id="adfdf-102">EvaluatePolynomialFxP operation</span></span>

<span data-ttu-id="adfdf-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="adfdf-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="adfdf-104">Пакет: [Microsoft. тактов. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="adfdf-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="adfdf-105">Вычисляет значение полинома в представлении с фиксированной запятой.</span><span class="sxs-lookup"><span data-stu-id="adfdf-105">Evaluates a polynomial in a fixed-point representation.</span></span>

```qsharp
operation EvaluatePolynomialFxP (coefficients : Double[], fpx : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="adfdf-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="adfdf-106">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="adfdf-107">коэффициенты: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="adfdf-107">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="adfdf-108">Коэффициенты полинома в виде массива Double, т. е. массива $ [a_0, a_1,..., a_d] $ для полиномного $P (x) = a_0 + a_1 x + \кдотс + a_d x ^ d $.</span><span class="sxs-lookup"><span data-stu-id="adfdf-108">Coefficients of the polynomial as a double array, i.e., the array $[a_0, a_1, ..., a_d]$ for the polynomial $P(x) = a_0 + a_1 x + \cdots + a_d x^d$.</span></span>


### <a name="fpx--fixedpoint"></a><span data-ttu-id="adfdf-109">ФПКС: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="adfdf-109">fpx : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="adfdf-110">Входное число с фиксированной запятой, для которого вычисляется степень полинома.</span><span class="sxs-lookup"><span data-stu-id="adfdf-110">Input fixed-point number for which to evaluate the polynomial.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="adfdf-111">результат: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="adfdf-111">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="adfdf-112">Выходное число с фиксированной запятой, которое будет содержать $P (x) $.</span><span class="sxs-lookup"><span data-stu-id="adfdf-112">Output fixed-point number which will hold $P(x)$.</span></span> <span data-ttu-id="adfdf-113">Должно быть в состоянии $ \кет {0} $ изначально.</span><span class="sxs-lookup"><span data-stu-id="adfdf-113">Must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="adfdf-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="adfdf-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

