---
uid: Microsoft.Quantum.Core.RangeEnd
title: Функция RangeEnd
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeEnd
qsharp.summary: Returns the defined end value of the given range, which is not necessarily the last element in the sequence.
ms.openlocfilehash: 4dbcf517c4dc17775040444c77deb0e449082390
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713242"
---
# <a name="rangeend-function"></a><span data-ttu-id="4479f-102">Функция RangeEnd</span><span class="sxs-lookup"><span data-stu-id="4479f-102">RangeEnd function</span></span>

<span data-ttu-id="4479f-103">Пространство имен: [Microsoft. тактов. Core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="4479f-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="4479f-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4479f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4479f-105">Возвращает определенное конечное значение заданного диапазона, которое не обязательно является последним элементом последовательности.</span><span class="sxs-lookup"><span data-stu-id="4479f-105">Returns the defined end value of the given range, which is not necessarily the last element in the sequence.</span></span>

```qsharp
function RangeEnd (range : Range) : Int
```


## <a name="input"></a><span data-ttu-id="4479f-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="4479f-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="4479f-107">диапазон: [диапазон](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="4479f-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>





## <a name="output--int"></a><span data-ttu-id="4479f-108">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4479f-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4479f-109">Определенное конечное значение заданного диапазона.</span><span class="sxs-lookup"><span data-stu-id="4479f-109">The defined end value of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="4479f-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="4479f-110">Remarks</span></span>

<span data-ttu-id="4479f-111">Первым элементом выражения диапазона является `start` , второй элемент —, `start+step` третий элемент — и `start+step+step` т. д., пока `end` не будет передан.</span><span class="sxs-lookup"><span data-stu-id="4479f-111">A range expression's first element is `start`, its second element is `start+step`, third element is `start+step+step`, etc., until `end` is passed.</span></span>

<span data-ttu-id="4479f-112">Обратите внимание, что определенное конечное значение диапазона может отличаться от последнего элемента последовательности, заданной диапазоном. Например, в диапазоне 0..</span><span class="sxs-lookup"><span data-stu-id="4479f-112">Note that the defined end value of a range can differ from the last element in the sequence specified by the range; for example, in a range 0 ..</span></span> <span data-ttu-id="4479f-113">2..</span><span class="sxs-lookup"><span data-stu-id="4479f-113">2 ..</span></span> <span data-ttu-id="4479f-114">5 последний элемент — 4, а конечное значение — 5.</span><span class="sxs-lookup"><span data-stu-id="4479f-114">5 the last element is 4 but the end value is 5.</span></span>