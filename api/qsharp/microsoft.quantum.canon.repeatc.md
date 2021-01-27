---
uid: Microsoft.Quantum.Canon.RepeatC
title: Операция Репеатк
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatC
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: efb820411be63352fc09ada2441a9140dd5575f9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840237"
---
# <a name="repeatc-operation"></a><span data-ttu-id="94c3a-102">Операция Репеатк</span><span class="sxs-lookup"><span data-stu-id="94c3a-102">RepeatC operation</span></span>

<span data-ttu-id="94c3a-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="94c3a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="94c3a-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="94c3a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="94c3a-105">Повторяет операцию заданное число раз.</span><span class="sxs-lookup"><span data-stu-id="94c3a-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation RepeatC<'TInput> (op : ('TInput => Unit is Ctl), nTimes : Int, input : 'TInput) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="94c3a-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="94c3a-106">Input</span></span>

### <a name="op--tinput--unit--is-ctl"></a><span data-ttu-id="94c3a-107">Op: "Тинпут = [Unit](xref:microsoft.quantum.lang-ref.unit) > является CTL</span><span class="sxs-lookup"><span data-stu-id="94c3a-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="94c3a-108">Операция, которая вызывается повторно.</span><span class="sxs-lookup"><span data-stu-id="94c3a-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="94c3a-109">Нтимес: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="94c3a-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="94c3a-110">Число вызовов `op` .</span><span class="sxs-lookup"><span data-stu-id="94c3a-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="94c3a-111">входные данные: ' Тинпут</span><span class="sxs-lookup"><span data-stu-id="94c3a-111">input : 'TInput</span></span>

<span data-ttu-id="94c3a-112">Входные данные, передаваемые в `op` .</span><span class="sxs-lookup"><span data-stu-id="94c3a-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="94c3a-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="94c3a-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="94c3a-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="94c3a-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="94c3a-115">' Тинпут</span><span class="sxs-lookup"><span data-stu-id="94c3a-115">'TInput</span></span>



## <a name="example"></a><span data-ttu-id="94c3a-116">Пример</span><span class="sxs-lookup"><span data-stu-id="94c3a-116">Example</span></span>

<span data-ttu-id="94c3a-117">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="94c3a-117">The following are equivalent:</span></span>

```qsharp
RepeatC(U, 17, target);
(BoundC(ConstantArray(17, U)))(target);
```

## <a name="see-also"></a><span data-ttu-id="94c3a-118">См. также:</span><span class="sxs-lookup"><span data-stu-id="94c3a-118">See Also</span></span>

- [<span data-ttu-id="94c3a-119">Microsoft. тактов. Arrays. Дравмани</span><span class="sxs-lookup"><span data-stu-id="94c3a-119">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="94c3a-120">Microsoft. тактов. Canon. REPEAT</span><span class="sxs-lookup"><span data-stu-id="94c3a-120">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)
- [<span data-ttu-id="94c3a-121">Microsoft. тактов. Canon. REPEAT</span><span class="sxs-lookup"><span data-stu-id="94c3a-121">Microsoft.Quantum.Canon.RepeatA</span></span>](xref:Microsoft.Quantum.Canon.RepeatA)
- [<span data-ttu-id="94c3a-122">Microsoft. тактов. Canon. Репеатка</span><span class="sxs-lookup"><span data-stu-id="94c3a-122">Microsoft.Quantum.Canon.RepeatCA</span></span>](xref:Microsoft.Quantum.Canon.RepeatCA)