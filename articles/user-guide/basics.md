---
title: Q#Основы
description: Основные понятияQ#
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 02/28/2020
ms.topic: article
uid: microsoft.quantum.guide.basics
no-loc:
- Q#
- $$v
ms.openlocfilehash: 4f4a75cdaaa070fd763d7f75429b7c39357d25a5
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869653"
---
# <a name="no-locq-basics"></a><span data-ttu-id="86012-103">Q#Основы</span><span class="sxs-lookup"><span data-stu-id="86012-103">Q# Basics</span></span>

<span data-ttu-id="86012-104">Эта статья содержит краткое введение в основные стандартные блоки Q# .</span><span class="sxs-lookup"><span data-stu-id="86012-104">This article presents a brief introduction to the basic building blocks of Q#.</span></span>

<span data-ttu-id="86012-105">Общие сведения о том, что такое Q# и где оно подходит в качестве фундаментального компонента пакета средств разработки тактов, см. в разделе [что такое Q# ?](xref:microsoft.quantum.overview.q-sharp).</span><span class="sxs-lookup"><span data-stu-id="86012-105">For an overview of what Q# is and where it fits in as a fundamental component of the Quantum Development Kit, see [What is Q#?](xref:microsoft.quantum.overview.q-sharp).</span></span> 

## <a name="what-is-a-quantum-program"></a><span data-ttu-id="86012-106">Что такое тактовая программа?</span><span class="sxs-lookup"><span data-stu-id="86012-106">What is a quantum program?</span></span>

<span data-ttu-id="86012-107">С технической точки зрения, тактовая программа — это определенный набор классических подпрограмм, которые при вызове выполняют определенные операции в тактовой системе.</span><span class="sxs-lookup"><span data-stu-id="86012-107">From a technical perspective, a quantum program is a particular set of classical subroutines which, when called, perform certain operations on a quantum system.</span></span>
<span data-ttu-id="86012-108">Важным следствием этого представления является то, что Q# Программа напрямую не моделирует Кубитс самостоятельно, а описывает, как классический управляемый компьютер взаимодействует с этими Кубитс.</span><span class="sxs-lookup"><span data-stu-id="86012-108">An important consequence of that view is that a Q# program does not directly model qubits themselves, but rather describes how a classically controlled computer interacts with those qubits.</span></span>
<span data-ttu-id="86012-109">По проекту не Q# определяет состояния тактов или другие свойства генератора тактов напрямую.</span><span class="sxs-lookup"><span data-stu-id="86012-109">By design, Q# does not define quantum states or other properties of quantum mechanics directly.</span></span>
<span data-ttu-id="86012-110">Например, рассмотрим состояние $ \кет{+} = \лефт (\кет {0} + \кет {1} \ригхт)/\скрт {2} $, обсуждаемое в этом [Quantum Computing Concepts](xref:microsoft.quantum.concepts.intro) руководством.</span><span class="sxs-lookup"><span data-stu-id="86012-110">For instance, consider the state $\ket{+} = \left(\ket{0} + \ket{1}\right) / \sqrt{2}$ discussed in the [Quantum Computing Concepts](xref:microsoft.quantum.concepts.intro) guide.</span></span>
<span data-ttu-id="86012-111">Чтобы подготовить это состояние в Q# , начните с факта инициализации Кубитс в состоянии $ \кет {0} $, а также в том, что $ \кет{+} = х\кет {0} $, где $H $ — это [Преобразование хадамард](xref:microsoft.quantum.glossary#hadamard), реализованное [ `H` операцией](xref:microsoft.quantum.intrinsic.h).</span><span class="sxs-lookup"><span data-stu-id="86012-111">To prepare this state in Q#, start with the facts that the qubits are initialized in the $\ket{0}$ state, and that $\ket{+} = H\ket{0}$, where $H$ is the [Hadamard transform](xref:microsoft.quantum.glossary#hadamard), implemented by the [`H` operation](xref:microsoft.quantum.intrinsic.h).</span></span> <span data-ttu-id="86012-112">Базовый Q# код для инициализации и преобразования кубит, затем выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="86012-112">The basic Q# code to initialize and transform a qubit, then, looks like this:</span></span>

