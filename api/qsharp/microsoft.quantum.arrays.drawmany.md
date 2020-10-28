---
uid: Microsoft.Quantum.Arrays.DrawMany
title: Операция Дравмани
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: DrawMany
qsharp.summary: Repeats an operation for a given number of samples, collecting its outputs in an array.
ms.openlocfilehash: 601fe603a869dcf977c1ceade5819ee64f634d53
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730352"
---
# <a name="drawmany-operation"></a><span data-ttu-id="2da10-102">Операция Дравмани</span><span class="sxs-lookup"><span data-stu-id="2da10-102">DrawMany operation</span></span>

<span data-ttu-id="2da10-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="2da10-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="2da10-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2da10-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2da10-105">Повторяет операцию для заданного числа выборок, собирая выходные данные в массиве.</span><span class="sxs-lookup"><span data-stu-id="2da10-105">Repeats an operation for a given number of samples, collecting its outputs in an array.</span></span>

```qsharp
operation DrawMany<'TInput, 'TOutput> (op : ('TInput => 'TOutput), nSamples : Int, input : 'TInput) : 'TOutput[]
```


## <a name="input"></a><span data-ttu-id="2da10-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2da10-106">Input</span></span>

### <a name="op--tinput--toutput"></a><span data-ttu-id="2da10-107">Op: ' Тинпут => ' Таутпут</span><span class="sxs-lookup"><span data-stu-id="2da10-107">op : 'TInput => 'TOutput</span></span> 

<span data-ttu-id="2da10-108">Операция, которая вызывается повторно.</span><span class="sxs-lookup"><span data-stu-id="2da10-108">The operation to be called repeatedly.</span></span>


### <a name="nsamples--int"></a><span data-ttu-id="2da10-109">Нсамплес: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2da10-109">nSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2da10-110">Число выборок вызова `op` для сбора.</span><span class="sxs-lookup"><span data-stu-id="2da10-110">The number of samples of calling `op` to collect.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="2da10-111">входные данные: ' Тинпут</span><span class="sxs-lookup"><span data-stu-id="2da10-111">input : 'TInput</span></span>

<span data-ttu-id="2da10-112">Входные данные, передаваемые в `op` .</span><span class="sxs-lookup"><span data-stu-id="2da10-112">The input to be passed to `op`.</span></span>



## <a name="output--toutput"></a><span data-ttu-id="2da10-113">Выходные данные: ' Таутпут []</span><span class="sxs-lookup"><span data-stu-id="2da10-113">Output : 'TOutput[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="2da10-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="2da10-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="2da10-115">' Тинпут</span><span class="sxs-lookup"><span data-stu-id="2da10-115">'TInput</span></span>


### <a name="toutput"></a><span data-ttu-id="2da10-116">' Таутпут</span><span class="sxs-lookup"><span data-stu-id="2da10-116">'TOutput</span></span>



## <a name="see-also"></a><span data-ttu-id="2da10-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="2da10-117">See Also</span></span>

- [<span data-ttu-id="2da10-118">Microsoft. тактов. Canon. REPEAT</span><span class="sxs-lookup"><span data-stu-id="2da10-118">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)