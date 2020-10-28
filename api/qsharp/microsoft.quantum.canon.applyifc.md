---
uid: Microsoft.Quantum.Canon.ApplyIfC
title: Операция Апплифк
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfC
qsharp.summary: Applies a controllable operation conditioned on a classical bit.
ms.openlocfilehash: e16254154909eb844164538acb7b82fedc11f86a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729593"
---
# <a name="applyifc-operation"></a><span data-ttu-id="12298-102">Операция Апплифк</span><span class="sxs-lookup"><span data-stu-id="12298-102">ApplyIfC operation</span></span>

<span data-ttu-id="12298-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="12298-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="12298-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="12298-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="12298-105">Применяет управляемую операцию к классическому биту.</span><span class="sxs-lookup"><span data-stu-id="12298-105">Applies a controllable operation conditioned on a classical bit.</span></span>

```qsharp
operation ApplyIfC<'T> (op : ('T => Unit is Ctl), bit : Bool, target : 'T) : Unit
```


## <a name="description"></a><span data-ttu-id="12298-106">Описание</span><span class="sxs-lookup"><span data-stu-id="12298-106">Description</span></span>

<span data-ttu-id="12298-107">При наличии операции `op` и битового значения `bit` применяется `op` к, `target` Если имеет `bit` значение `true` .</span><span class="sxs-lookup"><span data-stu-id="12298-107">Given an operation `op` and a bit value `bit`, applies `op` to the `target` if `bit` is `true`.</span></span> <span data-ttu-id="12298-108">Если значение `false` равно, то ничего не происходит с `target` .</span><span class="sxs-lookup"><span data-stu-id="12298-108">If `false`, nothing happens to the `target`.</span></span>
<span data-ttu-id="12298-109">Суффикс `C` указывает, что операция, которая должна быть применена, является управляемой.</span><span class="sxs-lookup"><span data-stu-id="12298-109">The suffix `C` indicates that the operation to be applied is controllable.</span></span>

## <a name="input"></a><span data-ttu-id="12298-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="12298-110">Input</span></span>

### <a name="op--t--unit-ctl"></a><span data-ttu-id="12298-111">Op: 'T => [единицы](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="12298-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="12298-112">Операция, применяемая к условию.</span><span class="sxs-lookup"><span data-stu-id="12298-112">An operation to be conditionally applied.</span></span>


### <a name="bit--bool"></a><span data-ttu-id="12298-113">bit: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="12298-113">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="12298-114">Логическое значение, определяющее, применяется ли оператор Op.</span><span class="sxs-lookup"><span data-stu-id="12298-114">a boolean that controls whether op is applied or not.</span></span>


### <a name="target--t"></a><span data-ttu-id="12298-115">Целевой объект: 'T</span><span class="sxs-lookup"><span data-stu-id="12298-115">target : 'T</span></span>

<span data-ttu-id="12298-116">Входные данные, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="12298-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="12298-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="12298-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="12298-118">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="12298-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="12298-119">Е</span><span class="sxs-lookup"><span data-stu-id="12298-119">'T</span></span>

<span data-ttu-id="12298-120">Тип входных данных операции, которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="12298-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="12298-121">См. также:</span><span class="sxs-lookup"><span data-stu-id="12298-121">See Also</span></span>

- [<span data-ttu-id="12298-122">Microsoft. тактов. Canon. Апплифк</span><span class="sxs-lookup"><span data-stu-id="12298-122">Microsoft.Quantum.Canon.ApplyIfC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [<span data-ttu-id="12298-123">Microsoft. тактов. Canon. Апплифа</span><span class="sxs-lookup"><span data-stu-id="12298-123">Microsoft.Quantum.Canon.ApplyIfA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [<span data-ttu-id="12298-124">Microsoft. тактов. Canon. Апплифка</span><span class="sxs-lookup"><span data-stu-id="12298-124">Microsoft.Quantum.Canon.ApplyIfCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfCA)