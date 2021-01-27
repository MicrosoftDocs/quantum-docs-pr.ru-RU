---
uid: Microsoft.Quantum.Arithmetic.MultiplyFxP
title: Операция Мултиплифксп
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyFxP
qsharp.summary: Multiplies two fixed-point numbers in quantum registers.
ms.openlocfilehash: 776ccb7a9e1ba1a34b28da6e1cf3a0aafe9da76b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843051"
---
# <a name="multiplyfxp-operation"></a><span data-ttu-id="1f67b-102">Операция Мултиплифксп</span><span class="sxs-lookup"><span data-stu-id="1f67b-102">MultiplyFxP operation</span></span>

<span data-ttu-id="1f67b-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="1f67b-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="1f67b-104">Пакет: [Microsoft. тактов. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="1f67b-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="1f67b-105">Умножает два числа с фиксированной запятой в тактовые регистры.</span><span class="sxs-lookup"><span data-stu-id="1f67b-105">Multiplies two fixed-point numbers in quantum registers.</span></span>

```qsharp
operation MultiplyFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="1f67b-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="1f67b-106">Input</span></span>

### <a name="fp1--fixedpoint"></a><span data-ttu-id="1f67b-107">FP1: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="1f67b-107">fp1 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="1f67b-108">Первое число с фиксированной запятой.</span><span class="sxs-lookup"><span data-stu-id="1f67b-108">First fixed-point number.</span></span>


### <a name="fp2--fixedpoint"></a><span data-ttu-id="1f67b-109">Fp2: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="1f67b-109">fp2 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="1f67b-110">Второе число с фиксированной запятой.</span><span class="sxs-lookup"><span data-stu-id="1f67b-110">Second fixed-point number.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="1f67b-111">результат: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="1f67b-111">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="1f67b-112">Число с фиксированной запятой результата должно быть в состоянии $ \кет {0} $ изначально.</span><span class="sxs-lookup"><span data-stu-id="1f67b-112">Result fixed-point number, must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1f67b-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1f67b-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="1f67b-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="1f67b-114">Remarks</span></span>

<span data-ttu-id="1f67b-115">Текущая реализация требует, чтобы три цифры с фиксированной запятой имели одинаковую позицию и одно и то же число Кубитс.</span><span class="sxs-lookup"><span data-stu-id="1f67b-115">The current implementation requires the three fixed-point numbers to have the same point position and the same number of qubits.</span></span>