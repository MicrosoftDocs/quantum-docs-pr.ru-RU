---
uid: Microsoft.Quantum.Canon.ConjugatedBy
title: Функция Конжугатедби
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ConjugatedBy
qsharp.summary: Given outer and inner operations, returns a new operation that conjugates the inner operation by the outer operation.
ms.openlocfilehash: ed5316d4603c31d7db2cd6b0d7e54b56fc750fcb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216733"
---
# <a name="conjugatedby-function"></a><span data-ttu-id="ec424-102">Функция Конжугатедби</span><span class="sxs-lookup"><span data-stu-id="ec424-102">ConjugatedBy function</span></span>

<span data-ttu-id="ec424-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ec424-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ec424-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ec424-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ec424-105">При наличии внешних и внутренних операций возвращает новую операцию, которая сопряжена с внутренней операцией внешней операцией.</span><span class="sxs-lookup"><span data-stu-id="ec424-105">Given outer and inner operations, returns a new operation that conjugates the inner operation by the outer operation.</span></span>

```qsharp
function ConjugatedBy<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit)) : ('T => Unit)
```


## <a name="input"></a><span data-ttu-id="ec424-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ec424-106">Input</span></span>

### <a name="outeroperation--t--unit--is-adj"></a><span data-ttu-id="ec424-107">Аутероператион: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)  Нагода</span><span class="sxs-lookup"><span data-stu-id="ec424-107">outerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="ec424-108">Операция $U $, которую следует использовать для сопряженного $V $.</span><span class="sxs-lookup"><span data-stu-id="ec424-108">The operation $U$ that should be used to conjugate $V$.</span></span> <span data-ttu-id="ec424-109">Обратите внимание, что внешняя операция $U $ должна быть аджоинтабле, но не обязательно должна быть управляемой.</span><span class="sxs-lookup"><span data-stu-id="ec424-109">Note that the outer operation $U$ needs to be adjointable, but does not need to be controllable.</span></span>


### <a name="inneroperation--t--unit"></a><span data-ttu-id="ec424-110">Иннероператион: 'T = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="ec424-110">innerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="ec424-111">Операция $V $, для которой выполняется сопряжение.</span><span class="sxs-lookup"><span data-stu-id="ec424-111">The operation $V$ being conjugated.</span></span>



## <a name="output--t--unit"></a><span data-ttu-id="ec424-112">Выходные данные: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ec424-112">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="ec424-113">Новая операция, действие которой представляется единой $U ^ {\дагжер} V U $.</span><span class="sxs-lookup"><span data-stu-id="ec424-113">A new operation whose action is represented by the unitary $U^{\dagger} V U$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="ec424-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="ec424-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ec424-115">Е</span><span class="sxs-lookup"><span data-stu-id="ec424-115">'T</span></span>

<span data-ttu-id="ec424-116">Тип целевого объекта, в котором работают все внутренние и внешние операции.</span><span class="sxs-lookup"><span data-stu-id="ec424-116">The type of the target on which each of the inner and outer operations act.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec424-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ec424-117">Remarks</span></span>

<span data-ttu-id="ec424-118">Во внешней операции всегда предполагается, что это аджоинтабле, но не обязательно быть управляемым, чтобы Объединенная операция была управляемой.</span><span class="sxs-lookup"><span data-stu-id="ec424-118">The outer operation is always assumed to be adjointable, but does not need to be controllable in order for the combined operation to be controllable.</span></span>

## <a name="see-also"></a><span data-ttu-id="ec424-119">См. также:</span><span class="sxs-lookup"><span data-stu-id="ec424-119">See Also</span></span>

- [<span data-ttu-id="ec424-120">Microsoft. тактов. Canon. Конжугатедбя</span><span class="sxs-lookup"><span data-stu-id="ec424-120">Microsoft.Quantum.Canon.ConjugatedByA</span></span>](xref:Microsoft.Quantum.Canon.ConjugatedByA)
- [<span data-ttu-id="ec424-121">Microsoft. тактов. Canon. Конжугатедбик</span><span class="sxs-lookup"><span data-stu-id="ec424-121">Microsoft.Quantum.Canon.ConjugatedByC</span></span>](xref:Microsoft.Quantum.Canon.ConjugatedByC)
- [<span data-ttu-id="ec424-122">Microsoft. тактов. Canon. Конжугатедбика</span><span class="sxs-lookup"><span data-stu-id="ec424-122">Microsoft.Quantum.Canon.ConjugatedByCA</span></span>](xref:Microsoft.Quantum.Canon.ConjugatedByCA)
- [<span data-ttu-id="ec424-123">Microsoft. тактов. Canon. Аппливис</span><span class="sxs-lookup"><span data-stu-id="ec424-123">Microsoft.Quantum.Canon.ApplyWith</span></span>](xref:Microsoft.Quantum.Canon.ApplyWith)