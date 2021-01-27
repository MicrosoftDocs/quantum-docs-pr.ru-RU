---
uid: Microsoft.Quantum.Canon.MultiplexZ
title: Операция Мултиплексз
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexZ
qsharp.summary: Applies a Pauli Z rotation conditioned on an array of qubits.
ms.openlocfilehash: dccfe86104263e23794bce33279e8748f11f5a54
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852428"
---
# <a name="multiplexz-operation"></a><span data-ttu-id="b14df-102">Операция Мултиплексз</span><span class="sxs-lookup"><span data-stu-id="b14df-102">MultiplexZ operation</span></span>

<span data-ttu-id="b14df-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b14df-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b14df-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b14df-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b14df-105">Применяет поворот Паули Z к массиву Кубитс.</span><span class="sxs-lookup"><span data-stu-id="b14df-105">Applies a Pauli Z rotation conditioned on an array of qubits.</span></span>

```qsharp
operation MultiplexZ (coefficients : Double[], control : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="b14df-106">Описание</span><span class="sxs-lookup"><span data-stu-id="b14df-106">Description</span></span>

<span data-ttu-id="b14df-107">Это применяет единую операцию умножения, которая выполняет повороты по угловому оператору $ \ theta_j $ о однокубит Паули operator $Z $ при управлении $n $-кубит номер State $ \кет{ж} $.</span><span class="sxs-lookup"><span data-stu-id="b14df-107">This applies the multiply controlled unitary operation that performs rotations by angle $\theta_j$ about single-qubit Pauli operator $Z$ when controlled by the $n$-qubit number state $\ket{j}$.</span></span>
<span data-ttu-id="b14df-108">В частности, эта операция может быть представлена единой</span><span class="sxs-lookup"><span data-stu-id="b14df-108">In particular, this operation can be represented by the unitary</span></span>

<span data-ttu-id="b14df-109">$ $ \бегин{алигн} U = \сум ^ {2 ^ n-1} _ {j = 0} \кет{ж}\бра{ж} \отимес e ^ {i Z \ theta_j}.</span><span class="sxs-lookup"><span data-stu-id="b14df-109">$$ \begin{align} U = \sum^{2^n-1}_{j=0} \ket{j}\bra{j} \otimes e^{i Z \theta_j}.</span></span>
<span data-ttu-id="b14df-110">\енд{алигн} $ $</span><span class="sxs-lookup"><span data-stu-id="b14df-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="b14df-111">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b14df-111">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="b14df-112">коэффициенты: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="b14df-112">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="b14df-113">Массив до $2 ^ n $ коэффициенты $ \ theta_j $.</span><span class="sxs-lookup"><span data-stu-id="b14df-113">Array of up to $2^n$ coefficients $\theta_j$.</span></span> <span data-ttu-id="b14df-114">Коэффициент $j $ TH индексирует числовое состояние $ \кет{ж} $, закодированное в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="b14df-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="control--littleendian"></a><span data-ttu-id="b14df-115">элемент управления: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="b14df-115">control : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="b14df-116">$n $-кубит управления регистром, который кодирует числовые состояния $ \кет{ж} $ в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="b14df-116">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="b14df-117">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="b14df-117">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="b14df-118">Один кубит регистр, повернутый $e ^ {i P \ theta_j} $.</span><span class="sxs-lookup"><span data-stu-id="b14df-118">Single qubit register that is rotated by $e^{i P \theta_j}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b14df-119">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b14df-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="b14df-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="b14df-120">Remarks</span></span>

<span data-ttu-id="b14df-121">`coefficients` будет дополнен элементами $ \ theta_j = $0,0, если указано меньше $2 ^ n $.</span><span class="sxs-lookup"><span data-stu-id="b14df-121">`coefficients` will be padded with elements $\theta_j = 0.0$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="b14df-122">Ссылки</span><span class="sxs-lookup"><span data-stu-id="b14df-122">References</span></span>

- <span data-ttu-id="b14df-123">Синтез каналов логики тактов Вивек V. Шенде, Стивен S. Буллокк, Игорь L. марковской https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="b14df-123">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>

## <a name="see-also"></a><span data-ttu-id="b14df-124">См. также:</span><span class="sxs-lookup"><span data-stu-id="b14df-124">See Also</span></span>

- [<span data-ttu-id="b14df-125">Microsoft. тактов. Canon. Аппроксимателимултиплексз</span><span class="sxs-lookup"><span data-stu-id="b14df-125">Microsoft.Quantum.Canon.ApproximatelyMultiplexZ</span></span>](xref:Microsoft.Quantum.Canon.ApproximatelyMultiplexZ)