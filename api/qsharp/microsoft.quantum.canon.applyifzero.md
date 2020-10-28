---
uid: Microsoft.Quantum.Canon.ApplyIfZero
title: Операция Апплифзеро
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfZero
qsharp.summary: Applies an operation conditioned on a classical result value being zero.
ms.openlocfilehash: 7435150937143a8d1a67afe334b683932a9655de
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718058"
---
# <a name="applyifzero-operation"></a><span data-ttu-id="dca26-102">Операция Апплифзеро</span><span class="sxs-lookup"><span data-stu-id="dca26-102">ApplyIfZero operation</span></span>

<span data-ttu-id="dca26-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="dca26-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="dca26-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="dca26-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="dca26-105">Применяет операцию с условием для классического значения result, равного нулю.</span><span class="sxs-lookup"><span data-stu-id="dca26-105">Applies an operation conditioned on a classical result value being zero.</span></span>

```qsharp
operation ApplyIfZero<'T> (result : Result, (op : ('T => Unit), target : 'T)) : Unit
```


## <a name="description"></a><span data-ttu-id="dca26-106">Описание</span><span class="sxs-lookup"><span data-stu-id="dca26-106">Description</span></span>

<span data-ttu-id="dca26-107">При наличии операции `op` и результирующего значения `result` применяется `op` к, `target` Если имеет `result` значение `Zero` .</span><span class="sxs-lookup"><span data-stu-id="dca26-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `Zero`.</span></span> <span data-ttu-id="dca26-108">Если значение `One` равно, то ничего не происходит с `target` .</span><span class="sxs-lookup"><span data-stu-id="dca26-108">If `One`, nothing happens to the `target`.</span></span>

## <a name="input"></a><span data-ttu-id="dca26-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="dca26-109">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="dca26-110">результат: __недопустимо <Result>__</span><span class="sxs-lookup"><span data-stu-id="dca26-110">result : __invalid<Result>__</span></span>

<span data-ttu-id="dca26-111">Результат измерения, определяющий, применяется ли оператор Op.</span><span class="sxs-lookup"><span data-stu-id="dca26-111">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit"></a><span data-ttu-id="dca26-112">Op: t = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="dca26-112">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="dca26-113">Операция, применяемая к условию.</span><span class="sxs-lookup"><span data-stu-id="dca26-113">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="dca26-114">Целевой объект: 'T</span><span class="sxs-lookup"><span data-stu-id="dca26-114">target : 'T</span></span>

<span data-ttu-id="dca26-115">Входные данные, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="dca26-115">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="dca26-116">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="dca26-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="dca26-117">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="dca26-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="dca26-118">Е</span><span class="sxs-lookup"><span data-stu-id="dca26-118">'T</span></span>

<span data-ttu-id="dca26-119">Тип входных данных операции, которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="dca26-119">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="dca26-120">См. также:</span><span class="sxs-lookup"><span data-stu-id="dca26-120">See Also</span></span>

- [<span data-ttu-id="dca26-121">Microsoft. тактов. Canon. Апплифзерок</span><span class="sxs-lookup"><span data-stu-id="dca26-121">Microsoft.Quantum.Canon.ApplyIfZeroC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroC)
- [<span data-ttu-id="dca26-122">Microsoft. тактов. Canon. Апплифзероа</span><span class="sxs-lookup"><span data-stu-id="dca26-122">Microsoft.Quantum.Canon.ApplyIfZeroA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroA)
- [<span data-ttu-id="dca26-123">Microsoft. тактов. Canon. Апплифзерока</span><span class="sxs-lookup"><span data-stu-id="dca26-123">Microsoft.Quantum.Canon.ApplyIfZeroCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroCA)