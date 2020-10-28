---
uid: Microsoft.Quantum.Preparation.PrepareArbitraryState
title: Операция Препареарбитраристате
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareArbitraryState
qsharp.summary: Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients.
ms.openlocfilehash: 18f45da601b02fc5f83936b086323e31a66fc20b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733241"
---
# <a name="preparearbitrarystate-operation"></a><span data-ttu-id="459ca-102">Операция Препареарбитраристате</span><span class="sxs-lookup"><span data-stu-id="459ca-102">PrepareArbitraryState operation</span></span>

<span data-ttu-id="459ca-103">Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="459ca-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="459ca-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="459ca-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="459ca-105">Учитывая набор коэффициентов и регистр такта с прямым порядком байтов, подготавливает к этому регистру состояние, описываемое заданным коэффициентом.</span><span class="sxs-lookup"><span data-stu-id="459ca-105">Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients.</span></span>

```qsharp
operation PrepareArbitraryState (coefficients : Microsoft.Quantum.Math.ComplexPolar[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="459ca-106">Описание</span><span class="sxs-lookup"><span data-stu-id="459ca-106">Description</span></span>

<span data-ttu-id="459ca-107">Эта операция подготавливает произвольное состояние такта $ \кет{\пси} $ с сложными коэффициентами $r _j e ^ {i t_j} $ из $n $-кубит вычислительное состояние $ \ket{0 \кдотс 0} $.</span><span class="sxs-lookup"><span data-stu-id="459ca-107">This operation prepares an arbitrary quantum state $\ket{\psi}$ with complex coefficients $r_j e^{i t_j}$ from the $n$-qubit computational basis state $\ket{0 \cdots 0}$.</span></span>
<span data-ttu-id="459ca-108">В частности, действие этой операции может быть смоделировано единым преобразованием $U $, которое работает в состоянии «все-нули», как</span><span class="sxs-lookup"><span data-stu-id="459ca-108">In particular, the action of this operation can be simulated by the a unitary transformation $U$ which acts on the all-zeros state as</span></span>

<span data-ttu-id="459ca-109">$ $ \бегин{алигн} У\кет {0... 0} & = \кет{\пси} \\ \\ & = \фрак{\ sum_ {j = 0} ^ {2 ^ n-1} r_j e ^ {i t_j} \кет{ж}} {\скрт{\ sum_ {j = 0} ^ {2 ^ n-1} | r_j | ^ 2}}.</span><span class="sxs-lookup"><span data-stu-id="459ca-109">$$ \begin{align} U\ket{0...0} & = \ket{\psi} \\\\ & = \frac{ \sum_{j=0}^{2^n-1} r_j e^{i t_j} \ket{j} }{ \sqrt{\sum_{j=0}^{2^n-1} |r_j|^2} }.</span></span>
<span data-ttu-id="459ca-110">\енд{алигн} $ $</span><span class="sxs-lookup"><span data-stu-id="459ca-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="459ca-111">Входные данные</span><span class="sxs-lookup"><span data-stu-id="459ca-111">Input</span></span>

### <a name="coefficients--complexpolar"></a><span data-ttu-id="459ca-112">коэффициенты: [комплексполар](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span><span class="sxs-lookup"><span data-stu-id="459ca-112">coefficients : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span></span>

<span data-ttu-id="459ca-113">Массив до $2 ^ n $ сложных коэффициентов, представленных абсолютным значением и фазой $ (r_j, t_j) $.</span><span class="sxs-lookup"><span data-stu-id="459ca-113">Array of up to $2^n$ complex coefficients represented by their absolute value and phase $(r_j, t_j)$.</span></span> <span data-ttu-id="459ca-114">Коэффициент $j $ TH индексирует числовое состояние $ \кет{ж} $, закодированное в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="459ca-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="459ca-115">Кубитс: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="459ca-115">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="459ca-116">Кубит регистр номеров кодировки в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="459ca-116">Qubit register encoding number states in little-endian format.</span></span> <span data-ttu-id="459ca-117">Это должно быть инициализировано в состоянии вычислительной базы $ \ket{0...0} $.</span><span class="sxs-lookup"><span data-stu-id="459ca-117">This is expected to be initialized in the computational basis state $\ket{0...0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="459ca-118">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="459ca-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="459ca-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="459ca-119">Remarks</span></span>

<span data-ttu-id="459ca-120">Отрицательные коэффициенты ввода $r _j < $0 будут рассматриваться как положительные значения $ | r_j | $.</span><span class="sxs-lookup"><span data-stu-id="459ca-120">Negative input coefficients $r_j < 0$ will be treated as though positive with value $|r_j|$.</span></span> <span data-ttu-id="459ca-121">`coefficients` будет дополнен элементами $ (r_j, t_j) = (0,0, 0,0) $, если указано меньше $2 ^ n $.</span><span class="sxs-lookup"><span data-stu-id="459ca-121">`coefficients` will be padded with elements $(r_j, t_j) = (0.0, 0.0)$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="459ca-122">Ссылки</span><span class="sxs-lookup"><span data-stu-id="459ca-122">References</span></span>

- <span data-ttu-id="459ca-123">Синтез каналов логики тактов Вивек V. Шенде, Стивен S. Буллокк, Игорь L. марковской https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="459ca-123">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>

## <a name="see-also"></a><span data-ttu-id="459ca-124">См. также:</span><span class="sxs-lookup"><span data-stu-id="459ca-124">See Also</span></span>

- [<span data-ttu-id="459ca-125">Microsoft. тактов. подготовка. Аппроксимателипрепареарбитраристате</span><span class="sxs-lookup"><span data-stu-id="459ca-125">Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState</span></span>](xref:Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState)