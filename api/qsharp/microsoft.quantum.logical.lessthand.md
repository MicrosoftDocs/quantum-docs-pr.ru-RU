---
uid: Microsoft.Quantum.Logical.LessThanD
title: Функция Лесссанд
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanD
qsharp.summary: Returns true if and only if a number is less than another number.
ms.openlocfilehash: 7135ed4b3414d143f5020496ae524bf89980a8a1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849158"
---
# <a name="lessthand-function"></a><span data-ttu-id="5fafa-102">Функция Лесссанд</span><span class="sxs-lookup"><span data-stu-id="5fafa-102">LessThanD function</span></span>

<span data-ttu-id="5fafa-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="5fafa-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="5fafa-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5fafa-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5fafa-105">Возвращает значение true только в том случае, если число меньше, чем другое число.</span><span class="sxs-lookup"><span data-stu-id="5fafa-105">Returns true if and only if a number is less than another number.</span></span>

```qsharp
function LessThanD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="5fafa-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5fafa-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="5fafa-107">ответ. [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5fafa-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="5fafa-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="5fafa-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="5fafa-109">б: [двойной](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5fafa-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="5fafa-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="5fafa-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="5fafa-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="5fafa-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="5fafa-112">`true` Если и, только если `a` является строго меньшим `b` .</span><span class="sxs-lookup"><span data-stu-id="5fafa-112">`true` if and only if `a` is strictly less than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fafa-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="5fafa-113">Remarks</span></span>

<span data-ttu-id="5fafa-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="5fafa-114">The following are equivalent:</span></span>

```qsharp
let cond = a < b;
let cond = LessThanD(a, b);
```