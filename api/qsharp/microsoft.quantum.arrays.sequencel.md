---
uid: Microsoft.Quantum.Arrays.SequenceL
title: Функция Sequence
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceL
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: 3e5c7f64825f09d82792d3e46fe3f53f5814510b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220269"
---
# <a name="sequencel-function"></a><span data-ttu-id="4ba82-102">Функция Sequence</span><span class="sxs-lookup"><span data-stu-id="4ba82-102">SequenceL function</span></span>

<span data-ttu-id="4ba82-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="4ba82-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="4ba82-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4ba82-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4ba82-105">Получение массива целых чисел в заданном интервале.</span><span class="sxs-lookup"><span data-stu-id="4ba82-105">Get an array of integers in a given interval.</span></span>

```qsharp
function SequenceL (from : BigInt, to : BigInt) : BigInt[]
```


## <a name="input"></a><span data-ttu-id="4ba82-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="4ba82-106">Input</span></span>

### <a name="from--bigint"></a><span data-ttu-id="4ba82-107">от: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="4ba82-107">from : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="4ba82-108">Инклюзивный начальный индекс интервала.</span><span class="sxs-lookup"><span data-stu-id="4ba82-108">An inclusive start index of the interval.</span></span>


### <a name="to--bigint"></a><span data-ttu-id="4ba82-109">в: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="4ba82-109">to : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="4ba82-110">Включающий Конечный индекс интервала, который не меньше `from` .</span><span class="sxs-lookup"><span data-stu-id="4ba82-110">An inclusive end index of the interval that is not smaller than `from`.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="4ba82-111">Выходные данные: [bigint](xref:microsoft.quantum.lang-ref.bigint)[]</span><span class="sxs-lookup"><span data-stu-id="4ba82-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)[]</span></span>

<span data-ttu-id="4ba82-112">Массив, содержащий последовательность чисел `from` , `from + 1` ,..., `to` .</span><span class="sxs-lookup"><span data-stu-id="4ba82-112">An array containing the sequence of numbers `from`, `from + 1`, ..., `to`.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ba82-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4ba82-113">Remarks</span></span>

<span data-ttu-id="4ba82-114">Разница между `from` и `to` должна соответствовать `Int` значению.</span><span class="sxs-lookup"><span data-stu-id="4ba82-114">The difference between `from` and `to` must fit into an `Int` value.</span></span>