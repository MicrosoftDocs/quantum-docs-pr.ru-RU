---
uid: Microsoft.Quantum.Logical.EqualI
title: Функция Екуали
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualI
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 6b805e76217e033cb0135cf85bd8f37a3eb8636a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710050"
---
# <a name="equali-function"></a><span data-ttu-id="353c2-102">Функция Екуали</span><span class="sxs-lookup"><span data-stu-id="353c2-102">EqualI function</span></span>

<span data-ttu-id="353c2-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="353c2-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="353c2-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="353c2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="353c2-105">Возвращает значение true только в том случае, если два входных значения равны.</span><span class="sxs-lookup"><span data-stu-id="353c2-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="353c2-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="353c2-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="353c2-107">ответ. [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="353c2-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="353c2-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="353c2-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="353c2-109">б: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="353c2-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="353c2-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="353c2-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="353c2-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="353c2-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="353c2-112">`true` Если и, только если `a` равно `b` .</span><span class="sxs-lookup"><span data-stu-id="353c2-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="353c2-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="353c2-113">Remarks</span></span>

<span data-ttu-id="353c2-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="353c2-114">The following are equivalent:</span></span>

```Q#
let cond = a == b;
let cond = EqualI(a, b);
```