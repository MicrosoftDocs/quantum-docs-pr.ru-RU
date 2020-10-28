---
uid: Microsoft.Quantum.Logical.LessThanOrEqualL
title: Функция Лесссанорекуалл
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanOrEqualL
qsharp.summary: Returns true if and only if a number is less than or equal to another number.
ms.openlocfilehash: 333b76fc4885104e107dd25003a4e0dd5a9dd4af
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709923"
---
# <a name="lessthanorequall-function"></a><span data-ttu-id="498e9-102">Функция Лесссанорекуалл</span><span class="sxs-lookup"><span data-stu-id="498e9-102">LessThanOrEqualL function</span></span>

<span data-ttu-id="498e9-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="498e9-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="498e9-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="498e9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="498e9-105">Возвращает значение true только в том случае, если число меньше или равно другому числу.</span><span class="sxs-lookup"><span data-stu-id="498e9-105">Returns true if and only if a number is less than or equal to another number.</span></span>

```qsharp
function LessThanOrEqualL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="498e9-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="498e9-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="498e9-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="498e9-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="498e9-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="498e9-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="498e9-109">б: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="498e9-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="498e9-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="498e9-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="498e9-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="498e9-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="498e9-112">`true` только в случае, если `a` меньше или равно `b` .</span><span class="sxs-lookup"><span data-stu-id="498e9-112">`true` if and only if `a` is less than or equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="498e9-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="498e9-113">Remarks</span></span>

<span data-ttu-id="498e9-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="498e9-114">The following are equivalent:</span></span>

```Q#
let cond = a <= b;
let cond = LessThanOrEqualL(a, b);
```