---
uid: Microsoft.Quantum.Canon.ApplyIfElseRCA
title: Операция Апплифелсерка
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseRCA
qsharp.summary: Applies one of two unitary operations, depending on the value of a classical result.
ms.openlocfilehash: dfd1c16a25a2da507024813a380386c8f4e49d30
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218756"
---
# <a name="applyifelserca-operation"></a><span data-ttu-id="2ea51-102">Операция Апплифелсерка</span><span class="sxs-lookup"><span data-stu-id="2ea51-102">ApplyIfElseRCA operation</span></span>

<span data-ttu-id="2ea51-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="2ea51-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="2ea51-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2ea51-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2ea51-105">Применяет одну из двух операций в зависимости от значения классического результата.</span><span class="sxs-lookup"><span data-stu-id="2ea51-105">Applies one of two unitary operations, depending on the value of a classical result.</span></span>

```qsharp
operation ApplyIfElseRCA<'T, 'U> (result : Result, (zeroOp : ('T => Unit is Adj + Ctl), zeroInput : 'T), (oneOp : ('U => Unit is Adj + Ctl), oneInput : 'U)) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="2ea51-106">Описание</span><span class="sxs-lookup"><span data-stu-id="2ea51-106">Description</span></span>

<span data-ttu-id="2ea51-107">Учитывая результат `result` , применяет операцию `zeroOp` с в `zeroInput` качестве входных данных, если равен `result` `Zero` , и применяется, `oneOp(oneInput)` когда `result == One` .</span><span class="sxs-lookup"><span data-stu-id="2ea51-107">Given a result `result`, applies the operation `zeroOp` with `zeroInput` as its input when `result` is equal to `Zero`, and applies `oneOp(oneInput)` when `result == One`.</span></span>

## <a name="input"></a><span data-ttu-id="2ea51-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2ea51-108">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="2ea51-109">результат: __недопустимо <Result>__</span><span class="sxs-lookup"><span data-stu-id="2ea51-109">result : __invalid<Result>__</span></span>

<span data-ttu-id="2ea51-110">Результат измерения, используемый для определения `zeroOp` применения или `oneOp` .</span><span class="sxs-lookup"><span data-stu-id="2ea51-110">The measurement result used to determine if `zeroOp` or `oneOp` is applied.</span></span>


### <a name="zeroop--t--unit--is-adj--ctl"></a><span data-ttu-id="2ea51-111">Зеруп: не>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="2ea51-111">zeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="2ea51-112">Единая операция, применяемая при `result == Zero` .</span><span class="sxs-lookup"><span data-stu-id="2ea51-112">The unitary operation to be applied when `result == Zero`.</span></span>


### <a name="zeroinput--t"></a><span data-ttu-id="2ea51-113">Зероинпут: 'T</span><span class="sxs-lookup"><span data-stu-id="2ea51-113">zeroInput : 'T</span></span>

<span data-ttu-id="2ea51-114">Входные данные, которые должны быть предоставлены в `zeroOp` when `result == Zero` .</span><span class="sxs-lookup"><span data-stu-id="2ea51-114">The input to be provided to `zeroOp` when `result == Zero`.</span></span>


### <a name="oneop--u--unit--is-adj--ctl"></a><span data-ttu-id="2ea51-115">Онеоп: "U => [единицей](xref:microsoft.quantum.lang-ref.unit)  является список" года + CTL "</span><span class="sxs-lookup"><span data-stu-id="2ea51-115">oneOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="2ea51-116">Единая операция, применяемая при `result == One` .</span><span class="sxs-lookup"><span data-stu-id="2ea51-116">The unitary operation to be applied when `result == One`.</span></span>


### <a name="oneinput--u"></a><span data-ttu-id="2ea51-117">Онеинпут: ' U</span><span class="sxs-lookup"><span data-stu-id="2ea51-117">oneInput : 'U</span></span>

<span data-ttu-id="2ea51-118">Входные данные, которые должны быть предоставлены в `oneOp` when `result == One` .</span><span class="sxs-lookup"><span data-stu-id="2ea51-118">The input to be provided to `oneOp` when `result == One`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2ea51-119">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2ea51-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="2ea51-120">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="2ea51-120">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2ea51-121">Е</span><span class="sxs-lookup"><span data-stu-id="2ea51-121">'T</span></span>

<span data-ttu-id="2ea51-122">Тип входных данных операции `zeroOp` , которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="2ea51-122">The input type of the operation `zeroOp` to be conditionally applied.</span></span>
### <a name="u"></a><span data-ttu-id="2ea51-123">' U</span><span class="sxs-lookup"><span data-stu-id="2ea51-123">'U</span></span>

<span data-ttu-id="2ea51-124">Тип входных данных операции `oneOp` , которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="2ea51-124">The input type of the operation `oneOp` to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="2ea51-125">См. также:</span><span class="sxs-lookup"><span data-stu-id="2ea51-125">See Also</span></span>

- [<span data-ttu-id="2ea51-126">Microsoft. тактов. Canon. Апплифзеро</span><span class="sxs-lookup"><span data-stu-id="2ea51-126">Microsoft.Quantum.Canon.ApplyIfZero</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZero)
- [<span data-ttu-id="2ea51-127">Microsoft. тактов. Canon. Апплифоне</span><span class="sxs-lookup"><span data-stu-id="2ea51-127">Microsoft.Quantum.Canon.ApplyIfOne</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- [<span data-ttu-id="2ea51-128">Microsoft. тактов. Canon. Апплифелсерк</span><span class="sxs-lookup"><span data-stu-id="2ea51-128">Microsoft.Quantum.Canon.ApplyIfElseRC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRC)
- [<span data-ttu-id="2ea51-129">Microsoft. тактов. Canon. Апплифелсера</span><span class="sxs-lookup"><span data-stu-id="2ea51-129">Microsoft.Quantum.Canon.ApplyIfElseRA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRA)
- [<span data-ttu-id="2ea51-130">Microsoft. тактов. Canon. Апплифелсерка</span><span class="sxs-lookup"><span data-stu-id="2ea51-130">Microsoft.Quantum.Canon.ApplyIfElseRCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRCA)