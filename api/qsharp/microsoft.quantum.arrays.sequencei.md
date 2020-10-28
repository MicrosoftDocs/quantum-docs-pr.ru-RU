---
uid: Microsoft.Quantum.Arrays.SequenceI
title: Функция Секуенцеи
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceI
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: d5dc4377c696e14b505c63701c2f5ca0dadca672
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730033"
---
# <a name="sequencei-function"></a><span data-ttu-id="96d25-102">Функция Секуенцеи</span><span class="sxs-lookup"><span data-stu-id="96d25-102">SequenceI function</span></span>

<span data-ttu-id="96d25-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="96d25-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="96d25-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="96d25-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="96d25-105">Получение массива целых чисел в заданном интервале.</span><span class="sxs-lookup"><span data-stu-id="96d25-105">Get an array of integers in a given interval.</span></span>

```qsharp
function SequenceI (from : Int, to : Int) : Int[]
```


## <a name="input"></a><span data-ttu-id="96d25-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="96d25-106">Input</span></span>

### <a name="from--int"></a><span data-ttu-id="96d25-107">от: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="96d25-107">from : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="96d25-108">Инклюзивный начальный индекс интервала.</span><span class="sxs-lookup"><span data-stu-id="96d25-108">An inclusive start index of the interval.</span></span>


### <a name="to--int"></a><span data-ttu-id="96d25-109">в: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="96d25-109">to : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="96d25-110">Включающий Конечный индекс интервала, который не меньше `from` .</span><span class="sxs-lookup"><span data-stu-id="96d25-110">An inclusive end index of the interval that is not smaller than `from`.</span></span>



## <a name="output--int"></a><span data-ttu-id="96d25-111">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="96d25-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="96d25-112">Массив, содержащий последовательность чисел `from` , `from + 1` ,..., `to` .</span><span class="sxs-lookup"><span data-stu-id="96d25-112">An array containing the sequence of numbers `from`, `from + 1`, ..., `to`.</span></span>