---
uid: Microsoft.Quantum.Core.RangeStep
title: Функция Ранжестеп
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeStep
qsharp.summary: Returns the integer that specifies how the next value of a range is calculated.
ms.openlocfilehash: 39c8581fe795a1b76d2a6e81c238a271287c2c38
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96213809"
---
# <a name="rangestep-function"></a><span data-ttu-id="03111-102">Функция Ранжестеп</span><span class="sxs-lookup"><span data-stu-id="03111-102">RangeStep function</span></span>

<span data-ttu-id="03111-103">Пространство имен: [Microsoft. тактов. Core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="03111-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="03111-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="03111-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="03111-105">Возвращает целое число, указывающее, как вычисляется следующее значение диапазона.</span><span class="sxs-lookup"><span data-stu-id="03111-105">Returns the integer that specifies how the next value of a range is calculated.</span></span>

```qsharp
function RangeStep (range : Range) : Int
```


## <a name="input"></a><span data-ttu-id="03111-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="03111-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="03111-107">диапазон: [диапазон](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="03111-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>





## <a name="output--int"></a><span data-ttu-id="03111-108">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="03111-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="03111-109">Заданное значение шага данного диапазона.</span><span class="sxs-lookup"><span data-stu-id="03111-109">The defined step value of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="03111-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="03111-110">Remarks</span></span>

<span data-ttu-id="03111-111">Первым элементом выражения диапазона является `start` , второй элемент —, `start+step` третий элемент — и `start+step+step` т. д., пока `end` не будет передан.</span><span class="sxs-lookup"><span data-stu-id="03111-111">A range expression's first element is `start`, its second element is `start+step`, third element is `start+step+step`, etc., until `end` is passed.</span></span>