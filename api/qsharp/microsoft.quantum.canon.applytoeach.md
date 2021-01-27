---
uid: Microsoft.Quantum.Canon.ApplyToEach
title: Операция Апплитоеач
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEach
qsharp.summary: Applies a single-qubit operation to each element in a register.
ms.openlocfilehash: 61dda69751989ef8a98fa8fb01d832014ec4ad35
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844626"
---
# <a name="applytoeach-operation"></a><span data-ttu-id="6e31c-102">Операция Апплитоеач</span><span class="sxs-lookup"><span data-stu-id="6e31c-102">ApplyToEach operation</span></span>

<span data-ttu-id="6e31c-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="6e31c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="6e31c-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6e31c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6e31c-105">Применяет одну операцию кубит к каждому элементу в регистре.</span><span class="sxs-lookup"><span data-stu-id="6e31c-105">Applies a single-qubit operation to each element in a register.</span></span>

```qsharp
operation ApplyToEach<'T> (singleElementOperation : ('T => Unit), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="6e31c-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="6e31c-106">Input</span></span>

### <a name="singleelementoperation--t--unit"></a><span data-ttu-id="6e31c-107">Синглилементоператион: 'T = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="6e31c-107">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="6e31c-108">Операция, применяемая к каждому кубит.</span><span class="sxs-lookup"><span data-stu-id="6e31c-108">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="6e31c-109">Register: не []</span><span class="sxs-lookup"><span data-stu-id="6e31c-109">register : 'T[]</span></span>

<span data-ttu-id="6e31c-110">Массив Кубитс, для которого применяется заданная операция.</span><span class="sxs-lookup"><span data-stu-id="6e31c-110">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="6e31c-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6e31c-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="6e31c-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="6e31c-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6e31c-113">Е</span><span class="sxs-lookup"><span data-stu-id="6e31c-113">'T</span></span>

<span data-ttu-id="6e31c-114">Целевой объект, на котором действует операция.</span><span class="sxs-lookup"><span data-stu-id="6e31c-114">The target on which the operation acts.</span></span>

## <a name="example"></a><span data-ttu-id="6e31c-115">Пример</span><span class="sxs-lookup"><span data-stu-id="6e31c-115">Example</span></span>

<span data-ttu-id="6e31c-116">Подготовьте три-кубит $ \кет{+} $ State:</span><span class="sxs-lookup"><span data-stu-id="6e31c-116">Prepare a three-qubit $\ket{+}$ state:</span></span>

```qsharp
using (register = Qubit[3]) {
    ApplyToEach(H, register);
}
```

## <a name="see-also"></a><span data-ttu-id="6e31c-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="6e31c-117">See Also</span></span>

- [<span data-ttu-id="6e31c-118">Microsoft. тактов. Canon. Апплитоеачк</span><span class="sxs-lookup"><span data-stu-id="6e31c-118">Microsoft.Quantum.Canon.ApplyToEachC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachC)
- [<span data-ttu-id="6e31c-119">Microsoft. тактов. Canon. Апплитоеача</span><span class="sxs-lookup"><span data-stu-id="6e31c-119">Microsoft.Quantum.Canon.ApplyToEachA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachA)
- [<span data-ttu-id="6e31c-120">Microsoft. тактов. Canon. Апплитоеачка</span><span class="sxs-lookup"><span data-stu-id="6e31c-120">Microsoft.Quantum.Canon.ApplyToEachCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachCA)