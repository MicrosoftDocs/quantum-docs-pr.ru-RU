---
uid: Microsoft.Quantum.Arrays.Filtered
title: Отфильтрованная функция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Filtered
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, returns an array that consists of those elements that satisfy the predicate.
ms.openlocfilehash: fa8600f4d773daf6eabf8b9961ab46961155d1fd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221272"
---
# <a name="filtered-function"></a><span data-ttu-id="2c024-102">Отфильтрованная функция</span><span class="sxs-lookup"><span data-stu-id="2c024-102">Filtered function</span></span>

<span data-ttu-id="2c024-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="2c024-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="2c024-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2c024-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2c024-105">При наличии массива и предиката, определенного для элементов массива, возвращает массив, состоящий из элементов, которые соответствуют предикату.</span><span class="sxs-lookup"><span data-stu-id="2c024-105">Given an array and a predicate that is defined for the elements of the array, returns an array that consists of those elements that satisfy the predicate.</span></span>

```qsharp
function Filtered<'T> (predicate : ('T -> Bool), array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="2c024-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2c024-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="2c024-107">предикат: не> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="2c024-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="2c024-108">Функция из `'T` в логическое значение, используемое для фильтрации элементов.</span><span class="sxs-lookup"><span data-stu-id="2c024-108">A function from `'T` to Boolean that is used to filter elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="2c024-109">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="2c024-109">array : 'T[]</span></span>

<span data-ttu-id="2c024-110">Массив элементов `'T` .</span><span class="sxs-lookup"><span data-stu-id="2c024-110">An array of elements over `'T`.</span></span>



## <a name="output--t"></a><span data-ttu-id="2c024-111">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="2c024-111">Output : 'T[]</span></span>

<span data-ttu-id="2c024-112">Массив `'T[]` элементов, которые соответствуют предикату.</span><span class="sxs-lookup"><span data-stu-id="2c024-112">An array `'T[]` of elements that satisfy the predicate.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="2c024-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="2c024-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2c024-114">Е</span><span class="sxs-lookup"><span data-stu-id="2c024-114">'T</span></span>

<span data-ttu-id="2c024-115">Тип `array` элементов.</span><span class="sxs-lookup"><span data-stu-id="2c024-115">The type of `array` elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c024-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2c024-116">Remarks</span></span>

<span data-ttu-id="2c024-117">Функция определена для универсальных типов, т. е. при наличии массива `'T[]` и предиката `'T -> Bool` можно фильтровать элементы.</span><span class="sxs-lookup"><span data-stu-id="2c024-117">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a predicate `'T -> Bool` we can filter elements.</span></span>