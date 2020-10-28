---
uid: Microsoft.Quantum.Canon.ApplyToEachC
title: Операция Апплитоеачк
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachC
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `C` indicates that the single-qubit operation is controllable.
ms.openlocfilehash: dfa18b6eb7a2c42fa2982994a2fc92170b52599c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717567"
---
# <a name="applytoeachc-operation"></a><span data-ttu-id="21fa2-102">Операция Апплитоеачк</span><span class="sxs-lookup"><span data-stu-id="21fa2-102">ApplyToEachC operation</span></span>

<span data-ttu-id="21fa2-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="21fa2-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="21fa2-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="21fa2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="21fa2-105">Применяет одну операцию кубит к каждому элементу в регистре.</span><span class="sxs-lookup"><span data-stu-id="21fa2-105">Applies a single-qubit operation to each element in a register.</span></span>
<span data-ttu-id="21fa2-106">Модификатор `C` указывает, что операция с одним кубит является управляемой.</span><span class="sxs-lookup"><span data-stu-id="21fa2-106">The modifier `C` indicates that the single-qubit operation is controllable.</span></span>

```qsharp
operation ApplyToEachC<'T> (singleElementOperation : ('T => Unit is Ctl), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="21fa2-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="21fa2-107">Input</span></span>

### <a name="singleelementoperation--t--unit-ctl"></a><span data-ttu-id="21fa2-108">Синглилементоператион: 'T = список CTL для [единицы](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="21fa2-108">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="21fa2-109">Операция, применяемая к каждому кубит.</span><span class="sxs-lookup"><span data-stu-id="21fa2-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="21fa2-110">Register: не []</span><span class="sxs-lookup"><span data-stu-id="21fa2-110">register : 'T[]</span></span>

<span data-ttu-id="21fa2-111">Массив Кубитс, для которого применяется заданная операция.</span><span class="sxs-lookup"><span data-stu-id="21fa2-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="21fa2-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="21fa2-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="21fa2-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="21fa2-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="21fa2-114">Е</span><span class="sxs-lookup"><span data-stu-id="21fa2-114">'T</span></span>

<span data-ttu-id="21fa2-115">Целевой объект, на котором действует операция.</span><span class="sxs-lookup"><span data-stu-id="21fa2-115">The target on which the operation acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="21fa2-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="21fa2-116">See Also</span></span>

- [<span data-ttu-id="21fa2-117">Microsoft. тактов. Canon. Апплитоеач</span><span class="sxs-lookup"><span data-stu-id="21fa2-117">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)