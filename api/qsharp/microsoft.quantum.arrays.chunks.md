---
uid: Microsoft.Quantum.Arrays.Chunks
title: Блоки, функция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Chunks
qsharp.summary: Splits an array into multiple parts of equal length.
ms.openlocfilehash: b323fdab1b207c72a4f46d5ca4cb368ecf0df818
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221612"
---
# <a name="chunks-function"></a><span data-ttu-id="a4d60-102">Блоки, функция</span><span class="sxs-lookup"><span data-stu-id="a4d60-102">Chunks function</span></span>

<span data-ttu-id="a4d60-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="a4d60-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="a4d60-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a4d60-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a4d60-105">Разделяет массив на несколько частей равной длины.</span><span class="sxs-lookup"><span data-stu-id="a4d60-105">Splits an array into multiple parts of equal length.</span></span>

```qsharp
function Chunks<'T> (nElements : Int, arr : 'T[]) : 'T[][]
```


## <a name="input"></a><span data-ttu-id="a4d60-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a4d60-106">Input</span></span>

### <a name="nelements--int"></a><span data-ttu-id="a4d60-107">Нелементс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a4d60-107">nElements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a4d60-108">Длина каждого блока.</span><span class="sxs-lookup"><span data-stu-id="a4d60-108">The length of each chunk.</span></span>


### <a name="arr--t"></a><span data-ttu-id="a4d60-109">ARR: 'T []</span><span class="sxs-lookup"><span data-stu-id="a4d60-109">arr : 'T[]</span></span>

<span data-ttu-id="a4d60-110">Массив для разбиения.</span><span class="sxs-lookup"><span data-stu-id="a4d60-110">The array to be split.</span></span>



## <a name="output--t"></a><span data-ttu-id="a4d60-111">Выходные данные: 'T [] []</span><span class="sxs-lookup"><span data-stu-id="a4d60-111">Output : 'T[][]</span></span>

<span data-ttu-id="a4d60-112">Массив, содержащий каждый фрагмент исходного массива.</span><span class="sxs-lookup"><span data-stu-id="a4d60-112">A array containing each chunk of the original array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a4d60-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="a4d60-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a4d60-114">Е</span><span class="sxs-lookup"><span data-stu-id="a4d60-114">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="a4d60-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a4d60-115">Remarks</span></span>

<span data-ttu-id="a4d60-116">Обратите внимание, что последний элемент выходных данных может быть короче, чем `nElements` `Length(arr)` , если не делится на `nElements` .</span><span class="sxs-lookup"><span data-stu-id="a4d60-116">Note that the last element of the output may be shorter than `nElements` if `Length(arr)` is not divisible by `nElements`.</span></span>