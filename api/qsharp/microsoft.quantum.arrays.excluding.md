---
uid: Microsoft.Quantum.Arrays.Excluding
title: Исключение функции
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Excluding
qsharp.summary: Returns an array containing the elements of another array, excluding elements at a given list of indices.
ms.openlocfilehash: 8848c6e89da50efb4f7550168f1757b25a214a24
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730288"
---
# <a name="excluding-function"></a><span data-ttu-id="6b2c1-102">Исключение функции</span><span class="sxs-lookup"><span data-stu-id="6b2c1-102">Excluding function</span></span>

<span data-ttu-id="6b2c1-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="6b2c1-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="6b2c1-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6b2c1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6b2c1-105">Возвращает массив, содержащий элементы другого массива, за исключением элементов в указанном списке индексов.</span><span class="sxs-lookup"><span data-stu-id="6b2c1-105">Returns an array containing the elements of another array, excluding elements at a given list of indices.</span></span>

```qsharp
function Excluding<'T> (remove : Int[], array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="6b2c1-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="6b2c1-106">Input</span></span>

### <a name="remove--int"></a><span data-ttu-id="6b2c1-107">Remove: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="6b2c1-107">remove : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="6b2c1-108">Массив индексов, обозначающий, какие элементы следует исключить из выходных данных.</span><span class="sxs-lookup"><span data-stu-id="6b2c1-108">An array of indices denoting which elements should be excluded from the output.</span></span>


### <a name="array--t"></a><span data-ttu-id="6b2c1-109">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="6b2c1-109">array : 'T[]</span></span>

<span data-ttu-id="6b2c1-110">Массив, в котором берутся значения в выходном массиве.</span><span class="sxs-lookup"><span data-stu-id="6b2c1-110">Array of which the values in the output array are taken.</span></span>



## <a name="output--t"></a><span data-ttu-id="6b2c1-111">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="6b2c1-111">Output : 'T[]</span></span>

<span data-ttu-id="6b2c1-112">Массив, `output` который `output[0]` является первым элементом, `array` индекс которого не отображается в `remove` , например, `output[1]` вторым таким элементом и т. д.</span><span class="sxs-lookup"><span data-stu-id="6b2c1-112">An array `output` such that `output[0]` is the first element of `array` whose index does not appear in `remove`, such that `output[1]` is the second such element, and so forth.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="6b2c1-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="6b2c1-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6b2c1-114">Е</span><span class="sxs-lookup"><span data-stu-id="6b2c1-114">'T</span></span>

<span data-ttu-id="6b2c1-115">Тип элементов массива.</span><span class="sxs-lookup"><span data-stu-id="6b2c1-115">The type of the array elements.</span></span>