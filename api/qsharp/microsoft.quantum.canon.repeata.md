---
uid: Microsoft.Quantum.Canon.RepeatA
title: Операция Repeat
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatA
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: 89d34e5a30a61dee392904ce1076605432e21395
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715565"
---
# <a name="repeata-operation"></a><span data-ttu-id="c55c5-102">Операция Repeat</span><span class="sxs-lookup"><span data-stu-id="c55c5-102">RepeatA operation</span></span>

<span data-ttu-id="c55c5-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c55c5-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c55c5-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c55c5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c55c5-105">Повторяет операцию заданное число раз.</span><span class="sxs-lookup"><span data-stu-id="c55c5-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation RepeatA<'TInput> (op : ('TInput => Unit is Adj), nTimes : Int, input : 'TInput) : Unit
```


## <a name="input"></a><span data-ttu-id="c55c5-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c55c5-106">Input</span></span>

### <a name="op--tinput--unit-adj"></a><span data-ttu-id="c55c5-107">Op: ' Тинпут [=>ная](xref:microsoft.quantum.lang-ref.unit) прогода</span><span class="sxs-lookup"><span data-stu-id="c55c5-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="c55c5-108">Операция, которая вызывается повторно.</span><span class="sxs-lookup"><span data-stu-id="c55c5-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="c55c5-109">Нтимес: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c55c5-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c55c5-110">Число вызовов `op` .</span><span class="sxs-lookup"><span data-stu-id="c55c5-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="c55c5-111">входные данные: ' Тинпут</span><span class="sxs-lookup"><span data-stu-id="c55c5-111">input : 'TInput</span></span>

<span data-ttu-id="c55c5-112">Входные данные, передаваемые в `op` .</span><span class="sxs-lookup"><span data-stu-id="c55c5-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c55c5-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c55c5-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="c55c5-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="c55c5-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="c55c5-115">' Тинпут</span><span class="sxs-lookup"><span data-stu-id="c55c5-115">'TInput</span></span>



## <a name="see-also"></a><span data-ttu-id="c55c5-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="c55c5-116">See Also</span></span>

- [<span data-ttu-id="c55c5-117">Microsoft. тактов. Arrays. Дравмани</span><span class="sxs-lookup"><span data-stu-id="c55c5-117">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="c55c5-118">Microsoft. тактов. Canon. REPEAT</span><span class="sxs-lookup"><span data-stu-id="c55c5-118">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)
- [<span data-ttu-id="c55c5-119">Microsoft. тактов. Canon. Репеатк</span><span class="sxs-lookup"><span data-stu-id="c55c5-119">Microsoft.Quantum.Canon.RepeatC</span></span>](xref:Microsoft.Quantum.Canon.RepeatC)
- [<span data-ttu-id="c55c5-120">Microsoft. тактов. Canon. Репеатка</span><span class="sxs-lookup"><span data-stu-id="c55c5-120">Microsoft.Quantum.Canon.RepeatCA</span></span>](xref:Microsoft.Quantum.Canon.RepeatCA)