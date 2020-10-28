---
uid: Microsoft.Quantum.Logical.LessThanL
title: Функция Лесссанл
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanL
qsharp.summary: Returns true if and only if a number is less than another number.
ms.openlocfilehash: fde57bcd9960056461bddac54300c298def8f7d5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709952"
---
# <a name="lessthanl-function"></a><span data-ttu-id="00c42-102">Функция Лесссанл</span><span class="sxs-lookup"><span data-stu-id="00c42-102">LessThanL function</span></span>

<span data-ttu-id="00c42-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="00c42-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="00c42-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="00c42-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="00c42-105">Возвращает значение true только в том случае, если число меньше, чем другое число.</span><span class="sxs-lookup"><span data-stu-id="00c42-105">Returns true if and only if a number is less than another number.</span></span>

```qsharp
function LessThanL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="00c42-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="00c42-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="00c42-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="00c42-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="00c42-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="00c42-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="00c42-109">б: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="00c42-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="00c42-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="00c42-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="00c42-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="00c42-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="00c42-112">`true` Если и, только если `a` является строго меньшим `b` .</span><span class="sxs-lookup"><span data-stu-id="00c42-112">`true` if and only if `a` is strictly less than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="00c42-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="00c42-113">Remarks</span></span>

<span data-ttu-id="00c42-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="00c42-114">The following are equivalent:</span></span>

```Q#
let cond = a < b;
let cond = LessThanL(a, b);
```