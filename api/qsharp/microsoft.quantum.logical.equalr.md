---
uid: Microsoft.Quantum.Logical.EqualR
title: Функция Equals
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualR
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 5aaa17303d75b27c3ac82cbe7d739a60016fdcb1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710035"
---
# <a name="equalr-function"></a><span data-ttu-id="8dd0a-102">Функция Equals</span><span class="sxs-lookup"><span data-stu-id="8dd0a-102">EqualR function</span></span>

<span data-ttu-id="8dd0a-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="8dd0a-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="8dd0a-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8dd0a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8dd0a-105">Возвращает значение true только в том случае, если два входных значения равны.</span><span class="sxs-lookup"><span data-stu-id="8dd0a-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualR (a : Result, b : Result) : Bool
```


## <a name="input"></a><span data-ttu-id="8dd0a-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="8dd0a-106">Input</span></span>

### <a name="a--__invalidresult__"></a><span data-ttu-id="8dd0a-107">ответ. __Недопустимый <Result>__</span><span class="sxs-lookup"><span data-stu-id="8dd0a-107">a : __invalid<Result>__</span></span>

<span data-ttu-id="8dd0a-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="8dd0a-108">The first value to be compared.</span></span>


### <a name="b--__invalidresult__"></a><span data-ttu-id="8dd0a-109">б: __недопустимо <Result>__</span><span class="sxs-lookup"><span data-stu-id="8dd0a-109">b : __invalid<Result>__</span></span>

<span data-ttu-id="8dd0a-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="8dd0a-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="8dd0a-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="8dd0a-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="8dd0a-112">`true` Если и, только если `a` равно `b` .</span><span class="sxs-lookup"><span data-stu-id="8dd0a-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="8dd0a-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="8dd0a-113">Remarks</span></span>

<span data-ttu-id="8dd0a-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="8dd0a-114">The following are equivalent:</span></span>

```Q#
let cond = a == b;
let cond = EqualR(a, b);
```