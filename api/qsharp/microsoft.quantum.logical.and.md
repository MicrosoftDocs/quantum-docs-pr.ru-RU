---
uid: Microsoft.Quantum.Logical.And
title: Функции и
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: And
qsharp.summary: Returns the Boolean conjunction of two values.
ms.openlocfilehash: cc81f650216c4db219a79c4fe89a42447a4e95b8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731304"
---
# <a name="and-function"></a><span data-ttu-id="7c151-102">Функции и</span><span class="sxs-lookup"><span data-stu-id="7c151-102">And function</span></span>

<span data-ttu-id="7c151-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="7c151-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="7c151-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7c151-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7c151-105">Возвращает логическое значение, умноженное на два значения.</span><span class="sxs-lookup"><span data-stu-id="7c151-105">Returns the Boolean conjunction of two values.</span></span>

```qsharp
function And (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="7c151-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7c151-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="7c151-107">ответ. [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="7c151-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="7c151-108">Первое значение, которое необходимо считать.</span><span class="sxs-lookup"><span data-stu-id="7c151-108">The first value to be considered.</span></span>


### <a name="b--bool"></a><span data-ttu-id="7c151-109">б: [логическое](xref:microsoft.quantum.lang-ref.bool) значение</span><span class="sxs-lookup"><span data-stu-id="7c151-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="7c151-110">Второе значение, которое необходимо считать.</span><span class="sxs-lookup"><span data-stu-id="7c151-110">The second value to be considered.</span></span>



## <a name="output--bool"></a><span data-ttu-id="7c151-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="7c151-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="7c151-112">`true` значение, только если `a` и `b` `true` .</span><span class="sxs-lookup"><span data-stu-id="7c151-112">`true` if and only if `a` and `b` are both `true`.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c151-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="7c151-113">Remarks</span></span>

<span data-ttu-id="7c151-114">В отличие от `and` оператора, эта функция не является сокращенной, так что оба входа полностью оцениваются.</span><span class="sxs-lookup"><span data-stu-id="7c151-114">Unlike the `and` operator, this function does not short-circuit, such that both inputs are fully evaluated.</span></span>

<span data-ttu-id="7c151-115">Ниже приведены эквивалентные действия для сокращенного поведения.</span><span class="sxs-lookup"><span data-stu-id="7c151-115">Up to short-circuiting behavior, the following are equivalent:</span></span>

```Q#
let x = a and b;
let x = And(a, b);
```