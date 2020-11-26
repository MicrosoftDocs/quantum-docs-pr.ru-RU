---
uid: Microsoft.Quantum.Logical.GreaterThanL
title: Функция Греатерсанл
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanL
qsharp.summary: Returns true if and only if a number is greater than another number.
ms.openlocfilehash: 5e1b2adab36b7937c83ea912b8a9cb148b626ee5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197982"
---
# <a name="greaterthanl-function"></a><span data-ttu-id="a0cb6-102">Функция Греатерсанл</span><span class="sxs-lookup"><span data-stu-id="a0cb6-102">GreaterThanL function</span></span>

<span data-ttu-id="a0cb6-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="a0cb6-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="a0cb6-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a0cb6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a0cb6-105">Возвращает значение true только в том случае, если число больше, чем другое число.</span><span class="sxs-lookup"><span data-stu-id="a0cb6-105">Returns true if and only if a number is greater than another number.</span></span>

```qsharp
function GreaterThanL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="a0cb6-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a0cb6-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="a0cb6-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="a0cb6-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="a0cb6-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="a0cb6-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="a0cb6-109">б: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="a0cb6-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="a0cb6-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="a0cb6-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="a0cb6-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="a0cb6-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="a0cb6-112">`true` только в случае, если `a` строго больше `b` .</span><span class="sxs-lookup"><span data-stu-id="a0cb6-112">`true` if and only if `a` is strictly greater than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0cb6-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a0cb6-113">Remarks</span></span>

<span data-ttu-id="a0cb6-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="a0cb6-114">The following are equivalent:</span></span>

```Q#
let cond = a > b;
let cond = GreaterThanL(a, b);
```