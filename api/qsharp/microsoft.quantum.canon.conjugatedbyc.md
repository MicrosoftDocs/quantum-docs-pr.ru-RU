---
uid: Microsoft.Quantum.Canon.ConjugatedByC
title: Функция Конжугатедбик
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ConjugatedByC
qsharp.summary: Given outer and inner operations, returns a new operation that conjugates the inner operation by the outer operation.
ms.openlocfilehash: c4c381e40c5a941487bcf78ebe5339574aedb45d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716461"
---
# <a name="conjugatedbyc-function"></a><span data-ttu-id="23ca4-102">Функция Конжугатедбик</span><span class="sxs-lookup"><span data-stu-id="23ca4-102">ConjugatedByC function</span></span>

<span data-ttu-id="23ca4-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="23ca4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="23ca4-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="23ca4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="23ca4-105">При наличии внешних и внутренних операций возвращает новую операцию, которая сопряжена с внутренней операцией внешней операцией.</span><span class="sxs-lookup"><span data-stu-id="23ca4-105">Given outer and inner operations, returns a new operation that conjugates the inner operation by the outer operation.</span></span>

```qsharp
function ConjugatedByC<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit is Ctl)) : ('T => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="23ca4-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="23ca4-106">Input</span></span>

### <a name="outeroperation--t--unit-adj"></a><span data-ttu-id="23ca4-107">Аутероператион: 'T [=>ное](xref:microsoft.quantum.lang-ref.unit) прогода</span><span class="sxs-lookup"><span data-stu-id="23ca4-107">outerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="23ca4-108">Операция $U $, которую следует использовать для сопряженного $V $.</span><span class="sxs-lookup"><span data-stu-id="23ca4-108">The operation $U$ that should be used to conjugate $V$.</span></span> <span data-ttu-id="23ca4-109">Обратите внимание, что внешняя операция $U $ должна быть аджоинтабле, но не обязательно должна быть управляемой.</span><span class="sxs-lookup"><span data-stu-id="23ca4-109">Note that the outer operation $U$ needs to be adjointable, but does not need to be controllable.</span></span>


### <a name="inneroperation--t--unit-ctl"></a><span data-ttu-id="23ca4-110">Иннероператион: 'T = список CTL для [единицы](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="23ca4-110">innerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="23ca4-111">Операция $V $, для которой выполняется сопряжение.</span><span class="sxs-lookup"><span data-stu-id="23ca4-111">The operation $V$ being conjugated.</span></span>



## <a name="output--t--unit-ctl"></a><span data-ttu-id="23ca4-112">Выходные данные: 'T => [единицы](xref:microsoft.quantum.lang-ref.unit) CTL</span><span class="sxs-lookup"><span data-stu-id="23ca4-112">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="23ca4-113">Новая операция, действие которой представляется единой $U ^ {\дагжер} V U $.</span><span class="sxs-lookup"><span data-stu-id="23ca4-113">A new operation whose action is represented by the unitary $U^{\dagger} V U$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="23ca4-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="23ca4-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="23ca4-115">Е</span><span class="sxs-lookup"><span data-stu-id="23ca4-115">'T</span></span>

<span data-ttu-id="23ca4-116">Тип целевого объекта, в котором работают все внутренние и внешние операции.</span><span class="sxs-lookup"><span data-stu-id="23ca4-116">The type of the target on which each of the inner and outer operations act.</span></span>

## <a name="remarks"></a><span data-ttu-id="23ca4-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="23ca4-117">Remarks</span></span>

<span data-ttu-id="23ca4-118">Во внешней операции всегда предполагается, что это аджоинтабле, но не обязательно быть управляемым, чтобы Объединенная операция была управляемой.</span><span class="sxs-lookup"><span data-stu-id="23ca4-118">The outer operation is always assumed to be adjointable, but does not need to be controllable in order for the combined operation to be controllable.</span></span>

## <a name="see-also"></a><span data-ttu-id="23ca4-119">См. также:</span><span class="sxs-lookup"><span data-stu-id="23ca4-119">See Also</span></span>

- [<span data-ttu-id="23ca4-120">Microsoft. тактов. Canon. Конжугатедби</span><span class="sxs-lookup"><span data-stu-id="23ca4-120">Microsoft.Quantum.Canon.ConjugatedBy</span></span>](xref:Microsoft.Quantum.Canon.ConjugatedBy)
- [<span data-ttu-id="23ca4-121">Microsoft. тактов. Canon. Конжугатедбя</span><span class="sxs-lookup"><span data-stu-id="23ca4-121">Microsoft.Quantum.Canon.ConjugatedByA</span></span>](xref:Microsoft.Quantum.Canon.ConjugatedByA)
- [<span data-ttu-id="23ca4-122">Microsoft. тактов. Canon. Конжугатедбика</span><span class="sxs-lookup"><span data-stu-id="23ca4-122">Microsoft.Quantum.Canon.ConjugatedByCA</span></span>](xref:Microsoft.Quantum.Canon.ConjugatedByCA)
- [<span data-ttu-id="23ca4-123">Microsoft. тактов. Canon. Аппливис</span><span class="sxs-lookup"><span data-stu-id="23ca4-123">Microsoft.Quantum.Canon.ApplyWith</span></span>](xref:Microsoft.Quantum.Canon.ApplyWith)