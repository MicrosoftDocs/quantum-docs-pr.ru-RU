---
uid: Microsoft.Quantum.Canon.ApplyToEachC
title: Операция Апплитоеачк
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachC
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `C` indicates that the single-qubit operation is controllable.
ms.openlocfilehash: b8b51e1c8d52c140c3ca1e5a54d0bd4cf4873046
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850853"
---
# <a name="applytoeachc-operation"></a><span data-ttu-id="759f6-102">Операция Апплитоеачк</span><span class="sxs-lookup"><span data-stu-id="759f6-102">ApplyToEachC operation</span></span>

<span data-ttu-id="759f6-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="759f6-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="759f6-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="759f6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="759f6-105">Применяет одну операцию кубит к каждому элементу в регистре.</span><span class="sxs-lookup"><span data-stu-id="759f6-105">Applies a single-qubit operation to each element in a register.</span></span>
<span data-ttu-id="759f6-106">Модификатор `C` указывает, что операция с одним кубит является управляемой.</span><span class="sxs-lookup"><span data-stu-id="759f6-106">The modifier `C` indicates that the single-qubit operation is controllable.</span></span>

```qsharp
operation ApplyToEachC<'T> (singleElementOperation : ('T => Unit is Ctl), register : 'T[]) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="759f6-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="759f6-107">Input</span></span>

### <a name="singleelementoperation--t--unit--is-ctl"></a><span data-ttu-id="759f6-108">Синглилементоператион: не>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — CTL</span><span class="sxs-lookup"><span data-stu-id="759f6-108">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="759f6-109">Операция, применяемая к каждому кубит.</span><span class="sxs-lookup"><span data-stu-id="759f6-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="759f6-110">Register: не []</span><span class="sxs-lookup"><span data-stu-id="759f6-110">register : 'T[]</span></span>

<span data-ttu-id="759f6-111">Массив Кубитс, для которого применяется заданная операция.</span><span class="sxs-lookup"><span data-stu-id="759f6-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="759f6-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="759f6-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="759f6-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="759f6-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="759f6-114">Е</span><span class="sxs-lookup"><span data-stu-id="759f6-114">'T</span></span>

<span data-ttu-id="759f6-115">Целевой объект, на котором действует операция.</span><span class="sxs-lookup"><span data-stu-id="759f6-115">The target on which the operation acts.</span></span>

## <a name="example"></a><span data-ttu-id="759f6-116">Пример</span><span class="sxs-lookup"><span data-stu-id="759f6-116">Example</span></span>

<span data-ttu-id="759f6-117">Подготовьте три-кубит $ \кет{+} $ State:</span><span class="sxs-lookup"><span data-stu-id="759f6-117">Prepare a three-qubit $\ket{+}$ state:</span></span>

```qsharp
using (register = Qubit[3]) {
    ApplyToEach(H, register);
}
```

## <a name="see-also"></a><span data-ttu-id="759f6-118">См. также:</span><span class="sxs-lookup"><span data-stu-id="759f6-118">See Also</span></span>

- [<span data-ttu-id="759f6-119">Microsoft. тактов. Canon. Апплитоеач</span><span class="sxs-lookup"><span data-stu-id="759f6-119">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)