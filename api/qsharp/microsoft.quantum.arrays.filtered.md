---
uid: Microsoft.Quantum.Arrays.Filtered
title: Отфильтрованная функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Filtered
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, returns an array that consists of those elements that satisfy the predicate.
ms.openlocfilehash: 83336b7001ce1d8ab1f5340b194abdcf93588c31
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847159"
---
# <a name="filtered-function"></a><span data-ttu-id="e6522-102">Отфильтрованная функция</span><span class="sxs-lookup"><span data-stu-id="e6522-102">Filtered function</span></span>

<span data-ttu-id="e6522-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="e6522-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="e6522-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e6522-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e6522-105">При наличии массива и предиката, определенного для элементов массива, возвращает массив, состоящий из элементов, которые соответствуют предикату.</span><span class="sxs-lookup"><span data-stu-id="e6522-105">Given an array and a predicate that is defined for the elements of the array, returns an array that consists of those elements that satisfy the predicate.</span></span>

```qsharp
function Filtered<'T> (predicate : ('T -> Bool), array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="e6522-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e6522-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="e6522-107">предикат: не> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="e6522-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="e6522-108">Функция из `'T` в логическое значение, используемое для фильтрации элементов.</span><span class="sxs-lookup"><span data-stu-id="e6522-108">A function from `'T` to Boolean that is used to filter elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="e6522-109">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="e6522-109">array : 'T[]</span></span>

<span data-ttu-id="e6522-110">Массив элементов `'T` .</span><span class="sxs-lookup"><span data-stu-id="e6522-110">An array of elements over `'T`.</span></span>



## <a name="output--t"></a><span data-ttu-id="e6522-111">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="e6522-111">Output : 'T[]</span></span>

<span data-ttu-id="e6522-112">Массив `'T[]` элементов, которые соответствуют предикату.</span><span class="sxs-lookup"><span data-stu-id="e6522-112">An array `'T[]` of elements that satisfy the predicate.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="e6522-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="e6522-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e6522-114">Е</span><span class="sxs-lookup"><span data-stu-id="e6522-114">'T</span></span>

<span data-ttu-id="e6522-115">Тип `array` элементов.</span><span class="sxs-lookup"><span data-stu-id="e6522-115">The type of `array` elements.</span></span>

## <a name="example"></a><span data-ttu-id="e6522-116">Пример</span><span class="sxs-lookup"><span data-stu-id="e6522-116">Example</span></span>

<span data-ttu-id="e6522-117">В следующем коде показана функция FILTERED.</span><span class="sxs-lookup"><span data-stu-id="e6522-117">The following code demonstrates the "Filtered" function.</span></span>
<span data-ttu-id="e6522-118">Предикат определяется с помощью @"microsoft.quantum.logical.greaterthani" функции:</span><span class="sxs-lookup"><span data-stu-id="e6522-118">A predicate is defined using the @"microsoft.quantum.logical.greaterthani" function:</span></span>

```qsharp
open Microsoft.Quantum.Arrays;
open Microsoft.Quantum.Logical;

function FilteredDemo() : Unit {
   let predicate = GreaterThanI(_, 5);
   let filteredArray = Filtered(predicate, [2, 5, 9, 1, 8]);
   Message($"{filteredArray}");
}
```

<span data-ttu-id="e6522-119">Результат, ожидаемый в этом примере, должен быть массивом чисел, превышающим 5.</span><span class="sxs-lookup"><span data-stu-id="e6522-119">The outcome one should expect from this example will be an array of numbers greater than 5.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6522-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="e6522-120">Remarks</span></span>

<span data-ttu-id="e6522-121">Функция определена для универсальных типов, т. е. при наличии массива `'T[]` и предиката `'T -> Bool` можно фильтровать элементы.</span><span class="sxs-lookup"><span data-stu-id="e6522-121">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a predicate `'T -> Bool` we can filter elements.</span></span>