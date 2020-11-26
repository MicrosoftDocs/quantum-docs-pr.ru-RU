---
uid: Microsoft.Quantum.Logical.GreaterThanOrEqualD
title: Функция Греатерсанорекуалд
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanOrEqualD
qsharp.summary: Returns true if and only if a number is greater than or equal to another number.
ms.openlocfilehash: 0c9fa353b549d3c137beac3bcc3cfb0e742f6d07
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197812"
---
# <a name="greaterthanorequald-function"></a><span data-ttu-id="c957b-102">Функция Греатерсанорекуалд</span><span class="sxs-lookup"><span data-stu-id="c957b-102">GreaterThanOrEqualD function</span></span>

<span data-ttu-id="c957b-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="c957b-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="c957b-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c957b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c957b-105">Возвращает значение true только в том случае, если число больше или равно другому числу.</span><span class="sxs-lookup"><span data-stu-id="c957b-105">Returns true if and only if a number is greater than or equal to another number.</span></span>

```qsharp
function GreaterThanOrEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="c957b-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c957b-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="c957b-107">ответ. [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="c957b-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="c957b-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="c957b-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="c957b-109">б: [двойной](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="c957b-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="c957b-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="c957b-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="c957b-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="c957b-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="c957b-112">`true` значение и, только если `a` значение больше или равно `b` .</span><span class="sxs-lookup"><span data-stu-id="c957b-112">`true` if and only if `a` is greater than or is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="c957b-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c957b-113">Remarks</span></span>

<span data-ttu-id="c957b-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="c957b-114">The following are equivalent:</span></span>

```Q#
let cond = a >= b;
let cond = GreaterThanOrEqualD(a, b);
```