---
uid: Microsoft.Quantum.Core.RangeEnd
title: Функция RangeEnd
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeEnd
qsharp.summary: Returns the defined end value of the given range, which is not necessarily the last element in the sequence.
ms.openlocfilehash: 196fab0bd97a441a16976033dc0d660c54cdfd6a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98831368"
---
# <a name="rangeend-function"></a><span data-ttu-id="e6213-102">Функция RangeEnd</span><span class="sxs-lookup"><span data-stu-id="e6213-102">RangeEnd function</span></span>

<span data-ttu-id="e6213-103">Пространство имен: [Microsoft. тактов. Core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="e6213-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="e6213-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="e6213-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="e6213-105">Возвращает определенное конечное значение заданного диапазона, которое не обязательно является последним элементом последовательности.</span><span class="sxs-lookup"><span data-stu-id="e6213-105">Returns the defined end value of the given range, which is not necessarily the last element in the sequence.</span></span>

```qsharp
function RangeEnd (range : Range) : Int
```


## <a name="input"></a><span data-ttu-id="e6213-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e6213-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="e6213-107">диапазон: [диапазон](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="e6213-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>





## <a name="output--int"></a><span data-ttu-id="e6213-108">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e6213-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e6213-109">Определенное конечное значение заданного диапазона.</span><span class="sxs-lookup"><span data-stu-id="e6213-109">The defined end value of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6213-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="e6213-110">Remarks</span></span>

<span data-ttu-id="e6213-111">Первым элементом выражения диапазона является `start` , второй элемент —, `start+step` третий элемент — и `start+step+step` т. д., пока `end` не будет передан.</span><span class="sxs-lookup"><span data-stu-id="e6213-111">A range expression's first element is `start`, its second element is `start+step`, third element is `start+step+step`, etc., until `end` is passed.</span></span>

<span data-ttu-id="e6213-112">Обратите внимание, что определенное конечное значение диапазона может отличаться от последнего элемента последовательности, заданной диапазоном. Например, в диапазоне 0..</span><span class="sxs-lookup"><span data-stu-id="e6213-112">Note that the defined end value of a range can differ from the last element in the sequence specified by the range; for example, in a range 0 ..</span></span> <span data-ttu-id="e6213-113">2..</span><span class="sxs-lookup"><span data-stu-id="e6213-113">2 ..</span></span> <span data-ttu-id="e6213-114">5 последний элемент — 4, а конечное значение — 5.</span><span class="sxs-lookup"><span data-stu-id="e6213-114">5 the last element is 4 but the end value is 5.</span></span>