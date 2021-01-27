---
uid: Microsoft.Quantum.Preparation.PrepareArbitraryStateD
title: Операция Препареарбитраристатед
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareArbitraryStateD
qsharp.summary: Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients.
ms.openlocfilehash: 61f6614821951435828cd28edeb1447cb33f3648
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842373"
---
# <a name="preparearbitrarystated-operation"></a><span data-ttu-id="7c113-102">Операция Препареарбитраристатед</span><span class="sxs-lookup"><span data-stu-id="7c113-102">PrepareArbitraryStateD operation</span></span>

<span data-ttu-id="7c113-103">Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="7c113-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="7c113-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7c113-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7c113-105">Учитывая набор коэффициентов и регистр такта с прямым порядком байтов, подготавливает к этому регистру состояние, описываемое заданным коэффициентом.</span><span class="sxs-lookup"><span data-stu-id="7c113-105">Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients.</span></span>

```qsharp
operation PrepareArbitraryStateD (coefficients : Double[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="7c113-106">Описание</span><span class="sxs-lookup"><span data-stu-id="7c113-106">Description</span></span>

<span data-ttu-id="7c113-107">Эта операция подготавливает произвольное состояние такта $ \кет{\пси} $ с сложными коэффициентами $r _j e ^ {i t_j} $ из $n $-кубит вычислительное состояние $ \ket{0 \кдотс 0} $.</span><span class="sxs-lookup"><span data-stu-id="7c113-107">This operation prepares an arbitrary quantum state $\ket{\psi}$ with complex coefficients $r_j e^{i t_j}$ from the $n$-qubit computational basis state $\ket{0 \cdots 0}$.</span></span>
<span data-ttu-id="7c113-108">В частности, действие этой операции может быть смоделировано единым преобразованием $U $, которое работает в состоянии «все-нули», как</span><span class="sxs-lookup"><span data-stu-id="7c113-108">In particular, the action of this operation can be simulated by the a unitary transformation $U$ that acts on the all-zeros state as</span></span>

<span data-ttu-id="7c113-109">$ $ \бегин{алигн} У\кет {0... 0} & = \кет{\пси} \\ \\ & = \фрак{\ sum_ {j = 0} ^ {2 ^ n-1} r_j e ^ {i t_j} \кет{ж}} {\скрт{\ sum_ {j = 0} ^ {2 ^ n-1} | r_j | ^ 2}}.</span><span class="sxs-lookup"><span data-stu-id="7c113-109">$$ \begin{align} U\ket{0...0} & = \ket{\psi} \\\\ & = \frac{ \sum_{j=0}^{2^n-1} r_j e^{i t_j} \ket{j} }{ \sqrt{\sum_{j=0}^{2^n-1} |r_j|^2} }.</span></span>
<span data-ttu-id="7c113-110">\енд{алигн} $ $</span><span class="sxs-lookup"><span data-stu-id="7c113-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="7c113-111">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7c113-111">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="7c113-112">коэффициенты: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="7c113-112">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="7c113-113">Массив до $2 ^ n $ Real коэффициентов.</span><span class="sxs-lookup"><span data-stu-id="7c113-113">Array of up to $2^n$ real coefficients.</span></span> <span data-ttu-id="7c113-114">Коэффициент $j $ TH индексирует числовое состояние $ \кет{ж} $, закодированное в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="7c113-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="7c113-115">Кубитс: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="7c113-115">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="7c113-116">Кубит регистр номеров кодировки в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="7c113-116">Qubit register encoding number states in little-endian format.</span></span> <span data-ttu-id="7c113-117">Это должно быть инициализировано в состоянии вычислительной базы $ \ket{0...0} $.</span><span class="sxs-lookup"><span data-stu-id="7c113-117">This is expected to be initialized in the computational basis state $\ket{0...0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7c113-118">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7c113-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="7c113-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="7c113-119">Remarks</span></span>

<span data-ttu-id="7c113-120">Отрицательные коэффициенты ввода $r _j < $0 будут рассматриваться как положительные значения $ | r_j | $.</span><span class="sxs-lookup"><span data-stu-id="7c113-120">Negative input coefficients $r_j < 0$ will be treated as though positive with value $|r_j|$.</span></span> <span data-ttu-id="7c113-121">`coefficients` будет дополнен элементами $ (r_j, t_j) = (0,0, 0,0) $, если указано меньше $2 ^ n $.</span><span class="sxs-lookup"><span data-stu-id="7c113-121">`coefficients` will be padded with elements $(r_j, t_j) = (0.0, 0.0)$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="7c113-122">Ссылки</span><span class="sxs-lookup"><span data-stu-id="7c113-122">References</span></span>

- <span data-ttu-id="7c113-123">Синтез каналов логики тактов Вивек V. Шенде, Стивен S. Буллокк, Игорь L. марковской https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="7c113-123">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>

## <a name="see-also"></a><span data-ttu-id="7c113-124">См. также:</span><span class="sxs-lookup"><span data-stu-id="7c113-124">See Also</span></span>

- [<span data-ttu-id="7c113-125">Microsoft. тактов. подготовка. Аппроксимателипрепареарбитраристате</span><span class="sxs-lookup"><span data-stu-id="7c113-125">Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState</span></span>](xref:Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState)