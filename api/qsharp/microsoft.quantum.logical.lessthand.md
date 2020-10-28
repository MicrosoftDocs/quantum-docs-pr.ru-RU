---
uid: Microsoft.Quantum.Logical.LessThanD
title: Функция Лесссанд
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanD
qsharp.summary: Returns true if and only if a number is less than another number.
ms.openlocfilehash: 8cd274d5e299df2f556006baf7457d54aebcd071
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732928"
---
# <a name="lessthand-function"></a><span data-ttu-id="2fe0f-102">Функция Лесссанд</span><span class="sxs-lookup"><span data-stu-id="2fe0f-102">LessThanD function</span></span>

<span data-ttu-id="2fe0f-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="2fe0f-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="2fe0f-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2fe0f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2fe0f-105">Возвращает значение true только в том случае, если число меньше, чем другое число.</span><span class="sxs-lookup"><span data-stu-id="2fe0f-105">Returns true if and only if a number is less than another number.</span></span>

```qsharp
function LessThanD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="2fe0f-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2fe0f-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="2fe0f-107">ответ. [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="2fe0f-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="2fe0f-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="2fe0f-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="2fe0f-109">б: [двойной](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="2fe0f-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="2fe0f-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="2fe0f-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="2fe0f-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="2fe0f-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="2fe0f-112">`true` Если и, только если `a` является строго меньшим `b` .</span><span class="sxs-lookup"><span data-stu-id="2fe0f-112">`true` if and only if `a` is strictly less than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fe0f-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="2fe0f-113">Remarks</span></span>

<span data-ttu-id="2fe0f-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="2fe0f-114">The following are equivalent:</span></span>

```Q#
let cond = a < b;
let cond = LessThanD(a, b);
```