---
uid: Microsoft.Quantum.Canon.ApplyIfZero
title: Операция Апплифзеро
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfZero
qsharp.summary: Applies an operation conditioned on a classical result value being zero.
ms.openlocfilehash: 215b71a8d2e4f8a22df05b210824bc40a969b6f6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841741"
---
# <a name="applyifzero-operation"></a><span data-ttu-id="6db60-102">Операция Апплифзеро</span><span class="sxs-lookup"><span data-stu-id="6db60-102">ApplyIfZero operation</span></span>

<span data-ttu-id="6db60-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="6db60-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="6db60-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6db60-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6db60-105">Применяет операцию с условием для классического значения result, равного нулю.</span><span class="sxs-lookup"><span data-stu-id="6db60-105">Applies an operation conditioned on a classical result value being zero.</span></span>

```qsharp
operation ApplyIfZero<'T> (result : Result, (op : ('T => Unit), target : 'T)) : Unit
```


## <a name="description"></a><span data-ttu-id="6db60-106">Описание</span><span class="sxs-lookup"><span data-stu-id="6db60-106">Description</span></span>

<span data-ttu-id="6db60-107">При наличии операции `op` и результирующего значения `result` применяется `op` к, `target` Если имеет `result` значение `Zero` .</span><span class="sxs-lookup"><span data-stu-id="6db60-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `Zero`.</span></span> <span data-ttu-id="6db60-108">Если значение `One` равно, то ничего не происходит с `target` .</span><span class="sxs-lookup"><span data-stu-id="6db60-108">If `One`, nothing happens to the `target`.</span></span>

## <a name="input"></a><span data-ttu-id="6db60-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="6db60-109">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="6db60-110">результат: __недопустимо <Result>__</span><span class="sxs-lookup"><span data-stu-id="6db60-110">result : __invalid<Result>__</span></span>

<span data-ttu-id="6db60-111">Результат измерения, определяющий, применяется ли оператор Op.</span><span class="sxs-lookup"><span data-stu-id="6db60-111">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit"></a><span data-ttu-id="6db60-112">Op: t = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="6db60-112">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="6db60-113">Операция, применяемая к условию.</span><span class="sxs-lookup"><span data-stu-id="6db60-113">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="6db60-114">Целевой объект: 'T</span><span class="sxs-lookup"><span data-stu-id="6db60-114">target : 'T</span></span>

<span data-ttu-id="6db60-115">Входные данные, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="6db60-115">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="6db60-116">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6db60-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="6db60-117">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="6db60-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6db60-118">Е</span><span class="sxs-lookup"><span data-stu-id="6db60-118">'T</span></span>

<span data-ttu-id="6db60-119">Тип входных данных операции, которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="6db60-119">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="6db60-120">См. также:</span><span class="sxs-lookup"><span data-stu-id="6db60-120">See Also</span></span>

- [<span data-ttu-id="6db60-121">Microsoft. тактов. Canon. Апплифзерок</span><span class="sxs-lookup"><span data-stu-id="6db60-121">Microsoft.Quantum.Canon.ApplyIfZeroC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroC)
- [<span data-ttu-id="6db60-122">Microsoft. тактов. Canon. Апплифзероа</span><span class="sxs-lookup"><span data-stu-id="6db60-122">Microsoft.Quantum.Canon.ApplyIfZeroA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroA)
- [<span data-ttu-id="6db60-123">Microsoft. тактов. Canon. Апплифзерока</span><span class="sxs-lookup"><span data-stu-id="6db60-123">Microsoft.Quantum.Canon.ApplyIfZeroCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroCA)