---
uid: Microsoft.Quantum.Canon.RepeatC
title: Операция Репеатк
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatC
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: 30fd172584b36601c4b81deff494cf55964518f2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205445"
---
# <a name="repeatc-operation"></a><span data-ttu-id="e7f6e-102">Операция Репеатк</span><span class="sxs-lookup"><span data-stu-id="e7f6e-102">RepeatC operation</span></span>

<span data-ttu-id="e7f6e-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e7f6e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e7f6e-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e7f6e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e7f6e-105">Повторяет операцию заданное число раз.</span><span class="sxs-lookup"><span data-stu-id="e7f6e-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation RepeatC<'TInput> (op : ('TInput => Unit is Ctl), nTimes : Int, input : 'TInput) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="e7f6e-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e7f6e-106">Input</span></span>

### <a name="op--tinput--unit--is-ctl"></a><span data-ttu-id="e7f6e-107">Op: "Тинпут = [Unit](xref:microsoft.quantum.lang-ref.unit) > является CTL</span><span class="sxs-lookup"><span data-stu-id="e7f6e-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="e7f6e-108">Операция, которая вызывается повторно.</span><span class="sxs-lookup"><span data-stu-id="e7f6e-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="e7f6e-109">Нтимес: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e7f6e-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e7f6e-110">Число вызовов `op` .</span><span class="sxs-lookup"><span data-stu-id="e7f6e-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="e7f6e-111">входные данные: ' Тинпут</span><span class="sxs-lookup"><span data-stu-id="e7f6e-111">input : 'TInput</span></span>

<span data-ttu-id="e7f6e-112">Входные данные, передаваемые в `op` .</span><span class="sxs-lookup"><span data-stu-id="e7f6e-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e7f6e-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e7f6e-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e7f6e-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="e7f6e-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="e7f6e-115">' Тинпут</span><span class="sxs-lookup"><span data-stu-id="e7f6e-115">'TInput</span></span>



## <a name="see-also"></a><span data-ttu-id="e7f6e-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="e7f6e-116">See Also</span></span>

- [<span data-ttu-id="e7f6e-117">Microsoft. тактов. Arrays. Дравмани</span><span class="sxs-lookup"><span data-stu-id="e7f6e-117">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="e7f6e-118">Microsoft. тактов. Canon. REPEAT</span><span class="sxs-lookup"><span data-stu-id="e7f6e-118">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)
- [<span data-ttu-id="e7f6e-119">Microsoft. тактов. Canon. REPEAT</span><span class="sxs-lookup"><span data-stu-id="e7f6e-119">Microsoft.Quantum.Canon.RepeatA</span></span>](xref:Microsoft.Quantum.Canon.RepeatA)
- [<span data-ttu-id="e7f6e-120">Microsoft. тактов. Canon. Репеатка</span><span class="sxs-lookup"><span data-stu-id="e7f6e-120">Microsoft.Quantum.Canon.RepeatCA</span></span>](xref:Microsoft.Quantum.Canon.RepeatCA)