---
uid: Microsoft.Quantum.Canon.ApplyToEachIndexA
title: Операция Апплитоеачиндекса
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndexA
qsharp.summary: Applies a single-qubit operation to each indexed element in a register. The modifier `A` indicates that the single-qubit operation is adjointable.
ms.openlocfilehash: 0fe0697e6f1d9441c2d2ad2c7396f6da8daa0e1e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717539"
---
# <a name="applytoeachindexa-operation"></a><span data-ttu-id="c290c-102">Операция Апплитоеачиндекса</span><span class="sxs-lookup"><span data-stu-id="c290c-102">ApplyToEachIndexA operation</span></span>

<span data-ttu-id="c290c-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c290c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c290c-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c290c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c290c-105">Применяет одну операцию кубит к каждому индексированному элементу в регистре.</span><span class="sxs-lookup"><span data-stu-id="c290c-105">Applies a single-qubit operation to each indexed element in a register.</span></span>
<span data-ttu-id="c290c-106">Модификатор `A` указывает, что единственной операцией кубит является аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="c290c-106">The modifier `A` indicates that the single-qubit operation is adjointable.</span></span>

```qsharp
operation ApplyToEachIndexA<'T> (singleElementOperation : ((Int, 'T) => Unit is Adj), register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="c290c-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c290c-107">Input</span></span>

### <a name="singleelementoperation--intt--unit-adj"></a><span data-ttu-id="c290c-108">Синглилементоператион: ([int](xref:microsoft.quantum.lang-ref.int), 't) [=>ное](xref:microsoft.quantum.lang-ref.unit) прогода</span><span class="sxs-lookup"><span data-stu-id="c290c-108">singleElementOperation : ([Int](xref:microsoft.quantum.lang-ref.int),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="c290c-109">Операция, применяемая к каждому кубит.</span><span class="sxs-lookup"><span data-stu-id="c290c-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="c290c-110">Register: не []</span><span class="sxs-lookup"><span data-stu-id="c290c-110">register : 'T[]</span></span>

<span data-ttu-id="c290c-111">Массив Кубитс, для которого применяется заданная операция.</span><span class="sxs-lookup"><span data-stu-id="c290c-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c290c-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c290c-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="c290c-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="c290c-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c290c-114">Е</span><span class="sxs-lookup"><span data-stu-id="c290c-114">'T</span></span>

<span data-ttu-id="c290c-115">Целевой объект, на котором действует каждая из операций.</span><span class="sxs-lookup"><span data-stu-id="c290c-115">The target on which each of the operations acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="c290c-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="c290c-116">See Also</span></span>

- [<span data-ttu-id="c290c-117">Microsoft. тактов. Canon. Апплитоеачиндекс</span><span class="sxs-lookup"><span data-stu-id="c290c-117">Microsoft.Quantum.Canon.ApplyToEachIndex</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndex)