---
uid: Microsoft.Quantum.Arrays.Windows
title: Функция Windows
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Windows
qsharp.summary: Returns all consecutive subarrays of length `size`.
ms.openlocfilehash: 8f32a23aa4379744b84c3b8d9c8f565e61c3c64e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219895"
---
# <a name="windows-function"></a><span data-ttu-id="761a4-102">Функция Windows</span><span class="sxs-lookup"><span data-stu-id="761a4-102">Windows function</span></span>

<span data-ttu-id="761a4-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="761a4-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="761a4-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="761a4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="761a4-105">Возвращает все последовательные подмассивы длины `size` .</span><span class="sxs-lookup"><span data-stu-id="761a4-105">Returns all consecutive subarrays of length `size`.</span></span>

```qsharp
function Windows<'T> (size : Int, array : 'T[]) : 'T[][]
```


## <a name="description"></a><span data-ttu-id="761a4-106">Описание</span><span class="sxs-lookup"><span data-stu-id="761a4-106">Description</span></span>

<span data-ttu-id="761a4-107">Эта функция возвращает все `n - size + 1` подмассивы длины `size` в порядке, где `n` — это длина `arr` .</span><span class="sxs-lookup"><span data-stu-id="761a4-107">This function returns all `n - size + 1` subarrays of length `size` in order, where `n` is the length of `arr`.</span></span>
<span data-ttu-id="761a4-108">Первые подмассивы находятся `arr[0..size - 1], arr[1..size], arr[2..size + 1]` до последнего подмассива `arr[n - size..n - 1]` .</span><span class="sxs-lookup"><span data-stu-id="761a4-108">The first subarrays are `arr[0..size - 1], arr[1..size], arr[2..size + 1]` until the last subarray `arr[n - size..n - 1]`.</span></span>

<span data-ttu-id="761a4-109">Если `size <= 0` или `size > n` , возвращается пустой массив.</span><span class="sxs-lookup"><span data-stu-id="761a4-109">If `size <= 0` or `size > n`, an empty array is returned.</span></span>

## <a name="input"></a><span data-ttu-id="761a4-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="761a4-110">Input</span></span>

### <a name="size--int"></a><span data-ttu-id="761a4-111">Размер: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="761a4-111">size : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="761a4-112">Длина подмассивов.</span><span class="sxs-lookup"><span data-stu-id="761a4-112">Length of the subarrays.</span></span>


### <a name="array--t"></a><span data-ttu-id="761a4-113">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="761a4-113">array : 'T[]</span></span>

<span data-ttu-id="761a4-114">Массив элементов.</span><span class="sxs-lookup"><span data-stu-id="761a4-114">An array of elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="761a4-115">Выходные данные: 'T [] []</span><span class="sxs-lookup"><span data-stu-id="761a4-115">Output : 'T[][]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="761a4-116">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="761a4-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="761a4-117">Е</span><span class="sxs-lookup"><span data-stu-id="761a4-117">'T</span></span>

<span data-ttu-id="761a4-118">Тип `array` элементов.</span><span class="sxs-lookup"><span data-stu-id="761a4-118">The type of `array` elements.</span></span>