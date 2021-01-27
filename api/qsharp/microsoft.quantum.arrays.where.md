---
uid: Microsoft.Quantum.Arrays.Where
title: WHERE, функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Where
qsharp.summary: Given a predicate and an array, returns the indices of that array where the predicate is true.
ms.openlocfilehash: 4a938114689177f7a9ee182e6e5f36debe4edac7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842223"
---
# <a name="where-function"></a><span data-ttu-id="2dbde-102">WHERE, функция</span><span class="sxs-lookup"><span data-stu-id="2dbde-102">Where function</span></span>

<span data-ttu-id="2dbde-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="2dbde-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="2dbde-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2dbde-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2dbde-105">При наличии предиката и массива возвращает индексы этого массива, где предикат имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="2dbde-105">Given a predicate and an array, returns the indices of that array where the predicate is true.</span></span>

```qsharp
function Where<'T> (predicate : ('T -> Bool), array : 'T[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="2dbde-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2dbde-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="2dbde-107">предикат: не> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="2dbde-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="2dbde-108">Функция из `'T` в логическое значение, используемое для фильтрации элементов.</span><span class="sxs-lookup"><span data-stu-id="2dbde-108">A function from `'T` to Boolean that is used to filter elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="2dbde-109">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="2dbde-109">array : 'T[]</span></span>

<span data-ttu-id="2dbde-110">Массив элементов `'T` .</span><span class="sxs-lookup"><span data-stu-id="2dbde-110">An array of elements over `'T`.</span></span>



## <a name="output--int"></a><span data-ttu-id="2dbde-111">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="2dbde-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="2dbde-112">Массив индексов, где `predicate` имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="2dbde-112">An array of indices where `predicate` is true.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="2dbde-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="2dbde-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2dbde-114">Е</span><span class="sxs-lookup"><span data-stu-id="2dbde-114">'T</span></span>

<span data-ttu-id="2dbde-115">Тип `array` элементов.</span><span class="sxs-lookup"><span data-stu-id="2dbde-115">The type of `array` elements.</span></span>