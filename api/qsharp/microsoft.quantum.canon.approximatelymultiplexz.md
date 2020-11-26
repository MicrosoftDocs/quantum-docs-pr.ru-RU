---
uid: Microsoft.Quantum.Canon.ApproximatelyMultiplexZ
title: Операция Аппроксимателимултиплексз
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApproximatelyMultiplexZ
qsharp.summary: Applies a Pauli Z rotation conditioned on an array of qubits, truncating small rotation angles according to a given tolerance.
ms.openlocfilehash: 5e254c2b2d6cbf29b428f4d55aef0e61356e3480
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217107"
---
# <a name="approximatelymultiplexz-operation"></a><span data-ttu-id="56507-102">Операция Аппроксимателимултиплексз</span><span class="sxs-lookup"><span data-stu-id="56507-102">ApproximatelyMultiplexZ operation</span></span>

<span data-ttu-id="56507-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="56507-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="56507-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="56507-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="56507-105">Применяет поворот Паули Z к массиву Кубитс, округляя небольшие углы вращения в соответствии с заданным отклонением.</span><span class="sxs-lookup"><span data-stu-id="56507-105">Applies a Pauli Z rotation conditioned on an array of qubits, truncating small rotation angles according to a given tolerance.</span></span>

```qsharp
operation ApproximatelyMultiplexZ (tolerance : Double, coefficients : Double[], control : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="56507-106">Описание</span><span class="sxs-lookup"><span data-stu-id="56507-106">Description</span></span>

<span data-ttu-id="56507-107">Это применяет единую операцию умножения, которая выполняет повороты по угловому оператору $ \ theta_j $ о однокубит Паули operator $Z $ при управлении $n $-кубит номер State $ \кет{ж} $.</span><span class="sxs-lookup"><span data-stu-id="56507-107">This applies the multiply controlled unitary operation that performs rotations by angle $\theta_j$ about single-qubit Pauli operator $Z$ when controlled by the $n$-qubit number state $\ket{j}$.</span></span>
<span data-ttu-id="56507-108">В частности, эта операция может быть представлена единой</span><span class="sxs-lookup"><span data-stu-id="56507-108">In particular, this operation can be represented by the unitary</span></span>

<span data-ttu-id="56507-109">$ $ \бегин{алигн} U = \сум ^ {2 ^ n-1} _ {j = 0} \кет{ж}\бра{ж} \отимес e ^ {i Z \ theta_j}.</span><span class="sxs-lookup"><span data-stu-id="56507-109">$$ \begin{align} U = \sum^{2^n-1}_{j=0} \ket{j}\bra{j} \otimes e^{i Z \theta_j}.</span></span>
<span data-ttu-id="56507-110">\енд{алигн} $ $</span><span class="sxs-lookup"><span data-stu-id="56507-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="56507-111">Входные данные</span><span class="sxs-lookup"><span data-stu-id="56507-111">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="56507-112">Допуск: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="56507-112">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="56507-113">Допуск, ниже которого усекаются небольшие коэффициенты.</span><span class="sxs-lookup"><span data-stu-id="56507-113">A tolerance below which small coefficients are truncated.</span></span>


### <a name="coefficients--double"></a><span data-ttu-id="56507-114">коэффициенты: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="56507-114">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="56507-115">Массив до $2 ^ n $ коэффициенты $ \ theta_j $.</span><span class="sxs-lookup"><span data-stu-id="56507-115">Array of up to $2^n$ coefficients $\theta_j$.</span></span> <span data-ttu-id="56507-116">Коэффициент $j $ TH индексирует числовое состояние $ \кет{ж} $, закодированное в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="56507-116">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="control--littleendian"></a><span data-ttu-id="56507-117">элемент управления: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="56507-117">control : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="56507-118">$n $-кубит управления регистром, который кодирует числовые состояния $ \кет{ж} $ в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="56507-118">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="56507-119">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="56507-119">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="56507-120">Один кубит регистр, повернутый $e ^ {i P \ theta_j} $.</span><span class="sxs-lookup"><span data-stu-id="56507-120">Single qubit register that is rotated by $e^{i P \theta_j}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="56507-121">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="56507-121">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="56507-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="56507-122">Remarks</span></span>

<span data-ttu-id="56507-123">`coefficients` будет дополнен элементами $ \ theta_j = $0,0, если указано меньше $2 ^ n $.</span><span class="sxs-lookup"><span data-stu-id="56507-123">`coefficients` will be padded with elements $\theta_j = 0.0$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="56507-124">Ссылки</span><span class="sxs-lookup"><span data-stu-id="56507-124">References</span></span>

- <span data-ttu-id="56507-125">Синтез каналов логики тактов Вивек V. Шенде, Стивен S. Буллокк, Игорь L. марковской https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="56507-125">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>

## <a name="see-also"></a><span data-ttu-id="56507-126">См. также:</span><span class="sxs-lookup"><span data-stu-id="56507-126">See Also</span></span>

- [<span data-ttu-id="56507-127">Microsoft. тактов. Canon. Мултиплексз</span><span class="sxs-lookup"><span data-stu-id="56507-127">Microsoft.Quantum.Canon.MultiplexZ</span></span>](xref:Microsoft.Quantum.Canon.MultiplexZ)