```qsharp
using (qubit = Qubit()) {
    // At this point, the qubit is in the state |0⟩.
    H(qubit);
    // H is now applied, such that the qubit is in H|0⟩ = |+⟩, as desired.
}
```
<span data-ttu-id="86012-113">Дополнительные сведения об инициализации и *выделении*Кубитс см. в разделе [Работа с Кубитс](xref:microsoft.quantum.guide.qubits).</span><span class="sxs-lookup"><span data-stu-id="86012-113">For more information on initializing, or *allocating*, qubits, see [Working with qubits](xref:microsoft.quantum.guide.qubits).</span></span>

## <a name="quantum-states-in-no-locq"></a><span data-ttu-id="86012-114">Состояния тактов вQ#</span><span class="sxs-lookup"><span data-stu-id="86012-114">Quantum states in Q#</span></span>

<span data-ttu-id="86012-115">Важно, что предыдущая программа не ссылается явно на состояние в, Q# но описывает, как наша программа *преобразует* состояние.</span><span class="sxs-lookup"><span data-stu-id="86012-115">Importantly, the previous program does not explicitly refer to the state within Q# but described how our program *transformed* the state.</span></span>
<span data-ttu-id="86012-116">При таком подходе можно полностью относиться к состоянию такта даже *на* каждом целевом компьютере, который может иметь различные интерпретации в зависимости от компьютера.</span><span class="sxs-lookup"><span data-stu-id="86012-116">With this approach, you can be entirely agnostic about what a quantum state even *is* on each target machine, which might have different interpretations depending on the machine.</span></span> 

<span data-ttu-id="86012-117">Q#Программа не может интроспект в состояние кубит.</span><span class="sxs-lookup"><span data-stu-id="86012-117">A Q# program cannot introspect into the state of a qubit.</span></span>
<span data-ttu-id="86012-118">Вместо этого программа может вызывать такие операции, как, [`Measure`](xref:microsoft.quantum.intrinsic.measure) чтобы получить сведения из кубит и вызвать операции, такие как [`X`](xref:microsoft.quantum.intrinsic.x) и, [`H`](xref:microsoft.quantum.intrinsic.h) чтобы действовать в состоянии кубит.</span><span class="sxs-lookup"><span data-stu-id="86012-118">Instead, a program can call operations such as [`Measure`](xref:microsoft.quantum.intrinsic.measure) to learn information from a qubit, and call operations such as [`X`](xref:microsoft.quantum.intrinsic.x) and [`H`](xref:microsoft.quantum.intrinsic.h) to act on the state of a qubit.</span></span>
<span data-ttu-id="86012-119">*Фактически эти операции делаются* только на целевом компьютере, используемом для запуска конкретной Q# программы.</span><span class="sxs-lookup"><span data-stu-id="86012-119">What these operations actually *do* is only made concrete by the target machine used to run the particular Q# program.</span></span>
<span data-ttu-id="86012-120">Например, если запустить программу в [симуляторе полного состояния](xref:microsoft.quantum.machines.full-state-simulator), симулятор выполняет соответствующие математические операции с имитацией тактовой системы.</span><span class="sxs-lookup"><span data-stu-id="86012-120">For example, if running the program on our [full-state simulator](xref:microsoft.quantum.machines.full-state-simulator), the simulator performs the corresponding mathematical operations to the simulated quantum system.</span></span>
<span data-ttu-id="86012-121">Но в будущем, когда целевой компьютер является реальным компьютером-тактом, вызов таких операций в Q# направляет тактовый компьютер на выполнение соответствующих *реальных* операций в *реальной* тактовой системе, например, в точности лазерных импульсов.</span><span class="sxs-lookup"><span data-stu-id="86012-121">But looking toward the future, when the target machine is a real quantum computer, calling such operations in Q# directs the quantum computer to perform the corresponding *real* operations on the *real* quantum system, for example, precisely timed laser pulses).</span></span>

<span data-ttu-id="86012-122">Q#Программа повторно объединяет эти операции в соответствии с определением на целевом компьютере для создания новых операций более высокого уровня для вычисления тактового времени.</span><span class="sxs-lookup"><span data-stu-id="86012-122">A Q# program recombines these operations as defined by a target machine to create new, higher-level operations to express quantum computation.</span></span>
<span data-ttu-id="86012-123">Таким образом, Q# упрощает выражать логику базового такта и гибридного такта, а также общие алгоритмы в отношении структуры целевого компьютера или симулятора.</span><span class="sxs-lookup"><span data-stu-id="86012-123">In this way, Q# makes it easy to express the logic underlying quantum and hybrid quantum–classical algorithms, while also being general with respect to the structure of a target machine or simulator.</span></span>

## <a name="no-locq-operations-and-functions"></a><span data-ttu-id="86012-124">Q#операции и функции</span><span class="sxs-lookup"><span data-stu-id="86012-124">Q# operations and functions</span></span>

<span data-ttu-id="86012-125">Конкретнее, Q# Программа состоит из *операций*, *функций*и любых определяемых пользователем типов.</span><span class="sxs-lookup"><span data-stu-id="86012-125">Concretely, a Q# program comprises *operations*, *functions*, and any user-defined types.</span></span> 

<span data-ttu-id="86012-126">Операции используются для описания преобразований тактовых систем и являются наиболее фундаментальным стандартным блоком Q# программ.</span><span class="sxs-lookup"><span data-stu-id="86012-126">Operations are used to describe the transformations of quantum systems and are the most fundamental building block of Q# programs.</span></span> <span data-ttu-id="86012-127">Каждая операция, определенная в Q# , может вызвать любое количество других операций.</span><span class="sxs-lookup"><span data-stu-id="86012-127">Each operation defined in Q# may then call any number of other operations.</span></span>

<span data-ttu-id="86012-128">В отличие от операций, функции используются для описания чисто *детерминированного* классического поведения и не имеют каких либо эффектов, помимо вычисления классических значений.</span><span class="sxs-lookup"><span data-stu-id="86012-128">In contrast to operations, functions are used to describe purely *deterministic* classical behavior and do not have any effects besides computing classical values.</span></span> <span data-ttu-id="86012-129">Например, предположим, что необходимо измерить Кубитс в конце программы и добавить результаты измерения в массив.</span><span class="sxs-lookup"><span data-stu-id="86012-129">For example, suppose you want to measure the qubits at the end of a program and add the measurement results to an array.</span></span>
<span data-ttu-id="86012-130">В этом случае `Measure` — это *Операция* , которая указывает целевому компьютеру на выполнение измерения в (реальном или смоделированной) Кубитс.</span><span class="sxs-lookup"><span data-stu-id="86012-130">In this case, `Measure` is an *operation* that instructs the target machine to perform a measurement on the (real or simulated) qubits.</span></span> <span data-ttu-id="86012-131">В то же время *функции* обрабатывают классический процесс добавления возвращаемых результатов в массив.</span><span class="sxs-lookup"><span data-stu-id="86012-131">At the same time, *functions* handle the classical process of adding the returned results to an array.</span></span>

<span data-ttu-id="86012-132">Вместе операции и функции называются *вызываемыми*.</span><span class="sxs-lookup"><span data-stu-id="86012-132">Together, operations and functions are known as *callables*.</span></span> <span data-ttu-id="86012-133">Их базовая структура и поведение представлены и подробно описаны в [операциях и функциях в Q# ](xref:microsoft.quantum.guide.operationsfunctions).</span><span class="sxs-lookup"><span data-stu-id="86012-133">Their underlying structure and behavior are introduced and detailed in [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions).</span></span>


## <a name="no-locq-syntax-overview"></a><span data-ttu-id="86012-134">Q#обзор синтаксиса</span><span class="sxs-lookup"><span data-stu-id="86012-134">Q# syntax overview</span></span>

<span data-ttu-id="86012-135">Синтаксис языка описывает различные сочетания символов, которые формируют синтаксическую правильную программу.</span><span class="sxs-lookup"><span data-stu-id="86012-135">The syntax of a language describes the different combinations of symbols that form a syntactically correct program.</span></span>
<span data-ttu-id="86012-136">В Q# элементы синтаксиса классифицируются в три различные группы: типы, выражения и операторы.</span><span class="sxs-lookup"><span data-stu-id="86012-136">In Q#, syntax elements are classified into three different groups: types, expressions, and statements.</span></span>

### <a name="types"></a><span data-ttu-id="86012-137">Типы</span><span class="sxs-lookup"><span data-stu-id="86012-137">Types</span></span>
<span data-ttu-id="86012-138">Q#— Это строго типизированный язык, позволяющий компилятору обеспечить строгую гарантию для Q# программ во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="86012-138">Q# is a strongly-typed language, such that careful use of types can help the compiler provide strong guarantees about Q# programs at compile time.</span></span>
<span data-ttu-id="86012-139">Помимо стандартных и потактовых встроенных типов-примитивов, например,,, `Int` `Bool` `Qubit` и `Result` , Q# обеспечивает поддержку определяемых пользователем типов.</span><span class="sxs-lookup"><span data-stu-id="86012-139">In addition to standard and quantum-specific built-in primitive types, for example, `Int`, `Bool`, `Qubit`, and `Result`, Q# provides support for user-defined types.</span></span>

<span data-ttu-id="86012-140">Описание всех типов-примитивов, сведений о типах массивов и кортежей, а также действиях по определению новых типов в Q# файле см. [в разделе Типы в Q# ](xref:microsoft.quantum.guide.types).</span><span class="sxs-lookup"><span data-stu-id="86012-140">For descriptions of all the primitive types, details for array and tuple types, and steps to define new types within a Q# file, see [Types in Q#](xref:microsoft.quantum.guide.types).</span></span>

### <a name="expressions"></a><span data-ttu-id="86012-141">Выражения</span><span class="sxs-lookup"><span data-stu-id="86012-141">Expressions</span></span>
<span data-ttu-id="86012-142">Выражение в языке программирования — это сочетание одной или нескольких констант, переменных, операторов и функций, которые язык программирования интерпретирует и вычисляет в определенном значении.</span><span class="sxs-lookup"><span data-stu-id="86012-142">An expression in a programming language is a combination of one or more constants, variables, operators, and functions that the programming language interprets and evaluates to a specific value.</span></span>
<span data-ttu-id="86012-143">Чаще всего для каждого типа в языке выражения этого типа могут быть либо *литералами* , либо символами, привязанными к значению этого типа.</span><span class="sxs-lookup"><span data-stu-id="86012-143">Most simply, for every type in a language, expressions of that type can be either *literals* or symbols bound to a value of that type.</span></span>
<span data-ttu-id="86012-144">Например, `5` является `Int` литералом (то есть выражением типа `Int` ), и если символ `count` привязан к целому значению `5` , то `count` также является целочисленным выражением.</span><span class="sxs-lookup"><span data-stu-id="86012-144">For example, `5` is an `Int` literal (thus also an expression of type `Int`), and if the symbol `count` is bound to the integer value `5`, then `count` is also an integer expression.</span></span>

<span data-ttu-id="86012-145">Кроме того, выражение может состоять из других выражений, Объединенных определенными операторами.</span><span class="sxs-lookup"><span data-stu-id="86012-145">Additionally, an expression can consist of other expressions combined by certain operators.</span></span>
<span data-ttu-id="86012-146">Например, другое `Int` выражение, результатом которого `5` является `2+3` .</span><span class="sxs-lookup"><span data-stu-id="86012-146">For example, another `Int` expression that evaluates to `5` is `2+3`.</span></span>

<span data-ttu-id="86012-147">Дополнительные сведения о выражениях и совместимых операторах в см Q# . в разделе [выражения типа Q# в ](xref:microsoft.quantum.guide.expressions).</span><span class="sxs-lookup"><span data-stu-id="86012-147">For more information about expressions and compatible operators in Q#, see [Type Expressions in Q#](xref:microsoft.quantum.guide.expressions).</span></span> 

### <a name="statements"></a><span data-ttu-id="86012-148">Операторы</span><span class="sxs-lookup"><span data-stu-id="86012-148">Statements</span></span> 
<span data-ttu-id="86012-149">Оператор — это Синтаксическая единица императивного языка программирования, который выражает какое-то действие для выполнения. Операторы, которые отличаются от выражений в этих инструкциях, не возвращают результаты и выполняются исключительно для своих побочных эффектов.</span><span class="sxs-lookup"><span data-stu-id="86012-149">A statement is a syntactic unit of an imperative programming language that expresses some action to carry out. Statements contrast with expressions in that statements do not return results and are executed solely for their side effects.</span></span> <span data-ttu-id="86012-150">Однако выражения всегда возвращают результат и часто не имеют побочных эффектов.</span><span class="sxs-lookup"><span data-stu-id="86012-150">Expressions, however, always return a result and often do not have side effects at all.</span></span> <span data-ttu-id="86012-151">Вкратце, Q# операторы выполняются, тогда как выражения оцениваются.</span><span class="sxs-lookup"><span data-stu-id="86012-151">In short, Q# statements are executed, while expressions are evaluated.</span></span>

<span data-ttu-id="86012-152">Простой пример оператора в Q# заключается в назначении символа выражению:</span><span class="sxs-lookup"><span data-stu-id="86012-152">A simple example of a statement in Q# is assigning a symbol to an expression:</span></span>
```qsharp
let count = 5;
```

<span data-ttu-id="86012-153">Более интересным примером является оператор, `for` который поддерживает итерацию и включает *блок операторов*.</span><span class="sxs-lookup"><span data-stu-id="86012-153">A more interesting example is the `for` statement which supports iteration and includes a *statement block*.</span></span>
<span data-ttu-id="86012-154">Предположим, `qubits` символ привязан к регистру Кубитс (техническим типом `Qubit[]` или массиву `Qubit` типов).</span><span class="sxs-lookup"><span data-stu-id="86012-154">Suppose `qubits` is the symbol bound to a register of qubits (technically of type `Qubit[]`, or an array of `Qubit` types).</span></span> <span data-ttu-id="86012-155">Следующее действие</span><span class="sxs-lookup"><span data-stu-id="86012-155">Then</span></span>
```qsharp
for (qubit in qubits) {
    H(qubit);
}
```
<span data-ttu-id="86012-156">Инструкция, которая выполняет перебор каждого кубит в регистре, выполняя `H` операцию с каждым из них.</span><span class="sxs-lookup"><span data-stu-id="86012-156">is a statement that iterates over each qubit in the register, performing the `H` operation on each one.</span></span> <span data-ttu-id="86012-157">Обратите внимание, что `H(qubit);` также является оператором.</span><span class="sxs-lookup"><span data-stu-id="86012-157">Note that `H(qubit);` is a statement in itself as well.</span></span>

<span data-ttu-id="86012-158">Можно использовать любое выражение вызова типа `Unit` ( `Unit` тип не возвращает никакой информации) в качестве инструкции.</span><span class="sxs-lookup"><span data-stu-id="86012-158">You can use any call expression of type `Unit` (a `Unit` type does not return any information) as a statement.</span></span>
<span data-ttu-id="86012-159">Этот тип выражения полезен при вызове операций с Кубитс, которые возвращают, `Unit` поскольку целью оператора является изменение неявного состояния такта.</span><span class="sxs-lookup"><span data-stu-id="86012-159">This type of expression is useful when calling operations on qubits that return `Unit` because the purpose of the statement is to modify the implicit quantum state.</span></span>
<span data-ttu-id="86012-160">Для операторов вычисления выражения требуется завершающая точка с запятой.</span><span class="sxs-lookup"><span data-stu-id="86012-160">Expression evaluation statements require a terminating semicolon.</span></span>

<span data-ttu-id="86012-161">Инструкции используются для создания практически всех аспектов Q# программы, и ни одна страница не может охватывать всю информацию, относящуюся к ним.</span><span class="sxs-lookup"><span data-stu-id="86012-161">You use statements to build nearly every aspect of a Q# program, and no single page could encompass all the information relating to them.</span></span>
<span data-ttu-id="86012-162">Дополнительные сведения о своей лексической структуре и форматировании см. в разделе [ Q# File Structure](xref:microsoft.quantum.guide.filestructure); для назначения и области привязки символов, см. [в разделе переменные Q# в ](xref:microsoft.quantum.guide.variables); и для циклов потока управления, таких как `for` , см. раздел [поток управления в Q# ](xref:microsoft.quantum.guide.controlflow).</span><span class="sxs-lookup"><span data-stu-id="86012-162">For more information about their lexical structure and formatting, see [Q# File Structure](xref:microsoft.quantum.guide.filestructure); for symbol binding assignment and scope, see [Variables in Q#](xref:microsoft.quantum.guide.variables); and for control flow loops such as `for`, see [Control Flow in Q#](xref:microsoft.quantum.guide.controlflow).</span></span>

## <a name="next-steps"></a><span data-ttu-id="86012-163">Дальнейшие шаги</span><span class="sxs-lookup"><span data-stu-id="86012-163">Next steps</span></span>

<span data-ttu-id="86012-164">Начните изучение [типов в Q# ](xref:microsoft.quantum.guide.types).</span><span class="sxs-lookup"><span data-stu-id="86012-164">Start learning about [Types in Q#](xref:microsoft.quantum.guide.types).</span></span>

<span data-ttu-id="86012-165">Дополнительные сведения об основах и мотивации Q# см. в разделе [Зачем нужно Q# ?](https://devblogs.microsoft.com/qsharp/why-do-we-need-q/)</span><span class="sxs-lookup"><span data-stu-id="86012-165">For more background about the foundations and motivation behind Q#, see [Why do we need Q#?](https://devblogs.microsoft.com/qsharp/why-do-we-need-q/).</span></span>
