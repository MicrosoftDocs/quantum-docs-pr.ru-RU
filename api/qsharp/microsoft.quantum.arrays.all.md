---
uid: Microsoft.Quantum.Arrays.All
title: ALL, функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: All
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, and checks if all elements of the array satisfy the predicate.
ms.openlocfilehash: 17e61ea161b90fe089b7df7c10188d604d72dcfa
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842899"
---
# <a name="all-function"></a><span data-ttu-id="24740-102">ALL, функция</span><span class="sxs-lookup"><span data-stu-id="24740-102">All function</span></span>

<span data-ttu-id="24740-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="24740-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="24740-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="24740-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="24740-105">При наличии массива и предиката, определенного для элементов массива, и проверяет, удовлетворяет ли предикату все элементы массива.</span><span class="sxs-lookup"><span data-stu-id="24740-105">Given an array and a predicate that is defined for the elements of the array, and checks if all elements of the array satisfy the predicate.</span></span>

```qsharp
function All<'T> (predicate : ('T -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="24740-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="24740-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="24740-107">предикат: не> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="24740-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="24740-108">Функция из `'T` в `Bool` , используемая для проверки элементов.</span><span class="sxs-lookup"><span data-stu-id="24740-108">A function from `'T` to `Bool` that is used to check elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="24740-109">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="24740-109">array : 'T[]</span></span>

<span data-ttu-id="24740-110">Массив элементов `'T` .</span><span class="sxs-lookup"><span data-stu-id="24740-110">An array of elements over `'T`.</span></span>



## <a name="output--bool"></a><span data-ttu-id="24740-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="24740-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="24740-112">`Bool`Значение функции и предиката, применяемого ко всем элементам.</span><span class="sxs-lookup"><span data-stu-id="24740-112">A `Bool` value of the AND function of the predicate applied to all elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="24740-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="24740-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="24740-114">Е</span><span class="sxs-lookup"><span data-stu-id="24740-114">'T</span></span>

<span data-ttu-id="24740-115">Тип `array` элементов.</span><span class="sxs-lookup"><span data-stu-id="24740-115">The type of `array` elements.</span></span>

## <a name="example"></a><span data-ttu-id="24740-116">Пример</span><span class="sxs-lookup"><span data-stu-id="24740-116">Example</span></span>

<span data-ttu-id="24740-117">Следующий код проверяет, не являются ли все элементы массива ненулевыми:</span><span class="sxs-lookup"><span data-stu-id="24740-117">The following code checks whether all elements of the array are non-zero:</span></span>

```qsharp
open Microsoft.Quantum.Arrays;
open Microsoft.Quantum.Logical;

function AllDemo() : Unit {
    let predicate = NotEqualI(_, 0);
    let isNonZero = All(predicate, [2, 3, 4, 5, 6, 0]);
    Message($"{isNonZero}");
}
```

## <a name="remarks"></a><span data-ttu-id="24740-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="24740-118">Remarks</span></span>

<span data-ttu-id="24740-119">Функция определена для универсальных типов, т. е. при наличии массива `'T[]` и функции `predicate: 'T -> Bool` мы можем получить `Bool` значение, которое указывает, соответствуют ли все элементы `predicate` .</span><span class="sxs-lookup"><span data-stu-id="24740-119">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a function `predicate: 'T -> Bool` we can produce a `Bool` value that indicates if all elements satisfy `predicate`.</span></span>