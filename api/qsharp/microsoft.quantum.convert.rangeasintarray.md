---
uid: Microsoft.Quantum.Convert.RangeAsIntArray
title: Функция Ранжеасинтаррай
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: RangeAsIntArray
qsharp.summary: Creates an array `arr` of integers enumerated by start..step..end.
ms.openlocfilehash: f756e42aef7dc600e1fc6943a02513ac791f2320
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96214013"
---
# <a name="rangeasintarray-function"></a><span data-ttu-id="963e3-102">Функция Ранжеасинтаррай</span><span class="sxs-lookup"><span data-stu-id="963e3-102">RangeAsIntArray function</span></span>

<span data-ttu-id="963e3-103">Пространство имен: [Microsoft. тактов. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="963e3-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="963e3-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="963e3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="963e3-105">Создает массив `arr` целых чисел, перечисленных с помощью Start.. шаг.. конце.</span><span class="sxs-lookup"><span data-stu-id="963e3-105">Creates an array `arr` of integers enumerated by start..step..end.</span></span>

```qsharp
function RangeAsIntArray (range : Range) : Int[]
```


## <a name="input"></a><span data-ttu-id="963e3-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="963e3-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="963e3-107">диапазон: [диапазон](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="963e3-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="963e3-108">Объект `Range` из значений, `start..step..end` преобразуемых в массив.</span><span class="sxs-lookup"><span data-stu-id="963e3-108">A `Range` of values `start..step..end` to be converted to an array.</span></span>



## <a name="output--int"></a><span data-ttu-id="963e3-109">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="963e3-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="963e3-110">Новый массив целых чисел, соответствующий значениям, перебираемым по `range` .</span><span class="sxs-lookup"><span data-stu-id="963e3-110">A new array of integers corresponding to values iterated over by `range`.</span></span>