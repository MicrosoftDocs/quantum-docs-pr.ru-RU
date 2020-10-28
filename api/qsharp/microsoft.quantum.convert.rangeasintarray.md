---
uid: Microsoft.Quantum.Convert.RangeAsIntArray
title: Функция Ранжеасинтаррай
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: RangeAsIntArray
qsharp.summary: Creates an array `arr` of integers enumerated by start..step..end.
ms.openlocfilehash: bd3ac51d2925d7a4450b2bc5e6f7899fcab18f2c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713367"
---
# <a name="rangeasintarray-function"></a><span data-ttu-id="4837b-102">Функция Ранжеасинтаррай</span><span class="sxs-lookup"><span data-stu-id="4837b-102">RangeAsIntArray function</span></span>

<span data-ttu-id="4837b-103">Пространство имен: [Microsoft. тактов. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="4837b-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="4837b-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4837b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4837b-105">Создает массив `arr` целых чисел, перечисленных с помощью Start.. шаг.. конце.</span><span class="sxs-lookup"><span data-stu-id="4837b-105">Creates an array `arr` of integers enumerated by start..step..end.</span></span>

```qsharp
function RangeAsIntArray (range : Range) : Int[]
```


## <a name="input"></a><span data-ttu-id="4837b-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="4837b-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="4837b-107">диапазон: [диапазон](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="4837b-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="4837b-108">Объект `Range` из значений, `start..step..end` преобразуемых в массив.</span><span class="sxs-lookup"><span data-stu-id="4837b-108">A `Range` of values `start..step..end` to be converted to an array.</span></span>



## <a name="output--int"></a><span data-ttu-id="4837b-109">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="4837b-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="4837b-110">Новый массив целых чисел, соответствующий значениям, перебираемым по `range` .</span><span class="sxs-lookup"><span data-stu-id="4837b-110">A new array of integers corresponding to values iterated over by `range`.</span></span>