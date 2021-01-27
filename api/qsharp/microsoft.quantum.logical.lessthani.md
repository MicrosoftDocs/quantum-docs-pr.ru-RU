---
uid: Microsoft.Quantum.Logical.LessThanI
title: Функция Лесссани
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanI
qsharp.summary: Returns true if and only if a number is less than another number.
ms.openlocfilehash: 69c3d7c414967b830c15189c895a2b34f409c7b3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98815837"
---
# <a name="lessthani-function"></a><span data-ttu-id="eaf5b-102">Функция Лесссани</span><span class="sxs-lookup"><span data-stu-id="eaf5b-102">LessThanI function</span></span>

<span data-ttu-id="eaf5b-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="eaf5b-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="eaf5b-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="eaf5b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="eaf5b-105">Возвращает значение true только в том случае, если число меньше, чем другое число.</span><span class="sxs-lookup"><span data-stu-id="eaf5b-105">Returns true if and only if a number is less than another number.</span></span>

```qsharp
function LessThanI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="eaf5b-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="eaf5b-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="eaf5b-107">ответ. [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="eaf5b-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="eaf5b-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="eaf5b-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="eaf5b-109">б: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="eaf5b-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="eaf5b-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="eaf5b-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="eaf5b-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="eaf5b-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="eaf5b-112">`true` Если и, только если `a` является строго меньшим `b` .</span><span class="sxs-lookup"><span data-stu-id="eaf5b-112">`true` if and only if `a` is strictly less than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="eaf5b-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="eaf5b-113">Remarks</span></span>

<span data-ttu-id="eaf5b-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="eaf5b-114">The following are equivalent:</span></span>

```qsharp
let cond = a < b;
let cond = LessThanI(a, b);
```