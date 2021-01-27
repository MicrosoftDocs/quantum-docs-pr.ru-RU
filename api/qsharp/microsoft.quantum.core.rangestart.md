---
uid: Microsoft.Quantum.Core.RangeStart
title: RangeStart, функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeStart
qsharp.summary: Returns the defined start value of the given range.
ms.openlocfilehash: 5b04e8c860a4bd6af7b10b4dbf803b1eb69ef5d8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98831120"
---
# <a name="rangestart-function"></a><span data-ttu-id="933f0-102">RangeStart, функция</span><span class="sxs-lookup"><span data-stu-id="933f0-102">RangeStart function</span></span>

<span data-ttu-id="933f0-103">Пространство имен: [Microsoft. тактов. Core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="933f0-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="933f0-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="933f0-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="933f0-105">Возвращает заданное начальное значение заданного диапазона.</span><span class="sxs-lookup"><span data-stu-id="933f0-105">Returns the defined start value of the given range.</span></span>

```qsharp
function RangeStart (range : Range) : Int
```


## <a name="input"></a><span data-ttu-id="933f0-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="933f0-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="933f0-107">диапазон: [диапазон](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="933f0-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>





## <a name="output--int"></a><span data-ttu-id="933f0-108">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="933f0-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="933f0-109">Заданное начальное значение заданного диапазона.</span><span class="sxs-lookup"><span data-stu-id="933f0-109">The defined start value of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="933f0-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="933f0-110">Remarks</span></span>

<span data-ttu-id="933f0-111">Первым элементом выражения диапазона является `start` , второй элемент —, `start+step` третий элемент — и `start+step+step` т. д., пока `end` не будет передан.</span><span class="sxs-lookup"><span data-stu-id="933f0-111">A range expression's first element is `start`, its second element is `start+step`, third element is `start+step+step`, etc., until `end` is passed.</span></span>

<span data-ttu-id="933f0-112">Обратите внимание, что определенное начальное значение диапазона совпадает с первым элементом последовательности, если диапазон не задает пустую последовательность (например, 2..</span><span class="sxs-lookup"><span data-stu-id="933f0-112">Note that the defined start value of a range is the same as the first element of the sequence, unless the range specifies an empty sequence (for example, 2 ..</span></span> <span data-ttu-id="933f0-113">1).</span><span class="sxs-lookup"><span data-stu-id="933f0-113">1).</span></span>