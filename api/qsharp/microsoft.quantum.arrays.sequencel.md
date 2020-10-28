---
uid: Microsoft.Quantum.Arrays.SequenceL
title: Функция Sequence
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceL
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: d5ce63575e703341fce42c0be393765c342bbd89
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730024"
---
# <a name="sequencel-function"></a><span data-ttu-id="2bb94-102">Функция Sequence</span><span class="sxs-lookup"><span data-stu-id="2bb94-102">SequenceL function</span></span>

<span data-ttu-id="2bb94-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="2bb94-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="2bb94-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2bb94-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2bb94-105">Получение массива целых чисел в заданном интервале.</span><span class="sxs-lookup"><span data-stu-id="2bb94-105">Get an array of integers in a given interval.</span></span>

```qsharp
function SequenceL (from : BigInt, to : BigInt) : BigInt[]
```


## <a name="input"></a><span data-ttu-id="2bb94-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2bb94-106">Input</span></span>

### <a name="from--bigint"></a><span data-ttu-id="2bb94-107">от: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="2bb94-107">from : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="2bb94-108">Инклюзивный начальный индекс интервала.</span><span class="sxs-lookup"><span data-stu-id="2bb94-108">An inclusive start index of the interval.</span></span>


### <a name="to--bigint"></a><span data-ttu-id="2bb94-109">в: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="2bb94-109">to : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="2bb94-110">Включающий Конечный индекс интервала, который не меньше `from` .</span><span class="sxs-lookup"><span data-stu-id="2bb94-110">An inclusive end index of the interval that is not smaller than `from`.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="2bb94-111">Выходные данные: [bigint](xref:microsoft.quantum.lang-ref.bigint)[]</span><span class="sxs-lookup"><span data-stu-id="2bb94-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)[]</span></span>

<span data-ttu-id="2bb94-112">Массив, содержащий последовательность чисел `from` , `from + 1` ,..., `to` .</span><span class="sxs-lookup"><span data-stu-id="2bb94-112">An array containing the sequence of numbers `from`, `from + 1`, ..., `to`.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bb94-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="2bb94-113">Remarks</span></span>

<span data-ttu-id="2bb94-114">Разница между `from` и `to` должна соответствовать `Int` значению.</span><span class="sxs-lookup"><span data-stu-id="2bb94-114">The difference between `from` and `to` must fit into an `Int` value.</span></span>