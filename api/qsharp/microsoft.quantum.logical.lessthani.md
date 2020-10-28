---
uid: Microsoft.Quantum.Logical.LessThanI
title: Функция Лесссани
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanI
qsharp.summary: Returns true if and only if a number is less than another number.
ms.openlocfilehash: 204e62a87d2b3d0070946985030d038ead686457
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732921"
---
# <a name="lessthani-function"></a><span data-ttu-id="6f9e0-102">Функция Лесссани</span><span class="sxs-lookup"><span data-stu-id="6f9e0-102">LessThanI function</span></span>

<span data-ttu-id="6f9e0-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="6f9e0-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="6f9e0-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6f9e0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6f9e0-105">Возвращает значение true только в том случае, если число меньше, чем другое число.</span><span class="sxs-lookup"><span data-stu-id="6f9e0-105">Returns true if and only if a number is less than another number.</span></span>

```qsharp
function LessThanI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="6f9e0-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="6f9e0-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="6f9e0-107">ответ. [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6f9e0-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6f9e0-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="6f9e0-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="6f9e0-109">б: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6f9e0-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6f9e0-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="6f9e0-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="6f9e0-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="6f9e0-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="6f9e0-112">`true` Если и, только если `a` является строго меньшим `b` .</span><span class="sxs-lookup"><span data-stu-id="6f9e0-112">`true` if and only if `a` is strictly less than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f9e0-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="6f9e0-113">Remarks</span></span>

<span data-ttu-id="6f9e0-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="6f9e0-114">The following are equivalent:</span></span>

```Q#
let cond = a < b;
let cond = LessThanI(a, b);
```