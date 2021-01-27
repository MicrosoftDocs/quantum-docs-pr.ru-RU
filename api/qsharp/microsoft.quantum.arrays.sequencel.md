---
uid: Microsoft.Quantum.Arrays.SequenceL
title: Функция Sequence
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceL
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: 7e3c5c31428f9be152e28afbe478a3d15eb0a56c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850984"
---
# <a name="sequencel-function"></a><span data-ttu-id="5d2cc-102">Функция Sequence</span><span class="sxs-lookup"><span data-stu-id="5d2cc-102">SequenceL function</span></span>

<span data-ttu-id="5d2cc-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="5d2cc-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="5d2cc-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5d2cc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5d2cc-105">Получение массива целых чисел в заданном интервале.</span><span class="sxs-lookup"><span data-stu-id="5d2cc-105">Get an array of integers in a given interval.</span></span>

```qsharp
function SequenceL (from : BigInt, to : BigInt) : BigInt[]
```


## <a name="input"></a><span data-ttu-id="5d2cc-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5d2cc-106">Input</span></span>

### <a name="from--bigint"></a><span data-ttu-id="5d2cc-107">от: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="5d2cc-107">from : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="5d2cc-108">Инклюзивный начальный индекс интервала.</span><span class="sxs-lookup"><span data-stu-id="5d2cc-108">An inclusive start index of the interval.</span></span>


### <a name="to--bigint"></a><span data-ttu-id="5d2cc-109">в: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="5d2cc-109">to : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="5d2cc-110">Включающий Конечный индекс интервала, который не меньше `from` .</span><span class="sxs-lookup"><span data-stu-id="5d2cc-110">An inclusive end index of the interval that is not smaller than `from`.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="5d2cc-111">Выходные данные: [bigint](xref:microsoft.quantum.lang-ref.bigint)[]</span><span class="sxs-lookup"><span data-stu-id="5d2cc-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)[]</span></span>

<span data-ttu-id="5d2cc-112">Массив, содержащий последовательность чисел `from` , `from + 1` ,..., `to` .</span><span class="sxs-lookup"><span data-stu-id="5d2cc-112">An array containing the sequence of numbers `from`, `from + 1`, ..., `to`.</span></span>

## <a name="example"></a><span data-ttu-id="5d2cc-113">Пример</span><span class="sxs-lookup"><span data-stu-id="5d2cc-113">Example</span></span>

```qsharp
let arr1 = SequenceL(0L, 3L); // [0L, 1L, 2L, 3L]
let arr2 = SequenceL(23L, 29L); // [23L, 24L, 25L, 26L, 27L, 28L, 29L]
let arr3 = SequenceL(-5L, -2L); // [-5L, -4L, -3L, -2L]
```

## <a name="remarks"></a><span data-ttu-id="5d2cc-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="5d2cc-114">Remarks</span></span>

<span data-ttu-id="5d2cc-115">Разница между `from` и `to` должна соответствовать `Int` значению.</span><span class="sxs-lookup"><span data-stu-id="5d2cc-115">The difference between `from` and `to` must fit into an `Int` value.</span></span>