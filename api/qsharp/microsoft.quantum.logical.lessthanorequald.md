---
uid: Microsoft.Quantum.Logical.LessThanOrEqualD
title: Функция Лесссанорекуалд
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanOrEqualD
qsharp.summary: Returns true if and only if a number is less than or equal to another number.
ms.openlocfilehash: 7b0e9da379bd67eb78a80e7a535a15dcb8ba85c7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709951"
---
# <a name="lessthanorequald-function"></a><span data-ttu-id="b959b-102">Функция Лесссанорекуалд</span><span class="sxs-lookup"><span data-stu-id="b959b-102">LessThanOrEqualD function</span></span>

<span data-ttu-id="b959b-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="b959b-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="b959b-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b959b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b959b-105">Возвращает значение true только в том случае, если число меньше или равно другому числу.</span><span class="sxs-lookup"><span data-stu-id="b959b-105">Returns true if and only if a number is less than or equal to another number.</span></span>

```qsharp
function LessThanOrEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="b959b-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b959b-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="b959b-107">ответ. [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="b959b-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="b959b-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="b959b-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="b959b-109">б: [двойной](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="b959b-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="b959b-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="b959b-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="b959b-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="b959b-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="b959b-112">`true` только в случае, если `a` меньше или равно `b` .</span><span class="sxs-lookup"><span data-stu-id="b959b-112">`true` if and only if `a` is less than or equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="b959b-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="b959b-113">Remarks</span></span>

<span data-ttu-id="b959b-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="b959b-114">The following are equivalent:</span></span>

```Q#
let cond = a <= b;
let cond = LessThanOrEqualD(a, b);
```