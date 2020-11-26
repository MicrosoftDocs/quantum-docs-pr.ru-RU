---
uid: Microsoft.Quantum.Arrays.Exclude
title: Функция Exclude
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Exclude
qsharp.summary: Returns an array containing the elements of another array, excluding elements at a given list of indices.
ms.openlocfilehash: 4ea0d754fce4fc7e3e4e42e55b56720cb3f95ca6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221357"
---
# <a name="exclude-function"></a><span data-ttu-id="3f5e3-102">Функция Exclude</span><span class="sxs-lookup"><span data-stu-id="3f5e3-102">Exclude function</span></span>

<span data-ttu-id="3f5e3-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="3f5e3-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="3f5e3-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3f5e3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3f5e3-105">Возвращает массив, содержащий элементы другого массива, за исключением элементов в указанном списке индексов.</span><span class="sxs-lookup"><span data-stu-id="3f5e3-105">Returns an array containing the elements of another array, excluding elements at a given list of indices.</span></span>

```qsharp
function Exclude<'T> (remove : Int[], array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="3f5e3-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="3f5e3-106">Input</span></span>

### <a name="remove--int"></a><span data-ttu-id="3f5e3-107">Remove: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="3f5e3-107">remove : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="3f5e3-108">Массив индексов, обозначающий, какие элементы следует исключить из выходных данных.</span><span class="sxs-lookup"><span data-stu-id="3f5e3-108">An array of indices denoting which elements should be excluded from the output.</span></span>


### <a name="array--t"></a><span data-ttu-id="3f5e3-109">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="3f5e3-109">array : 'T[]</span></span>

<span data-ttu-id="3f5e3-110">Массив, в котором берутся значения в выходном массиве.</span><span class="sxs-lookup"><span data-stu-id="3f5e3-110">Array of which the values in the output array are taken.</span></span>



## <a name="output--t"></a><span data-ttu-id="3f5e3-111">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="3f5e3-111">Output : 'T[]</span></span>

<span data-ttu-id="3f5e3-112">Массив, `output` который `output[0]` является первым элементом, `array` индекс которого не отображается в `remove` , например, `output[1]` вторым таким элементом и т. д.</span><span class="sxs-lookup"><span data-stu-id="3f5e3-112">An array `output` such that `output[0]` is the first element of `array` whose index does not appear in `remove`, such that `output[1]` is the second such element, and so forth.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="3f5e3-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="3f5e3-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="3f5e3-114">Е</span><span class="sxs-lookup"><span data-stu-id="3f5e3-114">'T</span></span>

<span data-ttu-id="3f5e3-115">Тип элементов массива.</span><span class="sxs-lookup"><span data-stu-id="3f5e3-115">The type of the array elements.</span></span>