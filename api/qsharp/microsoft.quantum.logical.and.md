---
uid: Microsoft.Quantum.Logical.And
title: Функции и
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: And
qsharp.summary: Returns the Boolean conjunction of two values.
ms.openlocfilehash: 6c405bdb4182cc7f32bd04952dec25a974c03445
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849227"
---
# <a name="and-function"></a><span data-ttu-id="5d78b-102">Функции и</span><span class="sxs-lookup"><span data-stu-id="5d78b-102">And function</span></span>

<span data-ttu-id="5d78b-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="5d78b-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="5d78b-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5d78b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5d78b-105">Возвращает логическое значение, умноженное на два значения.</span><span class="sxs-lookup"><span data-stu-id="5d78b-105">Returns the Boolean conjunction of two values.</span></span>

```qsharp
function And (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="5d78b-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5d78b-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="5d78b-107">ответ. [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="5d78b-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="5d78b-108">Первое значение, которое необходимо считать.</span><span class="sxs-lookup"><span data-stu-id="5d78b-108">The first value to be considered.</span></span>


### <a name="b--bool"></a><span data-ttu-id="5d78b-109">б: [логическое](xref:microsoft.quantum.lang-ref.bool) значение</span><span class="sxs-lookup"><span data-stu-id="5d78b-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="5d78b-110">Второе значение, которое необходимо считать.</span><span class="sxs-lookup"><span data-stu-id="5d78b-110">The second value to be considered.</span></span>



## <a name="output--bool"></a><span data-ttu-id="5d78b-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="5d78b-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="5d78b-112">`true` значение, только если `a` и `b` `true` .</span><span class="sxs-lookup"><span data-stu-id="5d78b-112">`true` if and only if `a` and `b` are both `true`.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d78b-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="5d78b-113">Remarks</span></span>

<span data-ttu-id="5d78b-114">В отличие от `and` оператора, эта функция не является сокращенной, так что оба входа полностью оцениваются.</span><span class="sxs-lookup"><span data-stu-id="5d78b-114">Unlike the `and` operator, this function does not short-circuit, such that both inputs are fully evaluated.</span></span>

<span data-ttu-id="5d78b-115">Ниже приведены эквивалентные действия для сокращенного поведения.</span><span class="sxs-lookup"><span data-stu-id="5d78b-115">Up to short-circuiting behavior, the following are equivalent:</span></span>

```qsharp
let x = a and b;
let x = And(a, b);
```