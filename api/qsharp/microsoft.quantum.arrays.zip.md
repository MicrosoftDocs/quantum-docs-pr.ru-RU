---
uid: Microsoft.Quantum.Arrays.Zip
title: Функция ZIP
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zip
qsharp.summary: >-
  > [!WARNING]

  > Zip has been deprecated. Please use <xref:Microsoft.Quantum.Arrays.Zipped> instead.


  Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.
ms.openlocfilehash: 32fea60fc36bfdbaa2ab2f3560f291bf4ce4fa51
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729921"
---
# <a name="zip-function"></a><span data-ttu-id="e3855-102">Функция ZIP</span><span class="sxs-lookup"><span data-stu-id="e3855-102">Zip function</span></span>

<span data-ttu-id="e3855-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="e3855-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="e3855-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e3855-104">Package: [](https://nuget.org/packages/)</span></span>


> [!WARNING]
> <span data-ttu-id="e3855-105">ZIP является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="e3855-105">Zip has been deprecated.</span></span> <span data-ttu-id="e3855-106">Взамен рекомендуется использовать <xref:Microsoft.Quantum.Arrays.Zipped>.</span><span class="sxs-lookup"><span data-stu-id="e3855-106">Please use <xref:Microsoft.Quantum.Arrays.Zipped> instead.</span></span>

<span data-ttu-id="e3855-107">При наличии двух массивов возвращает новый массив пар, в котором каждая пара содержит элемент из каждого исходного массива.</span><span class="sxs-lookup"><span data-stu-id="e3855-107">Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.</span></span>

```qsharp
function Zip<'T, 'U> (left : 'T[], right : 'U[]) : ('T, 'U)[]
```


## <a name="input"></a><span data-ttu-id="e3855-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e3855-108">Input</span></span>

### <a name="left--t"></a><span data-ttu-id="e3855-109">Left: ' ' []</span><span class="sxs-lookup"><span data-stu-id="e3855-109">left : 'T[]</span></span>

<span data-ttu-id="e3855-110">Массив, содержащий значения для первого элемента каждого кортежа.</span><span class="sxs-lookup"><span data-stu-id="e3855-110">An array containing values for the first element of each tuple.</span></span>


### <a name="right--u"></a><span data-ttu-id="e3855-111">Right: ' U []</span><span class="sxs-lookup"><span data-stu-id="e3855-111">right : 'U[]</span></span>

<span data-ttu-id="e3855-112">Массив, содержащий значения для второго элемента каждого кортежа.</span><span class="sxs-lookup"><span data-stu-id="e3855-112">An array containing values for the second element of each tuple.</span></span>



## <a name="output--tu"></a><span data-ttu-id="e3855-113">Выходные данные: ('T, ' U) []</span><span class="sxs-lookup"><span data-stu-id="e3855-113">Output : ('T,'U)[]</span></span>

<span data-ttu-id="e3855-114">Массив, содержащий пары форм `(left[idx], right[idx])` для каждого из них `idx` .</span><span class="sxs-lookup"><span data-stu-id="e3855-114">An array containing pairs of the form `(left[idx], right[idx])` for each `idx`.</span></span> <span data-ttu-id="e3855-115">Если два массива не имеют одинаковую длину, выходные данные будут иметь длину до более короткой из входных значений.</span><span class="sxs-lookup"><span data-stu-id="e3855-115">If the two arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="e3855-116">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="e3855-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e3855-117">Е</span><span class="sxs-lookup"><span data-stu-id="e3855-117">'T</span></span>

<span data-ttu-id="e3855-118">Тип элементов левого массива.</span><span class="sxs-lookup"><span data-stu-id="e3855-118">The type of the left array elements.</span></span>
### <a name="u"></a><span data-ttu-id="e3855-119">' U</span><span class="sxs-lookup"><span data-stu-id="e3855-119">'U</span></span>

<span data-ttu-id="e3855-120">Тип правых элементов массива.</span><span class="sxs-lookup"><span data-stu-id="e3855-120">The type of the right array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="e3855-121">См. также:</span><span class="sxs-lookup"><span data-stu-id="e3855-121">See Also</span></span>

- [<span data-ttu-id="e3855-122">Microsoft.Quantum.Arrays.Zip3</span><span class="sxs-lookup"><span data-stu-id="e3855-122">Microsoft.Quantum.Arrays.Zip3</span></span>](xref:Microsoft.Quantum.Arrays.Zip3)
- [<span data-ttu-id="e3855-123">Microsoft.Quantum.Arrays.Zip4</span><span class="sxs-lookup"><span data-stu-id="e3855-123">Microsoft.Quantum.Arrays.Zip4</span></span>](xref:Microsoft.Quantum.Arrays.Zip4)
- [<span data-ttu-id="e3855-124">Microsoft. тактов. Arrays. unzipped</span><span class="sxs-lookup"><span data-stu-id="e3855-124">Microsoft.Quantum.Arrays.Unzipped</span></span>](xref:Microsoft.Quantum.Arrays.Unzipped)