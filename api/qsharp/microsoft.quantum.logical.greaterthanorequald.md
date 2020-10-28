---
uid: Microsoft.Quantum.Logical.GreaterThanOrEqualD
title: Функция Греатерсанорекуалд
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanOrEqualD
qsharp.summary: Returns true if and only if a number is greater than or equal to another number.
ms.openlocfilehash: 9d794fa94c1ccbde4030c90198fd7c7654469876
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711379"
---
# <a name="greaterthanorequald-function"></a><span data-ttu-id="73e0c-102">Функция Греатерсанорекуалд</span><span class="sxs-lookup"><span data-stu-id="73e0c-102">GreaterThanOrEqualD function</span></span>

<span data-ttu-id="73e0c-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="73e0c-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="73e0c-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="73e0c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="73e0c-105">Возвращает значение true только в том случае, если число больше или равно другому числу.</span><span class="sxs-lookup"><span data-stu-id="73e0c-105">Returns true if and only if a number is greater than or equal to another number.</span></span>

```qsharp
function GreaterThanOrEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="73e0c-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="73e0c-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="73e0c-107">ответ. [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="73e0c-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="73e0c-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="73e0c-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="73e0c-109">б: [двойной](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="73e0c-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="73e0c-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="73e0c-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="73e0c-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="73e0c-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="73e0c-112">`true` значение и, только если `a` значение больше или равно `b` .</span><span class="sxs-lookup"><span data-stu-id="73e0c-112">`true` if and only if `a` is greater than or is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="73e0c-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="73e0c-113">Remarks</span></span>

<span data-ttu-id="73e0c-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="73e0c-114">The following are equivalent:</span></span>

```Q#
let cond = a >= b;
let cond = GreaterThanOrEqualD(a, b);
```