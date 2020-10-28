---
uid: Microsoft.Quantum.Canon.ApplyToEachCA
title: Операция Апплитоеачка
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachCA
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.
ms.openlocfilehash: b24fbb8c7a1a55c0a7750c5d096a61f4824dadfb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717553"
---
# <a name="applytoeachca-operation"></a><span data-ttu-id="389a6-102">Операция Апплитоеачка</span><span class="sxs-lookup"><span data-stu-id="389a6-102">ApplyToEachCA operation</span></span>

<span data-ttu-id="389a6-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="389a6-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="389a6-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="389a6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="389a6-105">Применяет одну операцию кубит к каждому элементу в регистре.</span><span class="sxs-lookup"><span data-stu-id="389a6-105">Applies a single-qubit operation to each element in a register.</span></span>
<span data-ttu-id="389a6-106">Модификатор `CA` указывает, что одна операция кубит является управляемой и аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="389a6-106">The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyToEachCA<'T> (singleElementOperation : ('T => Unit is Adj + Ctl), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="389a6-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="389a6-107">Input</span></span>

### <a name="singleelementoperation--t--unit-adj--ctl"></a><span data-ttu-id="389a6-108">Синглилементоператион: 'T => [модульные](xref:microsoft.quantum.lang-ref.unit) года + CTL</span><span class="sxs-lookup"><span data-stu-id="389a6-108">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="389a6-109">Операция, применяемая к каждому кубит.</span><span class="sxs-lookup"><span data-stu-id="389a6-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="389a6-110">Register: не []</span><span class="sxs-lookup"><span data-stu-id="389a6-110">register : 'T[]</span></span>

<span data-ttu-id="389a6-111">Массив Кубитс, для которого применяется заданная операция.</span><span class="sxs-lookup"><span data-stu-id="389a6-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="389a6-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="389a6-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="389a6-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="389a6-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="389a6-114">Е</span><span class="sxs-lookup"><span data-stu-id="389a6-114">'T</span></span>

<span data-ttu-id="389a6-115">Целевой объект, на котором действует операция.</span><span class="sxs-lookup"><span data-stu-id="389a6-115">The target on which the operation acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="389a6-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="389a6-116">See Also</span></span>

- [<span data-ttu-id="389a6-117">Microsoft. тактов. Canon. Апплитоеач</span><span class="sxs-lookup"><span data-stu-id="389a6-117">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)