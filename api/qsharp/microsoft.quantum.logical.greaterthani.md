---
uid: Microsoft.Quantum.Logical.GreaterThanI
title: Функция Греатерсани
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanI
qsharp.summary: Returns true if and only if a number is greater than another number.
ms.openlocfilehash: ffd00d8086654a2d783a351fe254fb2ee35b9184
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709980"
---
# <a name="greaterthani-function"></a><span data-ttu-id="bbd82-102">Функция Греатерсани</span><span class="sxs-lookup"><span data-stu-id="bbd82-102">GreaterThanI function</span></span>

<span data-ttu-id="bbd82-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="bbd82-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="bbd82-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="bbd82-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="bbd82-105">Возвращает значение true только в том случае, если число больше, чем другое число.</span><span class="sxs-lookup"><span data-stu-id="bbd82-105">Returns true if and only if a number is greater than another number.</span></span>

```qsharp
function GreaterThanI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="bbd82-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="bbd82-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="bbd82-107">ответ. [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="bbd82-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="bbd82-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="bbd82-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="bbd82-109">б: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="bbd82-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="bbd82-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="bbd82-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="bbd82-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="bbd82-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="bbd82-112">`true` только в случае, если `a` строго больше `b` .</span><span class="sxs-lookup"><span data-stu-id="bbd82-112">`true` if and only if `a` is strictly greater than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbd82-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="bbd82-113">Remarks</span></span>

<span data-ttu-id="bbd82-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="bbd82-114">The following are equivalent:</span></span>

```Q#
let cond = a > b;
let cond = GreaterThanI(a, b);
```