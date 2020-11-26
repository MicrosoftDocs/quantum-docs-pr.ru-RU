---
uid: Microsoft.Quantum.Canon.ApplyWithCA
title: Операция Аппливиска
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithCA
qsharp.summary: Given two operations, applies one as conjugated with the other.
ms.openlocfilehash: e86c452e9693c5a4d0d4e5a36471ab46bbf66dfe
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208148"
---
# <a name="applywithca-operation"></a><span data-ttu-id="bbd87-102">Операция Аппливиска</span><span class="sxs-lookup"><span data-stu-id="bbd87-102">ApplyWithCA operation</span></span>

<span data-ttu-id="bbd87-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="bbd87-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="bbd87-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bbd87-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bbd87-105">При выполнении двух операций применяется одна, как сопряженная с другой.</span><span class="sxs-lookup"><span data-stu-id="bbd87-105">Given two operations, applies one as conjugated with the other.</span></span>

```qsharp
operation ApplyWithCA<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit is Adj + Ctl), target : 'T) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="bbd87-106">Описание</span><span class="sxs-lookup"><span data-stu-id="bbd87-106">Description</span></span>

<span data-ttu-id="bbd87-107">При выполнении двух операций, которые соответственно описаны в единых операторах $U $ и $V $, применяет их в последовательности $U ^ {\дагжер} V U $.</span><span class="sxs-lookup"><span data-stu-id="bbd87-107">Given two operations, respectively described by unitary operators $U$ and $V$, applies them in the sequence $U^{\dagger} V U$.</span></span> <span data-ttu-id="bbd87-108">Это значит, что эта операция реализует оператор, заданный $V $ сопряженный с $U $.</span><span class="sxs-lookup"><span data-stu-id="bbd87-108">That is, this operation implements the unitary operator given by $V$ conjugated with $U$.</span></span>

## <a name="input"></a><span data-ttu-id="bbd87-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="bbd87-109">Input</span></span>

### <a name="outeroperation--t--unit--is-adj"></a><span data-ttu-id="bbd87-110">Аутероператион: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)  Нагода</span><span class="sxs-lookup"><span data-stu-id="bbd87-110">outerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="bbd87-111">Операция $U $, которую следует использовать для сопряженного $V $.</span><span class="sxs-lookup"><span data-stu-id="bbd87-111">The operation $U$ that should be used to conjugate $V$.</span></span> <span data-ttu-id="bbd87-112">Обратите внимание, что внешняя операция $U $ должна быть аджоинтабле, но не обязательно должна быть управляемой.</span><span class="sxs-lookup"><span data-stu-id="bbd87-112">Note that the outer operation $U$ needs to be adjointable, but does not need to be controllable.</span></span>


### <a name="inneroperation--t--unit--is-adj--ctl"></a><span data-ttu-id="bbd87-113">Иннероператион: не>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="bbd87-113">innerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="bbd87-114">Операция $V $, для которой выполняется сопряжение.</span><span class="sxs-lookup"><span data-stu-id="bbd87-114">The operation $V$ being conjugated.</span></span>


### <a name="target--t"></a><span data-ttu-id="bbd87-115">Целевой объект: 'T</span><span class="sxs-lookup"><span data-stu-id="bbd87-115">target : 'T</span></span>

<span data-ttu-id="bbd87-116">Входные данные, которые должны быть предоставлены внешним и внутренним операциям.</span><span class="sxs-lookup"><span data-stu-id="bbd87-116">The input to be provided to the outer and inner operations.</span></span>



## <a name="output--unit"></a><span data-ttu-id="bbd87-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bbd87-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="bbd87-118">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="bbd87-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="bbd87-119">Е</span><span class="sxs-lookup"><span data-stu-id="bbd87-119">'T</span></span>

<span data-ttu-id="bbd87-120">Целевой объект, на котором работают все внутренние и внешние операции.</span><span class="sxs-lookup"><span data-stu-id="bbd87-120">The target on which each of the inner and outer operations act.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbd87-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bbd87-121">Remarks</span></span>

<span data-ttu-id="bbd87-122">Во внешней операции всегда предполагается, что это аджоинтабле, но не обязательно быть управляемым, чтобы Объединенная операция была управляемой.</span><span class="sxs-lookup"><span data-stu-id="bbd87-122">The outer operation is always assumed to be adjointable, but does not need to be controllable in order for the combined operation to be controllable.</span></span>

## <a name="see-also"></a><span data-ttu-id="bbd87-123">См. также:</span><span class="sxs-lookup"><span data-stu-id="bbd87-123">See Also</span></span>

- [<span data-ttu-id="bbd87-124">Microsoft. тактов. Canon. Аппливис</span><span class="sxs-lookup"><span data-stu-id="bbd87-124">Microsoft.Quantum.Canon.ApplyWith</span></span>](xref:Microsoft.Quantum.Canon.ApplyWith)
- [<span data-ttu-id="bbd87-125">Microsoft. тактов. Canon. Аппливиса</span><span class="sxs-lookup"><span data-stu-id="bbd87-125">Microsoft.Quantum.Canon.ApplyWithA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithA)
- [<span data-ttu-id="bbd87-126">Microsoft. тактов. Canon. Аппливиск</span><span class="sxs-lookup"><span data-stu-id="bbd87-126">Microsoft.Quantum.Canon.ApplyWithC</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithC)