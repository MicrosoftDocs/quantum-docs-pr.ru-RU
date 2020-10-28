---
uid: Microsoft.Quantum.Logical.NotEqualR
title: Функция Нотекуалр
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualR
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 06615c7ffb6aafc296077990dfca0ce25e1e00fa
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709797"
---
# <a name="notequalr-function"></a><span data-ttu-id="8b5e7-102">Функция Нотекуалр</span><span class="sxs-lookup"><span data-stu-id="8b5e7-102">NotEqualR function</span></span>

<span data-ttu-id="8b5e7-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="8b5e7-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="8b5e7-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8b5e7-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8b5e7-105">Возвращает значение true только в том случае, если два входных значения не равны.</span><span class="sxs-lookup"><span data-stu-id="8b5e7-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualR (a : Result, b : Result) : Bool
```


## <a name="input"></a><span data-ttu-id="8b5e7-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="8b5e7-106">Input</span></span>

### <a name="a--__invalidresult__"></a><span data-ttu-id="8b5e7-107">ответ. __Недопустимый <Result>__</span><span class="sxs-lookup"><span data-stu-id="8b5e7-107">a : __invalid<Result>__</span></span>

<span data-ttu-id="8b5e7-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="8b5e7-108">The first value to be compared.</span></span>


### <a name="b--__invalidresult__"></a><span data-ttu-id="8b5e7-109">б: __недопустимо <Result>__</span><span class="sxs-lookup"><span data-stu-id="8b5e7-109">b : __invalid<Result>__</span></span>

<span data-ttu-id="8b5e7-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="8b5e7-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="8b5e7-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="8b5e7-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="8b5e7-112">`true` Если и, только если `a` не равно `b` .</span><span class="sxs-lookup"><span data-stu-id="8b5e7-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b5e7-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="8b5e7-113">Remarks</span></span>

<span data-ttu-id="8b5e7-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="8b5e7-114">The following are equivalent:</span></span>

```Q#
let cond = a != b;
let cond = NotEqualR(a, b);
```