---
uid: Microsoft.Quantum.Logical.EqualI
title: Функция Екуали
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualI
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: be92ef2b63981094e1a95c38e02de95c3c2bbf3a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198169"
---
# <a name="equali-function"></a><span data-ttu-id="8ad28-102">Функция Екуали</span><span class="sxs-lookup"><span data-stu-id="8ad28-102">EqualI function</span></span>

<span data-ttu-id="8ad28-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="8ad28-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="8ad28-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8ad28-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8ad28-105">Возвращает значение true только в том случае, если два входных значения равны.</span><span class="sxs-lookup"><span data-stu-id="8ad28-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="8ad28-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="8ad28-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="8ad28-107">ответ. [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8ad28-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8ad28-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="8ad28-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="8ad28-109">б: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8ad28-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8ad28-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="8ad28-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="8ad28-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="8ad28-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="8ad28-112">`true` Если и, только если `a` равно `b` .</span><span class="sxs-lookup"><span data-stu-id="8ad28-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ad28-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8ad28-113">Remarks</span></span>

<span data-ttu-id="8ad28-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="8ad28-114">The following are equivalent:</span></span>

```Q#
let cond = a == b;
let cond = EqualI(a, b);
```