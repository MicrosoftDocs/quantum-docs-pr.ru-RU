---
title: 'Методы Q # — тестирование и отладка | Документация Майкрософт'
description: 'Методы Q # — тестирование и отладка'
author: tcNickolas
ms.author: mamykhai@microsoft.com
uid: microsoft.quantum.techniques.testing-and-debugging
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 25679331f1bed9f98b86c6eb20f511c891bac1af
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/26/2019
ms.locfileid: "73183494"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="0bc05-103">Тестирование и отладка</span><span class="sxs-lookup"><span data-stu-id="0bc05-103">Testing and Debugging</span></span>

<span data-ttu-id="0bc05-104">Как и в случае с классическим программированием, важно иметь возможность проверить, правильно ли работают тактовые программы и может ли она диагностировать неправильные тактовые программы.</span><span class="sxs-lookup"><span data-stu-id="0bc05-104">As with classical programming, it is essential to be able to check that quantum programs act as intended, and to be able to diagnose a quantum program that is incorrect.</span></span>
<span data-ttu-id="0bc05-105">В этом разделе мы рассмотрим средства, предлагаемые Q # для тестирования и отладки тактовых программ.</span><span class="sxs-lookup"><span data-stu-id="0bc05-105">In this section, we cover the tools offered by Q# for testing and debugging quantum programs.</span></span>

## <a name="unit-tests"></a><span data-ttu-id="0bc05-106">Модульные тесты</span><span class="sxs-lookup"><span data-stu-id="0bc05-106">Unit Tests</span></span>

<span data-ttu-id="0bc05-107">Одним из распространенных подходов к тестированию классических программ является написание небольших программ, именуемых *модульными тестами* , которые выполняют код в библиотеке и сравнивают выходные данные с ожидаемыми выходными данными.</span><span class="sxs-lookup"><span data-stu-id="0bc05-107">One common approach to testing classical programs is to write small programs called *unit tests* which run code in a library and compare its output to some expected output.</span></span>
<span data-ttu-id="0bc05-108">Например, может потребоваться убедиться, что `Square(2)` возвращает `4`, так как мы узнали *приори* , что $2 ^ 2 = $4.</span><span class="sxs-lookup"><span data-stu-id="0bc05-108">For instance, we may want to ensure that `Square(2)` returns `4`, since we know *a priori* that $2^2 = 4$.</span></span>

<span data-ttu-id="0bc05-109">Q # поддерживает создание модульных тестов для тактовых программ и может выполняться как тесты в среде модульного тестирования [xUnit](https://xunit.github.io/) .</span><span class="sxs-lookup"><span data-stu-id="0bc05-109">Q# supports creating unit tests for quantum programs, and which can be executed as tests within the [xUnit](https://xunit.github.io/) unit testing framework.</span></span>

### <a name="creating-a-test-project"></a><span data-ttu-id="0bc05-110">Создание тестового проекта</span><span class="sxs-lookup"><span data-stu-id="0bc05-110">Creating a Test Project</span></span>

#### <a name="visual-studio-2019tabtabid-vs2019"></a>[<span data-ttu-id="0bc05-111">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="0bc05-111">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="0bc05-112">Откройте Visual Studio 2019.</span><span class="sxs-lookup"><span data-stu-id="0bc05-112">Open Visual Studio 2019.</span></span> <span data-ttu-id="0bc05-113">Перейдите в меню `File` и выберите `New` > `Project...`.</span><span class="sxs-lookup"><span data-stu-id="0bc05-113">Go to the `File` menu and select `New` > `Project...`.</span></span>
<span data-ttu-id="0bc05-114">В обозревателе шаблонов проектов в разделе `Installed` > `Visual C#`выберите шаблон `Q# Test Project`.</span><span class="sxs-lookup"><span data-stu-id="0bc05-114">In the project template explorer, under `Installed` > `Visual C#`, select the `Q# Test Project` template.</span></span>

#### <a name="command-line--visual-studio-codetabtabid-vscode"></a>[<span data-ttu-id="0bc05-115">Командная строка и Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="0bc05-115">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="0bc05-116">В командной строке избранного выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0bc05-116">From your favorite command line, run the following command:</span></span>
```bash
$ dotnet new xunit -lang Q# -o Tests
$ cd Tests
$ code . # To open in Visual Studio Code
```

****

<span data-ttu-id="0bc05-117">В любом случае в новом проекте будет открыто два файла.</span><span class="sxs-lookup"><span data-stu-id="0bc05-117">In either case, your new project will have two files open.</span></span>
<span data-ttu-id="0bc05-118">Первый файл, `Tests.qs`, предоставляет удобное место для определения новых модульных тестов Q #.</span><span class="sxs-lookup"><span data-stu-id="0bc05-118">The first file, `Tests.qs`, provides a convenient place to define new Q# unit tests.</span></span>
<span data-ttu-id="0bc05-119">Изначально этот файл содержит один пример модульного теста `AllocateQubitTest` который проверяет, что вновь выделенные кубит находятся в{0}\кет $ State $ и выводит сообщение:</span><span class="sxs-lookup"><span data-stu-id="0bc05-119">Initially this file contains one sample unit test `AllocateQubitTest` which checks that a newly allocated qubit is in the $\ket{0}$ state and prints a message:</span></span>

```qsharp
    operation AllocateQubitTest () : Unit {
        using (q = Qubit()) {
            Assert([PauliZ], [q], Zero, "Newly allocated qubit must be in the |0⟩ state.");
        }
        
        Message("Test passed");
    }
```

