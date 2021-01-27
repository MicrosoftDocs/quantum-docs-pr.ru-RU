---
uid: Microsoft.Quantum.Canon.ApplyIf
title: Операция Апплиф
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIf
qsharp.summary: Applies an operation conditioned on a classical bit.
ms.openlocfilehash: 109a5c4748d183f199e420b4b1aef687613d220c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841871"
---
# <a name="applyif-operation"></a><span data-ttu-id="e917c-102">Операция Апплиф</span><span class="sxs-lookup"><span data-stu-id="e917c-102">ApplyIf operation</span></span>

<span data-ttu-id="e917c-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e917c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e917c-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e917c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e917c-105">Применяет операцию с условием на Классический бит.</span><span class="sxs-lookup"><span data-stu-id="e917c-105">Applies an operation conditioned on a classical bit.</span></span>

```qsharp
operation ApplyIf<'T> (op : ('T => Unit), bit : Bool, target : 'T) : Unit
```


## <a name="description"></a><span data-ttu-id="e917c-106">Описание</span><span class="sxs-lookup"><span data-stu-id="e917c-106">Description</span></span>

<span data-ttu-id="e917c-107">При наличии операции `op` и битового значения `bit` применяется `op` к, `target` Если имеет `bit` значение `true` .</span><span class="sxs-lookup"><span data-stu-id="e917c-107">Given an operation `op` and a bit value `bit`, applies `op` to the `target` if `bit` is `true`.</span></span> <span data-ttu-id="e917c-108">Если значение `false` равно, то ничего не происходит с `target` .</span><span class="sxs-lookup"><span data-stu-id="e917c-108">If `false`, nothing happens to the `target`.</span></span>

## <a name="input"></a><span data-ttu-id="e917c-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e917c-109">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="e917c-110">Op: t = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="e917c-110">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="e917c-111">Операция, применяемая к условию.</span><span class="sxs-lookup"><span data-stu-id="e917c-111">An operation to be conditionally applied.</span></span>


### <a name="bit--bool"></a><span data-ttu-id="e917c-112">bit: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="e917c-112">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="e917c-113">Логическое значение, определяющее, применяется ли оператор Op.</span><span class="sxs-lookup"><span data-stu-id="e917c-113">a boolean that controls whether op is applied or not.</span></span>


### <a name="target--t"></a><span data-ttu-id="e917c-114">Целевой объект: 'T</span><span class="sxs-lookup"><span data-stu-id="e917c-114">target : 'T</span></span>

<span data-ttu-id="e917c-115">Входные данные, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="e917c-115">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e917c-116">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e917c-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e917c-117">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="e917c-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e917c-118">Е</span><span class="sxs-lookup"><span data-stu-id="e917c-118">'T</span></span>

<span data-ttu-id="e917c-119">Тип входных данных операции, которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="e917c-119">The input type of the operation to be conditionally applied.</span></span>

## <a name="example"></a><span data-ttu-id="e917c-120">Пример</span><span class="sxs-lookup"><span data-stu-id="e917c-120">Example</span></span>

<span data-ttu-id="e917c-121">Следующий командлет готовит регистр Кубитс в вычислительное состояние, представленное классическим битом строки, заданным как массив `Bool` значений:</span><span class="sxs-lookup"><span data-stu-id="e917c-121">The following prepares a register of qubits into a computational basis state represented by a classical bit string given as an array of `Bool` values:</span></span>

```qsharp
let bitstring = [true, false, true];
using (register = Qubit(3)) {
    ApplyToEach(ApplyIf(X, _, _), Zipped(bitstring, register));
    // register should now be in the state |101⟩.
    ...
}
```

## <a name="see-also"></a><span data-ttu-id="e917c-122">См. также:</span><span class="sxs-lookup"><span data-stu-id="e917c-122">See Also</span></span>

- [<span data-ttu-id="e917c-123">Microsoft. тактов. Canon. Апплифк</span><span class="sxs-lookup"><span data-stu-id="e917c-123">Microsoft.Quantum.Canon.ApplyIfC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [<span data-ttu-id="e917c-124">Microsoft. тактов. Canon. Апплифа</span><span class="sxs-lookup"><span data-stu-id="e917c-124">Microsoft.Quantum.Canon.ApplyIfA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [<span data-ttu-id="e917c-125">Microsoft. тактов. Canon. Апплифка</span><span class="sxs-lookup"><span data-stu-id="e917c-125">Microsoft.Quantum.Canon.ApplyIfCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfCA)