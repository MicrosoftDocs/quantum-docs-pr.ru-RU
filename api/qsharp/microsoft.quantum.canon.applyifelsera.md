---
uid: Microsoft.Quantum.Canon.ApplyIfElseRA
title: Операция Апплифелсера
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseRA
qsharp.summary: Applies one of two adjointable operations, depending on the value of a classical result.
ms.openlocfilehash: d0181d98a9867f71d8a8f8dea4331e5a13f9e59c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718142"
---
# <a name="applyifelsera-operation"></a><span data-ttu-id="23eb3-102">Операция Апплифелсера</span><span class="sxs-lookup"><span data-stu-id="23eb3-102">ApplyIfElseRA operation</span></span>

<span data-ttu-id="23eb3-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="23eb3-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="23eb3-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="23eb3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="23eb3-105">Применяет одну из двух операций аджоинтабле в зависимости от значения классического результата.</span><span class="sxs-lookup"><span data-stu-id="23eb3-105">Applies one of two adjointable operations, depending on the value of a classical result.</span></span>

```qsharp
operation ApplyIfElseRA<'T, 'U> (result : Result, (zeroOp : ('T => Unit is Adj), zeroInput : 'T), (oneOp : ('U => Unit is Adj), oneInput : 'U)) : Unit
```


## <a name="description"></a><span data-ttu-id="23eb3-106">Описание</span><span class="sxs-lookup"><span data-stu-id="23eb3-106">Description</span></span>

<span data-ttu-id="23eb3-107">Учитывая результат `result` , применяет операцию `zeroOp` с в `zeroInput` качестве входных данных, если равен `result` `Zero` , и применяется, `oneOp(oneInput)` когда `result == One` .</span><span class="sxs-lookup"><span data-stu-id="23eb3-107">Given a result `result`, applies the operation `zeroOp` with `zeroInput` as its input when `result` is equal to `Zero`, and applies `oneOp(oneInput)` when `result == One`.</span></span>

## <a name="input"></a><span data-ttu-id="23eb3-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="23eb3-108">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="23eb3-109">результат: __недопустимо <Result>__</span><span class="sxs-lookup"><span data-stu-id="23eb3-109">result : __invalid<Result>__</span></span>

<span data-ttu-id="23eb3-110">Результат измерения, используемый для определения `zeroOp` применения или `oneOp` .</span><span class="sxs-lookup"><span data-stu-id="23eb3-110">The measurement result used to determine if `zeroOp` or `oneOp` is applied.</span></span>


### <a name="zeroop--t--unit-adj"></a><span data-ttu-id="23eb3-111">Зеруп: 'T [=>ное](xref:microsoft.quantum.lang-ref.unit) прогода</span><span class="sxs-lookup"><span data-stu-id="23eb3-111">zeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="23eb3-112">Операция аджоинтабле, применяемая при `result == Zero` .</span><span class="sxs-lookup"><span data-stu-id="23eb3-112">The adjointable operation to be applied when `result == Zero`.</span></span>


### <a name="zeroinput--t"></a><span data-ttu-id="23eb3-113">Зероинпут: 'T</span><span class="sxs-lookup"><span data-stu-id="23eb3-113">zeroInput : 'T</span></span>

<span data-ttu-id="23eb3-114">Входные данные, которые должны быть предоставлены в `zeroOp` when `result == Zero` .</span><span class="sxs-lookup"><span data-stu-id="23eb3-114">The input to be provided to `zeroOp` when `result == Zero`.</span></span>


### <a name="oneop--u--unit-adj"></a><span data-ttu-id="23eb3-115">Онеоп: "U [=>ная](xref:microsoft.quantum.lang-ref.unit) прогода</span><span class="sxs-lookup"><span data-stu-id="23eb3-115">oneOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="23eb3-116">Операция аджоинтабле, применяемая при `result == One` .</span><span class="sxs-lookup"><span data-stu-id="23eb3-116">The adjointable operation to be applied when `result == One`.</span></span>


### <a name="oneinput--u"></a><span data-ttu-id="23eb3-117">Онеинпут: ' U</span><span class="sxs-lookup"><span data-stu-id="23eb3-117">oneInput : 'U</span></span>

<span data-ttu-id="23eb3-118">Входные данные, которые должны быть предоставлены в `oneOp` when `result == One` .</span><span class="sxs-lookup"><span data-stu-id="23eb3-118">The input to be provided to `oneOp` when `result == One`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="23eb3-119">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="23eb3-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="23eb3-120">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="23eb3-120">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="23eb3-121">Е</span><span class="sxs-lookup"><span data-stu-id="23eb3-121">'T</span></span>

<span data-ttu-id="23eb3-122">Тип входных данных операции `zeroOp` , которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="23eb3-122">The input type of the operation `zeroOp` to be conditionally applied.</span></span>
### <a name="u"></a><span data-ttu-id="23eb3-123">' U</span><span class="sxs-lookup"><span data-stu-id="23eb3-123">'U</span></span>

<span data-ttu-id="23eb3-124">Тип входных данных операции `oneOp` , которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="23eb3-124">The input type of the operation `oneOp` to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="23eb3-125">См. также:</span><span class="sxs-lookup"><span data-stu-id="23eb3-125">See Also</span></span>

- [<span data-ttu-id="23eb3-126">Microsoft. тактов. Canon. Апплифзеро</span><span class="sxs-lookup"><span data-stu-id="23eb3-126">Microsoft.Quantum.Canon.ApplyIfZero</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZero)
- [<span data-ttu-id="23eb3-127">Microsoft. тактов. Canon. Апплифоне</span><span class="sxs-lookup"><span data-stu-id="23eb3-127">Microsoft.Quantum.Canon.ApplyIfOne</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- [<span data-ttu-id="23eb3-128">Microsoft. тактов. Canon. Апплифелсерк</span><span class="sxs-lookup"><span data-stu-id="23eb3-128">Microsoft.Quantum.Canon.ApplyIfElseRC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRC)
- [<span data-ttu-id="23eb3-129">Microsoft. тактов. Canon. Апплифелсера</span><span class="sxs-lookup"><span data-stu-id="23eb3-129">Microsoft.Quantum.Canon.ApplyIfElseRA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRA)
- [<span data-ttu-id="23eb3-130">Microsoft. тактов. Canon. Апплифелсерка</span><span class="sxs-lookup"><span data-stu-id="23eb3-130">Microsoft.Quantum.Canon.ApplyIfElseRCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRCA)