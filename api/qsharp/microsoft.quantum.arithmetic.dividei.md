---
uid: Microsoft.Quantum.Arithmetic.DivideI
title: Операция Дивидеи
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: DivideI
qsharp.summary: Divides two quantum integers.
ms.openlocfilehash: 73c4e394ca38b8089b2990f8a8b6a3ee50f644d8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846682"
---
# <a name="dividei-operation"></a><span data-ttu-id="bc750-102">Операция Дивидеи</span><span class="sxs-lookup"><span data-stu-id="bc750-102">DivideI operation</span></span>

<span data-ttu-id="bc750-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="bc750-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="bc750-104">Пакет: [Microsoft. тактов. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="bc750-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="bc750-105">Делит два целочисленных целых числа.</span><span class="sxs-lookup"><span data-stu-id="bc750-105">Divides two quantum integers.</span></span>

```qsharp
operation DivideI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="bc750-106">Описание</span><span class="sxs-lookup"><span data-stu-id="bc750-106">Description</span></span>

<span data-ttu-id="bc750-107">`xs` будет содержать остаток `xs - floor(xs/ys) * ys` и `result` будет содержать `floor(xs/ys)` .</span><span class="sxs-lookup"><span data-stu-id="bc750-107">`xs` will hold the remainder `xs - floor(xs/ys) * ys` and `result` will hold `floor(xs/ys)`.</span></span>

## <a name="input"></a><span data-ttu-id="bc750-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="bc750-108">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="bc750-109">xs: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="bc750-109">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="bc750-110">$n $-bit делимое будет заменено остатком.</span><span class="sxs-lookup"><span data-stu-id="bc750-110">$n$-bit dividend, will be replaced by the remainder.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="bc750-111">ИС: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="bc750-111">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="bc750-112">$n $-разрядный делитель</span><span class="sxs-lookup"><span data-stu-id="bc750-112">$n$-bit divisor</span></span>


### <a name="result--littleendian"></a><span data-ttu-id="bc750-113">результат: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="bc750-113">result : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="bc750-114">$n $-разрядный результат, должен находиться в состоянии $ \кет {0} $ изначально и заменяться результатом целочисленного деления.</span><span class="sxs-lookup"><span data-stu-id="bc750-114">$n$-bit result, must be in state $\ket{0}$ initially and will be replaced by the result of the integer division.</span></span>



## <a name="output--unit"></a><span data-ttu-id="bc750-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bc750-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="bc750-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="bc750-116">Remarks</span></span>

<span data-ttu-id="bc750-117">Использует стандартный подход с сдвигом и вычитанием для реализации деления.</span><span class="sxs-lookup"><span data-stu-id="bc750-117">Uses a standard shift-and-subtract approach to implement the division.</span></span>
<span data-ttu-id="bc750-118">Контролируемая версия является специализированной, поэтому вычитание не требует дополнительных элементов управления.</span><span class="sxs-lookup"><span data-stu-id="bc750-118">The controlled version is specialized such the subtraction does not require additional controls.</span></span>