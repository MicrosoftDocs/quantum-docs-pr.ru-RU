---
uid: Microsoft.Quantum.Arrays.Subarray
title: Функция подмассивов
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Subarray
qsharp.summary: Takes an array and a list of locations and produces a new array formed from the elements of the original array that match the given locations.
ms.openlocfilehash: ccc041da0213d1f5dc5c8b4ff7a03b8b01ad107d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845419"
---
# <a name="subarray-function"></a><span data-ttu-id="f2058-102">Функция подмассивов</span><span class="sxs-lookup"><span data-stu-id="f2058-102">Subarray function</span></span>

<span data-ttu-id="f2058-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="f2058-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="f2058-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f2058-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f2058-105">Принимает массив и список расположений и создает новый массив, сформированный из элементов исходного массива, которые соответствуют заданным местам.</span><span class="sxs-lookup"><span data-stu-id="f2058-105">Takes an array and a list of locations and produces a new array formed from the elements of the original array that match the given locations.</span></span>

```qsharp
function Subarray<'T> (indices : Int[], array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="f2058-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f2058-106">Input</span></span>

### <a name="indices--int"></a><span data-ttu-id="f2058-107">индексы: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="f2058-107">indices : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="f2058-108">Список целых чисел, используемый для определения подмассива.</span><span class="sxs-lookup"><span data-stu-id="f2058-108">A list of integers that is used to define the subarray.</span></span>


### <a name="array--t"></a><span data-ttu-id="f2058-109">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="f2058-109">array : 'T[]</span></span>

<span data-ttu-id="f2058-110">Массив элементов `'T` .</span><span class="sxs-lookup"><span data-stu-id="f2058-110">An array of elements over `'T`.</span></span>



## <a name="output--t"></a><span data-ttu-id="f2058-111">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="f2058-111">Output : 'T[]</span></span>

<span data-ttu-id="f2058-112">Массив `out` элементов, индексы которых соответствуют подмассиву `out[idx] == array[indices[idx]]` .</span><span class="sxs-lookup"><span data-stu-id="f2058-112">An array `out` of elements whose indices correspond to the subarray, such that `out[idx] == array[indices[idx]]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="f2058-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="f2058-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f2058-114">Е</span><span class="sxs-lookup"><span data-stu-id="f2058-114">'T</span></span>

<span data-ttu-id="f2058-115">Тип `array` элементов.</span><span class="sxs-lookup"><span data-stu-id="f2058-115">The type of `array` elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2058-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="f2058-116">Remarks</span></span>

<span data-ttu-id="f2058-117">Функция определена для универсальных типов, т. е. при наличии массива `'T[]` и списка расположений, `Int[]` определяющих этот подмассив.</span><span class="sxs-lookup"><span data-stu-id="f2058-117">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a list of locations `Int[]` defining the subarray.</span></span>
<span data-ttu-id="f2058-118">Построение подмассива основано на создании новой глубокой копии заданного массива, а не на обслуживании ссылок.</span><span class="sxs-lookup"><span data-stu-id="f2058-118">The construction of the subarray is a based on generating a new, deep copy of the given array as opposed to maintaining references.</span></span>

<span data-ttu-id="f2058-119">Если значение равно `Length(indices) < Length(array)` , эта функция вернет подмножество `array` .</span><span class="sxs-lookup"><span data-stu-id="f2058-119">If `Length(indices) < Length(array)`, this function will return a subset of `array`.</span></span> <span data-ttu-id="f2058-120">С другой стороны, если `indices` содержит повторяющиеся элементы, соответствующие элементы `array` будут также повторяться.</span><span class="sxs-lookup"><span data-stu-id="f2058-120">On the other hand, if `indices` contains repeated elements, the corresponding elements of `array` will likewise be repeated.</span></span>
<span data-ttu-id="f2058-121">Если `indices` и `array` имеют одинаковую длину, эта функция предоставляет перестановки `array` .</span><span class="sxs-lookup"><span data-stu-id="f2058-121">If `indices` and `array` are the same length, this function provides permutations of `array`.</span></span>