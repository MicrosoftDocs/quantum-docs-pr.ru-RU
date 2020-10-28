---
uid: Microsoft.Quantum.Canon.Repeat
title: Повторить операцию
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Repeat
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: 5aedd056b851b8d8d7c25a32eb22587292e132a8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715594"
---
# <a name="repeat-operation"></a><span data-ttu-id="386d6-102">Повторить операцию</span><span class="sxs-lookup"><span data-stu-id="386d6-102">Repeat operation</span></span>

<span data-ttu-id="386d6-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="386d6-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="386d6-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="386d6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="386d6-105">Повторяет операцию заданное число раз.</span><span class="sxs-lookup"><span data-stu-id="386d6-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation Repeat<'TInput> (op : ('TInput => Unit), nTimes : Int, input : 'TInput) : Unit
```


## <a name="input"></a><span data-ttu-id="386d6-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="386d6-106">Input</span></span>

### <a name="op--tinput--unit"></a><span data-ttu-id="386d6-107">Op: "Тинпут = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="386d6-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="386d6-108">Операция, которая вызывается повторно.</span><span class="sxs-lookup"><span data-stu-id="386d6-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="386d6-109">Нтимес: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="386d6-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="386d6-110">Число вызовов `op` .</span><span class="sxs-lookup"><span data-stu-id="386d6-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="386d6-111">входные данные: ' Тинпут</span><span class="sxs-lookup"><span data-stu-id="386d6-111">input : 'TInput</span></span>

<span data-ttu-id="386d6-112">Входные данные, передаваемые в `op` .</span><span class="sxs-lookup"><span data-stu-id="386d6-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="386d6-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="386d6-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="386d6-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="386d6-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="386d6-115">' Тинпут</span><span class="sxs-lookup"><span data-stu-id="386d6-115">'TInput</span></span>



## <a name="see-also"></a><span data-ttu-id="386d6-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="386d6-116">See Also</span></span>

- [<span data-ttu-id="386d6-117">Microsoft. тактов. Arrays. Дравмани</span><span class="sxs-lookup"><span data-stu-id="386d6-117">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="386d6-118">Microsoft. тактов. Canon. REPEAT</span><span class="sxs-lookup"><span data-stu-id="386d6-118">Microsoft.Quantum.Canon.RepeatA</span></span>](xref:Microsoft.Quantum.Canon.RepeatA)
- [<span data-ttu-id="386d6-119">Microsoft. тактов. Canon. Репеатк</span><span class="sxs-lookup"><span data-stu-id="386d6-119">Microsoft.Quantum.Canon.RepeatC</span></span>](xref:Microsoft.Quantum.Canon.RepeatC)
- [<span data-ttu-id="386d6-120">Microsoft. тактов. Canon. Репеатка</span><span class="sxs-lookup"><span data-stu-id="386d6-120">Microsoft.Quantum.Canon.RepeatCA</span></span>](xref:Microsoft.Quantum.Canon.RepeatCA)