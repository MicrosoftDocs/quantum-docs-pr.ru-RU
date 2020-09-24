---
title: Руководство пользователя по Q#
description: Общие сведения о назначении и содержимом этого руководства пользователя
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide
no-loc:
- Q#
- $$v
ms.openlocfilehash: f0680e773c8233d6c4f1acb742b3cc38dbc069d5
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834760"
---
# <a name="the-no-locq-user-guide"></a><span data-ttu-id="84440-103">Руководство пользователя по Q#</span><span class="sxs-lookup"><span data-stu-id="84440-103">The Q# User Guide</span></span>

<span data-ttu-id="84440-104">Перед вами руководство пользователя по Q#.</span><span class="sxs-lookup"><span data-stu-id="84440-104">Welcome to the Q# User Guide!</span></span> 

<span data-ttu-id="84440-105">В различных статьях в рамках этого руководства мы подробно рассмотрим основные понятия языка Q# и все, что вам потребуется для написания квантовых программ.</span><span class="sxs-lookup"><span data-stu-id="84440-105">In the different topics of this guide, we detail the core concepts of the Q# language and all the information you need to write quantum programs.</span></span>

## <a name="user-guide-contents"></a><span data-ttu-id="84440-106">Содержимое руководства пользователя</span><span class="sxs-lookup"><span data-stu-id="84440-106">User Guide Contents</span></span>

- <span data-ttu-id="84440-107">[Основы Q#.](xref:microsoft.quantum.guide.basics) Вводные сведения о назначении и функциональных возможностях языка Q#.</span><span class="sxs-lookup"><span data-stu-id="84440-107">[Q# Basics](xref:microsoft.quantum.guide.basics): An introductory overview of the purpose and functionality of the Q# programming language.</span></span> 

- <span data-ttu-id="84440-108">[Способы запуска программы на Q#.](xref:microsoft.quantum.guide.host-programs) Здесь описывается ход выполнения программы на Q#, а также приводится обзор разных способов, с помощью которых ее можно вызвать: из командной строки, Jupyter Notebook для Q# или классической основной программы, написанной на Python или одном из языков .NET.</span><span class="sxs-lookup"><span data-stu-id="84440-108">[Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs): describes how a Q# program is run, and provides an overview of the various ways you can call the program: from the command line, in Q# Jupyter Notebooks, or from a classical host program written in Python or a .NET language.</span></span>

### <a name="no-locq-language"></a><span data-ttu-id="84440-109">Язык Q#</span><span class="sxs-lookup"><span data-stu-id="84440-109">Q# Language</span></span>

- <span data-ttu-id="84440-110">[Типы в Q#.](xref:microsoft.quantum.guide.types) Описание модели типов в Q#, а также синтаксиса для определения типов и работы с ними.</span><span class="sxs-lookup"><span data-stu-id="84440-110">[Types in Q#](xref:microsoft.quantum.guide.types): Lays out the Q# type model and describes the syntax for specifying and working with types.</span></span>

- <span data-ttu-id="84440-111">[Выражения типа.](xref:microsoft.quantum.guide.expressions) Сведения о том, как определять, указывать и объединять каждый из типов в Q#, а также работать с их значениями.</span><span class="sxs-lookup"><span data-stu-id="84440-111">[Type Expressions](xref:microsoft.quantum.guide.expressions): Details how to specify, reference, combine, and operate on values of each type in Q#.</span></span> 

### <a name="using-no-locq"></a><span data-ttu-id="84440-112">Использование Q#</span><span class="sxs-lookup"><span data-stu-id="84440-112">Using Q#</span></span>

- <span data-ttu-id="84440-113">[Структура файлаQ#.](xref:microsoft.quantum.guide.filestructure) Описание структуры и синтаксиса файла `*.qs` в Q#.</span><span class="sxs-lookup"><span data-stu-id="84440-113">[Q# File Structure](xref:microsoft.quantum.guide.filestructure): Describes the structure and syntax of a `*.qs` Q# file.</span></span>

- <span data-ttu-id="84440-114">[Операции и функции.](xref:microsoft.quantum.guide.operationsfunctions) Подробное описание двух вызываемых типов в языке Q#: *operations* для действий с регистрами кубитов и *functions* — исключительно для работы с классическими данными.</span><span class="sxs-lookup"><span data-stu-id="84440-114">[Operations and Functions](xref:microsoft.quantum.guide.operationsfunctions): Details the two callable types of the Q# language: *operations*, which include action on qubit registers, and *functions*, which strictly work with classical information.</span></span> 
    <span data-ttu-id="84440-115">Здесь также описано, как определять и вызывать эти типы, в том числе сопряженные и контролируемые версии квантовых операций.</span><span class="sxs-lookup"><span data-stu-id="84440-115">Here you see how to define and call them, including the adjoint and controlled versions of quantum operations.</span></span>

- <span data-ttu-id="84440-116">[Переменные](xref:microsoft.quantum.guide.variables). Описание роли переменных в программах на Q# и их эффективного использования.</span><span class="sxs-lookup"><span data-stu-id="84440-116">[Variables](xref:microsoft.quantum.guide.variables): Describes the role of variables within Q# programs and how to leverage them effectively.</span></span> 
    <span data-ttu-id="84440-117">В частности, вы найдете здесь сведения об областях привязки, узнаете разницу между неизменяемыми и изменяемыми переменными, а также научитесь назначать или переназначать их.</span><span class="sxs-lookup"><span data-stu-id="84440-117">For example, you can find information about binding scopes, as well as the difference between immutable and mutable variables and how to assign or re-assign them.</span></span>

- <span data-ttu-id="84440-118">[Работа с кубитами.](xref:microsoft.quantum.guide.qubits) Описание функций Q#, предназначенных для отдельных кубитов и систем кубитов, в частности для их подготовки, выполнения операций с ними и их измерения.</span><span class="sxs-lookup"><span data-stu-id="84440-118">[Working with qubits](xref:microsoft.quantum.guide.qubits): Describes the features of Q# used to address individual qubits and systems of qubits, specifically, allocating them, performing operations on them, and measuring them.</span></span> 

- <span data-ttu-id="84440-119">[Поток управления.](xref:microsoft.quantum.guide.controlflow) Подробные сведения о шаблонах программных потоков управления, доступных в Q#, включая множество стандартных методов (например, условная обработка, циклы *for* и *while*), а также специальном шаблоне квантовых вычислений *Repeat-Until-Success* (повторять до успешного выполнения).</span><span class="sxs-lookup"><span data-stu-id="84440-119">[Control Flow](xref:microsoft.quantum.guide.controlflow): Details the programming control flow patterns available in Q#, which includes many standard techniques (such as conditional processing, *for* loops, *while* loops) as well as the quantum-specific *Repeat-Until-Success* pattern.</span></span>

- <span data-ttu-id="84440-120">[Тестирование и отладка.](xref:microsoft.quantum.guide.testingdebugging) Подробное описание некоторых способов контроля правильности выполнения кода.</span><span class="sxs-lookup"><span data-stu-id="84440-120">[Testing and debugging](xref:microsoft.quantum.guide.testingdebugging): Details some techniques for making sure your code is doing what it is supposed to do.</span></span> 
    <span data-ttu-id="84440-121">В связи с общей непрозрачностью квантовой информации, отладка квантовой программы может потребовать специальных методов.</span><span class="sxs-lookup"><span data-stu-id="84440-121">Due to the general opacity of quantum information, debugging a quantum program can require specialized techniques.</span></span> 
    <span data-ttu-id="84440-122">К счастью, Q# поддерживает многие классические методы отладки, привычные для программистов, а также методы, характерные для квантовых вычислений.</span><span class="sxs-lookup"><span data-stu-id="84440-122">Fortunately, Q# supports many of the classical debugging techniques programmers are familiar with, as well as those that are quantum-specific.</span></span> <span data-ttu-id="84440-123">К ним относятся создание и запуск модульных тестов в Q#, встраивание *операторов утверждений* в значения и вероятности в коде, а также функции `Dump`, которые выводят сведения о состоянии целевых компьютеров.</span><span class="sxs-lookup"><span data-stu-id="84440-123">These include creating and running unit tests in Q#, embedding *assertions* on values and probabilities in your code, and the `Dump` functions which output the states of target machines.</span></span> 
    <span data-ttu-id="84440-124">Второй способ можно использовать наряду с нашим полнофункциональным симулятором для отладки определенных частей вычислений, обходя некоторые квантовые ограничения, например [теорему о запрете клонирования](xref:microsoft.quantum.concepts.pauli).</span><span class="sxs-lookup"><span data-stu-id="84440-124">The latter can be used alongside our full-state simulator to debug certain parts of computations by skirting some quantum limitations, for example, the [no-cloning theorem](xref:microsoft.quantum.concepts.pauli).</span></span>

### <a name="quantum-simulators-and-resource-estimators"></a><span data-ttu-id="84440-125">Квантовые симуляторы и средства оценки ресурсов</span><span class="sxs-lookup"><span data-stu-id="84440-125">Quantum Simulators and Resource Estimators</span></span>

- <span data-ttu-id="84440-126">[Квантовые симуляторы и ведущие приложения.](xref:microsoft.quantum.machines) Обзор доступных симуляторов и общей модели выполнения между основными программами и целевыми компьютерами.</span><span class="sxs-lookup"><span data-stu-id="84440-126">[Quantum simulators and host applications](xref:microsoft.quantum.machines): An overview of the different simulators available, as well as the general run model between host programs and target machines.</span></span>

- <span data-ttu-id="84440-127">[Симулятор полного состояния.](xref:microsoft.quantum.machines.full-state-simulator) Целевой компьютер, имитирующий полное квантовое состояние.</span><span class="sxs-lookup"><span data-stu-id="84440-127">[Full state simulator](xref:microsoft.quantum.machines.full-state-simulator): The target machine which simulates the full quantum state.</span></span> <span data-ttu-id="84440-128">Используется для выполнения или отладки программ небольшого размера (менее нескольких десятков кубит) в полном объеме.</span><span class="sxs-lookup"><span data-stu-id="84440-128">Useful for fully running or debugging smaller-scale programs (less than a few dozen qubits)</span></span>

- <span data-ttu-id="84440-129">[Оценщик ресурсов.](xref:microsoft.quantum.machines.resources-estimator) Оценивает потребность в ресурсах для выполнения определенного экземпляра операции Q# на квантовом компьютере.</span><span class="sxs-lookup"><span data-stu-id="84440-129">[Resources estimator](xref:microsoft.quantum.machines.resources-estimator): Estimates the resources required to run a given instance of a Q# operation on a quantum computer.</span></span>

- <span data-ttu-id="84440-130">[Симулятор трассировки.](xref:microsoft.quantum.machines.qc-trace-simulator.intro) Выполняет квантовую программу без фактической имитации состояния квантового компьютера. Это обеспечивает возможность работы квантовых программ с несколькими тысячами кубит.</span><span class="sxs-lookup"><span data-stu-id="84440-130">[Trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro): Runs a quantum program without actually simulating the state of a quantum computer, and therefore can run quantum programs that use thousands of qubits.</span></span> <span data-ttu-id="84440-131">Используется для отладки классического кода в квантовой программе, а также для оценки требуемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="84440-131">Useful for debugging classical code within a quantum program, as well as estimating resources required.</span></span>

- <span data-ttu-id="84440-132">[Симулятор Тоффоли.](xref:microsoft.quantum.machines.toffoli-simulator) Специализированный программный симулятор квантового состояния, который использоваться с миллионами кубитов, но только для программ с ограниченным набором квантовых операций: X, CNOT и X с множественным управлением.</span><span class="sxs-lookup"><span data-stu-id="84440-132">[Toffoli simulator](xref:microsoft.quantum.machines.toffoli-simulator): A special-purpose quantum simulator that can be used with millions of qubits, but only for programs with a restricted set of quantum operations - X, CNOT, and multi-controlled X.</span></span>

### <a name="quick-reference-pages"></a><span data-ttu-id="84440-133">Краткое справочное руководство</span><span class="sxs-lookup"><span data-stu-id="84440-133">Quick Reference Pages</span></span>

- <span data-ttu-id="84440-134">[Магические команды IQ#.](xref:microsoft.quantum.guide.quickref.iqsharp) Краткая справочная информация о магических командах IQ# в Jupyter Notebook для Q#.</span><span class="sxs-lookup"><span data-stu-id="84440-134">[IQ# Magic Commands](xref:microsoft.quantum.guide.quickref.iqsharp): Quick reference page for IQ# magic commands within Q# Jupyter Notebooks.</span></span>
