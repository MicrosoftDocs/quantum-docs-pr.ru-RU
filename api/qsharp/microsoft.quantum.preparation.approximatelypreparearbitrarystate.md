---
uid: Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState
title: Операция Аппроксимателипрепареарбитраристате
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: ApproximatelyPrepareArbitraryState
qsharp.summary: >-
  > [!WARNING]

  > ApproximatelyPrepareArbitraryState has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryStateCP> instead.


  Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients, up to a given approximation tolerance.
ms.openlocfilehash: 9e1b172258acd0cb09b824a773e7e79d44fec20c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193715"
---
# <a name="approximatelypreparearbitrarystate-operation"></a><span data-ttu-id="ac370-102">Операция Аппроксимателипрепареарбитраристате</span><span class="sxs-lookup"><span data-stu-id="ac370-102">ApproximatelyPrepareArbitraryState operation</span></span>

<span data-ttu-id="ac370-103">Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="ac370-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="ac370-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ac370-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="ac370-105">Аппроксимателипрепареарбитраристате является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="ac370-105">ApproximatelyPrepareArbitraryState has been deprecated.</span></span> <span data-ttu-id="ac370-106">Взамен рекомендуется использовать <xref:Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryStateCP>.</span><span class="sxs-lookup"><span data-stu-id="ac370-106">Please use <xref:Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryStateCP> instead.</span></span>

<span data-ttu-id="ac370-107">Учитывая набор коэффициентов и регистр такта с прямым порядком байтов, подготавливает состояние для этой регистрации, описываемое заданным коэффициентом, вплоть до заданного допустимого значения приближения.</span><span class="sxs-lookup"><span data-stu-id="ac370-107">Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients, up to a given approximation tolerance.</span></span>

```qsharp
operation ApproximatelyPrepareArbitraryState (tolerance : Double, coefficients : Microsoft.Quantum.Math.ComplexPolar[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="ac370-108">Описание</span><span class="sxs-lookup"><span data-stu-id="ac370-108">Description</span></span>

<span data-ttu-id="ac370-109">Эта операция подготавливает произвольное состояние такта $ \кет{\пси} $ с сложными коэффициентами $r _j e ^ {i t_j} $ из $n $-кубит вычислительное состояние $ \ket{0 \кдотс 0} $.</span><span class="sxs-lookup"><span data-stu-id="ac370-109">This operation prepares an arbitrary quantum state $\ket{\psi}$ with complex coefficients $r_j e^{i t_j}$ from the $n$-qubit computational basis state $\ket{0 \cdots 0}$.</span></span>
<span data-ttu-id="ac370-110">В частности, действие этой операции может быть смоделировано единым преобразованием $U $, которое работает в состоянии «все-нули», как</span><span class="sxs-lookup"><span data-stu-id="ac370-110">In particular, the action of this operation can be simulated by the a unitary transformation $U$ which acts on the all-zeros state as</span></span>

<span data-ttu-id="ac370-111">$ $ \бегин{алигн} У\кет {0... 0} & = \кет{\пси} \\ \\ & = \фрак{\ sum_ {j = 0} ^ {2 ^ n-1} r_j e ^ {i t_j} \кет{ж}} {\скрт{\ sum_ {j = 0} ^ {2 ^ n-1} | r_j | ^ 2}}.</span><span class="sxs-lookup"><span data-stu-id="ac370-111">$$ \begin{align} U\ket{0...0} & = \ket{\psi} \\\\ & = \frac{ \sum_{j=0}^{2^n-1} r_j e^{i t_j} \ket{j} }{ \sqrt{\sum_{j=0}^{2^n-1} |r_j|^2} }.</span></span>
<span data-ttu-id="ac370-112">\енд{алигн} $ $</span><span class="sxs-lookup"><span data-stu-id="ac370-112">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="ac370-113">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ac370-113">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="ac370-114">Допуск: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ac370-114">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="ac370-115">Отклонение аппроксимации, используемое при подготовке данного состояния.</span><span class="sxs-lookup"><span data-stu-id="ac370-115">The approximation tolerance to be used when preparing the given state.</span></span>


### <a name="coefficients--complexpolar"></a><span data-ttu-id="ac370-116">коэффициенты: [комплексполар](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span><span class="sxs-lookup"><span data-stu-id="ac370-116">coefficients : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span></span>

<span data-ttu-id="ac370-117">Массив до $2 ^ n $ сложных коэффициентов, представленных абсолютным значением и фазой $ (r_j, t_j) $.</span><span class="sxs-lookup"><span data-stu-id="ac370-117">Array of up to $2^n$ complex coefficients represented by their absolute value and phase $(r_j, t_j)$.</span></span> <span data-ttu-id="ac370-118">Коэффициент $j $ TH индексирует числовое состояние $ \кет{ж} $, закодированное в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="ac370-118">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="ac370-119">Кубитс: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="ac370-119">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="ac370-120">Кубит регистр номеров кодировки в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="ac370-120">Qubit register encoding number states in little-endian format.</span></span> <span data-ttu-id="ac370-121">Это должно быть инициализировано в состоянии вычислительной базы $ \ket{0...0} $.</span><span class="sxs-lookup"><span data-stu-id="ac370-121">This is expected to be initialized in the computational basis state $\ket{0...0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ac370-122">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ac370-122">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="ac370-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ac370-123">Remarks</span></span>

<span data-ttu-id="ac370-124">Отрицательные коэффициенты ввода $r _j < $0 будут рассматриваться как положительные значения $ | r_j | $.</span><span class="sxs-lookup"><span data-stu-id="ac370-124">Negative input coefficients $r_j < 0$ will be treated as though positive with value $|r_j|$.</span></span> <span data-ttu-id="ac370-125">`coefficients` будет дополнен элементами $ (r_j, t_j) = (0,0, 0,0) $, если указано меньше $2 ^ n $.</span><span class="sxs-lookup"><span data-stu-id="ac370-125">`coefficients` will be padded with elements $(r_j, t_j) = (0.0, 0.0)$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="ac370-126">Ссылки</span><span class="sxs-lookup"><span data-stu-id="ac370-126">References</span></span>

- <span data-ttu-id="ac370-127">Синтез каналов логики тактов Вивек V. Шенде, Стивен S. Буллокк, Игорь L. марковской https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="ac370-127">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>

## <a name="see-also"></a><span data-ttu-id="ac370-128">См. также:</span><span class="sxs-lookup"><span data-stu-id="ac370-128">See Also</span></span>

- [<span data-ttu-id="ac370-129">Microsoft. тактов. подготовка. Аппроксимателипрепареарбитраристате</span><span class="sxs-lookup"><span data-stu-id="ac370-129">Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState</span></span>](xref:Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState)