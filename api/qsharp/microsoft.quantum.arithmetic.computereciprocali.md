---
uid: Microsoft.Quantum.Arithmetic.ComputeReciprocalI
title: Операция КомпутереЦипрокали
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ComputeReciprocalI
qsharp.summary: Computes the reciprocal 1/x for an unsigned integer x using integer division. The result, interpreted as an integer, will be `floor(2^(2*n-1) / x)`.
ms.openlocfilehash: 9024da4a457265c65a41ef681cfbb99ebd4989a5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223363"
---
# <a name="computereciprocali-operation"></a><span data-ttu-id="7e16b-102">Операция КомпутереЦипрокали</span><span class="sxs-lookup"><span data-stu-id="7e16b-102">ComputeReciprocalI operation</span></span>

<span data-ttu-id="7e16b-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="7e16b-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="7e16b-104">Пакет: [Microsoft. тактов. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="7e16b-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="7e16b-105">Вычисление обратной величины 1/x для целого числа без знака x с использованием целочисленного деления.</span><span class="sxs-lookup"><span data-stu-id="7e16b-105">Computes the reciprocal 1/x for an unsigned integer x using integer division.</span></span> <span data-ttu-id="7e16b-106">Результат, интерпретируемый как целое число, будет иметь значение `floor(2^(2*n-1) / x)` .</span><span class="sxs-lookup"><span data-stu-id="7e16b-106">The result, interpreted as an integer, will be `floor(2^(2*n-1) / x)`.</span></span>

```qsharp
operation ComputeReciprocalI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="7e16b-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7e16b-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="7e16b-108">xs: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="7e16b-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="7e16b-109">n-разрядное целое число без знака</span><span class="sxs-lookup"><span data-stu-id="7e16b-109">n-bit unsigned integer</span></span>


### <a name="result--littleendian"></a><span data-ttu-id="7e16b-110">результат: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="7e16b-110">result : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="7e16b-111">2N-разрядный выход должен быть в $ \кет {0} $ изначально.</span><span class="sxs-lookup"><span data-stu-id="7e16b-111">2n-bit output, must be in $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7e16b-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7e16b-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="7e16b-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7e16b-113">Remarks</span></span>

<span data-ttu-id="7e16b-114">Для входных данных x = 0 выходные данные будут содержать все объекты.</span><span class="sxs-lookup"><span data-stu-id="7e16b-114">For the input x=0, the output will be all-ones.</span></span>