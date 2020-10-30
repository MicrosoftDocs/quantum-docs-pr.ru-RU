---
uid: Microsoft.Quantum.Arithmetic.MultiplyFxP
title: Операция Мултиплифксп
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyFxP
qsharp.summary: Multiplies two fixed-point numbers in quantum registers.
ms.openlocfilehash: 18883f3f4c3793b91e248f4bd89f9def640bf254
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730624"
---
# <a name="multiplyfxp-operation"></a><span data-ttu-id="a7f71-102">Операция Мултиплифксп</span><span class="sxs-lookup"><span data-stu-id="a7f71-102">MultiplyFxP operation</span></span>

<span data-ttu-id="a7f71-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="a7f71-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="a7f71-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a7f71-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a7f71-105">Умножает два числа с фиксированной запятой в тактовые регистры.</span><span class="sxs-lookup"><span data-stu-id="a7f71-105">Multiplies two fixed-point numbers in quantum registers.</span></span>

```qsharp
operation MultiplyFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit
```


## <a name="input"></a><span data-ttu-id="a7f71-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a7f71-106">Input</span></span>

### <a name="fp1--fixedpoint"></a><span data-ttu-id="a7f71-107">FP1: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="a7f71-107">fp1 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="a7f71-108">Первое число с фиксированной запятой.</span><span class="sxs-lookup"><span data-stu-id="a7f71-108">First fixed-point number.</span></span>


### <a name="fp2--fixedpoint"></a><span data-ttu-id="a7f71-109">Fp2: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="a7f71-109">fp2 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="a7f71-110">Второе число с фиксированной запятой.</span><span class="sxs-lookup"><span data-stu-id="a7f71-110">Second fixed-point number.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="a7f71-111">результат: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="a7f71-111">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="a7f71-112">Число с фиксированной запятой результата должно быть в состоянии $ \кет {0} $ изначально.</span><span class="sxs-lookup"><span data-stu-id="a7f71-112">Result fixed-point number, must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a7f71-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a7f71-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="a7f71-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="a7f71-114">Remarks</span></span>

<span data-ttu-id="a7f71-115">Текущая реализация требует, чтобы три цифры с фиксированной запятой имели одинаковую позицию и одно и то же число Кубитс.</span><span class="sxs-lookup"><span data-stu-id="a7f71-115">The current implementation requires the three fixed-point numbers to have the same point position and the same number of qubits.</span></span>