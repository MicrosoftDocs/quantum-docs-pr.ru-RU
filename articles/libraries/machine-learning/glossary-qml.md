---
title: Библиотека машинного обучения
author: alexeib2
ms.author: alexei.bocharov@microsoft.com
ms.date: 2/27/2020
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.training
ms.openlocfilehash: f9b33a607a892179795d0700ba3080f9a24ab94a
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/28/2020
ms.locfileid: "77909778"
---
# <a name="quantum-machine-learning-glossary"></a><span data-ttu-id="919a9-102">Глоссарий Машинное обучение</span><span class="sxs-lookup"><span data-stu-id="919a9-102">Quantum Machine Learning glossary</span></span>

<span data-ttu-id="919a9-103">Обучение классификатора тактовой передачи, ориентированного на цепь, — это процесс с множеством движущихся частей, требующих одинаковых (или немного большего) объема калибровки на основе пробы и ошибок в процессе обучения традиционных классификаторов.</span><span class="sxs-lookup"><span data-stu-id="919a9-103">Training of a circuit-centric quantum classifier is a process with many moving parts that require the same (or slightly larger) amount of calibration by trial and error as training of traditional classifiers.</span></span> <span data-ttu-id="919a9-104">Здесь мы определим основные понятия и составляющие этого обучающего процесса.</span><span class="sxs-lookup"><span data-stu-id="919a9-104">Here we define the main concepts and ingredients of this training process.</span></span>

## <a name="trainingtesting-schedules"></a><span data-ttu-id="919a9-105">Расписания обучения и тестирования</span><span class="sxs-lookup"><span data-stu-id="919a9-105">Training/testing schedules</span></span>

<span data-ttu-id="919a9-106">В контексте обучения классификатора описывается подмножество примеров данных в общем обучающем или проверочном наборе.</span><span class="sxs-lookup"><span data-stu-id="919a9-106">In the context of classifier training a *schedule* describes a subset of data samples in an overall training or testing set.</span></span> <span data-ttu-id="919a9-107">Расписание обычно определяется как коллекция образцов индексов.</span><span class="sxs-lookup"><span data-stu-id="919a9-107">A schedule is usually defined as a collection of sample indices.</span></span>

## <a name="parameterbias-scores"></a><span data-ttu-id="919a9-108">Параметры/показатели смещений</span><span class="sxs-lookup"><span data-stu-id="919a9-108">Parameter/bias scores</span></span>

<span data-ttu-id="919a9-109">При наличии вектора параметров-кандидата и смещения классификатора их *Оценка* измеряется относительно выбранного расписания проверки и выражается в количестве неправильной классификации по всем примерам в расписании.</span><span class="sxs-lookup"><span data-stu-id="919a9-109">Given a candidate parameter vector and a classifier bias, their *validation score* is measured relative to a chosen validation schedule S and is expressed by a number of misclassifications counted over all the samples in the schedule S.</span></span>

## <a name="hyperparameters"></a><span data-ttu-id="919a9-110">Гиперпараметров</span><span class="sxs-lookup"><span data-stu-id="919a9-110">Hyperparameters</span></span>

<span data-ttu-id="919a9-111">Процесс обучения модели регулируется определенными предварительно заданными значениями, которые называются *параметрами*.</span><span class="sxs-lookup"><span data-stu-id="919a9-111">The model training process is governed by certain pre-set values called *hyperparameters*:</span></span>

### <a name="learning-rate"></a><span data-ttu-id="919a9-112">Скорость обучения</span><span class="sxs-lookup"><span data-stu-id="919a9-112">Learning rate</span></span>

<span data-ttu-id="919a9-113">Это один из ключевых параметров.</span><span class="sxs-lookup"><span data-stu-id="919a9-113">It is one of the key hyperparameters.</span></span> <span data-ttu-id="919a9-114">Он определяет, сколько текущая оценка метод стохастического градиента влияет на обновление параметра.</span><span class="sxs-lookup"><span data-stu-id="919a9-114">It defines how much current stochastic gradient estimate impacts the parameter update.</span></span> <span data-ttu-id="919a9-115">Размер разностного обновления параметра пропорционален скорости обучения.</span><span class="sxs-lookup"><span data-stu-id="919a9-115">The size of parameter update delta is proportional to the learning rate.</span></span> <span data-ttu-id="919a9-116">Меньшие значения скорости обучения приводят к более медленному развитию параметров и более медленному конвергенции, но чрезмерно большие значения в LR могут нарушить схождение, так как спуск градиента никогда не фиксируется на определенном локальном минимуме.</span><span class="sxs-lookup"><span data-stu-id="919a9-116">Smaller learning rate values lead to slower parameter evolution and slower convergence, but excessively large values of LR may break the convergence altogether as the gradient descent never commits to a particular local minimum.</span></span> <span data-ttu-id="919a9-117">Хотя курс обучения адаптируется к некоторой степени в соответствии с алгоритмом обучения, для него важно выбрать хорошее начальное значение.</span><span class="sxs-lookup"><span data-stu-id="919a9-117">While learning rate is adaptively adjusted by the training algorithm to some extent, selecting a good initial value for it is important.</span></span> <span data-ttu-id="919a9-118">Обычно начальное значение по умолчанию для курса обучения — 0,1.</span><span class="sxs-lookup"><span data-stu-id="919a9-118">A usual default initial value for learning rate is 0.1.</span></span> <span data-ttu-id="919a9-119">Выбор лучшего значения курса обучения — это тонкая схема (см. раздел 4,3 из Гудфеллов et al., "глубокое обучение", нажмите кнопку MIT, 2017).</span><span class="sxs-lookup"><span data-stu-id="919a9-119">Selecting the best value of learning rate is a fine art (see, for example, section 4.3 of Goodfellow et al.,"Deep learning", MIT Press, 2017).</span></span>

