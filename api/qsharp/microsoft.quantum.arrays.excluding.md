---
uid: Microsoft.Quantum.Arrays.Excluding
title: Исключение функции
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Excluding
qsharp.summary: Returns an array containing the elements of another array, excluding elements at a given list of indices.
ms.openlocfilehash: 6585e619834a96953c9eae2d36a8ebe0a11dbda0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221323"
---
# <a name="excluding-function"></a><span data-ttu-id="a35dc-102">Исключение функции</span><span class="sxs-lookup"><span data-stu-id="a35dc-102">Excluding function</span></span>

<span data-ttu-id="a35dc-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="a35dc-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="a35dc-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a35dc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a35dc-105">Возвращает массив, содержащий элементы другого массива, за исключением элементов в указанном списке индексов.</span><span class="sxs-lookup"><span data-stu-id="a35dc-105">Returns an array containing the elements of another array, excluding elements at a given list of indices.</span></span>

```qsharp
function Excluding<'T> (remove : Int[], array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="a35dc-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a35dc-106">Input</span></span>

### <a name="remove--int"></a><span data-ttu-id="a35dc-107">Remove: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="a35dc-107">remove : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="a35dc-108">Массив индексов, обозначающий, какие элементы следует исключить из выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a35dc-108">An array of indices denoting which elements should be excluded from the output.</span></span>


### <a name="array--t"></a><span data-ttu-id="a35dc-109">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="a35dc-109">array : 'T[]</span></span>

<span data-ttu-id="a35dc-110">Массив, в котором берутся значения в выходном массиве.</span><span class="sxs-lookup"><span data-stu-id="a35dc-110">Array of which the values in the output array are taken.</span></span>



## <a name="output--t"></a><span data-ttu-id="a35dc-111">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="a35dc-111">Output : 'T[]</span></span>

<span data-ttu-id="a35dc-112">Массив, `output` который `output[0]` является первым элементом, `array` индекс которого не отображается в `remove` , например, `output[1]` вторым таким элементом и т. д.</span><span class="sxs-lookup"><span data-stu-id="a35dc-112">An array `output` such that `output[0]` is the first element of `array` whose index does not appear in `remove`, such that `output[1]` is the second such element, and so forth.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a35dc-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="a35dc-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a35dc-114">Е</span><span class="sxs-lookup"><span data-stu-id="a35dc-114">'T</span></span>

<span data-ttu-id="a35dc-115">Тип элементов массива.</span><span class="sxs-lookup"><span data-stu-id="a35dc-115">The type of the array elements.</span></span>