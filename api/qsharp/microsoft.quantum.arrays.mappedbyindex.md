---
uid: Microsoft.Quantum.Arrays.MappedByIndex
title: Функция Маппедбиндекс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedByIndex
qsharp.summary: Given an array and a function that is defined for the indexed elements of the array, returns a new array that consists of the images of the original array under the function.
ms.openlocfilehash: 584cabcb7b6059ae5d311f13f5f75bd1f87bdba5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845663"
---
# <a name="mappedbyindex-function"></a><span data-ttu-id="436b0-102">Функция Маппедбиндекс</span><span class="sxs-lookup"><span data-stu-id="436b0-102">MappedByIndex function</span></span>

<span data-ttu-id="436b0-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="436b0-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="436b0-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="436b0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="436b0-105">При наличии массива и функции, определенной для индексированных элементов массива, возвращает новый массив, состоящий из изображений исходного массива в функции.</span><span class="sxs-lookup"><span data-stu-id="436b0-105">Given an array and a function that is defined for the indexed elements of the array, returns a new array that consists of the images of the original array under the function.</span></span>

```qsharp
function MappedByIndex<'T, 'U> (mapper : ((Int, 'T) -> 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a><span data-ttu-id="436b0-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="436b0-106">Input</span></span>

### <a name="mapper--intt---u"></a><span data-ttu-id="436b0-107">сопоставитель: ([int](xref:microsoft.quantum.lang-ref.int), 't) — > ' U</span><span class="sxs-lookup"><span data-stu-id="436b0-107">mapper : ([Int](xref:microsoft.quantum.lang-ref.int),'T) -> 'U</span></span>

<span data-ttu-id="436b0-108">Функция из `(Int, 'T)` в `'U` , используемая для отображения элементов и их индексов.</span><span class="sxs-lookup"><span data-stu-id="436b0-108">A function from `(Int, 'T)` to `'U` that is used to map elements and their indices.</span></span>


### <a name="array--t"></a><span data-ttu-id="436b0-109">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="436b0-109">array : 'T[]</span></span>

<span data-ttu-id="436b0-110">Массив элементов `'T` .</span><span class="sxs-lookup"><span data-stu-id="436b0-110">An array of elements over `'T`.</span></span>



## <a name="output--u"></a><span data-ttu-id="436b0-111">Выходные данные: ' U []</span><span class="sxs-lookup"><span data-stu-id="436b0-111">Output : 'U[]</span></span>

<span data-ttu-id="436b0-112">Массив `'U[]` элементов, сопоставленных с `mapper` функцией.</span><span class="sxs-lookup"><span data-stu-id="436b0-112">An array `'U[]` of elements that are mapped by the `mapper` function.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="436b0-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="436b0-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="436b0-114">Е</span><span class="sxs-lookup"><span data-stu-id="436b0-114">'T</span></span>

<span data-ttu-id="436b0-115">Тип `array` элементов.</span><span class="sxs-lookup"><span data-stu-id="436b0-115">The type of `array` elements.</span></span>
### <a name="u"></a><span data-ttu-id="436b0-116">' U</span><span class="sxs-lookup"><span data-stu-id="436b0-116">'U</span></span>

<span data-ttu-id="436b0-117">Тип результата `mapper` функции.</span><span class="sxs-lookup"><span data-stu-id="436b0-117">The result type of the `mapper` function.</span></span>

## <a name="example"></a><span data-ttu-id="436b0-118">Пример</span><span class="sxs-lookup"><span data-stu-id="436b0-118">Example</span></span>

<span data-ttu-id="436b0-119">Следующие две строки эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="436b0-119">The following two lines are equivalent:</span></span>

```qsharp
let arr = MapIndex(f, [x0, x1, x2]);
```

<span data-ttu-id="436b0-120">и</span><span class="sxs-lookup"><span data-stu-id="436b0-120">and</span></span>

```qsharp
let arr = [f(0, x0), f(1, x1), f(2, x2)];
```

## <a name="see-also"></a><span data-ttu-id="436b0-121">См. также:</span><span class="sxs-lookup"><span data-stu-id="436b0-121">See Also</span></span>

- [<span data-ttu-id="436b0-122">Microsoft. тактов. Arrays. сопоставить</span><span class="sxs-lookup"><span data-stu-id="436b0-122">Microsoft.Quantum.Arrays.Mapped</span></span>](xref:Microsoft.Quantum.Arrays.Mapped)