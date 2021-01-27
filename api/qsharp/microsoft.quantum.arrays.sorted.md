---
uid: Microsoft.Quantum.Arrays.Sorted
title: Функция сортировки
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Sorted
qsharp.summary: Given an array, returns the elements of that array sorted by a given comparison function.
ms.openlocfilehash: cb8a1ef438d798c8201ed9f52677e253770df1d3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845449"
---
# <a name="sorted-function"></a><span data-ttu-id="37cc2-102">Функция сортировки</span><span class="sxs-lookup"><span data-stu-id="37cc2-102">Sorted function</span></span>

<span data-ttu-id="37cc2-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="37cc2-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="37cc2-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="37cc2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="37cc2-105">При наличии массива возвращает элементы этого массива, отсортированные по заданной функции сравнения.</span><span class="sxs-lookup"><span data-stu-id="37cc2-105">Given an array, returns the elements of that array sorted by a given comparison function.</span></span>

```qsharp
function Sorted<'T> (comparison : (('T, 'T) -> Bool), array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="37cc2-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="37cc2-106">Input</span></span>

### <a name="comparison--tt---bool"></a><span data-ttu-id="37cc2-107">Сравнение: ('T) — > [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="37cc2-107">comparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="37cc2-108">Функция, которая сравнивает два элемента, которые `a` считаются меньше или равными, `b` Если `comparison(a, b)` имеет значение `true` .</span><span class="sxs-lookup"><span data-stu-id="37cc2-108">A function that compares two elements such that `a` is considered to be less than or equal to `b` if `comparison(a, b)` is `true`.</span></span>


### <a name="array--t"></a><span data-ttu-id="37cc2-109">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="37cc2-109">array : 'T[]</span></span>

<span data-ttu-id="37cc2-110">Массив для сортировки.</span><span class="sxs-lookup"><span data-stu-id="37cc2-110">The array to be sorted.</span></span>



## <a name="output--t"></a><span data-ttu-id="37cc2-111">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="37cc2-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="37cc2-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="37cc2-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="37cc2-113">Е</span><span class="sxs-lookup"><span data-stu-id="37cc2-113">'T</span></span>

<span data-ttu-id="37cc2-114">Тип каждого элемента `array` .</span><span class="sxs-lookup"><span data-stu-id="37cc2-114">The type of each element of `array`.</span></span>

## <a name="example"></a><span data-ttu-id="37cc2-115">Пример</span><span class="sxs-lookup"><span data-stu-id="37cc2-115">Example</span></span>

<span data-ttu-id="37cc2-116">Следующий фрагмент кода сортирует массив целых чисел в возрастающем порядке:</span><span class="sxs-lookup"><span data-stu-id="37cc2-116">The following snippet sorts an array of integers to occur in ascending order:</span></span>

```qsharp
let sortedArray = Sorted(LessThanOrEqualI, [3, 17, 11, -201, -11]);
```

## <a name="remarks"></a><span data-ttu-id="37cc2-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="37cc2-117">Remarks</span></span>

<span data-ttu-id="37cc2-118">`comparison`Предполагается, что функция является транзитивным, например, если `comparison(a, b)` `comparison(b, c)` `comparison(a, c)` предполагается и.</span><span class="sxs-lookup"><span data-stu-id="37cc2-118">The function `comparison` is assumed to be transitive, such that if `comparison(a, b)` and `comparison(b, c)`, then `comparison(a, c)` is assumed.</span></span> <span data-ttu-id="37cc2-119">Если это свойство не удерживает, выходные данные этой функции могут быть неправильными.</span><span class="sxs-lookup"><span data-stu-id="37cc2-119">If this property does not hold, then the output of this function may be incorrect.</span></span>

<span data-ttu-id="37cc2-120">Так как это функция, результаты полностью детерминированные, даже если два элемента считаются равными по отношению к, `comparison` то есть когда `comparison(a, b)` и `comparison(b, a)` оба являются `true` .</span><span class="sxs-lookup"><span data-stu-id="37cc2-120">As this is a function, the results are completely determinstic, even when two elements are considered equal under `comparison`; that is, when `comparison(a, b)` and `comparison(b, a)` are both `true`.</span></span>
<span data-ttu-id="37cc2-121">В частности, сортировка, выполняемая этой функцией, гарантированно стабильной, поэтому если два элемента `a` и `b` выполняются в этом порядке в `array` и считаются равными в `comparison` , то `a` `b` в выходных данных также будет появляться.</span><span class="sxs-lookup"><span data-stu-id="37cc2-121">In particular, the sort performed by this function is guaranteed to be stable, so that if two elements `a` and `b` occur in that order within `array` and are considered equal under `comparison`, then `a` will also appear before `b` in the output.</span></span>

<span data-ttu-id="37cc2-122">Пример:</span><span class="sxs-lookup"><span data-stu-id="37cc2-122">For example:</span></span>

```qsharp
function LastDigitLessThanOrEqual(left : Int, right : Int) : Bool {
    return LessThanOrEqualI(
        left % 10, right % 10
    );
}

function SortedByLastDigit() : Int[] {
    return Sorted(LastDigitLessThanOrEqual, [3, 37, 11, 17]);
}
// returns [11, 3, 37, 17].
```