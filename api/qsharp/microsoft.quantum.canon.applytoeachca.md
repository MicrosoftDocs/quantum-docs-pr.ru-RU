---
uid: Microsoft.Quantum.Canon.ApplyToEachCA
title: Операция Апплитоеачка
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachCA
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.
ms.openlocfilehash: c85b33760eba8d10d9650be2f8306e4afdd1f307
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841487"
---
# <a name="applytoeachca-operation"></a><span data-ttu-id="fbb7a-102">Операция Апплитоеачка</span><span class="sxs-lookup"><span data-stu-id="fbb7a-102">ApplyToEachCA operation</span></span>

<span data-ttu-id="fbb7a-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="fbb7a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="fbb7a-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fbb7a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fbb7a-105">Применяет одну операцию кубит к каждому элементу в регистре.</span><span class="sxs-lookup"><span data-stu-id="fbb7a-105">Applies a single-qubit operation to each element in a register.</span></span>
<span data-ttu-id="fbb7a-106">Модификатор `CA` указывает, что одна операция кубит является управляемой и аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="fbb7a-106">The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyToEachCA<'T> (singleElementOperation : ('T => Unit is Adj + Ctl), register : 'T[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="fbb7a-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="fbb7a-107">Input</span></span>

### <a name="singleelementoperation--t--unit--is-adj--ctl"></a><span data-ttu-id="fbb7a-108">Синглилементоператион: не>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="fbb7a-108">singleElementOperation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="fbb7a-109">Операция, применяемая к каждому кубит.</span><span class="sxs-lookup"><span data-stu-id="fbb7a-109">Operation to apply to each qubit.</span></span>


### <a name="register--t"></a><span data-ttu-id="fbb7a-110">Register: не []</span><span class="sxs-lookup"><span data-stu-id="fbb7a-110">register : 'T[]</span></span>

<span data-ttu-id="fbb7a-111">Массив Кубитс, для которого применяется заданная операция.</span><span class="sxs-lookup"><span data-stu-id="fbb7a-111">Array of qubits on which to apply the given operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="fbb7a-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fbb7a-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="fbb7a-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="fbb7a-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="fbb7a-114">Е</span><span class="sxs-lookup"><span data-stu-id="fbb7a-114">'T</span></span>

<span data-ttu-id="fbb7a-115">Целевой объект, на котором действует операция.</span><span class="sxs-lookup"><span data-stu-id="fbb7a-115">The target on which the operation acts.</span></span>

## <a name="example"></a><span data-ttu-id="fbb7a-116">Пример</span><span class="sxs-lookup"><span data-stu-id="fbb7a-116">Example</span></span>

<span data-ttu-id="fbb7a-117">Подготовьте три-кубит $ \кет{+} $ State:</span><span class="sxs-lookup"><span data-stu-id="fbb7a-117">Prepare a three-qubit $\ket{+}$ state:</span></span>

```qsharp
using (register = Qubit[3]) {
    ApplyToEach(H, register);
}
```

## <a name="see-also"></a><span data-ttu-id="fbb7a-118">См. также:</span><span class="sxs-lookup"><span data-stu-id="fbb7a-118">See Also</span></span>

- [<span data-ttu-id="fbb7a-119">Microsoft. тактов. Canon. Апплитоеач</span><span class="sxs-lookup"><span data-stu-id="fbb7a-119">Microsoft.Quantum.Canon.ApplyToEach</span></span>](xref:Microsoft.Quantum.Canon.ApplyToEach)