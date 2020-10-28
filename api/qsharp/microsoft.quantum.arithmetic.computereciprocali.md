---
uid: Microsoft.Quantum.Arithmetic.ComputeReciprocalI
title: Операция КомпутереЦипрокали
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ComputeReciprocalI
qsharp.summary: Computes the reciprocal 1/x for an unsigned integer x using integer division. The result, interpreted as an integer, will be `floor(2^(2*n-1) / x)`.
ms.openlocfilehash: b99e816ed69af6e6d1758442d6f95c5ab0e5c07a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731585"
---
# <a name="computereciprocali-operation"></a><span data-ttu-id="f776c-102">Операция КомпутереЦипрокали</span><span class="sxs-lookup"><span data-stu-id="f776c-102">ComputeReciprocalI operation</span></span>

<span data-ttu-id="f776c-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="f776c-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="f776c-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f776c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f776c-105">Вычисление обратной величины 1/x для целого числа без знака x с использованием целочисленного деления.</span><span class="sxs-lookup"><span data-stu-id="f776c-105">Computes the reciprocal 1/x for an unsigned integer x using integer division.</span></span> <span data-ttu-id="f776c-106">Результат, интерпретируемый как целое число, будет иметь значение `floor(2^(2*n-1) / x)` .</span><span class="sxs-lookup"><span data-stu-id="f776c-106">The result, interpreted as an integer, will be `floor(2^(2*n-1) / x)`.</span></span>

```qsharp
operation ComputeReciprocalI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="f776c-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f776c-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="f776c-108">xs: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="f776c-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="f776c-109">n-разрядное целое число без знака</span><span class="sxs-lookup"><span data-stu-id="f776c-109">n-bit unsigned integer</span></span>


### <a name="result--littleendian"></a><span data-ttu-id="f776c-110">результат: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="f776c-110">result : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="f776c-111">2N-разрядный выход должен быть в $ \кет {0} $ изначально.</span><span class="sxs-lookup"><span data-stu-id="f776c-111">2n-bit output, must be in $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f776c-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f776c-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="f776c-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="f776c-113">Remarks</span></span>

<span data-ttu-id="f776c-114">Для входных данных x = 0 выходные данные будут содержать все объекты.</span><span class="sxs-lookup"><span data-stu-id="f776c-114">For the input x=0, the output will be all-ones.</span></span>