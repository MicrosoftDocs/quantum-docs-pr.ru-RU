---
uid: Microsoft.Quantum.Logical.LessThanOrEqualI
title: Функция Лесссанорекуали
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanOrEqualI
qsharp.summary: Returns true if and only if a number is less than or equal to another number.
ms.openlocfilehash: dd934fde3fae9c1a43032b4b08ac03afa72798d1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709937"
---
# <a name="lessthanorequali-function"></a><span data-ttu-id="f65ea-102">Функция Лесссанорекуали</span><span class="sxs-lookup"><span data-stu-id="f65ea-102">LessThanOrEqualI function</span></span>

<span data-ttu-id="f65ea-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="f65ea-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="f65ea-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f65ea-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f65ea-105">Возвращает значение true только в том случае, если число меньше или равно другому числу.</span><span class="sxs-lookup"><span data-stu-id="f65ea-105">Returns true if and only if a number is less than or equal to another number.</span></span>

```qsharp
function LessThanOrEqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="f65ea-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f65ea-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="f65ea-107">ответ. [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f65ea-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f65ea-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="f65ea-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="f65ea-109">б: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f65ea-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f65ea-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="f65ea-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="f65ea-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="f65ea-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="f65ea-112">`true` только в случае, если `a` меньше или равно `b` .</span><span class="sxs-lookup"><span data-stu-id="f65ea-112">`true` if and only if `a` is less than or equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="f65ea-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="f65ea-113">Remarks</span></span>

<span data-ttu-id="f65ea-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="f65ea-114">The following are equivalent:</span></span>

```Q#
let cond = a <= b;
let cond = LessThanOrEqualI(a, b);
```