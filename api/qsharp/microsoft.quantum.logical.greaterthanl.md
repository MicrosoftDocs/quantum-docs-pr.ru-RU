---
uid: Microsoft.Quantum.Logical.GreaterThanL
title: Функция Греатерсанл
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanL
qsharp.summary: Returns true if and only if a number is greater than another number.
ms.openlocfilehash: 676defa7824e53578504c559c6d8f24b2ffc1a88
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711380"
---
# <a name="greaterthanl-function"></a><span data-ttu-id="4cece-102">Функция Греатерсанл</span><span class="sxs-lookup"><span data-stu-id="4cece-102">GreaterThanL function</span></span>

<span data-ttu-id="4cece-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="4cece-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="4cece-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4cece-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4cece-105">Возвращает значение true только в том случае, если число больше, чем другое число.</span><span class="sxs-lookup"><span data-stu-id="4cece-105">Returns true if and only if a number is greater than another number.</span></span>

```qsharp
function GreaterThanL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="4cece-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="4cece-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="4cece-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="4cece-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="4cece-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="4cece-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="4cece-109">б: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="4cece-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="4cece-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="4cece-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="4cece-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="4cece-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="4cece-112">`true` только в случае, если `a` строго больше `b` .</span><span class="sxs-lookup"><span data-stu-id="4cece-112">`true` if and only if `a` is strictly greater than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cece-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="4cece-113">Remarks</span></span>

<span data-ttu-id="4cece-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="4cece-114">The following are equivalent:</span></span>

```Q#
let cond = a > b;
let cond = GreaterThanL(a, b);
```