---
uid: Microsoft.Quantum.Arrays.Filtered
title: Отфильтрованная функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Filtered
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, returns an array that consists of those elements that satisfy the predicate.
ms.openlocfilehash: 4c786c69b0896b517f108611e32501867838aeb1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730281"
---
# <a name="filtered-function"></a><span data-ttu-id="81163-102">Отфильтрованная функция</span><span class="sxs-lookup"><span data-stu-id="81163-102">Filtered function</span></span>

<span data-ttu-id="81163-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="81163-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="81163-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="81163-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="81163-105">При наличии массива и предиката, определенного для элементов массива, возвращает массив, состоящий из элементов, которые соответствуют предикату.</span><span class="sxs-lookup"><span data-stu-id="81163-105">Given an array and a predicate that is defined for the elements of the array, returns an array that consists of those elements that satisfy the predicate.</span></span>

```qsharp
function Filtered<'T> (predicate : ('T -> Bool), array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="81163-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="81163-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="81163-107">предикат: не> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="81163-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="81163-108">Функция из `'T` в логическое значение, используемое для фильтрации элементов.</span><span class="sxs-lookup"><span data-stu-id="81163-108">A function from `'T` to Boolean that is used to filter elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="81163-109">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="81163-109">array : 'T[]</span></span>

<span data-ttu-id="81163-110">Массив элементов `'T` .</span><span class="sxs-lookup"><span data-stu-id="81163-110">An array of elements over `'T`.</span></span>



## <a name="output--t"></a><span data-ttu-id="81163-111">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="81163-111">Output : 'T[]</span></span>

<span data-ttu-id="81163-112">Массив `'T[]` элементов, которые соответствуют предикату.</span><span class="sxs-lookup"><span data-stu-id="81163-112">An array `'T[]` of elements that satisfy the predicate.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="81163-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="81163-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="81163-114">Е</span><span class="sxs-lookup"><span data-stu-id="81163-114">'T</span></span>

<span data-ttu-id="81163-115">Тип `array` элементов.</span><span class="sxs-lookup"><span data-stu-id="81163-115">The type of `array` elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="81163-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="81163-116">Remarks</span></span>

<span data-ttu-id="81163-117">Функция определена для универсальных типов, т. е. при наличии массива `'T[]` и предиката `'T -> Bool` можно фильтровать элементы.</span><span class="sxs-lookup"><span data-stu-id="81163-117">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a predicate `'T -> Bool` we can filter elements.</span></span>