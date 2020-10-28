---
uid: Microsoft.Quantum.Arithmetic.DivideI
title: Операция Дивидеи
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: DivideI
qsharp.summary: Divides two quantum integers.
ms.openlocfilehash: 0cc16dddc27a000dbc30de6ae27976a01fd9f4ed
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731584"
---
# <a name="dividei-operation"></a><span data-ttu-id="9e6db-102">Операция Дивидеи</span><span class="sxs-lookup"><span data-stu-id="9e6db-102">DivideI operation</span></span>

<span data-ttu-id="9e6db-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="9e6db-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="9e6db-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9e6db-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9e6db-105">Делит два целочисленных целых числа.</span><span class="sxs-lookup"><span data-stu-id="9e6db-105">Divides two quantum integers.</span></span>

```qsharp
operation DivideI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="9e6db-106">Описание</span><span class="sxs-lookup"><span data-stu-id="9e6db-106">Description</span></span>

<span data-ttu-id="9e6db-107">`xs` будет содержать остаток `xs - floor(xs/ys) * ys` и `result` будет содержать `floor(xs/ys)` .</span><span class="sxs-lookup"><span data-stu-id="9e6db-107">`xs` will hold the remainder `xs - floor(xs/ys) * ys` and `result` will hold `floor(xs/ys)`.</span></span>

## <a name="input"></a><span data-ttu-id="9e6db-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="9e6db-108">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="9e6db-109">xs: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="9e6db-109">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="9e6db-110">$n $-bit делимое будет заменено остатком.</span><span class="sxs-lookup"><span data-stu-id="9e6db-110">$n$-bit dividend, will be replaced by the remainder.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="9e6db-111">ИС: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="9e6db-111">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="9e6db-112">$n $-разрядный делитель</span><span class="sxs-lookup"><span data-stu-id="9e6db-112">$n$-bit divisor</span></span>


### <a name="result--littleendian"></a><span data-ttu-id="9e6db-113">результат: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="9e6db-113">result : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="9e6db-114">$n $-разрядный результат, должен находиться в состоянии $ \кет {0} $ изначально и заменяться результатом целочисленного деления.</span><span class="sxs-lookup"><span data-stu-id="9e6db-114">$n$-bit result, must be in state $\ket{0}$ initially and will be replaced by the result of the integer division.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9e6db-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9e6db-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="9e6db-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="9e6db-116">Remarks</span></span>

<span data-ttu-id="9e6db-117">Использует стандартный подход с сдвигом и вычитанием для реализации деления.</span><span class="sxs-lookup"><span data-stu-id="9e6db-117">Uses a standard shift-and-subtract approach to implement the division.</span></span>
<span data-ttu-id="9e6db-118">Контролируемая версия является специализированной, поэтому вычитание не требует дополнительных элементов управления.</span><span class="sxs-lookup"><span data-stu-id="9e6db-118">The controlled version is specialized such the subtraction does not require additional controls.</span></span>