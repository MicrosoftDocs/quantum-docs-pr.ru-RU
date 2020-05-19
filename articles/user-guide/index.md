---
title: Руководство пользователя Q#
description: Общие сведения о назначении и содержимом этого руководства пользователя
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide
ms.openlocfilehash: f535aaedbe6ce181375d48f7023409ad8212c702
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2020
ms.locfileid: "83430617"
---
# <a name="the-q-user-guide"></a><span data-ttu-id="fd0f4-103">Руководство пользователя Q#</span><span class="sxs-lookup"><span data-stu-id="fd0f4-103">The Q# User Guide</span></span>

<span data-ttu-id="fd0f4-104">Перед вами руководство пользователя по Q#.</span><span class="sxs-lookup"><span data-stu-id="fd0f4-104">Welcome to the Q# User Guide!</span></span> 

<span data-ttu-id="fd0f4-105">Здесь мы подробно рассмотрим основные понятия языка Q # и все, что вам потребуется для написания квантовых программ.</span><span class="sxs-lookup"><span data-stu-id="fd0f4-105">Here we detail the core concepts of the Q# language and all the information you need to write quantum programs.</span></span>

## <a name="user-guide-contents"></a><span data-ttu-id="fd0f4-106">Содержимое руководства пользователя</span><span class="sxs-lookup"><span data-stu-id="fd0f4-106">User Guide Contents</span></span>

- <span data-ttu-id="fd0f4-107">[Основы Q#](xref:microsoft.quantum.guide.basics). Вводные сведения о назначении и функциональных возможностях языка программирования Q#.</span><span class="sxs-lookup"><span data-stu-id="fd0f4-107">[Q# Basics](xref:microsoft.quantum.guide.basics): an introductory overview of the purpose and functionality of the Q# programming language.</span></span> 

### <a name="q-language"></a><span data-ttu-id="fd0f4-108">Язык Q#</span><span class="sxs-lookup"><span data-stu-id="fd0f4-108">Q# Language</span></span>

- <span data-ttu-id="fd0f4-109">[Типы в Q#](xref:microsoft.quantum.guide.types). Описание модели типов в Q# и синтаксиса для определения типов и работы с ними.</span><span class="sxs-lookup"><span data-stu-id="fd0f4-109">[Types in Q#](xref:microsoft.quantum.guide.types): lays out the Q# type model and describes the syntax for specifying and working with types.</span></span>

- <span data-ttu-id="fd0f4-110">[Выражения типов](xref:microsoft.quantum.guide.expressions). Сведения о том, как определять, использовать и объединять каждый из типов в Q#, а также работать с их значениями.</span><span class="sxs-lookup"><span data-stu-id="fd0f4-110">[Type Expressions](xref:microsoft.quantum.guide.expressions): details how to specify, reference, combine, and operate on values of each type in Q#.</span></span> 

### <a name="using-q"></a><span data-ttu-id="fd0f4-111">Использование Q#</span><span class="sxs-lookup"><span data-stu-id="fd0f4-111">Using Q#</span></span>

- <span data-ttu-id="fd0f4-112">[Структура файла Q#.](xref:microsoft.quantum.guide.filestructure) Описание структуры и синтаксиса файла `*.qs` Q#.</span><span class="sxs-lookup"><span data-stu-id="fd0f4-112">[Q# File Structure](xref:microsoft.quantum.guide.filestructure): describes the structure and syntax of a `*.qs` Q# file.</span></span>

- <span data-ttu-id="fd0f4-113">[Операции и функции.](xref:microsoft.quantum.guide.operationsfunctions) Подробное описание двух вызываемых типов в языке Q#: *операции* для действий над кубитами и квантовыми системами и *функции* строго для работы с классическими данными.</span><span class="sxs-lookup"><span data-stu-id="fd0f4-113">[Operations and Functions](xref:microsoft.quantum.guide.operationsfunctions): details the two callable types of the Q# language: *operations*, which include action on qubit registers and *functions*, which strictly work with classical information.</span></span> 
    <span data-ttu-id="fd0f4-114">Здесь также описано, как определять и вызывать эти типы, в том числе сопряженные и контролируемые версии квантовых операций.</span><span class="sxs-lookup"><span data-stu-id="fd0f4-114">Here you see how to define and call them, including the adjoint and controlled versions of quantum operations.</span></span>

- <span data-ttu-id="fd0f4-115">[Локальные переменные.](xref:microsoft.quantum.guide.variables) Описание роли переменных в программах на Q# и способа их эффективного использования.</span><span class="sxs-lookup"><span data-stu-id="fd0f4-115">[Variables](xref:microsoft.quantum.guide.variables): describes the role of variables within Q# programs and how to leverage them effectively.</span></span> 
    <span data-ttu-id="fd0f4-116">В частности, вы найдете здесь сведения об областях привязки, узнаете разницу между неизменяемыми и изменяемыми переменными, а также научитесь назначать и переназначать их.</span><span class="sxs-lookup"><span data-stu-id="fd0f4-116">For example, you can find information about binding scopes, as well as the difference between immutable/mutable variables and how to assign/re-assign them.</span></span>

- <span data-ttu-id="fd0f4-117">[Работа с кубитами.](xref:microsoft.quantum.guide.qubits) Описание функций Q#, которые можно применять к отдельным кубитам и системам кубитов.</span><span class="sxs-lookup"><span data-stu-id="fd0f4-117">[Working with qubits](xref:microsoft.quantum.guide.qubits): describes the features of Q# used to address individual qubits and systems of qubits.</span></span> 
    <span data-ttu-id="fd0f4-118">В частности, это влечет за собой их распределение, выполнение операций над ними и, в конечном счете, их измерение.</span><span class="sxs-lookup"><span data-stu-id="fd0f4-118">Specifically, that entails their allocation, performing operations on them, and ultimately their measurement.</span></span> 

- <span data-ttu-id="fd0f4-119">[Поток управления.](xref:microsoft.quantum.guide.controlflow) Подробные сведения о шаблонах программных потоков управления, доступных в Q#, включая множество стандартных методов (условное выполнение, циклы for и while и т. д.), а также специальном шаблоне квантовых вычислений "повторять до успешного выполнения".</span><span class="sxs-lookup"><span data-stu-id="fd0f4-119">[Control Flow](xref:microsoft.quantum.guide.controlflow): details the programming control flow patterns available in Q#, which includes many standard techniques (conditional execution, for loops, while loops, etc.) as well as the quantum-specific "Repeat-Until-Success" pattern.</span></span>

- <span data-ttu-id="fd0f4-120">[Тестирование и отладка.](xref:microsoft.quantum.guide.testingdebugging) Подробное описание некоторых способов контроля правильности выполнения кода.</span><span class="sxs-lookup"><span data-stu-id="fd0f4-120">[Testing and debugging](xref:microsoft.quantum.guide.testingdebugging): details some techniques for making sure your code is doing what it is supposed to do.</span></span> 
    <span data-ttu-id="fd0f4-121">В связи с общей непрозрачностью квантовой информации, отладка квантовой программы может потребовать специальных методов.</span><span class="sxs-lookup"><span data-stu-id="fd0f4-121">Due to the general opacity of quantum information, debugging a quantum program can require specialized techniques.</span></span> 
    <span data-ttu-id="fd0f4-122">К счастью, Q# поддерживает многие классические методы отладки, к которым привыкли программисты, а также квантово-специфические методы.</span><span class="sxs-lookup"><span data-stu-id="fd0f4-122">Fortunately, Q# supports many of the classical debugging techniques programmers are used to, as well as those that are quantum-specific.</span></span> <span data-ttu-id="fd0f4-123">К ним относятся создание и запуск модульных тестов в Q#, встраивание *операторов утверждений* к значениям и вероятностям в коде, а также функции `Dump`, которые выводят состояние целевого компьютера.</span><span class="sxs-lookup"><span data-stu-id="fd0f4-123">These include creating/running unit tests in Q#, embedding *assertions* on values and probabilities in your code, and the `Dump` functions which output the state of target machine.</span></span> 
    <span data-ttu-id="fd0f4-124">Второй способ можно использовать наряду с нашим полнофункциональным симулятором для отладки некоторых частей вычислений, обходя некоторые квантовые ограничения (такие как теорема о запрете клонирования).</span><span class="sxs-lookup"><span data-stu-id="fd0f4-124">The latter can be used alongside our full-state simulator to debug certain parts of computations by skirting some quantum limitations (e.g. the no-cloning theorem).</span></span>

### <a name="quantum-simulators-and-resource-estimators"></a><span data-ttu-id="fd0f4-125">Квантовые симуляторы и средства оценки ресурсов</span><span class="sxs-lookup"><span data-stu-id="fd0f4-125">Quantum Simulators and Resource Estimators</span></span>

- <span data-ttu-id="fd0f4-126">[Квантовые симуляторы и основные приложения.](xref:microsoft.quantum.machines) Обзор доступных симуляторов и общей модели выполнения между основным приложением и целевыми компьютерами.</span><span class="sxs-lookup"><span data-stu-id="fd0f4-126">[Quantum simulators and host applications](xref:microsoft.quantum.machines): an overview of the different simulators available, as well as the general execution model between host program and target machines.</span></span>

- <span data-ttu-id="fd0f4-127">[Симулятор полного состояния.](xref:microsoft.quantum.machines.full-state-simulator) Целевой компьютер, имитирующий полное квантовое состояние.</span><span class="sxs-lookup"><span data-stu-id="fd0f4-127">[Full state simulator](xref:microsoft.quantum.machines.full-state-simulator): the target machine which simulates the full quantum state.</span></span> <span data-ttu-id="fd0f4-128">Используется для выполнения или отладки программ небольшого размера (менее двух десятков кубитов).</span><span class="sxs-lookup"><span data-stu-id="fd0f4-128">Useful for fully executing or debugging smaller scale programs (less than a couple dozen qubits)</span></span>

- <span data-ttu-id="fd0f4-129">[Оценщик ресурсов.](xref:microsoft.quantum.machines.resources-estimator) Оценивает потребность в ресурсах для выполнения определенного экземпляра операции Q# на квантовом компьютере.</span><span class="sxs-lookup"><span data-stu-id="fd0f4-129">[Resources estimator](xref:microsoft.quantum.machines.resources-estimator): estimates the resources required to run a given instance of a Q# operation on a quantum computer.</span></span>

- <span data-ttu-id="fd0f4-130">[Симулятор трассировки.](xref:microsoft.quantum.machines.qc-trace-simulator.intro) Выполняет квантовую программу без фактической имитации состояния квантового компьютера, позволяя выполнять квантовые программы с несколькими тысячами кубитов.</span><span class="sxs-lookup"><span data-stu-id="fd0f4-130">[Trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro): executes a quantum program without actually simulating the state of a quantum computer, and therefore can execute quantum programs that use thousands of qubits.</span></span> <span data-ttu-id="fd0f4-131">Используется для отладки классического кода в квантовой программе, а также для оценки требуемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fd0f4-131">Useful for debugging classical code within a quantum program, as well as estimating resources required.</span></span>

- <span data-ttu-id="fd0f4-132">[Симулятор Тоффоли.](xref:microsoft.quantum.machines.toffoli-simulator) Специализированный программный симулятор квантового состояния, который умеет имитировать небольшой набор квантовых операций (X, CNOT и X с множественным управлением) для очень большого числа кубитов.</span><span class="sxs-lookup"><span data-stu-id="fd0f4-132">[Toffoli simulator](xref:microsoft.quantum.machines.toffoli-simulator): a special purpose quantum simulator that can be used with millions of qubits, but only for programs with a restricted set of quantum operations (namely X, CNOT, and multi-controlled X).</span></span>

### <a name="quick-reference-pages"></a><span data-ttu-id="fd0f4-133">Краткое справочное руководство</span><span class="sxs-lookup"><span data-stu-id="fd0f4-133">Quick Reference Pages</span></span>

- <span data-ttu-id="fd0f4-134">[Магические команды IQ#](xref:microsoft.quantum.guide.quickref.iqsharp) Краткая справочная информация о магических командах IQ# в Jupyter Notebook для Q#.</span><span class="sxs-lookup"><span data-stu-id="fd0f4-134">[IQ# Magic Commands](xref:microsoft.quantum.guide.quickref.iqsharp): Quick reference page for IQ# magic commands within Q# Jupyter Notebooks.</span></span>
