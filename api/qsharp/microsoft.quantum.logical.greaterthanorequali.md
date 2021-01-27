---
uid: Microsoft.Quantum.Logical.GreaterThanOrEqualI
title: Функция Греатерсанорекуали
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanOrEqualI
qsharp.summary: Returns true if and only if a number is greater than or equal to another number.
ms.openlocfilehash: c1a513500c8a70bd7628976974387cba48162e80
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849184"
---
# <a name="greaterthanorequali-function"></a><span data-ttu-id="96822-102">Функция Греатерсанорекуали</span><span class="sxs-lookup"><span data-stu-id="96822-102">GreaterThanOrEqualI function</span></span>

<span data-ttu-id="96822-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="96822-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="96822-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="96822-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="96822-105">Возвращает значение true только в том случае, если число больше или равно другому числу.</span><span class="sxs-lookup"><span data-stu-id="96822-105">Returns true if and only if a number is greater than or equal to another number.</span></span>

```qsharp
function GreaterThanOrEqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="96822-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="96822-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="96822-107">ответ. [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="96822-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="96822-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="96822-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="96822-109">б: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="96822-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="96822-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="96822-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="96822-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="96822-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="96822-112">`true` значение и, только если `a` значение больше или равно `b` .</span><span class="sxs-lookup"><span data-stu-id="96822-112">`true` if and only if `a` is greater than or is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="96822-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="96822-113">Remarks</span></span>

<span data-ttu-id="96822-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="96822-114">The following are equivalent:</span></span>

```qsharp
let cond = a >= b;
let cond = GreaterThanOrEqualI(a, b);
```