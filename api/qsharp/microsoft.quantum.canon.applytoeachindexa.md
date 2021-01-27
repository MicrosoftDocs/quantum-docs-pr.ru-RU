---
uid: Microsoft.Quantum.Canon.ApplyToEachIndexA
title: Операция Апплитоеачиндекса
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndexA
qsharp.summary: Applies a single-qubit operation to each indexed element in a register. The modifier `A` indicates that the single-qubit operation is adjointable.
ms.openlocfilehash: fb278f217ac450ab48aa37b0035cd1bdd295d3e5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850829"
---
# <a name="applytoeachindexa-operation"></a><span data-ttu-id="c955e-102">Операция Апплитоеачиндекса</span><span class="sxs-lookup"><span data-stu-id="c955e-102">ApplyToEachIndexA operation</span></span>

<span data-ttu-id="c955e-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c955e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c955e-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c955e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c955e-105">Применяет одну операцию кубит к каждому индексированному элементу в регистре.</span><span class="sxs-lookup"><span data-stu-id="c955e-105">Applies a single-qubit operation to each indexed element in a register.</span></span>
<span data-ttu-id="c955e-106">Модификатор `A` указывает, что единственной операцией кубит является аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="c955e-106">The modifier `A` indicates that the single-qubit operation is adjointable.</span></span>

```qsharp
operation ApplyToEachIndexA<'T> (singleElementOperation : ((Int, 'T) => Unit is Adj), register : 'T[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="c955e-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c955e-107">Input</span></span>

### <a name="singleelementoperation--intt--unit--is-adj"></a><span data-ttu-id="c955e-108">Синглилементоператион: ([int](xref:microsoft.quantum.lang-ref.int), 't) = [единица](xref:microsoft.quantum.lang-ref.unit) > является просуммой</span><span class="sxs-lookup"><span data-stu-id="c955e-108">singleElementOperation : ([Int](xref:microsoft.quantum.lang-ref.int),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="c955e-109">Операция, применяемая к каждому кубит.</span><span class="sxs-lookup"><span data-stu-id="c955e-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="c955e-110">Register: не []</span><span class="sxs-lookup"><span data-stu-id="c955e-110">register : 'T[]</span></span>

<span data-ttu-id="c955e-111">Массив Кубитс, для которого применяется заданная операция.</span><span class="sxs-lookup"><span data-stu-id="c955e-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c955e-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c955e-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="c955e-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="c955e-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c955e-114">Е</span><span class="sxs-lookup"><span data-stu-id="c955e-114">'T</span></span>

<span data-ttu-id="c955e-115">Целевой объект, на котором действует каждая из операций.</span><span class="sxs-lookup"><span data-stu-id="c955e-115">The target on which each of the operations acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="c955e-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="c955e-116">See Also</span></span>

- [<span data-ttu-id="c955e-117">Microsoft. тактов. Canon. Апплитоеачиндекс</span><span class="sxs-lookup"><span data-stu-id="c955e-117">Microsoft.Quantum.Canon.ApplyToEachIndex</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndex)