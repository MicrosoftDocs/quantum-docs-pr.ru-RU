---
uid: Microsoft.Quantum.Logical.LessThanOrEqualL
title: Функция Лесссанорекуалл
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanOrEqualL
qsharp.summary: Returns true if and only if a number is less than or equal to another number.
ms.openlocfilehash: 2322ae4dd6025108d322d29770f42953213aa025
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197607"
---
# <a name="lessthanorequall-function"></a><span data-ttu-id="fdfeb-102">Функция Лесссанорекуалл</span><span class="sxs-lookup"><span data-stu-id="fdfeb-102">LessThanOrEqualL function</span></span>

<span data-ttu-id="fdfeb-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="fdfeb-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="fdfeb-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fdfeb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fdfeb-105">Возвращает значение true только в том случае, если число меньше или равно другому числу.</span><span class="sxs-lookup"><span data-stu-id="fdfeb-105">Returns true if and only if a number is less than or equal to another number.</span></span>

```qsharp
function LessThanOrEqualL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="fdfeb-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="fdfeb-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="fdfeb-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="fdfeb-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="fdfeb-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="fdfeb-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="fdfeb-109">б: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="fdfeb-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="fdfeb-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="fdfeb-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="fdfeb-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="fdfeb-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="fdfeb-112">`true` только в случае, если `a` меньше или равно `b` .</span><span class="sxs-lookup"><span data-stu-id="fdfeb-112">`true` if and only if `a` is less than or equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdfeb-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fdfeb-113">Remarks</span></span>

<span data-ttu-id="fdfeb-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="fdfeb-114">The following are equivalent:</span></span>

```Q#
let cond = a <= b;
let cond = LessThanOrEqualL(a, b);
```