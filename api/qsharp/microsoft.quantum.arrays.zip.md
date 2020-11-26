---
uid: Microsoft.Quantum.Arrays.Zip
title: Функция ZIP
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zip
qsharp.summary: >-
  > [!WARNING]

  > Zip has been deprecated. Please use <xref:Microsoft.Quantum.Arrays.Zipped> instead.


  Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.
ms.openlocfilehash: 44db8d38d96babd16ead5ae6dde91da23bdee2c9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219861"
---
# <a name="zip-function"></a><span data-ttu-id="83993-102">Функция ZIP</span><span class="sxs-lookup"><span data-stu-id="83993-102">Zip function</span></span>

<span data-ttu-id="83993-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="83993-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="83993-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="83993-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="83993-105">ZIP является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="83993-105">Zip has been deprecated.</span></span> <span data-ttu-id="83993-106">Взамен рекомендуется использовать <xref:Microsoft.Quantum.Arrays.Zipped>.</span><span class="sxs-lookup"><span data-stu-id="83993-106">Please use <xref:Microsoft.Quantum.Arrays.Zipped> instead.</span></span>

<span data-ttu-id="83993-107">При наличии двух массивов возвращает новый массив пар, в котором каждая пара содержит элемент из каждого исходного массива.</span><span class="sxs-lookup"><span data-stu-id="83993-107">Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.</span></span>

```qsharp
function Zip<'T, 'U> (left : 'T[], right : 'U[]) : ('T, 'U)[]
```


## <a name="input"></a><span data-ttu-id="83993-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="83993-108">Input</span></span>

### <a name="left--t"></a><span data-ttu-id="83993-109">Left: ' ' []</span><span class="sxs-lookup"><span data-stu-id="83993-109">left : 'T[]</span></span>

<span data-ttu-id="83993-110">Массив, содержащий значения для первого элемента каждого кортежа.</span><span class="sxs-lookup"><span data-stu-id="83993-110">An array containing values for the first element of each tuple.</span></span>


### <a name="right--u"></a><span data-ttu-id="83993-111">Right: ' U []</span><span class="sxs-lookup"><span data-stu-id="83993-111">right : 'U[]</span></span>

<span data-ttu-id="83993-112">Массив, содержащий значения для второго элемента каждого кортежа.</span><span class="sxs-lookup"><span data-stu-id="83993-112">An array containing values for the second element of each tuple.</span></span>



## <a name="output--tu"></a><span data-ttu-id="83993-113">Выходные данные: ('T, ' U) []</span><span class="sxs-lookup"><span data-stu-id="83993-113">Output : ('T,'U)[]</span></span>

<span data-ttu-id="83993-114">Массив, содержащий пары форм `(left[idx], right[idx])` для каждого из них `idx` .</span><span class="sxs-lookup"><span data-stu-id="83993-114">An array containing pairs of the form `(left[idx], right[idx])` for each `idx`.</span></span> <span data-ttu-id="83993-115">Если два массива не имеют одинаковую длину, выходные данные будут иметь длину до более короткой из входных значений.</span><span class="sxs-lookup"><span data-stu-id="83993-115">If the two arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="83993-116">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="83993-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="83993-117">Е</span><span class="sxs-lookup"><span data-stu-id="83993-117">'T</span></span>

<span data-ttu-id="83993-118">Тип элементов левого массива.</span><span class="sxs-lookup"><span data-stu-id="83993-118">The type of the left array elements.</span></span>
### <a name="u"></a><span data-ttu-id="83993-119">' U</span><span class="sxs-lookup"><span data-stu-id="83993-119">'U</span></span>

<span data-ttu-id="83993-120">Тип правых элементов массива.</span><span class="sxs-lookup"><span data-stu-id="83993-120">The type of the right array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="83993-121">См. также:</span><span class="sxs-lookup"><span data-stu-id="83993-121">See Also</span></span>

- [<span data-ttu-id="83993-122">Microsoft.Quantum.Arrays.Zip3</span><span class="sxs-lookup"><span data-stu-id="83993-122">Microsoft.Quantum.Arrays.Zip3</span></span>](xref:Microsoft.Quantum.Arrays.Zip3)
- [<span data-ttu-id="83993-123">Microsoft.Quantum.Arrays.Zip4</span><span class="sxs-lookup"><span data-stu-id="83993-123">Microsoft.Quantum.Arrays.Zip4</span></span>](xref:Microsoft.Quantum.Arrays.Zip4)
- [<span data-ttu-id="83993-124">Microsoft. тактов. Arrays. unzipped</span><span class="sxs-lookup"><span data-stu-id="83993-124">Microsoft.Quantum.Arrays.Unzipped</span></span>](xref:Microsoft.Quantum.Arrays.Unzipped)