---
uid: Microsoft.Quantum.Arrays.IndexRange
title: Функция Индексранже
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexRange
qsharp.summary: Given an array, returns a range over the indices of that array, suitable for use in a for loop.
ms.openlocfilehash: 7f9779acd4a781c50388217aa780710bd0b99ff3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730201"
---
# <a name="indexrange-function"></a><span data-ttu-id="42022-102">Функция Индексранже</span><span class="sxs-lookup"><span data-stu-id="42022-102">IndexRange function</span></span>

<span data-ttu-id="42022-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="42022-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="42022-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="42022-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="42022-105">При наличии массива возвращает диапазон по индексам этого массива, который подходит для использования в цикле for.</span><span class="sxs-lookup"><span data-stu-id="42022-105">Given an array, returns a range over the indices of that array, suitable for use in a for loop.</span></span>

```qsharp
function IndexRange<'TElement> (array : 'TElement[]) : Range
```


## <a name="input"></a><span data-ttu-id="42022-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="42022-106">Input</span></span>

### <a name="array--telement"></a><span data-ttu-id="42022-107">массив: ' TElement []</span><span class="sxs-lookup"><span data-stu-id="42022-107">array : 'TElement[]</span></span>

<span data-ttu-id="42022-108">Массив, для которого должен быть возвращен диапазон индексов.</span><span class="sxs-lookup"><span data-stu-id="42022-108">An array for which a range of indices should be returned.</span></span>



## <a name="output--range"></a><span data-ttu-id="42022-109">Выходные данные: [диапазон](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="42022-109">Output : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="42022-110">Диапазон для всех индексов массива.</span><span class="sxs-lookup"><span data-stu-id="42022-110">A range over all indices of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="42022-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="42022-111">Type Parameters</span></span>

### <a name="telement"></a><span data-ttu-id="42022-112">' TElement</span><span class="sxs-lookup"><span data-stu-id="42022-112">'TElement</span></span>

<span data-ttu-id="42022-113">Тип элементов массива.</span><span class="sxs-lookup"><span data-stu-id="42022-113">The type of elements of the array.</span></span>