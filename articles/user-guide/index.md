---
title: Руководство пользователя Q#
description: Общие сведения о назначении и содержимом этого руководства пользователя
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide
ms.openlocfilehash: c5611f3e2907791f2dfc1644be0a45515d50dfd7
ms.sourcegitcommit: af10179284967bd7a72a52ae7e1c4da65c7d128d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "85415376"
---
# <a name="the-q-user-guide"></a><span data-ttu-id="a82b3-103">Руководство пользователя Q#</span><span class="sxs-lookup"><span data-stu-id="a82b3-103">The Q# User Guide</span></span>

<span data-ttu-id="a82b3-104">Перед вами руководство пользователя по Q#.</span><span class="sxs-lookup"><span data-stu-id="a82b3-104">Welcome to the Q# User Guide!</span></span> 

<span data-ttu-id="a82b3-105">В различных статьях в рамках этого руководства мы подробно рассмотрим основные понятия языка Q# и все, что вам потребуется для написания квантовых программ.</span><span class="sxs-lookup"><span data-stu-id="a82b3-105">In the different topics of this guide, we detail the core concepts of the Q# language and all the information you need to write quantum programs.</span></span>

## <a name="user-guide-contents"></a><span data-ttu-id="a82b3-106">Содержимое руководства пользователя</span><span class="sxs-lookup"><span data-stu-id="a82b3-106">User Guide Contents</span></span>

- <span data-ttu-id="a82b3-107">[Основы Q#.](xref:microsoft.quantum.guide.basics) Вводные сведения о назначении и функциональных возможностях языка Q#.</span><span class="sxs-lookup"><span data-stu-id="a82b3-107">[Q# Basics](xref:microsoft.quantum.guide.basics): An introductory overview of the purpose and functionality of the Q# programming language.</span></span> 

### <a name="q-language"></a><span data-ttu-id="a82b3-108">Язык Q#</span><span class="sxs-lookup"><span data-stu-id="a82b3-108">Q# Language</span></span>

- <span data-ttu-id="a82b3-109">[Типы в Q#.](xref:microsoft.quantum.guide.types) Описание модели типов в Q#, а также синтаксиса для определения типов и работы с ними.</span><span class="sxs-lookup"><span data-stu-id="a82b3-109">[Types in Q#](xref:microsoft.quantum.guide.types): Lays out the Q# type model and describes the syntax for specifying and working with types.</span></span>

- <span data-ttu-id="a82b3-110">[Выражения типа.](xref:microsoft.quantum.guide.expressions) Сведения о том, как определять, указывать и объединять каждый из типов в Q#, а также работать с их значениями.</span><span class="sxs-lookup"><span data-stu-id="a82b3-110">[Type Expressions](xref:microsoft.quantum.guide.expressions): Details how to specify, reference, combine, and operate on values of each type in Q#.</span></span> 

### <a name="using-q"></a><span data-ttu-id="a82b3-111">Использование Q#</span><span class="sxs-lookup"><span data-stu-id="a82b3-111">Using Q#</span></span>

- <span data-ttu-id="a82b3-112">[Структура файла Q#.](xref:microsoft.quantum.guide.filestructure) Описание структуры и синтаксиса файла `*.qs` в Q#.</span><span class="sxs-lookup"><span data-stu-id="a82b3-112">[Q# File Structure](xref:microsoft.quantum.guide.filestructure): Describes the structure and syntax of a `*.qs` Q# file.</span></span>

- <span data-ttu-id="a82b3-113">[Операции и функции.](xref:microsoft.quantum.guide.operationsfunctions) Подробное описание двух вызываемых типов в языке Q#: *operations* для действий с регистрами кубитов и *functions* — исключительно для работы с классическими данными.</span><span class="sxs-lookup"><span data-stu-id="a82b3-113">[Operations and Functions](xref:microsoft.quantum.guide.operationsfunctions): Details the two callable types of the Q# language: *operations*, which include action on qubit registers, and *functions*, which strictly work with classical information.</span></span> 
    <span data-ttu-id="a82b3-114">Здесь также описано, как определять и вызывать эти типы, в том числе сопряженные и контролируемые версии квантовых операций.</span><span class="sxs-lookup"><span data-stu-id="a82b3-114">Here you see how to define and call them, including the adjoint and controlled versions of quantum operations.</span></span>

- <span data-ttu-id="a82b3-115">[Переменные](xref:microsoft.quantum.guide.variables). Описание роли переменных в программах на Q# и их эффективного использования.</span><span class="sxs-lookup"><span data-stu-id="a82b3-115">[Variables](xref:microsoft.quantum.guide.variables): Describes the role of variables within Q# programs and how to leverage them effectively.</span></span> 
    <span data-ttu-id="a82b3-116">В частности, вы найдете здесь сведения об областях привязки, узнаете разницу между неизменяемыми и изменяемыми переменными, а также научитесь назначать или переназначать их.</span><span class="sxs-lookup"><span data-stu-id="a82b3-116">For example, you can find information about binding scopes, as well as the difference between immutable and mutable variables and how to assign or re-assign them.</span></span>

- <span data-ttu-id="a82b3-117">[Работа с кубитами.](xref:microsoft.quantum.guide.qubits) Описание функций Q#, предназначенных для отдельных кубитов и систем кубитов, в частности для их выделения, выполнения операций с ними и их измерения.</span><span class="sxs-lookup"><span data-stu-id="a82b3-117">[Working with qubits](xref:microsoft.quantum.guide.qubits): Describes the features of Q# used to address individual qubits and systems of qubits, specifically, allocating them, performing operations on them, and measuring them.</span></span> 

- <span data-ttu-id="a82b3-118">[Поток управления.](xref:microsoft.quantum.guide.controlflow) Подробные сведения о шаблонах программных потоков управления, доступных в Q#, включая множество стандартных методов (например, условное выполнение, циклы for и while), а также специальном шаблоне квантовых вычислений "повторять до успешного выполнения".</span><span class="sxs-lookup"><span data-stu-id="a82b3-118">[Control Flow](xref:microsoft.quantum.guide.controlflow): Details the programming control flow patterns available in Q#, which includes many standard techniques (such as conditional execution, for loops, while loops) as well as the quantum-specific "Repeat-Until-Success" pattern.</span></span>

- <span data-ttu-id="a82b3-119">[Тестирование и отладка.](xref:microsoft.quantum.guide.testingdebugging) Подробное описание некоторых способов контроля правильности выполнения кода.</span><span class="sxs-lookup"><span data-stu-id="a82b3-119">[Testing and debugging](xref:microsoft.quantum.guide.testingdebugging): Details some techniques for making sure your code is doing what it is supposed to do.</span></span> 
    <span data-ttu-id="a82b3-120">В связи с общей непрозрачностью квантовой информации, отладка квантовой программы может потребовать специальных методов.</span><span class="sxs-lookup"><span data-stu-id="a82b3-120">Due to the general opacity of quantum information, debugging a quantum program can require specialized techniques.</span></span> 
    <span data-ttu-id="a82b3-121">К счастью, Q# поддерживает многие классические методы отладки, привычные для программистов, а также методы, характерные для квантовых вычислений.</span><span class="sxs-lookup"><span data-stu-id="a82b3-121">Fortunately, Q# supports many of the classical debugging techniques programmers are familiar with, as well as those that are quantum-specific.</span></span> <span data-ttu-id="a82b3-122">К ним относятся создание и запуск модульных тестов в Q#, встраивание *операторов утверждений* в значения и вероятности в коде, а также функции `Dump`, которые выводят сведения о состоянии целевых компьютеров.</span><span class="sxs-lookup"><span data-stu-id="a82b3-122">These include creating and running unit tests in Q#, embedding *assertions* on values and probabilities in your code, and the `Dump` functions which output the states of target machines.</span></span> 
    <span data-ttu-id="a82b3-123">Второй способ можно использовать наряду с нашим полнофункциональным симулятором для отладки определенных частей вычислений, обходя некоторые квантовые ограничения, например [теорему о запрете клонирования](xref:microsoft.quantum.concepts.pauli).</span><span class="sxs-lookup"><span data-stu-id="a82b3-123">The latter can be used alongside our full-state simulator to debug certain parts of computations by skirting some quantum limitations, for example, the [no-cloning theorem](xref:microsoft.quantum.concepts.pauli).</span></span>

### <a name="quantum-simulators-and-resource-estimators"></a><span data-ttu-id="a82b3-124">Квантовые симуляторы и средства оценки ресурсов</span><span class="sxs-lookup"><span data-stu-id="a82b3-124">Quantum Simulators and Resource Estimators</span></span>

- <span data-ttu-id="a82b3-125">[Квантовые симуляторы и ведущие приложения.](xref:microsoft.quantum.machines) Обзор различных доступных симуляторов и общей модели выполнения между ведущими приложениями и целевыми компьютерами.</span><span class="sxs-lookup"><span data-stu-id="a82b3-125">[Quantum simulators and host applications](xref:microsoft.quantum.machines): An overview of the different simulators available, as well as the general execution model between host programs and target machines.</span></span>

- <span data-ttu-id="a82b3-126">[Симулятор полного состояния.](xref:microsoft.quantum.machines.full-state-simulator) Целевой компьютер, имитирующий полное квантовое состояние.</span><span class="sxs-lookup"><span data-stu-id="a82b3-126">[Full state simulator](xref:microsoft.quantum.machines.full-state-simulator): The target machine which simulates the full quantum state.</span></span> <span data-ttu-id="a82b3-127">Используется для выполнения или отладки программ небольшого размера (менее нескольких десятков кубитов) в полном объеме.</span><span class="sxs-lookup"><span data-stu-id="a82b3-127">Useful for fully executing or debugging smaller-scale programs (less than a few dozen qubits)</span></span>

- <span data-ttu-id="a82b3-128">[Оценщик ресурсов.](xref:microsoft.quantum.machines.resources-estimator) Оценивает потребность в ресурсах для выполнения определенного экземпляра операции Q# на квантовом компьютере.</span><span class="sxs-lookup"><span data-stu-id="a82b3-128">[Resources estimator](xref:microsoft.quantum.machines.resources-estimator): Estimates the resources required to run a given instance of a Q# operation on a quantum computer.</span></span>

- <span data-ttu-id="a82b3-129">[Симулятор трассировки.](xref:microsoft.quantum.machines.qc-trace-simulator.intro) Выполняет квантовую программу без фактической имитации состояния квантового компьютера. Это обеспечивает возможность работы квантовых программ с несколькими тысячами кубитов.</span><span class="sxs-lookup"><span data-stu-id="a82b3-129">[Trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro): Executes a quantum program without actually simulating the state of a quantum computer, and therefore can execute quantum programs that use thousands of qubits.</span></span> <span data-ttu-id="a82b3-130">Используется для отладки классического кода в квантовой программе, а также для оценки требуемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a82b3-130">Useful for debugging classical code within a quantum program, as well as estimating resources required.</span></span>

- <span data-ttu-id="a82b3-131">[Симулятор Тоффоли.](xref:microsoft.quantum.machines.toffoli-simulator) Специализированный программный симулятор квантового состояния, который использоваться с миллионами кубитов, но только для программ с ограниченным набором квантовых операций: X, CNOT и X с множественным управлением.</span><span class="sxs-lookup"><span data-stu-id="a82b3-131">[Toffoli simulator](xref:microsoft.quantum.machines.toffoli-simulator): A special-purpose quantum simulator that can be used with millions of qubits, but only for programs with a restricted set of quantum operations - X, CNOT, and multi-controlled X.</span></span>

### <a name="quick-reference-pages"></a><span data-ttu-id="a82b3-132">Краткое справочное руководство</span><span class="sxs-lookup"><span data-stu-id="a82b3-132">Quick Reference Pages</span></span>

- <span data-ttu-id="a82b3-133">[Магические команды IQ#](xref:microsoft.quantum.guide.quickref.iqsharp) Краткая справочная информация о магических командах IQ# в Jupyter Notebook для Q#.</span><span class="sxs-lookup"><span data-stu-id="a82b3-133">[IQ# Magic Commands](xref:microsoft.quantum.guide.quickref.iqsharp): Quick reference page for IQ# magic commands within Q# Jupyter Notebooks.</span></span>
