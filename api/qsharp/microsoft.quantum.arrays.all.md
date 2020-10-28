---
uid: Microsoft.Quantum.Arrays.All
title: ALL, функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: All
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, and checks if all elements of the array satisfy the predicate.
ms.openlocfilehash: 345c3fb92babd4ae2e54803b6c3b79b3313ef417
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730424"
---
# <a name="all-function"></a><span data-ttu-id="6c4ab-102">ALL, функция</span><span class="sxs-lookup"><span data-stu-id="6c4ab-102">All function</span></span>

<span data-ttu-id="6c4ab-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="6c4ab-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="6c4ab-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6c4ab-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6c4ab-105">При наличии массива и предиката, определенного для элементов массива, и проверяет, удовлетворяет ли предикату все элементы массива.</span><span class="sxs-lookup"><span data-stu-id="6c4ab-105">Given an array and a predicate that is defined for the elements of the array, and checks if all elements of the array satisfy the predicate.</span></span>

```qsharp
function All<'T> (predicate : ('T -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="6c4ab-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="6c4ab-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="6c4ab-107">предикат: не> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="6c4ab-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="6c4ab-108">Функция из `'T` в `Bool` , используемая для проверки элементов.</span><span class="sxs-lookup"><span data-stu-id="6c4ab-108">A function from `'T` to `Bool` that is used to check elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="6c4ab-109">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="6c4ab-109">array : 'T[]</span></span>

<span data-ttu-id="6c4ab-110">Массив элементов `'T` .</span><span class="sxs-lookup"><span data-stu-id="6c4ab-110">An array of elements over `'T`.</span></span>



## <a name="output--bool"></a><span data-ttu-id="6c4ab-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="6c4ab-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="6c4ab-112">`Bool`Значение функции и предиката, применяемого ко всем элементам.</span><span class="sxs-lookup"><span data-stu-id="6c4ab-112">A `Bool` value of the AND function of the predicate applied to all elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="6c4ab-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="6c4ab-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6c4ab-114">Е</span><span class="sxs-lookup"><span data-stu-id="6c4ab-114">'T</span></span>

<span data-ttu-id="6c4ab-115">Тип `array` элементов.</span><span class="sxs-lookup"><span data-stu-id="6c4ab-115">The type of `array` elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c4ab-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="6c4ab-116">Remarks</span></span>

<span data-ttu-id="6c4ab-117">Функция определена для универсальных типов, т. е. при наличии массива `'T[]` и функции `predicate: 'T -> Bool` мы можем получить `Bool` значение, которое указывает, соответствуют ли все элементы `predicate` .</span><span class="sxs-lookup"><span data-stu-id="6c4ab-117">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a function `predicate: 'T -> Bool` we can produce a `Bool` value that indicates if all elements satisfy `predicate`.</span></span>