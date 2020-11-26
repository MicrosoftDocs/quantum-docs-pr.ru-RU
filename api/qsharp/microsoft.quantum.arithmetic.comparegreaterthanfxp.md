---
uid: Microsoft.Quantum.Arithmetic.CompareGreaterThanFxP
title: Операция Компарегреатерсанфксп
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGreaterThanFxP
qsharp.summary: Compares two fixed-point numbers stored in quantum registers, and controls a flip on the result.
ms.openlocfilehash: 1e9afc7645f62b932fa8ebc3d33e21a2a5182361
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223533"
---
# <a name="comparegreaterthanfxp-operation"></a><span data-ttu-id="43774-102">Операция Компарегреатерсанфксп</span><span class="sxs-lookup"><span data-stu-id="43774-102">CompareGreaterThanFxP operation</span></span>

<span data-ttu-id="43774-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="43774-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="43774-104">Пакет: [Microsoft. тактов. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="43774-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="43774-105">Сравнивает два числа с фиксированной запятой, хранящихся в тактовых регистрах, и управляет отражением результата.</span><span class="sxs-lookup"><span data-stu-id="43774-105">Compares two fixed-point numbers stored in quantum registers, and controls a flip on the result.</span></span>

```qsharp
operation CompareGreaterThanFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint, result : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="43774-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="43774-106">Input</span></span>

### <a name="fp1--fixedpoint"></a><span data-ttu-id="43774-107">FP1: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="43774-107">fp1 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="43774-108">Первое сравниваемое число с фиксированной запятой.</span><span class="sxs-lookup"><span data-stu-id="43774-108">First fixed-point number to be compared.</span></span>


### <a name="fp2--fixedpoint"></a><span data-ttu-id="43774-109">Fp2: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="43774-109">fp2 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="43774-110">Второе сравниваемое число с фиксированной запятой.</span><span class="sxs-lookup"><span data-stu-id="43774-110">Second fixed-point number to be compared.</span></span>


### <a name="result--qubit"></a><span data-ttu-id="43774-111">результат: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="43774-111">result : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="43774-112">Результат сравнения.</span><span class="sxs-lookup"><span data-stu-id="43774-112">Result of the comparison.</span></span> <span data-ttu-id="43774-113">Будет отражено, если `fp1 > fp2` .</span><span class="sxs-lookup"><span data-stu-id="43774-113">Will be flipped if `fp1 > fp2`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="43774-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="43774-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="43774-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="43774-115">Remarks</span></span>

<span data-ttu-id="43774-116">Текущая реализация требует, чтобы два числа с фиксированной запятой имели одно и то же расположение точки и одно и то же число Кубитс.</span><span class="sxs-lookup"><span data-stu-id="43774-116">The current implementation requires the two fixed-point numbers to have the same point position and the same number of qubits.</span></span>