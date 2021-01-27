---
uid: Microsoft.Quantum.Arrays.IndexRange
title: Функция Индексранже
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexRange
qsharp.summary: Given an array, returns a range over the indices of that array, suitable for use in a for loop.
ms.openlocfilehash: 043b56a1ac3cbe5cd59cdd45d3725f301d81a6ee
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845779"
---
# <a name="indexrange-function"></a><span data-ttu-id="0c966-102">Функция Индексранже</span><span class="sxs-lookup"><span data-stu-id="0c966-102">IndexRange function</span></span>

<span data-ttu-id="0c966-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="0c966-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="0c966-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="0c966-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="0c966-105">При наличии массива возвращает диапазон по индексам этого массива, который подходит для использования в цикле for.</span><span class="sxs-lookup"><span data-stu-id="0c966-105">Given an array, returns a range over the indices of that array, suitable for use in a for loop.</span></span>

```qsharp
function IndexRange<'TElement> (array : 'TElement[]) : Range
```


## <a name="input"></a><span data-ttu-id="0c966-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="0c966-106">Input</span></span>

### <a name="array--telement"></a><span data-ttu-id="0c966-107">массив: ' TElement []</span><span class="sxs-lookup"><span data-stu-id="0c966-107">array : 'TElement[]</span></span>

<span data-ttu-id="0c966-108">Массив, для которого должен быть возвращен диапазон индексов.</span><span class="sxs-lookup"><span data-stu-id="0c966-108">An array for which a range of indices should be returned.</span></span>



## <a name="output--range"></a><span data-ttu-id="0c966-109">Выходные данные: [диапазон](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="0c966-109">Output : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="0c966-110">Диапазон для всех индексов массива.</span><span class="sxs-lookup"><span data-stu-id="0c966-110">A range over all indices of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="0c966-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="0c966-111">Type Parameters</span></span>

### <a name="telement"></a><span data-ttu-id="0c966-112">' TElement</span><span class="sxs-lookup"><span data-stu-id="0c966-112">'TElement</span></span>

<span data-ttu-id="0c966-113">Тип элементов массива.</span><span class="sxs-lookup"><span data-stu-id="0c966-113">The type of elements of the array.</span></span>

## <a name="example"></a><span data-ttu-id="0c966-114">Пример</span><span class="sxs-lookup"><span data-stu-id="0c966-114">Example</span></span>

<span data-ttu-id="0c966-115">Следующие `for` циклы эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="0c966-115">The following `for` loops are equivalent:</span></span>

```qsharp
for (idx in IndexRange(array)) { ... }
for (idx in IndexRange(array)) { ... }
```