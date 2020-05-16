---
title: Квантовые схемы
description: Узнайте, как визуально представить простые и сложные тактовые операции с помощью схем тактов.
author: QuantumWriter
uid: microsoft.quantum.concepts.circuits
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 43f14d67db76dabda34bf881ccbfae0bfd1784ff
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2020
ms.locfileid: "83426614"
---
# <a name="quantum-circuits"></a><span data-ttu-id="a4c45-103">Тактовые цепи</span><span class="sxs-lookup"><span data-stu-id="a4c45-103">Quantum Circuits</span></span>
<span data-ttu-id="a4c45-104">Рассмотрим в течение некоторого времени единое преобразование $ \текст{кнот} _ {01} (х\отимес 1) $.</span><span class="sxs-lookup"><span data-stu-id="a4c45-104">Consider for a moment the unitary transformation $\text{ CNOT}_{01}(H\otimes 1)$.</span></span>
<span data-ttu-id="a4c45-105">Эта последовательность является фундаментальной важностью для вычислений на основе тактовой задержки, так как она создает максимально запутанныминое состояние из двух кубит:</span><span class="sxs-lookup"><span data-stu-id="a4c45-105">This gate sequence is of fundamental significance to quantum computing because it creates a maximally entangled two-qubit state:</span></span>

<span data-ttu-id="a4c45-106">$ $ \mathrm{CNOT}_ {01} (х\отимес 1) \кет {00} = \фрак {1} {\скрт {2} } \лефт (\кет {00} + \кет {11} \ригхт), $ $</span><span class="sxs-lookup"><span data-stu-id="a4c45-106">$$\mathrm{CNOT}_{01}(H\otimes 1)\ket{00} = \frac{1}{\sqrt{2}} \left(\ket{00} + \ket{11} \right),$$</span></span>

<span data-ttu-id="a4c45-107">Операции с такой или большей сложностью являются повсеместными в алгоритмах тактовой задержки и коррекции ошибок такта, поэтому они должны быть очень простыми методами визуализации, называемыми *схемой*последовательностей.</span><span class="sxs-lookup"><span data-stu-id="a4c45-107">Operations with this or greater complexity are ubiquitous in quantum algorithms and quantum error correction, so it should come as a great relief that there is a simple method for their visualization called a *quantum circuit diagram*.</span></span>
<span data-ttu-id="a4c45-108">Схема канала для подготовки этого максимального запутанными состояния такта:</span><span class="sxs-lookup"><span data-stu-id="a4c45-108">The circuit diagram for preparing this maximally entangled quantum state is:</span></span>

<!--- ![](.\media\1.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
<span data-ttu-id="a4c45-109">![Схема цепи для максимального запутанными состояния кубит](~/media/1.svg)</span><span class="sxs-lookup"><span data-stu-id="a4c45-109">![Circuit diagram for a maximally entangled two-qubit state](~/media/1.svg)</span></span>

## <a name="quantum-circuit-diagram-conventions"></a><span data-ttu-id="a4c45-110">Обозначения схемы тактовой цепи</span><span class="sxs-lookup"><span data-stu-id="a4c45-110">Quantum circuit diagram conventions</span></span>
<span data-ttu-id="a4c45-111">Этот визуальный язык для операций над тактовыми операциями может быть более легко удобную, чем написание эквивалентной матрицы после того, как вы понимаете соглашения для выражения тактовой цепи.</span><span class="sxs-lookup"><span data-stu-id="a4c45-111">This visual language for quantum operations can be more readily digestible than writing down its equivalent matrix once you understand the conventions for expressing a quantum circuit.</span></span>
<span data-ttu-id="a4c45-112">Мы рассмотрим эти соглашения ниже.</span><span class="sxs-lookup"><span data-stu-id="a4c45-112">We review these conventions below.</span></span>

<span data-ttu-id="a4c45-113">В схеме цепи каждая сплошная линия изображает кубит или более, как правило, кубит регистр.</span><span class="sxs-lookup"><span data-stu-id="a4c45-113">In a circuit diagram, each solid line depicts a qubit or more generally a qubit register.</span></span>
<span data-ttu-id="a4c45-114">По соглашению в верхней строке используется кубит Register $0 $, а остаток помечается последовательно.</span><span class="sxs-lookup"><span data-stu-id="a4c45-114">By convention, the top line is qubit register $0$ and the remainder are labeled sequentially.</span></span> <span data-ttu-id="a4c45-115">Приведенный выше канал примера показан как работа с двумя Кубитс (или аналогично двумя регистрами, состоящими из одного кубит).</span><span class="sxs-lookup"><span data-stu-id="a4c45-115">The above example circuit is depicted as acting on two qubits (or equivalently two registers consisting of one qubit).</span></span>
<span data-ttu-id="a4c45-116">Шлюзы, действующие на один или несколько регистров кубит, обозначаются как Box.</span><span class="sxs-lookup"><span data-stu-id="a4c45-116">Gates acting on one or more qubit registers are denoted as a box.</span></span>
<span data-ttu-id="a4c45-117">Например, символ</span><span class="sxs-lookup"><span data-stu-id="a4c45-117">For example, the symbol</span></span>

<!--- ![](.\media\2.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
<span data-ttu-id="a4c45-118">![Символ для операции Хадамард, действующей на одном кубит регистре](~/media/2.svg)</span><span class="sxs-lookup"><span data-stu-id="a4c45-118">![Symbol for a Hadamard operation acting on a single-qubit register](~/media/2.svg)</span></span>

<span data-ttu-id="a4c45-119">— Это операция [хадамард](xref:microsoft.quantum.intrinsic.h) , действующая на кубит регистр.</span><span class="sxs-lookup"><span data-stu-id="a4c45-119">is a [Hadamard](xref:microsoft.quantum.intrinsic.h) operation acting on a single-qubit register.</span></span>

<span data-ttu-id="a4c45-120">Тактовые шлюзы упорядочиваются в хронологическом порядке с самым левым шлюзом, так как шлюз сначала применяется к Кубитс.</span><span class="sxs-lookup"><span data-stu-id="a4c45-120">Quantum gates are ordered in chronological order with the left-most gate as the gate first applied to the qubits.</span></span>
<span data-ttu-id="a4c45-121">Иными словами, если вы просматриваете провода как состояние такта, провода поместит состояние такта через каждый из шлюзов на схеме слева направо.</span><span class="sxs-lookup"><span data-stu-id="a4c45-121">In other words, if you picture the wires as holding the quantum state, the wires bring the quantum state through each of the gates in the diagram from left to right.</span></span>
<span data-ttu-id="a4c45-122">Это можно сказать</span><span class="sxs-lookup"><span data-stu-id="a4c45-122">That is to say</span></span> 

<!--- ![](.\media\3.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
<span data-ttu-id="a4c45-123">![Схема применяемых тактовых шлюзов слева направо](~/media/3.svg)</span><span class="sxs-lookup"><span data-stu-id="a4c45-123">![Diagram of quantum gates being applied left-to-right](~/media/3.svg)</span></span>

<span data-ttu-id="a4c45-124">является единой матрицей $CBA $.</span><span class="sxs-lookup"><span data-stu-id="a4c45-124">is the unitary matrix $CBA$.</span></span>
<span data-ttu-id="a4c45-125">Умножение матрицы подчиняется соглашению о противоположности: сначала применяется самая правая матрица.</span><span class="sxs-lookup"><span data-stu-id="a4c45-125">Matrix multiplication obeys the opposite convention: the right-most matrix is applied first.</span></span> <span data-ttu-id="a4c45-126">Однако в схемах тактовой цепи сначала применяется самый левый шлюз.</span><span class="sxs-lookup"><span data-stu-id="a4c45-126">In quantum circuit diagrams, however, the left-most gate is applied first.</span></span>
<span data-ttu-id="a4c45-127">Это различие может иногда привести к путанице, поэтому важно отметить это существенное различие между линейной алгебраические нотации и схемами тактовой цепи.</span><span class="sxs-lookup"><span data-stu-id="a4c45-127">This difference can at times lead to confusion, so it is important to note this significant difference between the linear algebraic notation and quantum circuit diagrams.</span></span>

## <a name="inputs-and-outputs-of-quantum-circuits"></a><span data-ttu-id="a4c45-128">Входы и выходы каналов тактов</span><span class="sxs-lookup"><span data-stu-id="a4c45-128">Inputs and outputs of quantum circuits</span></span>
<span data-ttu-id="a4c45-129">Все приведенные выше примеры имеют точно такое же число проводов (Кубитс), что и для шлюза такта, как количество проводов.</span><span class="sxs-lookup"><span data-stu-id="a4c45-129">All previous examples given have had precisely the same number of wires (qubits) input to a quantum gate as the number of wires out from the quantum gate.</span></span>
<span data-ttu-id="a4c45-130">Это может показаться вполне разумным, что тактовые каналы могут иметь больше или меньше выходных данных, чем в общем.</span><span class="sxs-lookup"><span data-stu-id="a4c45-130">It may at first seem reasonable that quantum circuits could have more, or fewer, outputs than inputs in general.</span></span>
<span data-ttu-id="a4c45-131">Однако это невозможно, так как все операции над тактами, сохранение измерения являются едиными и, следовательно, обратимыми.</span><span class="sxs-lookup"><span data-stu-id="a4c45-131">This is impossible, however, because all quantum operations, save measurement, are unitary and hence reversible.</span></span>
<span data-ttu-id="a4c45-132">Если у них не было одинакового количества выходов в качестве входных данных, они не были бы обратимыми и, следовательно, не являются едиными, то есть противоречит.</span><span class="sxs-lookup"><span data-stu-id="a4c45-132">If they did not have the same number of outputs as inputs they would not be reversible and hence not unitary, which is a contradiction.</span></span>
<span data-ttu-id="a4c45-133">По этой причине любой прямоугольник, нарисованный на схеме цепи, должен иметь точно такое же количество проводов, что и при его выходе.</span><span class="sxs-lookup"><span data-stu-id="a4c45-133">For this reason any box drawn in a circuit diagram must have precisely the same number of wires entering it as exiting it.</span></span>

<span data-ttu-id="a4c45-134">Схемы многокубитной цепи соответствуют аналогичным соглашениям с одним кубит.</span><span class="sxs-lookup"><span data-stu-id="a4c45-134">Multi-qubit circuit diagrams follow similar conventions to single-qubit ones.</span></span>
<span data-ttu-id="a4c45-135">В качестве уточненного примера мы можем определить кубит единую операцию, $B $ в $ (H С\отимес X) $ и выразить цепь эквивалентно, как</span><span class="sxs-lookup"><span data-stu-id="a4c45-135">As a clarifying example, we can define a two-qubit unitary operation $B$ to be $(H S\otimes X)$ and express the circuit equivalently as</span></span>

<!--- ![](.\media\4.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
<span data-ttu-id="a4c45-136">![Схема цепи кубит операции](~/media/4.svg)</span><span class="sxs-lookup"><span data-stu-id="a4c45-136">![Circuit diagram of a two-qubit unitary operation](~/media/4.svg)</span></span>

<span data-ttu-id="a4c45-137">Можно также просмотреть $B $ как наличие действия с одним кубит регистром, а не 2 1-кубит регистров в зависимости от контекста, в котором используется канал.</span><span class="sxs-lookup"><span data-stu-id="a4c45-137">We can also view $B$ as having an action on a single two-qubit register rather than two one-qubit registers depending on the context in which the circuit is used.</span></span> <span data-ttu-id="a4c45-138">Возможно, наиболее полезным свойством таких схем абстрактного канала является то, что они позволяют описывать сложные алгоритмы такта на высоком уровне без необходимости их компиляции в фундаментальные шлюзы.</span><span class="sxs-lookup"><span data-stu-id="a4c45-138">Perhaps the most useful property of such abstract circuit diagrams is that they allow complicated quantum algorithms to be described at a high level without having to compile them down to fundamental gates.</span></span>
<span data-ttu-id="a4c45-139">Это означает, что вы можете получить интуиция о потоке данных для большого тактового алгоритма, не требуя понимания всех сведений о том, как работает каждая из подпрограмм в алгоритме.</span><span class="sxs-lookup"><span data-stu-id="a4c45-139">This means that you can get an intuition about the data flow for a large quantum algorithm without needing to understand all the details of how each of the subroutines within the algorithm work.</span></span>

## <a name="controlled-gates"></a><span data-ttu-id="a4c45-140">Контролируемые шлюзы</span><span class="sxs-lookup"><span data-stu-id="a4c45-140">Controlled gates</span></span>
<span data-ttu-id="a4c45-141">Другая конструкция, встроенная в диаграммы с несколькими кубит тактовыми каналами, — это управление.</span><span class="sxs-lookup"><span data-stu-id="a4c45-141">The other construct that is built into multi-qubit quantum circuit diagrams is control.</span></span>
<span data-ttu-id="a4c45-142">Действие одномерного управляемого генератора, обозначенное как $ \Ламбда (G) $, где значение одного кубита управляет применением $G $, может быть понято в следующем примере входного состояния продукта $ \Ламбда (G) (\алфа \кет {0} + \бета \кет {1} ) \кет{\пси} = \алфа \кет {0} \кет{\пси} + \бета \кет {1} G\ket {\ PSI} $.</span><span class="sxs-lookup"><span data-stu-id="a4c45-142">The action of a quantum singly controlled gate, denoted $\Lambda(G)$, where a single qubit's value controls the application of $G$, can be understood by looking at the following example of a product state input $\Lambda(G) (\alpha \ket{0} + \beta \ket{1}) \ket{\psi} = \alpha \ket{0} \ket{\psi} + \beta \ket{1} G\ket{\psi}$.</span></span>
<span data-ttu-id="a4c45-143">Например, управляемый шлюз применяет $G $ к регистру, содержащему $ \пси $ if, и только в том случае, если кубит элемента управления принимает значение $1 $.</span><span class="sxs-lookup"><span data-stu-id="a4c45-143">That is to say, the controlled gate applies $G$ to the register containing $\psi$ if and only if the control qubit takes the value $1$.</span></span>
<span data-ttu-id="a4c45-144">Как правило, в схемах каналов описаны такие контролируемые операции, как</span><span class="sxs-lookup"><span data-stu-id="a4c45-144">In general, we describe such controlled operations in circuit diagrams as</span></span>

<!--- ![](.\media\5.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
<span data-ttu-id="a4c45-145">![Схема цепи с однонаправленным управлением шлюзом](~/media/5.svg)</span><span class="sxs-lookup"><span data-stu-id="a4c45-145">![Circuit diagram of a singly controlled gate](~/media/5.svg)</span></span>

<span data-ttu-id="a4c45-146">Здесь черный круг обозначает тактовый бит, на котором управляется шлюз, и вертикальная линия обозначает единую линию, которая применяется, когда элемент управления кубит принимает значение $1 $.</span><span class="sxs-lookup"><span data-stu-id="a4c45-146">Here the black circle denotes the quantum bit on which the gate is controlled and a vertical wire denotes the unitary that is applied when the control qubit takes the value $1$.</span></span>
<span data-ttu-id="a4c45-147">В особых случаях, где $G = X $ и $G = Z $, мы представляем следующую нотацию для описания управляемой версии шлюзов (Обратите внимание, что шлюз управляемого X является [$CNOTным шлюзом](xref:microsoft.quantum.intrinsic.cnot)):</span><span class="sxs-lookup"><span data-stu-id="a4c45-147">For the special cases where $G=X$ and $G=Z$ we introduce the following notation to describe the controlled version of the gates (note that the controlled-X gate is the [$CNOT$ gate](xref:microsoft.quantum.intrinsic.cnot)):</span></span>

<!--- ![](.\media\6.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
<span data-ttu-id="a4c45-148">![Схема цепи для особых случаев управляемых шлюзов](~/media/6.svg)</span><span class="sxs-lookup"><span data-stu-id="a4c45-148">![Circuit diagram for special cases of controlled gates](~/media/6.svg)</span></span>

<span data-ttu-id="a4c45-149">Q # предоставляет методы для автоматического создания управляемой версии операции, которая позволяет программисту вручную выполнять код этих операций.</span><span class="sxs-lookup"><span data-stu-id="a4c45-149">Q# provides methods to automatically generate the controlled version of an operation, which saves the programmer from having to hand code these operations.</span></span> <span data-ttu-id="a4c45-150">Ниже приведен пример.</span><span class="sxs-lookup"><span data-stu-id="a4c45-150">An example of this is shown below:</span></span>

```qsharp
operation PrepareSuperposition(qubit : Qubit) : Unit
is Ctl { // Auto-generate the controlled specialization of the operation
    H(qubit);
}
```

## <a name="measurement-operator"></a><span data-ttu-id="a4c45-151">Оператор измерения</span><span class="sxs-lookup"><span data-stu-id="a4c45-151">Measurement operator</span></span>
<span data-ttu-id="a4c45-152">Оставшаяся операция визуализации на схемах схемы — это измерение.</span><span class="sxs-lookup"><span data-stu-id="a4c45-152">The remaining operation to visualize in circuit diagrams is measurement.</span></span>
<span data-ttu-id="a4c45-153">Измерение принимает кубит регистр, измеряет его и выводит результат в виде классической информации.</span><span class="sxs-lookup"><span data-stu-id="a4c45-153">Measurement takes a qubit register, measures it, and outputs the result as classical information.</span></span>
<span data-ttu-id="a4c45-154">Операция измерения обозначается символом измерения и всегда принимает в качестве входных данных кубит регистр (обозначенный сплошной линией) и выводит классическую информацию (обозначенную двойной линией).</span><span class="sxs-lookup"><span data-stu-id="a4c45-154">A measurement operation is denoted by a meter symbol and always takes as input a qubit register (denoted by a solid line) and outputs classical information (denoted by a double line).</span></span>
<span data-ttu-id="a4c45-155">В частности, такая подсхема выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a4c45-155">Specifically, such a subcircuit looks like:</span></span>

<!--- ![](.\media\7.svg) ---->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
<span data-ttu-id="a4c45-156">![Символ, представляющий операцию измерения](~/media/7.svg)</span><span class="sxs-lookup"><span data-stu-id="a4c45-156">![Symbol representing a measurement operation](~/media/7.svg)</span></span>

<span data-ttu-id="a4c45-157">Q # реализует [оператор Measure](xref:microsoft.quantum.intrinsic.measure) для этой цели.</span><span class="sxs-lookup"><span data-stu-id="a4c45-157">Q# implements a [Measure operator](xref:microsoft.quantum.intrinsic.measure) for this purpose.</span></span>
<span data-ttu-id="a4c45-158">Дополнительные сведения см. в [разделе об измерениях](xref:microsoft.quantum.libraries.standard.prelude#measurements) .</span><span class="sxs-lookup"><span data-stu-id="a4c45-158">See the [section on measurements](xref:microsoft.quantum.libraries.standard.prelude#measurements) for more information.</span></span>

<span data-ttu-id="a4c45-159">Аналогично, подканал</span><span class="sxs-lookup"><span data-stu-id="a4c45-159">Similarly, the subcircuit</span></span>

<!--- ![](.\media\8.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
<span data-ttu-id="a4c45-160">![Схема цепи, представляющая управляемую операцию](~/media/8.svg)</span><span class="sxs-lookup"><span data-stu-id="a4c45-160">![Circuit diagram representing a controlled operation](~/media/8.svg)</span></span>

<span data-ttu-id="a4c45-161">предоставляет классический контролируемый шлюз, где $G $ применяется к классическому контрольному биту Value $1 $.</span><span class="sxs-lookup"><span data-stu-id="a4c45-161">gives a classically controlled gate, where $G$ is applied conditioned on the classical control bit being value $1$.</span></span>

## <a name="teleportation-circuit-diagram"></a><span data-ttu-id="a4c45-162">Схема цепи для переноса</span><span class="sxs-lookup"><span data-stu-id="a4c45-162">Teleportation circuit diagram</span></span>
<span data-ttu-id="a4c45-163">Для иллюстрации этих компонентов, возможно, это лучший алгоритм в тактовой заходе.</span><span class="sxs-lookup"><span data-stu-id="a4c45-163">Quantum teleportation is perhaps the best quantum algorithm for illustrating these components.</span></span>
<span data-ttu-id="a4c45-164">Вы можете ознакомиться с практическими сведениями о том, как [Перенаката](xref:microsoft.quantum.overview.katas) тактовый генератор тактов тактовой задержки — это способ перемещения данных на тактовый компьютер (или даже между удаленными тактовыми компьютерами в тактовой сети) с помощью замкнутые и измерения.</span><span class="sxs-lookup"><span data-stu-id="a4c45-164">You can learn hands-on with the corresponding [Quantum Kata](xref:microsoft.quantum.overview.katas) Quantum teleportation is a method for moving data within a quantum computer (or even between distant quantum computers in a quantum network) through the use of entanglement and measurement.</span></span>
<span data-ttu-id="a4c45-165">Интересно, что он действительно способен переместить состояние такта, скажем, значение в заданном кубит, от одного кубит к другому, не зная, что значение кубит.</span><span class="sxs-lookup"><span data-stu-id="a4c45-165">Interestingly, it is actually capable of moving a quantum state, say the value in a given qubit, from one qubit to another, without even knowing what the qubit's value is!</span></span>
<span data-ttu-id="a4c45-166">Это необходимо, чтобы протокол работал в соответствии с законами тактовой механики.</span><span class="sxs-lookup"><span data-stu-id="a4c45-166">This is necessary for the protocol to work according to the laws of quantum mechanics.</span></span>
<span data-ttu-id="a4c45-167">Канал передачи данных о тактовой линии приведен ниже; Кроме того, мы предоставляем версию канала с заметками, чтобы продемонстрировать, как читать тактовую цепь.</span><span class="sxs-lookup"><span data-stu-id="a4c45-167">The quantum teleportation circuit is given below; we also provide an annotated version of the circuit to illustrate how to read the quantum circuit.</span></span>

<!--- ![](.\media\tp2.svg){ width=50% } --->
<span data-ttu-id="a4c45-168">![Канал потактовой передачи](~/media/tp2.svg)</span><span class="sxs-lookup"><span data-stu-id="a4c45-168">![Quantum teleportation circuit](~/media/tp2.svg)</span></span>
