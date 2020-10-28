---
uid: Microsoft.Quantum.Canon.ApplyIfOneA
title: Операция Апплифонеа
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfOneA
qsharp.summary: Applies an adjointable operation conditioned on a classical result value being one.
ms.openlocfilehash: 76c15aba6042c2801ecfe8470e82099c54ba3846
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718099"
---
# <a name="applyifonea-operation"></a><span data-ttu-id="435f7-102">Операция Апплифонеа</span><span class="sxs-lookup"><span data-stu-id="435f7-102">ApplyIfOneA operation</span></span>

<span data-ttu-id="435f7-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="435f7-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="435f7-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="435f7-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="435f7-105">Применяет операцию аджоинтабле с условием для классического значения result.</span><span class="sxs-lookup"><span data-stu-id="435f7-105">Applies an adjointable operation conditioned on a classical result value being one.</span></span>

```qsharp
operation ApplyIfOneA<'T> (result : Result, (op : ('T => Unit is Adj), target : 'T)) : Unit
```


## <a name="description"></a><span data-ttu-id="435f7-106">Описание</span><span class="sxs-lookup"><span data-stu-id="435f7-106">Description</span></span>

<span data-ttu-id="435f7-107">При наличии операции `op` и результирующего значения `result` применяется `op` к, `target` Если имеет `result` значение `One` .</span><span class="sxs-lookup"><span data-stu-id="435f7-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `One`.</span></span> <span data-ttu-id="435f7-108">Если значение `Zero` равно, то ничего не происходит с `target` .</span><span class="sxs-lookup"><span data-stu-id="435f7-108">If `Zero`, nothing happens to the `target`.</span></span>
<span data-ttu-id="435f7-109">Суффикс `A` указывает, что операция, которую необходимо применить, — аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="435f7-109">The suffix `A` indicates that the operation to be applied is adjointable.</span></span>

## <a name="input"></a><span data-ttu-id="435f7-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="435f7-110">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="435f7-111">результат: __недопустимо <Result>__</span><span class="sxs-lookup"><span data-stu-id="435f7-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="435f7-112">Результат измерения, определяющий, применяется ли оператор Op.</span><span class="sxs-lookup"><span data-stu-id="435f7-112">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit-adj"></a><span data-ttu-id="435f7-113">Op: 'T => [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="435f7-113">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="435f7-114">Операция, применяемая к условию.</span><span class="sxs-lookup"><span data-stu-id="435f7-114">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="435f7-115">Целевой объект: 'T</span><span class="sxs-lookup"><span data-stu-id="435f7-115">target : 'T</span></span>

<span data-ttu-id="435f7-116">Входные данные, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="435f7-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="435f7-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="435f7-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="435f7-118">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="435f7-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="435f7-119">Е</span><span class="sxs-lookup"><span data-stu-id="435f7-119">'T</span></span>

<span data-ttu-id="435f7-120">Тип входных данных операции, которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="435f7-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="435f7-121">См. также:</span><span class="sxs-lookup"><span data-stu-id="435f7-121">See Also</span></span>

- [<span data-ttu-id="435f7-122">Microsoft. тактов. Canon. Апплифонек</span><span class="sxs-lookup"><span data-stu-id="435f7-122">Microsoft.Quantum.Canon.ApplyIfOneC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneC)
- [<span data-ttu-id="435f7-123">Microsoft. тактов. Canon. Апплифонеа</span><span class="sxs-lookup"><span data-stu-id="435f7-123">Microsoft.Quantum.Canon.ApplyIfOneA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneA)
- [<span data-ttu-id="435f7-124">Microsoft. тактов. Canon. Апплифонека</span><span class="sxs-lookup"><span data-stu-id="435f7-124">Microsoft.Quantum.Canon.ApplyIfOneCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneCA)