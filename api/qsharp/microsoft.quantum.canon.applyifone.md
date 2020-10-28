---
uid: Microsoft.Quantum.Canon.ApplyIfOne
title: Операция Апплифоне
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfOne
qsharp.summary: Applies an operation conditioned on a classical result value being one.
ms.openlocfilehash: 8c668423d126f02736bcb541e73e210a761c5719
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718100"
---
# <a name="applyifone-operation"></a><span data-ttu-id="83dfd-102">Операция Апплифоне</span><span class="sxs-lookup"><span data-stu-id="83dfd-102">ApplyIfOne operation</span></span>

<span data-ttu-id="83dfd-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="83dfd-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="83dfd-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="83dfd-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="83dfd-105">Применяет операцию с условием для классического значения результата, равного одному.</span><span class="sxs-lookup"><span data-stu-id="83dfd-105">Applies an operation conditioned on a classical result value being one.</span></span>

```qsharp
operation ApplyIfOne<'T> (result : Result, (op : ('T => Unit), target : 'T)) : Unit
```


## <a name="description"></a><span data-ttu-id="83dfd-106">Описание</span><span class="sxs-lookup"><span data-stu-id="83dfd-106">Description</span></span>

<span data-ttu-id="83dfd-107">При наличии операции `op` и результирующего значения `result` применяется `op` к, `target` Если имеет `result` значение `One` .</span><span class="sxs-lookup"><span data-stu-id="83dfd-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `One`.</span></span> <span data-ttu-id="83dfd-108">Если значение `Zero` равно, то ничего не происходит с `target` .</span><span class="sxs-lookup"><span data-stu-id="83dfd-108">If `Zero`, nothing happens to the `target`.</span></span>

## <a name="input"></a><span data-ttu-id="83dfd-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="83dfd-109">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="83dfd-110">результат: __недопустимо <Result>__</span><span class="sxs-lookup"><span data-stu-id="83dfd-110">result : __invalid<Result>__</span></span>

<span data-ttu-id="83dfd-111">Результат измерения, определяющий, применяется ли оператор Op.</span><span class="sxs-lookup"><span data-stu-id="83dfd-111">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit"></a><span data-ttu-id="83dfd-112">Op: t = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="83dfd-112">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="83dfd-113">Операция, применяемая к условию.</span><span class="sxs-lookup"><span data-stu-id="83dfd-113">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="83dfd-114">Целевой объект: 'T</span><span class="sxs-lookup"><span data-stu-id="83dfd-114">target : 'T</span></span>

<span data-ttu-id="83dfd-115">Входные данные, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="83dfd-115">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="83dfd-116">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="83dfd-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="83dfd-117">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="83dfd-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="83dfd-118">Е</span><span class="sxs-lookup"><span data-stu-id="83dfd-118">'T</span></span>

<span data-ttu-id="83dfd-119">Тип входных данных операции, которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="83dfd-119">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="83dfd-120">См. также:</span><span class="sxs-lookup"><span data-stu-id="83dfd-120">See Also</span></span>

- [<span data-ttu-id="83dfd-121">Microsoft. тактов. Canon. Апплифонек</span><span class="sxs-lookup"><span data-stu-id="83dfd-121">Microsoft.Quantum.Canon.ApplyIfOneC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneC)
- [<span data-ttu-id="83dfd-122">Microsoft. тактов. Canon. Апплифонеа</span><span class="sxs-lookup"><span data-stu-id="83dfd-122">Microsoft.Quantum.Canon.ApplyIfOneA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneA)
- [<span data-ttu-id="83dfd-123">Microsoft. тактов. Canon. Апплифонека</span><span class="sxs-lookup"><span data-stu-id="83dfd-123">Microsoft.Quantum.Canon.ApplyIfOneCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneCA)