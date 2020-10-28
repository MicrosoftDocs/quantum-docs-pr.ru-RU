---
uid: Microsoft.Quantum.Arithmetic.CompareGreaterThanFxP
title: Операция Компарегреатерсанфксп
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGreaterThanFxP
qsharp.summary: Compares two fixed-point numbers stored in quantum registers, and controls a flip on the result.
ms.openlocfilehash: bd3bcedd7a4a81fc600f7f4b6bdf1d2a797abbd4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731633"
---
# <a name="comparegreaterthanfxp-operation"></a><span data-ttu-id="d6e16-102">Операция Компарегреатерсанфксп</span><span class="sxs-lookup"><span data-stu-id="d6e16-102">CompareGreaterThanFxP operation</span></span>

<span data-ttu-id="d6e16-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="d6e16-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="d6e16-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d6e16-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d6e16-105">Сравнивает два числа с фиксированной запятой, хранящихся в тактовых регистрах, и управляет отражением результата.</span><span class="sxs-lookup"><span data-stu-id="d6e16-105">Compares two fixed-point numbers stored in quantum registers, and controls a flip on the result.</span></span>

```qsharp
operation CompareGreaterThanFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint, result : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="d6e16-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d6e16-106">Input</span></span>

### <a name="fp1--fixedpoint"></a><span data-ttu-id="d6e16-107">FP1: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="d6e16-107">fp1 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="d6e16-108">Первое сравниваемое число с фиксированной запятой.</span><span class="sxs-lookup"><span data-stu-id="d6e16-108">First fixed-point number to be compared.</span></span>


### <a name="fp2--fixedpoint"></a><span data-ttu-id="d6e16-109">Fp2: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="d6e16-109">fp2 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="d6e16-110">Второе сравниваемое число с фиксированной запятой.</span><span class="sxs-lookup"><span data-stu-id="d6e16-110">Second fixed-point number to be compared.</span></span>


### <a name="result--qubit"></a><span data-ttu-id="d6e16-111">результат: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="d6e16-111">result : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="d6e16-112">Результат сравнения.</span><span class="sxs-lookup"><span data-stu-id="d6e16-112">Result of the comparison.</span></span> <span data-ttu-id="d6e16-113">Будет отражено, если `fp1 > fp2` .</span><span class="sxs-lookup"><span data-stu-id="d6e16-113">Will be flipped if `fp1 > fp2`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d6e16-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d6e16-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="d6e16-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="d6e16-115">Remarks</span></span>

<span data-ttu-id="d6e16-116">Текущая реализация требует, чтобы два числа с фиксированной запятой имели одно и то же расположение точки и одно и то же число Кубитс.</span><span class="sxs-lookup"><span data-stu-id="d6e16-116">The current implementation requires the two fixed-point numbers to have the same point position and the same number of qubits.</span></span>