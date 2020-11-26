---
uid: Microsoft.Quantum.Canon.ApplyIfCA
title: Операция Апплифка
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfCA
qsharp.summary: Applies a unitary operation conditioned on a classical bit.
ms.openlocfilehash: b0ac469d6dea51951e0d9b2cfceb54253d4b4c5d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209627"
---
# <a name="applyifca-operation"></a><span data-ttu-id="bbfcd-102">Операция Апплифка</span><span class="sxs-lookup"><span data-stu-id="bbfcd-102">ApplyIfCA operation</span></span>

<span data-ttu-id="bbfcd-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="bbfcd-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="bbfcd-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bbfcd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bbfcd-105">Применяет единую операцию с условием на Классический бит.</span><span class="sxs-lookup"><span data-stu-id="bbfcd-105">Applies a unitary operation conditioned on a classical bit.</span></span>

```qsharp
operation ApplyIfCA<'T> (op : ('T => Unit is Ctl + Adj), bit : Bool, target : 'T) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="bbfcd-106">Описание</span><span class="sxs-lookup"><span data-stu-id="bbfcd-106">Description</span></span>

<span data-ttu-id="bbfcd-107">При наличии операции `op` и битового значения `bit` применяется `op` к, `target` Если имеет `bit` значение `true` .</span><span class="sxs-lookup"><span data-stu-id="bbfcd-107">Given an operation `op` and a bit value `bit`, applies `op` to the `target` if `bit` is `true`.</span></span> <span data-ttu-id="bbfcd-108">Если значение `false` равно, то ничего не происходит с `target` .</span><span class="sxs-lookup"><span data-stu-id="bbfcd-108">If `false`, nothing happens to the `target`.</span></span>
<span data-ttu-id="bbfcd-109">Суффикс `CA` указывает, что применяемая операция является единой (управляемой и аджоинтабле).</span><span class="sxs-lookup"><span data-stu-id="bbfcd-109">The suffix `CA` indicates that the operation to be applied is unitary (controllable and adjointable).</span></span>

## <a name="input"></a><span data-ttu-id="bbfcd-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="bbfcd-110">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="bbfcd-111">Op: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="bbfcd-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="bbfcd-112">Операция, применяемая к условию.</span><span class="sxs-lookup"><span data-stu-id="bbfcd-112">An operation to be conditionally applied.</span></span>


### <a name="bit--bool"></a><span data-ttu-id="bbfcd-113">bit: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="bbfcd-113">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="bbfcd-114">Логическое значение, определяющее, применяется ли оператор Op.</span><span class="sxs-lookup"><span data-stu-id="bbfcd-114">a boolean that controls whether op is applied or not.</span></span>


### <a name="target--t"></a><span data-ttu-id="bbfcd-115">Целевой объект: 'T</span><span class="sxs-lookup"><span data-stu-id="bbfcd-115">target : 'T</span></span>

<span data-ttu-id="bbfcd-116">Входные данные, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="bbfcd-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="bbfcd-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bbfcd-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="bbfcd-118">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="bbfcd-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="bbfcd-119">Е</span><span class="sxs-lookup"><span data-stu-id="bbfcd-119">'T</span></span>

<span data-ttu-id="bbfcd-120">Тип входных данных операции, которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="bbfcd-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="bbfcd-121">См. также:</span><span class="sxs-lookup"><span data-stu-id="bbfcd-121">See Also</span></span>

- [<span data-ttu-id="bbfcd-122">Microsoft. тактов. Canon. Апплифк</span><span class="sxs-lookup"><span data-stu-id="bbfcd-122">Microsoft.Quantum.Canon.ApplyIfC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [<span data-ttu-id="bbfcd-123">Microsoft. тактов. Canon. Апплифа</span><span class="sxs-lookup"><span data-stu-id="bbfcd-123">Microsoft.Quantum.Canon.ApplyIfA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [<span data-ttu-id="bbfcd-124">Microsoft. тактов. Canon. Апплифка</span><span class="sxs-lookup"><span data-stu-id="bbfcd-124">Microsoft.Quantum.Canon.ApplyIfCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfCA)