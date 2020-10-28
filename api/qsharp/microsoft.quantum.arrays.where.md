---
uid: Microsoft.Quantum.Arrays.Where
title: WHERE, функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Where
qsharp.summary: Given a predicate and an array, returns the indices of that array where the predicate is true.
ms.openlocfilehash: 1c9fa0463ed49788d12502257d735b965565d1ab
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729937"
---
# <a name="where-function"></a><span data-ttu-id="67c38-102">WHERE, функция</span><span class="sxs-lookup"><span data-stu-id="67c38-102">Where function</span></span>

<span data-ttu-id="67c38-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="67c38-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="67c38-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="67c38-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="67c38-105">При наличии предиката и массива возвращает индексы этого массива, где предикат имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="67c38-105">Given a predicate and an array, returns the indices of that array where the predicate is true.</span></span>

```qsharp
function Where<'T> (predicate : ('T -> Bool), array : 'T[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="67c38-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="67c38-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="67c38-107">предикат: не> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="67c38-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="67c38-108">Функция из `'T` в логическое значение, используемое для фильтрации элементов.</span><span class="sxs-lookup"><span data-stu-id="67c38-108">A function from `'T` to Boolean that is used to filter elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="67c38-109">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="67c38-109">array : 'T[]</span></span>

<span data-ttu-id="67c38-110">Массив элементов `'T` .</span><span class="sxs-lookup"><span data-stu-id="67c38-110">An array of elements over `'T`.</span></span>



## <a name="output--int"></a><span data-ttu-id="67c38-111">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="67c38-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="67c38-112">Массив индексов, где `predicate` имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="67c38-112">An array of indices where `predicate` is true.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="67c38-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="67c38-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="67c38-114">Е</span><span class="sxs-lookup"><span data-stu-id="67c38-114">'T</span></span>

<span data-ttu-id="67c38-115">Тип `array` элементов.</span><span class="sxs-lookup"><span data-stu-id="67c38-115">The type of `array` elements.</span></span>