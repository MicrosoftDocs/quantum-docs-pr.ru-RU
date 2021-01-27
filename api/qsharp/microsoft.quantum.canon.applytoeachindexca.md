---
uid: Microsoft.Quantum.Canon.ApplyToEachIndexCA
title: Операция Апплитоеачиндекска
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndexCA
qsharp.summary: Applies a single-qubit operation to each indexed element in a register. The modifier `CA` indicates that the single-qubit operation is adjointable and controllable.
ms.openlocfilehash: 5046edc54576420bd8919ca52947076aed17cbce
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850799"
---
# <a name="applytoeachindexca-operation"></a><span data-ttu-id="92992-102">Операция Апплитоеачиндекска</span><span class="sxs-lookup"><span data-stu-id="92992-102">ApplyToEachIndexCA operation</span></span>

<span data-ttu-id="92992-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="92992-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="92992-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="92992-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="92992-105">Применяет одну операцию кубит к каждому индексированному элементу в регистре.</span><span class="sxs-lookup"><span data-stu-id="92992-105">Applies a single-qubit operation to each indexed element in a register.</span></span>
<span data-ttu-id="92992-106">Модификатор `CA` указывает, что операция с одним кубитом является аджоинтабле и управляемой.</span><span class="sxs-lookup"><span data-stu-id="92992-106">The modifier `CA` indicates that the single-qubit operation is adjointable and controllable.</span></span>

```qsharp
operation ApplyToEachIndexCA<'T> (singleElementOperation : ((Int, 'T) => Unit is Adj + Ctl), register : 'T[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="92992-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="92992-107">Input</span></span>

### <a name="singleelementoperation--intt--unit--is-adj--ctl"></a><span data-ttu-id="92992-108">Синглилементоператион: ([int](xref:microsoft.quantum.lang-ref.int), 't) => [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="92992-108">singleElementOperation : ([Int](xref:microsoft.quantum.lang-ref.int),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="92992-109">Операция, применяемая к каждому кубит.</span><span class="sxs-lookup"><span data-stu-id="92992-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="92992-110">Register: не []</span><span class="sxs-lookup"><span data-stu-id="92992-110">register : 'T[]</span></span>

<span data-ttu-id="92992-111">Массив Кубитс, для которого применяется заданная операция.</span><span class="sxs-lookup"><span data-stu-id="92992-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="92992-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="92992-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="92992-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="92992-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="92992-114">Е</span><span class="sxs-lookup"><span data-stu-id="92992-114">'T</span></span>

<span data-ttu-id="92992-115">Целевой объект, на котором действует каждая из операций.</span><span class="sxs-lookup"><span data-stu-id="92992-115">The target on which each of the operations acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="92992-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="92992-116">See Also</span></span>

- [<span data-ttu-id="92992-117">Microsoft. тактов. Canon. Апплитоеачиндекс</span><span class="sxs-lookup"><span data-stu-id="92992-117">Microsoft.Quantum.Canon.ApplyToEachIndex</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndex)