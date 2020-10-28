---
uid: Microsoft.Quantum.Arrays.MappedByIndex
title: Функция Маппедбиндекс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedByIndex
qsharp.summary: Given an array and a function that is defined for the indexed elements of the array, returns a new array that consists of the images of the original array under the function.
ms.openlocfilehash: 07ca523248c363f2229551a14e77803dc4f4f82e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730137"
---
# <a name="mappedbyindex-function"></a><span data-ttu-id="3badb-102">Функция Маппедбиндекс</span><span class="sxs-lookup"><span data-stu-id="3badb-102">MappedByIndex function</span></span>

<span data-ttu-id="3badb-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="3badb-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="3badb-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3badb-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3badb-105">При наличии массива и функции, определенной для индексированных элементов массива, возвращает новый массив, состоящий из изображений исходного массива в функции.</span><span class="sxs-lookup"><span data-stu-id="3badb-105">Given an array and a function that is defined for the indexed elements of the array, returns a new array that consists of the images of the original array under the function.</span></span>

```qsharp
function MappedByIndex<'T, 'U> (mapper : ((Int, 'T) -> 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a><span data-ttu-id="3badb-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="3badb-106">Input</span></span>

### <a name="mapper--intt---u"></a><span data-ttu-id="3badb-107">сопоставитель: ([int](xref:microsoft.quantum.lang-ref.int), 't) — > ' U</span><span class="sxs-lookup"><span data-stu-id="3badb-107">mapper : ([Int](xref:microsoft.quantum.lang-ref.int),'T) -> 'U</span></span>

<span data-ttu-id="3badb-108">Функция из `(Int, 'T)` в `'U` , используемая для отображения элементов и их индексов.</span><span class="sxs-lookup"><span data-stu-id="3badb-108">A function from `(Int, 'T)` to `'U` that is used to map elements and their indices.</span></span>


### <a name="array--t"></a><span data-ttu-id="3badb-109">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="3badb-109">array : 'T[]</span></span>

<span data-ttu-id="3badb-110">Массив элементов `'T` .</span><span class="sxs-lookup"><span data-stu-id="3badb-110">An array of elements over `'T`.</span></span>



## <a name="output--u"></a><span data-ttu-id="3badb-111">Выходные данные: ' U []</span><span class="sxs-lookup"><span data-stu-id="3badb-111">Output : 'U[]</span></span>

<span data-ttu-id="3badb-112">Массив `'U[]` элементов, сопоставленных с `mapper` функцией.</span><span class="sxs-lookup"><span data-stu-id="3badb-112">An array `'U[]` of elements that are mapped by the `mapper` function.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="3badb-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="3badb-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="3badb-114">Е</span><span class="sxs-lookup"><span data-stu-id="3badb-114">'T</span></span>

<span data-ttu-id="3badb-115">Тип `array` элементов.</span><span class="sxs-lookup"><span data-stu-id="3badb-115">The type of `array` elements.</span></span>
### <a name="u"></a><span data-ttu-id="3badb-116">' U</span><span class="sxs-lookup"><span data-stu-id="3badb-116">'U</span></span>

<span data-ttu-id="3badb-117">Тип результата `mapper` функции.</span><span class="sxs-lookup"><span data-stu-id="3badb-117">The result type of the `mapper` function.</span></span>

## <a name="see-also"></a><span data-ttu-id="3badb-118">См. также:</span><span class="sxs-lookup"><span data-stu-id="3badb-118">See Also</span></span>

- [<span data-ttu-id="3badb-119">Microsoft. тактов. Arrays. сопоставить</span><span class="sxs-lookup"><span data-stu-id="3badb-119">Microsoft.Quantum.Arrays.Mapped</span></span>](xref:Microsoft.Quantum.Arrays.Mapped)