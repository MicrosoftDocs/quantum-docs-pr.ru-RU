---
uid: Microsoft.Quantum.Canon.DecomposedIntoTimeStepsCA
title: Функция Декомпосединтотиместепска
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DecomposedIntoTimeStepsCA
qsharp.summary: Returns an operation implementing the Trotter–Suzuki integrator for a given operation.
ms.openlocfilehash: e82df36d2e4f3767a152d5c92d7b1897c744a2ca
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840689"
---
# <a name="decomposedintotimestepsca-function"></a><span data-ttu-id="8f653-102">Функция Декомпосединтотиместепска</span><span class="sxs-lookup"><span data-stu-id="8f653-102">DecomposedIntoTimeStepsCA function</span></span>

<span data-ttu-id="8f653-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8f653-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8f653-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8f653-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8f653-105">Возвращает операцию, реализующую интегратор Троттер – Сузуки для данной операции.</span><span class="sxs-lookup"><span data-stu-id="8f653-105">Returns an operation implementing the Trotter–Suzuki integrator for a given operation.</span></span>

```qsharp
function DecomposedIntoTimeStepsCA<'T> ((nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), trotterOrder : Int) : ((Double, 'T) => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="8f653-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="8f653-106">Input</span></span>

### <a name="nsteps--int"></a><span data-ttu-id="8f653-107">Нстепс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8f653-107">nSteps : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8f653-108">Количество операций, которые необходимо отложить на временные шаги.</span><span class="sxs-lookup"><span data-stu-id="8f653-108">The number of operations to be decomposed into time steps.</span></span>


### <a name="op--intdoublet--unit--is-adj--ctl"></a><span data-ttu-id="8f653-109">Op: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), t) =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="8f653-109">op : ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="8f653-110">Операция, которая принимает входные данные индекса (тип `Int` ) и входные данные времени (тип `Double` ) для декомпозиции.</span><span class="sxs-lookup"><span data-stu-id="8f653-110">An operation which accepts an index input (type `Int`) and a time input (type `Double`) for decomposition.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="8f653-111">Троттерордер: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8f653-111">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8f653-112">Выбирает порядок использования Троттер – Сузуки Integrator.</span><span class="sxs-lookup"><span data-stu-id="8f653-112">Selects the order of the Trotter–Suzuki integrator to be used.</span></span>
<span data-ttu-id="8f653-113">Порядок 1 и даже заказы 2, 4, 6,... в настоящее время поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="8f653-113">Order 1 and even orders 2, 4, 6,... are currently supported.</span></span>



## <a name="output--doublet--unit--is-adj--ctl"></a><span data-ttu-id="8f653-114">Выходные данные: ([Double](xref:microsoft.quantum.lang-ref.double), t) => [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="8f653-114">Output : ([Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="8f653-115">Возвращает единую реализацию интегратора Троттер – Сузуки, где первым параметром `Double` является размер шага интеграции, а второй параметр — это целевой объект.</span><span class="sxs-lookup"><span data-stu-id="8f653-115">Returns a unitary implementing the Trotter–Suzuki integrator, where the first parameter `Double` is the integration step size, and the second parameter is the target acted upon.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="8f653-116">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="8f653-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8f653-117">Е</span><span class="sxs-lookup"><span data-stu-id="8f653-117">'T</span></span>

<span data-ttu-id="8f653-118">Тип, с которым должен действовать каждый шаг времени; как правило, `Qubit[]` или `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="8f653-118">The type which each time step should act upon; typically, either `Qubit[]` or `Qubit`.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f653-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="8f653-119">Remarks</span></span>

<span data-ttu-id="8f653-120">При вызове с параметром `order` Equals `1` Эта функция возвращает операцию, которая может быть смоделирована с помощью самого низкого порядка Троттер – Сузуки Integrator $ $ \бегин{алигн} S_1 (\ламбда) = \ prod_ {j = 1} ^ {m} e ^ {H_j \ламбда}, \енд{алигн} $ $, где мы соблюдаем нотацию [Куант-pH/0508139](https://arxiv.org/abs/quant-ph/0508139) и разберем $ \ламбда $ как время развития (представленное первыми входными данными возвращаемой операции), и пусть $ \{ H_j \} _ {j = 1} ^ {m} $ является набором (неравномерные) динамических генераторов (хермитиан), которые `op(j, lambda, _)` моделируются с помощью единого оператора $e ^ {H_j \lambda} $.</span><span class="sxs-lookup"><span data-stu-id="8f653-120">When called with `order` equal to `1`, this function returns an operation that can be simulated by the lowest-order Trotter–Suzuki integrator $$ \begin{align} S_1(\lambda) = \prod_{j = 1}^{m} e^{H_j \lambda}, \end{align} $$ where we have followed the notation of [quant-ph/0508139](https://arxiv.org/abs/quant-ph/0508139) and let $\lambda$ be the evolution time (represented by the first input of the returned operation), and have let $\{H_j\}_{j = 1}^{m}$ be the set of (skew-Hermitian) dynamical generators being integrated such that `op(j, lambda, _)` is simulated by the unitary operator $e^{H_j \lambda}$.</span></span>

<span data-ttu-id="8f653-121">Аналогично, функция `order` из `2` возвращает симметричный Троттер — Сузуки Integrator $ $ \бегин{алигн} S_2 (\ламбда) = \ prod_ {j = 1} ^ {m} e ^ {H_k \ламбда/2} \ prod_ {j ' = m} ^ {1} e ^ {H_ {j '} \ламбда/2}.</span><span class="sxs-lookup"><span data-stu-id="8f653-121">Similarly, an `order` of `2` returns the second-order symmetric Trotter–Suzuki integrator $$ \begin{align} S_2(\lambda) = \prod_{j = 1}^{m} e^{H_k \lambda / 2} \prod_{j' = m}^{1} e^{H_{j'} \lambda / 2}.</span></span>
<span data-ttu-id="8f653-122">\енд{алигн} $ $</span><span class="sxs-lookup"><span data-stu-id="8f653-122">\end{align} $$</span></span>

<span data-ttu-id="8f653-123">Более высокие значения даже `order` реализуются с помощью рекурсивного создания [Куант-pH/0508139](https://arxiv.org/abs/quant-ph/0508139).</span><span class="sxs-lookup"><span data-stu-id="8f653-123">Higher even values of `order` are implemented using the recursive construction of [quant-ph/0508139](https://arxiv.org/abs/quant-ph/0508139).</span></span>

## <a name="references"></a><span data-ttu-id="8f653-124">Ссылки</span><span class="sxs-lookup"><span data-stu-id="8f653-124">References</span></span>

- [<span data-ttu-id="8f653-125">*D. W. Берри, G. Ахокас, R. Cleve, B. C. Сандерс*</span><span class="sxs-lookup"><span data-stu-id="8f653-125"> *D. W. Berry, G. Ahokas, R. Cleve, B. C. Sanders* </span></span>](https://arxiv.org/abs/quant-ph/0508139)