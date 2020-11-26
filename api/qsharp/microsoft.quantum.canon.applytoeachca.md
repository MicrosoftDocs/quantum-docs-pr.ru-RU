---
uid: Microsoft.Quantum.Canon.ApplyToEachCA
title: Операция Апплитоеачка
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachCA
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.
ms.openlocfilehash: dcfd4619a77413e71044e6a7d5fc19a9f22bbf94
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217753"
---
# <a name="applytoeachca-operation"></a><span data-ttu-id="6a0c0-102">Операция Апплитоеачка</span><span class="sxs-lookup"><span data-stu-id="6a0c0-102">ApplyToEachCA operation</span></span>

<span data-ttu-id="6a0c0-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="6a0c0-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="6a0c0-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6a0c0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6a0c0-105">Применяет одну операцию кубит к каждому элементу в регистре.</span><span class="sxs-lookup"><span data-stu-id="6a0c0-105">Applies a single-qubit operation to each element in a register.</span></span>
<span data-ttu-id="6a0c0-106">Модификатор `CA` указывает, что одна операция кубит является управляемой и аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="6a0c0-106">The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyToEachCA<'T> (singleElementOperation : ('T => Unit is Adj + Ctl), register : 'T[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="6a0c0-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="6a0c0-107">Input</span></span>

### <a name="singleelementoperation--t--unit--is-adj--ctl"></a><span data-ttu-id="6a0c0-108">Синглилементоператион: не>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="6a0c0-108">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="6a0c0-109">Операция, применяемая к каждому кубит.</span><span class="sxs-lookup"><span data-stu-id="6a0c0-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="6a0c0-110">Register: не []</span><span class="sxs-lookup"><span data-stu-id="6a0c0-110">register : 'T[]</span></span>

<span data-ttu-id="6a0c0-111">Массив Кубитс, для которого применяется заданная операция.</span><span class="sxs-lookup"><span data-stu-id="6a0c0-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="6a0c0-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6a0c0-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="6a0c0-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="6a0c0-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6a0c0-114">Е</span><span class="sxs-lookup"><span data-stu-id="6a0c0-114">'T</span></span>

<span data-ttu-id="6a0c0-115">Целевой объект, на котором действует операция.</span><span class="sxs-lookup"><span data-stu-id="6a0c0-115">The target on which the operation acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="6a0c0-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="6a0c0-116">See Also</span></span>

- [<span data-ttu-id="6a0c0-117">Microsoft. тактов. Canon. Апплитоеач</span><span class="sxs-lookup"><span data-stu-id="6a0c0-117">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)