<span data-ttu-id="0bc05-120">Любая операция Q #, совместимая с типом `(Unit => Unit)` или функцией, совместимой с `(Unit -> Unit)`, может выполняться как модульный тест.</span><span class="sxs-lookup"><span data-stu-id="0bc05-120">Any Q# operation compatible with the type `(Unit => Unit)` or function compatible with `(Unit -> Unit)` can be executed as a unit test.</span></span> 

<span data-ttu-id="0bc05-121">Второй файл, `TestSuiteRunner.cs` содержит метод, который обнаруживает и выполняет модульные тесты Q #.</span><span class="sxs-lookup"><span data-stu-id="0bc05-121">The second file, `TestSuiteRunner.cs` contains a method that discovers and runs Q# unit tests.</span></span> <span data-ttu-id="0bc05-122">Этот метод `TestTarget` закомментировать атрибут `OperationDriver`.</span><span class="sxs-lookup"><span data-stu-id="0bc05-122">This is the method `TestTarget` annotated with `OperationDriver` attribute.</span></span>
<span data-ttu-id="0bc05-123">Атрибут `OperationDriver` является частью библиотеки расширений xUnit Microsoft. Квант. моделирования. xUnit.</span><span class="sxs-lookup"><span data-stu-id="0bc05-123">The `OperationDriver` attribute is a part of the Xunit extension library Microsoft.Quantum.Simulation.Xunit.</span></span>
<span data-ttu-id="0bc05-124">Платформа модульного тестирования вызывает метод `TestTarget` для каждого обнаруженного модульного теста Q #.</span><span class="sxs-lookup"><span data-stu-id="0bc05-124">The unit testing framework calls `TestTarget` method for every Q# unit test it has discovered.</span></span>
<span data-ttu-id="0bc05-125">Платформа передает описание модульного теста методу с помощью `op` аргументе.</span><span class="sxs-lookup"><span data-stu-id="0bc05-125">The framework passes the unit test description to the method through `op` argument.</span></span> <span data-ttu-id="0bc05-126">Следующая строка кода:</span><span class="sxs-lookup"><span data-stu-id="0bc05-126">The following line of code:</span></span>
```csharp
op.TestOperationRunner(sim);
```
<span data-ttu-id="0bc05-127">выполняет модульный тест на `QuantumSimulator`.</span><span class="sxs-lookup"><span data-stu-id="0bc05-127">executes the unit test on `QuantumSimulator`.</span></span>

<span data-ttu-id="0bc05-128">По умолчанию механизм обнаружения модульных тестов ищет все функции Q # или операции совместимого типа, которые соответствуют следующим свойствам:</span><span class="sxs-lookup"><span data-stu-id="0bc05-128">By default, the unit test discovery mechanism looks for all Q# functions or operations of compatible type that satisfy the following properties:</span></span>
* <span data-ttu-id="0bc05-129">Находится в той же сборке, что и метод, помеченный атрибутом `OperationDriver`.</span><span class="sxs-lookup"><span data-stu-id="0bc05-129">Located in the same assembly as the method annotated with the `OperationDriver` attribute.</span></span>
* <span data-ttu-id="0bc05-130">Находится в том же пространстве имен, что и метод, помеченный атрибутом `OperationDriver`.</span><span class="sxs-lookup"><span data-stu-id="0bc05-130">Located in the same namespace as the method annotated with the `OperationDriver` attribute.</span></span>
* <span data-ttu-id="0bc05-131">Имеет имя, завершающееся `Test`.</span><span class="sxs-lookup"><span data-stu-id="0bc05-131">Has a name ending with `Test`.</span></span>

<span data-ttu-id="0bc05-132">Сборку, пространство имен и суффикс для функций и операций модульного тестирования можно задать с помощью необязательных параметров атрибута `OperationDriver`:</span><span class="sxs-lookup"><span data-stu-id="0bc05-132">An assembly, a namespace, and a suffix for unit test functions and operations can be set using optional parameters of the `OperationDriver` attribute:</span></span>
* <span data-ttu-id="0bc05-133">`AssemblyName` параметр задает имя сборки, в которой выполняется поиск тестов.</span><span class="sxs-lookup"><span data-stu-id="0bc05-133">`AssemblyName` parameter sets the name of the assembly which is being searched for tests.</span></span>
* <span data-ttu-id="0bc05-134">`TestNamespace` параметр задает имя пространства имен, в котором выполняется поиск тестов.</span><span class="sxs-lookup"><span data-stu-id="0bc05-134">`TestNamespace` parameter sets the name of the namespace which is being searched for tests.</span></span>
* <span data-ttu-id="0bc05-135">`Suffix` задает суффикс имен операций или функций, которые считаются модульными тестами.</span><span class="sxs-lookup"><span data-stu-id="0bc05-135">`Suffix` sets the suffix of operation or function names that are considered to be unit tests.</span></span>

<span data-ttu-id="0bc05-136">Кроме того, `TestCasePrefix` необязательный параметр позволяет задать префикс для имени тестового случая.</span><span class="sxs-lookup"><span data-stu-id="0bc05-136">In addition, the `TestCasePrefix` optional parameter lets you set a prefix for the name of the test case.</span></span> <span data-ttu-id="0bc05-137">Префикс перед именем операции появится в списке тестовых случаев.</span><span class="sxs-lookup"><span data-stu-id="0bc05-137">The prefix in front of the operation name will appear in the list of test cases.</span></span> <span data-ttu-id="0bc05-138">Например, `TestCasePrefix = "QSim:"` приведет к тому, что `AllocateQubitTest` будет выглядеть как `QSim:AllocateQubitTest` в списке найденных тестов.</span><span class="sxs-lookup"><span data-stu-id="0bc05-138">For example, `TestCasePrefix = "QSim:"` will cause `AllocateQubitTest` to appear as `QSim:AllocateQubitTest` in the list of found tests.</span></span> <span data-ttu-id="0bc05-139">Это может быть полезно для того, чтобы указать, например, симулятор, используемый для выполнения теста.</span><span class="sxs-lookup"><span data-stu-id="0bc05-139">This can be useful to indicate, for instance, which simulator is used to run a test.</span></span>

### <a name="running-q-unit-tests"></a><span data-ttu-id="0bc05-140">Выполнение модульных тестов Q #</span><span class="sxs-lookup"><span data-stu-id="0bc05-140">Running Q# Unit Tests</span></span>

#### <a name="visual-studio-2019tabtabid-vs2019"></a>[<span data-ttu-id="0bc05-141">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="0bc05-141">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="0bc05-142">В качестве одноразовой настройки для каждого решения перейдите в меню `Test` и выберите `Test Settings` > `Default Processor Architecture` > `X64`.</span><span class="sxs-lookup"><span data-stu-id="0bc05-142">As a one-time per-solution setup, go to `Test` menu and select `Test Settings` > `Default Processor Architecture` > `X64`.</span></span>

> [!TIP]
> <span data-ttu-id="0bc05-143">Параметр архитектуры процессора по умолчанию для Visual Studio хранится в файле параметров решения (`.suo`) для каждого решения.</span><span class="sxs-lookup"><span data-stu-id="0bc05-143">The default processor architecture setting for Visual Studio is stored in the solution options (`.suo`) file for each solution.</span></span>
> <span data-ttu-id="0bc05-144">Если удалить этот файл, вам потребуется снова выбрать `X64` в качестве архитектуры процессора.</span><span class="sxs-lookup"><span data-stu-id="0bc05-144">If you delete this file, then you will need to select `X64` as your processor architecture again.</span></span>

<span data-ttu-id="0bc05-145">Выполните сборку проекта, перейдите в меню `Test` и выберите `Windows` > `Test Explorer`.</span><span class="sxs-lookup"><span data-stu-id="0bc05-145">Build the project, go to the `Test` menu and select `Windows` > `Test Explorer`.</span></span> <span data-ttu-id="0bc05-146">`AllocateQubitTest` будут отображаться в списке тестов в группе `Not Run Tests`.</span><span class="sxs-lookup"><span data-stu-id="0bc05-146">`AllocateQubitTest` will show up in the list of tests in the `Not Run Tests` group.</span></span> <span data-ttu-id="0bc05-147">Выберите `Run All` или запустите этот отдельный тест, и он должен пройти!</span><span class="sxs-lookup"><span data-stu-id="0bc05-147">Select `Run All` or run this individual test, and it should pass!</span></span>

#### <a name="command-line--visual-studio-codetabtabid-vscode"></a>[<span data-ttu-id="0bc05-148">Командная строка и Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="0bc05-148">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="0bc05-149">Чтобы запустить тесты, перейдите в папку проекта (папку, содержащую `Tests.csproj`) и выполните команду:</span><span class="sxs-lookup"><span data-stu-id="0bc05-149">To run tests, navigate to the project folder (the folder which contains `Tests.csproj`), and execute the command:</span></span>

```bash
$ dotnet restore
$ dotnet test
```

<span data-ttu-id="0bc05-150">Должен отобразиться результат, аналогичный приведенному ниже.</span><span class="sxs-lookup"><span data-stu-id="0bc05-150">You should get output similar to the following:</span></span>

```
Build started, please wait...
Build completed.

Test run for C:\Users\chgranad.REDMOND\tmp\Tests\bin\Debug\netcoreapp2.0\Tests.dll(.NETCoreApp,Version=v2.0)
Microsoft (R) Test Execution Command Line Tool Version 15.3.0-preview-20170628-02
Copyright (c) Microsoft Corporation.  All rights reserved.

Starting test execution, please wait...
[xUnit.net 00:00:00.5864002]   Discovering: Tests
[xUnit.net 00:00:00.7073844]   Discovered:  Tests
[xUnit.net 00:00:00.7453826]   Starting:    Tests
[xUnit.net 00:00:00.9590439]   Finished:    Tests

Total tests: 1. Passed: 1. Failed: 0. Skipped: 0.
Test Run Successful.
Test execution time: 1.9607 Seconds
```

***

## <a name="logging-and-assertions"></a><span data-ttu-id="0bc05-151">Ведение журнала и утверждения</span><span class="sxs-lookup"><span data-stu-id="0bc05-151">Logging and Assertions</span></span>

<span data-ttu-id="0bc05-152">Одной из важных последствий того факта, что функции в Q # не имеют побочных эффектов, является то, что любой эффект выполнения функции, тип вывода которой является пустым кортежем, `()` не может рассматриваться в программе Q #.</span><span class="sxs-lookup"><span data-stu-id="0bc05-152">One important consequence of the fact that functions in Q# have no side effects is that any effects of executing a function whose output type is the empty tuple `()` can never be observed from within a Q# program.</span></span>
<span data-ttu-id="0bc05-153">То есть целевой компьютер может не выполнять какую-либо функцию, возвращающую `()` с гарантией, что это не приведет к изменению поведения любого следующего кода Q #.</span><span class="sxs-lookup"><span data-stu-id="0bc05-153">That is, a target machine can choose not to execute any function which returns `()` with the guarantee that this omission will not modify the behavior of any following Q# code.</span></span>
<span data-ttu-id="0bc05-154">Это позволяет функциям возвращать `()` полезное средство для внедрения утверждений и логики отладки в программы Q #.</span><span class="sxs-lookup"><span data-stu-id="0bc05-154">This makes functions returning `()` a useful tool for embedding assertions and debugging logic into Q# programs.</span></span> 

### <a name="logging"></a><span data-ttu-id="0bc05-155">Ведение журнала</span><span class="sxs-lookup"><span data-stu-id="0bc05-155">Logging</span></span>

<span data-ttu-id="0bc05-156">Встроенная функция <xref:microsoft.quantum.intrinsic.message> имеет тип `(String -> Unit)` и позволяет создавать диагностические сообщения.</span><span class="sxs-lookup"><span data-stu-id="0bc05-156">The intrinsic function <xref:microsoft.quantum.intrinsic.message> has type `(String -> Unit)` and enables the creation of diagnostic messages.</span></span>

<span data-ttu-id="0bc05-157">`onLog` действие `QuantumSimulator` можно использовать для определения действий, выполняемых при вызове кода Q # `Message`.</span><span class="sxs-lookup"><span data-stu-id="0bc05-157">The `onLog` action of `QuantumSimulator` can be used to define actions performed when Q# code calls `Message`.</span></span> <span data-ttu-id="0bc05-158">По умолчанию сообщения, записанные в журнал, выводятся в стандартный вывод.</span><span class="sxs-lookup"><span data-stu-id="0bc05-158">By default logged messages are printed to standard output.</span></span>

<span data-ttu-id="0bc05-159">При определении набора модульных тестов записанные в журнал сообщения можно направлять в выходные данные теста.</span><span class="sxs-lookup"><span data-stu-id="0bc05-159">When defining a unit test suite, the logged messages can be directed to the test output.</span></span> <span data-ttu-id="0bc05-160">При создании проекта с помощью шаблона тестового проекта Q # это перенаправление предварительно настроено для набора и создается по умолчанию следующим образом.</span><span class="sxs-lookup"><span data-stu-id="0bc05-160">When a project is created from Q# Test Project template, this redirection is pre-configured for the suite and created by default as follows:</span></span>

```qsharp
using (var sim = new QuantumSimulator())
{
    // OnLog defines action(s) performed when Q# test calls operation Message
    sim.OnLog += (msg) => { output.WriteLine(msg); };
    op.TestOperationRunner(sim);
}
```

#### <a name="visual-studio-2019tabtabid-vs2019"></a>[<span data-ttu-id="0bc05-161">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="0bc05-161">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="0bc05-162">После выполнения теста в обозревателе тестов и нажатия кнопки тест появится панель со сведениями о выполнении теста: состояние пройдено/неудачно, затраченное время и ссылка "выходные данные".</span><span class="sxs-lookup"><span data-stu-id="0bc05-162">After you execute a test in Test Explorer and click on the test, a panel will appear with information about test execution: Passed/Failed status, elapsed time and an "Output" link.</span></span> <span data-ttu-id="0bc05-163">Если щелкнуть ссылку "выходные данные", тестовый вывод откроется в новом окне.</span><span class="sxs-lookup"><span data-stu-id="0bc05-163">If you click the "Output" link, test output will open in a new window.</span></span>

![выходные данные теста](~/media/unit-test-output.png)

#### <a name="command-line--visual-studio-codetabtabid-vscode"></a>[<span data-ttu-id="0bc05-165">Командная строка и Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="0bc05-165">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="0bc05-166">Состояние "успех/сбой" для каждого теста выводится на консоль `dotnet test`.</span><span class="sxs-lookup"><span data-stu-id="0bc05-166">The pass/fail status for each test is printed to the console by `dotnet test`.</span></span>
<span data-ttu-id="0bc05-167">Для неудачных тестов выходные данные, регистрируемые в результате `output.WriteLine(msg)`ного вызова выше, также выводятся на консоль для облегчения диагностики сбоя.</span><span class="sxs-lookup"><span data-stu-id="0bc05-167">For failing tests, the outputs logged as a result of the `output.WriteLine(msg)` call above are also printed to the console to help diagnose the failure.</span></span>

***

### <a name="assertions"></a><span data-ttu-id="0bc05-168">Утверждения</span><span class="sxs-lookup"><span data-stu-id="0bc05-168">Assertions</span></span>

<span data-ttu-id="0bc05-169">Для реализации утверждений можно применить ту же логику.</span><span class="sxs-lookup"><span data-stu-id="0bc05-169">The same logic can be applied to implementing assertions.</span></span> <span data-ttu-id="0bc05-170">Рассмотрим простой пример:</span><span class="sxs-lookup"><span data-stu-id="0bc05-170">Let's consider a simple example:</span></span>

```qsharp
function AssertPositive(value : Double) : Unit 
{
    if (value <= 0) 
    {
        fail "Expected a positive number.";
    }
}
```

<span data-ttu-id="0bc05-171">В этом случае ключевое слово `fail` указывает, что вычисление не должно выполняться, вызывая исключение на целевом компьютере, на котором выполняется программа Q #.</span><span class="sxs-lookup"><span data-stu-id="0bc05-171">Here, the keyword `fail` indicates that the computation should not proceed, raising an exception in the target machine running the Q# program.</span></span>
<span data-ttu-id="0bc05-172">По определению, сбой этого вида не может рассматриваться в Q #, так как дальнейший код Q # не будет выполняться после того, как будет достигнута инструкция `fail`.</span><span class="sxs-lookup"><span data-stu-id="0bc05-172">By definition, a failure of this kind cannot be observed from within Q#, as no further Q# code is run after a `fail` statement is reached.</span></span>
<span data-ttu-id="0bc05-173">Таким же, если бы мы пропустили вызов `AssertPositive`, мы можем быть уверены, что его входные данные были положительными.</span><span class="sxs-lookup"><span data-stu-id="0bc05-173">Thus, if we proceed past a call to `AssertPositive`, we can be assured by that its input was positive.</span></span>

<span data-ttu-id="0bc05-174">Основываясь на этих идеях, [версионного](xref:microsoft.quantum.libraries.standard.prelude) предлагает два особенно полезных утверждения, <xref:microsoft.quantum.intrinsic.assert> и <xref:microsoft.quantum.intrinsic.assertprob> как с помощью операций, так и в `()`.</span><span class="sxs-lookup"><span data-stu-id="0bc05-174">Building on these ideas, [the prelude](xref:microsoft.quantum.libraries.standard.prelude) offers two especially useful assertions, <xref:microsoft.quantum.intrinsic.assert> and <xref:microsoft.quantum.intrinsic.assertprob> both modeled as operations onto `()`.</span></span> <span data-ttu-id="0bc05-175">Каждый из этих утверждений принимает Оператор Паули, описывающий определенное измерение интересов, тактовый регистр, на котором выполняется измерение, и гипотетический результат.</span><span class="sxs-lookup"><span data-stu-id="0bc05-175">These assertions each take a Pauli operator describing a particular measurement of interest, a quantum register on which a measurement is to be performed, and a hypothetical outcome.</span></span>
<span data-ttu-id="0bc05-176">На целевых компьютерах, работающих по моделированию, мы не привязаны [к Теорема без клонирования](https://en.wikipedia.org/wiki/No-cloning_theorem)и могут выполнять такие измерения без нарушения регистра, передаваемого в такие утверждения.</span><span class="sxs-lookup"><span data-stu-id="0bc05-176">On target machines which work by simulation, we are not bound by [the no-cloning theorem](https://en.wikipedia.org/wiki/No-cloning_theorem), and can perform such measurements without disturbing the register passed to such assertions.</span></span>
<span data-ttu-id="0bc05-177">Симулятор может, как и приведенная выше функция `AssertPositive`, прерывать вычисления, если гипотетический результат не наблюдается на практике:</span><span class="sxs-lookup"><span data-stu-id="0bc05-177">A simulator can then, similar to the `AssertPositive` function above, abort computation if the hypothetical outcome would not be observed in practice:</span></span>

```qsharp
using (register = Qubit()) 
{
    H(register);
    Assert([PauliX], [register], Zero);
    // Even though we do not have access to states in Q#,
    // we know by the anthropic principle that the state
    // of register at this point is |+〉.
}
```

<span data-ttu-id="0bc05-178">На оборудовании физического такта, где Теорема без клонирования предотвращает исследование состояния такта, операции `Assert` и `AssertProb` просто возвращают `()` без какого-либо другого действия.</span><span class="sxs-lookup"><span data-stu-id="0bc05-178">On physical quantum hardware, where the no-cloning theorem prevents examination of quantum state, the `Assert` and `AssertProb` operations simply return `()` with no other effect.</span></span>

<span data-ttu-id="0bc05-179">Пространство имен <xref:microsoft.quantum.diagnostics> предоставляет несколько дополнительных функций семейства `Assert`, которые позволяют проверять более сложные условия.</span><span class="sxs-lookup"><span data-stu-id="0bc05-179">The <xref:microsoft.quantum.diagnostics> namespace provides several more functions of the `Assert` family which allow us to check more advanced conditions.</span></span> 

## <a name="dump-functions"></a><span data-ttu-id="0bc05-180">Функции дампа</span><span class="sxs-lookup"><span data-stu-id="0bc05-180">Dump Functions</span></span>

<span data-ttu-id="0bc05-181">Чтобы помочь в устранении неполадок в тактовых программах, пространство имен <xref:microsoft.quantum.diagnostics> предлагает две функции, которые могут выводить дамп в файл текущее состояние целевого компьютера: <xref:microsoft.quantum.diagnostics.dumpmachine> и <xref:microsoft.quantum.diagnostics.dumpregister>.</span><span class="sxs-lookup"><span data-stu-id="0bc05-181">To help troubleshooting quantum programs, the <xref:microsoft.quantum.diagnostics> namespace offers two functions that can dump into a file the current status of the target machine: <xref:microsoft.quantum.diagnostics.dumpmachine> and <xref:microsoft.quantum.diagnostics.dumpregister>.</span></span> <span data-ttu-id="0bc05-182">Созданные выходные данные каждого из них зависят от целевого компьютера.</span><span class="sxs-lookup"><span data-stu-id="0bc05-182">The generated output of each depends on the target machine.</span></span>

### <a name="dumpmachine"></a><span data-ttu-id="0bc05-183">думпмачине</span><span class="sxs-lookup"><span data-stu-id="0bc05-183">DumpMachine</span></span>

<span data-ttu-id="0bc05-184">Симулятор имитатора с полным состоянием, распространяемый как часть пакета разработки такта, записывает в файл [функцию Wave](https://en.wikipedia.org/wiki/Wave_function) всей тактовой системы, в виде одномерного массива комплексных чисел, в котором каждый элемент представляет амплитуду элемента вероятность измерения вычислительного базового состояния $ \кет{н} $, где $ \кет{н} = \ket{B_{n-1}... b_1b_0} $ для BITS $\{b_i\}$.</span><span class="sxs-lookup"><span data-stu-id="0bc05-184">The full-state quantum simulator distributed as part of the Quantum Development Kit writes into the file the [wave function](https://en.wikipedia.org/wiki/Wave_function) of the entire quantum system, as a one-dimensional array of complex numbers, in which each element represents the amplitude of the probability of measuring the computational basis state $\ket{n}$, where $\ket{n} = \ket{b_{n-1}...b_1b_0}$ for bits $\{b_i\}$.</span></span> <span data-ttu-id="0bc05-185">Например, на компьютере с двумя выделенными Кубитс и в состоянии такта $ $ \бегин{алигн} \кет{\пси} = \фрак{1}{\скрт{2}} \кет{00}-\фрак{(1 + i)}{2} \кет{10}, \енд{алигн} $ $ вызов <xref:microsoft.quantum.diagnostics.dumpmachine> создает этот результат. :</span><span class="sxs-lookup"><span data-stu-id="0bc05-185">For example, on a machine with only two qubits allocated and in the quantum state $$ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10}, \end{align} $$ calling <xref:microsoft.quantum.diagnostics.dumpmachine> generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 0;1
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣2❭:    -0.500000 + -0.500000 i  ==     **********           [ 0.500000 ]   /     [ -2.35619 rad ]
∣3❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

<span data-ttu-id="0bc05-186">Первая строка содержит комментарий с идентификаторами соответствующего Кубитс в значительном порядке.</span><span class="sxs-lookup"><span data-stu-id="0bc05-186">The first row provides a comment with the IDs of the corresponding qubits in their significant order.</span></span>
<span data-ttu-id="0bc05-187">Остальные строки описывают амплитуду вероятности по измерению вектора состояния базы данных $ \кет{н} $ в декартовой и полярной форматах.</span><span class="sxs-lookup"><span data-stu-id="0bc05-187">The rest of the rows describe the probability amplitude of measuring the basis state vector $\ket{n}$ in both Cartesian and polar formats.</span></span> <span data-ttu-id="0bc05-188">Подробно для первой строки:</span><span class="sxs-lookup"><span data-stu-id="0bc05-188">In detail for the first row:</span></span>

* <span data-ttu-id="0bc05-189">**`∣0❭:`** эта строка соответствует `0`ному состоянию вычислительной базы</span><span class="sxs-lookup"><span data-stu-id="0bc05-189">**`∣0❭:`** this row corresponds to the `0` computational basis state</span></span>
* <span data-ttu-id="0bc05-190">**`0.707107 +  0.000000 i`** : амплитуда вероятности в формате декартовы.</span><span class="sxs-lookup"><span data-stu-id="0bc05-190">**`0.707107 +  0.000000 i`**: the probability amplitude in Cartesian format.</span></span>
* <span data-ttu-id="0bc05-191">**` == `** : `equal` знак, который разписывает оба эквивалентных представления.</span><span class="sxs-lookup"><span data-stu-id="0bc05-191">**` == `**: the `equal` sign seperates both equivalent representations.</span></span>
* <span data-ttu-id="0bc05-192">**`**********  `** : графическое представление величины, количество `*` пропорционально вероятности измерения этого вектора состояния.</span><span class="sxs-lookup"><span data-stu-id="0bc05-192">**`**********  `**: A graphical representation of the magnitude, the number of `*` is proportionate to the probability of measuring this state vector.</span></span>
* <span data-ttu-id="0bc05-193">**`[ 0.500000 ]`** : числовое значение величины</span><span class="sxs-lookup"><span data-stu-id="0bc05-193">**`[ 0.500000 ]`**: the numeric value of the magnitude</span></span>
* <span data-ttu-id="0bc05-194">**`    ---`** : графическое представление фазы амплитуды (см. ниже).</span><span class="sxs-lookup"><span data-stu-id="0bc05-194">**`    ---`**: A graphical representation of the amplitude's phase (see below).</span></span>
* <span data-ttu-id="0bc05-195">**`[ 0.0000 rad ]`** : числовое значение этапа (в радианах).</span><span class="sxs-lookup"><span data-stu-id="0bc05-195">**`[ 0.0000 rad ]`**: the numeric value of the phase (in radians).</span></span>

<span data-ttu-id="0bc05-196">Как величина, так и фаза отображаются с графическим представлением.</span><span class="sxs-lookup"><span data-stu-id="0bc05-196">Both the magnitude and the phase are displayed with a graphical representation.</span></span> <span data-ttu-id="0bc05-197">Представление величины прямо вперед: оно показывает отрезок `*`, чем больше вероятность, чем больше строка.</span><span class="sxs-lookup"><span data-stu-id="0bc05-197">The magnitude representation is straight-forward: it shows a bar of `*`, the bigger the probability the bigger the bar will be.</span></span> <span data-ttu-id="0bc05-198">Для этапа показаны следующие символы, представляющие угол на основе диапазонов:</span><span class="sxs-lookup"><span data-stu-id="0bc05-198">For the phase, we show the following symbols to represent the angle based on ranges:</span></span>

```
[ -π/16,   π/16)       ---
[  π/16,  3π/16)        /-
[ 3π/16,  5π/16)        / 
[ 5π/16,  7π/16)       +/ 
[ 7π/16,  9π/16)      ↑   
[ 8π/16, 11π/16)    \-    
[ 7π/16, 13π/16)    \     
[ 7π/16, 15π/16)   +\     
[15π/16, 19π/16)   ---    
[17π/16, 19π/16)   -/     
[19π/16, 21π/16)    /     
[21π/16, 23π/16)    /+    
[23π/16, 25π/16)      ↓   
[25π/16, 27π/16)       -\ 
[27π/16, 29π/16)        \ 
[29π/16, 31π/16)        \+
[31π/16,   π/16)       ---
```

<span data-ttu-id="0bc05-199">В следующих примерах показаны `DumpMachine` для некоторых распространенных состояний.</span><span class="sxs-lookup"><span data-stu-id="0bc05-199">The following examples show `DumpMachine` for some common states:</span></span>

### `∣0❭`

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

### `∣1❭`

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣1❭:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
```

### `∣+❭`

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]      --- [  0.00000 rad ]
∣1❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]      --- [  0.00000 rad ]
```

### `∣-❭`

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]      --- [  0.00000 rad ]
∣1❭:    -0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]  ---     [  3.14159 rad ]
```


  > [!NOTE]
  > <span data-ttu-id="0bc05-200">Идентификатор кубит назначается во время выполнения и не обязательно соответствует порядку выделения кубит или его позиции в кубит регистре.</span><span class="sxs-lookup"><span data-stu-id="0bc05-200">The id of a qubit is assigned at runtime and it's not necessarily aligned with the order in which the qubit was allocated or its position within a qubit register.</span></span>


#### <a name="visual-studio-2019tabtabid-vs2019"></a>[<span data-ttu-id="0bc05-201">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="0bc05-201">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

  > [!TIP]
  > <span data-ttu-id="0bc05-202">Чтобы определить идентификатор кубит в Visual Studio, поместите точку останова в код и проверьте значение переменной кубит, например:</span><span class="sxs-lookup"><span data-stu-id="0bc05-202">You can figure out a qubit id in Visual Studio by putting a breakpoint in your code and inspecting the value of a qubit variable, for example:</span></span>
  > 
  > ![показывать идентификатор кубит в Visual Studio](~/media/qubit_id.png)
  >
  > <span data-ttu-id="0bc05-204">Кубит с индексом `0` в `register2` имеет ID =`3`, кубит с индексом `1` имеет ID =`2`.</span><span class="sxs-lookup"><span data-stu-id="0bc05-204">the qubit with index `0` on `register2` has id=`3`, the qubit with index `1` has id=`2`.</span></span>

#### <a name="command-line--visual-studio-codetabtabid-vscode"></a>[<span data-ttu-id="0bc05-205">Командная строка и Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="0bc05-205">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

  > [!TIP]
  > <span data-ttu-id="0bc05-206">Вы можете определить идентификатор кубит с помощью функции <xref:microsoft.quantum.intrinsic.message> и передать переменную кубит в сообщении, например:</span><span class="sxs-lookup"><span data-stu-id="0bc05-206">You can figure out a qubit id by using the <xref:microsoft.quantum.intrinsic.message> function and passing the qubit variable in the message, for example:</span></span>
  >
  > ```qsharp
  > Message($"0={register2[0]}; 1={register2[1]}");
  > ```
  > 
  > <span data-ttu-id="0bc05-207">которые могут формировать этот результат:</span><span class="sxs-lookup"><span data-stu-id="0bc05-207">which could generate this output:</span></span>
  >```
  > 0=q:3; 1=q:2
  >```
  > <span data-ttu-id="0bc05-208">Это означает, что кубит с индексом `0` в `register2` имеет ID =`3`, кубит с индексом `1` имеет ID =`2`.</span><span class="sxs-lookup"><span data-stu-id="0bc05-208">which means that the qubit with index `0` on `register2` has id=`3`, the qubit with index `1` has id=`2`.</span></span>


***

<span data-ttu-id="0bc05-209"><xref:microsoft.quantum.diagnostics.dumpmachine> является частью пространства имен <xref:microsoft.quantum.diagnostics>, поэтому для его использования необходимо добавить инструкцию `open`:</span><span class="sxs-lookup"><span data-stu-id="0bc05-209"><xref:microsoft.quantum.diagnostics.dumpmachine> is part of the  <xref:microsoft.quantum.diagnostics> namespace, so in order to use it you must add an `open` statement:</span></span>

```qsharp
namespace Samples {
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Diagnostics;

    operation Operation () : Unit {
        using (qubits = Qubit[2]) {
            H(qubits[1]);
            DumpMachine("dump.txt");
        }
    }
}
```


### <a name="dumpregister"></a><span data-ttu-id="0bc05-210">думпрегистер</span><span class="sxs-lookup"><span data-stu-id="0bc05-210">DumpRegister</span></span>

<span data-ttu-id="0bc05-211"><xref:microsoft.quantum.diagnostics.dumpregister> работает так же, как <xref:microsoft.quantum.diagnostics.dumpmachine>, за исключением того, что он также принимает массив Кубитс, чтобы ограничить объем информации, относящейся только к соответствующему Кубитс.</span><span class="sxs-lookup"><span data-stu-id="0bc05-211"><xref:microsoft.quantum.diagnostics.dumpregister> works like <xref:microsoft.quantum.diagnostics.dumpmachine>, except it also takes an array of qubits to limit the amount of information to only that relevant to the corresponding qubits.</span></span>

<span data-ttu-id="0bc05-212">Как и в случае с <xref:microsoft.quantum.diagnostics.dumpmachine>, сведения, создаваемые <xref:microsoft.quantum.diagnostics.dumpregister>, зависят от целевого компьютера.</span><span class="sxs-lookup"><span data-stu-id="0bc05-212">As with <xref:microsoft.quantum.diagnostics.dumpmachine>, the information generated by <xref:microsoft.quantum.diagnostics.dumpregister> depends on the target machine.</span></span> <span data-ttu-id="0bc05-213">Для имитатора такта с полным состоянием он записывает в файл функцию Wave вплоть до глобального этапа подсистемы такта, созданной предоставленным Кубитс в том же формате, что и <xref:microsoft.quantum.diagnostics.dumpmachine>.</span><span class="sxs-lookup"><span data-stu-id="0bc05-213">For the full-state quantum simulator it writes into the file the wave function up to a global phase of the quantum sub-system generated by the provided qubits in the same format as <xref:microsoft.quantum.diagnostics.dumpmachine>.</span></span>  <span data-ttu-id="0bc05-214">Например, еще один компьютер с двумя выделенными Кубитс и в состоянии такта $ $ \бегин{алигн} \кет{\пси} = \фрак{1}{\скрт{2}} \кет{00}-\фрак{(1 + i)}{2} \кет{10} =-e ^ {-i \ PI/4} ((\фрак{1}{\скрт{2}} \ Сисакет{0}-\фрак{(1 + i)}{2} \кет{1}) \отимес \фрак{-(1 + i)} {\скрт{2}} \кет{0}), \енд{алигн} $ $ вызов <xref:microsoft.quantum.diagnostics.dumpregister> для `qubit[0]` создает эти выходные данные:</span><span class="sxs-lookup"><span data-stu-id="0bc05-214">For example, take again a machine with only two qubits allocated and in the quantum state $$ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10} = - e^{-i\pi/4} ( (\frac{1}{\sqrt{2}} \ket{0} - \frac{(1 + i)}{2} \ket{1} ) \otimes \frac{-(1 + i)}{\sqrt{2}} \ket{0} ) , \end{align} $$ calling <xref:microsoft.quantum.diagnostics.dumpregister> for `qubit[0]` generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:    -0.707107 + -0.707107 i  ==     ******************** [ 1.000000 ]  /      [ -2.35619 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

<span data-ttu-id="0bc05-215">и вызов <xref:microsoft.quantum.diagnostics.dumpregister> для `qubit[1]` создает следующие выходные данные:</span><span class="sxs-lookup"><span data-stu-id="0bc05-215">and calling <xref:microsoft.quantum.diagnostics.dumpregister> for `qubit[1]` generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 1
∣0❭:     0.707107 +  0.000000 i  ==     ***********          [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:    -0.500000 + -0.500000 i  ==     ***********          [ 0.500000 ]  /      [ -2.35619 rad ]
```

