---
uid: Microsoft.Quantum.Core.RangeStart
title: RangeStart, функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeStart
qsharp.summary: Returns the defined start value of the given range.
ms.openlocfilehash: 3e4b0cebe34b4c98cb1d582a9cd11b46ff778517
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713171"
---
# <a name="rangestart-function"></a><span data-ttu-id="2c044-102">RangeStart, функция</span><span class="sxs-lookup"><span data-stu-id="2c044-102">RangeStart function</span></span>

<span data-ttu-id="2c044-103">Пространство имен: [Microsoft. тактов. Core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="2c044-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="2c044-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2c044-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2c044-105">Возвращает заданное начальное значение заданного диапазона.</span><span class="sxs-lookup"><span data-stu-id="2c044-105">Returns the defined start value of the given range.</span></span>

```qsharp
function RangeStart (range : Range) : Int
```


## <a name="input"></a><span data-ttu-id="2c044-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2c044-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="2c044-107">диапазон: [диапазон](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="2c044-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>





## <a name="output--int"></a><span data-ttu-id="2c044-108">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2c044-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2c044-109">Заданное начальное значение заданного диапазона.</span><span class="sxs-lookup"><span data-stu-id="2c044-109">The defined start value of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c044-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="2c044-110">Remarks</span></span>

<span data-ttu-id="2c044-111">Первым элементом выражения диапазона является `start` , второй элемент —, `start+step` третий элемент — и `start+step+step` т. д., пока `end` не будет передан.</span><span class="sxs-lookup"><span data-stu-id="2c044-111">A range expression's first element is `start`, its second element is `start+step`, third element is `start+step+step`, etc., until `end` is passed.</span></span>

<span data-ttu-id="2c044-112">Обратите внимание, что определенное начальное значение диапазона совпадает с первым элементом последовательности, если диапазон не задает пустую последовательность (например, 2..</span><span class="sxs-lookup"><span data-stu-id="2c044-112">Note that the defined start value of a range is the same as the first element of the sequence, unless the range specifies an empty sequence (for example, 2 ..</span></span> <span data-ttu-id="2c044-113">1).</span><span class="sxs-lookup"><span data-stu-id="2c044-113">1).</span></span>