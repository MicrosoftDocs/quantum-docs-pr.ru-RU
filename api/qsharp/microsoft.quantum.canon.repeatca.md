---
uid: Microsoft.Quantum.Canon.RepeatCA
title: Операция Репеатка
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatCA
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: 24606486b3d5703065a7c7f62d3bbc7e3d07615f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205411"
---
# <a name="repeatca-operation"></a><span data-ttu-id="a218e-102">Операция Репеатка</span><span class="sxs-lookup"><span data-stu-id="a218e-102">RepeatCA operation</span></span>

<span data-ttu-id="a218e-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a218e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a218e-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a218e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a218e-105">Повторяет операцию заданное число раз.</span><span class="sxs-lookup"><span data-stu-id="a218e-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation RepeatCA<'TInput> (op : ('TInput => Unit is Adj + Ctl), nTimes : Int, input : 'TInput) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="a218e-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a218e-106">Input</span></span>

### <a name="op--tinput--unit--is-adj--ctl"></a><span data-ttu-id="a218e-107">Op: ' Тинпут =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="a218e-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="a218e-108">Операция, которая вызывается повторно.</span><span class="sxs-lookup"><span data-stu-id="a218e-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="a218e-109">Нтимес: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a218e-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a218e-110">Число вызовов `op` .</span><span class="sxs-lookup"><span data-stu-id="a218e-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="a218e-111">входные данные: ' Тинпут</span><span class="sxs-lookup"><span data-stu-id="a218e-111">input : 'TInput</span></span>

<span data-ttu-id="a218e-112">Входные данные, передаваемые в `op` .</span><span class="sxs-lookup"><span data-stu-id="a218e-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a218e-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a218e-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="a218e-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="a218e-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="a218e-115">' Тинпут</span><span class="sxs-lookup"><span data-stu-id="a218e-115">'TInput</span></span>



## <a name="see-also"></a><span data-ttu-id="a218e-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="a218e-116">See Also</span></span>

- [<span data-ttu-id="a218e-117">Microsoft. тактов. Arrays. Дравмани</span><span class="sxs-lookup"><span data-stu-id="a218e-117">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="a218e-118">Microsoft. тактов. Canon. REPEAT</span><span class="sxs-lookup"><span data-stu-id="a218e-118">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)
- [<span data-ttu-id="a218e-119">Microsoft. тактов. Canon. REPEAT</span><span class="sxs-lookup"><span data-stu-id="a218e-119">Microsoft.Quantum.Canon.RepeatA</span></span>](xref:Microsoft.Quantum.Canon.RepeatA)
- [<span data-ttu-id="a218e-120">Microsoft. тактов. Canon. Репеатк</span><span class="sxs-lookup"><span data-stu-id="a218e-120">Microsoft.Quantum.Canon.RepeatC</span></span>](xref:Microsoft.Quantum.Canon.RepeatC)