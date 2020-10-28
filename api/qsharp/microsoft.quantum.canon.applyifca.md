---
uid: Microsoft.Quantum.Canon.ApplyIfCA
title: Операция Апплифка
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfCA
qsharp.summary: Applies a unitary operation conditioned on a classical bit.
ms.openlocfilehash: 9057c79622f15a082963d94fc261664e00322feb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729592"
---
# <a name="applyifca-operation"></a><span data-ttu-id="23016-102">Операция Апплифка</span><span class="sxs-lookup"><span data-stu-id="23016-102">ApplyIfCA operation</span></span>

<span data-ttu-id="23016-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="23016-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="23016-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="23016-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="23016-105">Применяет единую операцию с условием на Классический бит.</span><span class="sxs-lookup"><span data-stu-id="23016-105">Applies a unitary operation conditioned on a classical bit.</span></span>

```qsharp
operation ApplyIfCA<'T> (op : ('T => Unit is Ctl + Adj), bit : Bool, target : 'T) : Unit
```


## <a name="description"></a><span data-ttu-id="23016-106">Описание</span><span class="sxs-lookup"><span data-stu-id="23016-106">Description</span></span>

<span data-ttu-id="23016-107">При наличии операции `op` и битового значения `bit` применяется `op` к, `target` Если имеет `bit` значение `true` .</span><span class="sxs-lookup"><span data-stu-id="23016-107">Given an operation `op` and a bit value `bit`, applies `op` to the `target` if `bit` is `true`.</span></span> <span data-ttu-id="23016-108">Если значение `false` равно, то ничего не происходит с `target` .</span><span class="sxs-lookup"><span data-stu-id="23016-108">If `false`, nothing happens to the `target`.</span></span>
<span data-ttu-id="23016-109">Суффикс `CA` указывает, что применяемая операция является единой (управляемой и аджоинтабле).</span><span class="sxs-lookup"><span data-stu-id="23016-109">The suffix `CA` indicates that the operation to be applied is unitary (controllable and adjointable).</span></span>

## <a name="input"></a><span data-ttu-id="23016-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="23016-110">Input</span></span>

### <a name="op--t--unit-ctl--adj"></a><span data-ttu-id="23016-111">Op: t => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + прилагательные</span><span class="sxs-lookup"><span data-stu-id="23016-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="23016-112">Операция, применяемая к условию.</span><span class="sxs-lookup"><span data-stu-id="23016-112">An operation to be conditionally applied.</span></span>


### <a name="bit--bool"></a><span data-ttu-id="23016-113">bit: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="23016-113">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="23016-114">Логическое значение, определяющее, применяется ли оператор Op.</span><span class="sxs-lookup"><span data-stu-id="23016-114">a boolean that controls whether op is applied or not.</span></span>


### <a name="target--t"></a><span data-ttu-id="23016-115">Целевой объект: 'T</span><span class="sxs-lookup"><span data-stu-id="23016-115">target : 'T</span></span>

<span data-ttu-id="23016-116">Входные данные, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="23016-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="23016-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="23016-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="23016-118">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="23016-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="23016-119">Е</span><span class="sxs-lookup"><span data-stu-id="23016-119">'T</span></span>

<span data-ttu-id="23016-120">Тип входных данных операции, которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="23016-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="23016-121">См. также:</span><span class="sxs-lookup"><span data-stu-id="23016-121">See Also</span></span>

- [<span data-ttu-id="23016-122">Microsoft. тактов. Canon. Апплифк</span><span class="sxs-lookup"><span data-stu-id="23016-122">Microsoft.Quantum.Canon.ApplyIfC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [<span data-ttu-id="23016-123">Microsoft. тактов. Canon. Апплифа</span><span class="sxs-lookup"><span data-stu-id="23016-123">Microsoft.Quantum.Canon.ApplyIfA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [<span data-ttu-id="23016-124">Microsoft. тактов. Canon. Апплифка</span><span class="sxs-lookup"><span data-stu-id="23016-124">Microsoft.Quantum.Canon.ApplyIfCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfCA)