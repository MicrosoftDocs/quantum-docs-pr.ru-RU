---
uid: Microsoft.Quantum.Canon.RepeatA
title: Операция Repeat
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatA
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: 9ae3123a64b2a886df3b7575b2840522f9b011ee
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852222"
---
# <a name="repeata-operation"></a><span data-ttu-id="a1836-102">Операция Repeat</span><span class="sxs-lookup"><span data-stu-id="a1836-102">RepeatA operation</span></span>

<span data-ttu-id="a1836-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a1836-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a1836-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a1836-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a1836-105">Повторяет операцию заданное число раз.</span><span class="sxs-lookup"><span data-stu-id="a1836-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation RepeatA<'TInput> (op : ('TInput => Unit is Adj), nTimes : Int, input : 'TInput) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="a1836-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a1836-106">Input</span></span>

### <a name="op--tinput--unit--is-adj"></a><span data-ttu-id="a1836-107">Op: ' Тинпут =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  в сумме</span><span class="sxs-lookup"><span data-stu-id="a1836-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="a1836-108">Операция, которая вызывается повторно.</span><span class="sxs-lookup"><span data-stu-id="a1836-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="a1836-109">Нтимес: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a1836-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a1836-110">Число вызовов `op` .</span><span class="sxs-lookup"><span data-stu-id="a1836-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="a1836-111">входные данные: ' Тинпут</span><span class="sxs-lookup"><span data-stu-id="a1836-111">input : 'TInput</span></span>

<span data-ttu-id="a1836-112">Входные данные, передаваемые в `op` .</span><span class="sxs-lookup"><span data-stu-id="a1836-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a1836-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a1836-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="a1836-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="a1836-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="a1836-115">' Тинпут</span><span class="sxs-lookup"><span data-stu-id="a1836-115">'TInput</span></span>



## <a name="example"></a><span data-ttu-id="a1836-116">Пример</span><span class="sxs-lookup"><span data-stu-id="a1836-116">Example</span></span>

<span data-ttu-id="a1836-117">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="a1836-117">The following are equivalent:</span></span>

```qsharp
RepeatA(U, 17, target);
(BoundA(ConstantArray(17, U)))(target);
```

## <a name="see-also"></a><span data-ttu-id="a1836-118">См. также:</span><span class="sxs-lookup"><span data-stu-id="a1836-118">See Also</span></span>

- [<span data-ttu-id="a1836-119">Microsoft. тактов. Arrays. Дравмани</span><span class="sxs-lookup"><span data-stu-id="a1836-119">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="a1836-120">Microsoft. тактов. Canon. REPEAT</span><span class="sxs-lookup"><span data-stu-id="a1836-120">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)
- [<span data-ttu-id="a1836-121">Microsoft. тактов. Canon. Репеатк</span><span class="sxs-lookup"><span data-stu-id="a1836-121">Microsoft.Quantum.Canon.RepeatC</span></span>](xref:Microsoft.Quantum.Canon.RepeatC)
- [<span data-ttu-id="a1836-122">Microsoft. тактов. Canon. Репеатка</span><span class="sxs-lookup"><span data-stu-id="a1836-122">Microsoft.Quantum.Canon.RepeatCA</span></span>](xref:Microsoft.Quantum.Canon.RepeatCA)