---
uid: Microsoft.Quantum.Arrays.DrawMany
title: Операция Дравмани
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: DrawMany
qsharp.summary: Repeats an operation for a given number of samples, collecting its outputs in an array.
ms.openlocfilehash: bf63ce308679cef97c776d3383ff732ed4d4e500
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846210"
---
# <a name="drawmany-operation"></a><span data-ttu-id="bbb6f-102">Операция Дравмани</span><span class="sxs-lookup"><span data-stu-id="bbb6f-102">DrawMany operation</span></span>

<span data-ttu-id="bbb6f-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="bbb6f-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="bbb6f-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bbb6f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bbb6f-105">Повторяет операцию для заданного числа выборок, собирая выходные данные в массиве.</span><span class="sxs-lookup"><span data-stu-id="bbb6f-105">Repeats an operation for a given number of samples, collecting its outputs in an array.</span></span>

```qsharp
operation DrawMany<'TInput, 'TOutput> (op : ('TInput => 'TOutput), nSamples : Int, input : 'TInput) : 'TOutput[]
```


## <a name="input"></a><span data-ttu-id="bbb6f-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="bbb6f-106">Input</span></span>

### <a name="op--tinput--toutput"></a><span data-ttu-id="bbb6f-107">Op: ' Тинпут => ' Таутпут</span><span class="sxs-lookup"><span data-stu-id="bbb6f-107">op : 'TInput => 'TOutput</span></span> 

<span data-ttu-id="bbb6f-108">Операция, которая вызывается повторно.</span><span class="sxs-lookup"><span data-stu-id="bbb6f-108">The operation to be called repeatedly.</span></span>


### <a name="nsamples--int"></a><span data-ttu-id="bbb6f-109">Нсамплес: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="bbb6f-109">nSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="bbb6f-110">Число выборок вызова `op` для сбора.</span><span class="sxs-lookup"><span data-stu-id="bbb6f-110">The number of samples of calling `op` to collect.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="bbb6f-111">входные данные: ' Тинпут</span><span class="sxs-lookup"><span data-stu-id="bbb6f-111">input : 'TInput</span></span>

<span data-ttu-id="bbb6f-112">Входные данные, передаваемые в `op` .</span><span class="sxs-lookup"><span data-stu-id="bbb6f-112">The input to be passed to `op`.</span></span>



## <a name="output--toutput"></a><span data-ttu-id="bbb6f-113">Выходные данные: ' Таутпут []</span><span class="sxs-lookup"><span data-stu-id="bbb6f-113">Output : 'TOutput[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="bbb6f-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="bbb6f-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="bbb6f-115">' Тинпут</span><span class="sxs-lookup"><span data-stu-id="bbb6f-115">'TInput</span></span>


### <a name="toutput"></a><span data-ttu-id="bbb6f-116">' Таутпут</span><span class="sxs-lookup"><span data-stu-id="bbb6f-116">'TOutput</span></span>



## <a name="example"></a><span data-ttu-id="bbb6f-117">Пример</span><span class="sxs-lookup"><span data-stu-id="bbb6f-117">Example</span></span>

<span data-ttu-id="bbb6f-118">Следующий пример кода выдает целое число с учетом операции, которая производит выборку по одному биту за раз.</span><span class="sxs-lookup"><span data-stu-id="bbb6f-118">The following samples an integer, given an operation that samples a single bit at a time.</span></span>

```qsharp
let randomInteger = BoolArrayAsInt(DrawMany(SampleRandomBit, 16, ()));
```

## <a name="see-also"></a><span data-ttu-id="bbb6f-119">См. также:</span><span class="sxs-lookup"><span data-stu-id="bbb6f-119">See Also</span></span>

- [<span data-ttu-id="bbb6f-120">Microsoft. тактов. Canon. REPEAT</span><span class="sxs-lookup"><span data-stu-id="bbb6f-120">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)