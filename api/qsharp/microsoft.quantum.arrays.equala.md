---
uid: Microsoft.Quantum.Arrays.EqualA
title: Функция EQUAL
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: EqualA
qsharp.summary: Given two arrays of the same type and a predicate that is defined for pairs of elements of the arrays, checks whether the arrays are equal.
ms.openlocfilehash: fe22e208f67d2c289b0b2d99f19ff26fc5abc3d8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848692"
---
# <a name="equala-function"></a><span data-ttu-id="22cfa-102">Функция EQUAL</span><span class="sxs-lookup"><span data-stu-id="22cfa-102">EqualA function</span></span>

<span data-ttu-id="22cfa-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="22cfa-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="22cfa-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="22cfa-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="22cfa-105">При наличии двух массивов одного типа и предиката, определенного для пар элементов массивов, проверяет, равны ли массивы.</span><span class="sxs-lookup"><span data-stu-id="22cfa-105">Given two arrays of the same type and a predicate that is defined for pairs of elements of the arrays, checks whether the arrays are equal.</span></span>

```qsharp
function EqualA<'T> (equal : (('T, 'T) -> Bool), array1 : 'T[], array2 : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="22cfa-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="22cfa-106">Input</span></span>

### <a name="equal--tt---bool"></a><span data-ttu-id="22cfa-107">равно: ('T) — > [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="22cfa-107">equal : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="22cfa-108">Функция из кортежа `('T, 'T)` в `Bool` , используемая для проверки того, равны ли два элемента массивов.</span><span class="sxs-lookup"><span data-stu-id="22cfa-108">A function from tuple `('T, 'T)` to `Bool` that is used to check whether two elements of arrays are equal.</span></span>


### <a name="array1--t"></a><span data-ttu-id="22cfa-109">Массив1: 'T []</span><span class="sxs-lookup"><span data-stu-id="22cfa-109">array1 : 'T[]</span></span>

<span data-ttu-id="22cfa-110">Первый сравниваемый массив.</span><span class="sxs-lookup"><span data-stu-id="22cfa-110">The first array to be compared.</span></span>


### <a name="array2--t"></a><span data-ttu-id="22cfa-111">Массив2: 'T []</span><span class="sxs-lookup"><span data-stu-id="22cfa-111">array2 : 'T[]</span></span>

<span data-ttu-id="22cfa-112">Второй сравниваемый массив.</span><span class="sxs-lookup"><span data-stu-id="22cfa-112">The second array to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="22cfa-113">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="22cfa-113">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="22cfa-114">Значение, `true` если и только если `array1` и `array2` равны.</span><span class="sxs-lookup"><span data-stu-id="22cfa-114">The value `true` if and only if `array1` and `array2` are equal.</span></span>
<span data-ttu-id="22cfa-115">То есть, если оба массива имеют одинаковую длину, и все элементы равны, как определено в `equal` .</span><span class="sxs-lookup"><span data-stu-id="22cfa-115">That is, if both arrays have the same length, and all elements are equal as defined by `equal`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="22cfa-116">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="22cfa-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="22cfa-117">Е</span><span class="sxs-lookup"><span data-stu-id="22cfa-117">'T</span></span>

<span data-ttu-id="22cfa-118">Тип элементов каждого массива.</span><span class="sxs-lookup"><span data-stu-id="22cfa-118">The type of each array's elements.</span></span>

## <a name="example"></a><span data-ttu-id="22cfa-119">Пример</span><span class="sxs-lookup"><span data-stu-id="22cfa-119">Example</span></span>

<span data-ttu-id="22cfa-120">Следующий код проверяет, равны ли разные пары массивов:</span><span class="sxs-lookup"><span data-stu-id="22cfa-120">The following code checks whether different pairs of arrays are equal:</span></span>

```qsharp
open Microsoft.Quantum.Arrays;
open Microsoft.Quantum.Logical;

function EqualADemo() : Unit {
    let equalArrays = EqualA(EqualI, [2, 3, 4], [2, 3, 4]);
    let differentLength = EqualA(EqualD, [2.0, 3.0, 4.0], [2.0, 3.0]);
    let differentElements = EqualA(EqualR, [One, Zero], [One, One]);
    Message($"Equal arrays are {equalArrays ? "equal" | "not equal"}");
    Message($"Arrays of different length are {differentLength ? "equal" | "not equal"}");
    Message($"Arrays of the same length with different elements are {differentElements ? "equal" | "not equal"}");
}
```

## <a name="remarks"></a><span data-ttu-id="22cfa-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="22cfa-121">Remarks</span></span>

<span data-ttu-id="22cfa-122">Эта функция определена для универсальных типов; Например, если у нас есть два массива `'T[]` и функция `equal: ('T, 'T) -> Bool` , эта функция возвращает `Bool` значение, указывающее, равны ли массивы.</span><span class="sxs-lookup"><span data-stu-id="22cfa-122">This function is defined for generic types; i.e., whenever we have two arrays `'T[]` and a function `equal: ('T, 'T) -> Bool`, this function returns a `Bool` value that indicates whether the arrays are equal.</span></span>
<span data-ttu-id="22cfa-123">Чтобы два массива считались равными, они должны иметь одинаковую длину, а элементы в одинаковых позициях массивов должны быть равны.</span><span class="sxs-lookup"><span data-stu-id="22cfa-123">For two arrays to be considered equal, they have to have equal length and the elements in the same positions in the arrays have to be equal.</span></span>