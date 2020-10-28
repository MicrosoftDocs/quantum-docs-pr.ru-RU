---
uid: Microsoft.Quantum.Arrays.Partitioned
title: Секционированная функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Partitioned
qsharp.summary: Splits an array into multiple parts.
ms.openlocfilehash: e3395afeda206e255a58175b57245f91c588d978
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730088"
---
# <a name="partitioned-function"></a><span data-ttu-id="ca204-102">Секционированная функция</span><span class="sxs-lookup"><span data-stu-id="ca204-102">Partitioned function</span></span>

<span data-ttu-id="ca204-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="ca204-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="ca204-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ca204-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ca204-105">Разделяет массив на несколько частей.</span><span class="sxs-lookup"><span data-stu-id="ca204-105">Splits an array into multiple parts.</span></span>

```qsharp
function Partitioned<'T> (nElements : Int[], arr : 'T[]) : 'T[][]
```


## <a name="input"></a><span data-ttu-id="ca204-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ca204-106">Input</span></span>

### <a name="nelements--int"></a><span data-ttu-id="ca204-107">Нелементс: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="ca204-107">nElements : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="ca204-108">Число элементов в каждой части массива</span><span class="sxs-lookup"><span data-stu-id="ca204-108">Number of elements in each part of array</span></span>


### <a name="arr--t"></a><span data-ttu-id="ca204-109">ARR: 'T []</span><span class="sxs-lookup"><span data-stu-id="ca204-109">arr : 'T[]</span></span>

<span data-ttu-id="ca204-110">Входной массив для разбиения.</span><span class="sxs-lookup"><span data-stu-id="ca204-110">Input array to be split.</span></span>



## <a name="output--t"></a><span data-ttu-id="ca204-111">Выходные данные: 'T [] []</span><span class="sxs-lookup"><span data-stu-id="ca204-111">Output : 'T[][]</span></span>

<span data-ttu-id="ca204-112">Несколько массивов, в которых первый массив является первым, `nElements[0]` `arr` а второй массив — рядом и `nElements[1]` `arr` т. д. Последний массив будет содержать все оставшиеся элементы.</span><span class="sxs-lookup"><span data-stu-id="ca204-112">Multiple arrays where the first array is the first `nElements[0]` of `arr` and the second array are the next `nElements[1]` of `arr` etc. The last array will contain all remaining elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="ca204-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="ca204-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ca204-114">Е</span><span class="sxs-lookup"><span data-stu-id="ca204-114">'T</span></span>

