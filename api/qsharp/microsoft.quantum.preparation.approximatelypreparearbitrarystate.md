---
uid: Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState
title: Операция Аппроксимателипрепареарбитраристате
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: ApproximatelyPrepareArbitraryState
qsharp.summary: Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients, up to a given approximation tolerance.
ms.openlocfilehash: 2561b098c5faf2d24bb9ab348fb052025808e441
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733265"
---
# <a name="approximatelypreparearbitrarystate-operation"></a><span data-ttu-id="b4853-102">Операция Аппроксимателипрепареарбитраристате</span><span class="sxs-lookup"><span data-stu-id="b4853-102">ApproximatelyPrepareArbitraryState operation</span></span>

<span data-ttu-id="b4853-103">Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="b4853-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="b4853-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b4853-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b4853-105">Учитывая набор коэффициентов и регистр такта с прямым порядком байтов, подготавливает состояние для этой регистрации, описываемое заданным коэффициентом, вплоть до заданного допустимого значения приближения.</span><span class="sxs-lookup"><span data-stu-id="b4853-105">Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients, up to a given approximation tolerance.</span></span>

```qsharp
operation ApproximatelyPrepareArbitraryState (tolerance : Double, coefficients : Microsoft.Quantum.Math.ComplexPolar[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="b4853-106">Описание</span><span class="sxs-lookup"><span data-stu-id="b4853-106">Description</span></span>

<span data-ttu-id="b4853-107">Эта операция подготавливает произвольное состояние такта $ \кет{\пси} $ с сложными коэффициентами $r _j e ^ {i t_j} $ из $n $-кубит вычислительное состояние $ \ket{0 \кдотс 0} $.</span><span class="sxs-lookup"><span data-stu-id="b4853-107">This operation prepares an arbitrary quantum state $\ket{\psi}$ with complex coefficients $r_j e^{i t_j}$ from the $n$-qubit computational basis state $\ket{0 \cdots 0}$.</span></span>
<span data-ttu-id="b4853-108">В частности, действие этой операции может быть смоделировано единым преобразованием $U $, которое работает в состоянии «все-нули», как</span><span class="sxs-lookup"><span data-stu-id="b4853-108">In particular, the action of this operation can be simulated by the a unitary transformation $U$ which acts on the all-zeros state as</span></span>

<span data-ttu-id="b4853-109">$ $ \бегин{алигн} У\кет {0... 0} & = \кет{\пси} \\ \\ & = \фрак{\ sum_ {j = 0} ^ {2 ^ n-1} r_j e ^ {i t_j} \кет{ж}} {\скрт{\ sum_ {j = 0} ^ {2 ^ n-1} | r_j | ^ 2}}.</span><span class="sxs-lookup"><span data-stu-id="b4853-109">$$ \begin{align} U\ket{0...0} & = \ket{\psi} \\\\ & = \frac{ \sum_{j=0}^{2^n-1} r_j e^{i t_j} \ket{j} }{ \sqrt{\sum_{j=0}^{2^n-1} |r_j|^2} }.</span></span>
<span data-ttu-id="b4853-110">\енд{алигн} $ $</span><span class="sxs-lookup"><span data-stu-id="b4853-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="b4853-111">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b4853-111">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="b4853-112">Допуск: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="b4853-112">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="b4853-113">Отклонение аппроксимации, используемое при подготовке данного состояния.</span><span class="sxs-lookup"><span data-stu-id="b4853-113">The approximation tolerance to be used when preparing the given state.</span></span>


### <a name="coefficients--complexpolar"></a><span data-ttu-id="b4853-114">коэффициенты: [комплексполар](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span><span class="sxs-lookup"><span data-stu-id="b4853-114">coefficients : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span></span>

<span data-ttu-id="b4853-115">Массив до $2 ^ n $ сложных коэффициентов, представленных абсолютным значением и фазой $ (r_j, t_j) $.</span><span class="sxs-lookup"><span data-stu-id="b4853-115">Array of up to $2^n$ complex coefficients represented by their absolute value and phase $(r_j, t_j)$.</span></span> <span data-ttu-id="b4853-116">Коэффициент $j $ TH индексирует числовое состояние $ \кет{ж} $, закодированное в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="b4853-116">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="b4853-117">Кубитс: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="b4853-117">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="b4853-118">Кубит регистр номеров кодировки в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="b4853-118">Qubit register encoding number states in little-endian format.</span></span> <span data-ttu-id="b4853-119">Это должно быть инициализировано в состоянии вычислительной базы $ \ket{0...0} $.</span><span class="sxs-lookup"><span data-stu-id="b4853-119">This is expected to be initialized in the computational basis state $\ket{0...0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b4853-120">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b4853-120">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="b4853-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="b4853-121">Remarks</span></span>

<span data-ttu-id="b4853-122">Отрицательные коэффициенты ввода $r _j < $0 будут рассматриваться как положительные значения $ | r_j | $.</span><span class="sxs-lookup"><span data-stu-id="b4853-122">Negative input coefficients $r_j < 0$ will be treated as though positive with value $|r_j|$.</span></span> <span data-ttu-id="b4853-123">`coefficients` будет дополнен элементами $ (r_j, t_j) = (0,0, 0,0) $, если указано меньше $2 ^ n $.</span><span class="sxs-lookup"><span data-stu-id="b4853-123">`coefficients` will be padded with elements $(r_j, t_j) = (0.0, 0.0)$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="b4853-124">Ссылки</span><span class="sxs-lookup"><span data-stu-id="b4853-124">References</span></span>

- <span data-ttu-id="b4853-125">Синтез каналов логики тактов Вивек V. Шенде, Стивен S. Буллокк, Игорь L. марковской https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="b4853-125">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>

## <a name="see-also"></a><span data-ttu-id="b4853-126">См. также:</span><span class="sxs-lookup"><span data-stu-id="b4853-126">See Also</span></span>

- [<span data-ttu-id="b4853-127">Microsoft. тактов. подготовка. Аппроксимателипрепареарбитраристате</span><span class="sxs-lookup"><span data-stu-id="b4853-127">Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState</span></span>](xref:Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState)