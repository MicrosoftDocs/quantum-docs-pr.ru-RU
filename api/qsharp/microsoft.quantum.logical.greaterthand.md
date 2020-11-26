---
uid: Microsoft.Quantum.Logical.GreaterThanD
title: Функция Греатерсанд
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanD
qsharp.summary: Returns true if and only if a number is greater than another number.
ms.openlocfilehash: c23d85cf513bb6d37e67260eeeb3b81b42e6771a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198033"
---
# <a name="greaterthand-function"></a><span data-ttu-id="40dba-102">Функция Греатерсанд</span><span class="sxs-lookup"><span data-stu-id="40dba-102">GreaterThanD function</span></span>

<span data-ttu-id="40dba-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="40dba-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="40dba-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="40dba-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="40dba-105">Возвращает значение true только в том случае, если число больше, чем другое число.</span><span class="sxs-lookup"><span data-stu-id="40dba-105">Returns true if and only if a number is greater than another number.</span></span>

```qsharp
function GreaterThanD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="40dba-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="40dba-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="40dba-107">ответ. [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="40dba-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="40dba-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="40dba-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="40dba-109">б: [двойной](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="40dba-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="40dba-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="40dba-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="40dba-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="40dba-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="40dba-112">`true` только в случае, если `a` строго больше `b` .</span><span class="sxs-lookup"><span data-stu-id="40dba-112">`true` if and only if `a` is strictly greater than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="40dba-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="40dba-113">Remarks</span></span>

<span data-ttu-id="40dba-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="40dba-114">The following are equivalent:</span></span>

```Q#
let cond = a > b;
let cond = GreaterThanD(a, b);
```