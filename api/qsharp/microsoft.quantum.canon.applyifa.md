---
uid: Microsoft.Quantum.Canon.ApplyIfA
title: Операция Апплифа
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfA
qsharp.summary: Applies a adjointable operation conditioned on a classical bit.
ms.openlocfilehash: 8bdca1bf286d564dfbb540bc9d63c035d2196f00
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845039"
---
# <a name="applyifa-operation"></a><span data-ttu-id="811d8-102">Операция Апплифа</span><span class="sxs-lookup"><span data-stu-id="811d8-102">ApplyIfA operation</span></span>

<span data-ttu-id="811d8-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="811d8-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="811d8-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="811d8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="811d8-105">Применяет операцию аджоинтабле к классическому биту.</span><span class="sxs-lookup"><span data-stu-id="811d8-105">Applies a adjointable operation conditioned on a classical bit.</span></span>

```qsharp
operation ApplyIfA<'T> (op : ('T => Unit is Adj), bit : Bool, target : 'T) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="811d8-106">Описание</span><span class="sxs-lookup"><span data-stu-id="811d8-106">Description</span></span>

<span data-ttu-id="811d8-107">При наличии операции `op` и битового значения `bit` применяется `op` к, `target` Если имеет `bit` значение `true` .</span><span class="sxs-lookup"><span data-stu-id="811d8-107">Given an operation `op` and a bit value `bit`, applies `op` to the `target` if `bit` is `true`.</span></span> <span data-ttu-id="811d8-108">Если значение `false` равно, то ничего не происходит с `target` .</span><span class="sxs-lookup"><span data-stu-id="811d8-108">If `false`, nothing happens to the `target`.</span></span>
<span data-ttu-id="811d8-109">Суффикс `A` указывает, что операция, которую необходимо применить, — аджоинтабле.</span><span class="sxs-lookup"><span data-stu-id="811d8-109">The suffix `A` indicates that the operation to be applied is adjointable.</span></span>

## <a name="input"></a><span data-ttu-id="811d8-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="811d8-110">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="811d8-111">Op: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  является просуммой</span><span class="sxs-lookup"><span data-stu-id="811d8-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="811d8-112">Операция, применяемая к условию.</span><span class="sxs-lookup"><span data-stu-id="811d8-112">An operation to be conditionally applied.</span></span>


### <a name="bit--bool"></a><span data-ttu-id="811d8-113">bit: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="811d8-113">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="811d8-114">Логическое значение, определяющее, применяется ли оператор Op.</span><span class="sxs-lookup"><span data-stu-id="811d8-114">a boolean that controls whether op is applied or not.</span></span>


### <a name="target--t"></a><span data-ttu-id="811d8-115">Целевой объект: 'T</span><span class="sxs-lookup"><span data-stu-id="811d8-115">target : 'T</span></span>

<span data-ttu-id="811d8-116">Входные данные, к которым применяется операция.</span><span class="sxs-lookup"><span data-stu-id="811d8-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="811d8-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="811d8-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="811d8-118">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="811d8-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="811d8-119">Е</span><span class="sxs-lookup"><span data-stu-id="811d8-119">'T</span></span>

<span data-ttu-id="811d8-120">Тип входных данных операции, которая должна применяться условно.</span><span class="sxs-lookup"><span data-stu-id="811d8-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="example"></a><span data-ttu-id="811d8-121">Пример</span><span class="sxs-lookup"><span data-stu-id="811d8-121">Example</span></span>

<span data-ttu-id="811d8-122">Следующий командлет готовит регистр Кубитс в вычислительное состояние, представленное классическим битом строки, заданным как массив `Bool` значений:</span><span class="sxs-lookup"><span data-stu-id="811d8-122">The following prepares a register of qubits into a computational basis state represented by a classical bit string given as an array of `Bool` values:</span></span>

```qsharp
let bitstring = [true, false, true];
using (register = Qubit(3)) {
    ApplyToEach(ApplyIf(X, _, _), Zipped(bitstring, register));
    // register should now be in the state |101⟩.
    ...
}
```

## <a name="see-also"></a><span data-ttu-id="811d8-123">См. также:</span><span class="sxs-lookup"><span data-stu-id="811d8-123">See Also</span></span>

- [<span data-ttu-id="811d8-124">Microsoft. тактов. Canon. Апплифк</span><span class="sxs-lookup"><span data-stu-id="811d8-124">Microsoft.Quantum.Canon.ApplyIfC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [<span data-ttu-id="811d8-125">Microsoft. тактов. Canon. Апплифа</span><span class="sxs-lookup"><span data-stu-id="811d8-125">Microsoft.Quantum.Canon.ApplyIfA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [<span data-ttu-id="811d8-126">Microsoft. тактов. Canon. Апплифка</span><span class="sxs-lookup"><span data-stu-id="811d8-126">Microsoft.Quantum.Canon.ApplyIfCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfCA)