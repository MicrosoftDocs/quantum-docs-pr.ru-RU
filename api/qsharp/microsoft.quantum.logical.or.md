---
uid: Microsoft.Quantum.Logical.Or
title: Или, функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Or
qsharp.summary: Returns the Boolean disjunction of two values.
ms.openlocfilehash: 98a416229386461b241d087b7ae95f078f8be70a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730753"
---
# <a name="or-function"></a><span data-ttu-id="8642b-102">Или, функция</span><span class="sxs-lookup"><span data-stu-id="8642b-102">Or function</span></span>

<span data-ttu-id="8642b-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="8642b-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="8642b-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8642b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8642b-105">Возвращает логическое сложение двух значений.</span><span class="sxs-lookup"><span data-stu-id="8642b-105">Returns the Boolean disjunction of two values.</span></span>

```qsharp
function Or (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="8642b-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="8642b-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="8642b-107">ответ. [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="8642b-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="8642b-108">Первое значение, которое необходимо считать.</span><span class="sxs-lookup"><span data-stu-id="8642b-108">The first value to be considered.</span></span>


### <a name="b--bool"></a><span data-ttu-id="8642b-109">б: [логическое](xref:microsoft.quantum.lang-ref.bool) значение</span><span class="sxs-lookup"><span data-stu-id="8642b-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="8642b-110">Второе значение, которое необходимо считать.</span><span class="sxs-lookup"><span data-stu-id="8642b-110">The second value to be considered.</span></span>



## <a name="output--bool"></a><span data-ttu-id="8642b-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="8642b-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="8642b-112">`true` Если и, и только в том случае `a` , если имеет значение или `b` `true` .</span><span class="sxs-lookup"><span data-stu-id="8642b-112">`true` if and only if either `a` or `b` are `true`.</span></span>

## <a name="remarks"></a><span data-ttu-id="8642b-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="8642b-113">Remarks</span></span>

<span data-ttu-id="8642b-114">В отличие от `or` оператора, эта функция не является сокращенной, так что оба входа полностью оцениваются.</span><span class="sxs-lookup"><span data-stu-id="8642b-114">Unlike the `or` operator, this function does not short-circuit, such that both inputs are fully evaluated.</span></span>

<span data-ttu-id="8642b-115">Ниже приведены эквивалентные действия для сокращенного поведения.</span><span class="sxs-lookup"><span data-stu-id="8642b-115">Up to short-circuiting behavior, the following are equivalent:</span></span>

```Q#
let x = a or b;
let x = Or(a, b);
```