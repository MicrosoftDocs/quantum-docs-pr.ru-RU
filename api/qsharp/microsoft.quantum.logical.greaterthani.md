---
uid: Microsoft.Quantum.Logical.GreaterThanI
title: Функция Греатерсани
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanI
qsharp.summary: Returns true if and only if a number is greater than another number.
ms.openlocfilehash: 86fc8e927c292a2ea814ed80a33de42bffdb96b1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98815958"
---
# <a name="greaterthani-function"></a><span data-ttu-id="f94b6-102">Функция Греатерсани</span><span class="sxs-lookup"><span data-stu-id="f94b6-102">GreaterThanI function</span></span>

<span data-ttu-id="f94b6-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="f94b6-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="f94b6-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f94b6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f94b6-105">Возвращает значение true только в том случае, если число больше, чем другое число.</span><span class="sxs-lookup"><span data-stu-id="f94b6-105">Returns true if and only if a number is greater than another number.</span></span>

```qsharp
function GreaterThanI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="f94b6-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f94b6-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="f94b6-107">ответ. [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f94b6-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f94b6-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="f94b6-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="f94b6-109">б: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f94b6-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f94b6-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="f94b6-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="f94b6-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="f94b6-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="f94b6-112">`true` только в случае, если `a` строго больше `b` .</span><span class="sxs-lookup"><span data-stu-id="f94b6-112">`true` if and only if `a` is strictly greater than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="f94b6-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="f94b6-113">Remarks</span></span>

<span data-ttu-id="f94b6-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="f94b6-114">The following are equivalent:</span></span>

```qsharp
let cond = a > b;
let cond = GreaterThanI(a, b);
```