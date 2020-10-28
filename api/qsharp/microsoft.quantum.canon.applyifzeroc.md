---
uid: Microsoft.Quantum.Canon.ApplyIfZeroC
title: Операция Апплифзерок
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfZeroC
qsharp.summary: Applies a controllable operation conditioned on a classical result value being zero.
ms.openlocfilehash: cfc2a659f4da011baadff1a0d6a20a2a36d0a285
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718015"
---
# <a name="applyifzeroc-operation"></a><span data-ttu-id="35a30-102">Операция Апплифзерок</span><span class="sxs-lookup"><span data-stu-id="35a30-102">ApplyIfZeroC operation</span></span>

<span data-ttu-id="35a30-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="35a30-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="35a30-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="35a30-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="35a30-105">Применяет управляемую операцию, заданную для классического результирующего значения, равного нулю.</span><span class="sxs-lookup"><span data-stu-id="35a30-105">Applies a controllable operation conditioned on a classical result value being zero.</span></span>

```qsharp
operation ApplyIfZeroC<'T> (result : Result, (op : ('T => Unit is Ctl), target : 'T)) : Unit
```


## <a name="description"></a><span data-ttu-id="35a30-106">Описание</span><span class="sxs-lookup"><span data-stu-id="35a30-106">Description</span></span>

<span data-ttu-id="35a30-107">При наличии операции `op` и результирующего значения `result` применяется `op` к, `target` Если имеет `result` значение `Zero` .</span><span class="sxs-lookup"><span data-stu-id="35a30-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `Zero`.</span></span> <span data-ttu-id="35a30-108">Если значение `One` равно, то ничего не происходит с `target` .</span><span class="sxs-lookup"><span data-stu-id="35a30-108">If `One`, nothing happens to the `target`.</span></span>
<span data-ttu-id="35a30-109">Суффикс `C` указывает, что операция, которая должна быть применена, является управляемой.</span><span class="sxs-lookup"><span data-stu-id="35a30-109">The suffix `C` indicates that the operation to be applied is controllable.</span></span>

## <a name="input"></a><span data-ttu-id="35a30-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="35a30-110">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="35a30-111">результат: __недопустимо <Result>__</span><span class="sxs-lookup"><span data-stu-id="35a30-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="35a30-112">Результат измерения, определяющий, применяется ли оператор Op.</span><span class="sxs-lookup"><span data-stu-id="35a30-112">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit-ctl"></a><span data-ttu-id="35a30-113">Op: 'T => [единицы](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="35a30-113">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="35a30-114">Операция, применяемая к условию.</span><span class="sxs-lookup"><span data-stu-id="35a30-114">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="35a30-115">Целевой объект: 'T</span><span class="sxs-lookup"><span data-stu-id="35a30-115">target : 'T</span></span>

<span data-ttu-id="35a30-116">Входные данные, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="35a30-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="35a30-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="35a30-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="35a30-118">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="35a30-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="35a30-119">Е</span><span class="sxs-lookup"><span data-stu-id="35a30-119">'T</span></span>

<span data-ttu-id="35a30-120">Тип входных данных операции, которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="35a30-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="35a30-121">См. также:</span><span class="sxs-lookup"><span data-stu-id="35a30-121">See Also</span></span>

- [<span data-ttu-id="35a30-122">Microsoft. тактов. Canon. Апплифзерок</span><span class="sxs-lookup"><span data-stu-id="35a30-122">Microsoft.Quantum.Canon.ApplyIfZeroC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroC)
- [<span data-ttu-id="35a30-123">Microsoft. тактов. Canon. Апплифзероа</span><span class="sxs-lookup"><span data-stu-id="35a30-123">Microsoft.Quantum.Canon.ApplyIfZeroA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroA)
- [<span data-ttu-id="35a30-124">Microsoft. тактов. Canon. Апплифзерока</span><span class="sxs-lookup"><span data-stu-id="35a30-124">Microsoft.Quantum.Canon.ApplyIfZeroCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroCA)