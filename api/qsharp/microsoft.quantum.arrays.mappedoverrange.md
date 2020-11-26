---
uid: Microsoft.Quantum.Arrays.MappedOverRange
title: Функция Маппедоверранже
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedOverRange
qsharp.summary: Given a range and a function that takes an integer as input, returns a new array that consists of the images of the range values under the function.
ms.openlocfilehash: b1d73c2503e63ed09a3d6a56421760ca29eb0c3f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220694"
---
# <a name="mappedoverrange-function"></a><span data-ttu-id="40d85-102">Функция Маппедоверранже</span><span class="sxs-lookup"><span data-stu-id="40d85-102">MappedOverRange function</span></span>

<span data-ttu-id="40d85-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="40d85-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="40d85-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="40d85-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="40d85-105">При наличии диапазона и функции, принимающей в качестве входных данных целое число, возвращает новый массив, состоящий из изображений значений диапазона в функции.</span><span class="sxs-lookup"><span data-stu-id="40d85-105">Given a range and a function that takes an integer as input, returns a new array that consists of the images of the range values under the function.</span></span>

```qsharp
function MappedOverRange<'T> (mapper : (Int -> 'T), range : Range) : 'T[]
```


## <a name="input"></a><span data-ttu-id="40d85-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="40d85-106">Input</span></span>

### <a name="mapper--int---t"></a><span data-ttu-id="40d85-107">сопоставитель: [int](xref:microsoft.quantum.lang-ref.int) -></span><span class="sxs-lookup"><span data-stu-id="40d85-107">mapper : [Int](xref:microsoft.quantum.lang-ref.int) -> 'T</span></span>

<span data-ttu-id="40d85-108">Функция из `Int` в `'T` , используемая для отображения значений диапазона.</span><span class="sxs-lookup"><span data-stu-id="40d85-108">A function from `Int` to `'T` that is used to map range values.</span></span>


### <a name="range--range"></a><span data-ttu-id="40d85-109">диапазон: [диапазон](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="40d85-109">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="40d85-110">Диапазон целых чисел.</span><span class="sxs-lookup"><span data-stu-id="40d85-110">A range of integers.</span></span>



## <a name="output--t"></a><span data-ttu-id="40d85-111">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="40d85-111">Output : 'T[]</span></span>

<span data-ttu-id="40d85-112">Массив `'T[]` элементов, сопоставленных с `mapper` функцией.</span><span class="sxs-lookup"><span data-stu-id="40d85-112">An array `'T[]` of elements that are mapped by the `mapper` function.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="40d85-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="40d85-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="40d85-114">Е</span><span class="sxs-lookup"><span data-stu-id="40d85-114">'T</span></span>

<span data-ttu-id="40d85-115">Тип результата `mapper` функции.</span><span class="sxs-lookup"><span data-stu-id="40d85-115">The result type of the `mapper` function.</span></span>

## <a name="remarks"></a><span data-ttu-id="40d85-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="40d85-116">Remarks</span></span>

<span data-ttu-id="40d85-117">Функция определена для универсальных типов, т. е. каждый раз, когда у нас есть функция, `mapper: Int -> 'T` можно сопоставлять значения диапазона и создавать массив типа `'T[]` .</span><span class="sxs-lookup"><span data-stu-id="40d85-117">The function is defined for generic types, i.e., whenever we have a function `mapper: Int -> 'T` we can map the values of the range and produce an array of type `'T[]`.</span></span>

## <a name="see-also"></a><span data-ttu-id="40d85-118">См. также:</span><span class="sxs-lookup"><span data-stu-id="40d85-118">See Also</span></span>

- [<span data-ttu-id="40d85-119">Microsoft. тактов. Arrays. сопоставить</span><span class="sxs-lookup"><span data-stu-id="40d85-119">Microsoft.Quantum.Arrays.Mapped</span></span>](xref:Microsoft.Quantum.Arrays.Mapped)