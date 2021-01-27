---
uid: Microsoft.Quantum.Canon.ApplyIfOneA
title: Операция Апплифонеа
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfOneA
qsharp.summary: Applies an adjointable operation conditioned on a classical result value being one.
ms.openlocfilehash: 1593f565e950a9410df0ae9de59e6d0e6a7b99b0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844926"
---
# <a name="applyifonea-operation"></a><span data-ttu-id="965d3-102">Операция Апплифонеа</span><span class="sxs-lookup"><span data-stu-id="965d3-102">ApplyIfOneA operation</span></span>

<span data-ttu-id="965d3-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="965d3-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="965d3-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="965d3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="965d3-105">Применяет операцию аджоинтабле с условием для классического значения result.</span><span class="sxs-lookup"><span data-stu-id="965d3-105">Applies an adjointable operation conditioned on a classical result value being one.</span></span>

```qsharp
operation ApplyIfOneA<'T> (result : Result, (op : ('T => Unit is Adj), target : 'T)) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="965d3-106">Описание</span><span class="sxs-lookup"><span data-stu-id="965d3-106">Description</span></span>

<span data-ttu-id="965d3-107">При наличии операции `op` и результирующего значения `result` применяется `op` к, `target` Если имеет `result` значение `One` .</span><span class="sxs-lookup"><span data-stu-id="965d3-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `One`.</span></span> <span data-ttu-id="965d3-108">Если значение `Zero` равно, то ничего не происходит с `target` .</span><span class="sxs-lookup"><span data-stu-id="965d3-108">If `Zero`, nothing happens to the `target`.</span></span>
<span data-ttu-id="965d3-109">Суффикс `A` указывает, что операция, которую необходимо применить, — аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="965d3-109">The suffix `A` indicates that the operation to be applied is adjointable.</span></span>

## <a name="input"></a><span data-ttu-id="965d3-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="965d3-110">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="965d3-111">результат: __недопустимо <Result>__</span><span class="sxs-lookup"><span data-stu-id="965d3-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="965d3-112">Результат измерения, определяющий, применяется ли оператор Op.</span><span class="sxs-lookup"><span data-stu-id="965d3-112">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit--is-adj"></a><span data-ttu-id="965d3-113">Op: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  является просуммой</span><span class="sxs-lookup"><span data-stu-id="965d3-113">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="965d3-114">Операция, применяемая к условию.</span><span class="sxs-lookup"><span data-stu-id="965d3-114">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="965d3-115">Целевой объект: 'T</span><span class="sxs-lookup"><span data-stu-id="965d3-115">target : 'T</span></span>

<span data-ttu-id="965d3-116">Входные данные, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="965d3-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="965d3-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="965d3-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="965d3-118">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="965d3-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="965d3-119">Е</span><span class="sxs-lookup"><span data-stu-id="965d3-119">'T</span></span>

<span data-ttu-id="965d3-120">Тип входных данных операции, которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="965d3-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="965d3-121">См. также:</span><span class="sxs-lookup"><span data-stu-id="965d3-121">See Also</span></span>

- [<span data-ttu-id="965d3-122">Microsoft. тактов. Canon. Апплифонек</span><span class="sxs-lookup"><span data-stu-id="965d3-122">Microsoft.Quantum.Canon.ApplyIfOneC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneC)
- [<span data-ttu-id="965d3-123">Microsoft. тактов. Canon. Апплифонеа</span><span class="sxs-lookup"><span data-stu-id="965d3-123">Microsoft.Quantum.Canon.ApplyIfOneA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneA)
- [<span data-ttu-id="965d3-124">Microsoft. тактов. Canon. Апплифонека</span><span class="sxs-lookup"><span data-stu-id="965d3-124">Microsoft.Quantum.Canon.ApplyIfOneCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneCA)