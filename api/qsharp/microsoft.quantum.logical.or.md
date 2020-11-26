---
uid: Microsoft.Quantum.Logical.Or
title: Или, функция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Or
qsharp.summary: Returns the Boolean disjunction of two values.
ms.openlocfilehash: 7093d908696a8cfda6b5ef648f9dfafcfac97144
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197132"
---
# <a name="or-function"></a><span data-ttu-id="390d4-102">Или, функция</span><span class="sxs-lookup"><span data-stu-id="390d4-102">Or function</span></span>

<span data-ttu-id="390d4-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="390d4-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="390d4-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="390d4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="390d4-105">Возвращает логическое сложение двух значений.</span><span class="sxs-lookup"><span data-stu-id="390d4-105">Returns the Boolean disjunction of two values.</span></span>

```qsharp
function Or (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="390d4-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="390d4-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="390d4-107">ответ. [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="390d4-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="390d4-108">Первое значение, которое необходимо считать.</span><span class="sxs-lookup"><span data-stu-id="390d4-108">The first value to be considered.</span></span>


### <a name="b--bool"></a><span data-ttu-id="390d4-109">б: [логическое](xref:microsoft.quantum.lang-ref.bool) значение</span><span class="sxs-lookup"><span data-stu-id="390d4-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="390d4-110">Второе значение, которое необходимо считать.</span><span class="sxs-lookup"><span data-stu-id="390d4-110">The second value to be considered.</span></span>



## <a name="output--bool"></a><span data-ttu-id="390d4-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="390d4-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="390d4-112">`true` Если и, и только в том случае `a` , если имеет значение или `b` `true` .</span><span class="sxs-lookup"><span data-stu-id="390d4-112">`true` if and only if either `a` or `b` are `true`.</span></span>

## <a name="remarks"></a><span data-ttu-id="390d4-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="390d4-113">Remarks</span></span>

<span data-ttu-id="390d4-114">В отличие от `or` оператора, эта функция не является сокращенной, так что оба входа полностью оцениваются.</span><span class="sxs-lookup"><span data-stu-id="390d4-114">Unlike the `or` operator, this function does not short-circuit, such that both inputs are fully evaluated.</span></span>

<span data-ttu-id="390d4-115">Ниже приведены эквивалентные действия для сокращенного поведения.</span><span class="sxs-lookup"><span data-stu-id="390d4-115">Up to short-circuiting behavior, the following are equivalent:</span></span>

```Q#
let x = a or b;
let x = Or(a, b);
```