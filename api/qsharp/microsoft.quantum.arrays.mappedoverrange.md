---
uid: Microsoft.Quantum.Arrays.MappedOverRange
title: Функция Маппедоверранже
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedOverRange
qsharp.summary: Given a range and a function that takes an integer as input, returns a new array that consists of the images of the range values under the function.
ms.openlocfilehash: 7093043e2a290e6132774b8fe154d3627a254f27
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845655"
---
# <a name="mappedoverrange-function"></a><span data-ttu-id="bba5d-102">Функция Маппедоверранже</span><span class="sxs-lookup"><span data-stu-id="bba5d-102">MappedOverRange function</span></span>

<span data-ttu-id="bba5d-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="bba5d-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="bba5d-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bba5d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bba5d-105">При наличии диапазона и функции, принимающей в качестве входных данных целое число, возвращает новый массив, состоящий из изображений значений диапазона в функции.</span><span class="sxs-lookup"><span data-stu-id="bba5d-105">Given a range and a function that takes an integer as input, returns a new array that consists of the images of the range values under the function.</span></span>

```qsharp
function MappedOverRange<'T> (mapper : (Int -> 'T), range : Range) : 'T[]
```


## <a name="input"></a><span data-ttu-id="bba5d-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="bba5d-106">Input</span></span>

### <a name="mapper--int---t"></a><span data-ttu-id="bba5d-107">сопоставитель: [int](xref:microsoft.quantum.lang-ref.int) -></span><span class="sxs-lookup"><span data-stu-id="bba5d-107">mapper : [Int](xref:microsoft.quantum.lang-ref.int) -> 'T</span></span>

<span data-ttu-id="bba5d-108">Функция из `Int` в `'T` , используемая для отображения значений диапазона.</span><span class="sxs-lookup"><span data-stu-id="bba5d-108">A function from `Int` to `'T` that is used to map range values.</span></span>


### <a name="range--range"></a><span data-ttu-id="bba5d-109">диапазон: [диапазон](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="bba5d-109">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="bba5d-110">Диапазон целых чисел.</span><span class="sxs-lookup"><span data-stu-id="bba5d-110">A range of integers.</span></span>



## <a name="output--t"></a><span data-ttu-id="bba5d-111">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="bba5d-111">Output : 'T[]</span></span>

<span data-ttu-id="bba5d-112">Массив `'T[]` элементов, сопоставленных с `mapper` функцией.</span><span class="sxs-lookup"><span data-stu-id="bba5d-112">An array `'T[]` of elements that are mapped by the `mapper` function.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="bba5d-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="bba5d-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="bba5d-114">Е</span><span class="sxs-lookup"><span data-stu-id="bba5d-114">'T</span></span>

<span data-ttu-id="bba5d-115">Тип результата `mapper` функции.</span><span class="sxs-lookup"><span data-stu-id="bba5d-115">The result type of the `mapper` function.</span></span>

## <a name="example"></a><span data-ttu-id="bba5d-116">Пример</span><span class="sxs-lookup"><span data-stu-id="bba5d-116">Example</span></span>

<span data-ttu-id="bba5d-117">В этом примере добавляется 1 к диапазону четных чисел:</span><span class="sxs-lookup"><span data-stu-id="bba5d-117">This example adds 1 to a range of even numbers:</span></span>

```qsharp
let numbers = MappedOverRange(PlusI(1, _), 0..2..10);
// numbers = [1, 3, 5, 7, 9, 11]
```

## <a name="remarks"></a><span data-ttu-id="bba5d-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="bba5d-118">Remarks</span></span>

<span data-ttu-id="bba5d-119">Функция определена для универсальных типов, т. е. каждый раз, когда у нас есть функция, `mapper: Int -> 'T` можно сопоставлять значения диапазона и создавать массив типа `'T[]` .</span><span class="sxs-lookup"><span data-stu-id="bba5d-119">The function is defined for generic types, i.e., whenever we have a function `mapper: Int -> 'T` we can map the values of the range and produce an array of type `'T[]`.</span></span>

## <a name="see-also"></a><span data-ttu-id="bba5d-120">См. также:</span><span class="sxs-lookup"><span data-stu-id="bba5d-120">See Also</span></span>

- [<span data-ttu-id="bba5d-121">Microsoft. тактов. Arrays. сопоставить</span><span class="sxs-lookup"><span data-stu-id="bba5d-121">Microsoft.Quantum.Arrays.Mapped</span></span>](xref:Microsoft.Quantum.Arrays.Mapped)