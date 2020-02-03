---
title: 'Все вместе — методы Q # | Документация Майкрософт'
description: 'Все вместе — методы Q #'
uid: microsoft.quantum.techniques.puttingittogether
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 3605826da159757d4b321dbf4ec6acd7f4e6be05
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820170"
---
# <a name="putting-it-all-together-teleportation"></a><span data-ttu-id="94e91-103">Совместное размещение: телепередача</span><span class="sxs-lookup"><span data-stu-id="94e91-103">Putting It All Together: Teleportation</span></span> #
<span data-ttu-id="94e91-104">Давайте вернемся к примеру канала телепереноса, определенного в [тактовой цепи](xref:microsoft.quantum.concepts.circuits).</span><span class="sxs-lookup"><span data-stu-id="94e91-104">Let's return to the example of the teleportation circuit defined in [Quantum Circuits](xref:microsoft.quantum.concepts.circuits).</span></span> <span data-ttu-id="94e91-105">Мы будем использовать его для иллюстрации концепций, которые мы узнали до сих пор.</span><span class="sxs-lookup"><span data-stu-id="94e91-105">We're going to use this to illustrate the concepts we've learned so far.</span></span> <span data-ttu-id="94e91-106">Пояснения о телепортовой телетранспортировке приведены ниже для тех, кто не знаком с теории, за которым следует пошаговое руководство по реализации кода в Q #.</span><span class="sxs-lookup"><span data-stu-id="94e91-106">An explanation of quantum teleportation is provided below for those who are unfamiliar with the theory, followed by a walkthrough of the code implementation in Q#.</span></span> 

## <a name="quantum-teleportation-theory"></a><span data-ttu-id="94e91-107">Потактовая попорция: теория</span><span class="sxs-lookup"><span data-stu-id="94e91-107">Quantum Teleportation: Theory</span></span>
<span data-ttu-id="94e91-108">Для отправки неизвестного состояния такта (которое мы будем называть "__сообщением__") из кубит в одном расположении в кубит в другом месте (мы будем ссылаться на эти Кубитс как "__здесь__"__и "in" соответственно__).</span><span class="sxs-lookup"><span data-stu-id="94e91-108">Quantum teleportation is a technique for sending an unknown quantum state (which we'll refer to as the '__message__') from a qubit in one location to a qubit in another location (we'll refer to these qubits as '__here__' and '__there__', respectively).</span></span> <span data-ttu-id="94e91-109">Мы можем представить наше __сообщение__ в виде вектора с помощью нотации Дирак:</span><span class="sxs-lookup"><span data-stu-id="94e91-109">We can represent our __message__ as a vector using Dirac notation:</span></span> 

<span data-ttu-id="94e91-110">$ $ \кет{\пси} = \алфа\кет{0} + \бета\кет{1} $ $</span><span class="sxs-lookup"><span data-stu-id="94e91-110">$$ \ket{\psi} = \alpha\ket{0} + \beta\ket{1} $$</span></span>

<span data-ttu-id="94e91-111">Состояние __сообщения__ кубит неизвестно нам, так как мы не понимаем значения $ \алфа $ и $ \бета $.</span><span class="sxs-lookup"><span data-stu-id="94e91-111">The __message__ qubit's state is unknown to us as we do not know the values of $\alpha$ and $\beta$.</span></span>

### <a name="step-1-create-an-entangled-state"></a><span data-ttu-id="94e91-112">Шаг 1. Создание состояния запутанными</span><span class="sxs-lookup"><span data-stu-id="94e91-112">Step 1: Create an entangled state</span></span>
<span data-ttu-id="94e91-113">Чтобы отправить __сообщение__ , необходимо, __чтобы кубит,__ запутанными с кубит __там__.</span><span class="sxs-lookup"><span data-stu-id="94e91-113">In order to send the __message__ we need for the qubit __here__ to be entangled with the qubit __there__.</span></span> <span data-ttu-id="94e91-114">Это достигается путем применения шлюза Хадамард, за которым следует шлюз кнот.</span><span class="sxs-lookup"><span data-stu-id="94e91-114">This is achieved by applying a Hadamard gate, followed by a CNOT gate.</span></span> <span data-ttu-id="94e91-115">Давайте взглянем на математические части этих операций Gate.</span><span class="sxs-lookup"><span data-stu-id="94e91-115">Let's look at the math behind these gate operations.</span></span>

