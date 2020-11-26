---
uid: Microsoft.Quantum.Logical.GreaterThanOrEqualI
title: Функция Греатерсанорекуали
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanOrEqualI
qsharp.summary: Returns true if and only if a number is greater than or equal to another number.
ms.openlocfilehash: 0435aae4a824bd19d972e9f6b331260bbe21f692
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197795"
---
# <a name="greaterthanorequali-function"></a><span data-ttu-id="81512-102">Функция Греатерсанорекуали</span><span class="sxs-lookup"><span data-stu-id="81512-102">GreaterThanOrEqualI function</span></span>

<span data-ttu-id="81512-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="81512-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="81512-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="81512-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="81512-105">Возвращает значение true только в том случае, если число больше или равно другому числу.</span><span class="sxs-lookup"><span data-stu-id="81512-105">Returns true if and only if a number is greater than or equal to another number.</span></span>

```qsharp
function GreaterThanOrEqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="81512-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="81512-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="81512-107">ответ. [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="81512-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="81512-108">Первое сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="81512-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="81512-109">б: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="81512-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="81512-110">Второе сравниваемое значение.</span><span class="sxs-lookup"><span data-stu-id="81512-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="81512-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="81512-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="81512-112">`true` значение и, только если `a` значение больше или равно `b` .</span><span class="sxs-lookup"><span data-stu-id="81512-112">`true` if and only if `a` is greater than or is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="81512-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="81512-113">Remarks</span></span>

<span data-ttu-id="81512-114">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="81512-114">The following are equivalent:</span></span>

```Q#
let cond = a >= b;
let cond = GreaterThanOrEqualI(a, b);
```