### <a name="minibatch-size"></a><span data-ttu-id="919a9-120">Размер уменьшив</span><span class="sxs-lookup"><span data-stu-id="919a9-120">Minibatch size</span></span>

<span data-ttu-id="919a9-121">Определяет, сколько выборок данных используется для одной оценки метод стохастического градиента.</span><span class="sxs-lookup"><span data-stu-id="919a9-121">Defines how many data samples is used for a single estimation of stochastic gradient.</span></span> <span data-ttu-id="919a9-122">Большие значения размера уменьшив обычно приводят к более надежному и монотонному конвергенции, но может замедлить процесс обучения, так как затраты на одну оценку градиента пропорциональны размеру minimatch.</span><span class="sxs-lookup"><span data-stu-id="919a9-122">Larger values of minibatch size generally lead to more robust and more monotonic convergence but can potentially slow down the training process, as the cost of any one gradient estimation is proportional to the minimatch size.</span></span> <span data-ttu-id="919a9-123">Обычно значение по умолчанию для размера уменьшив равно 10.</span><span class="sxs-lookup"><span data-stu-id="919a9-123">A usual default value for the minibatch size is 10.</span></span>

### <a name="training-epochs-tolerance-gridlocks"></a><span data-ttu-id="919a9-124">Обучающие эпохи, допуск, гридлоккс</span><span class="sxs-lookup"><span data-stu-id="919a9-124">Training epochs, tolerance, gridlocks</span></span>

<span data-ttu-id="919a9-125">«Эпоха» означает один полный проход по запланированным обучающим данным.</span><span class="sxs-lookup"><span data-stu-id="919a9-125">"Epoch" means one complete pass through the scheduled training data.</span></span>
<span data-ttu-id="919a9-126">Максимальное число эпох на обучающий поток (см. ниже) должно быть ограничено.</span><span class="sxs-lookup"><span data-stu-id="919a9-126">The maximum number of epochs per a training thread (see below) should be capped.</span></span> <span data-ttu-id="919a9-127">Поток обучения определяется как завершенный (с наиболее известными параметрами-кандидатами) при выполнении максимального числа эпох.</span><span class="sxs-lookup"><span data-stu-id="919a9-127">The training thread is defined to terminate (with the best known candidate parameters) when the maximum number of epochs has been executed.</span></span> <span data-ttu-id="919a9-128">Однако такое обучение должно завершиться раньше, если ставка неправильной классификации в расписании проверки станет ниже выбранной допустимости.</span><span class="sxs-lookup"><span data-stu-id="919a9-128">However such training would terminate earlier when misclassification rate on validation schedule falls below a chosen tolerance.</span></span> <span data-ttu-id="919a9-129">Предположим, например, что погрешность неправильной классификации равна 0,01 (1%); Если в проверочном наборе из 2000 обнаружено менее 20 недопустимых классификаций, то достигнут уровень допуска.</span><span class="sxs-lookup"><span data-stu-id="919a9-129">Suppose, for example, that misclassification tolerance is 0.01 (1%); if on validation set of 2000 samples we are seeing fewer than 20 misclassifications, then the tolerance level has been achieved.</span></span> <span data-ttu-id="919a9-130">Поток обучения также завершается преждевременно, если оценка модели-кандидата не показала никакого улучшения по нескольким последовательным эпохам (пробок).</span><span class="sxs-lookup"><span data-stu-id="919a9-130">A training thread also terminates prematurely if the validation score of the candidate model has not shown any improvement over several consecutive epochs (a gridlock).</span></span> <span data-ttu-id="919a9-131">Логика завершения пробок в настоящее время жестко закодирована.</span><span class="sxs-lookup"><span data-stu-id="919a9-131">The logic for the gridlock termination is currently hardcoded.</span></span>

### <a name="measurements-count"></a><span data-ttu-id="919a9-132">Количество измерений</span><span class="sxs-lookup"><span data-stu-id="919a9-132">Measurements count</span></span>

<span data-ttu-id="919a9-133">Оценка оценок обучения и проверки и компонентов градиента метод стохастического на устройстве такта для оценки перекрытий состояний тактов, требующих нескольких измерений соответствующего observable.</span><span class="sxs-lookup"><span data-stu-id="919a9-133">Estimating the training/validation scores and the components of the stochastic gradient on a quantum device amounts to estimating quantum state overlaps that requires multiple measurements of the appropriate observables.</span></span> <span data-ttu-id="919a9-134">Количество единиц измерения должно масштабироваться как $O (1/\ Эпсилон ^ 2) $, где $ \епсилон $ — желаемая ошибка оценки.</span><span class="sxs-lookup"><span data-stu-id="919a9-134">The number of measurements should scale as $O(1/\epsilon^2)$ where $\epsilon$ is the desired estimation error.</span></span>
<span data-ttu-id="919a9-135">Как правило, начальное количество измерений может составлять приблизительно $1/\ Mbox {допуск} ^ 2 $ (см. Определение допуска в предыдущем абзаце).</span><span class="sxs-lookup"><span data-stu-id="919a9-135">As a rule of thumb, the initial measurements count could be approximately $1/\mbox{tolerance}^2$ (see definition of tolerance in the previous paragraph).</span></span> <span data-ttu-id="919a9-136">Если шкала градиента кажется слишком неустойчивой и для достижения этого не удается добиться слишком сложного конвергенциа, необходимо будет пересмотреть число измерений вверх.</span><span class="sxs-lookup"><span data-stu-id="919a9-136">One would need to revise the measurement count upward if the gradient descent appears to be too erratic and convergence too hard to achieve.</span></span>

### <a name="training-threads"></a><span data-ttu-id="919a9-137">Обучающие потоки</span><span class="sxs-lookup"><span data-stu-id="919a9-137">Training threads</span></span>

<span data-ttu-id="919a9-138">Функция правдоподобия, которая является служебной программой для классификатора, очень редко выпуклой, то есть она обычно имеет множество локальных Оптима в пространстве параметров, которая может значительно различаться по качеству.</span><span class="sxs-lookup"><span data-stu-id="919a9-138">The likelihood function which is the training utility for the classifier is very seldom convex, meaning that it usually has a multitude of local optima in the parameter space that may differ significantly by quality.</span></span> <span data-ttu-id="919a9-139">Поскольку процесс SGD может объединять только один конкретный оптимальный способ, важно изучить несколько начальных векторов параметров.</span><span class="sxs-lookup"><span data-stu-id="919a9-139">Since the SGD process can converge to only one specific optimum, it is important to explore multiple starting parameter vectors.</span></span> <span data-ttu-id="919a9-140">В машинном обучении обычно инициализируют такие начальные векторы случайным образом.</span><span class="sxs-lookup"><span data-stu-id="919a9-140">Common practice in machine learning is to initialize such starting vectors randomly.</span></span> <span data-ttu-id="919a9-141">API обучения Q # принимает произвольный массив таких начальных векторов, но базовый код анализирует их последовательно.</span><span class="sxs-lookup"><span data-stu-id="919a9-141">The Q# training API accepts an arbitrary array of such starting vectors but the underlying code explores them sequentially.</span></span> <span data-ttu-id="919a9-142">На многоядерной компьютере или на любой архитектуре параллельных вычислений рекомендуется выполнять несколько вызовов API-интерфейса Q # Training параллельно с разными инициализациями параметров во всех вызовах.</span><span class="sxs-lookup"><span data-stu-id="919a9-142">On a multicore computer or in fact on any parallel computing architecture it is advisable to perform several calls to Q# training API in parallel with different parameter initializations across the calls.</span></span>

#### <a name="how-to-modify-the-hyperparameters"></a><span data-ttu-id="919a9-143">Изменение параметров</span><span class="sxs-lookup"><span data-stu-id="919a9-143">How to modify the hyperparameters</span></span>

<span data-ttu-id="919a9-144">В библиотеке КМЛ наилучшим способом изменения параметров является переопределение значений по умолчанию определяемого пользователем типа [`TrainingOptions`](xref:microsoft.quantum.machinelearning.trainingoptions).</span><span class="sxs-lookup"><span data-stu-id="919a9-144">In the QML library, the best way to modify the hyperparameters is by overriding the default values of the UDT [`TrainingOptions`](xref:microsoft.quantum.machinelearning.trainingoptions).</span></span> <span data-ttu-id="919a9-145">Для этого вызовите его с помощью функции [`DefaultTrainingOptions`](xref:microsoft.quantum.machinelearning.defaulttrainingoptions) и примените оператор `w/`, чтобы переопределить значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="919a9-145">To do this we call it with the function [`DefaultTrainingOptions`](xref:microsoft.quantum.machinelearning.defaulttrainingoptions) and apply the operator `w/` to override the default values.</span></span> <span data-ttu-id="919a9-146">Например, чтобы использовать измерения 100 000 и частоту обучения 0,01:</span><span class="sxs-lookup"><span data-stu-id="919a9-146">For example, to use 100,000 measurements and a learning rate of 0.01:</span></span>
 ```qsharp
let options = DefaultTrainingOptions()
w/ LearningRate <- 0.01
w/ NMeasurements <- 100000;
 ```