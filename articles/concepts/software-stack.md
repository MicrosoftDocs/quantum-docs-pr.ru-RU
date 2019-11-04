---
title: Стек программного обеспечения | Документация Майкрософт
description: Программный стек
author: QuantumWriter
uid: microsoft.quantum.concepts.software-stack
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: f97dfacf6cde5fa92e1f368efaae36554a5c944d
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/28/2019
ms.locfileid: "73184735"
---
# <a name="software-stack-for-quantum-computing"></a><span data-ttu-id="97ccd-103">Программный стек для вычислений для тактов</span><span class="sxs-lookup"><span data-stu-id="97ccd-103">Software stack for quantum computing</span></span>
<span data-ttu-id="97ccd-104">Как правило, если компьютер выдумал одно устройство, на котором работает приложение, современные вычислительные среды гораздо более сложны и расширены.</span><span class="sxs-lookup"><span data-stu-id="97ccd-104">Normally when we think of a computer we envision a single device running an application, but modern computing environments are much more complex and advanced.</span></span> <span data-ttu-id="97ccd-105">Приложение, которое мы взаимодействует с, обычно налагаются на нескольких уровнях программного обеспечения, которые обеспечивают выполнение приложения на уровне оборудования.</span><span class="sxs-lookup"><span data-stu-id="97ccd-105">The application we interact with typically rests on multiple layers of software that provide for the application's execution down to the hardware level.</span></span> <span data-ttu-id="97ccd-106">Эти уровни программного обеспечения необходимы для того, чтобы абстрактно разрабатывать решения для приложений от базовой сложности всей вычислительной системы.</span><span class="sxs-lookup"><span data-stu-id="97ccd-106">These software layers are necessary to abstract the development of an application solution from the underlying complexity of the complete computing system.</span></span> <span data-ttu-id="97ccd-107">Если разработчику пришлось думать о шине, архитектурах кэша, протоколах связи и многом во время написания простого приложения для смартфонов, задача стала гораздо более сложной.</span><span class="sxs-lookup"><span data-stu-id="97ccd-107">If a developer had to think about bus, cache architectures, communication protocols, and more while writing a simple smartphone app, the task would become much more complex.</span></span>  <span data-ttu-id="97ccd-108">Концепция *программного стека* была разработана в классический вычислительной среде для решения этих проблем.</span><span class="sxs-lookup"><span data-stu-id="97ccd-108">The concept of a *software stack* was developed in classical computing to address these issues.</span></span>  <span data-ttu-id="97ccd-109">Позаимствование из классической концепции, программный стек также является ключевой частью концепции обработки тактовых вычислений с помощью Q #.</span><span class="sxs-lookup"><span data-stu-id="97ccd-109">Borrowing from the classical concept, a software stack is also a key part of the vision behind quantum computing with Q#.</span></span>

## <a name="conventional-stack"></a><span data-ttu-id="97ccd-110">Основной стек</span><span class="sxs-lookup"><span data-stu-id="97ccd-110">Conventional stack</span></span>
<span data-ttu-id="97ccd-111">Ключевая идея программного стека — рекурсия.</span><span class="sxs-lookup"><span data-stu-id="97ccd-111">The key idea behind a software stack is recursion.</span></span>  <span data-ttu-id="97ccd-112">Он состоит из нескольких вложенных уровней интерфейсов, которые позволяют получить более подробные сведения о более низких уровнях устройства от разработчика.</span><span class="sxs-lookup"><span data-stu-id="97ccd-112">It consists of several nested layers of interfaces that abstract the details of the lower levels of the device away from the developer.</span></span>  <span data-ttu-id="97ccd-113">Например, часто используемый стек программного обеспечения включает в себя запуск ASP.NET (язык программирования), поверх SQL Server (система управления реляционными базами данных), который работает поверх службы IIS (веб-сервера), работающего поверх Windows Server ( операционная система), которая управляет оборудованием компьютера.</span><span class="sxs-lookup"><span data-stu-id="97ccd-113">For example, a commonly used software stack involves running ASP.NET (a programming language), on top of SQL server (a relational database management system), which runs on top of Internet Information Services (a web server), which runs on top of Windows server (an operating system), which drives the computer hardware.</span></span>  <span data-ttu-id="97ccd-114">Изучив программное обеспечение как иерархию, можно написать программное обеспечение в ASP.NET без необходимости понимания сведений о низком уровне по отношению к программному обеспечению, расположенному ниже.</span><span class="sxs-lookup"><span data-stu-id="97ccd-114">By looking at software as a hierarchy, one can write software in ASP.NET without needing to understand the low-level details of all the software below it.</span></span>

## <a name="quantum-stack"></a><span data-ttu-id="97ccd-115">Тактовый стек</span><span class="sxs-lookup"><span data-stu-id="97ccd-115">Quantum stack</span></span>

<span data-ttu-id="97ccd-116">Стек программного обеспечения в тактовых вычислениях не имеет иного принципа, и на практике работает на более низком уровне по сравнению с традиционными стеками.</span><span class="sxs-lookup"><span data-stu-id="97ccd-116">The software stack in quantum computing is no different in principle, and in practice operates at a lower level than traditional stacks.</span></span>  <span data-ttu-id="97ccd-117">Как выглядит тактовая область?</span><span class="sxs-lookup"><span data-stu-id="97ccd-117">What does a quantum stack look like?</span></span>  <span data-ttu-id="97ccd-118">Компьютер-такт не заменяет традиционные (часто называемые классическими) компьютеры.</span><span class="sxs-lookup"><span data-stu-id="97ccd-118">A quantum computer is not a replacement for traditional (often called classical) computers.</span></span>  <span data-ttu-id="97ccd-119">На самом деле, тактовые компьютеры почти наверняка будут работать совместно с классическими компьютерами для решения вычислительных задач.</span><span class="sxs-lookup"><span data-stu-id="97ccd-119">In fact, quantum computers will almost certainly work in tandem with classical computers to solve computational problems.</span></span>  <span data-ttu-id="97ccd-120">В части это происходит из-за хрупкости данных о такте.</span><span class="sxs-lookup"><span data-stu-id="97ccd-120">In part, this arises because of the fragility of quantum data.</span></span>  <span data-ttu-id="97ccd-121">Данные такта настолько ненадежны, что если вы даже Взгляните на него, вы почти наверняка повредите наблюдаемую информацию.</span><span class="sxs-lookup"><span data-stu-id="97ccd-121">Quantum data is so fragile that if you even look at it you almost certainly damage the information being observed.</span></span>  <span data-ttu-id="97ccd-122">Таким образом, тактовые компьютеры должны быть спроектированы с учетом коррекции ошибок такта, поэтому непреднамеренное взаимодействие из физической среды не приводит к случайному повреждению информации и вычислений.</span><span class="sxs-lookup"><span data-stu-id="97ccd-122">Quantum computers will thus need to be designed with quantum error correction in mind so that stray interactions from its physical environment do not inadvertently damage the information and computation.</span></span> <span data-ttu-id="97ccd-123">По этой причине естественная цель для Q # — это исправленный с ошибками тактовый компьютер (часто *называемый отказоустойчивым компьютерным тактовым* ), который принимает список тактовых инструкций (называемых шлюзами или операциями шлюза) и применяет эти инструкции к такту. хранящиеся в нем данные.</span><span class="sxs-lookup"><span data-stu-id="97ccd-123">For this reason, a natural target for Q# is an error-corrected quantum computer (often called a *fault-tolerant* quantum computer) that accepts a list of quantum instructions (called gates or gate operations) and applies those instructions to the quantum data stored within it.</span></span>  <span data-ttu-id="97ccd-124">Обратите внимание, что если количество операций Кубитс и шлюзов в алгоритме такта или программе достаточно мало, исправление ошибок может оказаться необязательным.</span><span class="sxs-lookup"><span data-stu-id="97ccd-124">Note that if the number of qubits and gate operations in a quantum algorithm or program is small enough, error correction may not be absolutely necessary.</span></span>  <span data-ttu-id="97ccd-125">Тем не менее, по мере роста количества операций Кубитс и Gate это будет обязательным требованием, поэтому мы Разрабатывайте стек программного обеспечения и раздел Q # на выразился и эффективно обработаем исправление ошибок и обеспечивайте масштабируемые, отказоустойчивые тактовые вычисления.</span><span class="sxs-lookup"><span data-stu-id="97ccd-125">However as the number of qubits and gate operations grow, it will more certainly be a requirement, thus we architect our software stack and Q# to aptly and efficiently handle error correction and enable scalable, fault-tolerant quantum computing.</span></span>

