---
uid: Microsoft.Quantum.Canon.ApplyIfOneCA
title: Операция Апплифонека
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfOneCA
qsharp.summary: Applies a unitary operation conditioned on a classical result value being one.
ms.openlocfilehash: 29801ed0bec08d0ab818f237feb17c2a2a7af1e4
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218586"
---
# <a name="applyifoneca-operation"></a><span data-ttu-id="87e5f-102">Операция Апплифонека</span><span class="sxs-lookup"><span data-stu-id="87e5f-102">ApplyIfOneCA operation</span></span>

<span data-ttu-id="87e5f-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="87e5f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="87e5f-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="87e5f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="87e5f-105">Применяет единую операцию с условием для классического результирующего значения One.</span><span class="sxs-lookup"><span data-stu-id="87e5f-105">Applies a unitary operation conditioned on a classical result value being one.</span></span>

```qsharp
operation ApplyIfOneCA<'T> (result : Result, (op : ('T => Unit is Adj + Ctl), target : 'T)) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="87e5f-106">Описание</span><span class="sxs-lookup"><span data-stu-id="87e5f-106">Description</span></span>

<span data-ttu-id="87e5f-107">При наличии операции `op` и результирующего значения `result` применяется `op` к, `target` Если имеет `result` значение `One` .</span><span class="sxs-lookup"><span data-stu-id="87e5f-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `One`.</span></span> <span data-ttu-id="87e5f-108">Если значение `Zero` равно, то ничего не происходит с `target` .</span><span class="sxs-lookup"><span data-stu-id="87e5f-108">If `Zero`, nothing happens to the `target`.</span></span>
<span data-ttu-id="87e5f-109">Суффикс `CA` указывает, что применяемая операция является единой (управляемой и аджоинтабле).</span><span class="sxs-lookup"><span data-stu-id="87e5f-109">The suffix `CA` indicates that the operation to be applied is unitary (controllable and adjointable).</span></span>

## <a name="input"></a><span data-ttu-id="87e5f-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="87e5f-110">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="87e5f-111">результат: __недопустимо <Result>__</span><span class="sxs-lookup"><span data-stu-id="87e5f-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="87e5f-112">Результат измерения, определяющий, применяется ли оператор Op.</span><span class="sxs-lookup"><span data-stu-id="87e5f-112">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="87e5f-113">Op: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="87e5f-113">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="87e5f-114">Операция, применяемая к условию.</span><span class="sxs-lookup"><span data-stu-id="87e5f-114">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="87e5f-115">Целевой объект: 'T</span><span class="sxs-lookup"><span data-stu-id="87e5f-115">target : 'T</span></span>

<span data-ttu-id="87e5f-116">Входные данные, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="87e5f-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="87e5f-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="87e5f-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="87e5f-118">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="87e5f-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="87e5f-119">Е</span><span class="sxs-lookup"><span data-stu-id="87e5f-119">'T</span></span>

<span data-ttu-id="87e5f-120">Тип входных данных операции, которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="87e5f-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="87e5f-121">См. также:</span><span class="sxs-lookup"><span data-stu-id="87e5f-121">See Also</span></span>

- [<span data-ttu-id="87e5f-122">Microsoft. тактов. Canon. Апплифонек</span><span class="sxs-lookup"><span data-stu-id="87e5f-122">Microsoft.Quantum.Canon.ApplyIfOneC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneC)
- [<span data-ttu-id="87e5f-123">Microsoft. тактов. Canon. Апплифонеа</span><span class="sxs-lookup"><span data-stu-id="87e5f-123">Microsoft.Quantum.Canon.ApplyIfOneA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneA)
- [<span data-ttu-id="87e5f-124">Microsoft. тактов. Canon. Апплифонека</span><span class="sxs-lookup"><span data-stu-id="87e5f-124">Microsoft.Quantum.Canon.ApplyIfOneCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneCA)