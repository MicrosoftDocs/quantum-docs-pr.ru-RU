---
uid: Microsoft.Quantum.Arrays.Zip
title: Функция ZIP
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zip
qsharp.summary: >-
  > [!WARNING]

  > Zip has been deprecated. Please use <xref:Microsoft.Quantum.Arrays.Zipped> instead.


  Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.
ms.openlocfilehash: 8ed658003f749efd31b8d841cecbb0a23a471af5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850903"
---
# <a name="zip-function"></a><span data-ttu-id="7db1b-102">Функция ZIP</span><span class="sxs-lookup"><span data-stu-id="7db1b-102">Zip function</span></span>

<span data-ttu-id="7db1b-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="7db1b-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="7db1b-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7db1b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="7db1b-105">ZIP является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="7db1b-105">Zip has been deprecated.</span></span> <span data-ttu-id="7db1b-106">Взамен рекомендуется использовать <xref:Microsoft.Quantum.Arrays.Zipped>.</span><span class="sxs-lookup"><span data-stu-id="7db1b-106">Please use <xref:Microsoft.Quantum.Arrays.Zipped> instead.</span></span>

<span data-ttu-id="7db1b-107">При наличии двух массивов возвращает новый массив пар, в котором каждая пара содержит элемент из каждого исходного массива.</span><span class="sxs-lookup"><span data-stu-id="7db1b-107">Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.</span></span>

```qsharp
function Zip<'T, 'U> (left : 'T[], right : 'U[]) : ('T, 'U)[]
```


## <a name="input"></a><span data-ttu-id="7db1b-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7db1b-108">Input</span></span>

### <a name="left--t"></a><span data-ttu-id="7db1b-109">Left: ' ' []</span><span class="sxs-lookup"><span data-stu-id="7db1b-109">left : 'T[]</span></span>

<span data-ttu-id="7db1b-110">Массив, содержащий значения для первого элемента каждого кортежа.</span><span class="sxs-lookup"><span data-stu-id="7db1b-110">An array containing values for the first element of each tuple.</span></span>


### <a name="right--u"></a><span data-ttu-id="7db1b-111">Right: ' U []</span><span class="sxs-lookup"><span data-stu-id="7db1b-111">right : 'U[]</span></span>

<span data-ttu-id="7db1b-112">Массив, содержащий значения для второго элемента каждого кортежа.</span><span class="sxs-lookup"><span data-stu-id="7db1b-112">An array containing values for the second element of each tuple.</span></span>



## <a name="output--tu"></a><span data-ttu-id="7db1b-113">Выходные данные: ('T, ' U) []</span><span class="sxs-lookup"><span data-stu-id="7db1b-113">Output : ('T,'U)[]</span></span>

<span data-ttu-id="7db1b-114">Массив, содержащий пары форм `(left[idx], right[idx])` для каждого из них `idx` .</span><span class="sxs-lookup"><span data-stu-id="7db1b-114">An array containing pairs of the form `(left[idx], right[idx])` for each `idx`.</span></span> <span data-ttu-id="7db1b-115">Если два массива не имеют одинаковую длину, выходные данные будут иметь длину до более короткой из входных значений.</span><span class="sxs-lookup"><span data-stu-id="7db1b-115">If the two arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="7db1b-116">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="7db1b-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7db1b-117">Е</span><span class="sxs-lookup"><span data-stu-id="7db1b-117">'T</span></span>

<span data-ttu-id="7db1b-118">Тип элементов левого массива.</span><span class="sxs-lookup"><span data-stu-id="7db1b-118">The type of the left array elements.</span></span>
### <a name="u"></a><span data-ttu-id="7db1b-119">' U</span><span class="sxs-lookup"><span data-stu-id="7db1b-119">'U</span></span>

<span data-ttu-id="7db1b-120">Тип правых элементов массива.</span><span class="sxs-lookup"><span data-stu-id="7db1b-120">The type of the right array elements.</span></span>

## <a name="example"></a><span data-ttu-id="7db1b-121">Пример</span><span class="sxs-lookup"><span data-stu-id="7db1b-121">Example</span></span>

```qsharp
let left = [1, 3, 71];
let right = [false, true];
let pairs = Zip(left, right); // [(1, false), (3, true)]
```

## <a name="see-also"></a><span data-ttu-id="7db1b-122">См. также:</span><span class="sxs-lookup"><span data-stu-id="7db1b-122">See Also</span></span>

- [<span data-ttu-id="7db1b-123">Microsoft.Quantum.Arrays.Zip3</span><span class="sxs-lookup"><span data-stu-id="7db1b-123">Microsoft.Quantum.Arrays.Zip3</span></span>](xref:Microsoft.Quantum.Arrays.Zip3)
- [<span data-ttu-id="7db1b-124">Microsoft.Quantum.Arrays.Zip4</span><span class="sxs-lookup"><span data-stu-id="7db1b-124">Microsoft.Quantum.Arrays.Zip4</span></span>](xref:Microsoft.Quantum.Arrays.Zip4)
- [<span data-ttu-id="7db1b-125">Microsoft. тактов. Arrays. unzipped</span><span class="sxs-lookup"><span data-stu-id="7db1b-125">Microsoft.Quantum.Arrays.Unzipped</span></span>](xref:Microsoft.Quantum.Arrays.Unzipped)