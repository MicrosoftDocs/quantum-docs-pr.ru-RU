---
uid: Microsoft.Quantum.Canon.ApplyWithA
title: Операция Аппливиса
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithA
qsharp.summary: Given two operations, applies one as conjugated with the other.
ms.openlocfilehash: f1ff31da53952931426d358cbedad44a50d87f5e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716924"
---
# <a name="applywitha-operation"></a><span data-ttu-id="8a478-102">Операция Аппливиса</span><span class="sxs-lookup"><span data-stu-id="8a478-102">ApplyWithA operation</span></span>

<span data-ttu-id="8a478-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8a478-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8a478-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8a478-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8a478-105">При выполнении двух операций применяется одна, как сопряженная с другой.</span><span class="sxs-lookup"><span data-stu-id="8a478-105">Given two operations, applies one as conjugated with the other.</span></span>

```qsharp
operation ApplyWithA<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit is Adj), target : 'T) : Unit
```


## <a name="description"></a><span data-ttu-id="8a478-106">Описание</span><span class="sxs-lookup"><span data-stu-id="8a478-106">Description</span></span>

<span data-ttu-id="8a478-107">При выполнении двух операций, которые соответственно описаны в единых операторах $U $ и $V $, применяет их в последовательности $U ^ {\дагжер} V U $.</span><span class="sxs-lookup"><span data-stu-id="8a478-107">Given two operations, respectively described by unitary operators $U$ and $V$, applies them in the sequence $U^{\dagger} V U$.</span></span> <span data-ttu-id="8a478-108">Это значит, что эта операция реализует оператор, заданный $V $ сопряженный с $U $.</span><span class="sxs-lookup"><span data-stu-id="8a478-108">That is, this operation implements the unitary operator given by $V$ conjugated with $U$.</span></span>

## <a name="input"></a><span data-ttu-id="8a478-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="8a478-109">Input</span></span>

### <a name="outeroperation--t--unit-adj"></a><span data-ttu-id="8a478-110">Аутероператион: 'T [=>ное](xref:microsoft.quantum.lang-ref.unit) прогода</span><span class="sxs-lookup"><span data-stu-id="8a478-110">outerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="8a478-111">Операция $U $, которую следует использовать для сопряженного $V $.</span><span class="sxs-lookup"><span data-stu-id="8a478-111">The operation $U$ that should be used to conjugate $V$.</span></span> <span data-ttu-id="8a478-112">Обратите внимание, что внешняя операция $U $ должна быть аджоинтабле, но не обязательно должна быть управляемой.</span><span class="sxs-lookup"><span data-stu-id="8a478-112">Note that the outer operation $U$ needs to be adjointable, but does not need to be controllable.</span></span>


### <a name="inneroperation--t--unit-adj"></a><span data-ttu-id="8a478-113">Иннероператион: 'T [=>ное](xref:microsoft.quantum.lang-ref.unit) прогода</span><span class="sxs-lookup"><span data-stu-id="8a478-113">innerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="8a478-114">Операция $V $, для которой выполняется сопряжение.</span><span class="sxs-lookup"><span data-stu-id="8a478-114">The operation $V$ being conjugated.</span></span>


### <a name="target--t"></a><span data-ttu-id="8a478-115">Целевой объект: 'T</span><span class="sxs-lookup"><span data-stu-id="8a478-115">target : 'T</span></span>

<span data-ttu-id="8a478-116">Входные данные, которые должны быть предоставлены внешним и внутренним операциям.</span><span class="sxs-lookup"><span data-stu-id="8a478-116">The input to be provided to the outer and inner operations.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8a478-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8a478-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="8a478-118">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="8a478-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8a478-119">Е</span><span class="sxs-lookup"><span data-stu-id="8a478-119">'T</span></span>

<span data-ttu-id="8a478-120">Целевой объект, на котором работают все внутренние и внешние операции.</span><span class="sxs-lookup"><span data-stu-id="8a478-120">The target on which each of the inner and outer operations act.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a478-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="8a478-121">Remarks</span></span>

<span data-ttu-id="8a478-122">Во внешней операции всегда предполагается, что это аджоинтабле, но не обязательно быть управляемым, чтобы Объединенная операция была управляемой.</span><span class="sxs-lookup"><span data-stu-id="8a478-122">The outer operation is always assumed to be adjointable, but does not need to be controllable in order for the combined operation to be controllable.</span></span>

## <a name="see-also"></a><span data-ttu-id="8a478-123">См. также:</span><span class="sxs-lookup"><span data-stu-id="8a478-123">See Also</span></span>

- [<span data-ttu-id="8a478-124">Microsoft. тактов. Canon. Аппливис</span><span class="sxs-lookup"><span data-stu-id="8a478-124">Microsoft.Quantum.Canon.ApplyWith</span></span>](xref:Microsoft.Quantum.Canon.ApplyWith)
- [<span data-ttu-id="8a478-125">Microsoft. тактов. Canon. Аппливиск</span><span class="sxs-lookup"><span data-stu-id="8a478-125">Microsoft.Quantum.Canon.ApplyWithC</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithC)
- [<span data-ttu-id="8a478-126">Microsoft. тактов. Canon. Аппливиска</span><span class="sxs-lookup"><span data-stu-id="8a478-126">Microsoft.Quantum.Canon.ApplyWithCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithCA)