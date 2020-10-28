---
uid: Microsoft.Quantum.Canon.ApplyWithCA
title: Операция Аппливиска
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithCA
qsharp.summary: Given two operations, applies one as conjugated with the other.
ms.openlocfilehash: abc62791416e78c1b2937a226327b71da8b8e288
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716882"
---
# <a name="applywithca-operation"></a><span data-ttu-id="95668-102">Операция Аппливиска</span><span class="sxs-lookup"><span data-stu-id="95668-102">ApplyWithCA operation</span></span>

<span data-ttu-id="95668-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="95668-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="95668-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="95668-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="95668-105">При выполнении двух операций применяется одна, как сопряженная с другой.</span><span class="sxs-lookup"><span data-stu-id="95668-105">Given two operations, applies one as conjugated with the other.</span></span>

```qsharp
operation ApplyWithCA<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit is Adj + Ctl), target : 'T) : Unit
```


## <a name="description"></a><span data-ttu-id="95668-106">Описание</span><span class="sxs-lookup"><span data-stu-id="95668-106">Description</span></span>

<span data-ttu-id="95668-107">При выполнении двух операций, которые соответственно описаны в единых операторах $U $ и $V $, применяет их в последовательности $U ^ {\дагжер} V U $.</span><span class="sxs-lookup"><span data-stu-id="95668-107">Given two operations, respectively described by unitary operators $U$ and $V$, applies them in the sequence $U^{\dagger} V U$.</span></span> <span data-ttu-id="95668-108">Это значит, что эта операция реализует оператор, заданный $V $ сопряженный с $U $.</span><span class="sxs-lookup"><span data-stu-id="95668-108">That is, this operation implements the unitary operator given by $V$ conjugated with $U$.</span></span>

## <a name="input"></a><span data-ttu-id="95668-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="95668-109">Input</span></span>

### <a name="outeroperation--t--unit-adj"></a><span data-ttu-id="95668-110">Аутероператион: 'T [=>ное](xref:microsoft.quantum.lang-ref.unit) прогода</span><span class="sxs-lookup"><span data-stu-id="95668-110">outerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="95668-111">Операция $U $, которую следует использовать для сопряженного $V $.</span><span class="sxs-lookup"><span data-stu-id="95668-111">The operation $U$ that should be used to conjugate $V$.</span></span> <span data-ttu-id="95668-112">Обратите внимание, что внешняя операция $U $ должна быть аджоинтабле, но не обязательно должна быть управляемой.</span><span class="sxs-lookup"><span data-stu-id="95668-112">Note that the outer operation $U$ needs to be adjointable, but does not need to be controllable.</span></span>


### <a name="inneroperation--t--unit-adj--ctl"></a><span data-ttu-id="95668-113">Иннероператион: 'T => [модульные](xref:microsoft.quantum.lang-ref.unit) года + CTL</span><span class="sxs-lookup"><span data-stu-id="95668-113">innerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="95668-114">Операция $V $, для которой выполняется сопряжение.</span><span class="sxs-lookup"><span data-stu-id="95668-114">The operation $V$ being conjugated.</span></span>


### <a name="target--t"></a><span data-ttu-id="95668-115">Целевой объект: 'T</span><span class="sxs-lookup"><span data-stu-id="95668-115">target : 'T</span></span>

<span data-ttu-id="95668-116">Входные данные, которые должны быть предоставлены внешним и внутренним операциям.</span><span class="sxs-lookup"><span data-stu-id="95668-116">The input to be provided to the outer and inner operations.</span></span>



## <a name="output--unit"></a><span data-ttu-id="95668-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="95668-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="95668-118">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="95668-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="95668-119">Е</span><span class="sxs-lookup"><span data-stu-id="95668-119">'T</span></span>

<span data-ttu-id="95668-120">Целевой объект, на котором работают все внутренние и внешние операции.</span><span class="sxs-lookup"><span data-stu-id="95668-120">The target on which each of the inner and outer operations act.</span></span>

## <a name="remarks"></a><span data-ttu-id="95668-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="95668-121">Remarks</span></span>

<span data-ttu-id="95668-122">Во внешней операции всегда предполагается, что это аджоинтабле, но не обязательно быть управляемым, чтобы Объединенная операция была управляемой.</span><span class="sxs-lookup"><span data-stu-id="95668-122">The outer operation is always assumed to be adjointable, but does not need to be controllable in order for the combined operation to be controllable.</span></span>

## <a name="see-also"></a><span data-ttu-id="95668-123">См. также:</span><span class="sxs-lookup"><span data-stu-id="95668-123">See Also</span></span>

- [<span data-ttu-id="95668-124">Microsoft. тактов. Canon. Аппливис</span><span class="sxs-lookup"><span data-stu-id="95668-124">Microsoft.Quantum.Canon.ApplyWith</span></span>](xref:Microsoft.Quantum.Canon.ApplyWith)
- [<span data-ttu-id="95668-125">Microsoft. тактов. Canon. Аппливиса</span><span class="sxs-lookup"><span data-stu-id="95668-125">Microsoft.Quantum.Canon.ApplyWithA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithA)
- [<span data-ttu-id="95668-126">Microsoft. тактов. Canon. Аппливиск</span><span class="sxs-lookup"><span data-stu-id="95668-126">Microsoft.Quantum.Canon.ApplyWithC</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithC)