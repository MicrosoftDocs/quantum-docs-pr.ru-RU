---
uid: Microsoft.Quantum.Canon.Repeat
title: Повторить операцию
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Repeat
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: 40ee191e8d9044f33aa1621303c70f7e0847e8f6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852242"
---
# <a name="repeat-operation"></a><span data-ttu-id="5e8a0-102">Повторить операцию</span><span class="sxs-lookup"><span data-stu-id="5e8a0-102">Repeat operation</span></span>

<span data-ttu-id="5e8a0-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5e8a0-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5e8a0-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5e8a0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5e8a0-105">Повторяет операцию заданное число раз.</span><span class="sxs-lookup"><span data-stu-id="5e8a0-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation Repeat<'TInput> (op : ('TInput => Unit), nTimes : Int, input : 'TInput) : Unit
```


## <a name="input"></a><span data-ttu-id="5e8a0-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5e8a0-106">Input</span></span>

### <a name="op--tinput--unit"></a><span data-ttu-id="5e8a0-107">Op: "Тинпут = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="5e8a0-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="5e8a0-108">Операция, которая вызывается повторно.</span><span class="sxs-lookup"><span data-stu-id="5e8a0-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="5e8a0-109">Нтимес: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5e8a0-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5e8a0-110">Число вызовов `op` .</span><span class="sxs-lookup"><span data-stu-id="5e8a0-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="5e8a0-111">входные данные: ' Тинпут</span><span class="sxs-lookup"><span data-stu-id="5e8a0-111">input : 'TInput</span></span>

<span data-ttu-id="5e8a0-112">Входные данные, передаваемые в `op` .</span><span class="sxs-lookup"><span data-stu-id="5e8a0-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5e8a0-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5e8a0-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="5e8a0-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="5e8a0-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="5e8a0-115">' Тинпут</span><span class="sxs-lookup"><span data-stu-id="5e8a0-115">'TInput</span></span>



## <a name="example"></a><span data-ttu-id="5e8a0-116">Пример</span><span class="sxs-lookup"><span data-stu-id="5e8a0-116">Example</span></span>

<span data-ttu-id="5e8a0-117">Следующие эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="5e8a0-117">The following are equivalent:</span></span>

```qsharp
Repeat(U, 17, target);
(Bound(ConstantArray(17, U)))(target);
```

## <a name="see-also"></a><span data-ttu-id="5e8a0-118">См. также:</span><span class="sxs-lookup"><span data-stu-id="5e8a0-118">See Also</span></span>

- [<span data-ttu-id="5e8a0-119">Microsoft. тактов. Arrays. Дравмани</span><span class="sxs-lookup"><span data-stu-id="5e8a0-119">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="5e8a0-120">Microsoft. тактов. Canon. REPEAT</span><span class="sxs-lookup"><span data-stu-id="5e8a0-120">Microsoft.Quantum.Canon.RepeatA</span></span>](xref:Microsoft.Quantum.Canon.RepeatA)
- [<span data-ttu-id="5e8a0-121">Microsoft. тактов. Canon. Репеатк</span><span class="sxs-lookup"><span data-stu-id="5e8a0-121">Microsoft.Quantum.Canon.RepeatC</span></span>](xref:Microsoft.Quantum.Canon.RepeatC)
- [<span data-ttu-id="5e8a0-122">Microsoft. тактов. Canon. Репеатка</span><span class="sxs-lookup"><span data-stu-id="5e8a0-122">Microsoft.Quantum.Canon.RepeatCA</span></span>](xref:Microsoft.Quantum.Canon.RepeatCA)