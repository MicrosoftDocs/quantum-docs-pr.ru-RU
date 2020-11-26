---
uid: Microsoft.Quantum.Arrays.Where
title: WHERE, функция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Where
qsharp.summary: Given a predicate and an array, returns the indices of that array where the predicate is true.
ms.openlocfilehash: 97598aa25d2d085aaab94f3d60ee64db9e2b89d6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219929"
---
# <a name="where-function"></a><span data-ttu-id="960ca-102">WHERE, функция</span><span class="sxs-lookup"><span data-stu-id="960ca-102">Where function</span></span>

<span data-ttu-id="960ca-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="960ca-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="960ca-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="960ca-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="960ca-105">При наличии предиката и массива возвращает индексы этого массива, где предикат имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="960ca-105">Given a predicate and an array, returns the indices of that array where the predicate is true.</span></span>

```qsharp
function Where<'T> (predicate : ('T -> Bool), array : 'T[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="960ca-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="960ca-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="960ca-107">предикат: не> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="960ca-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="960ca-108">Функция из `'T` в логическое значение, используемое для фильтрации элементов.</span><span class="sxs-lookup"><span data-stu-id="960ca-108">A function from `'T` to Boolean that is used to filter elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="960ca-109">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="960ca-109">array : 'T[]</span></span>

<span data-ttu-id="960ca-110">Массив элементов `'T` .</span><span class="sxs-lookup"><span data-stu-id="960ca-110">An array of elements over `'T`.</span></span>



## <a name="output--int"></a><span data-ttu-id="960ca-111">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="960ca-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="960ca-112">Массив индексов, где `predicate` имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="960ca-112">An array of indices where `predicate` is true.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="960ca-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="960ca-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="960ca-114">Е</span><span class="sxs-lookup"><span data-stu-id="960ca-114">'T</span></span>

<span data-ttu-id="960ca-115">Тип `array` элементов.</span><span class="sxs-lookup"><span data-stu-id="960ca-115">The type of `array` elements.</span></span>