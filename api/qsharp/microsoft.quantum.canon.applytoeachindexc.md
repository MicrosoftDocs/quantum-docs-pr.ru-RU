---
uid: Microsoft.Quantum.Canon.ApplyToEachIndexC
title: Операция Апплитоеачиндекск
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndexC
qsharp.summary: Applies a single-qubit operation to each indexed element in a register. The modifier `C` indicates that the single-qubit operation is controllable.
ms.openlocfilehash: c005f616d580438891fbcb9f3c727b8e961e138d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850810"
---
# <a name="applytoeachindexc-operation"></a><span data-ttu-id="1a2cd-102">Операция Апплитоеачиндекск</span><span class="sxs-lookup"><span data-stu-id="1a2cd-102">ApplyToEachIndexC operation</span></span>

<span data-ttu-id="1a2cd-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="1a2cd-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="1a2cd-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1a2cd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1a2cd-105">Применяет одну операцию кубит к каждому индексированному элементу в регистре.</span><span class="sxs-lookup"><span data-stu-id="1a2cd-105">Applies a single-qubit operation to each indexed element in a register.</span></span>
<span data-ttu-id="1a2cd-106">Модификатор `C` указывает, что операция с одним кубит является управляемой.</span><span class="sxs-lookup"><span data-stu-id="1a2cd-106">The modifier `C` indicates that the single-qubit operation is controllable.</span></span>

```qsharp
operation ApplyToEachIndexC<'T> (singleElementOperation : ((Int, 'T) => Unit is Ctl), register : 'T[]) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="1a2cd-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="1a2cd-107">Input</span></span>

### <a name="singleelementoperation--intt--unit--is-ctl"></a><span data-ttu-id="1a2cd-108">Синглилементоператион: ([int](xref:microsoft.quantum.lang-ref.int), 't) = [единица](xref:microsoft.quantum.lang-ref.unit) > является CTL</span><span class="sxs-lookup"><span data-stu-id="1a2cd-108">singleElementOperation : ([Int](xref:microsoft.quantum.lang-ref.int),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="1a2cd-109">Операция, применяемая к каждому кубит.</span><span class="sxs-lookup"><span data-stu-id="1a2cd-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="1a2cd-110">Register: не []</span><span class="sxs-lookup"><span data-stu-id="1a2cd-110">register : 'T[]</span></span>

<span data-ttu-id="1a2cd-111">Массив Кубитс, для которого применяется заданная операция.</span><span class="sxs-lookup"><span data-stu-id="1a2cd-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1a2cd-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1a2cd-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="1a2cd-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="1a2cd-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="1a2cd-114">Е</span><span class="sxs-lookup"><span data-stu-id="1a2cd-114">'T</span></span>

<span data-ttu-id="1a2cd-115">Целевой объект, на котором действует каждая из операций.</span><span class="sxs-lookup"><span data-stu-id="1a2cd-115">The target on which each of the operations acts.</span></span>

## <a name="see-also"></a><span data-ttu-id="1a2cd-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="1a2cd-116">See Also</span></span>

- [<span data-ttu-id="1a2cd-117">Microsoft. тактов. Canon. Апплитоеачиндекс</span><span class="sxs-lookup"><span data-stu-id="1a2cd-117">Microsoft.Quantum.Canon.ApplyToEachIndex</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEachIndex)