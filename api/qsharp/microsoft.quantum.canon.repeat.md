---
uid: Microsoft.Quantum.Canon.Repeat
title: Повторить операцию
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Repeat
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: cd572e5e082df94d762a0869ad2c1923fb71fd3d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205608"
---
# <a name="repeat-operation"></a><span data-ttu-id="39f8c-102">Повторить операцию</span><span class="sxs-lookup"><span data-stu-id="39f8c-102">Repeat operation</span></span>

<span data-ttu-id="39f8c-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="39f8c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="39f8c-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="39f8c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="39f8c-105">Повторяет операцию заданное число раз.</span><span class="sxs-lookup"><span data-stu-id="39f8c-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation Repeat<'TInput> (op : ('TInput => Unit), nTimes : Int, input : 'TInput) : Unit
```


## <a name="input"></a><span data-ttu-id="39f8c-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="39f8c-106">Input</span></span>

### <a name="op--tinput--unit"></a><span data-ttu-id="39f8c-107">Op: "Тинпут = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="39f8c-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="39f8c-108">Операция, которая вызывается повторно.</span><span class="sxs-lookup"><span data-stu-id="39f8c-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="39f8c-109">Нтимес: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="39f8c-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="39f8c-110">Число вызовов `op` .</span><span class="sxs-lookup"><span data-stu-id="39f8c-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="39f8c-111">входные данные: ' Тинпут</span><span class="sxs-lookup"><span data-stu-id="39f8c-111">input : 'TInput</span></span>

<span data-ttu-id="39f8c-112">Входные данные, передаваемые в `op` .</span><span class="sxs-lookup"><span data-stu-id="39f8c-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="39f8c-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="39f8c-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="39f8c-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="39f8c-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="39f8c-115">' Тинпут</span><span class="sxs-lookup"><span data-stu-id="39f8c-115">'TInput</span></span>



## <a name="see-also"></a><span data-ttu-id="39f8c-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="39f8c-116">See Also</span></span>

- [<span data-ttu-id="39f8c-117">Microsoft. тактов. Arrays. Дравмани</span><span class="sxs-lookup"><span data-stu-id="39f8c-117">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="39f8c-118">Microsoft. тактов. Canon. REPEAT</span><span class="sxs-lookup"><span data-stu-id="39f8c-118">Microsoft.Quantum.Canon.RepeatA</span></span>](xref:Microsoft.Quantum.Canon.RepeatA)
- [<span data-ttu-id="39f8c-119">Microsoft. тактов. Canon. Репеатк</span><span class="sxs-lookup"><span data-stu-id="39f8c-119">Microsoft.Quantum.Canon.RepeatC</span></span>](xref:Microsoft.Quantum.Canon.RepeatC)
- [<span data-ttu-id="39f8c-120">Microsoft. тактов. Canon. Репеатка</span><span class="sxs-lookup"><span data-stu-id="39f8c-120">Microsoft.Quantum.Canon.RepeatCA</span></span>](xref:Microsoft.Quantum.Canon.RepeatCA)