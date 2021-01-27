---
uid: Microsoft.Quantum.Canon.ApplyWithA
title: Операция Аппливиса
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithA
qsharp.summary: Given two operations, applies one as conjugated with the other.
ms.openlocfilehash: f717347a81e4efa5ad1736485ad9e1c518d736a7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841156"
---
# <a name="applywitha-operation"></a><span data-ttu-id="3d377-102">Операция Аппливиса</span><span class="sxs-lookup"><span data-stu-id="3d377-102">ApplyWithA operation</span></span>

<span data-ttu-id="3d377-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="3d377-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="3d377-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3d377-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3d377-105">При выполнении двух операций применяется одна, как сопряженная с другой.</span><span class="sxs-lookup"><span data-stu-id="3d377-105">Given two operations, applies one as conjugated with the other.</span></span>

```qsharp
operation ApplyWithA<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit is Adj), target : 'T) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="3d377-106">Описание</span><span class="sxs-lookup"><span data-stu-id="3d377-106">Description</span></span>

<span data-ttu-id="3d377-107">При выполнении двух операций, которые соответственно описаны в единых операторах $U $ и $V $, применяет их в последовательности $U ^ {\дагжер} V U $.</span><span class="sxs-lookup"><span data-stu-id="3d377-107">Given two operations, respectively described by unitary operators $U$ and $V$, applies them in the sequence $U^{\dagger} V U$.</span></span> <span data-ttu-id="3d377-108">Это значит, что эта операция реализует оператор, заданный $V $ сопряженный с $U $.</span><span class="sxs-lookup"><span data-stu-id="3d377-108">That is, this operation implements the unitary operator given by $V$ conjugated with $U$.</span></span>

## <a name="input"></a><span data-ttu-id="3d377-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="3d377-109">Input</span></span>

### <a name="outeroperation--t--unit--is-adj"></a><span data-ttu-id="3d377-110">Аутероператион: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)  Нагода</span><span class="sxs-lookup"><span data-stu-id="3d377-110">outerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="3d377-111">Операция $U $, которую следует использовать для сопряженного $V $.</span><span class="sxs-lookup"><span data-stu-id="3d377-111">The operation $U$ that should be used to conjugate $V$.</span></span> <span data-ttu-id="3d377-112">Обратите внимание, что внешняя операция $U $ должна быть аджоинтабле, но не обязательно должна быть управляемой.</span><span class="sxs-lookup"><span data-stu-id="3d377-112">Note that the outer operation $U$ needs to be adjointable, but does not need to be controllable.</span></span>


### <a name="inneroperation--t--unit--is-adj"></a><span data-ttu-id="3d377-113">Иннероператион: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)  Нагода</span><span class="sxs-lookup"><span data-stu-id="3d377-113">innerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="3d377-114">Операция $V $, для которой выполняется сопряжение.</span><span class="sxs-lookup"><span data-stu-id="3d377-114">The operation $V$ being conjugated.</span></span>


### <a name="target--t"></a><span data-ttu-id="3d377-115">Целевой объект: 'T</span><span class="sxs-lookup"><span data-stu-id="3d377-115">target : 'T</span></span>

<span data-ttu-id="3d377-116">Входные данные, которые должны быть предоставлены внешним и внутренним операциям.</span><span class="sxs-lookup"><span data-stu-id="3d377-116">The input to be provided to the outer and inner operations.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3d377-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3d377-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="3d377-118">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="3d377-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="3d377-119">Е</span><span class="sxs-lookup"><span data-stu-id="3d377-119">'T</span></span>

<span data-ttu-id="3d377-120">Целевой объект, на котором работают все внутренние и внешние операции.</span><span class="sxs-lookup"><span data-stu-id="3d377-120">The target on which each of the inner and outer operations act.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d377-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="3d377-121">Remarks</span></span>

<span data-ttu-id="3d377-122">Во внешней операции всегда предполагается, что это аджоинтабле, но не обязательно быть управляемым, чтобы Объединенная операция была управляемой.</span><span class="sxs-lookup"><span data-stu-id="3d377-122">The outer operation is always assumed to be adjointable, but does not need to be controllable in order for the combined operation to be controllable.</span></span>

## <a name="see-also"></a><span data-ttu-id="3d377-123">См. также:</span><span class="sxs-lookup"><span data-stu-id="3d377-123">See Also</span></span>

- [<span data-ttu-id="3d377-124">Microsoft. тактов. Canon. Аппливис</span><span class="sxs-lookup"><span data-stu-id="3d377-124">Microsoft.Quantum.Canon.ApplyWith</span></span>](xref:Microsoft.Quantum.Canon.ApplyWith)
- [<span data-ttu-id="3d377-125">Microsoft. тактов. Canon. Аппливиск</span><span class="sxs-lookup"><span data-stu-id="3d377-125">Microsoft.Quantum.Canon.ApplyWithC</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithC)
- [<span data-ttu-id="3d377-126">Microsoft. тактов. Canon. Аппливиска</span><span class="sxs-lookup"><span data-stu-id="3d377-126">Microsoft.Quantum.Canon.ApplyWithCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithCA)