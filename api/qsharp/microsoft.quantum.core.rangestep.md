---
uid: Microsoft.Quantum.Core.RangeStep
title: Функция Ранжестеп
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeStep
qsharp.summary: Returns the integer that specifies how the next value of a range is calculated.
ms.openlocfilehash: f8e4c42330f2d6afdc1c0a9bdde36081ccab2f94
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713158"
---
# <a name="rangestep-function"></a><span data-ttu-id="a6955-102">Функция Ранжестеп</span><span class="sxs-lookup"><span data-stu-id="a6955-102">RangeStep function</span></span>

<span data-ttu-id="a6955-103">Пространство имен: [Microsoft. тактов. Core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="a6955-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="a6955-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a6955-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a6955-105">Возвращает целое число, указывающее, как вычисляется следующее значение диапазона.</span><span class="sxs-lookup"><span data-stu-id="a6955-105">Returns the integer that specifies how the next value of a range is calculated.</span></span>

```qsharp
function RangeStep (range : Range) : Int
```


## <a name="input"></a><span data-ttu-id="a6955-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a6955-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="a6955-107">диапазон: [диапазон](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="a6955-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>





## <a name="output--int"></a><span data-ttu-id="a6955-108">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a6955-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a6955-109">Заданное значение шага данного диапазона.</span><span class="sxs-lookup"><span data-stu-id="a6955-109">The defined step value of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6955-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="a6955-110">Remarks</span></span>

<span data-ttu-id="a6955-111">Первым элементом выражения диапазона является `start` , второй элемент —, `start+step` третий элемент — и `start+step+step` т. д., пока `end` не будет передан.</span><span class="sxs-lookup"><span data-stu-id="a6955-111">A range expression's first element is `start`, its second element is `start+step`, third element is `start+step+step`, etc., until `end` is passed.</span></span>