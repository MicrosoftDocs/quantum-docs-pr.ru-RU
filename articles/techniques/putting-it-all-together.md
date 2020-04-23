---
title: Методы - Сложить все это вместе
description: Прогулка по основной программе, которая демонстрирует квантовую телепортацию.
uid: microsoft.quantum.techniques.puttingittogether
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 4bd91699017e4c1acd9f4449b8a65e39bd07878e
ms.sourcegitcommit: b6b8459eb654040f1e19f66411b29fc9e48e95c9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2020
ms.locfileid: "82030571"
---
# <a name="putting-it-all-together-teleportation"></a><span data-ttu-id="ca422-103">Ввод все это вместе: Телепортация</span><span class="sxs-lookup"><span data-stu-id="ca422-103">Putting It All Together: Teleportation</span></span> #
<span data-ttu-id="ca422-104">Вернемся к примеру телепортации цепи, определенной в [квантовых цепях.](xref:microsoft.quantum.concepts.circuits)</span><span class="sxs-lookup"><span data-stu-id="ca422-104">Let's return to the example of the teleportation circuit defined in [Quantum Circuits](xref:microsoft.quantum.concepts.circuits).</span></span> <span data-ttu-id="ca422-105">Мы собираемся использовать это, чтобы проиллюстрировать концепции, которые мы узнали до сих пор.</span><span class="sxs-lookup"><span data-stu-id="ca422-105">We're going to use this to illustrate the concepts we've learned so far.</span></span> <span data-ttu-id="ca422-106">Объяснение квантовой телепортации приведено ниже для тех, кто не знаком с теорией, а затем пошаговое решение о реализации кода в q.</span><span class="sxs-lookup"><span data-stu-id="ca422-106">An explanation of quantum teleportation is provided below for those who are unfamiliar with the theory, followed by a walkthrough of the code implementation in Q#.</span></span> 

## <a name="quantum-teleportation-theory"></a><span data-ttu-id="ca422-107">Квантовая телепортация: Теория</span><span class="sxs-lookup"><span data-stu-id="ca422-107">Quantum Teleportation: Theory</span></span>
<span data-ttu-id="ca422-108">Квантовая телепортация — это метод отправки неизвестного квантового состояния (которое мы назначам как __«сообщение»)__ от кубитов в одном месте к кубиту в другом месте (мы будем называть эти кубитовые кубитоты «__здесь»__ и __«там»,__ соответственно).</span><span class="sxs-lookup"><span data-stu-id="ca422-108">Quantum teleportation is a technique for sending an unknown quantum state (which we'll refer to as the '__message__') from a qubit in one location to a qubit in another location (we'll refer to these qubits as '__here__' and '__there__', respectively).</span></span> <span data-ttu-id="ca422-109">Мы можем представить наше __сообщение__ как вектор, используя обозначение Dirac:</span><span class="sxs-lookup"><span data-stu-id="ca422-109">We can represent our __message__ as a vector using Dirac notation:</span></span> 

<span data-ttu-id="ca422-110">$$ »кет»пси»{0} {1}</span><span class="sxs-lookup"><span data-stu-id="ca422-110">$$ \ket{\psi} = \alpha\ket{0} + \beta\ket{1} $$</span></span>

<span data-ttu-id="ca422-111">Состояние __сообщения__ qubit нам неизвестно, так как мы не знаем значений $'alpha$ и $'beta$.</span><span class="sxs-lookup"><span data-stu-id="ca422-111">The __message__ qubit's state is unknown to us as we do not know the values of $\alpha$ and $\beta$.</span></span>

### <a name="step-1-create-an-entangled-state"></a><span data-ttu-id="ca422-112">Шаг 1: Создать запутавное состояние</span><span class="sxs-lookup"><span data-stu-id="ca422-112">Step 1: Create an entangled state</span></span>
<span data-ttu-id="ca422-113">Для того, чтобы отправить __сообщение__ нам нужно для кубит __здесь,__ чтобы быть запутался с кубитом __там__.</span><span class="sxs-lookup"><span data-stu-id="ca422-113">In order to send the __message__ we need for the qubit __here__ to be entangled with the qubit __there__.</span></span> <span data-ttu-id="ca422-114">Это достигается путем применения ворот Хадамард, а затем ворота CNOT.</span><span class="sxs-lookup"><span data-stu-id="ca422-114">This is achieved by applying a Hadamard gate, followed by a CNOT gate.</span></span> <span data-ttu-id="ca422-115">Давайте посмотрим на математику за этими операциями ворот.</span><span class="sxs-lookup"><span data-stu-id="ca422-115">Let's look at the math behind these gate operations.</span></span>

<span data-ttu-id="ca422-116">Мы начнем с кубитов __здесь__ и __там__ как{0}в $ кет $ состоянии.</span><span class="sxs-lookup"><span data-stu-id="ca422-116">We will begin with the qubits __here__ and __there__ both in the $\ket{0}$ state.</span></span> <span data-ttu-id="ca422-117">После запутывания этих кубитов, они находятся в состоянии:</span><span class="sxs-lookup"><span data-stu-id="ca422-117">After entangling these qubits, they are in the state:</span></span>

<span data-ttu-id="ca422-118">$$ (кет)) - (фрак){1}{2}{00} {11}</span><span class="sxs-lookup"><span data-stu-id="ca422-118">$$ \ket{\phi^+} = \frac{1}{\sqrt{2}}(\ket{00} + \ket{11}) $$</span></span>

### <a name="step-2-send-the-message"></a><span data-ttu-id="ca422-119">Шаг 2: Отправить сообщение</span><span class="sxs-lookup"><span data-stu-id="ca422-119">Step 2: Send the message</span></span>
<span data-ttu-id="ca422-120">Для отправки __сообщения__ мы сначала применить cNOT ворота с __сообщением__ кубит и __здесь__ кубит, как входы __(сообщение__ кубит является контроль и __здесь__ кубит является целевой кубит, в данном случае).</span><span class="sxs-lookup"><span data-stu-id="ca422-120">To send the __message__ we first apply a CNOT gate with the __message__ qubit and __here__ qubit as inputs (the __message__ qubit being the control and the __here__ qubit being the target qubit, in this instance).</span></span> <span data-ttu-id="ca422-121">Это состояние ввода может быть написано:</span><span class="sxs-lookup"><span data-stu-id="ca422-121">This input state can be written:</span></span>

