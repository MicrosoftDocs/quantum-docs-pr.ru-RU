---
uid: Microsoft.Quantum.Logical.NotEqualR
title: Функция Нотекуалр
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualR
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 39601396a75d8c1b9193d4b8f34fa05466beff06
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848502"
---
# <a name="notequalr-function"></a><span data-ttu-id="465f8-102">Функция Нотекуалр</span><span class="sxs-lookup"><span data-stu-id="465f8-102">NotEqualR function</span></span>

<span data-ttu-id="465f8-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="465f8-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="465f8-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="465f8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="465f8-105">Возвращает значение true только в том случае, если два входных значения не равны.</span><span class="sxs-lookup"><span data-stu-id="465f8-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualR (a : Result, b : Result) : Bool
```


## <a name="input"></a><span data-ttu-id="465f8-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="465f8-106">Input</span></span>

### <a name="a--__invalidresult__"></a><span data-ttu-id="465f8-107">ответ. __Недопустимый <Result>__</span><span class="sxs-lookup"><span data-stu-id="465f8-107">a : __invalid<Result>__</span></span>

<span data-ttu-id="465f8-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="465f8-108">The first value to be compared.</span></span>


### <a name="b--__invalidresult__"></a><span data-ttu-id="465f8-109">б: __недопустимо <Result>__</span><span class="sxs-lookup"><span data-stu-id="465f8-109">b : __invalid<Result>__</span></span>

<span data-ttu-id="465f8-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="465f8-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="465f8-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="465f8-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="465f8-112">`true` Если и, только если `a` не равно `b` .</span><span class="sxs-lookup"><span data-stu-id="465f8-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="465f8-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="465f8-113">Remarks</span></span>

<span data-ttu-id="465f8-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="465f8-114">The following are equivalent:</span></span>

```qsharp
let cond = a != b;
let cond = NotEqualR(a, b);
```