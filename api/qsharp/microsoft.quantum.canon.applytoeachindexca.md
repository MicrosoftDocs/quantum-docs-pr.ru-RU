---
uid: Microsoft.Quantum.Canon.ApplyToEachIndexCA
title: Операция Апплитоеачиндекска
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndexCA
qsharp.summary: Applies a single-qubit operation to each indexed element in a register. The modifier `CA` indicates that the single-qubit operation is adjointable and controllable.
ms.openlocfilehash: c5bb61aadbdaab9c74a3dcd418088c532b495ff5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717512"
---
# <a name="applytoeachindexca-operation"></a><span data-ttu-id="5db6c-102">Операция Апплитоеачиндекска</span><span class="sxs-lookup"><span data-stu-id="5db6c-102">ApplyToEachIndexCA operation</span></span>

<span data-ttu-id="5db6c-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5db6c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5db6c-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5db6c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5db6c-105">Применяет одну операцию кубит к каждому индексированному элементу в регистре.</span><span class="sxs-lookup"><span data-stu-id="5db6c-105">Applies a single-qubit operation to each indexed element in a register.</span></span>
<span data-ttu-id="5db6c-106">Модификатор `CA` указывает, что операция с одним кубитом является аджоинтабле и управляемой.</span><span class="sxs-lookup"><span data-stu-id="5db6c-106">The modifier `CA` indicates that the single-qubit operation is adjointable and controllable.</span></span>

```qsharp
operation ApplyToEachIndexCA<'T> (singleElementOperation : ((Int, 'T) => Unit is Adj + Ctl), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="5db6c-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5db6c-107">Input</span></span>

### <a name="singleelementoperation--intt--unit-adj--ctl"></a><span data-ttu-id="5db6c-108">Синглилементоператион: ([int](xref:microsoft.quantum.lang-ref.int), 't) =>ная начисление [единиц](xref:microsoft.quantum.lang-ref.unit) + CTL</span><span class="sxs-lookup"><span data-stu-id="5db6c-108">singleElementOperation : ([Int](xref:microsoft.quantum.lang-ref.int),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="5db6c-109">Операция, применяемая к каждому кубит.</span><span class="sxs-lookup"><span data-stu-id="5db6c-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="5db6c-110">Register: не []</span><span class="sxs-lookup"><span data-stu-id="5db6c-110">register : 'T[]</span></span>

<span data-ttu-id="5db6c-111">Массив Кубитс, для которого применяется заданная операция.</span><span class="sxs-lookup"><span data-stu-id="5db6c-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5db6c-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5db6c-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="5db6c-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="5db6c-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5db6c-114">Е</span><span class="sxs-lookup"><span data-stu-id="5db6c-114">'T</span></span>

<span data-ttu-id="5db6c-115">Целевой объект, на котором действует каждая из операций.</span><span class="sxs-lookup"><span data-stu-id="5db6c-115">The target on which each of the operations acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="5db6c-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="5db6c-116">See Also</span></span>

- [<span data-ttu-id="5db6c-117">Microsoft. тактов. Canon. Апплитоеачиндекс</span><span class="sxs-lookup"><span data-stu-id="5db6c-117">Microsoft.Quantum.Canon.ApplyToEachIndex</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndex)