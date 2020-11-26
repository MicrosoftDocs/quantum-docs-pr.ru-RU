---
uid: Microsoft.Quantum.Arrays.DrawMany
title: Операция Дравмани
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: DrawMany
qsharp.summary: Repeats an operation for a given number of samples, collecting its outputs in an array.
ms.openlocfilehash: 3185f2ec01a2b9d01cff82a0c4667f12483801a7
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210001"
---
# <a name="drawmany-operation"></a><span data-ttu-id="6b51d-102">Операция Дравмани</span><span class="sxs-lookup"><span data-stu-id="6b51d-102">DrawMany operation</span></span>

<span data-ttu-id="6b51d-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="6b51d-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="6b51d-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6b51d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6b51d-105">Повторяет операцию для заданного числа выборок, собирая выходные данные в массиве.</span><span class="sxs-lookup"><span data-stu-id="6b51d-105">Repeats an operation for a given number of samples, collecting its outputs in an array.</span></span>

```qsharp
operation DrawMany<'TInput, 'TOutput> (op : ('TInput => 'TOutput), nSamples : Int, input : 'TInput) : 'TOutput[]
```


## <a name="input"></a><span data-ttu-id="6b51d-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="6b51d-106">Input</span></span>

### <a name="op--tinput--toutput"></a><span data-ttu-id="6b51d-107">Op: ' Тинпут => ' Таутпут</span><span class="sxs-lookup"><span data-stu-id="6b51d-107">op : 'TInput => 'TOutput</span></span> 

<span data-ttu-id="6b51d-108">Операция, которая вызывается повторно.</span><span class="sxs-lookup"><span data-stu-id="6b51d-108">The operation to be called repeatedly.</span></span>


### <a name="nsamples--int"></a><span data-ttu-id="6b51d-109">Нсамплес: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6b51d-109">nSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6b51d-110">Число выборок вызова `op` для сбора.</span><span class="sxs-lookup"><span data-stu-id="6b51d-110">The number of samples of calling `op` to collect.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="6b51d-111">входные данные: ' Тинпут</span><span class="sxs-lookup"><span data-stu-id="6b51d-111">input : 'TInput</span></span>

<span data-ttu-id="6b51d-112">Входные данные, передаваемые в `op` .</span><span class="sxs-lookup"><span data-stu-id="6b51d-112">The input to be passed to `op`.</span></span>



## <a name="output--toutput"></a><span data-ttu-id="6b51d-113">Выходные данные: ' Таутпут []</span><span class="sxs-lookup"><span data-stu-id="6b51d-113">Output : 'TOutput[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="6b51d-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="6b51d-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="6b51d-115">' Тинпут</span><span class="sxs-lookup"><span data-stu-id="6b51d-115">'TInput</span></span>


### <a name="toutput"></a><span data-ttu-id="6b51d-116">' Таутпут</span><span class="sxs-lookup"><span data-stu-id="6b51d-116">'TOutput</span></span>



## <a name="see-also"></a><span data-ttu-id="6b51d-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="6b51d-117">See Also</span></span>

- [<span data-ttu-id="6b51d-118">Microsoft. тактов. Canon. REPEAT</span><span class="sxs-lookup"><span data-stu-id="6b51d-118">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)