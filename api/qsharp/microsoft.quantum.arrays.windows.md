---
uid: Microsoft.Quantum.Arrays.Windows
title: Функция Windows
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Windows
qsharp.summary: Returns all consecutive subarrays of length `size`.
ms.openlocfilehash: adfea2b9a2f6c22446817538d29586284dba723e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842196"
---
# <a name="windows-function"></a><span data-ttu-id="26167-102">Функция Windows</span><span class="sxs-lookup"><span data-stu-id="26167-102">Windows function</span></span>

<span data-ttu-id="26167-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="26167-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="26167-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="26167-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="26167-105">Возвращает все последовательные подмассивы длины `size` .</span><span class="sxs-lookup"><span data-stu-id="26167-105">Returns all consecutive subarrays of length `size`.</span></span>

```qsharp
function Windows<'T> (size : Int, array : 'T[]) : 'T[][]
```


## <a name="description"></a><span data-ttu-id="26167-106">Описание</span><span class="sxs-lookup"><span data-stu-id="26167-106">Description</span></span>

<span data-ttu-id="26167-107">Эта функция возвращает все `n - size + 1` подмассивы длины `size` в порядке, где `n` — это длина `arr` .</span><span class="sxs-lookup"><span data-stu-id="26167-107">This function returns all `n - size + 1` subarrays of length `size` in order, where `n` is the length of `arr`.</span></span>
<span data-ttu-id="26167-108">Первые подмассивы находятся `arr[0..size - 1], arr[1..size], arr[2..size + 1]` до последнего подмассива `arr[n - size..n - 1]` .</span><span class="sxs-lookup"><span data-stu-id="26167-108">The first subarrays are `arr[0..size - 1], arr[1..size], arr[2..size + 1]` until the last subarray `arr[n - size..n - 1]`.</span></span>

<span data-ttu-id="26167-109">Если `size <= 0` или `size > n` , возвращается пустой массив.</span><span class="sxs-lookup"><span data-stu-id="26167-109">If `size <= 0` or `size > n`, an empty array is returned.</span></span>

## <a name="input"></a><span data-ttu-id="26167-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="26167-110">Input</span></span>

### <a name="size--int"></a><span data-ttu-id="26167-111">Размер: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="26167-111">size : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="26167-112">Длина подмассивов.</span><span class="sxs-lookup"><span data-stu-id="26167-112">Length of the subarrays.</span></span>


### <a name="array--t"></a><span data-ttu-id="26167-113">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="26167-113">array : 'T[]</span></span>

<span data-ttu-id="26167-114">Массив элементов.</span><span class="sxs-lookup"><span data-stu-id="26167-114">An array of elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="26167-115">Выходные данные: 'T [] []</span><span class="sxs-lookup"><span data-stu-id="26167-115">Output : 'T[][]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="26167-116">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="26167-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="26167-117">Е</span><span class="sxs-lookup"><span data-stu-id="26167-117">'T</span></span>

<span data-ttu-id="26167-118">Тип `array` элементов.</span><span class="sxs-lookup"><span data-stu-id="26167-118">The type of `array` elements.</span></span>

## <a name="example"></a><span data-ttu-id="26167-119">Пример</span><span class="sxs-lookup"><span data-stu-id="26167-119">Example</span></span>

```qsharp
// same as [[1, 2, 3], [2, 3, 4], [3, 4, 5]]
let windows = Windows(3, [1, 2, 3, 4, 5]);
```