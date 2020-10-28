---
uid: Microsoft.Quantum.Logical.GreaterThanOrEqualL
title: Функция Греатерсанорекуалл
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanOrEqualL
qsharp.summary: Returns true if and only if a number is greater than or equal to another number.
ms.openlocfilehash: a59a9eca2941a44a70ec5a379b146ac459390bd4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732441"
---
# <a name="greaterthanorequall-function"></a><span data-ttu-id="ba59f-102">Функция Греатерсанорекуалл</span><span class="sxs-lookup"><span data-stu-id="ba59f-102">GreaterThanOrEqualL function</span></span>

<span data-ttu-id="ba59f-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="ba59f-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="ba59f-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ba59f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ba59f-105">Возвращает значение true только в том случае, если число больше или равно другому числу.</span><span class="sxs-lookup"><span data-stu-id="ba59f-105">Returns true if and only if a number is greater than or equal to another number.</span></span>

```qsharp
function GreaterThanOrEqualL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="ba59f-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ba59f-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="ba59f-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="ba59f-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="ba59f-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="ba59f-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="ba59f-109">б: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="ba59f-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="ba59f-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="ba59f-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="ba59f-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="ba59f-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="ba59f-112">`true` значение и, только если `a` значение больше или равно `b` .</span><span class="sxs-lookup"><span data-stu-id="ba59f-112">`true` if and only if `a` is greater than or is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba59f-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="ba59f-113">Remarks</span></span>

<span data-ttu-id="ba59f-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="ba59f-114">The following are equivalent:</span></span>

```Q#
let cond = a >= b;
let cond = GreaterThanOrEqualL(a, b);
```