<span data-ttu-id="94e91-116">Мы начнем с Кубитс __здесь__ , а также как в \кет, __так и в__ состоянии $:{0}$.</span><span class="sxs-lookup"><span data-stu-id="94e91-116">We will begin with the qubits __here__ and __there__ both in the $\ket{0}$ state.</span></span> <span data-ttu-id="94e91-117">После ентанглинг этих Кубитс они находятся в состоянии:</span><span class="sxs-lookup"><span data-stu-id="94e91-117">After entangling these qubits, they are in the state:</span></span>

<span data-ttu-id="94e91-118">$ $ \кет{\фи ^ +} = \фрак{1}{\скрт{2}} (\кет{00} + \кет{11}) $ $</span><span class="sxs-lookup"><span data-stu-id="94e91-118">$$ \ket{\phi^+} = \frac{1}{\sqrt{2}}(\ket{00} + \ket{11}) $$</span></span>

### <a name="step-2-send-the-message"></a><span data-ttu-id="94e91-119">Шаг 2. Отправка сообщения</span><span class="sxs-lookup"><span data-stu-id="94e91-119">Step 2: Send the message</span></span>
<span data-ttu-id="94e91-120">Чтобы отправить __сообщение__ , сначала ПРИМЕНИТе кнотный шлюз с __сообщением__ кубит, __а здесь__ кубит в качестве входных данных ( __сообщение__ кубит является элементом управления, а в данном __случае кубит — целевым кубит)__ .</span><span class="sxs-lookup"><span data-stu-id="94e91-120">To send the __message__ we first apply a CNOT gate with the __message__ qubit and __here__ qubit as inputs (the __message__ qubit being the control and the __here__ qubit being the target qubit, in this instance).</span></span> <span data-ttu-id="94e91-121">Входное состояние может быть написано:</span><span class="sxs-lookup"><span data-stu-id="94e91-121">This input state can be written:</span></span>

<span data-ttu-id="94e91-122">$ $ \кет{\пси}\кет{\фи ^ +} = (\алфа\кет{0} + \бета\кет{1}) (\фрак{1}{\скрт{2}} (\кет{00} + \кет{11})) $ $</span><span class="sxs-lookup"><span data-stu-id="94e91-122">$$ \ket{\psi}\ket{\phi^+} = (\alpha\ket{0} + \beta\ket{1})(\frac{1}{\sqrt{2}}(\ket{00} + \ket{11})) $$</span></span>

<span data-ttu-id="94e91-123">Это расширяется до:</span><span class="sxs-lookup"><span data-stu-id="94e91-123">This expands to:</span></span>

<span data-ttu-id="94e91-124">$ $ \кет{\пси}\кет{\фи ^ +} = \фрак{\алфа}{\скрт{2}} \кет{000} + \фрак{\алфа}{\скрт{2}} \кет{011} + \фрак{\бета}{\скрт{2}} \ket{100} + \frac{\beta}{\sqrt{2}} \ket{111} $ $</span><span class="sxs-lookup"><span data-stu-id="94e91-124">$$ \ket{\psi}\ket{\phi^+} = \frac{\alpha}{\sqrt{2}}\ket{000} + \frac{\alpha}{\sqrt{2}}\ket{011} + \frac{\beta}{\sqrt{2}}\ket{100} + \frac{\beta}{\sqrt{2}}\ket{111} $$</span></span>

<span data-ttu-id="94e91-125">Как напоминание, шлюз кнот переворачивает целевой кубит, когда элемент управления кубит равен 1.</span><span class="sxs-lookup"><span data-stu-id="94e91-125">As a reminder, the CNOT gate flips the target qubit when the control qubit is 1.</span></span> <span data-ttu-id="94e91-126">Например, входные данные $ \кет{000}$ не будут изменяться, так как первый кубит (элемент управления) равен 0.</span><span class="sxs-lookup"><span data-stu-id="94e91-126">So for example, an input of $\ket{000}$ will result in no change as the first qubit (the control) is 0.</span></span> <span data-ttu-id="94e91-127">Однако возьмем случай, когда первый кубит имеет значение 1, например входные данные $ \кет{100}$.</span><span class="sxs-lookup"><span data-stu-id="94e91-127">However, take a case where the first qubit is 1 - for example an input of $\ket{100}$.</span></span> <span data-ttu-id="94e91-128">В этом экземпляре выходные данные имеют значение $ \кет{110}$, так как второй кубит (целевой объект) зеркально отражается шлюзом кнот.</span><span class="sxs-lookup"><span data-stu-id="94e91-128">In this instance, the output is $\ket{110}$ as the second qubit (the target) is flipped by the CNOT gate.</span></span>

<span data-ttu-id="94e91-129">Давайте теперь рассмотрим наши выходные данные, когда кнот ворота полагается на наши входные данные выше.</span><span class="sxs-lookup"><span data-stu-id="94e91-129">Let's now consider our output once the CNOT gate has acted on our input above.</span></span> <span data-ttu-id="94e91-130">Результат:</span><span class="sxs-lookup"><span data-stu-id="94e91-130">The result is:</span></span>

<span data-ttu-id="94e91-131">$ $ \фрак{\алфа}{\скрт{2}} \кет{000} + \фрак{\алфа}{\скрт{2}} \кет{011} + \фрак{\бета}{\скрт{2}} \кет{110} + \фрак{\бета}{\скрт{2}} \ket{101} $ $</span><span class="sxs-lookup"><span data-stu-id="94e91-131">$$ \frac{\alpha}{\sqrt{2}}\ket{000} + \frac{\alpha}{\sqrt{2}}\ket{011} + \frac{\beta}{\sqrt{2}}\ket{110} + \frac{\beta}{\sqrt{2}}\ket{101} $$</span></span>

<span data-ttu-id="94e91-132">Следующим шагом для отправки __сообщения__ является применение шлюза хадамард к __сообщению__ кубит (первое кубит каждого термина).</span><span class="sxs-lookup"><span data-stu-id="94e91-132">The next step to send the __message__ is to apply a Hadamard gate to the __message__ qubit (that's the first qubit of each term).</span></span> 

<span data-ttu-id="94e91-133">Как напоминание, шлюз Хадамард выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="94e91-133">As a reminder, the Hadamard gate does the following:</span></span>

<span data-ttu-id="94e91-134">Входные данные</span><span class="sxs-lookup"><span data-stu-id="94e91-134">Input</span></span> | <span data-ttu-id="94e91-135">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="94e91-135">Output</span></span>
---------------------------| ---------------------------------------------------------------
<span data-ttu-id="94e91-136">$ \кет{0}$</span><span class="sxs-lookup"><span data-stu-id="94e91-136">$\ket{0}$</span></span>  | <span data-ttu-id="94e91-137">$ \фрак{1}{\скрт{2}} (\кет{0} + \кет{1}) $</span><span class="sxs-lookup"><span data-stu-id="94e91-137">$\frac{1}{\sqrt{2}}(\ket{0} + \ket{1})$</span></span>
<span data-ttu-id="94e91-138">$ \кет{1}$</span><span class="sxs-lookup"><span data-stu-id="94e91-138">$\ket{1}$</span></span>  | <span data-ttu-id="94e91-139">$ \фрак{1}{\скрт{2}} (\кет{0} — \кет{1}) $</span><span class="sxs-lookup"><span data-stu-id="94e91-139">$\frac{1}{\sqrt{2}}(\ket{0} - \ket{1})$</span></span>

<span data-ttu-id="94e91-140">Если применить шлюз Хадамард к первому кубиту каждого из приведенных выше выходных данных, мы получаем следующий результат:</span><span class="sxs-lookup"><span data-stu-id="94e91-140">If we apply the Hadamard gate to the first qubit of each term of our output above, we get the following result:</span></span>

<span data-ttu-id="94e91-141">$ $ \фрак{\алфа}{\скрт{2}} (\фрак{1}{\скрт{2}} (\кет{0} + \кет{1})) \кет{00} + \фрак{\алфа}{\скрт{2}} (\фрак{1}{\скрт{2}} (\кет{0} + \кет{1})) \ket{11} + \frac{\beta}{\sqrt{2}} (\frac{1}{\sqrt{2}} (\ket{0}-\ket{1})) \ket{10} + \frac{\beta}{\sqrt{2}} (\frac{1}{\sqrt{2}} (\ket{0}-\ket{1})) \ket{01} $ $</span><span class="sxs-lookup"><span data-stu-id="94e91-141">$$ \frac{\alpha}{\sqrt{2}}(\frac{1}{\sqrt{2}}(\ket{0} + \ket{1}))\ket{00} + \frac{\alpha}{\sqrt{2}}(\frac{1}{\sqrt{2}}(\ket{0} + \ket{1}))\ket{11} + \frac{\beta}{\sqrt{2}}(\frac{1}{\sqrt{2}}(\ket{0} - \ket{1}))\ket{10} + \frac{\beta}{\sqrt{2}}(\frac{1}{\sqrt{2}}(\ket{0} - \ket{1}))\ket{01} $$</span></span>

<span data-ttu-id="94e91-142">Обратите внимание, что каждый термин имеет $2 \фрак{1}{\скрт{2}} $ факторов.</span><span class="sxs-lookup"><span data-stu-id="94e91-142">Note that each term has two $\frac{1}{\sqrt{2}}$ factors.</span></span> <span data-ttu-id="94e91-143">Мы можем умножить эти данные, предоставив следующий результат:</span><span class="sxs-lookup"><span data-stu-id="94e91-143">We can multiply these out giving the following result:</span></span>

<span data-ttu-id="94e91-144">$ $ \фрак{\алфа}{2}(\кет{0} + \кет{1}) \кет{00} + \фрак{\алфа}{2}(\кет{0} + \кет{1}) \кет{11} + \фрак{\бета}{2}(\кет{0}-\кет{1}) \кет{10} + \фрак{\бета}{2}(\ket{0}-\ket{1}) \ket{01} $ $</span><span class="sxs-lookup"><span data-stu-id="94e91-144">$$ \frac{\alpha}{2}(\ket{0} + \ket{1})\ket{00} + \frac{\alpha}{2}(\ket{0} + \ket{1})\ket{11} + \frac{\beta}{2}(\ket{0} - \ket{1})\ket{10} + \frac{\beta}{2}(\ket{0} - \ket{1})\ket{01} $$</span></span>

<span data-ttu-id="94e91-145">Параметр $ \фрак{1}{2}$ является общим для каждого термина, поэтому теперь его можно использовать за пределами квадратных скобок:</span><span class="sxs-lookup"><span data-stu-id="94e91-145">The  $\frac{1}{2}$ factor is common to each term so we can now take it outside the brackets:</span></span>

<span data-ttu-id="94e91-146">$ $ \фрак{1}{2}\биг [\алфа (\кет{0} + \кет{1}) \кет{00} + \алфа (\кет{0} + \кет{1}) \кет{11} + \бета (\кет{0}-\кет{1}) \кет{10} + \бета (\кет{0}-\кет{1}) \ket{01}\big] $ $</span><span class="sxs-lookup"><span data-stu-id="94e91-146">$$ \frac{1}{2}\big[\alpha(\ket{0} + \ket{1})\ket{00} + \alpha(\ket{0} + \ket{1})\ket{11} + \beta(\ket{0} - \ket{1})\ket{10} + \beta(\ket{0} - \ket{1})\ket{01}\big] $$</span></span>

<span data-ttu-id="94e91-147">Затем можно умножить квадратные скобки для каждого термина:</span><span class="sxs-lookup"><span data-stu-id="94e91-147">We can then multiply out the brackets for each term giving:</span></span>

<span data-ttu-id="94e91-148">$ $ \фрак{1}{2}\биг [\алфа\кет{000} + \алфа\кет{100} + \алфа\кет{011} + \алфа\кет{111} + \бета\кет{010}-\бета\кет{110} + \бета\кет{001}-\beta\ket{101}\big] $ $</span><span class="sxs-lookup"><span data-stu-id="94e91-148">$$ \frac{1}{2}\big[\alpha\ket{000} + \alpha\ket{100} + \alpha\ket{011} + \alpha\ket{111} + \beta\ket{010} - \beta\ket{110} + \beta\ket{001} - \beta\ket{101}\big] $$</span></span>

### <a name="step-3-measure-the-result"></a><span data-ttu-id="94e91-149">Шаг 3. Измерение результата</span><span class="sxs-lookup"><span data-stu-id="94e91-149">Step 3: Measure the result</span></span>

<span data-ttu-id="94e91-150">Из-за __того, что__ у вас __есть__ запутанными, любое измерение в __этом__ случае повлияет на его __состояние.__</span><span class="sxs-lookup"><span data-stu-id="94e91-150">Due to __here__ and __there__ being entangled, any measurement on __here__ will affect the state of __there__.</span></span> <span data-ttu-id="94e91-151">Если мы измеряем первый и второй кубит (__сообщение__ и __здесь__), то можете узнать, какое состояние __есть__ в связи с этим свойством замкнутые.</span><span class="sxs-lookup"><span data-stu-id="94e91-151">If we measure the first and second qubit (__message__ and __here__) we can learn what state __there__ is in, due to this property of entanglement.</span></span> 

* <span data-ttu-id="94e91-152">Если мы измеряем и получаем результат 00, то в самом простом месте сворачивается только термин, который соответствует этому результату.</span><span class="sxs-lookup"><span data-stu-id="94e91-152">If we measure and get a result 00, the superposition collapses, leaving only terms consistent with this result.</span></span> <span data-ttu-id="94e91-153">Это $ \алфа\кет{000} + \бета\кет{001}$.</span><span class="sxs-lookup"><span data-stu-id="94e91-153">That's $\alpha\ket{000} +\beta\ket{001}$.</span></span> <span data-ttu-id="94e91-154">Для этого можно выполнить рефакторинг до $ \кет{00}(\алфа\кет{0} + \бета\кет{1}) $.</span><span class="sxs-lookup"><span data-stu-id="94e91-154">This can be refactored to $\ket{00}(\alpha\ket{0} +\beta\ket{1})$.</span></span> <span data-ttu-id="94e91-155">Поэтому при измерении первого и второго кубита до 00 мы __понимаем, что третий кубит, находится__в состоянии $ (\алфа\кет{0} + \бета\кет{1}) $.</span><span class="sxs-lookup"><span data-stu-id="94e91-155">Therefore if we measure the first and second qubit to be 00, we know that the third qubit, __there__, is in the state $(\alpha\ket{0} +\beta\ket{1})$.</span></span>
* <span data-ttu-id="94e91-156">Если мы измеряем и получаем результат 01, то переворачивание будет приводить к тому, что покидает только термины, соответствующие этому результату.</span><span class="sxs-lookup"><span data-stu-id="94e91-156">If we measure and get a result 01, the superposition collapses, leaving only terms consistent with this result.</span></span> <span data-ttu-id="94e91-157">Это $ \алфа\кет{011} + \бета\кет{010}$.</span><span class="sxs-lookup"><span data-stu-id="94e91-157">That's $\alpha\ket{011} +\beta\ket{010}$.</span></span> <span data-ttu-id="94e91-158">Для этого можно выполнить рефакторинг до $ \кет{01}(\алфа\кет{1} + \бета\кет{0}) $.</span><span class="sxs-lookup"><span data-stu-id="94e91-158">This can be refactored to $\ket{01}(\alpha\ket{1} +\beta\ket{0})$.</span></span> <span data-ttu-id="94e91-159">Поэтому, если измерение первого и второго кубита равно 01, мы __понимаем, что третий кубит, находится__в состоянии $ (\алфа\кет{1} + \бета\кет{0}) $.</span><span class="sxs-lookup"><span data-stu-id="94e91-159">Therefore if we measure the first and second qubit to be 01, we know that the third qubit, __there__, is in the state $(\alpha\ket{1} +\beta\ket{0})$.</span></span>
* <span data-ttu-id="94e91-160">Если мы измеряем и получаем результат 10, в нем сворачивается только термин, содержащий только те термины, которые соответствуют этому результату.</span><span class="sxs-lookup"><span data-stu-id="94e91-160">If we measure and get a result 10, the superposition collapses, leaving only terms consistent with this result.</span></span> <span data-ttu-id="94e91-161">Это $ \алфа\кет{100}-\бета\кет{101}$.</span><span class="sxs-lookup"><span data-stu-id="94e91-161">That's $\alpha\ket{100} -\beta\ket{101}$.</span></span> <span data-ttu-id="94e91-162">Для этого можно выполнить рефакторинг для $ \кет{10}(\алфа\кет{0}-\бета\кет{1}) $.</span><span class="sxs-lookup"><span data-stu-id="94e91-162">This can be refactored to $\ket{10}(\alpha\ket{0} -\beta\ket{1})$.</span></span> <span data-ttu-id="94e91-163">Поэтому при измерении первого и второго кубита до 10 мы __понимаем, что третья кубит, находится__в состоянии $ (\алфа\кет{0}-\бета\кет{1}) $.</span><span class="sxs-lookup"><span data-stu-id="94e91-163">Therefore if we measure the first and second qubit to be 10, we know that the third qubit, __there__, is in the state $(\alpha\ket{0} -\beta\ket{1})$.</span></span>
* <span data-ttu-id="94e91-164">Если мы измеряем и получаем результат 11, то в самом простом месте сворачивается только термин, который соответствует этому результату.</span><span class="sxs-lookup"><span data-stu-id="94e91-164">If we measure and get a result 11, the superposition collapses, leaving only terms consistent with this result.</span></span> <span data-ttu-id="94e91-165">Это $ \алфа\кет{111}-\бета\кет{110}$.</span><span class="sxs-lookup"><span data-stu-id="94e91-165">That's $\alpha\ket{111} -\beta\ket{110}$.</span></span> <span data-ttu-id="94e91-166">Для этого можно выполнить рефакторинг для $ \кет{11}(\алфа\кет{1}-\бета\кет{0}) $.</span><span class="sxs-lookup"><span data-stu-id="94e91-166">This can be refactored to $\ket{11}(\alpha\ket{1} -\beta\ket{0})$.</span></span> <span data-ttu-id="94e91-167">Поэтому при измерении первого и второго кубита до 11 мы __понимаем, что третья кубит, находится__в состоянии $ (\алфа\кет{1}-\бета\кет{0}) $.</span><span class="sxs-lookup"><span data-stu-id="94e91-167">Therefore if we measure the first and second qubit to be 11, we know that the third qubit, __there__, is in the state $(\alpha\ket{1} -\beta\ket{0})$.</span></span>

### <a name="step-4-interpret-the-result"></a><span data-ttu-id="94e91-168">Шаг 4. анализ результата</span><span class="sxs-lookup"><span data-stu-id="94e91-168">Step 4: Interpret the result</span></span>

<span data-ttu-id="94e91-169">Как напоминание, исходное __сообщение__ , которое мы хотели отправить:</span><span class="sxs-lookup"><span data-stu-id="94e91-169">As a reminder, the original __message__ we wished to send was:</span></span>

<span data-ttu-id="94e91-170">$ $ \кет{\пси} = \алфа\кет{0} + \бета\кет{1} $ $</span><span class="sxs-lookup"><span data-stu-id="94e91-170">$$ \ket{\psi} = \alpha\ket{0} + \beta\ket{1} $$</span></span>

<span data-ttu-id="94e91-171">Нам нужно __получить кубит в__ этом состоянии, чтобы полученное состояние было назначено.</span><span class="sxs-lookup"><span data-stu-id="94e91-171">We need to get the __there__ qubit into this state, so that the received state is the one that was intended.</span></span> 

* <span data-ttu-id="94e91-172">Если мы измеряем и получили результат __00, третье кубит, находится__в состоянии $ (\алфа\кет{0} + \бета\кет{1}) $.</span><span class="sxs-lookup"><span data-stu-id="94e91-172">If we measured and got a result of 00, then the third qubit, __there__, is in the state $(\alpha\ket{0} +\beta\ket{1})$.</span></span> <span data-ttu-id="94e91-173">Так как это __сообщение__является предполагаемым, изменения не требуются.</span><span class="sxs-lookup"><span data-stu-id="94e91-173">As this is the intended __message__, no alteration is required.</span></span>
* <span data-ttu-id="94e91-174">Если мы измеряем и получили результат __01, третье кубит, находится__в состоянии $ (\алфа\кет{1} + \бета\кет{0}) $.</span><span class="sxs-lookup"><span data-stu-id="94e91-174">If we measured and got a result of 01, then the third qubit, __there__, is in the state $(\alpha\ket{1} +\beta\ket{0})$.</span></span> <span data-ttu-id="94e91-175">Это отличается от предполагаемого __сообщения__, но применение не шлюза дает нам требуемое состояние $ (\алфа\кет{0} + \бета\кет{1}) $.</span><span class="sxs-lookup"><span data-stu-id="94e91-175">This differs from the intended __message__, however applying a NOT gate gives us the desired state $(\alpha\ket{0} +\beta\ket{1})$.</span></span>
* <span data-ttu-id="94e91-176">Если мы измеряем и получили результат __10, третье кубит, находится__в состоянии $ (\алфа\кет{0}-\бета\кет{1}) $.</span><span class="sxs-lookup"><span data-stu-id="94e91-176">If we measured and got a result of 10, then the third qubit, __there__, is in the state $(\alpha\ket{0} -\beta\ket{1})$.</span></span> <span data-ttu-id="94e91-177">Это отличается от предполагаемого __сообщения__, однако применение шлюза Z дает нам требуемое состояние $ (\алфа\кет{0} + \бета\кет{1}) $.</span><span class="sxs-lookup"><span data-stu-id="94e91-177">This differs from the intended __message__, however applying a Z gate gives us the desired state $(\alpha\ket{0} +\beta\ket{1})$.</span></span>
* <span data-ttu-id="94e91-178">Если мы измеряем и получили результат __11, третье кубит, находится__в состоянии $ (\алфа\кет{1}-\бета\кет{0}) $.</span><span class="sxs-lookup"><span data-stu-id="94e91-178">If we measured and got a result of 11, then the third qubit, __there__, is in the state $(\alpha\ket{1} -\beta\ket{0})$.</span></span> <span data-ttu-id="94e91-179">Это отличается от предполагаемого __сообщения__, однако применение нешлюза, за которым следует шлюз Z, дает нам требуемое состояние $ (\алфа\кет{0} + \бета\кет{1}) $.</span><span class="sxs-lookup"><span data-stu-id="94e91-179">This differs from the intended __message__, however applying a NOT gate followed by a Z gate gives us the desired state $(\alpha\ket{0} +\beta\ket{1})$.</span></span>

<span data-ttu-id="94e91-180">Если мы измеряем, а первый кубит — 1, то применяется вентиль Z.</span><span class="sxs-lookup"><span data-stu-id="94e91-180">To summarize, if we measure and the first qubit is 1, a Z gate is applied.</span></span> <span data-ttu-id="94e91-181">Если мы измеряем, а второй кубит — 1, то применяется Шлюз NOT.</span><span class="sxs-lookup"><span data-stu-id="94e91-181">If we measure and the second qubit is 1, a NOT gate is applied.</span></span>

### <a name="summary"></a><span data-ttu-id="94e91-182">Сводка</span><span class="sxs-lookup"><span data-stu-id="94e91-182">Summary</span></span>
<span data-ttu-id="94e91-183">Ниже приведена тактовая цепь в виде текстовых пошаговых схем, в которой реализована телефонная линия.</span><span class="sxs-lookup"><span data-stu-id="94e91-183">Shown below is a text-book quantum circuit that implements the teleportation.</span></span> <span data-ttu-id="94e91-184">Перемещаясь слева направо, можно увидеть следующее:</span><span class="sxs-lookup"><span data-stu-id="94e91-184">Moving from left to right you can see:</span></span>
- <span data-ttu-id="94e91-185">Шаг 1. Ентанглинг __здесь__ и в __нем__ применяет шлюз хадамард и шлюз кнот.</span><span class="sxs-lookup"><span data-stu-id="94e91-185">Step 1: Entangling __here__ and __there__ by applying a Hadamard gate and CNOT gate.</span></span>
- <span data-ttu-id="94e91-186">Шаг 2. Отправка __сообщения__ с помощью шлюза кнот и шлюза хадамард.</span><span class="sxs-lookup"><span data-stu-id="94e91-186">Step 2: Sending the __message__ using a CNOT gate and a Hadamard gate.</span></span>
- <span data-ttu-id="94e91-187">Шаг 3. Получение измерения первого и второго Кубитс, __сообщения__ и __здесь__.</span><span class="sxs-lookup"><span data-stu-id="94e91-187">Step 3: Taking a measurement of the first and second qubits, __message__ and __here__.</span></span>
- <span data-ttu-id="94e91-188">Шаг 4. применение шлюза, не шлюза или Z, в зависимости от результата измерения в шаге 3.</span><span class="sxs-lookup"><span data-stu-id="94e91-188">Step 4: Applying a NOT gate or a Z gate, depending on the result of the measurement in step 3.</span></span>

!["Телепортируйтесь (MSG: кубит, кубит): Unit"](~/media/teleportation.svg)

## <a name="quantum-teleportation-code"></a><span data-ttu-id="94e91-190">Номер телепередачи такта: код</span><span class="sxs-lookup"><span data-stu-id="94e91-190">Quantum Teleportation: Code</span></span>

<span data-ttu-id="94e91-191">У нас есть наш канал для пов тактовую транспортировку:</span><span class="sxs-lookup"><span data-stu-id="94e91-191">We have our circuit for quantum teleportation:</span></span>

!["Телепортируйтесь (MSG: кубит, кубит): Unit"](~/media/teleportation.svg)

<span data-ttu-id="94e91-193">Теперь мы можем преобразовать каждый шаг в этом такте в Q #.</span><span class="sxs-lookup"><span data-stu-id="94e91-193">We can now translate each of the steps in this quantum circuit into Q#.</span></span>

### <a name="step-0-definition"></a><span data-ttu-id="94e91-194">Шаг 0. определение</span><span class="sxs-lookup"><span data-stu-id="94e91-194">Step 0: Definition</span></span>
<span data-ttu-id="94e91-195">При выполнении телепередачи необходимо сообщить __сообщение__ , которое мы хотим отправить, и куда мы хотим отправить его (__там__).</span><span class="sxs-lookup"><span data-stu-id="94e91-195">When we perform teleportation, we must know the __message__ we wish to send, and where we wish to send it (__there__).</span></span> <span data-ttu-id="94e91-196">По этой причине мы начнем с определения новой операции телепортируйтесь, которая выдает два Кубитс в качестве аргументов, `msg` и `there`:</span><span class="sxs-lookup"><span data-stu-id="94e91-196">For this reason, we begin by defining a new Teleport operation that is given two qubits as arguments, `msg` and `there`:</span></span>

```qsharp
operation Teleport(msg : Qubit, there : Qubit) : Unit {
```

<span data-ttu-id="94e91-197">Также необходимо выделить кубит `here`, который мы достиг `using` блока:</span><span class="sxs-lookup"><span data-stu-id="94e91-197">We also need to allocate a qubit `here` which we achieve with a `using` block:</span></span>

```qsharp
    using (here = Qubit()) {
```

### <a name="step-1-create-an-entangled-state"></a><span data-ttu-id="94e91-198">Шаг 1. Создание состояния запутанными</span><span class="sxs-lookup"><span data-stu-id="94e91-198">Step 1: Create an entangled state</span></span>
<span data-ttu-id="94e91-199">Затем можно создать пару запутанными между `here` и `there` с помощью операций @"microsoft.quantum.intrinsic.h" и @"microsoft.quantum.intrinsic.cnot":</span><span class="sxs-lookup"><span data-stu-id="94e91-199">We can then create the entangled pair between `here` and `there` by using the @"microsoft.quantum.intrinsic.h" and @"microsoft.quantum.intrinsic.cnot" operations:</span></span>

```qsharp
        H(here);
        CNOT(here, there);
```

### <a name="step-2-send-the-message"></a><span data-ttu-id="94e91-200">Шаг 2. Отправка сообщения</span><span class="sxs-lookup"><span data-stu-id="94e91-200">Step 2: Send the message</span></span>
<span data-ttu-id="94e91-201">Затем мы используем следующий $ \Операторнаме{кнот} $ и $H $ Гейтс, чтобы переместить сообщение кубит:</span><span class="sxs-lookup"><span data-stu-id="94e91-201">We then use the next $\operatorname{CNOT}$ and $H$ gates to move our message qubit:</span></span>

```qsharp
        CNOT(msg, here);
        H(msg);
```

### <a name="step-3--4-measuring-and-interpreting-the-result"></a><span data-ttu-id="94e91-202">Шаг 3 & 4. измерение и анализ результата</span><span class="sxs-lookup"><span data-stu-id="94e91-202">Step 3 & 4: Measuring and interpreting the result</span></span>
<span data-ttu-id="94e91-203">Наконец, мы используем @"microsoft.quantum.intrinsic.m" для выполнения измерений и выполнения необходимых операций Gate для получения требуемого состояния, как показано в инструкциях `if`:</span><span class="sxs-lookup"><span data-stu-id="94e91-203">Finally, we use @"microsoft.quantum.intrinsic.m" to perform the measurements and perform the necessary gate operations to get the desired state, as denoted by `if` statements:</span></span>

```qsharp
        // Measure out the entanglement
        if (M(msg) == One)  { Z(there); }
        if (M(here) == One) { X(there); }
```

<span data-ttu-id="94e91-204">После этого определение оператора для передачи по номеру завершится, так что мы можем освободить `here`, завершить тело и завершить операцию.</span><span class="sxs-lookup"><span data-stu-id="94e91-204">This finishes the definition of our teleportation operator, so we can deallocate `here`, end the body, and end the operation.</span></span>

```qsharp
    }
}
```
