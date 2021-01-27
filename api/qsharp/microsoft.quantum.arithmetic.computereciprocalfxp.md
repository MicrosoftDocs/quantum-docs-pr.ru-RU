---
uid: Microsoft.Quantum.Arithmetic.ComputeReciprocalFxP
title: Операция КомпутереЦипрокалфксп
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ComputeReciprocalFxP
qsharp.summary: Computes $1/x$ for a fixed-point number $x$.
ms.openlocfilehash: db7425f1a8a9b5ddfdc6b123dad003298e3670e6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843244"
---
# <a name="computereciprocalfxp-operation"></a><span data-ttu-id="9a6ba-102">Операция КомпутереЦипрокалфксп</span><span class="sxs-lookup"><span data-stu-id="9a6ba-102">ComputeReciprocalFxP operation</span></span>

<span data-ttu-id="9a6ba-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="9a6ba-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="9a6ba-104">Пакет: [Microsoft. тактов. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="9a6ba-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="9a6ba-105">Вычисление $1/x $ для числа с фиксированной запятой $x $.</span><span class="sxs-lookup"><span data-stu-id="9a6ba-105">Computes $1/x$ for a fixed-point number $x$.</span></span>

```qsharp
operation ComputeReciprocalFxP (x : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="9a6ba-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="9a6ba-106">Input</span></span>

### <a name="x--fixedpoint"></a><span data-ttu-id="9a6ba-107">x: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="9a6ba-107">x : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="9a6ba-108">Число с фиксированной запятой, которое необходимо инвертировать.</span><span class="sxs-lookup"><span data-stu-id="9a6ba-108">Fixed-point number to be inverted.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="9a6ba-109">результат: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="9a6ba-109">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="9a6ba-110">Число с фиксированной запятой, которое будет содержать результат.</span><span class="sxs-lookup"><span data-stu-id="9a6ba-110">Fixed-point number that will hold the result.</span></span> <span data-ttu-id="9a6ba-111">Необходимо инициализировать в $ \ket{0.0} $.</span><span class="sxs-lookup"><span data-stu-id="9a6ba-111">Must be initialized to $\ket{0.0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9a6ba-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9a6ba-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

