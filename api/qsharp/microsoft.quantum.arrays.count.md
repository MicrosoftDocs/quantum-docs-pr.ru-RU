---
uid: Microsoft.Quantum.Arrays.Count
title: Count, функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Count
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, returns the number of elements an array that consists of those elements that satisfy the predicate.
ms.openlocfilehash: e178ee63526e3485e8cc83a3ba8f827d8ecac552
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842852"
---
# <a name="count-function"></a><span data-ttu-id="ee14a-102">Count, функция</span><span class="sxs-lookup"><span data-stu-id="ee14a-102">Count function</span></span>

<span data-ttu-id="ee14a-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="ee14a-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="ee14a-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ee14a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ee14a-105">При наличии массива и предиката, определенного для элементов массива, возвращает число элементов массива, состоящего из элементов, которые соответствуют предикату.</span><span class="sxs-lookup"><span data-stu-id="ee14a-105">Given an array and a predicate that is defined for the elements of the array, returns the number of elements an array that consists of those elements that satisfy the predicate.</span></span>

```qsharp
function Count<'T> (predicate : ('T -> Bool), array : 'T[]) : Int
```


## <a name="input"></a><span data-ttu-id="ee14a-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ee14a-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="ee14a-107">предикат: не> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="ee14a-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="ee14a-108">Функция из `'T` в логическое значение, используемое для фильтрации элементов.</span><span class="sxs-lookup"><span data-stu-id="ee14a-108">A function from `'T` to Boolean that is used to filter elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="ee14a-109">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="ee14a-109">array : 'T[]</span></span>

<span data-ttu-id="ee14a-110">Массив элементов `'T` .</span><span class="sxs-lookup"><span data-stu-id="ee14a-110">An array of elements over `'T`.</span></span>



## <a name="output--int"></a><span data-ttu-id="ee14a-111">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ee14a-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ee14a-112">Количество элементов в `array` , которые соответствуют предикату.</span><span class="sxs-lookup"><span data-stu-id="ee14a-112">The number of elements in `array` that satisfy the predicate.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="ee14a-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="ee14a-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ee14a-114">Е</span><span class="sxs-lookup"><span data-stu-id="ee14a-114">'T</span></span>

<span data-ttu-id="ee14a-115">Тип `array` элементов.</span><span class="sxs-lookup"><span data-stu-id="ee14a-115">The type of `array` elements.</span></span>

## <a name="example"></a><span data-ttu-id="ee14a-116">Пример</span><span class="sxs-lookup"><span data-stu-id="ee14a-116">Example</span></span>

<span data-ttu-id="ee14a-117">В следующем коде показана функция "Count".</span><span class="sxs-lookup"><span data-stu-id="ee14a-117">The following code demonstrates the "Count" function.</span></span>
<span data-ttu-id="ee14a-118">Предикат определяется с помощью @"microsoft.quantum.logical.greaterthani" функции:</span><span class="sxs-lookup"><span data-stu-id="ee14a-118">A predicate is defined using the @"microsoft.quantum.logical.greaterthani" function:</span></span>

```qsharp
 let predicate = GreaterThanI(_, 5);
 let count = Count(predicate, [2, 5, 9, 1, 8]);
 // count = 2
```

## <a name="remarks"></a><span data-ttu-id="ee14a-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="ee14a-119">Remarks</span></span>

<span data-ttu-id="ee14a-120">Функция определена для универсальных типов, т. е. при наличии массива `'T[]` и предиката `'T -> Bool` можно фильтровать элементы.</span><span class="sxs-lookup"><span data-stu-id="ee14a-120">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a predicate `'T -> Bool` we can filter elements.</span></span>