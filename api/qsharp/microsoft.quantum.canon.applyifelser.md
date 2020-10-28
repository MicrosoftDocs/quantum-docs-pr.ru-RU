---
uid: Microsoft.Quantum.Canon.ApplyIfElseR
title: Операция Апплифелсер
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseR
qsharp.summary: Applies one of two operations, depending on the value of a classical result.
ms.openlocfilehash: 78c1cf23614fbb7c27122548de487c7350467948
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718156"
---
# <a name="applyifelser-operation"></a><span data-ttu-id="6b58a-102">Операция Апплифелсер</span><span class="sxs-lookup"><span data-stu-id="6b58a-102">ApplyIfElseR operation</span></span>

<span data-ttu-id="6b58a-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="6b58a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="6b58a-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6b58a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6b58a-105">Применяет одну из двух операций в зависимости от значения классического результата.</span><span class="sxs-lookup"><span data-stu-id="6b58a-105">Applies one of two operations, depending on the value of a classical result.</span></span>

```qsharp
operation ApplyIfElseR<'T, 'U> (result : Result, (zeroOp : ('T => Unit), zeroInput : 'T), (oneOp : ('U => Unit), oneInput : 'U)) : Unit
```


## <a name="description"></a><span data-ttu-id="6b58a-106">Описание</span><span class="sxs-lookup"><span data-stu-id="6b58a-106">Description</span></span>

<span data-ttu-id="6b58a-107">Учитывая результат `result` , применяет операцию `zeroOp` с в `zeroInput` качестве входных данных, если равен `result` `Zero` , и применяется, `oneOp(oneInput)` когда `result == One` .</span><span class="sxs-lookup"><span data-stu-id="6b58a-107">Given a result `result`, applies the operation `zeroOp` with `zeroInput` as its input when `result` is equal to `Zero`, and applies `oneOp(oneInput)` when `result == One`.</span></span>

## <a name="input"></a><span data-ttu-id="6b58a-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="6b58a-108">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="6b58a-109">результат: __недопустимо <Result>__</span><span class="sxs-lookup"><span data-stu-id="6b58a-109">result : __invalid<Result>__</span></span>

<span data-ttu-id="6b58a-110">Результат измерения, используемый для определения `zeroOp` применения или `oneOp` .</span><span class="sxs-lookup"><span data-stu-id="6b58a-110">The measurement result used to determine if `zeroOp` or `oneOp` is applied.</span></span>


### <a name="zeroop--t--unit"></a><span data-ttu-id="6b58a-111">Зеруп: 'T = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="6b58a-111">zeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="6b58a-112">Операция, которая должна быть применена, когда `result == Zero` .</span><span class="sxs-lookup"><span data-stu-id="6b58a-112">The operation to be applied when `result == Zero`.</span></span>


### <a name="zeroinput--t"></a><span data-ttu-id="6b58a-113">Зероинпут: 'T</span><span class="sxs-lookup"><span data-stu-id="6b58a-113">zeroInput : 'T</span></span>

<span data-ttu-id="6b58a-114">Входные данные, которые должны быть предоставлены в `zeroOp` when `result == Zero` .</span><span class="sxs-lookup"><span data-stu-id="6b58a-114">The input to be provided to `zeroOp` when `result == Zero`.</span></span>


### <a name="oneop--u--unit"></a><span data-ttu-id="6b58a-115">Онеоп: "U = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="6b58a-115">oneOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="6b58a-116">Операция, которая должна быть применена, когда `result == One` .</span><span class="sxs-lookup"><span data-stu-id="6b58a-116">The operation to be applied when `result == One`.</span></span>


### <a name="oneinput--u"></a><span data-ttu-id="6b58a-117">Онеинпут: ' U</span><span class="sxs-lookup"><span data-stu-id="6b58a-117">oneInput : 'U</span></span>

<span data-ttu-id="6b58a-118">Входные данные, которые должны быть предоставлены в `oneOp` when `result == One` .</span><span class="sxs-lookup"><span data-stu-id="6b58a-118">The input to be provided to `oneOp` when `result == One`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="6b58a-119">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6b58a-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="6b58a-120">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="6b58a-120">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6b58a-121">Е</span><span class="sxs-lookup"><span data-stu-id="6b58a-121">'T</span></span>

<span data-ttu-id="6b58a-122">Тип входных данных операции `zeroOp` , которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="6b58a-122">The input type of the operation `zeroOp` to be conditionally applied.</span></span>
### <a name="u"></a><span data-ttu-id="6b58a-123">' U</span><span class="sxs-lookup"><span data-stu-id="6b58a-123">'U</span></span>

<span data-ttu-id="6b58a-124">Тип входных данных операции `oneOp` , которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="6b58a-124">The input type of the operation `oneOp` to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="6b58a-125">См. также:</span><span class="sxs-lookup"><span data-stu-id="6b58a-125">See Also</span></span>

- [<span data-ttu-id="6b58a-126">Microsoft. тактов. Canon. Апплифзеро</span><span class="sxs-lookup"><span data-stu-id="6b58a-126">Microsoft.Quantum.Canon.ApplyIfZero</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZero)
- [<span data-ttu-id="6b58a-127">Microsoft. тактов. Canon. Апплифоне</span><span class="sxs-lookup"><span data-stu-id="6b58a-127">Microsoft.Quantum.Canon.ApplyIfOne</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- [<span data-ttu-id="6b58a-128">Microsoft. тактов. Canon. Апплифелсерк</span><span class="sxs-lookup"><span data-stu-id="6b58a-128">Microsoft.Quantum.Canon.ApplyIfElseRC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRC)
- [<span data-ttu-id="6b58a-129">Microsoft. тактов. Canon. Апплифелсера</span><span class="sxs-lookup"><span data-stu-id="6b58a-129">Microsoft.Quantum.Canon.ApplyIfElseRA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRA)
- [<span data-ttu-id="6b58a-130">Microsoft. тактов. Canon. Апплифелсерка</span><span class="sxs-lookup"><span data-stu-id="6b58a-130">Microsoft.Quantum.Canon.ApplyIfElseRCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRCA)