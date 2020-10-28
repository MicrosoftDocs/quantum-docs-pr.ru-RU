---
uid: Microsoft.Quantum.Research.Characterization.RandomWalkPhaseEstimation
title: Операция Рандомвалкфасистиматион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Characterization
qsharp.name: RandomWalkPhaseEstimation
qsharp.summary: Performs iterative phase estimation using a random walk to approximate Bayesian inference on the classical measurement results from a given oracle and eigenstate.
ms.openlocfilehash: 5e0c0871b916ff51b85dec8703111788b5204bc6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710876"
---
# <a name="randomwalkphaseestimation-operation"></a><span data-ttu-id="5a2cb-102">Операция Рандомвалкфасистиматион</span><span class="sxs-lookup"><span data-stu-id="5a2cb-102">RandomWalkPhaseEstimation operation</span></span>

<span data-ttu-id="5a2cb-103">Пространство имен: [Microsoft. тактов. Research. character](xref:Microsoft.Quantum.Research.Characterization)</span><span class="sxs-lookup"><span data-stu-id="5a2cb-103">Namespace: [Microsoft.Quantum.Research.Characterization](xref:Microsoft.Quantum.Research.Characterization)</span></span>

<span data-ttu-id="5a2cb-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5a2cb-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5a2cb-105">Выполняет итеративную оценку этапа с помощью случайного прохода, чтобы приблизительно Байеса вывод на классический результат измерения из заданных Oracle и еиженстате.</span><span class="sxs-lookup"><span data-stu-id="5a2cb-105">Performs iterative phase estimation using a random walk to approximate Bayesian inference on the classical measurement results from a given oracle and eigenstate.</span></span>

```qsharp
operation RandomWalkPhaseEstimation (initialMean : Double, initialStdDev : Double, nMeasurements : Int, maxMeasurements : Int, unwind : Int, oracle : Microsoft.Quantum.Oracles.ContinuousOracle, targetState : Qubit[]) : Double
```


## <a name="input"></a><span data-ttu-id="5a2cb-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5a2cb-106">Input</span></span>

### <a name="initialmean--double"></a><span data-ttu-id="5a2cb-107">Инитиалмеан: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5a2cb-107">initialMean : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="5a2cb-108">Среднее первоначальное предварительное распределение по $ \фи $.</span><span class="sxs-lookup"><span data-stu-id="5a2cb-108">Mean of the initial normal prior distribution over $\phi$.</span></span>


### <a name="initialstddev--double"></a><span data-ttu-id="5a2cb-109">Инитиалстддев: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5a2cb-109">initialStdDev : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="5a2cb-110">Стандартное отклонение начального нормального предварительного распространения по $ \фи $.</span><span class="sxs-lookup"><span data-stu-id="5a2cb-110">Standard deviation of the initial normal prior distribution over $\phi$.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="5a2cb-111">Нмеасурементс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5a2cb-111">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5a2cb-112">Количество измерений, которое должно быть принято в окончательной оценке апостериорные.</span><span class="sxs-lookup"><span data-stu-id="5a2cb-112">Number of measurements to be accepted into the final posterior estimate.</span></span>


### <a name="maxmeasurements--int"></a><span data-ttu-id="5a2cb-113">Максмеасурементс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5a2cb-113">maxMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5a2cb-114">Общее количество измерений, которое может быть выполнено до того, как операция будет считаться неудачной.</span><span class="sxs-lookup"><span data-stu-id="5a2cb-114">Total number of measurements than can be taken before the operation is considered to have failed.</span></span>


### <a name="unwind--int"></a><span data-ttu-id="5a2cb-115">Очистка: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5a2cb-115">unwind : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5a2cb-116">Количество результатов, которое следует забывать при сбое проверок согласованности.</span><span class="sxs-lookup"><span data-stu-id="5a2cb-116">Number of results to forget when consistency checks fail.</span></span>


### <a name="oracle--continuousoracle"></a><span data-ttu-id="5a2cb-117">Oracle: [континуаусоракле](xref:Microsoft.Quantum.Oracles.ContinuousOracle)</span><span class="sxs-lookup"><span data-stu-id="5a2cb-117">oracle : [ContinuousOracle](xref:Microsoft.Quantum.Oracles.ContinuousOracle)</span></span>

<span data-ttu-id="5a2cb-118">Операция, представляющая единое $U $ например, $U (t) \кет{\фи} = e ^ {i t \фи}\кет{\фи} $ для еиженстатес $ \кет{\фи} $ с неизвестным этапом $ \фи \ин \Масбб{р} ^ + $.</span><span class="sxs-lookup"><span data-stu-id="5a2cb-118">An operation representing a unitary $U$ such that $U(t)\ket{\phi} = e^{i t \phi}\ket{\phi}$ for eigenstates $\ket{\phi}$ with unknown phase $\phi \in \mathbb{R}^+$.</span></span>


### <a name="targetstate--qubit"></a><span data-ttu-id="5a2cb-119">Таржетстате: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="5a2cb-119">targetState : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="5a2cb-120">Регистр, с которым работает $U $.</span><span class="sxs-lookup"><span data-stu-id="5a2cb-120">A register that $U$ acts on.</span></span>



## <a name="output--double"></a><span data-ttu-id="5a2cb-121">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5a2cb-121">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="5a2cb-122">Окончательная оценка $ \хат{\фи} \масрел{: =} \експект [\фи] $, где ожидание на апостериорные задается всеми принятыми данными.</span><span class="sxs-lookup"><span data-stu-id="5a2cb-122">The final estimate $\hat{\phi} \mathrel{:=} \expect[\phi]$ , where the expectation is over the posterior given all accepted data.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a2cb-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="5a2cb-123">Remarks</span></span>

### <a name="iterative-phase-estimation-and-eigenstates"></a><span data-ttu-id="5a2cb-124">Оценка этапа итерации и Еиженстатес</span><span class="sxs-lookup"><span data-stu-id="5a2cb-124">Iterative Phase Estimation and Eigenstates</span></span>

<span data-ttu-id="5a2cb-125">В общем случае входной регистр `eigenstate` не должен быть еиженстате $ \кет{\фи} $ of $U $, но может быть частью еиженстатес.</span><span class="sxs-lookup"><span data-stu-id="5a2cb-125">In general, the input register `eigenstate` need not be an eigenstate $\ket{\phi}$ of $U$, but can be a superposition over eigenstates.</span></span> <span data-ttu-id="5a2cb-126">Предположим, что входное состояние предоставлено \бегин{алигн} \кет{\пси} & = \сум \_ {j} \алфа \_ j \кет{\фи \_ j}, \енд{алигн}, где $ \{ \алфа \_ j \} $ являются сложными коэффициентами, такими, что $ \сум \_ j | \алфа \_ j | ^ 2 = $1 и где $U \кет{\фи \_ j} = \Phi \_ j\ket {\ фи \_ j} $.</span><span class="sxs-lookup"><span data-stu-id="5a2cb-126">Suppose that the input state is given by \begin{align} \ket{\psi} & = \sum\_{j} \alpha\_j \ket{\phi\_j}, \end{align} where $\{\alpha\_j\}$ are complex coefficients such that $\sum\_j |\alpha\_j|^2 = 1$ and where $U\ket{\phi\_j} = \phi\_j\ket{\phi\_j}$.</span></span>

<span data-ttu-id="5a2cb-127">Затем выполнение итеративной оценки этапа будет в конечном итоге соединить один еиженстате, как описано в разделе " [рекомендации по разработке](xref:microsoft.quantum.libraries.characterization#iterative-phase-estimation-without-eigenstates)".</span><span class="sxs-lookup"><span data-stu-id="5a2cb-127">Then, performing iterative phase estimation will eventually converge to a single eigenstate, as described in the [development guide](xref:microsoft.quantum.libraries.characterization#iterative-phase-estimation-without-eigenstates).</span></span>

### <a name="experiment-design"></a><span data-ttu-id="5a2cb-128">Проектирование экспериментов</span><span class="sxs-lookup"><span data-stu-id="5a2cb-128">Experiment Design</span></span>

<span data-ttu-id="5a2cb-129">Измерение времени $t $ и углов инверсии $ \сета $, переданных в, `oracle` выбирается в соответствии с *эвристическим эвристиком предположения* , \Бегин{алигн} \сета \сим \пр (\фи), \куад t \аппрокс \фрак {1} {\варианце{\фи}}.</span><span class="sxs-lookup"><span data-stu-id="5a2cb-129">The measurement times $t$ and inversion angles $\theta$ passed to `oracle` are chosen according to the *particle guess heuristic* , \begin{align} \theta \sim \Pr(\phi),\quad t \approx \frac{1}{\variance{\phi}}.</span></span>
<span data-ttu-id="5a2cb-130">\енд{алигн} этот эвристический подход оптимальен для уменьшения ожидаемой дисперсии апостериорные в итеративной оценке этапа в соответствии с предположением обычного ранее.</span><span class="sxs-lookup"><span data-stu-id="5a2cb-130">\end{align} This heuristic is optimal for reducing the expected posterior variance in iterative phase estimation under the assumption of a normal prior.</span></span>

### <a name="optimality"></a><span data-ttu-id="5a2cb-131">Оптимальность</span><span class="sxs-lookup"><span data-stu-id="5a2cb-131">Optimality</span></span>

<span data-ttu-id="5a2cb-132">Эта операция приближена к оптимальному средству оценки для этапа $ \фи $, как это было оценено с использованием квадратичной потери $L (\фи, \хат{\фи}) \масрел{: =} (\фи-\хат{\фи}) ^ 2 $.</span><span class="sxs-lookup"><span data-stu-id="5a2cb-132">This operation approximates the optimal estimator for the phase $\phi$, as evaluated using the quadratic loss $L(\phi, \hat{\phi}) \mathrel{:=} (\phi - \hat{\phi})^2$.</span></span>

<span data-ttu-id="5a2cb-133">Дополнительные сведения о статистике оценки этапа итерации см. в разделе [Оценка этапа Байеса](xref:microsoft.quantum.libraries.characterization#bayesian-phase-estimation) .</span><span class="sxs-lookup"><span data-stu-id="5a2cb-133">See [Bayesian Phase Estimation](xref:microsoft.quantum.libraries.characterization#bayesian-phase-estimation) for more details on the statistics of iterative phase estimation.</span></span>

## <a name="references"></a><span data-ttu-id="5a2cb-134">Ссылки</span><span class="sxs-lookup"><span data-stu-id="5a2cb-134">References</span></span>

- <span data-ttu-id="5a2cb-135">Феррие *et al.* 2011 [ДОИ: 10/tfx](https://doi.org/10.1007/s11128-012-0407-6), [арксив: 1110.3067](https://arxiv.org/abs/1110.3067).</span><span class="sxs-lookup"><span data-stu-id="5a2cb-135">Ferrie *et al.* 2011 [doi:10/tfx](https://doi.org/10.1007/s11128-012-0407-6), [arXiv:1110.3067](https://arxiv.org/abs/1110.3067).</span></span>
- <span data-ttu-id="5a2cb-136">Виебе *et al.* 2013 [ДОИ: 10/TF3](https://doi.org/10.1103/PhysRevLett.112.190501), [арксив: 1309.0876](https://arxiv.org/abs/1309.0876)</span><span class="sxs-lookup"><span data-stu-id="5a2cb-136">Wiebe *et al.* 2013 [doi:10/tf3](https://doi.org/10.1103/PhysRevLett.112.190501), [arXiv:1309.0876](https://arxiv.org/abs/1309.0876)</span></span>
- <span data-ttu-id="5a2cb-137">Виебе и Гранаде 2018 *(в процессе подготовки)* .</span><span class="sxs-lookup"><span data-stu-id="5a2cb-137">Wiebe and Granade 2018 *(in preparation)* .</span></span>