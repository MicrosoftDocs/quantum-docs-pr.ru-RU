---
uid: Microsoft.Quantum.Arrays.Windows
title: Функция Windows
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Windows
qsharp.summary: Returns all consecutive subarrays of length `size`.
ms.openlocfilehash: 6071d1c3e5981855c57abd0e741b1de0201c30a3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729936"
---
# <a name="windows-function"></a><span data-ttu-id="5eabe-102">Функция Windows</span><span class="sxs-lookup"><span data-stu-id="5eabe-102">Windows function</span></span>

<span data-ttu-id="5eabe-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="5eabe-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="5eabe-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5eabe-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5eabe-105">Возвращает все последовательные подмассивы длины `size` .</span><span class="sxs-lookup"><span data-stu-id="5eabe-105">Returns all consecutive subarrays of length `size`.</span></span>

```qsharp
function Windows<'T> (size : Int, array : 'T[]) : 'T[][]
```


## <a name="description"></a><span data-ttu-id="5eabe-106">Описание</span><span class="sxs-lookup"><span data-stu-id="5eabe-106">Description</span></span>

<span data-ttu-id="5eabe-107">Эта функция возвращает все `n - size + 1` подмассивы длины `size` в порядке, где `n` — это длина `arr` .</span><span class="sxs-lookup"><span data-stu-id="5eabe-107">This function returns all `n - size + 1` subarrays of length `size` in order, where `n` is the length of `arr`.</span></span>
<span data-ttu-id="5eabe-108">Первые подмассивы находятся `arr[0..size - 1], arr[1..size], arr[2..size + 1]` до последнего подмассива `arr[n - size..n - 1]` .</span><span class="sxs-lookup"><span data-stu-id="5eabe-108">The first subarrays are `arr[0..size - 1], arr[1..size], arr[2..size + 1]` until the last subarray `arr[n - size..n - 1]`.</span></span>

<span data-ttu-id="5eabe-109">Если `size <= 0` или `size > n` , возвращается пустой массив.</span><span class="sxs-lookup"><span data-stu-id="5eabe-109">If `size <= 0` or `size > n`, an empty array is returned.</span></span>

## <a name="input"></a><span data-ttu-id="5eabe-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5eabe-110">Input</span></span>

### <a name="size--int"></a><span data-ttu-id="5eabe-111">Размер: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5eabe-111">size : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5eabe-112">Длина подмассивов.</span><span class="sxs-lookup"><span data-stu-id="5eabe-112">Length of the subarrays.</span></span>


### <a name="array--t"></a><span data-ttu-id="5eabe-113">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="5eabe-113">array : 'T[]</span></span>

<span data-ttu-id="5eabe-114">Массив элементов.</span><span class="sxs-lookup"><span data-stu-id="5eabe-114">An array of elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="5eabe-115">Выходные данные: 'T [] []</span><span class="sxs-lookup"><span data-stu-id="5eabe-115">Output : 'T[][]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="5eabe-116">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="5eabe-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5eabe-117">Е</span><span class="sxs-lookup"><span data-stu-id="5eabe-117">'T</span></span>

<span data-ttu-id="5eabe-118">Тип `array` элементов.</span><span class="sxs-lookup"><span data-stu-id="5eabe-118">The type of `array` elements.</span></span>