---
uid: Microsoft.Quantum.Canon.ApplyToEach
title: Операция Апплитоеач
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEach
qsharp.summary: Applies a single-qubit operation to each element in a register.
ms.openlocfilehash: 11f9363feb38676df3f805496c74036aa96160c1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217872"
---
# <a name="applytoeach-operation"></a><span data-ttu-id="158fb-102">Операция Апплитоеач</span><span class="sxs-lookup"><span data-stu-id="158fb-102">ApplyToEach operation</span></span>

<span data-ttu-id="158fb-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="158fb-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="158fb-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="158fb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="158fb-105">Применяет одну операцию кубит к каждому элементу в регистре.</span><span class="sxs-lookup"><span data-stu-id="158fb-105">Applies a single-qubit operation to each element in a register.</span></span>

```qsharp
operation ApplyToEach<'T> (singleElementOperation : ('T => Unit), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="158fb-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="158fb-106">Input</span></span>

### <a name="singleelementoperation--t--unit"></a><span data-ttu-id="158fb-107">Синглилементоператион: 'T = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="158fb-107">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="158fb-108">Операция, применяемая к каждому кубит.</span><span class="sxs-lookup"><span data-stu-id="158fb-108">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="158fb-109">Register: не []</span><span class="sxs-lookup"><span data-stu-id="158fb-109">register : 'T[]</span></span>

<span data-ttu-id="158fb-110">Массив Кубитс, для которого применяется заданная операция.</span><span class="sxs-lookup"><span data-stu-id="158fb-110">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="158fb-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="158fb-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="158fb-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="158fb-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="158fb-113">Е</span><span class="sxs-lookup"><span data-stu-id="158fb-113">'T</span></span>

<span data-ttu-id="158fb-114">Целевой объект, на котором действует операция.</span><span class="sxs-lookup"><span data-stu-id="158fb-114">The target on which the operation acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="158fb-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="158fb-115">See Also</span></span>

- [<span data-ttu-id="158fb-116">Microsoft. тактов. Canon. Апплитоеачк</span><span class="sxs-lookup"><span data-stu-id="158fb-116">Microsoft.Quantum.Canon.ApplyToEachC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachC)
- [<span data-ttu-id="158fb-117">Microsoft. тактов. Canon. Апплитоеача</span><span class="sxs-lookup"><span data-stu-id="158fb-117">Microsoft.Quantum.Canon.ApplyToEachA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachA)
- [<span data-ttu-id="158fb-118">Microsoft. тактов. Canon. Апплитоеачка</span><span class="sxs-lookup"><span data-stu-id="158fb-118">Microsoft.Quantum.Canon.ApplyToEachCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachCA)