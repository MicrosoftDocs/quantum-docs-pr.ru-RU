---
uid: Microsoft.Quantum.Arrays.Partitioned
title: Секционированная функция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Partitioned
qsharp.summary: Splits an array into multiple parts.
ms.openlocfilehash: bce46262e3ef64a43e578098d81c5dd39225915e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220507"
---
# <a name="partitioned-function"></a><span data-ttu-id="90cd8-102">Секционированная функция</span><span class="sxs-lookup"><span data-stu-id="90cd8-102">Partitioned function</span></span>

<span data-ttu-id="90cd8-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="90cd8-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="90cd8-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="90cd8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="90cd8-105">Разделяет массив на несколько частей.</span><span class="sxs-lookup"><span data-stu-id="90cd8-105">Splits an array into multiple parts.</span></span>

```qsharp
function Partitioned<'T> (nElements : Int[], arr : 'T[]) : 'T[][]
```


## <a name="input"></a><span data-ttu-id="90cd8-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="90cd8-106">Input</span></span>

### <a name="nelements--int"></a><span data-ttu-id="90cd8-107">Нелементс: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="90cd8-107">nElements : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="90cd8-108">Число элементов в каждой части массива</span><span class="sxs-lookup"><span data-stu-id="90cd8-108">Number of elements in each part of array</span></span>


### <a name="arr--t"></a><span data-ttu-id="90cd8-109">ARR: 'T []</span><span class="sxs-lookup"><span data-stu-id="90cd8-109">arr : 'T[]</span></span>

<span data-ttu-id="90cd8-110">Входной массив для разбиения.</span><span class="sxs-lookup"><span data-stu-id="90cd8-110">Input array to be split.</span></span>



## <a name="output--t"></a><span data-ttu-id="90cd8-111">Выходные данные: 'T [] []</span><span class="sxs-lookup"><span data-stu-id="90cd8-111">Output : 'T[][]</span></span>

<span data-ttu-id="90cd8-112">Несколько массивов, в которых первый массив является первым, `nElements[0]` `arr` а второй массив — рядом и `nElements[1]` `arr` т. д. Последний массив будет содержать все оставшиеся элементы.</span><span class="sxs-lookup"><span data-stu-id="90cd8-112">Multiple arrays where the first array is the first `nElements[0]` of `arr` and the second array are the next `nElements[1]` of `arr` etc. The last array will contain all remaining elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="90cd8-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="90cd8-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="90cd8-114">Е</span><span class="sxs-lookup"><span data-stu-id="90cd8-114">'T</span></span>

