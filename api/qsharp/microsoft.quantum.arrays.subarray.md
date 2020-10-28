---
uid: Microsoft.Quantum.Arrays.Subarray
title: Функция подмассивов
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Subarray
qsharp.summary: Takes an array and a list of locations and produces a new array formed from the elements of the original array that match the given locations.
ms.openlocfilehash: be7b6ee1a396d67ebc311d8d97f4bd751a32d171
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730000"
---
# <a name="subarray-function"></a><span data-ttu-id="04568-102">Функция подмассивов</span><span class="sxs-lookup"><span data-stu-id="04568-102">Subarray function</span></span>

<span data-ttu-id="04568-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="04568-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="04568-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="04568-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="04568-105">Принимает массив и список расположений и создает новый массив, сформированный из элементов исходного массива, которые соответствуют заданным местам.</span><span class="sxs-lookup"><span data-stu-id="04568-105">Takes an array and a list of locations and produces a new array formed from the elements of the original array that match the given locations.</span></span>

```qsharp
function Subarray<'T> (indices : Int[], array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="04568-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="04568-106">Input</span></span>

### <a name="indices--int"></a><span data-ttu-id="04568-107">индексы: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="04568-107">indices : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="04568-108">Список целых чисел, используемый для определения подмассива.</span><span class="sxs-lookup"><span data-stu-id="04568-108">A list of integers that is used to define the subarray.</span></span>


### <a name="array--t"></a><span data-ttu-id="04568-109">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="04568-109">array : 'T[]</span></span>

<span data-ttu-id="04568-110">Массив элементов `'T` .</span><span class="sxs-lookup"><span data-stu-id="04568-110">An array of elements over `'T`.</span></span>



## <a name="output--t"></a><span data-ttu-id="04568-111">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="04568-111">Output : 'T[]</span></span>

<span data-ttu-id="04568-112">Массив `out` элементов, индексы которых соответствуют подмассиву `out[idx] == array[indices[idx]]` .</span><span class="sxs-lookup"><span data-stu-id="04568-112">An array `out` of elements whose indices correspond to the subarray, such that `out[idx] == array[indices[idx]]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="04568-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="04568-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="04568-114">Е</span><span class="sxs-lookup"><span data-stu-id="04568-114">'T</span></span>

<span data-ttu-id="04568-115">Тип `array` элементов.</span><span class="sxs-lookup"><span data-stu-id="04568-115">The type of `array` elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="04568-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="04568-116">Remarks</span></span>

<span data-ttu-id="04568-117">Функция определена для универсальных типов, т. е. при наличии массива `'T[]` и списка расположений, `Int[]` определяющих этот подмассив.</span><span class="sxs-lookup"><span data-stu-id="04568-117">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a list of locations `Int[]` defining the subarray.</span></span>
<span data-ttu-id="04568-118">Построение подмассива основано на создании новой глубокой копии заданного массива, а не на обслуживании ссылок.</span><span class="sxs-lookup"><span data-stu-id="04568-118">The construction of the subarray is a based on generating a new, deep copy of the given array as opposed to maintaining references.</span></span>

<span data-ttu-id="04568-119">Если значение равно `Length(indices) < Length(array)` , эта функция вернет подмножество `array` .</span><span class="sxs-lookup"><span data-stu-id="04568-119">If `Length(indices) < Length(array)`, this function will return a subset of `array`.</span></span> <span data-ttu-id="04568-120">С другой стороны, если `indices` содержит повторяющиеся элементы, соответствующие элементы `array` будут также повторяться.</span><span class="sxs-lookup"><span data-stu-id="04568-120">On the other hand, if `indices` contains repeated elements, the corresponding elements of `array` will likewise be repeated.</span></span>
<span data-ttu-id="04568-121">Если `indices` и `array` имеют одинаковую длину, эта функция предоставляет перестановки `array` .</span><span class="sxs-lookup"><span data-stu-id="04568-121">If `indices` and `array` are the same length, this function provides permutations of `array`.</span></span>