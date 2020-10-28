---
uid: Microsoft.Quantum.Canon.ApplyToEachIndexC
title: Операция Апплитоеачиндекск
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndexC
qsharp.summary: Applies a single-qubit operation to each indexed element in a register. The modifier `C` indicates that the single-qubit operation is controllable.
ms.openlocfilehash: 387d7ea24b9251386a71b42a1f51ce70933bf6fc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717526"
---
# <a name="applytoeachindexc-operation"></a><span data-ttu-id="46678-102">Операция Апплитоеачиндекск</span><span class="sxs-lookup"><span data-stu-id="46678-102">ApplyToEachIndexC operation</span></span>

<span data-ttu-id="46678-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="46678-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="46678-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="46678-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="46678-105">Применяет одну операцию кубит к каждому индексированному элементу в регистре.</span><span class="sxs-lookup"><span data-stu-id="46678-105">Applies a single-qubit operation to each indexed element in a register.</span></span>
<span data-ttu-id="46678-106">Модификатор `C` указывает, что операция с одним кубит является управляемой.</span><span class="sxs-lookup"><span data-stu-id="46678-106">The modifier `C` indicates that the single-qubit operation is controllable.</span></span>

```qsharp
operation ApplyToEachIndexC<'T> (singleElementOperation : ((Int, 'T) => Unit is Ctl), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="46678-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="46678-107">Input</span></span>

### <a name="singleelementoperation--intt--unit-ctl"></a><span data-ttu-id="46678-108">Синглилементоператион: ([int](xref:microsoft.quantum.lang-ref.int), t) = Ctl [единицы](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="46678-108">singleElementOperation : ([Int](xref:microsoft.quantum.lang-ref.int),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="46678-109">Операция, применяемая к каждому кубит.</span><span class="sxs-lookup"><span data-stu-id="46678-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="46678-110">Register: не []</span><span class="sxs-lookup"><span data-stu-id="46678-110">register : 'T[]</span></span>

<span data-ttu-id="46678-111">Массив Кубитс, для которого применяется заданная операция.</span><span class="sxs-lookup"><span data-stu-id="46678-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="46678-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="46678-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="46678-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="46678-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="46678-114">Е</span><span class="sxs-lookup"><span data-stu-id="46678-114">'T</span></span>

<span data-ttu-id="46678-115">Целевой объект, на котором действует каждая из операций.</span><span class="sxs-lookup"><span data-stu-id="46678-115">The target on which each of the operations acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="46678-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="46678-116">See Also</span></span>

- [<span data-ttu-id="46678-117">Microsoft. тактов. Canon. Апплитоеачиндекс</span><span class="sxs-lookup"><span data-stu-id="46678-117">Microsoft.Quantum.Canon.ApplyToEachIndex</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndex)