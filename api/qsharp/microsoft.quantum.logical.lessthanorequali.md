---
uid: Microsoft.Quantum.Logical.LessThanOrEqualI
title: Функция Лесссанорекуали
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanOrEqualI
qsharp.summary: Returns true if and only if a number is less than or equal to another number.
ms.openlocfilehash: b2974c9bc84d0b4366767f47682ab542f85063e2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197572"
---
# <a name="lessthanorequali-function"></a><span data-ttu-id="dc2bf-102">Функция Лесссанорекуали</span><span class="sxs-lookup"><span data-stu-id="dc2bf-102">LessThanOrEqualI function</span></span>

<span data-ttu-id="dc2bf-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="dc2bf-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="dc2bf-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="dc2bf-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="dc2bf-105">Возвращает значение true только в том случае, если число меньше или равно другому числу.</span><span class="sxs-lookup"><span data-stu-id="dc2bf-105">Returns true if and only if a number is less than or equal to another number.</span></span>

```qsharp
function LessThanOrEqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="dc2bf-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="dc2bf-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="dc2bf-107">ответ. [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="dc2bf-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="dc2bf-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="dc2bf-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="dc2bf-109">б: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="dc2bf-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="dc2bf-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="dc2bf-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="dc2bf-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="dc2bf-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="dc2bf-112">`true` только в случае, если `a` меньше или равно `b` .</span><span class="sxs-lookup"><span data-stu-id="dc2bf-112">`true` if and only if `a` is less than or equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc2bf-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dc2bf-113">Remarks</span></span>

<span data-ttu-id="dc2bf-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="dc2bf-114">The following are equivalent:</span></span>

```Q#
let cond = a <= b;
let cond = LessThanOrEqualI(a, b);
```