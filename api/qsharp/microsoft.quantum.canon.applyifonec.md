---
uid: Microsoft.Quantum.Canon.ApplyIfOneC
title: Операция Апплифонек
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfOneC
qsharp.summary: Applies a controllable operation conditioned on a classical result value being one.
ms.openlocfilehash: 24a00d83c1bbe6b07adb27c58fc70bc76af0a910
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209424"
---
# <a name="applyifonec-operation"></a><span data-ttu-id="2ee11-102">Операция Апплифонек</span><span class="sxs-lookup"><span data-stu-id="2ee11-102">ApplyIfOneC operation</span></span>

<span data-ttu-id="2ee11-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="2ee11-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="2ee11-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2ee11-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2ee11-105">Применяет управляемую операцию с условием для классического значения result.</span><span class="sxs-lookup"><span data-stu-id="2ee11-105">Applies a controllable operation conditioned on a classical result value being one.</span></span>

```qsharp
operation ApplyIfOneC<'T> (result : Result, (op : ('T => Unit is Ctl), target : 'T)) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="2ee11-106">Описание</span><span class="sxs-lookup"><span data-stu-id="2ee11-106">Description</span></span>

<span data-ttu-id="2ee11-107">При наличии операции `op` и результирующего значения `result` применяется `op` к, `target` Если имеет `result` значение `One` .</span><span class="sxs-lookup"><span data-stu-id="2ee11-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `One`.</span></span> <span data-ttu-id="2ee11-108">Если значение `Zero` равно, то ничего не происходит с `target` .</span><span class="sxs-lookup"><span data-stu-id="2ee11-108">If `Zero`, nothing happens to the `target`.</span></span>
<span data-ttu-id="2ee11-109">Суффикс `C` указывает, что операция, которая должна быть применена, является управляемой.</span><span class="sxs-lookup"><span data-stu-id="2ee11-109">The suffix `C` indicates that the operation to be applied is controllable.</span></span>

## <a name="input"></a><span data-ttu-id="2ee11-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2ee11-110">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="2ee11-111">результат: __недопустимо <Result>__</span><span class="sxs-lookup"><span data-stu-id="2ee11-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="2ee11-112">Результат измерения, определяющий, применяется ли оператор Op.</span><span class="sxs-lookup"><span data-stu-id="2ee11-112">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="2ee11-113">Op: не>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — CTL</span><span class="sxs-lookup"><span data-stu-id="2ee11-113">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="2ee11-114">Операция, применяемая к условию.</span><span class="sxs-lookup"><span data-stu-id="2ee11-114">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="2ee11-115">Целевой объект: 'T</span><span class="sxs-lookup"><span data-stu-id="2ee11-115">target : 'T</span></span>

<span data-ttu-id="2ee11-116">Входные данные, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="2ee11-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2ee11-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2ee11-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="2ee11-118">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="2ee11-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2ee11-119">Е</span><span class="sxs-lookup"><span data-stu-id="2ee11-119">'T</span></span>

<span data-ttu-id="2ee11-120">Тип входных данных операции, которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="2ee11-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="2ee11-121">См. также:</span><span class="sxs-lookup"><span data-stu-id="2ee11-121">See Also</span></span>

- [<span data-ttu-id="2ee11-122">Microsoft. тактов. Canon. Апплифонек</span><span class="sxs-lookup"><span data-stu-id="2ee11-122">Microsoft.Quantum.Canon.ApplyIfOneC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneC)
- [<span data-ttu-id="2ee11-123">Microsoft. тактов. Canon. Апплифонеа</span><span class="sxs-lookup"><span data-stu-id="2ee11-123">Microsoft.Quantum.Canon.ApplyIfOneA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneA)
- [<span data-ttu-id="2ee11-124">Microsoft. тактов. Canon. Апплифонека</span><span class="sxs-lookup"><span data-stu-id="2ee11-124">Microsoft.Quantum.Canon.ApplyIfOneCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneCA)