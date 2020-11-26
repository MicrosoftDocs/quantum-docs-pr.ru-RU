---
uid: Microsoft.Quantum.Logical.LessThanI
title: Функция Лесссани
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanI
qsharp.summary: Returns true if and only if a number is less than another number.
ms.openlocfilehash: 5d5b17c8481ccf58b8e4fc4bb958e0adbf6d8f00
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197778"
---
# <a name="lessthani-function"></a><span data-ttu-id="d7cfc-102">Функция Лесссани</span><span class="sxs-lookup"><span data-stu-id="d7cfc-102">LessThanI function</span></span>

<span data-ttu-id="d7cfc-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="d7cfc-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="d7cfc-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d7cfc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d7cfc-105">Возвращает значение true только в том случае, если число меньше, чем другое число.</span><span class="sxs-lookup"><span data-stu-id="d7cfc-105">Returns true if and only if a number is less than another number.</span></span>

```qsharp
function LessThanI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="d7cfc-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d7cfc-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="d7cfc-107">ответ. [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d7cfc-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d7cfc-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="d7cfc-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="d7cfc-109">б: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d7cfc-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d7cfc-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="d7cfc-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="d7cfc-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="d7cfc-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="d7cfc-112">`true` Если и, только если `a` является строго меньшим `b` .</span><span class="sxs-lookup"><span data-stu-id="d7cfc-112">`true` if and only if `a` is strictly less than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7cfc-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d7cfc-113">Remarks</span></span>

<span data-ttu-id="d7cfc-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="d7cfc-114">The following are equivalent:</span></span>

```Q#
let cond = a < b;
let cond = LessThanI(a, b);
```