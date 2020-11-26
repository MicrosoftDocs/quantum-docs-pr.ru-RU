---
uid: Microsoft.Quantum.Logical.EqualR
title: Функция Equals
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualR
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: d68b2f1a26bf318400d3c88b37d9aabcc38cbdfe
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198012"
---
# <a name="equalr-function"></a><span data-ttu-id="5167e-102">Функция Equals</span><span class="sxs-lookup"><span data-stu-id="5167e-102">EqualR function</span></span>

<span data-ttu-id="5167e-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="5167e-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="5167e-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5167e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5167e-105">Возвращает значение true только в том случае, если два входных значения равны.</span><span class="sxs-lookup"><span data-stu-id="5167e-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualR (a : Result, b : Result) : Bool
```


## <a name="input"></a><span data-ttu-id="5167e-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5167e-106">Input</span></span>

### <a name="a--__invalidresult__"></a><span data-ttu-id="5167e-107">ответ. __Недопустимый <Result>__</span><span class="sxs-lookup"><span data-stu-id="5167e-107">a : __invalid<Result>__</span></span>

<span data-ttu-id="5167e-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="5167e-108">The first value to be compared.</span></span>


### <a name="b--__invalidresult__"></a><span data-ttu-id="5167e-109">б: __недопустимо <Result>__</span><span class="sxs-lookup"><span data-stu-id="5167e-109">b : __invalid<Result>__</span></span>

<span data-ttu-id="5167e-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="5167e-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="5167e-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="5167e-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="5167e-112">`true` Если и, только если `a` равно `b` .</span><span class="sxs-lookup"><span data-stu-id="5167e-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="5167e-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5167e-113">Remarks</span></span>

<span data-ttu-id="5167e-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="5167e-114">The following are equivalent:</span></span>

```Q#
let cond = a == b;
let cond = EqualR(a, b);
```