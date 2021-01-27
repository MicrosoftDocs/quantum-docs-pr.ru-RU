---
uid: Microsoft.Quantum.Canon.ApproximatelyMultiplexPauli
title: Операция Аппроксимателимултиплекспаули
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApproximatelyMultiplexPauli
qsharp.summary: Applies a Pauli rotation conditioned on an array of qubits, truncating small rotation angles according to a given tolerance.
ms.openlocfilehash: 1fc8a8857b6b37d4c3e812a3c4cb2941b9238800
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844575"
---
# <a name="approximatelymultiplexpauli-operation"></a><span data-ttu-id="d6ac7-102">Операция Аппроксимателимултиплекспаули</span><span class="sxs-lookup"><span data-stu-id="d6ac7-102">ApproximatelyMultiplexPauli operation</span></span>

<span data-ttu-id="d6ac7-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d6ac7-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d6ac7-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d6ac7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d6ac7-105">Применяет вращение Паули к массиву Кубитс, округляя небольшие углы вращения в соответствии с заданным отклонением.</span><span class="sxs-lookup"><span data-stu-id="d6ac7-105">Applies a Pauli rotation conditioned on an array of qubits, truncating small rotation angles according to a given tolerance.</span></span>

```qsharp
operation ApproximatelyMultiplexPauli (tolerance : Double, coefficients : Double[], pauli : Pauli, control : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="d6ac7-106">Описание</span><span class="sxs-lookup"><span data-stu-id="d6ac7-106">Description</span></span>

<span data-ttu-id="d6ac7-107">Это применяет единую операцию умножения, которая выполняет повороты по угловому оператору $ \ theta_j $ о однокубит Паули operator $P $ при управлении $n $-кубит номер State $ \кет{ж} $.</span><span class="sxs-lookup"><span data-stu-id="d6ac7-107">This applies a multiply controlled unitary operation that performs rotations by angle $\theta_j$ about single-qubit Pauli operator $P$ when controlled by the $n$-qubit number state $\ket{j}$.</span></span>
<span data-ttu-id="d6ac7-108">В частности, действие этой операции представлено единым</span><span class="sxs-lookup"><span data-stu-id="d6ac7-108">In particular, the action of this operation is represented by the unitary</span></span>

<span data-ttu-id="d6ac7-109">$ $ \бегин{алигн} U = \сум ^ {2 ^ n-1} _ {j = 0} \кет{ж}\бра{ж} \отимес e ^ {i P \ theta_j}.</span><span class="sxs-lookup"><span data-stu-id="d6ac7-109">$$ \begin{align} U = \sum^{2^n - 1}_{j=0} \ket{j}\bra{j} \otimes e^{i P \theta_j}.</span></span>
<span data-ttu-id="d6ac7-110">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="d6ac7-110">\end{align}</span></span>

##

## <a name="input"></a><span data-ttu-id="d6ac7-111">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d6ac7-111">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="d6ac7-112">Допуск: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d6ac7-112">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="d6ac7-113">Допуск, ниже которого усекаются небольшие коэффициенты.</span><span class="sxs-lookup"><span data-stu-id="d6ac7-113">A tolerance below which small coefficients are truncated.</span></span>


### <a name="coefficients--double"></a><span data-ttu-id="d6ac7-114">коэффициенты: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="d6ac7-114">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="d6ac7-115">Массив до $2 ^ n $ коэффициенты $ \ theta_j $.</span><span class="sxs-lookup"><span data-stu-id="d6ac7-115">Array of up to $2^n$ coefficients $\theta_j$.</span></span> <span data-ttu-id="d6ac7-116">Коэффициент $j $ TH индексирует числовое состояние $ \кет{ж} $, закодированное в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="d6ac7-116">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="pauli--pauli"></a><span data-ttu-id="d6ac7-117">Паули: [Паули](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="d6ac7-117">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="d6ac7-118">Оператор Паули $P $, определяющий ось вращения.</span><span class="sxs-lookup"><span data-stu-id="d6ac7-118">Pauli operator $P$ that determines axis of rotation.</span></span>


### <a name="control--littleendian"></a><span data-ttu-id="d6ac7-119">элемент управления: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="d6ac7-119">control : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="d6ac7-120">$n $-кубит управления регистром, который кодирует числовые состояния $ \кет{ж} $ в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="d6ac7-120">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="d6ac7-121">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="d6ac7-121">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="d6ac7-122">Один кубит регистр, повернутый $e ^ {i P \ theta_j} $.</span><span class="sxs-lookup"><span data-stu-id="d6ac7-122">Single qubit register that is rotated by $e^{i P \theta_j}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d6ac7-123">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d6ac7-123">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="d6ac7-124">Remarks</span><span class="sxs-lookup"><span data-stu-id="d6ac7-124">Remarks</span></span>

<span data-ttu-id="d6ac7-125">`coefficients` будет дополнен элементами $ \ theta_j = $0,0, если указано меньше $2 ^ n $.</span><span class="sxs-lookup"><span data-stu-id="d6ac7-125">`coefficients` will be padded with elements $\theta_j = 0.0$ if fewer than $2^n$ are specified.</span></span>

## <a name="see-also"></a><span data-ttu-id="d6ac7-126">См. также:</span><span class="sxs-lookup"><span data-stu-id="d6ac7-126">See Also</span></span>

- [<span data-ttu-id="d6ac7-127">Microsoft. тактов. Canon. Мултиплекспаули</span><span class="sxs-lookup"><span data-stu-id="d6ac7-127">Microsoft.Quantum.Canon.MultiplexPauli</span></span>](xref:Microsoft.Quantum.Canon.MultiplexPauli)