### <a name="error-correction"></a><span data-ttu-id="97ccd-126">Исправление ошибок</span><span class="sxs-lookup"><span data-stu-id="97ccd-126">Error correction</span></span>
<span data-ttu-id="97ccd-127">Для исправления ошибок требуется быстрый и надежный классический компьютер в сочетании с тактовым компьютером, чтобы исправлять ошибки по мере их появления в вычислении такта.</span><span class="sxs-lookup"><span data-stu-id="97ccd-127">Error correction requires a fast and reliable classical computer to be run in concert with the quantum computer to correct errors as they appear in the quantum computation.</span></span>  <span data-ttu-id="97ccd-128">На практике такие компоненты, как программируемые массивы шлюзов (FPGA) или быстрые крйоженик процессоры, могут потребоваться для обнаружения и исправления ошибок быстрее, чем они естественным образом накапливаются на тактовых компьютерах.</span><span class="sxs-lookup"><span data-stu-id="97ccd-128">In practice, components such as field-programmable gate arrays (FPGAs) or fast cryogenic processors may be needed to identify and correct the errors faster than they naturally accumulate in the quantum computer.</span></span>  <span data-ttu-id="97ccd-129">В результате компьютер-такт является гибридным компьютером, который состоит из нескольких вычислительных устройств, которые работают на широком диапазоне температур.</span><span class="sxs-lookup"><span data-stu-id="97ccd-129">As a result, a quantum computer is a hybrid machine comprised of several different computational devices that operate over a wide range of temperatures.</span></span>  <span data-ttu-id="97ccd-130">По этой причине гораздо лучше подумать о программировании тактового компьютера с помощью линзы программного стека, так как существует множество уровней оборудования и программного обеспечения (классический и тактовый), которые требуются для достижения максимальной реализации такта. алгоритм на компьютере-такте.</span><span class="sxs-lookup"><span data-stu-id="97ccd-130">For this reason, it is much more helpful to think about programming a quantum computer through the lens of a software stack, as there are many layers of hardware and software (classical and quantum) required to ultimately achieve the implementation of a quantum algorithm on a quantum computer.</span></span>

### <a name="quantum-conceptual-stack"></a><span data-ttu-id="97ccd-131">Стек концептуальных тактов</span><span class="sxs-lookup"><span data-stu-id="97ccd-131">Quantum conceptual stack</span></span>
<span data-ttu-id="97ccd-132">Ниже приведен концептуальный стек, иллюстрирующий функциональный поток, в котором показано, как выполняется рефакторинг 8704143553785700723 в среде тактовой передачи.</span><span class="sxs-lookup"><span data-stu-id="97ccd-132">A conceptual stack that illustrates the functional flow of factoring 8704143553785700723 in a quantum computing environment is shown below:</span></span>

![Программный стек](~/media/concepts_stack.png)

### <a name="specification-and-algorithm"></a><span data-ttu-id="97ccd-134">Спецификация и алгоритм</span><span class="sxs-lookup"><span data-stu-id="97ccd-134">Specification and algorithm</span></span>
<span data-ttu-id="97ccd-135">Существует несколько обширных этапов программирования, таких как вычисления тактов.</span><span class="sxs-lookup"><span data-stu-id="97ccd-135">There are several broad stages of programming such a quantum computation.</span></span>  <span data-ttu-id="97ccd-136">Первый, и, вероятно, самый сложный этап — указание проблемы, которую один из них хочет решить.</span><span class="sxs-lookup"><span data-stu-id="97ccd-136">The first, and arguably most challenging phase, is specifying the problem that one wishes to solve.</span></span>  <span data-ttu-id="97ccd-137">В этом случае проблема состоит в том, чтобы разделить число 8704143553785700723 на произведение двух простых чисел.</span><span class="sxs-lookup"><span data-stu-id="97ccd-137">In this case, the problem is to factor the number 8704143553785700723  into a product of two prime numbers.</span></span>  <span data-ttu-id="97ccd-138">Следующий шаг включает создание алгоритма для решения этой вычислительной задачи.</span><span class="sxs-lookup"><span data-stu-id="97ccd-138">The next step involves designing an algorithm for solving this computational problem.</span></span>  <span data-ttu-id="97ccd-139">В этом случае для определения факторов можно использовать известный алгоритм факторинга тактов Шор.</span><span class="sxs-lookup"><span data-stu-id="97ccd-139">In this case, Shor's famous quantum factoring algorithm can be used to find the factors.</span></span>  <span data-ttu-id="97ccd-140">Этот алгоритм выражается в Q #, а затем последовательность операций тактов, которые можно выполнить на идеальном компьютере, отличном от ошибок.</span><span class="sxs-lookup"><span data-stu-id="97ccd-140">This algorithm is expressed in Q# and then a sequence of quantum operations is output that could be run on an idealized error-free quantum computer.</span></span>  

### <a name="physical-gates"></a><span data-ttu-id="97ccd-141">Физические шлюзы</span><span class="sxs-lookup"><span data-stu-id="97ccd-141">Physical gates</span></span>
<span data-ttu-id="97ccd-142">В этом примере предполагается, что нет такого рода, чтобы предоставить бесплатный тактовый компьютер с ошибками, чтобы на последующем шаге выполнить операции, созданные в Q #, и переведет их с помощью шаблонов, заданных методом исправления ошибок такта, выбранного в физических шлюзах, которые Базовое оборудование может выполняться.</span><span class="sxs-lookup"><span data-stu-id="97ccd-142">In this example, assume nature is not so kind as to provide an error-free quantum computer so the subsequent step takes the operations emitted by Q# and translates them using templates specified by the quantum error correction method chosen into physical gates that the basic hardware can execute.</span></span>  <span data-ttu-id="97ccd-143">Этот процесс подразумевает замену каждого логического кубит, описанного в предыдущей модели, узлом физической Кубитс, который используется для хранения и защиты информации в пределах одного кубит в избыточном виде, который может выставить на себя проблемы с локальными ошибками во всех составляющих физических Кубитс достаточно долго для обнаружения и исправления таких ошибок.</span><span class="sxs-lookup"><span data-stu-id="97ccd-143">This process involves replacing every logical qubit described in the previous model with a host of physical qubits that are used to store and protect the information within a single qubit in a redundant fashion that can resist local errors on the constituent physical qubits long enough for such errors to be detected and corrected.</span></span>  <span data-ttu-id="97ccd-144">Точно так же, как логическая Кубитс, описываемая в коде Q #, должна быть заменена многими физическими Кубитс, аналогичным образом каждый тактовый шлюз, описанный в выходных данных, должен быть преобразован в последовательность физических шлюзов, которые работают с физическим Кубитс.</span><span class="sxs-lookup"><span data-stu-id="97ccd-144">Just as the logical qubits described by the Q# code need to be replaced with many physical qubits, similarly each quantum gate described in the output needs to be translated into a sequence of physical gates that act upon the physical qubits.</span></span>  <span data-ttu-id="97ccd-145">По этой причине выход Q # редко является окончательным целевым объектом для тактовых вычислений, и дополнительные уровни абстракции необходимы для выполнения кода на оборудовании очевиднымным образом.</span><span class="sxs-lookup"><span data-stu-id="97ccd-145">For this reason, the output of Q# is seldom the final target for quantum computing and further levels of abstraction are needed to execute the code on hardware in an oblivious fashion.</span></span>

