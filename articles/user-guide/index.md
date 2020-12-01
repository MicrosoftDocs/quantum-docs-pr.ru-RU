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
ms.openlocfilehash: 979e468cc743bd9125eaba0b71f794977c914447
ms.sourcegitcommit: b930bb59a1ba8f41d2edc9ed98197109aa8c7f1b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96231763"
---
# <a name="the-no-locq-user-guide"></a><span data-ttu-id="c8e4f-103">Руководство пользователя по Q#</span><span class="sxs-lookup"><span data-stu-id="c8e4f-103">The Q# User Guide</span></span>

<span data-ttu-id="c8e4f-104">Перед вами руководство пользователя по Q#.</span><span class="sxs-lookup"><span data-stu-id="c8e4f-104">Welcome to the Q# User Guide!</span></span> 

<span data-ttu-id="c8e4f-105">В нем приведены общие сведения о разработке квантовых программ с использованием Q#.</span><span class="sxs-lookup"><span data-stu-id="c8e4f-105">In the different topics of this guide, we introduce some of the basics for developing quantum programs using Q#.</span></span>

<span data-ttu-id="c8e4f-106">Ссылки на полную спецификацию и документацию по квантовому языку программирования Q# см. в [руководстве по языку Q#](xref:microsoft.quantum.qsharp.index).</span><span class="sxs-lookup"><span data-stu-id="c8e4f-106">We refer to the [Q# language guide](xref:microsoft.quantum.qsharp.index) for a full specification and documentation of the Q# quantum programming language.</span></span> 

## <a name="user-guide-contents"></a><span data-ttu-id="c8e4f-107">Содержимое руководства пользователя</span><span class="sxs-lookup"><span data-stu-id="c8e4f-107">User Guide Contents</span></span>

- <span data-ttu-id="c8e4f-108">[Программы на Q#](xref:microsoft.quantum.guide.programs) — краткое введение в квантовые программы на Q#.</span><span class="sxs-lookup"><span data-stu-id="c8e4f-108">[Q# programs](xref:microsoft.quantum.guide.programs): An quick introduction to quantum programs in Q#.</span></span> 

- <span data-ttu-id="c8e4f-109">[Способы запуска программы на Q#.](xref:microsoft.quantum.guide.host-programs) Здесь описывается ход выполнения программы на Q#, а также приводится обзор разных способов, с помощью которых ее можно вызвать: из командной строки, Jupyter Notebook для Q# или классической основной программы, написанной на Python или одном из языков .NET.</span><span class="sxs-lookup"><span data-stu-id="c8e4f-109">[Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs): describes how a Q# program is run, and provides an overview of the various ways you can call the program: from the command line, in Q# Jupyter Notebooks, or from a classical host program written in Python or a .NET language.</span></span>

- <span data-ttu-id="c8e4f-110">[Тестирование и отладка.](xref:microsoft.quantum.guide.testingdebugging) Подробное описание некоторых способов контроля правильности выполнения кода.</span><span class="sxs-lookup"><span data-stu-id="c8e4f-110">[Testing and debugging](xref:microsoft.quantum.guide.testingdebugging): Details some techniques for making sure your code is doing what it is supposed to do.</span></span> 
    <span data-ttu-id="c8e4f-111">В связи с общей непрозрачностью квантовой информации, отладка квантовой программы может потребовать специальных методов.</span><span class="sxs-lookup"><span data-stu-id="c8e4f-111">Due to the general opacity of quantum information, debugging a quantum program can require specialized techniques.</span></span> 
    <span data-ttu-id="c8e4f-112">К счастью, Q# поддерживает многие классические методы отладки, привычные для программистов, а также методы, характерные для квантовых вычислений.</span><span class="sxs-lookup"><span data-stu-id="c8e4f-112">Fortunately, Q# supports many of the classical debugging techniques programmers are familiar with, as well as those that are quantum-specific.</span></span> <span data-ttu-id="c8e4f-113">К ним относятся создание и запуск модульных тестов в Q#, встраивание *операторов утверждений* в значения и вероятности в коде, а также функции `Dump`, которые выводят сведения о состоянии целевых компьютеров.</span><span class="sxs-lookup"><span data-stu-id="c8e4f-113">These include creating and running unit tests in Q#, embedding *assertions* on values and probabilities in your code, and the `Dump` functions which output the states of target machines.</span></span> 
    <span data-ttu-id="c8e4f-114">Второй способ можно использовать наряду с нашим полнофункциональным симулятором для отладки определенных частей вычислений, обходя некоторые квантовые ограничения, например [теорему о запрете клонирования](xref:microsoft.quantum.concepts.pauli).</span><span class="sxs-lookup"><span data-stu-id="c8e4f-114">The latter can be used alongside our full-state simulator to debug certain parts of computations by skirting some quantum limitations, for example, the [no-cloning theorem](xref:microsoft.quantum.concepts.pauli).</span></span>

### <a name="quantum-simulators-and-resource-estimators"></a><span data-ttu-id="c8e4f-115">Квантовые симуляторы и средства оценки ресурсов</span><span class="sxs-lookup"><span data-stu-id="c8e4f-115">Quantum Simulators and Resource Estimators</span></span>

- <span data-ttu-id="c8e4f-116">[Квантовые симуляторы и ведущие приложения.](xref:microsoft.quantum.machines) Обзор доступных симуляторов и способа взаимодействия основных программ и целевых компьютеров для выполнения программ Q#.</span><span class="sxs-lookup"><span data-stu-id="c8e4f-116">[Quantum simulators and host applications](xref:microsoft.quantum.machines): An overview of the different simulators available, as well of how host programs and target machines work together to run Q# programs.</span></span>

- <span data-ttu-id="c8e4f-117">[Симулятор полного состояния.](xref:microsoft.quantum.machines.full-state-simulator) Целевой компьютер, имитирующий полное квантовое состояние.</span><span class="sxs-lookup"><span data-stu-id="c8e4f-117">[Full state simulator](xref:microsoft.quantum.machines.full-state-simulator): The target machine which simulates the full quantum state.</span></span> <span data-ttu-id="c8e4f-118">Используется для выполнения или отладки программ небольшого размера (менее нескольких десятков кубит) в полном объеме.</span><span class="sxs-lookup"><span data-stu-id="c8e4f-118">Useful for fully running or debugging smaller-scale programs (less than a few dozen qubits)</span></span>

- <span data-ttu-id="c8e4f-119">[Оценщик ресурсов.](xref:microsoft.quantum.machines.resources-estimator) Оценивает потребность в ресурсах для выполнения определенного экземпляра операции Q# на квантовом компьютере.</span><span class="sxs-lookup"><span data-stu-id="c8e4f-119">[Resources estimator](xref:microsoft.quantum.machines.resources-estimator): Estimates the resources required to run a given instance of a Q# operation on a quantum computer.</span></span>

- <span data-ttu-id="c8e4f-120">[Симулятор трассировки.](xref:microsoft.quantum.machines.qc-trace-simulator.intro) Выполняет квантовую программу без фактической имитации состояния квантового компьютера. Это обеспечивает возможность работы квантовых программ с несколькими тысячами кубит.</span><span class="sxs-lookup"><span data-stu-id="c8e4f-120">[Trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro): Runs a quantum program without actually simulating the state of a quantum computer, and therefore can run quantum programs that use thousands of qubits.</span></span> <span data-ttu-id="c8e4f-121">Используется для отладки классического кода в квантовой программе, а также для оценки требуемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c8e4f-121">Useful for debugging classical code within a quantum program, as well as estimating resources required.</span></span>

- <span data-ttu-id="c8e4f-122">[Симулятор Тоффоли.](xref:microsoft.quantum.machines.toffoli-simulator) Специализированный программный симулятор квантового состояния, который использоваться с миллионами кубитов, но только для программ с ограниченным набором квантовых операций: X, CNOT и X с множественным управлением.</span><span class="sxs-lookup"><span data-stu-id="c8e4f-122">[Toffoli simulator](xref:microsoft.quantum.machines.toffoli-simulator): A special-purpose quantum simulator that can be used with millions of qubits, but only for programs with a restricted set of quantum operations - X, CNOT, and multi-controlled X.</span></span>

### <a name="quick-reference-pages"></a><span data-ttu-id="c8e4f-123">Краткое справочное руководство</span><span class="sxs-lookup"><span data-stu-id="c8e4f-123">Quick Reference Pages</span></span>

- <span data-ttu-id="c8e4f-124">[Магические команды IQ#.](xref:microsoft.quantum.guide.quickref.iqsharp) Краткая справочная информация о магических командах IQ# в Jupyter Notebook для Q#.</span><span class="sxs-lookup"><span data-stu-id="c8e4f-124">[IQ# Magic Commands](xref:microsoft.quantum.guide.quickref.iqsharp): Quick reference page for IQ# magic commands within Q# Jupyter Notebooks.</span></span>
