---
uid: Microsoft.Quantum.Logical.GreaterThanI
title: Функция Греатерсани
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanI
qsharp.summary: Returns true if and only if a number is greater than another number.
ms.openlocfilehash: 06cae04150f9f0164b06a4e3d4bb78242b41dc0b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198016"
---
# <a name="greaterthani-function"></a><span data-ttu-id="cce02-102">Функция Греатерсани</span><span class="sxs-lookup"><span data-stu-id="cce02-102">GreaterThanI function</span></span>

<span data-ttu-id="cce02-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="cce02-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="cce02-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cce02-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cce02-105">Возвращает значение true только в том случае, если число больше, чем другое число.</span><span class="sxs-lookup"><span data-stu-id="cce02-105">Returns true if and only if a number is greater than another number.</span></span>

```qsharp
function GreaterThanI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="cce02-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="cce02-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="cce02-107">ответ. [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="cce02-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="cce02-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="cce02-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="cce02-109">б: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="cce02-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="cce02-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="cce02-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="cce02-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="cce02-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="cce02-112">`true` только в случае, если `a` строго больше `b` .</span><span class="sxs-lookup"><span data-stu-id="cce02-112">`true` if and only if `a` is strictly greater than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="cce02-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cce02-113">Remarks</span></span>

<span data-ttu-id="cce02-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="cce02-114">The following are equivalent:</span></span>

```Q#
let cond = a > b;
let cond = GreaterThanI(a, b);
```