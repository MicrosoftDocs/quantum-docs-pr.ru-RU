---
uid: Microsoft.Quantum.Arrays.EqualA
title: Функция EQUAL
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: EqualA
qsharp.summary: Given two arrays of the same type and a predicate that is defined for pairs of elements of the arrays, checks whether the arrays are equal.
ms.openlocfilehash: 176e15139a27d375fb047c07fa1ee778dc8cc2ce
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221374"
---
# <a name="equala-function"></a><span data-ttu-id="51d44-102">Функция EQUAL</span><span class="sxs-lookup"><span data-stu-id="51d44-102">EqualA function</span></span>

<span data-ttu-id="51d44-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="51d44-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="51d44-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="51d44-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="51d44-105">При наличии двух массивов одного типа и предиката, определенного для пар элементов массивов, проверяет, равны ли массивы.</span><span class="sxs-lookup"><span data-stu-id="51d44-105">Given two arrays of the same type and a predicate that is defined for pairs of elements of the arrays, checks whether the arrays are equal.</span></span>

```qsharp
function EqualA<'T> (equal : (('T, 'T) -> Bool), array1 : 'T[], array2 : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="51d44-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="51d44-106">Input</span></span>

### <a name="equal--tt---bool"></a><span data-ttu-id="51d44-107">равно: ('T) — > [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="51d44-107">equal : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="51d44-108">Функция из кортежа `('T, 'T)` в `Bool` , используемая для проверки того, равны ли два элемента массивов.</span><span class="sxs-lookup"><span data-stu-id="51d44-108">A function from tuple `('T, 'T)` to `Bool` that is used to check whether two elements of arrays are equal.</span></span>


### <a name="array1--t"></a><span data-ttu-id="51d44-109">Массив1: 'T []</span><span class="sxs-lookup"><span data-stu-id="51d44-109">array1 : 'T[]</span></span>

<span data-ttu-id="51d44-110">Первый сравниваемый массив.</span><span class="sxs-lookup"><span data-stu-id="51d44-110">The first array to be compared.</span></span>


### <a name="array2--t"></a><span data-ttu-id="51d44-111">Массив2: 'T []</span><span class="sxs-lookup"><span data-stu-id="51d44-111">array2 : 'T[]</span></span>

<span data-ttu-id="51d44-112">Второй сравниваемый массив.</span><span class="sxs-lookup"><span data-stu-id="51d44-112">The second array to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="51d44-113">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="51d44-113">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="51d44-114">Значение, `true` если и только если `array1` и `array2` равны.</span><span class="sxs-lookup"><span data-stu-id="51d44-114">The value `true` if and only if `array1` and `array2` are equal.</span></span>
<span data-ttu-id="51d44-115">То есть, если оба массива имеют одинаковую длину, и все элементы равны, как определено в `equal` .</span><span class="sxs-lookup"><span data-stu-id="51d44-115">That is, if both arrays have the same length, and all elements are equal as defined by `equal`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="51d44-116">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="51d44-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="51d44-117">Е</span><span class="sxs-lookup"><span data-stu-id="51d44-117">'T</span></span>

<span data-ttu-id="51d44-118">Тип элементов каждого массива.</span><span class="sxs-lookup"><span data-stu-id="51d44-118">The type of each array's elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="51d44-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="51d44-119">Remarks</span></span>

<span data-ttu-id="51d44-120">Эта функция определена для универсальных типов; Например, если у нас есть два массива `'T[]` и функция `equal: ('T, 'T) -> Bool` , эта функция возвращает `Bool` значение, указывающее, равны ли массивы.</span><span class="sxs-lookup"><span data-stu-id="51d44-120">This function is defined for generic types; i.e., whenever we have two arrays `'T[]` and a function `equal: ('T, 'T) -> Bool`, this function returns a `Bool` value that indicates whether the arrays are equal.</span></span>
<span data-ttu-id="51d44-121">Чтобы два массива считались равными, они должны иметь одинаковую длину, а элементы в одинаковых позициях массивов должны быть равны.</span><span class="sxs-lookup"><span data-stu-id="51d44-121">For two arrays to be considered equal, they have to have equal length and the elements in the same positions in the arrays have to be equal.</span></span>