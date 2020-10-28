---
uid: Microsoft.Quantum.Arrays.Exclude
title: Функция Exclude
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Exclude
qsharp.summary: Returns an array containing the elements of another array, excluding elements at a given list of indices.
ms.openlocfilehash: e1fa7e728d4846db90872055454a8182a77a518b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730289"
---
# <a name="exclude-function"></a><span data-ttu-id="58655-102">Функция Exclude</span><span class="sxs-lookup"><span data-stu-id="58655-102">Exclude function</span></span>

<span data-ttu-id="58655-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="58655-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="58655-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="58655-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="58655-105">Возвращает массив, содержащий элементы другого массива, за исключением элементов в указанном списке индексов.</span><span class="sxs-lookup"><span data-stu-id="58655-105">Returns an array containing the elements of another array, excluding elements at a given list of indices.</span></span>

```qsharp
function Exclude<'T> (remove : Int[], array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="58655-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="58655-106">Input</span></span>

### <a name="remove--int"></a><span data-ttu-id="58655-107">Remove: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="58655-107">remove : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="58655-108">Массив индексов, обозначающий, какие элементы следует исключить из выходных данных.</span><span class="sxs-lookup"><span data-stu-id="58655-108">An array of indices denoting which elements should be excluded from the output.</span></span>


### <a name="array--t"></a><span data-ttu-id="58655-109">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="58655-109">array : 'T[]</span></span>

<span data-ttu-id="58655-110">Массив, в котором берутся значения в выходном массиве.</span><span class="sxs-lookup"><span data-stu-id="58655-110">Array of which the values in the output array are taken.</span></span>



## <a name="output--t"></a><span data-ttu-id="58655-111">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="58655-111">Output : 'T[]</span></span>

<span data-ttu-id="58655-112">Массив, `output` который `output[0]` является первым элементом, `array` индекс которого не отображается в `remove` , например, `output[1]` вторым таким элементом и т. д.</span><span class="sxs-lookup"><span data-stu-id="58655-112">An array `output` such that `output[0]` is the first element of `array` whose index does not appear in `remove`, such that `output[1]` is the second such element, and so forth.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="58655-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="58655-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="58655-114">Е</span><span class="sxs-lookup"><span data-stu-id="58655-114">'T</span></span>

<span data-ttu-id="58655-115">Тип элементов массива.</span><span class="sxs-lookup"><span data-stu-id="58655-115">The type of the array elements.</span></span>