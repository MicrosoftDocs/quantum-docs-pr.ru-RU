---
uid: Microsoft.Quantum.Arrays.Chunks
title: Блоки, функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Chunks
qsharp.summary: Splits an array into multiple parts of equal length.
ms.openlocfilehash: fe10999d35ed05908fd59b9dad8b5c0c51233ae6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730416"
---
# <a name="chunks-function"></a><span data-ttu-id="3dc82-102">Блоки, функция</span><span class="sxs-lookup"><span data-stu-id="3dc82-102">Chunks function</span></span>

<span data-ttu-id="3dc82-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="3dc82-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="3dc82-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3dc82-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3dc82-105">Разделяет массив на несколько частей равной длины.</span><span class="sxs-lookup"><span data-stu-id="3dc82-105">Splits an array into multiple parts of equal length.</span></span>

```qsharp
function Chunks<'T> (nElements : Int, arr : 'T[]) : 'T[][]
```


## <a name="input"></a><span data-ttu-id="3dc82-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="3dc82-106">Input</span></span>

### <a name="nelements--int"></a><span data-ttu-id="3dc82-107">Нелементс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3dc82-107">nElements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3dc82-108">Длина каждого блока.</span><span class="sxs-lookup"><span data-stu-id="3dc82-108">The length of each chunk.</span></span>


### <a name="arr--t"></a><span data-ttu-id="3dc82-109">ARR: 'T []</span><span class="sxs-lookup"><span data-stu-id="3dc82-109">arr : 'T[]</span></span>

<span data-ttu-id="3dc82-110">Массив для разбиения.</span><span class="sxs-lookup"><span data-stu-id="3dc82-110">The array to be split.</span></span>



## <a name="output--t"></a><span data-ttu-id="3dc82-111">Выходные данные: 'T [] []</span><span class="sxs-lookup"><span data-stu-id="3dc82-111">Output : 'T[][]</span></span>

<span data-ttu-id="3dc82-112">Массив, содержащий каждый фрагмент исходного массива.</span><span class="sxs-lookup"><span data-stu-id="3dc82-112">A array containing each chunk of the original array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="3dc82-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="3dc82-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="3dc82-114">Е</span><span class="sxs-lookup"><span data-stu-id="3dc82-114">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="3dc82-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="3dc82-115">Remarks</span></span>

<span data-ttu-id="3dc82-116">Обратите внимание, что последний элемент выходных данных может быть короче, чем `nElements` `Length(arr)` , если не делится на `nElements` .</span><span class="sxs-lookup"><span data-stu-id="3dc82-116">Note that the last element of the output may be shorter than `nElements` if `Length(arr)` is not divisible by `nElements`.</span></span>