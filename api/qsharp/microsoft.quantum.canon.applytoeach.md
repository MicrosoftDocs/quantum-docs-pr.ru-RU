---
uid: Microsoft.Quantum.Canon.ApplyToEach
title: Операция Апплитоеач
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEach
qsharp.summary: Applies a single-qubit operation to each element in a register.
ms.openlocfilehash: e1625829e2e9efd9d39fe0692f01c1cbbffc651c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717595"
---
# <a name="applytoeach-operation"></a><span data-ttu-id="97225-102">Операция Апплитоеач</span><span class="sxs-lookup"><span data-stu-id="97225-102">ApplyToEach operation</span></span>

<span data-ttu-id="97225-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="97225-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="97225-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="97225-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="97225-105">Применяет одну операцию кубит к каждому элементу в регистре.</span><span class="sxs-lookup"><span data-stu-id="97225-105">Applies a single-qubit operation to each element in a register.</span></span>

```qsharp
operation ApplyToEach<'T> (singleElementOperation : ('T => Unit), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="97225-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="97225-106">Input</span></span>

### <a name="singleelementoperation--t--unit"></a><span data-ttu-id="97225-107">Синглилементоператион: 'T = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="97225-107">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="97225-108">Операция, применяемая к каждому кубит.</span><span class="sxs-lookup"><span data-stu-id="97225-108">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="97225-109">Register: не []</span><span class="sxs-lookup"><span data-stu-id="97225-109">register : 'T[]</span></span>

<span data-ttu-id="97225-110">Массив Кубитс, для которого применяется заданная операция.</span><span class="sxs-lookup"><span data-stu-id="97225-110">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="97225-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="97225-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="97225-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="97225-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="97225-113">Е</span><span class="sxs-lookup"><span data-stu-id="97225-113">'T</span></span>

<span data-ttu-id="97225-114">Целевой объект, на котором действует операция.</span><span class="sxs-lookup"><span data-stu-id="97225-114">The target on which the operation acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="97225-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="97225-115">See Also</span></span>

- [<span data-ttu-id="97225-116">Microsoft. тактов. Canon. Апплитоеачк</span><span class="sxs-lookup"><span data-stu-id="97225-116">Microsoft.Quantum.Canon.ApplyToEachC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachC)
- [<span data-ttu-id="97225-117">Microsoft. тактов. Canon. Апплитоеача</span><span class="sxs-lookup"><span data-stu-id="97225-117">Microsoft.Quantum.Canon.ApplyToEachA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachA)
- [<span data-ttu-id="97225-118">Microsoft. тактов. Canon. Апплитоеачка</span><span class="sxs-lookup"><span data-stu-id="97225-118">Microsoft.Quantum.Canon.ApplyToEachCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachCA)