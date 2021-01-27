---
uid: Microsoft.Quantum.Canon.ApplyIfOne
title: Операция Апплифоне
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfOne
qsharp.summary: Applies an operation conditioned on a classical result value being one.
ms.openlocfilehash: b86aecf3dc3d02d1a6bf0c112bdc45a55a2cf087
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841770"
---
# <a name="applyifone-operation"></a><span data-ttu-id="942b3-102">Операция Апплифоне</span><span class="sxs-lookup"><span data-stu-id="942b3-102">ApplyIfOne operation</span></span>

<span data-ttu-id="942b3-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="942b3-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="942b3-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="942b3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="942b3-105">Применяет операцию с условием для классического значения результата, равного одному.</span><span class="sxs-lookup"><span data-stu-id="942b3-105">Applies an operation conditioned on a classical result value being one.</span></span>

```qsharp
operation ApplyIfOne<'T> (result : Result, (op : ('T => Unit), target : 'T)) : Unit
```


## <a name="description"></a><span data-ttu-id="942b3-106">Описание</span><span class="sxs-lookup"><span data-stu-id="942b3-106">Description</span></span>

<span data-ttu-id="942b3-107">При наличии операции `op` и результирующего значения `result` применяется `op` к, `target` Если имеет `result` значение `One` .</span><span class="sxs-lookup"><span data-stu-id="942b3-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `One`.</span></span> <span data-ttu-id="942b3-108">Если значение `Zero` равно, то ничего не происходит с `target` .</span><span class="sxs-lookup"><span data-stu-id="942b3-108">If `Zero`, nothing happens to the `target`.</span></span>

## <a name="input"></a><span data-ttu-id="942b3-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="942b3-109">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="942b3-110">результат: __недопустимо <Result>__</span><span class="sxs-lookup"><span data-stu-id="942b3-110">result : __invalid<Result>__</span></span>

<span data-ttu-id="942b3-111">Результат измерения, определяющий, применяется ли оператор Op.</span><span class="sxs-lookup"><span data-stu-id="942b3-111">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit"></a><span data-ttu-id="942b3-112">Op: t = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="942b3-112">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="942b3-113">Операция, применяемая к условию.</span><span class="sxs-lookup"><span data-stu-id="942b3-113">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="942b3-114">Целевой объект: 'T</span><span class="sxs-lookup"><span data-stu-id="942b3-114">target : 'T</span></span>

<span data-ttu-id="942b3-115">Входные данные, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="942b3-115">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="942b3-116">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="942b3-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="942b3-117">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="942b3-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="942b3-118">Е</span><span class="sxs-lookup"><span data-stu-id="942b3-118">'T</span></span>

<span data-ttu-id="942b3-119">Тип входных данных операции, которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="942b3-119">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="942b3-120">См. также:</span><span class="sxs-lookup"><span data-stu-id="942b3-120">See Also</span></span>

- [<span data-ttu-id="942b3-121">Microsoft. тактов. Canon. Апплифонек</span><span class="sxs-lookup"><span data-stu-id="942b3-121">Microsoft.Quantum.Canon.ApplyIfOneC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneC)
- [<span data-ttu-id="942b3-122">Microsoft. тактов. Canon. Апплифонеа</span><span class="sxs-lookup"><span data-stu-id="942b3-122">Microsoft.Quantum.Canon.ApplyIfOneA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneA)
- [<span data-ttu-id="942b3-123">Microsoft. тактов. Canon. Апплифонека</span><span class="sxs-lookup"><span data-stu-id="942b3-123">Microsoft.Quantum.Canon.ApplyIfOneCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneCA)