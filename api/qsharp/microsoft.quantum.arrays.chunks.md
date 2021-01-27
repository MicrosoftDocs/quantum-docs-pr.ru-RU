---
uid: Microsoft.Quantum.Arrays.Chunks
title: Блоки, функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Chunks
qsharp.summary: Splits an array into multiple parts of equal length.
ms.openlocfilehash: 977594839a7d2fe09de8138d32a4a50e8a752390
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842870"
---
# <a name="chunks-function"></a><span data-ttu-id="60dad-102">Блоки, функция</span><span class="sxs-lookup"><span data-stu-id="60dad-102">Chunks function</span></span>

<span data-ttu-id="60dad-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="60dad-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="60dad-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="60dad-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="60dad-105">Разделяет массив на несколько частей равной длины.</span><span class="sxs-lookup"><span data-stu-id="60dad-105">Splits an array into multiple parts of equal length.</span></span>

```qsharp
function Chunks<'T> (nElements : Int, arr : 'T[]) : 'T[][]
```


## <a name="input"></a><span data-ttu-id="60dad-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="60dad-106">Input</span></span>

### <a name="nelements--int"></a><span data-ttu-id="60dad-107">Нелементс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="60dad-107">nElements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="60dad-108">Длина каждого блока.</span><span class="sxs-lookup"><span data-stu-id="60dad-108">The length of each chunk.</span></span>


### <a name="arr--t"></a><span data-ttu-id="60dad-109">ARR: 'T []</span><span class="sxs-lookup"><span data-stu-id="60dad-109">arr : 'T[]</span></span>

<span data-ttu-id="60dad-110">Массив для разбиения.</span><span class="sxs-lookup"><span data-stu-id="60dad-110">The array to be split.</span></span>



## <a name="output--t"></a><span data-ttu-id="60dad-111">Выходные данные: 'T [] []</span><span class="sxs-lookup"><span data-stu-id="60dad-111">Output : 'T[][]</span></span>

<span data-ttu-id="60dad-112">Массив, содержащий каждый фрагмент исходного массива.</span><span class="sxs-lookup"><span data-stu-id="60dad-112">A array containing each chunk of the original array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="60dad-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="60dad-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="60dad-114">Е</span><span class="sxs-lookup"><span data-stu-id="60dad-114">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="60dad-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="60dad-115">Remarks</span></span>

<span data-ttu-id="60dad-116">Обратите внимание, что последний элемент выходных данных может быть короче, чем `nElements` `Length(arr)` , если не делится на `nElements` .</span><span class="sxs-lookup"><span data-stu-id="60dad-116">Note that the last element of the output may be shorter than `nElements` if `Length(arr)` is not divisible by `nElements`.</span></span>