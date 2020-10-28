---
uid: Microsoft.Quantum.Canon.ApplyToEachA
title: Операция Апплитоеача
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachA
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `A` indicates that the single-qubit operation is adjointable.
ms.openlocfilehash: 9485c6549ed4e1a6fb3abdfa3f85ba35579d8b0b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717581"
---
# <a name="applytoeacha-operation"></a><span data-ttu-id="267ec-102">Операция Апплитоеача</span><span class="sxs-lookup"><span data-stu-id="267ec-102">ApplyToEachA operation</span></span>

<span data-ttu-id="267ec-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="267ec-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="267ec-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="267ec-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="267ec-105">Применяет одну операцию кубит к каждому элементу в регистре.</span><span class="sxs-lookup"><span data-stu-id="267ec-105">Applies a single-qubit operation to each element in a register.</span></span>
<span data-ttu-id="267ec-106">Модификатор `A` указывает, что единственной операцией кубит является аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="267ec-106">The modifier `A` indicates that the single-qubit operation is adjointable.</span></span>

```qsharp
operation ApplyToEachA<'T> (singleElementOperation : ('T => Unit is Adj), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="267ec-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="267ec-107">Input</span></span>

### <a name="singleelementoperation--t--unit-adj"></a><span data-ttu-id="267ec-108">Синглилементоператион: 'T [=>ное](xref:microsoft.quantum.lang-ref.unit) прогода</span><span class="sxs-lookup"><span data-stu-id="267ec-108">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="267ec-109">Операция, применяемая к каждому кубит.</span><span class="sxs-lookup"><span data-stu-id="267ec-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="267ec-110">Register: не []</span><span class="sxs-lookup"><span data-stu-id="267ec-110">register : 'T[]</span></span>

<span data-ttu-id="267ec-111">Массив Кубитс, для которого применяется заданная операция.</span><span class="sxs-lookup"><span data-stu-id="267ec-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="267ec-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="267ec-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="267ec-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="267ec-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="267ec-114">Е</span><span class="sxs-lookup"><span data-stu-id="267ec-114">'T</span></span>

<span data-ttu-id="267ec-115">Целевой объект, на котором действует операция.</span><span class="sxs-lookup"><span data-stu-id="267ec-115">The target on which the operation acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="267ec-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="267ec-116">See Also</span></span>

- [<span data-ttu-id="267ec-117">Microsoft. тактов. Canon. Апплитоеач</span><span class="sxs-lookup"><span data-stu-id="267ec-117">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)