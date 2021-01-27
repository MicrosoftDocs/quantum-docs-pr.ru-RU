---
uid: Microsoft.Quantum.Arrays.Zipped
title: Функция ZIP
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zipped
qsharp.summary: Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.
ms.openlocfilehash: 5177ab0ade5a9ad7788e60c1028befb84b0191d4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845334"
---
# <a name="zipped-function"></a><span data-ttu-id="52465-102">Функция ZIP</span><span class="sxs-lookup"><span data-stu-id="52465-102">Zipped function</span></span>

<span data-ttu-id="52465-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="52465-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="52465-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="52465-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="52465-105">При наличии двух массивов возвращает новый массив пар, в котором каждая пара содержит элемент из каждого исходного массива.</span><span class="sxs-lookup"><span data-stu-id="52465-105">Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.</span></span>

```qsharp
function Zipped<'T, 'U> (left : 'T[], right : 'U[]) : ('T, 'U)[]
```


## <a name="input"></a><span data-ttu-id="52465-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="52465-106">Input</span></span>

### <a name="left--t"></a><span data-ttu-id="52465-107">Left: ' ' []</span><span class="sxs-lookup"><span data-stu-id="52465-107">left : 'T[]</span></span>

<span data-ttu-id="52465-108">Массив, содержащий значения для первого элемента каждого кортежа.</span><span class="sxs-lookup"><span data-stu-id="52465-108">An array containing values for the first element of each tuple.</span></span>


### <a name="right--u"></a><span data-ttu-id="52465-109">Right: ' U []</span><span class="sxs-lookup"><span data-stu-id="52465-109">right : 'U[]</span></span>

<span data-ttu-id="52465-110">Массив, содержащий значения для второго элемента каждого кортежа.</span><span class="sxs-lookup"><span data-stu-id="52465-110">An array containing values for the second element of each tuple.</span></span>



## <a name="output--tu"></a><span data-ttu-id="52465-111">Выходные данные: ('T, ' U) []</span><span class="sxs-lookup"><span data-stu-id="52465-111">Output : ('T,'U)[]</span></span>

<span data-ttu-id="52465-112">Массив, содержащий пары форм `(left[idx], right[idx])` для каждого из них `idx` .</span><span class="sxs-lookup"><span data-stu-id="52465-112">An array containing pairs of the form `(left[idx], right[idx])` for each `idx`.</span></span> <span data-ttu-id="52465-113">Если два массива не имеют одинаковую длину, выходные данные будут иметь длину до более короткой из входных значений.</span><span class="sxs-lookup"><span data-stu-id="52465-113">If the two arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="52465-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="52465-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="52465-115">Е</span><span class="sxs-lookup"><span data-stu-id="52465-115">'T</span></span>

<span data-ttu-id="52465-116">Тип элементов левого массива.</span><span class="sxs-lookup"><span data-stu-id="52465-116">The type of the left array elements.</span></span>
### <a name="u"></a><span data-ttu-id="52465-117">' U</span><span class="sxs-lookup"><span data-stu-id="52465-117">'U</span></span>

<span data-ttu-id="52465-118">Тип правых элементов массива.</span><span class="sxs-lookup"><span data-stu-id="52465-118">The type of the right array elements.</span></span>

## <a name="example"></a><span data-ttu-id="52465-119">Пример</span><span class="sxs-lookup"><span data-stu-id="52465-119">Example</span></span>

```qsharp
let left = [1, 3, 71];
let right = [false, true];
let pairs = Zipped(left, right); // [(1, false), (3, true)]
```

## <a name="see-also"></a><span data-ttu-id="52465-120">См. также:</span><span class="sxs-lookup"><span data-stu-id="52465-120">See Also</span></span>

- [<span data-ttu-id="52465-121">Microsoft.Quantum.Arrays.Zipped3</span><span class="sxs-lookup"><span data-stu-id="52465-121">Microsoft.Quantum.Arrays.Zipped3</span></span>](xref:Microsoft.Quantum.Arrays.Zipped3)
- [<span data-ttu-id="52465-122">Microsoft.Quantum.Arrays.Zipped4</span><span class="sxs-lookup"><span data-stu-id="52465-122">Microsoft.Quantum.Arrays.Zipped4</span></span>](xref:Microsoft.Quantum.Arrays.Zipped4)
- [<span data-ttu-id="52465-123">Microsoft. тактов. Arrays. unzipped</span><span class="sxs-lookup"><span data-stu-id="52465-123">Microsoft.Quantum.Arrays.Unzipped</span></span>](xref:Microsoft.Quantum.Arrays.Unzipped)