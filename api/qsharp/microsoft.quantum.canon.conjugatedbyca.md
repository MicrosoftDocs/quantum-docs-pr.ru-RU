---
uid: Microsoft.Quantum.Canon.ConjugatedByCA
title: Функция Конжугатедбика
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ConjugatedByCA
qsharp.summary: Given outer and inner operations, returns a new operation that conjugates the inner operation by the outer operation.
ms.openlocfilehash: 54301f991d3bda14e2d2a0a6837ee89d299f2e04
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840816"
---
# <a name="conjugatedbyca-function"></a><span data-ttu-id="11adc-102">Функция Конжугатедбика</span><span class="sxs-lookup"><span data-stu-id="11adc-102">ConjugatedByCA function</span></span>

<span data-ttu-id="11adc-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="11adc-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="11adc-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="11adc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="11adc-105">При наличии внешних и внутренних операций возвращает новую операцию, которая сопряжена с внутренней операцией внешней операцией.</span><span class="sxs-lookup"><span data-stu-id="11adc-105">Given outer and inner operations, returns a new operation that conjugates the inner operation by the outer operation.</span></span>

```qsharp
function ConjugatedByCA<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit is Adj + Ctl)) : ('T => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="11adc-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="11adc-106">Input</span></span>

### <a name="outeroperation--t--unit--is-adj"></a><span data-ttu-id="11adc-107">Аутероператион: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)  Нагода</span><span class="sxs-lookup"><span data-stu-id="11adc-107">outerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="11adc-108">Операция $U $, которую следует использовать для сопряженного $V $.</span><span class="sxs-lookup"><span data-stu-id="11adc-108">The operation $U$ that should be used to conjugate $V$.</span></span> <span data-ttu-id="11adc-109">Обратите внимание, что внешняя операция $U $ должна быть аджоинтабле, но не обязательно должна быть управляемой.</span><span class="sxs-lookup"><span data-stu-id="11adc-109">Note that the outer operation $U$ needs to be adjointable, but does not need to be controllable.</span></span>


### <a name="inneroperation--t--unit--is-adj--ctl"></a><span data-ttu-id="11adc-110">Иннероператион: не>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="11adc-110">innerOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="11adc-111">Операция $V $, для которой выполняется сопряжение.</span><span class="sxs-lookup"><span data-stu-id="11adc-111">The operation $V$ being conjugated.</span></span>



## <a name="output--t--unit--is-adj--ctl"></a><span data-ttu-id="11adc-112">Выходные данные: 'T => [единицы измерения](xref:microsoft.quantum.lang-ref.unit)  и CTL</span><span class="sxs-lookup"><span data-stu-id="11adc-112">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="11adc-113">Новая операция, действие которой представляется единой $U ^ {\дагжер} V U $.</span><span class="sxs-lookup"><span data-stu-id="11adc-113">A new operation whose action is represented by the unitary $U^{\dagger} V U$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="11adc-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="11adc-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="11adc-115">Е</span><span class="sxs-lookup"><span data-stu-id="11adc-115">'T</span></span>

<span data-ttu-id="11adc-116">Тип целевого объекта, в котором работают все внутренние и внешние операции.</span><span class="sxs-lookup"><span data-stu-id="11adc-116">The type of the target on which each of the inner and outer operations act.</span></span>

## <a name="remarks"></a><span data-ttu-id="11adc-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="11adc-117">Remarks</span></span>

<span data-ttu-id="11adc-118">Во внешней операции всегда предполагается, что это аджоинтабле, но не обязательно быть управляемым, чтобы Объединенная операция была управляемой.</span><span class="sxs-lookup"><span data-stu-id="11adc-118">The outer operation is always assumed to be adjointable, but does not need to be controllable in order for the combined operation to be controllable.</span></span>

## <a name="see-also"></a><span data-ttu-id="11adc-119">См. также:</span><span class="sxs-lookup"><span data-stu-id="11adc-119">See Also</span></span>

- [<span data-ttu-id="11adc-120">Microsoft. тактов. Canon. Конжугатедбя</span><span class="sxs-lookup"><span data-stu-id="11adc-120">Microsoft.Quantum.Canon.ConjugatedByA</span></span>](xref:Microsoft.Quantum.Canon.ConjugatedByA)
- [<span data-ttu-id="11adc-121">Microsoft. тактов. Canon. Конжугатедбик</span><span class="sxs-lookup"><span data-stu-id="11adc-121">Microsoft.Quantum.Canon.ConjugatedByC</span></span>](xref:Microsoft.Quantum.Canon.ConjugatedByC)
- [<span data-ttu-id="11adc-122">Microsoft. тактов. Canon. Конжугатедбика</span><span class="sxs-lookup"><span data-stu-id="11adc-122">Microsoft.Quantum.Canon.ConjugatedByCA</span></span>](xref:Microsoft.Quantum.Canon.ConjugatedByCA)
- [<span data-ttu-id="11adc-123">Microsoft. тактов. Canon. Аппливис</span><span class="sxs-lookup"><span data-stu-id="11adc-123">Microsoft.Quantum.Canon.ApplyWith</span></span>](xref:Microsoft.Quantum.Canon.ApplyWith)