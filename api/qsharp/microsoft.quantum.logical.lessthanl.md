---
uid: Microsoft.Quantum.Logical.LessThanL
title: Функция Лесссанл
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanL
qsharp.summary: Returns true if and only if a number is less than another number.
ms.openlocfilehash: 9a0678569596ac188c87c3944f3759783fcc77ee
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197727"
---
# <a name="lessthanl-function"></a><span data-ttu-id="a63c2-102">Функция Лесссанл</span><span class="sxs-lookup"><span data-stu-id="a63c2-102">LessThanL function</span></span>

<span data-ttu-id="a63c2-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="a63c2-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="a63c2-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a63c2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a63c2-105">Возвращает значение true только в том случае, если число меньше, чем другое число.</span><span class="sxs-lookup"><span data-stu-id="a63c2-105">Returns true if and only if a number is less than another number.</span></span>

```qsharp
function LessThanL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="a63c2-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a63c2-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="a63c2-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="a63c2-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="a63c2-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="a63c2-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="a63c2-109">б: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="a63c2-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="a63c2-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="a63c2-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="a63c2-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="a63c2-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="a63c2-112">`true` Если и, только если `a` является строго меньшим `b` .</span><span class="sxs-lookup"><span data-stu-id="a63c2-112">`true` if and only if `a` is strictly less than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="a63c2-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a63c2-113">Remarks</span></span>

<span data-ttu-id="a63c2-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="a63c2-114">The following are equivalent:</span></span>

```Q#
let cond = a < b;
let cond = LessThanL(a, b);
```