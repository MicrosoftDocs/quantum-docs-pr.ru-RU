---
uid: Microsoft.Quantum.Canon.ApplyToEachA
title: Операция Апплитоеача
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachA
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `A` indicates that the single-qubit operation is adjointable.
ms.openlocfilehash: 9819e78760caf6180edc5c2ca5e402060e3029a5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217804"
---
# <a name="applytoeacha-operation"></a><span data-ttu-id="194c7-102">Операция Апплитоеача</span><span class="sxs-lookup"><span data-stu-id="194c7-102">ApplyToEachA operation</span></span>

<span data-ttu-id="194c7-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="194c7-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="194c7-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="194c7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="194c7-105">Применяет одну операцию кубит к каждому элементу в регистре.</span><span class="sxs-lookup"><span data-stu-id="194c7-105">Applies a single-qubit operation to each element in a register.</span></span>
<span data-ttu-id="194c7-106">Модификатор `A` указывает, что единственной операцией кубит является аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="194c7-106">The modifier `A` indicates that the single-qubit operation is adjointable.</span></span>

```qsharp
operation ApplyToEachA<'T> (singleElementOperation : ('T => Unit is Adj), register : 'T[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="194c7-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="194c7-107">Input</span></span>

### <a name="singleelementoperation--t--unit--is-adj"></a><span data-ttu-id="194c7-108">Синглилементоператион: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)  Нагода</span><span class="sxs-lookup"><span data-stu-id="194c7-108">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="194c7-109">Операция, применяемая к каждому кубит.</span><span class="sxs-lookup"><span data-stu-id="194c7-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="194c7-110">Register: не []</span><span class="sxs-lookup"><span data-stu-id="194c7-110">register : 'T[]</span></span>

<span data-ttu-id="194c7-111">Массив Кубитс, для которого применяется заданная операция.</span><span class="sxs-lookup"><span data-stu-id="194c7-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="194c7-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="194c7-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="194c7-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="194c7-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="194c7-114">Е</span><span class="sxs-lookup"><span data-stu-id="194c7-114">'T</span></span>

<span data-ttu-id="194c7-115">Целевой объект, на котором действует операция.</span><span class="sxs-lookup"><span data-stu-id="194c7-115">The target on which the operation acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="194c7-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="194c7-116">See Also</span></span>

- [<span data-ttu-id="194c7-117">Microsoft. тактов. Canon. Апплитоеач</span><span class="sxs-lookup"><span data-stu-id="194c7-117">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)