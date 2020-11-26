---
uid: Microsoft.Quantum.Logical.LessThanOrEqualD
title: Функция Лесссанорекуалд
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanOrEqualD
qsharp.summary: Returns true if and only if a number is less than or equal to another number.
ms.openlocfilehash: 3f4ccb0888e7df7c43ff73be8a3140e3fa84d4dc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197642"
---
# <a name="lessthanorequald-function"></a><span data-ttu-id="53b8e-102">Функция Лесссанорекуалд</span><span class="sxs-lookup"><span data-stu-id="53b8e-102">LessThanOrEqualD function</span></span>

<span data-ttu-id="53b8e-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="53b8e-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="53b8e-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="53b8e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="53b8e-105">Возвращает значение true только в том случае, если число меньше или равно другому числу.</span><span class="sxs-lookup"><span data-stu-id="53b8e-105">Returns true if and only if a number is less than or equal to another number.</span></span>

```qsharp
function LessThanOrEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="53b8e-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="53b8e-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="53b8e-107">ответ. [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="53b8e-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="53b8e-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="53b8e-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="53b8e-109">б: [двойной](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="53b8e-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="53b8e-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="53b8e-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="53b8e-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="53b8e-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="53b8e-112">`true` только в случае, если `a` меньше или равно `b` .</span><span class="sxs-lookup"><span data-stu-id="53b8e-112">`true` if and only if `a` is less than or equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="53b8e-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="53b8e-113">Remarks</span></span>

<span data-ttu-id="53b8e-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="53b8e-114">The following are equivalent:</span></span>

```Q#
let cond = a <= b;
let cond = LessThanOrEqualD(a, b);
```