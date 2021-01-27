---
uid: Microsoft.Quantum.Canon.ApplyIfZeroC
title: Операция Апплифзерок
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfZeroC
qsharp.summary: Applies a controllable operation conditioned on a classical result value being zero.
ms.openlocfilehash: 3876e2baf1b3ad5bbfa0097d468b1e88adf05db4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841721"
---
# <a name="applyifzeroc-operation"></a><span data-ttu-id="a171e-102">Операция Апплифзерок</span><span class="sxs-lookup"><span data-stu-id="a171e-102">ApplyIfZeroC operation</span></span>

<span data-ttu-id="a171e-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a171e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a171e-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a171e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a171e-105">Применяет управляемую операцию, заданную для классического результирующего значения, равного нулю.</span><span class="sxs-lookup"><span data-stu-id="a171e-105">Applies a controllable operation conditioned on a classical result value being zero.</span></span>

```qsharp
operation ApplyIfZeroC<'T> (result : Result, (op : ('T => Unit is Ctl), target : 'T)) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="a171e-106">Описание</span><span class="sxs-lookup"><span data-stu-id="a171e-106">Description</span></span>

<span data-ttu-id="a171e-107">При наличии операции `op` и результирующего значения `result` применяется `op` к, `target` Если имеет `result` значение `Zero` .</span><span class="sxs-lookup"><span data-stu-id="a171e-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `Zero`.</span></span> <span data-ttu-id="a171e-108">Если значение `One` равно, то ничего не происходит с `target` .</span><span class="sxs-lookup"><span data-stu-id="a171e-108">If `One`, nothing happens to the `target`.</span></span>
<span data-ttu-id="a171e-109">Суффикс `C` указывает, что операция, которая должна быть применена, является управляемой.</span><span class="sxs-lookup"><span data-stu-id="a171e-109">The suffix `C` indicates that the operation to be applied is controllable.</span></span>

## <a name="input"></a><span data-ttu-id="a171e-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a171e-110">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="a171e-111">результат: __недопустимо <Result>__</span><span class="sxs-lookup"><span data-stu-id="a171e-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="a171e-112">Результат измерения, определяющий, применяется ли оператор Op.</span><span class="sxs-lookup"><span data-stu-id="a171e-112">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="a171e-113">Op: не>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — CTL</span><span class="sxs-lookup"><span data-stu-id="a171e-113">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="a171e-114">Операция, применяемая к условию.</span><span class="sxs-lookup"><span data-stu-id="a171e-114">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="a171e-115">Целевой объект: 'T</span><span class="sxs-lookup"><span data-stu-id="a171e-115">target : 'T</span></span>

<span data-ttu-id="a171e-116">Входные данные, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="a171e-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a171e-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a171e-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="a171e-118">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="a171e-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a171e-119">Е</span><span class="sxs-lookup"><span data-stu-id="a171e-119">'T</span></span>

<span data-ttu-id="a171e-120">Тип входных данных операции, которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="a171e-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="a171e-121">См. также:</span><span class="sxs-lookup"><span data-stu-id="a171e-121">See Also</span></span>

- [<span data-ttu-id="a171e-122">Microsoft. тактов. Canon. Апплифзерок</span><span class="sxs-lookup"><span data-stu-id="a171e-122">Microsoft.Quantum.Canon.ApplyIfZeroC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroC)
- [<span data-ttu-id="a171e-123">Microsoft. тактов. Canon. Апплифзероа</span><span class="sxs-lookup"><span data-stu-id="a171e-123">Microsoft.Quantum.Canon.ApplyIfZeroA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroA)
- [<span data-ttu-id="a171e-124">Microsoft. тактов. Canon. Апплифзерока</span><span class="sxs-lookup"><span data-stu-id="a171e-124">Microsoft.Quantum.Canon.ApplyIfZeroCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroCA)