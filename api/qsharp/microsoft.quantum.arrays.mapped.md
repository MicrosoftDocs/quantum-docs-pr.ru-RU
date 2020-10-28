---
uid: Microsoft.Quantum.Arrays.Mapped
title: Сопоставленная функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Mapped
qsharp.summary: Given an array and a function that is defined for the elements of the array, returns a new array that consists of the images of the original array under the function.
ms.openlocfilehash: 1abb9d6fb1a921b49554bef968442f4f2b346b71
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730153"
---
# <a name="mapped-function"></a><span data-ttu-id="45a7e-102">Сопоставленная функция</span><span class="sxs-lookup"><span data-stu-id="45a7e-102">Mapped function</span></span>

<span data-ttu-id="45a7e-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="45a7e-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="45a7e-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="45a7e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="45a7e-105">При наличии массива и функции, определенной для элементов массива, возвращает новый массив, состоящий из изображений исходного массива в функции.</span><span class="sxs-lookup"><span data-stu-id="45a7e-105">Given an array and a function that is defined for the elements of the array, returns a new array that consists of the images of the original array under the function.</span></span>

```qsharp
function Mapped<'T, 'U> (mapper : ('T -> 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a><span data-ttu-id="45a7e-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="45a7e-106">Input</span></span>

### <a name="mapper--t---u"></a><span data-ttu-id="45a7e-107">сопоставитель: не> ' U</span><span class="sxs-lookup"><span data-stu-id="45a7e-107">mapper : 'T -> 'U</span></span>

<span data-ttu-id="45a7e-108">Функция из `'T` в `'U` , используемая для отображения элементов.</span><span class="sxs-lookup"><span data-stu-id="45a7e-108">A function from `'T` to `'U` that is used to map elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="45a7e-109">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="45a7e-109">array : 'T[]</span></span>

<span data-ttu-id="45a7e-110">Массив элементов `'T` .</span><span class="sxs-lookup"><span data-stu-id="45a7e-110">An array of elements over `'T`.</span></span>



## <a name="output--u"></a><span data-ttu-id="45a7e-111">Выходные данные: ' U []</span><span class="sxs-lookup"><span data-stu-id="45a7e-111">Output : 'U[]</span></span>

<span data-ttu-id="45a7e-112">Массив `'U[]` элементов, сопоставленных с `mapper` функцией.</span><span class="sxs-lookup"><span data-stu-id="45a7e-112">An array `'U[]` of elements that are mapped by the `mapper` function.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="45a7e-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="45a7e-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="45a7e-114">Е</span><span class="sxs-lookup"><span data-stu-id="45a7e-114">'T</span></span>

<span data-ttu-id="45a7e-115">Тип `array` элементов.</span><span class="sxs-lookup"><span data-stu-id="45a7e-115">The type of `array` elements.</span></span>
### <a name="u"></a><span data-ttu-id="45a7e-116">' U</span><span class="sxs-lookup"><span data-stu-id="45a7e-116">'U</span></span>

<span data-ttu-id="45a7e-117">Тип результата `mapper` функции.</span><span class="sxs-lookup"><span data-stu-id="45a7e-117">The result type of the `mapper` function.</span></span>

## <a name="remarks"></a><span data-ttu-id="45a7e-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="45a7e-118">Remarks</span></span>

<span data-ttu-id="45a7e-119">Функция определена для универсальных типов, т. е. при наличии массива `'T[]` и функции `mapper: 'T -> 'U` мы можем сопоставлять элементы массива и создавать новый массив типа `'U[]` .</span><span class="sxs-lookup"><span data-stu-id="45a7e-119">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a function `mapper: 'T -> 'U` we can map the elements of the array and produce a new array of type `'U[]`.</span></span>