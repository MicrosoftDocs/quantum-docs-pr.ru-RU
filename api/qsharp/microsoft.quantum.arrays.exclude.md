---
uid: Microsoft.Quantum.Arrays.Exclude
title: Функция Exclude
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Exclude
qsharp.summary: Returns an array containing the elements of another array, excluding elements at a given list of indices.
ms.openlocfilehash: 76cdee56e84951c63e80babfdca6a3de33583cab
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848677"
---
# <a name="exclude-function"></a><span data-ttu-id="d8edb-102">Функция Exclude</span><span class="sxs-lookup"><span data-stu-id="d8edb-102">Exclude function</span></span>

<span data-ttu-id="d8edb-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="d8edb-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="d8edb-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d8edb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d8edb-105">Возвращает массив, содержащий элементы другого массива, за исключением элементов в указанном списке индексов.</span><span class="sxs-lookup"><span data-stu-id="d8edb-105">Returns an array containing the elements of another array, excluding elements at a given list of indices.</span></span>

```qsharp
function Exclude<'T> (remove : Int[], array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="d8edb-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d8edb-106">Input</span></span>

### <a name="remove--int"></a><span data-ttu-id="d8edb-107">Remove: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="d8edb-107">remove : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="d8edb-108">Массив индексов, обозначающий, какие элементы следует исключить из выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d8edb-108">An array of indices denoting which elements should be excluded from the output.</span></span>


### <a name="array--t"></a><span data-ttu-id="d8edb-109">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="d8edb-109">array : 'T[]</span></span>

<span data-ttu-id="d8edb-110">Массив, в котором берутся значения в выходном массиве.</span><span class="sxs-lookup"><span data-stu-id="d8edb-110">Array of which the values in the output array are taken.</span></span>



## <a name="output--t"></a><span data-ttu-id="d8edb-111">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="d8edb-111">Output : 'T[]</span></span>

<span data-ttu-id="d8edb-112">Массив, `output` который `output[0]` является первым элементом, `array` индекс которого не отображается в `remove` , например, `output[1]` вторым таким элементом и т. д.</span><span class="sxs-lookup"><span data-stu-id="d8edb-112">An array `output` such that `output[0]` is the first element of `array` whose index does not appear in `remove`, such that `output[1]` is the second such element, and so forth.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="d8edb-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="d8edb-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d8edb-114">Е</span><span class="sxs-lookup"><span data-stu-id="d8edb-114">'T</span></span>

<span data-ttu-id="d8edb-115">Тип элементов массива.</span><span class="sxs-lookup"><span data-stu-id="d8edb-115">The type of the array elements.</span></span>

## <a name="example"></a><span data-ttu-id="d8edb-116">Пример</span><span class="sxs-lookup"><span data-stu-id="d8edb-116">Example</span></span>

```qsharp
let array = [10, 11, 12, 13, 14, 15];
// The following line returns [10, 12, 15].
let subarray = Exclude([1, 3, 4], array);
```