---
uid: Microsoft.Quantum.Arrays.Any
title: Любая функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Any
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, checks if at least one element of the array satisfies the predicate.
ms.openlocfilehash: a05f9531168bf2b32977665d38cc00f3c8e64879
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846282"
---
# <a name="any-function"></a><span data-ttu-id="fbdf4-102">Любая функция</span><span class="sxs-lookup"><span data-stu-id="fbdf4-102">Any function</span></span>

<span data-ttu-id="fbdf4-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="fbdf4-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="fbdf4-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fbdf4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fbdf4-105">При наличии массива и предиката, определенного для элементов массива, проверяет, удовлетворяет ли предикату хотя бы один элемент массива.</span><span class="sxs-lookup"><span data-stu-id="fbdf4-105">Given an array and a predicate that is defined for the elements of the array, checks if at least one element of the array satisfies the predicate.</span></span>

```qsharp
function Any<'T> (predicate : ('T -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="fbdf4-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="fbdf4-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="fbdf4-107">предикат: не> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="fbdf4-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="fbdf4-108">Функция из `'T` в `Bool` , используемая для проверки элементов.</span><span class="sxs-lookup"><span data-stu-id="fbdf4-108">A function from `'T` to `Bool` that is used to check elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="fbdf4-109">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="fbdf4-109">array : 'T[]</span></span>

<span data-ttu-id="fbdf4-110">Массив элементов `'T` .</span><span class="sxs-lookup"><span data-stu-id="fbdf4-110">An array of elements over `'T`.</span></span>



## <a name="output--bool"></a><span data-ttu-id="fbdf4-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="fbdf4-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="fbdf4-112">`Bool`Значение функции или предиката, применяемого ко всем элементам.</span><span class="sxs-lookup"><span data-stu-id="fbdf4-112">A `Bool` value of the OR function of the predicate applied to all elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="fbdf4-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="fbdf4-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="fbdf4-114">Е</span><span class="sxs-lookup"><span data-stu-id="fbdf4-114">'T</span></span>

<span data-ttu-id="fbdf4-115">Тип `array` элементов.</span><span class="sxs-lookup"><span data-stu-id="fbdf4-115">The type of `array` elements.</span></span>

## <a name="example"></a><span data-ttu-id="fbdf4-116">Пример</span><span class="sxs-lookup"><span data-stu-id="fbdf4-116">Example</span></span>

```qsharp
open Microsoft.Quantum.Arrays;
open Microsoft.Quantum.Logical;

function IsThreePresent() : Bool {
    let arrayOfInts = [1, 2, 3, 4, 5];
    let is3Present = IsNumberPresentInArray(3, arrayOfInts);
    return is3Present;
}

function IsNumberPresentInArray(n : Int, array : Int[]) : Bool {
    return Any(EqualI(_, n), array);
}
```

## <a name="remarks"></a><span data-ttu-id="fbdf4-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="fbdf4-117">Remarks</span></span>

<span data-ttu-id="fbdf4-118">Функция определена для универсальных типов, т. е. при наличии массива `'T[]` и функции `predicate: 'T -> Bool` мы можем получить `Bool` значение, которое указывает, удовлетворяет ли какой-либо элемент `predicate` .</span><span class="sxs-lookup"><span data-stu-id="fbdf4-118">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a function `predicate: 'T -> Bool` we can produce a `Bool` value that indicates if some element satisfies `predicate`.</span></span>