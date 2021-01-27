---
uid: Microsoft.Quantum.Arrays.Partitioned
title: Секционированная функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Partitioned
qsharp.summary: Splits an array into multiple parts.
ms.openlocfilehash: 43d99a0e33a813e4af23a3890ace808e91c1049c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845543"
---
# <a name="partitioned-function"></a><span data-ttu-id="2c1cb-102">Секционированная функция</span><span class="sxs-lookup"><span data-stu-id="2c1cb-102">Partitioned function</span></span>

<span data-ttu-id="2c1cb-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="2c1cb-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="2c1cb-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2c1cb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2c1cb-105">Разделяет массив на несколько частей.</span><span class="sxs-lookup"><span data-stu-id="2c1cb-105">Splits an array into multiple parts.</span></span>

```qsharp
function Partitioned<'T> (nElements : Int[], arr : 'T[]) : 'T[][]
```


## <a name="input"></a><span data-ttu-id="2c1cb-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2c1cb-106">Input</span></span>

### <a name="nelements--int"></a><span data-ttu-id="2c1cb-107">Нелементс: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="2c1cb-107">nElements : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="2c1cb-108">Число элементов в каждой части массива</span><span class="sxs-lookup"><span data-stu-id="2c1cb-108">Number of elements in each part of array</span></span>


### <a name="arr--t"></a><span data-ttu-id="2c1cb-109">ARR: 'T []</span><span class="sxs-lookup"><span data-stu-id="2c1cb-109">arr : 'T[]</span></span>

<span data-ttu-id="2c1cb-110">Входной массив для разбиения.</span><span class="sxs-lookup"><span data-stu-id="2c1cb-110">Input array to be split.</span></span>



## <a name="output--t"></a><span data-ttu-id="2c1cb-111">Выходные данные: 'T [] []</span><span class="sxs-lookup"><span data-stu-id="2c1cb-111">Output : 'T[][]</span></span>

<span data-ttu-id="2c1cb-112">Несколько массивов, в которых первый массив является первым, `nElements[0]` `arr` а второй массив — рядом и `nElements[1]` `arr` т. д. Последний массив будет содержать все оставшиеся элементы.</span><span class="sxs-lookup"><span data-stu-id="2c1cb-112">Multiple arrays where the first array is the first `nElements[0]` of `arr` and the second array are the next `nElements[1]` of `arr` etc. The last array will contain all remaining elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="2c1cb-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="2c1cb-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2c1cb-114">Е</span><span class="sxs-lookup"><span data-stu-id="2c1cb-114">'T</span></span>



## <a name="example"></a><span data-ttu-id="2c1cb-115">Пример</span><span class="sxs-lookup"><span data-stu-id="2c1cb-115">Example</span></span>

```qsharp
// The following returns [[1, 5], [3], [7]];
let split = Partitioned([2,1], [1,5,3,7]);
```