<span data-ttu-id="ca422-122">$${0} (кет)-пси-кет-фи) (альфа-кет) («Альфа»кет) («фэк»{1}кет)( «фрак»{11}{1}ксрт{2}(кет ){00}</span><span class="sxs-lookup"><span data-stu-id="ca422-122">$$ \ket{\psi}\ket{\phi^+} = (\alpha\ket{0} + \beta\ket{1})(\frac{1}{\sqrt{2}}(\ket{00} + \ket{11})) $$</span></span>

<span data-ttu-id="ca422-123">Это распространяется на:</span><span class="sxs-lookup"><span data-stu-id="ca422-123">This expands to:</span></span>

<span data-ttu-id="ca422-124">$$ (кет) «пси» (кет) и «фрак»-альфа» (frac)-альфа»{2}{000} (frac) «фрак»{2}(кет) »квет»-{011} {2}{100} {2}{111}</span><span class="sxs-lookup"><span data-stu-id="ca422-124">$$ \ket{\psi}\ket{\phi^+} = \frac{\alpha}{\sqrt{2}}\ket{000} + \frac{\alpha}{\sqrt{2}}\ket{011} + \frac{\beta}{\sqrt{2}}\ket{100} + \frac{\beta}{\sqrt{2}}\ket{111} $$</span></span>

<span data-ttu-id="ca422-125">Напоминаем, что ворота CNOT переворачивает целевой кубит, когда кубит управления равен 1.</span><span class="sxs-lookup"><span data-stu-id="ca422-125">As a reminder, the CNOT gate flips the target qubit when the control qubit is 1.</span></span> <span data-ttu-id="ca422-126">Так, например, вход в ${000}$ не приведет к никаким изменениям, как первый кубит (контроль) составляет 0.</span><span class="sxs-lookup"><span data-stu-id="ca422-126">So for example, an input of $\ket{000}$ will result in no change as the first qubit (the control) is 0.</span></span> <span data-ttu-id="ca422-127">Тем не менее, возьмем случай, когда первый кубит составляет 1{100}- например, вход в $ $ .</span><span class="sxs-lookup"><span data-stu-id="ca422-127">However, take a case where the first qubit is 1 - for example an input of $\ket{100}$.</span></span> <span data-ttu-id="ca422-128">В этом случае выход составляет ${110}$ в качестве второго кубитов (цель) переворачивается на ворота CNOT.</span><span class="sxs-lookup"><span data-stu-id="ca422-128">In this instance, the output is $\ket{110}$ as the second qubit (the target) is flipped by the CNOT gate.</span></span>

<span data-ttu-id="ca422-129">Давайте теперь рассмотрим наш выход после того, как ворота CNOT действовали на наш вклад выше.</span><span class="sxs-lookup"><span data-stu-id="ca422-129">Let's now consider our output once the CNOT gate has acted on our input above.</span></span> <span data-ttu-id="ca422-130">Результат:</span><span class="sxs-lookup"><span data-stu-id="ca422-130">The result is:</span></span>

<span data-ttu-id="ca422-131">$${2}(фрак){000} альфа-кет (кет) и «фрак» (альфа){2}кврт{011} (кет) и «фрак»{2}(фрак){110} » кврт кет (кв. ) » кета »кета»{2}{101} (кета)</span><span class="sxs-lookup"><span data-stu-id="ca422-131">$$ \frac{\alpha}{\sqrt{2}}\ket{000} + \frac{\alpha}{\sqrt{2}}\ket{011} + \frac{\beta}{\sqrt{2}}\ket{110} + \frac{\beta}{\sqrt{2}}\ket{101} $$</span></span>

<span data-ttu-id="ca422-132">Следующим шагом для отправки __сообщения__ является применение ворот Хадамард к __кубиту сообщения__ (это первый кубит каждого термина).</span><span class="sxs-lookup"><span data-stu-id="ca422-132">The next step to send the __message__ is to apply a Hadamard gate to the __message__ qubit (that's the first qubit of each term).</span></span> 

<span data-ttu-id="ca422-133">Напомним, что ворота Хадамарда:</span><span class="sxs-lookup"><span data-stu-id="ca422-133">As a reminder, the Hadamard gate does the following:</span></span>

<span data-ttu-id="ca422-134">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ca422-134">Input</span></span> | <span data-ttu-id="ca422-135">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="ca422-135">Output</span></span>
---------------------------| ---------------------------------------------------------------
<span data-ttu-id="ca422-136">$'ket{0}$</span><span class="sxs-lookup"><span data-stu-id="ca422-136">$\ket{0}$</span></span>  | <span data-ttu-id="ca422-137">$'frac{1}(кета){2}{0} {1}</span><span class="sxs-lookup"><span data-stu-id="ca422-137">$\frac{1}{\sqrt{2}}(\ket{0} + \ket{1})$</span></span>
<span data-ttu-id="ca422-138">$'ket{1}$</span><span class="sxs-lookup"><span data-stu-id="ca422-138">$\ket{1}$</span></span>  | <span data-ttu-id="ca422-139">$'frac{1}(кет{2}{0} - кет)${1}</span><span class="sxs-lookup"><span data-stu-id="ca422-139">$\frac{1}{\sqrt{2}}(\ket{0} - \ket{1})$</span></span>

<span data-ttu-id="ca422-140">Если мы применяем ворота Хадамард апервый к первому кубиту каждого термина нашего вышеуказанного, мы получим следующий результат:</span><span class="sxs-lookup"><span data-stu-id="ca422-140">If we apply the Hadamard gate to the first qubit of each term of our output above, we get the following result:</span></span>

<span data-ttu-id="ca422-141">$$ (фрак) альфа-кврт{2}{1}(«фрак»{2}(кет) кет{0} и{1}кет)){00} {2}{1}{2}{0} {1}{11} frac(frac) - sqrt{2}("фрак"{1}{2}{0} (кет) кет{1}(кет){10} {2}{1}{2}{0} {1}{01}</span><span class="sxs-lookup"><span data-stu-id="ca422-141">$$ \frac{\alpha}{\sqrt{2}}(\frac{1}{\sqrt{2}}(\ket{0} + \ket{1}))\ket{00} + \frac{\alpha}{\sqrt{2}}(\frac{1}{\sqrt{2}}(\ket{0} + \ket{1}))\ket{11} + \frac{\beta}{\sqrt{2}}(\frac{1}{\sqrt{2}}(\ket{0} - \ket{1}))\ket{10} + \frac{\beta}{\sqrt{2}}(\frac{1}{\sqrt{2}}(\ket{0} - \ket{1}))\ket{01} $$</span></span>

<span data-ttu-id="ca422-142">Обратите внимание, что каждый{1}термин имеет{2}два фактора $ »frac »sqrt » $.</span><span class="sxs-lookup"><span data-stu-id="ca422-142">Note that each term has two $\frac{1}{\sqrt{2}}$ factors.</span></span> <span data-ttu-id="ca422-143">Мы можем умножить их, давая следующий результат:</span><span class="sxs-lookup"><span data-stu-id="ca422-143">We can multiply these out giving the following result:</span></span>

<span data-ttu-id="ca422-144">$${2}(фрак){0} (кет) (кет){1}(кет) кет{00} ( «фрак»-альфа»{2}(кет){0} »кет»{1}{11} {2}{0} {1}{10} {2}{0} {1}{01} (кет) »кет» (кет)</span><span class="sxs-lookup"><span data-stu-id="ca422-144">$$ \frac{\alpha}{2}(\ket{0} + \ket{1})\ket{00} + \frac{\alpha}{2}(\ket{0} + \ket{1})\ket{11} + \frac{\beta}{2}(\ket{0} - \ket{1})\ket{10} + \frac{\beta}{2}(\ket{0} - \ket{1})\ket{01} $$</span></span>

<span data-ttu-id="ca422-145">Коэффициент{1}{2}$ $ является общим для каждого термина, чтобы теперь мы могли взять его за пределы скобки:</span><span class="sxs-lookup"><span data-stu-id="ca422-145">The  $\frac{1}{2}$ factor is common to each term so we can now take it outside the brackets:</span></span>

<span data-ttu-id="ca422-146">$${1}{2}«фрак» (большой» альфа)» кет{0} {1}({00} кет) кет{0} » альфа{1}(кет){11} » кет »{0} » кет) »{10} кет » кет{0} »{1}{01}{1}кет »</span><span class="sxs-lookup"><span data-stu-id="ca422-146">$$ \frac{1}{2}\big[\alpha(\ket{0} + \ket{1})\ket{00} + \alpha(\ket{0} + \ket{1})\ket{11} + \beta(\ket{0} - \ket{1})\ket{10} + \beta(\ket{0} - \ket{1})\ket{01}\big] $$</span></span>

<span data-ttu-id="ca422-147">Затем мы можем умножить скобки для каждого термина дает:</span><span class="sxs-lookup"><span data-stu-id="ca422-147">We can then multiply out the brackets for each term giving:</span></span>

<span data-ttu-id="ca422-148">$${1}{2}«фрак» (большой){000} альфа-кет »{100} альфа-кет{011} , альфа-кет{111} , альфа-кет{010} , «альфа»кет » » бета-кет -{110} «бета-кет»{001} {101}</span><span class="sxs-lookup"><span data-stu-id="ca422-148">$$ \frac{1}{2}\big[\alpha\ket{000} + \alpha\ket{100} + \alpha\ket{011} + \alpha\ket{111} + \beta\ket{010} - \beta\ket{110} + \beta\ket{001} - \beta\ket{101}\big] $$</span></span>

### <a name="step-3-measure-the-result"></a><span data-ttu-id="ca422-149">Шаг 3: Измерьте результат</span><span class="sxs-lookup"><span data-stu-id="ca422-149">Step 3: Measure the result</span></span>

<span data-ttu-id="ca422-150">Из-за __здесь__ и __там__ запутался, любое измерение __здесь__ будет влиять на состояние __там__.</span><span class="sxs-lookup"><span data-stu-id="ca422-150">Due to __here__ and __there__ being entangled, any measurement on __here__ will affect the state of __there__.</span></span> <span data-ttu-id="ca422-151">Если мы измеряем первый и второй кубит __(сообщение__ и __здесь),__ мы можем узнать, в каком состоянии __находится,__ из-за этого свойства запутанности.</span><span class="sxs-lookup"><span data-stu-id="ca422-151">If we measure the first and second qubit (__message__ and __here__) we can learn what state __there__ is in, due to this property of entanglement.</span></span> 

* <span data-ttu-id="ca422-152">Если мы измеряем и получаем результат 00, суперпозиция рухнет, оставляя только сроки, соответствующие этому результату.</span><span class="sxs-lookup"><span data-stu-id="ca422-152">If we measure and get a result 00, the superposition collapses, leaving only terms consistent with this result.</span></span> <span data-ttu-id="ca422-153">Это{000} $'альфа-кет, бета-кет{001}$.</span><span class="sxs-lookup"><span data-stu-id="ca422-153">That's $\alpha\ket{000} +\beta\ket{001}$.</span></span> <span data-ttu-id="ca422-154">Это может быть рефакторинг до{00}$ кет{0} (альфа-кет{1}»бета-кет)$.</span><span class="sxs-lookup"><span data-stu-id="ca422-154">This can be refactored to $\ket{00}(\alpha\ket{0} +\beta\ket{1})$.</span></span> <span data-ttu-id="ca422-155">Поэтому, если мы измеряем первый и второй кубит, чтобы быть 00, мы знаем,{0} что третий кубит, __есть,__ находится в состоянии $(Альфа-кет »бета-кет)$.{1}</span><span class="sxs-lookup"><span data-stu-id="ca422-155">Therefore if we measure the first and second qubit to be 00, we know that the third qubit, __there__, is in the state $(\alpha\ket{0} +\beta\ket{1})$.</span></span>
* <span data-ttu-id="ca422-156">Если мы измеряем и получаем результат 01, суперпозиция рухнет, оставляя только сроки, соответствующие этому результату.</span><span class="sxs-lookup"><span data-stu-id="ca422-156">If we measure and get a result 01, the superposition collapses, leaving only terms consistent with this result.</span></span> <span data-ttu-id="ca422-157">Это{011} $'альфа-кет, бета-кет{010}$.</span><span class="sxs-lookup"><span data-stu-id="ca422-157">That's $\alpha\ket{011} +\beta\ket{010}$.</span></span> <span data-ttu-id="ca422-158">Это может быть рефакторинг до{01}$ кет{1} (альфа-кет{0}»бета-кет)$.</span><span class="sxs-lookup"><span data-stu-id="ca422-158">This can be refactored to $\ket{01}(\alpha\ket{1} +\beta\ket{0})$.</span></span> <span data-ttu-id="ca422-159">Поэтому, если мы измеряем первый и второй кубит, чтобы быть 01, мы знаем,{1} что третий кубит, __есть,__ находится в состоянии $(Альфа-кет »бета-кет)$.{0}</span><span class="sxs-lookup"><span data-stu-id="ca422-159">Therefore if we measure the first and second qubit to be 01, we know that the third qubit, __there__, is in the state $(\alpha\ket{1} +\beta\ket{0})$.</span></span>
* <span data-ttu-id="ca422-160">Если мы измеряем и получаем результат 10, суперпозиция рухнет, оставляя только сроки, соответствующие этому результату.</span><span class="sxs-lookup"><span data-stu-id="ca422-160">If we measure and get a result 10, the superposition collapses, leaving only terms consistent with this result.</span></span> <span data-ttu-id="ca422-161">Это $'альфа-кет{100} - бета-кет{101}$.</span><span class="sxs-lookup"><span data-stu-id="ca422-161">That's $\alpha\ket{100} -\beta\ket{101}$.</span></span> <span data-ttu-id="ca422-162">Это может быть рефакторинг до{10}$ кет{0} (альфа-кет{1}- бета-кет )$.</span><span class="sxs-lookup"><span data-stu-id="ca422-162">This can be refactored to $\ket{10}(\alpha\ket{0} -\beta\ket{1})$.</span></span> <span data-ttu-id="ca422-163">Поэтому, если мы измеряем первый и второй кубит, чтобы быть 10, мы знаем,{0} что третий кубит, __есть,__ находится в состоянии $(Альфа-кет - бета-кет{1})$.</span><span class="sxs-lookup"><span data-stu-id="ca422-163">Therefore if we measure the first and second qubit to be 10, we know that the third qubit, __there__, is in the state $(\alpha\ket{0} -\beta\ket{1})$.</span></span>
* <span data-ttu-id="ca422-164">Если мы измеряем и получаем результат 11, суперпозиция рухнет, оставляя только сроки, соответствующие этому результату.</span><span class="sxs-lookup"><span data-stu-id="ca422-164">If we measure and get a result 11, the superposition collapses, leaving only terms consistent with this result.</span></span> <span data-ttu-id="ca422-165">Это $'альфа-кет{111} - бета-кет{110}$.</span><span class="sxs-lookup"><span data-stu-id="ca422-165">That's $\alpha\ket{111} -\beta\ket{110}$.</span></span> <span data-ttu-id="ca422-166">Это может быть рефакторинг до{11}$ кет{1} (альфа-кет{0}- бета-кет )$.</span><span class="sxs-lookup"><span data-stu-id="ca422-166">This can be refactored to $\ket{11}(\alpha\ket{1} -\beta\ket{0})$.</span></span> <span data-ttu-id="ca422-167">Поэтому, если мы измеряем первый и второй кубит, чтобы быть 11, мы знаем,{1} что третий кубит, __есть,__ находится в состоянии $(Альфа-кет - бета-кет)$.{0}</span><span class="sxs-lookup"><span data-stu-id="ca422-167">Therefore if we measure the first and second qubit to be 11, we know that the third qubit, __there__, is in the state $(\alpha\ket{1} -\beta\ket{0})$.</span></span>

### <a name="step-4-interpret-the-result"></a><span data-ttu-id="ca422-168">Шаг 4: Интерпретировать результат</span><span class="sxs-lookup"><span data-stu-id="ca422-168">Step 4: Interpret the result</span></span>

<span data-ttu-id="ca422-169">Напомним, что первоначальное __сообщение,__ отправленное нам, было:</span><span class="sxs-lookup"><span data-stu-id="ca422-169">As a reminder, the original __message__ we wished to send was:</span></span>

<span data-ttu-id="ca422-170">$$ »кет»пси»{0} {1}</span><span class="sxs-lookup"><span data-stu-id="ca422-170">$$ \ket{\psi} = \alpha\ket{0} + \beta\ket{1} $$</span></span>

<span data-ttu-id="ca422-171">Мы должны получить __там__ кубит в этом состоянии, так что получил состояние является тот, который был предназначен.</span><span class="sxs-lookup"><span data-stu-id="ca422-171">We need to get the __there__ qubit into this state, so that the received state is the one that was intended.</span></span> 

* <span data-ttu-id="ca422-172">Если мы измерили и получили результат 00, то третий кубит, __там,__{0} находится в состоянии{1}$('альфа-кет»-бета-кет)$.</span><span class="sxs-lookup"><span data-stu-id="ca422-172">If we measured and got a result of 00, then the third qubit, __there__, is in the state $(\alpha\ket{0} +\beta\ket{1})$.</span></span> <span data-ttu-id="ca422-173">Поскольку это предполагаемое __сообщение,__ никаких изменений не требуется.</span><span class="sxs-lookup"><span data-stu-id="ca422-173">As this is the intended __message__, no alteration is required.</span></span>
* <span data-ttu-id="ca422-174">Если мы измерили и получили результат 01, то третий кубит, __там,__{1} находится в состоянии{0}$(»альфа-кет»-бета-кет)$.</span><span class="sxs-lookup"><span data-stu-id="ca422-174">If we measured and got a result of 01, then the third qubit, __there__, is in the state $(\alpha\ket{1} +\beta\ket{0})$.</span></span> <span data-ttu-id="ca422-175">Это отличается от предполагаемого __сообщения__, однако применение НЕ ворота дает нам{0} желаемое состояние{1}$(Альфа-кет »бета-кет)$.</span><span class="sxs-lookup"><span data-stu-id="ca422-175">This differs from the intended __message__, however applying a NOT gate gives us the desired state $(\alpha\ket{0} +\beta\ket{1})$.</span></span>
* <span data-ttu-id="ca422-176">Если мы измерили и получили результат 10, то третий кубит, __там,__{0} находится в состоянии{1}$('альфа-кет -'beta'ket)$.</span><span class="sxs-lookup"><span data-stu-id="ca422-176">If we measured and got a result of 10, then the third qubit, __there__, is in the state $(\alpha\ket{0} -\beta\ket{1})$.</span></span> <span data-ttu-id="ca422-177">Это отличается от предполагаемого __сообщения__, однако применение врата дает нам{0} желаемое состояние{1}$(«альфа-кет» («бета-кет»)$.</span><span class="sxs-lookup"><span data-stu-id="ca422-177">This differs from the intended __message__, however applying a Z gate gives us the desired state $(\alpha\ket{0} +\beta\ket{1})$.</span></span>
* <span data-ttu-id="ca422-178">Если мы измерили и получили результат 11, то третий кубит, __там,__{1} находится в состоянии{0}$('альфа-кет -'beta'ket)$.</span><span class="sxs-lookup"><span data-stu-id="ca422-178">If we measured and got a result of 11, then the third qubit, __there__, is in the state $(\alpha\ket{1} -\beta\ket{0})$.</span></span> <span data-ttu-id="ca422-179">Это отличается от предполагаемого __сообщения__, однако применение не ворота следуют ворота, а затем{0} ворота дает нам{1}желаемое состояние $ (альфа-кет »бета-кет)$.</span><span class="sxs-lookup"><span data-stu-id="ca422-179">This differs from the intended __message__, however applying a NOT gate followed by a Z gate gives us the desired state $(\alpha\ket{0} +\beta\ket{1})$.</span></span>

<span data-ttu-id="ca422-180">Подводя итог, если мы измеряем и первый кубит составляет 1, применяется ворота .</span><span class="sxs-lookup"><span data-stu-id="ca422-180">To summarize, if we measure and the first qubit is 1, a Z gate is applied.</span></span> <span data-ttu-id="ca422-181">Если мы измеряем и второй кубит 1, не применяются ворота НЕ.</span><span class="sxs-lookup"><span data-stu-id="ca422-181">If we measure and the second qubit is 1, a NOT gate is applied.</span></span>

### <a name="summary"></a><span data-ttu-id="ca422-182">Сводка</span><span class="sxs-lookup"><span data-stu-id="ca422-182">Summary</span></span>
<span data-ttu-id="ca422-183">Ниже показана квантовая квантовая схема с текстом книги, которая реализует телепортацию.</span><span class="sxs-lookup"><span data-stu-id="ca422-183">Shown below is a text-book quantum circuit that implements the teleportation.</span></span> <span data-ttu-id="ca422-184">Перемещение слева направо вы можете увидеть:</span><span class="sxs-lookup"><span data-stu-id="ca422-184">Moving from left to right you can see:</span></span>
- <span data-ttu-id="ca422-185">Шаг 1: Запутывание __здесь__ и __там,__ применяя ворота Хадамард и ворота CNOT.</span><span class="sxs-lookup"><span data-stu-id="ca422-185">Step 1: Entangling __here__ and __there__ by applying a Hadamard gate and CNOT gate.</span></span>
- <span data-ttu-id="ca422-186">Шаг 2: Отправка __сообщения__ с помощью ворот CNOT и ворот Хадамарда.</span><span class="sxs-lookup"><span data-stu-id="ca422-186">Step 2: Sending the __message__ using a CNOT gate and a Hadamard gate.</span></span>
- <span data-ttu-id="ca422-187">Шаг 3: Принимая измерения первого и второго кубитов, __сообщение__ и __здесь__.</span><span class="sxs-lookup"><span data-stu-id="ca422-187">Step 3: Taking a measurement of the first and second qubits, __message__ and __here__.</span></span>
- <span data-ttu-id="ca422-188">Шаг 4: Применение НЕ-ворота или ворота, в зависимости от результата измерения в шаге 3.</span><span class="sxs-lookup"><span data-stu-id="ca422-188">Step 4: Applying a NOT gate or a Z gate, depending on the result of the measurement in step 3.</span></span>

!['Телепорт (msg : Кубит, там : Зубит) : Единица'](~/media/teleportation.svg)

## <a name="quantum-teleportation-code"></a><span data-ttu-id="ca422-190">Квантовая телепортация: Код</span><span class="sxs-lookup"><span data-stu-id="ca422-190">Quantum Teleportation: Code</span></span>

<span data-ttu-id="ca422-191">У нас есть наша схема для квантовой телепортации:</span><span class="sxs-lookup"><span data-stu-id="ca422-191">We have our circuit for quantum teleportation:</span></span>

!['Телепорт (msg : Кубит, там : Зубит) : Единица'](~/media/teleportation.svg)

<span data-ttu-id="ca422-193">Теперь мы можем перевести каждый из шагов в этой квантовой цепи в квантовую схему в квантовую схему.</span><span class="sxs-lookup"><span data-stu-id="ca422-193">We can now translate each of the steps in this quantum circuit into Q#.</span></span>

### <a name="step-0-definition"></a><span data-ttu-id="ca422-194">Шаг 0: Определение</span><span class="sxs-lookup"><span data-stu-id="ca422-194">Step 0: Definition</span></span>
<span data-ttu-id="ca422-195">Когда мы выполняем телепортацию, мы должны знать __сообщение,__ что мы хотим отправить, и где мы хотим отправить его __(там__).</span><span class="sxs-lookup"><span data-stu-id="ca422-195">When we perform teleportation, we must know the __message__ we wish to send, and where we wish to send it (__there__).</span></span> <span data-ttu-id="ca422-196">По этой причине мы начинаем с определения новой операции Телепорт, которая `msg` `there`дается два кубитов в качестве аргументов, и:</span><span class="sxs-lookup"><span data-stu-id="ca422-196">For this reason, we begin by defining a new Teleport operation that is given two qubits as arguments, `msg` and `there`:</span></span>

```qsharp
operation Teleport(msg : Qubit, there : Qubit) : Unit {
```

<span data-ttu-id="ca422-197">Нам также необходимо выделить `here` кубит, который `using` мы достигаем с блоком:</span><span class="sxs-lookup"><span data-stu-id="ca422-197">We also need to allocate a qubit `here` which we achieve with a `using` block:</span></span>

```qsharp
    using (here = Qubit()) {
```

### <a name="step-1-create-an-entangled-state"></a><span data-ttu-id="ca422-198">Шаг 1: Создать запутавное состояние</span><span class="sxs-lookup"><span data-stu-id="ca422-198">Step 1: Create an entangled state</span></span>
<span data-ttu-id="ca422-199">Затем мы можем создать запутанную `here` пару между и `there` с помощью @"microsoft.quantum.intrinsic.h" @"microsoft.quantum.intrinsic.cnot" операций:</span><span class="sxs-lookup"><span data-stu-id="ca422-199">We can then create the entangled pair between `here` and `there` by using the @"microsoft.quantum.intrinsic.h" and @"microsoft.quantum.intrinsic.cnot" operations:</span></span>

```qsharp
        H(here);
        CNOT(here, there);
```

### <a name="step-2-send-the-message"></a><span data-ttu-id="ca422-200">Шаг 2: Отправить сообщение</span><span class="sxs-lookup"><span data-stu-id="ca422-200">Step 2: Send the message</span></span>
<span data-ttu-id="ca422-201">Затем мы используем следующий $ операторимя »CNOT» $ и $H $ ворота для перемещения нашего сообщения qubit:</span><span class="sxs-lookup"><span data-stu-id="ca422-201">We then use the next $\operatorname{CNOT}$ and $H$ gates to move our message qubit:</span></span>

```qsharp
        CNOT(msg, here);
        H(msg);
```

### <a name="step-3--4-measuring-and-interpreting-the-result"></a><span data-ttu-id="ca422-202">Шаг 3 & 4: Измерение и интерпретация результата</span><span class="sxs-lookup"><span data-stu-id="ca422-202">Step 3 & 4: Measuring and interpreting the result</span></span>
<span data-ttu-id="ca422-203">Наконец, @"microsoft.quantum.intrinsic.m" мы используем для выполнения измерений и выполнения необходимых операций `if` ворот, чтобы получить желаемое состояние, как обозначается операторами:</span><span class="sxs-lookup"><span data-stu-id="ca422-203">Finally, we use @"microsoft.quantum.intrinsic.m" to perform the measurements and perform the necessary gate operations to get the desired state, as denoted by `if` statements:</span></span>

```qsharp
        // Measure out the entanglement
        if (M(msg) == One)  { Z(there); }
        if (M(here) == One) { X(there); }
```

### <a name="step-5-restarting-the-qubit-register"></a><span data-ttu-id="ca422-204">Шаг 5: Перезапуск регистра кубита</span><span class="sxs-lookup"><span data-stu-id="ca422-204">Step 5: Restarting the qubit register</span></span>

<span data-ttu-id="ca422-205">В конце каждой операции мы должны позволить кубитов в состоянии $ кет{0}.</span><span class="sxs-lookup"><span data-stu-id="ca422-205">At the end of every Q# operation we need to let the qubits in the state $\ket{0}$.</span></span> <span data-ttu-id="ca422-206">Мы можем @"microsoft.quantum.intrinsic.reset" использовать для перезапуска всех кубитов до нулевого состояния, и это завершит нашу работу.</span><span class="sxs-lookup"><span data-stu-id="ca422-206">We can use @"microsoft.quantum.intrinsic.reset" to restart all the qubits to the zero state and this will finish our operation.</span></span>

```qsharp
        Reset(msg);
        Reset(here);
        Reset(there);
    }
}
```


