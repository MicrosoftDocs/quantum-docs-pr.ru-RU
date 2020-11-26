---
uid: Microsoft.Quantum.Core.RangeEnd
title: Функция RangeEnd
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeEnd
qsharp.summary: Returns the defined end value of the given range, which is not necessarily the last element in the sequence.
ms.openlocfilehash: 90a9e31bf5c4a5e92a35998ddaec8c9e9de9888e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224043"
---
# <a name="rangeend-function"></a><span data-ttu-id="2a1e9-102">Функция RangeEnd</span><span class="sxs-lookup"><span data-stu-id="2a1e9-102">RangeEnd function</span></span>

<span data-ttu-id="2a1e9-103">Пространство имен: [Microsoft. тактов. Core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="2a1e9-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="2a1e9-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="2a1e9-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="2a1e9-105">Возвращает определенное конечное значение заданного диапазона, которое не обязательно является последним элементом последовательности.</span><span class="sxs-lookup"><span data-stu-id="2a1e9-105">Returns the defined end value of the given range, which is not necessarily the last element in the sequence.</span></span>

```qsharp
function RangeEnd (range : Range) : Int
```


## <a name="input"></a><span data-ttu-id="2a1e9-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2a1e9-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="2a1e9-107">диапазон: [диапазон](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="2a1e9-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>





## <a name="output--int"></a><span data-ttu-id="2a1e9-108">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2a1e9-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2a1e9-109">Определенное конечное значение заданного диапазона.</span><span class="sxs-lookup"><span data-stu-id="2a1e9-109">The defined end value of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a1e9-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2a1e9-110">Remarks</span></span>

<span data-ttu-id="2a1e9-111">Первым элементом выражения диапазона является `start` , второй элемент —, `start+step` третий элемент — и `start+step+step` т. д., пока `end` не будет передан.</span><span class="sxs-lookup"><span data-stu-id="2a1e9-111">A range expression's first element is `start`, its second element is `start+step`, third element is `start+step+step`, etc., until `end` is passed.</span></span>

<span data-ttu-id="2a1e9-112">Обратите внимание, что определенное конечное значение диапазона может отличаться от последнего элемента последовательности, заданной диапазоном. Например, в диапазоне 0..</span><span class="sxs-lookup"><span data-stu-id="2a1e9-112">Note that the defined end value of a range can differ from the last element in the sequence specified by the range; for example, in a range 0 ..</span></span> <span data-ttu-id="2a1e9-113">2..</span><span class="sxs-lookup"><span data-stu-id="2a1e9-113">2 ..</span></span> <span data-ttu-id="2a1e9-114">5 последний элемент — 4, а конечное значение — 5.</span><span class="sxs-lookup"><span data-stu-id="2a1e9-114">5 the last element is 4 but the end value is 5.</span></span>