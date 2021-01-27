---
uid: Microsoft.Quantum.Logical.LessThanL
title: Функция Лесссанл
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanL
qsharp.summary: Returns true if and only if a number is less than another number.
ms.openlocfilehash: d5753f9e1447fc1bd433703037fe44c86aaa659c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849151"
---
# <a name="lessthanl-function"></a><span data-ttu-id="0b69e-102">Функция Лесссанл</span><span class="sxs-lookup"><span data-stu-id="0b69e-102">LessThanL function</span></span>

<span data-ttu-id="0b69e-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="0b69e-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="0b69e-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0b69e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0b69e-105">Возвращает значение true только в том случае, если число меньше, чем другое число.</span><span class="sxs-lookup"><span data-stu-id="0b69e-105">Returns true if and only if a number is less than another number.</span></span>

```qsharp
function LessThanL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="0b69e-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="0b69e-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="0b69e-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="0b69e-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="0b69e-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="0b69e-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="0b69e-109">б: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="0b69e-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="0b69e-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="0b69e-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="0b69e-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="0b69e-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="0b69e-112">`true` Если и, только если `a` является строго меньшим `b` .</span><span class="sxs-lookup"><span data-stu-id="0b69e-112">`true` if and only if `a` is strictly less than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b69e-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="0b69e-113">Remarks</span></span>

<span data-ttu-id="0b69e-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="0b69e-114">The following are equivalent:</span></span>

```qsharp
let cond = a < b;
let cond = LessThanL(a, b);
```