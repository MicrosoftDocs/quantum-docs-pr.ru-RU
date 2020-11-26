---
uid: Microsoft.Quantum.Arrays.Sorted
title: Функция сортировки
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Sorted
qsharp.summary: Given an array, returns the elements of that array sorted by a given comparison function.
ms.openlocfilehash: bd8b869e03c7f4687c456a944e07a811ae0d2ce2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220235"
---
# <a name="sorted-function"></a><span data-ttu-id="bdfdf-102">Функция сортировки</span><span class="sxs-lookup"><span data-stu-id="bdfdf-102">Sorted function</span></span>

<span data-ttu-id="bdfdf-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="bdfdf-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="bdfdf-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bdfdf-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bdfdf-105">При наличии массива возвращает элементы этого массива, отсортированные по заданной функции сравнения.</span><span class="sxs-lookup"><span data-stu-id="bdfdf-105">Given an array, returns the elements of that array sorted by a given comparison function.</span></span>

```qsharp
function Sorted<'T> (comparison : (('T, 'T) -> Bool), array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="bdfdf-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="bdfdf-106">Input</span></span>

### <a name="comparison--tt---bool"></a><span data-ttu-id="bdfdf-107">Сравнение: ('T) — > [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="bdfdf-107">comparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="bdfdf-108">Функция, которая сравнивает два элемента, которые `a` считаются меньше или равными, `b` Если `comparison(a, b)` имеет значение `true` .</span><span class="sxs-lookup"><span data-stu-id="bdfdf-108">A function that compares two elements such that `a` is considered to be less than or equal to `b` if `comparison(a, b)` is `true`.</span></span>


### <a name="array--t"></a><span data-ttu-id="bdfdf-109">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="bdfdf-109">array : 'T[]</span></span>

<span data-ttu-id="bdfdf-110">Массив для сортировки.</span><span class="sxs-lookup"><span data-stu-id="bdfdf-110">The array to be sorted.</span></span>



## <a name="output--t"></a><span data-ttu-id="bdfdf-111">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="bdfdf-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="bdfdf-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="bdfdf-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="bdfdf-113">Е</span><span class="sxs-lookup"><span data-stu-id="bdfdf-113">'T</span></span>

<span data-ttu-id="bdfdf-114">Тип каждого элемента `array` .</span><span class="sxs-lookup"><span data-stu-id="bdfdf-114">The type of each element of `array`.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdfdf-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bdfdf-115">Remarks</span></span>

<span data-ttu-id="bdfdf-116">`comparison`Предполагается, что функция является транзитивным, например, если `comparison(a, b)` `comparison(b, c)` `comparison(a, c)` предполагается и.</span><span class="sxs-lookup"><span data-stu-id="bdfdf-116">The function `comparison` is assumed to be transitive, such that if `comparison(a, b)` and `comparison(b, c)`, then `comparison(a, c)` is assumed.</span></span> <span data-ttu-id="bdfdf-117">Если это свойство не удерживает, выходные данные этой функции могут быть неправильными.</span><span class="sxs-lookup"><span data-stu-id="bdfdf-117">If this property does not hold, then the output of this function may be incorrect.</span></span>

<span data-ttu-id="bdfdf-118">Так как это функция, результаты полностью детерминированные, даже если два элемента считаются равными по отношению к, `comparison` то есть когда `comparison(a, b)` и `comparison(b, a)` оба являются `true` .</span><span class="sxs-lookup"><span data-stu-id="bdfdf-118">As this is a function, the results are completely determinstic, even when two elements are considered equal under `comparison`; that is, when `comparison(a, b)` and `comparison(b, a)` are both `true`.</span></span>
<span data-ttu-id="bdfdf-119">В частности, сортировка, выполняемая этой функцией, гарантированно стабильной, поэтому если два элемента `a` и `b` выполняются в этом порядке в `array` и считаются равными в `comparison` , то `a` `b` в выходных данных также будет появляться.</span><span class="sxs-lookup"><span data-stu-id="bdfdf-119">In particular, the sort performed by this function is guaranteed to be stable, so that if two elements `a` and `b` occur in that order within `array` and are considered equal under `comparison`, then `a` will also appear before `b` in the output.</span></span>

<span data-ttu-id="bdfdf-120">Пример:</span><span class="sxs-lookup"><span data-stu-id="bdfdf-120">For example:</span></span>

```Q#
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