---
uid: Microsoft.Quantum.Arrays.Count
title: Count, функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Count
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, returns the number of elements an array that consists of those elements that satisfy the predicate.
ms.openlocfilehash: 408a4a42dda6a4827db6d5865e2b4b8a8df5b37a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730369"
---
# <a name="count-function"></a><span data-ttu-id="df421-102">Count, функция</span><span class="sxs-lookup"><span data-stu-id="df421-102">Count function</span></span>

<span data-ttu-id="df421-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="df421-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="df421-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="df421-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="df421-105">При наличии массива и предиката, определенного для элементов массива, возвращает число элементов массива, состоящего из элементов, которые соответствуют предикату.</span><span class="sxs-lookup"><span data-stu-id="df421-105">Given an array and a predicate that is defined for the elements of the array, returns the number of elements an array that consists of those elements that satisfy the predicate.</span></span>

```qsharp
function Count<'T> (predicate : ('T -> Bool), array : 'T[]) : Int
```


## <a name="input"></a><span data-ttu-id="df421-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="df421-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="df421-107">предикат: не> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="df421-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="df421-108">Функция из `'T` в логическое значение, используемое для фильтрации элементов.</span><span class="sxs-lookup"><span data-stu-id="df421-108">A function from `'T` to Boolean that is used to filter elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="df421-109">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="df421-109">array : 'T[]</span></span>

<span data-ttu-id="df421-110">Массив элементов `'T` .</span><span class="sxs-lookup"><span data-stu-id="df421-110">An array of elements over `'T`.</span></span>



## <a name="output--int"></a><span data-ttu-id="df421-111">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="df421-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="df421-112">Количество элементов в `array` , которые соответствуют предикату.</span><span class="sxs-lookup"><span data-stu-id="df421-112">The number of elements in `array` that satisfy the predicate.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="df421-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="df421-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="df421-114">Е</span><span class="sxs-lookup"><span data-stu-id="df421-114">'T</span></span>

<span data-ttu-id="df421-115">Тип `array` элементов.</span><span class="sxs-lookup"><span data-stu-id="df421-115">The type of `array` elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="df421-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="df421-116">Remarks</span></span>

<span data-ttu-id="df421-117">Функция определена для универсальных типов, т. е. при наличии массива `'T[]` и предиката `'T -> Bool` можно фильтровать элементы.</span><span class="sxs-lookup"><span data-stu-id="df421-117">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a predicate `'T -> Bool` we can filter elements.</span></span>