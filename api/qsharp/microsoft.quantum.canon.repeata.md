---
uid: Microsoft.Quantum.Canon.RepeatA
title: Операция Repeat
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatA
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: 5f418f67d7265d4cb39b3636906c74d33d80f472
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205564"
---
# <a name="repeata-operation"></a><span data-ttu-id="5bf06-102">Операция Repeat</span><span class="sxs-lookup"><span data-stu-id="5bf06-102">RepeatA operation</span></span>

<span data-ttu-id="5bf06-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5bf06-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5bf06-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5bf06-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5bf06-105">Повторяет операцию заданное число раз.</span><span class="sxs-lookup"><span data-stu-id="5bf06-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation RepeatA<'TInput> (op : ('TInput => Unit is Adj), nTimes : Int, input : 'TInput) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="5bf06-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5bf06-106">Input</span></span>

### <a name="op--tinput--unit--is-adj"></a><span data-ttu-id="5bf06-107">Op: ' Тинпут =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  в сумме</span><span class="sxs-lookup"><span data-stu-id="5bf06-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="5bf06-108">Операция, которая вызывается повторно.</span><span class="sxs-lookup"><span data-stu-id="5bf06-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="5bf06-109">Нтимес: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5bf06-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5bf06-110">Число вызовов `op` .</span><span class="sxs-lookup"><span data-stu-id="5bf06-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="5bf06-111">входные данные: ' Тинпут</span><span class="sxs-lookup"><span data-stu-id="5bf06-111">input : 'TInput</span></span>

<span data-ttu-id="5bf06-112">Входные данные, передаваемые в `op` .</span><span class="sxs-lookup"><span data-stu-id="5bf06-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5bf06-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5bf06-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="5bf06-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="5bf06-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="5bf06-115">' Тинпут</span><span class="sxs-lookup"><span data-stu-id="5bf06-115">'TInput</span></span>



## <a name="see-also"></a><span data-ttu-id="5bf06-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="5bf06-116">See Also</span></span>

- [<span data-ttu-id="5bf06-117">Microsoft. тактов. Arrays. Дравмани</span><span class="sxs-lookup"><span data-stu-id="5bf06-117">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="5bf06-118">Microsoft. тактов. Canon. REPEAT</span><span class="sxs-lookup"><span data-stu-id="5bf06-118">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)
- [<span data-ttu-id="5bf06-119">Microsoft. тактов. Canon. Репеатк</span><span class="sxs-lookup"><span data-stu-id="5bf06-119">Microsoft.Quantum.Canon.RepeatC</span></span>](xref:Microsoft.Quantum.Canon.RepeatC)
- [<span data-ttu-id="5bf06-120">Microsoft. тактов. Canon. Репеатка</span><span class="sxs-lookup"><span data-stu-id="5bf06-120">Microsoft.Quantum.Canon.RepeatCA</span></span>](xref:Microsoft.Quantum.Canon.RepeatCA)