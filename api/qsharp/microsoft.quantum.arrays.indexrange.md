---
uid: Microsoft.Quantum.Arrays.IndexRange
title: Функция Индексранже
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexRange
qsharp.summary: Given an array, returns a range over the indices of that array, suitable for use in a for loop.
ms.openlocfilehash: 5afd4cc260ac3e384d2736bf7b43d941afd9ef73
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220949"
---
# <a name="indexrange-function"></a><span data-ttu-id="ace04-102">Функция Индексранже</span><span class="sxs-lookup"><span data-stu-id="ace04-102">IndexRange function</span></span>

<span data-ttu-id="ace04-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="ace04-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="ace04-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="ace04-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="ace04-105">При наличии массива возвращает диапазон по индексам этого массива, который подходит для использования в цикле for.</span><span class="sxs-lookup"><span data-stu-id="ace04-105">Given an array, returns a range over the indices of that array, suitable for use in a for loop.</span></span>

```qsharp
function IndexRange<'TElement> (array : 'TElement[]) : Range
```


## <a name="input"></a><span data-ttu-id="ace04-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ace04-106">Input</span></span>

### <a name="array--telement"></a><span data-ttu-id="ace04-107">массив: ' TElement []</span><span class="sxs-lookup"><span data-stu-id="ace04-107">array : 'TElement[]</span></span>

<span data-ttu-id="ace04-108">Массив, для которого должен быть возвращен диапазон индексов.</span><span class="sxs-lookup"><span data-stu-id="ace04-108">An array for which a range of indices should be returned.</span></span>



## <a name="output--range"></a><span data-ttu-id="ace04-109">Выходные данные: [диапазон](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="ace04-109">Output : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="ace04-110">Диапазон для всех индексов массива.</span><span class="sxs-lookup"><span data-stu-id="ace04-110">A range over all indices of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="ace04-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="ace04-111">Type Parameters</span></span>

### <a name="telement"></a><span data-ttu-id="ace04-112">' TElement</span><span class="sxs-lookup"><span data-stu-id="ace04-112">'TElement</span></span>

<span data-ttu-id="ace04-113">Тип элементов массива.</span><span class="sxs-lookup"><span data-stu-id="ace04-113">The type of elements of the array.</span></span>