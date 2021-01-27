---
uid: Microsoft.Quantum.Logical.Or
title: Или, функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Or
qsharp.summary: Returns the Boolean disjunction of two values.
ms.openlocfilehash: 4a29b7684b28b904b43ccceb8e63280999690349
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848467"
---
# <a name="or-function"></a><span data-ttu-id="f4013-102">Или, функция</span><span class="sxs-lookup"><span data-stu-id="f4013-102">Or function</span></span>

<span data-ttu-id="f4013-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="f4013-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="f4013-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f4013-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f4013-105">Возвращает логическое сложение двух значений.</span><span class="sxs-lookup"><span data-stu-id="f4013-105">Returns the Boolean disjunction of two values.</span></span>

```qsharp
function Or (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="f4013-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f4013-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="f4013-107">ответ. [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="f4013-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="f4013-108">Первое значение, которое необходимо считать.</span><span class="sxs-lookup"><span data-stu-id="f4013-108">The first value to be considered.</span></span>


### <a name="b--bool"></a><span data-ttu-id="f4013-109">б: [логическое](xref:microsoft.quantum.lang-ref.bool) значение</span><span class="sxs-lookup"><span data-stu-id="f4013-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="f4013-110">Второе значение, которое необходимо считать.</span><span class="sxs-lookup"><span data-stu-id="f4013-110">The second value to be considered.</span></span>



## <a name="output--bool"></a><span data-ttu-id="f4013-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="f4013-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="f4013-112">`true` Если и, и только в том случае `a` , если имеет значение или `b` `true` .</span><span class="sxs-lookup"><span data-stu-id="f4013-112">`true` if and only if either `a` or `b` are `true`.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4013-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="f4013-113">Remarks</span></span>

<span data-ttu-id="f4013-114">В отличие от `or` оператора, эта функция не является сокращенной, так что оба входа полностью оцениваются.</span><span class="sxs-lookup"><span data-stu-id="f4013-114">Unlike the `or` operator, this function does not short-circuit, such that both inputs are fully evaluated.</span></span>

<span data-ttu-id="f4013-115">Ниже приведены эквивалентные действия для сокращенного поведения.</span><span class="sxs-lookup"><span data-stu-id="f4013-115">Up to short-circuiting behavior, the following are equivalent:</span></span>

```qsharp
let x = a or b;
let x = Or(a, b);
```