---
uid: Microsoft.Quantum.Canon.MultiplexPauli
title: Операция Мултиплекспаули
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexPauli
qsharp.summary: Applies a Pauli rotation conditioned on an array of qubits.
ms.openlocfilehash: 656b510cb19af69a9a3f0d537d54b0abfe76de4b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852445"
---
# <a name="multiplexpauli-operation"></a><span data-ttu-id="e857b-102">Операция Мултиплекспаули</span><span class="sxs-lookup"><span data-stu-id="e857b-102">MultiplexPauli operation</span></span>

<span data-ttu-id="e857b-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e857b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e857b-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e857b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e857b-105">Применяет вращение Паули к массиву Кубитс.</span><span class="sxs-lookup"><span data-stu-id="e857b-105">Applies a Pauli rotation conditioned on an array of qubits.</span></span>

```qsharp
operation MultiplexPauli (coefficients : Double[], pauli : Pauli, control : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="e857b-106">Описание</span><span class="sxs-lookup"><span data-stu-id="e857b-106">Description</span></span>

<span data-ttu-id="e857b-107">Это применяет единую операцию умножения, которая выполняет повороты по угловому оператору $ \ theta_j $ о однокубит Паули operator $P $ при управлении $n $-кубит номер State $ \кет{ж} $.</span><span class="sxs-lookup"><span data-stu-id="e857b-107">This applies a multiply controlled unitary operation that performs rotations by angle $\theta_j$ about single-qubit Pauli operator $P$ when controlled by the $n$-qubit number state $\ket{j}$.</span></span>
<span data-ttu-id="e857b-108">В частности, действие этой операции представлено единым</span><span class="sxs-lookup"><span data-stu-id="e857b-108">In particular, the action of this operation is represented by the unitary</span></span>

<span data-ttu-id="e857b-109">$ $ \бегин{алигн} U = \сум ^ {2 ^ n-1} _ {j = 0} \кет{ж}\бра{ж} \отимес e ^ {i P \ theta_j}.</span><span class="sxs-lookup"><span data-stu-id="e857b-109">$$ \begin{align} U = \sum^{2^n - 1}_{j=0} \ket{j}\bra{j} \otimes e^{i P \theta_j}.</span></span>
<span data-ttu-id="e857b-110">\енд{алигн} $ $</span><span class="sxs-lookup"><span data-stu-id="e857b-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="e857b-111">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e857b-111">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="e857b-112">коэффициенты: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="e857b-112">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="e857b-113">Массив до $2 ^ n $ коэффициенты $ \ theta_j $.</span><span class="sxs-lookup"><span data-stu-id="e857b-113">Array of up to $2^n$ coefficients $\theta_j$.</span></span> <span data-ttu-id="e857b-114">Коэффициент $j $ TH индексирует числовое состояние $ \кет{ж} $, закодированное в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="e857b-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="pauli--pauli"></a><span data-ttu-id="e857b-115">Паули: [Паули](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="e857b-115">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="e857b-116">Оператор Паули $P $, определяющий ось вращения.</span><span class="sxs-lookup"><span data-stu-id="e857b-116">Pauli operator $P$ that determines axis of rotation.</span></span>


### <a name="control--littleendian"></a><span data-ttu-id="e857b-117">элемент управления: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="e857b-117">control : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="e857b-118">$n $-кубит управления регистром, который кодирует числовые состояния $ \кет{ж} $ в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="e857b-118">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="e857b-119">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="e857b-119">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="e857b-120">Один кубит регистр, повернутый $e ^ {i P \ theta_j} $.</span><span class="sxs-lookup"><span data-stu-id="e857b-120">Single qubit register that is rotated by $e^{i P \theta_j}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e857b-121">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e857b-121">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="e857b-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="e857b-122">Remarks</span></span>

<span data-ttu-id="e857b-123">`coefficients` будет дополнен элементами $ \ theta_j = $0,0, если указано меньше $2 ^ n $.</span><span class="sxs-lookup"><span data-stu-id="e857b-123">`coefficients` will be padded with elements $\theta_j = 0.0$ if fewer than $2^n$ are specified.</span></span>

## <a name="see-also"></a><span data-ttu-id="e857b-124">См. также:</span><span class="sxs-lookup"><span data-stu-id="e857b-124">See Also</span></span>

- [<span data-ttu-id="e857b-125">Microsoft. тактов. Canon. Аппроксимателимултиплекспаули</span><span class="sxs-lookup"><span data-stu-id="e857b-125">Microsoft.Quantum.Canon.ApproximatelyMultiplexPauli</span></span>](xref:Microsoft.Quantum.Canon.ApproximatelyMultiplexPauli)