<span data-ttu-id="0bc05-216">Как правило, состояние регистра, запутанными с другим регистром, находится в смешанном состоянии, а не в чистом состоянии.</span><span class="sxs-lookup"><span data-stu-id="0bc05-216">In general, the state of a register that is entangled with another register is a mixed state rather than a pure state.</span></span> <span data-ttu-id="0bc05-217">В этом случае <xref:microsoft.quantum.diagnostics.dumpregister> выводит следующее сообщение:</span><span class="sxs-lookup"><span data-stu-id="0bc05-217">In this case, <xref:microsoft.quantum.diagnostics.dumpregister> outputs the following message:</span></span>

```
Qubits provided (0;) are entangled with some other qubit.
```

<span data-ttu-id="0bc05-218">В следующем примере показано, как можно использовать как <xref:microsoft.quantum.diagnostics.dumpregister>, так и <xref:microsoft.quantum.diagnostics.dumpmachine> в коде Q #:</span><span class="sxs-lookup"><span data-stu-id="0bc05-218">The following example shows you how you can use both <xref:microsoft.quantum.diagnostics.dumpregister> and <xref:microsoft.quantum.diagnostics.dumpmachine> in your Q# code:</span></span>

```qsharp
namespace app
{
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Diagnostics;

    operation Operation () : Unit {

        using (qubits = Qubit[2]) {
            X(qubits[1]);
            H(qubits[1]);
            R1Frac(1, 2, qubits[1]);
            
            DumpMachine("dump.txt");
            DumpRegister("q0.txt", qubits[0..0]);
            DumpRegister("q1.txt", qubits[1..1]);

            ResetAll(qubits);
        }
    }
}
```

## <a name="debugging"></a><span data-ttu-id="0bc05-219">Отладка</span><span class="sxs-lookup"><span data-stu-id="0bc05-219">Debugging</span></span>

<span data-ttu-id="0bc05-220">В поверх `Assert` и `Dump` функций и операций, Q # поддерживает подмножество стандартных возможностей отладки Visual Studio: [Задание точек останова в строке](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), [пошаговое выполнение кода с помощью клавиши F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger) и [Проверка значений классических переменных. ](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows)все это возможно во время выполнения кода в симуляторе.</span><span class="sxs-lookup"><span data-stu-id="0bc05-220">On top of `Assert` and `Dump` functions and operations, Q# supports a subset of standard Visual Studio debugging capabilities: [setting line breakpoints](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), [stepping through code using F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger) and [inspecting values of classic variables](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) are all possible during code execution on the simulator.</span></span>

<span data-ttu-id="0bc05-221">Отладка в Visual Studio Code пока не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0bc05-221">Debugging in Visual Studio Code is not yet supported.</span></span>

