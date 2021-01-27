---
uid: Microsoft.Quantum.Canon.ApplyIfOneC
title: Операция Апплифонек
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfOneC
qsharp.summary: Applies a controllable operation conditioned on a classical result value being one.
ms.openlocfilehash: ebeec5b46567892ad30f194ababb42876ba08bcb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841753"
---
# <a name="applyifonec-operation"></a><span data-ttu-id="f7fd8-102">Операция Апплифонек</span><span class="sxs-lookup"><span data-stu-id="f7fd8-102">ApplyIfOneC operation</span></span>

<span data-ttu-id="f7fd8-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f7fd8-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f7fd8-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f7fd8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f7fd8-105">Применяет управляемую операцию с условием для классического значения result.</span><span class="sxs-lookup"><span data-stu-id="f7fd8-105">Applies a controllable operation conditioned on a classical result value being one.</span></span>

```qsharp
operation ApplyIfOneC<'T> (result : Result, (op : ('T => Unit is Ctl), target : 'T)) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="f7fd8-106">Описание</span><span class="sxs-lookup"><span data-stu-id="f7fd8-106">Description</span></span>

<span data-ttu-id="f7fd8-107">При наличии операции `op` и результирующего значения `result` применяется `op` к, `target` Если имеет `result` значение `One` .</span><span class="sxs-lookup"><span data-stu-id="f7fd8-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `One`.</span></span> <span data-ttu-id="f7fd8-108">Если значение `Zero` равно, то ничего не происходит с `target` .</span><span class="sxs-lookup"><span data-stu-id="f7fd8-108">If `Zero`, nothing happens to the `target`.</span></span>
<span data-ttu-id="f7fd8-109">Суффикс `C` указывает, что операция, которая должна быть применена, является управляемой.</span><span class="sxs-lookup"><span data-stu-id="f7fd8-109">The suffix `C` indicates that the operation to be applied is controllable.</span></span>

## <a name="input"></a><span data-ttu-id="f7fd8-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f7fd8-110">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="f7fd8-111">результат: __недопустимо <Result>__</span><span class="sxs-lookup"><span data-stu-id="f7fd8-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="f7fd8-112">Результат измерения, определяющий, применяется ли оператор Op.</span><span class="sxs-lookup"><span data-stu-id="f7fd8-112">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="f7fd8-113">Op: не>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — CTL</span><span class="sxs-lookup"><span data-stu-id="f7fd8-113">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="f7fd8-114">Операция, применяемая к условию.</span><span class="sxs-lookup"><span data-stu-id="f7fd8-114">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="f7fd8-115">Целевой объект: 'T</span><span class="sxs-lookup"><span data-stu-id="f7fd8-115">target : 'T</span></span>

<span data-ttu-id="f7fd8-116">Входные данные, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="f7fd8-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f7fd8-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f7fd8-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f7fd8-118">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="f7fd8-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f7fd8-119">Е</span><span class="sxs-lookup"><span data-stu-id="f7fd8-119">'T</span></span>

<span data-ttu-id="f7fd8-120">Тип входных данных операции, которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="f7fd8-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="f7fd8-121">См. также:</span><span class="sxs-lookup"><span data-stu-id="f7fd8-121">See Also</span></span>

- [<span data-ttu-id="f7fd8-122">Microsoft. тактов. Canon. Апплифонек</span><span class="sxs-lookup"><span data-stu-id="f7fd8-122">Microsoft.Quantum.Canon.ApplyIfOneC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneC)
- [<span data-ttu-id="f7fd8-123">Microsoft. тактов. Canon. Апплифонеа</span><span class="sxs-lookup"><span data-stu-id="f7fd8-123">Microsoft.Quantum.Canon.ApplyIfOneA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneA)
- [<span data-ttu-id="f7fd8-124">Microsoft. тактов. Canon. Апплифонека</span><span class="sxs-lookup"><span data-stu-id="f7fd8-124">Microsoft.Quantum.Canon.ApplyIfOneCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneCA)