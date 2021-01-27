---
uid: Microsoft.Quantum.Arrays.Unique
title: Уникальная функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Unique
qsharp.summary: Returns a new array that has no equal adjacent elements.
ms.openlocfilehash: b3aa03d20195bdd8bb64783a9b68cafac29e68f6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850922"
---
# <a name="unique-function"></a><span data-ttu-id="66cd1-102">Уникальная функция</span><span class="sxs-lookup"><span data-stu-id="66cd1-102">Unique function</span></span>

<span data-ttu-id="66cd1-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="66cd1-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="66cd1-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="66cd1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="66cd1-105">Возвращает новый массив, у которого нет равных смежных элементов.</span><span class="sxs-lookup"><span data-stu-id="66cd1-105">Returns a new array that has no equal adjacent elements.</span></span>

```qsharp
function Unique<'T> (equal : (('T, 'T) -> Bool), array : 'T[]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="66cd1-106">Описание</span><span class="sxs-lookup"><span data-stu-id="66cd1-106">Description</span></span>

<span data-ttu-id="66cd1-107">При наличии массива элементов и функции для проверки равенства эта функция возвращает новый массив, в котором сохраняется относительный порядок элементов, но все смежные элементы, которые равны, фильтруются только в один элемент.</span><span class="sxs-lookup"><span data-stu-id="66cd1-107">Given some array of elements and a function to test equality, this function returns a new array in which the relative order of elements is kept, but all adjacent elements which are equal are filtered to just a single element.</span></span>

## <a name="input"></a><span data-ttu-id="66cd1-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="66cd1-108">Input</span></span>

### <a name="equal--tt---bool"></a><span data-ttu-id="66cd1-109">равно: ('T) — > [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="66cd1-109">equal : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="66cd1-110">Функция, которая сравнивает два элемента, которые `a` считаются равными, `b` Если `equal(a, b)` имеет значение `true` .</span><span class="sxs-lookup"><span data-stu-id="66cd1-110">A function that compares two elements such that `a` is considered to be equal to `b` if `equal(a, b)` is `true`.</span></span>


### <a name="array--t"></a><span data-ttu-id="66cd1-111">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="66cd1-111">array : 'T[]</span></span>

<span data-ttu-id="66cd1-112">Массив для фильтрации уникальных элементов.</span><span class="sxs-lookup"><span data-stu-id="66cd1-112">The array to be filtered for unique elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="66cd1-113">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="66cd1-113">Output : 'T[]</span></span>

<span data-ttu-id="66cd1-114">Массив без равных смежных элементов.</span><span class="sxs-lookup"><span data-stu-id="66cd1-114">Array with no equal adjacent elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="66cd1-115">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="66cd1-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="66cd1-116">Е</span><span class="sxs-lookup"><span data-stu-id="66cd1-116">'T</span></span>

<span data-ttu-id="66cd1-117">Тип каждого элемента `array` .</span><span class="sxs-lookup"><span data-stu-id="66cd1-117">The type of each element of `array`.</span></span>

## <a name="example"></a><span data-ttu-id="66cd1-118">Пример</span><span class="sxs-lookup"><span data-stu-id="66cd1-118">Example</span></span>

```qsharp
let unique1 = Unique(EqualI, [1, 1, 3, 3, 2, 5, 5, 5, 7]);
// same as [1, 3, 2, 5, 7]
let unique2 = Unique(EqualI, [2, 2, 1, 1, 2, 2, 1, 1]);
// same as [2, 1, 2, 1];
let unique3 = Unique(EqualI, Sorted(LessThanOrEqualI, [2, 2, 1, 1, 2, 2, 1, 1]));
// same as [1, 2];
```

## <a name="remarks"></a><span data-ttu-id="66cd1-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="66cd1-119">Remarks</span></span>

<span data-ttu-id="66cd1-120">Если существует несколько элементов, которые равны, но не расположены рядом друг с другом, в выходном массиве будет несколько вхождений.</span><span class="sxs-lookup"><span data-stu-id="66cd1-120">If there are multiple elements that are equal but not next to each other, there will be multiple occurrences in the output array.</span></span>  <span data-ttu-id="66cd1-121">Используйте эту функцию вместе с `Sorted` для получения массива с общими уникальными элементами.</span><span class="sxs-lookup"><span data-stu-id="66cd1-121">Use this function together with `Sorted` to get an array with overall unique elements.</span></span>