### <a name="control-computer"></a><span data-ttu-id="97ccd-146">Компьютер управления</span><span class="sxs-lookup"><span data-stu-id="97ccd-146">Control computer</span></span>
<span data-ttu-id="97ccd-147">После этого физическая цепочка шлюзов загружается в обычный компьютер, который отправляет эти инструкции на контрольный компьютер, который напрямую взаимодействует с тактовым компьютером.</span><span class="sxs-lookup"><span data-stu-id="97ccd-147">The physical gate sequence is then loaded into an ordinary computer that sends these instructions down to a control computer that interfaces directly with the quantum computer.</span></span>  <span data-ttu-id="97ccd-148">Этот слой в стеке программного обеспечения часто обрабатывается экспериментальным программным обеспечением, например [ккодес](http://qcodes.github.io/Qcodes/).</span><span class="sxs-lookup"><span data-stu-id="97ccd-148">This layer within the software stack is often handled by experimental control software such as [QCoDeS](http://qcodes.github.io/Qcodes/).</span></span>

### <a name="interface-computer"></a><span data-ttu-id="97ccd-149">Компьютер интерфейса</span><span class="sxs-lookup"><span data-stu-id="97ccd-149">Interface computer</span></span>
<span data-ttu-id="97ccd-150">Последний шаг в этом процессе подразумевает, что компьютер интерфейса сначала подает шлюзам необходимые для быстрого управления компьютер.</span><span class="sxs-lookup"><span data-stu-id="97ccd-150">The final step in this process involves the interface computer first streaming the gates as needed to a fast control computer.</span></span> <span data-ttu-id="97ccd-151">Затем компьютер быстрого управления применяет требуемые напряжения (обычно называемые пульсом) для реализации необходимого шлюза на Кубитс.</span><span class="sxs-lookup"><span data-stu-id="97ccd-151">Then the fast control computer applies the voltages needed (commonly called pulses) to implement the required gates on qubits.</span></span> <span data-ttu-id="97ccd-152">Это необходимо сделать при исправлении ошибок, которые могут воздействовать при исправлении ошибок такта.</span><span class="sxs-lookup"><span data-stu-id="97ccd-152">This has to be done while correcting any errors that are observed through quantum error correction.</span></span>  <span data-ttu-id="97ccd-153">Крйоженик FPGAs или другое exoticное оборудование может потребоваться для выполнения этих шагов в рамках строгого требования к времени, накладываемого скоростью, с которой ошибки появляются на компьютере такта.</span><span class="sxs-lookup"><span data-stu-id="97ccd-153">Cryogenic FPGAs or other exotic hardware may be needed to perform these steps within the stringent time requirements imposed by the rate at which errors appear in the quantum computer.</span></span>  <span data-ttu-id="97ccd-154">Целевой язык на этом уровне часто [вхдл](https://en.wikipedia.org/wiki/VHDL), что требует отдельного способа думать от того, что используется в верхнем конце стека для анализа описания алгоритма такта.</span><span class="sxs-lookup"><span data-stu-id="97ccd-154">The target language on this level is often [VHDL](https://en.wikipedia.org/wiki/VHDL), which requires a distinct way of thinking from that which is used at the top end of the stack to parse a description of a quantum algorithm.</span></span>

### <a name="the-q-quantum-programming-language"></a><span data-ttu-id="97ccd-155">Язык программирования на такт Q #</span><span class="sxs-lookup"><span data-stu-id="97ccd-155">The Q# quantum programming language</span></span>
<span data-ttu-id="97ccd-156">Цель Q # — предоставить простой язык, позволяющий разработчикам писать код, нацеленный на множество платформ тактовых вычислений, и взаимодействовать с промежуточными слоями программного обеспечения, которое находится между пользователем и устройством такта.</span><span class="sxs-lookup"><span data-stu-id="97ccd-156">The aim of Q# is to provide a simple language that allows developers to write code that targets a wealth of quantum computing platforms and interface with the intervening layers of software that stand between the user and the quantum device.</span></span>  <span data-ttu-id="97ccd-157">Этот язык упрощает этот процесс, принимая понятие стека программного обеспечения и абстракции многих деталей на базовом компьютере-такте, позволяя другим уровням стека, таким как C#, выполнять необходимые действия. переводы кода Q # в фундаментальные операции.</span><span class="sxs-lookup"><span data-stu-id="97ccd-157">The language facilitates this by embracing the notion of a software stack and abstracting many of the details of the underlying quantum computer while allowing other levels of the stack, exposed through a language such as C#, to perform the necessary translations from Q# code to fundamental operations.</span></span>  <span data-ttu-id="97ccd-158">Это позволяет разработчику сосредоточиться на том, что они делают лучше: Проектирование алгоритмов и устранение проблем.</span><span class="sxs-lookup"><span data-stu-id="97ccd-158">This allows the developer to focus on what they do best: designing algorithms and solving problems.</span></span>