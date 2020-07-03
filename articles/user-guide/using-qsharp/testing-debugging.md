---
title: Тестирование и отладка
description: Узнайте, как использовать модульные тесты, факты и утверждения и функции дампа для тестирования и отладки тактовых программ.
author: tcNickolas
ms.author: mamykhai@microsoft.com
ms.date: 06/01/2020
ms.topic: article
uid: microsoft.quantum.guide.testingdebugging
ms.openlocfilehash: cd619607af9e2b601f3bec1304c5729d84312f35
ms.sourcegitcommit: a3775921db1dc5c653c97b8fa8fe2c0ddd5261ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2020
ms.locfileid: "85884089"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="4b5fb-103">Тестирование и отладка</span><span class="sxs-lookup"><span data-stu-id="4b5fb-103">Testing and debugging</span></span>

<span data-ttu-id="4b5fb-104">Как и в случае с классическим программированием, важно иметь возможность проверять, что тактовые программы действуют как намеченные и могут диагностировать неправильное поведение.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-104">As with classical programming, it is essential to be able to check that quantum programs act as intended, and to be able to diagnose incorrect behavior.</span></span>
<span data-ttu-id="4b5fb-105">В этом разделе мы рассмотрим средства, предлагаемые Q # для тестирования и отладки тактовых программ.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-105">In this section, we cover the tools offered by Q# for testing and debugging quantum programs.</span></span>

## <a name="unit-tests"></a><span data-ttu-id="4b5fb-106">Модульные тесты</span><span class="sxs-lookup"><span data-stu-id="4b5fb-106">Unit Tests</span></span>

<span data-ttu-id="4b5fb-107">Одним из распространенных подходов к тестированию классических программ является написание небольших программ, именуемых *модульными тестами*, которые выполняют код в библиотеке и сравнивают выходные данные с ожидаемыми выходными данными.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-107">One common approach to testing classical programs is to write small programs called *unit tests*, which run code in a library and compare its output to some expected output.</span></span>
<span data-ttu-id="4b5fb-108">Например, можно гарантировать, что `Square(2)` возвраты будут возвращаться, `4` так как вы узнали *приори* , что $2 ^ 2 = $4.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-108">For example, you can ensure that `Square(2)` returns `4` since you know *a priori* that $2^2 = 4$.</span></span>

<span data-ttu-id="4b5fb-109">Q # поддерживает создание модульных тестов для тактовых программ и может выполняться как тесты в среде модульного тестирования [xUnit](https://xunit.github.io/) .</span><span class="sxs-lookup"><span data-stu-id="4b5fb-109">Q# supports creating unit tests for quantum programs, and which can run as tests within the [xUnit](https://xunit.github.io/) unit testing framework.</span></span>

### <a name="creating-a-test-project"></a><span data-ttu-id="4b5fb-110">Создание тестового проекта</span><span class="sxs-lookup"><span data-stu-id="4b5fb-110">Creating a Test Project</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="4b5fb-111">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="4b5fb-111">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="4b5fb-112">Запустите Visual Studio 2019.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-112">Open Visual Studio 2019.</span></span> <span data-ttu-id="4b5fb-113">Перейдите в меню **файл** и выберите **создать > проект...**. В правом верхнем углу найдите `Q#` и выберите шаблон **проект Q # Test** .</span><span class="sxs-lookup"><span data-stu-id="4b5fb-113">Go to the **File** menu and select **New > Project...**. In the upper right corner, search for `Q#`, and select the **Q# Test Project** template.</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="4b5fb-114">Командная строка и Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="4b5fb-114">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="4b5fb-115">В командной строке избранного выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="4b5fb-115">From your favorite command line, run the following command:</span></span>
```dotnetcli
$ dotnet new xunit -lang Q# -o Tests
$ cd Tests
$ code . # To open in Visual Studio Code
```

****

<span data-ttu-id="4b5fb-116">Новый проект содержит один файл `Tests.qs` , который предоставляет удобное место для определения новых модульных тестов Q #.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-116">Your new project has a single file `Tests.qs`, which provides a convenient place to define new Q# unit tests.</span></span>
<span data-ttu-id="4b5fb-117">Изначально этот файл содержит один пример модульного теста, `AllocateQubit` который проверяет, что вновь выделенное кубит находится в состоянии $ \кет {0} $, и выводит сообщение:</span><span class="sxs-lookup"><span data-stu-id="4b5fb-117">Initially, this file contains one sample unit test `AllocateQubit` which checks that a newly allocated qubit is in the $\ket{0}$ state and prints a message:</span></span>

```qsharp
    @Test("QuantumSimulator")
    operation AllocateQubit () : Unit {

        using (qubit = Qubit()) {
            Assert([PauliZ], [qubit], Zero, "Newly allocated qubit must be in the |0⟩ state.");
        }
        
        Message("Test passed");
    }
```

<span data-ttu-id="4b5fb-118">Любая операция или функция Q #, которая принимает аргумент типа `Unit` и возвращает, `Unit` может быть помечена как модульный тест с помощью `@Test("...")` атрибута.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-118">Any Q# operation or function that takes an argument of type `Unit` and returns `Unit` can be marked as a unit test via the `@Test("...")` attribute.</span></span> <span data-ttu-id="4b5fb-119">В предыдущем примере аргумент для этого атрибута, `"QuantumSimulator"` , указывает целевой объект, в котором выполняется тест.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-119">In the previous example, the argument to that attribute, `"QuantumSimulator"`, specifies the target on which the test runs.</span></span> <span data-ttu-id="4b5fb-120">Один тест может выполняться на нескольких целевых объектах.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-120">A single test can run on multiple targets.</span></span> <span data-ttu-id="4b5fb-121">Например, добавьте атрибут `@Test("ResourcesEstimator")` перед `AllocateQubit` .</span><span class="sxs-lookup"><span data-stu-id="4b5fb-121">For example, add an attribute `@Test("ResourcesEstimator")` before `AllocateQubit`.</span></span> 
```qsharp
    @Test("QuantumSimulator")
    @Test("ResourcesEstimator")
    operation AllocateQubit () : Unit {
        ...
```
<span data-ttu-id="4b5fb-122">Сохраните файл и выполните все тесты.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-122">Save the file and run all tests.</span></span> <span data-ttu-id="4b5fb-123">Теперь должно быть два модульных теста: один, где `AllocateQubit` выполняется в `QuantumSimulator` , и один, где он выполняется в `ResourcesEstimator` .</span><span class="sxs-lookup"><span data-stu-id="4b5fb-123">There should now be two unit tests, one where `AllocateQubit` runs on the `QuantumSimulator`, and one where it runs in the `ResourcesEstimator`.</span></span> 

<span data-ttu-id="4b5fb-124">Компилятор Q # распознает встроенные целевые объекты `"QuantumSimulator"` , `"ToffoliSimulator"` а `"ResourcesEstimator"` также допустимые целевые объекты выполнения для модульных тестов.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-124">The Q# compiler recognizes the built-in targets `"QuantumSimulator"`, `"ToffoliSimulator"`, and `"ResourcesEstimator"` as valid execution targets for unit tests.</span></span> <span data-ttu-id="4b5fb-125">Можно также указать любое полное имя для определения пользовательского целевого объекта выполнения.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-125">It is also possible to specify any fully qualified name to define a custom execution target.</span></span> 

### <a name="running-q-unit-tests"></a><span data-ttu-id="4b5fb-126">Выполнение модульных тестов Q #</span><span class="sxs-lookup"><span data-stu-id="4b5fb-126">Running Q# Unit Tests</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="4b5fb-127">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="4b5fb-127">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="4b5fb-128">В качестве одноразовой настройки для каждого решения перейдите в меню **тест** и выберите **Параметры тестирования > архитектура процессора по умолчанию > x64**.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-128">As a one-time per-solution setup, go to the **Test** menu and select **Test Settings > Default Processor Architecture > X64**.</span></span>

> [!TIP]
> <span data-ttu-id="4b5fb-129">Параметр архитектуры процессора по умолчанию для Visual Studio хранится в файле параметров решения ( `.suo` ) для каждого решения.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-129">The default processor architecture setting for Visual Studio is stored in the solution options (`.suo`) file for each solution.</span></span>
> <span data-ttu-id="4b5fb-130">При удалении этого файла необходимо снова выбрать **x64** в качестве архитектуры процессора.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-130">If you delete this file, then you need to select **X64** as your processor architecture again.</span></span>

<span data-ttu-id="4b5fb-131">Постройте проект, откройте меню **тест** и выберите **Windows > обозреватель тестов**.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-131">Build the project, open the **Test** menu, and select **Windows > Test Explorer**.</span></span> <span data-ttu-id="4b5fb-132">**Аллокатекубит** отображается в списке тестов в группе **Невыполненные тесты** .</span><span class="sxs-lookup"><span data-stu-id="4b5fb-132">**AllocateQubit** displays in the list of tests in the **Not Run Tests** group.</span></span> <span data-ttu-id="4b5fb-133">Выберите **выполнить все** или выполните этот отдельный тест.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-133">Select **Run All** or run this individual test.</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="4b5fb-134">Командная строка и Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="4b5fb-134">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="4b5fb-135">Чтобы запустить тесты, перейдите в папку проекта (папку, содержащую `Tests.csproj` ) и выполните команду:</span><span class="sxs-lookup"><span data-stu-id="4b5fb-135">To run tests, navigate to the project folder (the folder which contains `Tests.csproj`), and run the command:</span></span>

```bash
$ dotnet restore
$ dotnet test
```

<span data-ttu-id="4b5fb-136">Должен отобразиться результат, аналогичный приведенному ниже.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-136">You should get output similar to the following:</span></span>

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

<span data-ttu-id="4b5fb-137">Модульные тесты можно фильтровать в соответствии с их именем или целевым объектом выполнения:</span><span class="sxs-lookup"><span data-stu-id="4b5fb-137">Unit tests can be filtered according to their name or the execution target:</span></span>

```bash 
$ dotnet test --filter "Target=QuantumSimulator"
$ dotnet test --filter "Name=AllocateQubit"
```


***

<span data-ttu-id="4b5fb-138">Встроенная функция <xref:microsoft.quantum.intrinsic.message> имеет тип `(String -> Unit)` и позволяет создавать сообщения диагностики.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-138">The intrinsic function <xref:microsoft.quantum.intrinsic.message> has type `(String -> Unit)` and enables the creation of diagnostic messages.</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="4b5fb-139">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="4b5fb-139">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="4b5fb-140">После запуска теста в обозревателе тестов и нажатия кнопки тест отображается панель со сведениями о выполнении теста: состояние передачи/сбоя, затраченное время и ссылка на выходные данные.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-140">After you run a test in Test Explorer and click on the test, a panel displays with information about test execution: Pass/fail status, elapsed time, and a link to the output.</span></span> <span data-ttu-id="4b5fb-141">Нажмите кнопку **выходные данные** , чтобы открыть тестовый вывод в новом окне.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-141">Click **Output** to open the test output in a new window.</span></span>

![выходные данные теста](~/media/unit-test-output.png)

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="4b5fb-143">Командная строка и Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="4b5fb-143">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="4b5fb-144">Состояние "успех/сбой" для каждого теста выводится на консоль `dotnet test` .</span><span class="sxs-lookup"><span data-stu-id="4b5fb-144">The pass/fail status for each test is printed to the console by `dotnet test`.</span></span>
<span data-ttu-id="4b5fb-145">Для неудачных тестов выходные данные также выводятся на консоль для облегчения диагностики сбоя.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-145">For failing tests, the outputs are also printed to the console to help diagnose the failure.</span></span>

***

## <a name="facts-and-assertions"></a><span data-ttu-id="4b5fb-146">Факты и утверждения</span><span class="sxs-lookup"><span data-stu-id="4b5fb-146">Facts and Assertions</span></span>

<span data-ttu-id="4b5fb-147">Поскольку функции в Q # не имеют _логических_ побочных эффектов, вы никогда не можете наблюдать за тем, что из программы Q # другие виды эффектов запуска функции, тип вывода которой является пустым кортежем `()` .</span><span class="sxs-lookup"><span data-stu-id="4b5fb-147">Because functions in Q# have no _logical_ side effects, you can never observe, from within a Q# program, any other kinds of effects from running a function whose output type is the empty tuple `()`.</span></span>
<span data-ttu-id="4b5fb-148">Это значит, что целевой компьютер может не выполнять какую-либо функцию, которая возвращает, `()` что это не приведет к изменению поведения любого следующего кода Q #.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-148">That is, a target machine can choose not to run any function which returns `()` with the guarantee that this omission will not modify the behavior of any following Q# code.</span></span>
<span data-ttu-id="4b5fb-149">Это поведение позволяет функциям возвращать `()` (например, `Unit` ) полезные средства для внедрения утверждений и логики отладки в программы Q #.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-149">This behavior makes functions returning `()` (such as `Unit`) a useful tool for embedding assertions and debugging logic into Q# programs.</span></span> 

<span data-ttu-id="4b5fb-150">Рассмотрим простой пример:</span><span class="sxs-lookup"><span data-stu-id="4b5fb-150">Let's consider a simple example:</span></span>

```qsharp
function PositivityFact(value : Double) : Unit 
{
    if (value <= 0) 
    {
        fail "Expected a positive number.";
    }
}
```

<span data-ttu-id="4b5fb-151">Здесь ключевое слово `fail` указывает, что вычисление не должно выполняться, и создает исключение на целевом компьютере, на котором выполняется программа Q #.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-151">Here, the keyword `fail` indicates that the computation should not proceed, and raises an exception in the target machine running the Q# program.</span></span>
<span data-ttu-id="4b5fb-152">По определению, сбой этого вида не может рассматриваться в Q #, так как целевой компьютер больше не выполняет код Q # после достижения `fail` инструкции.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-152">By definition, a failure of this kind cannot be observed from within Q#, as the target machine no longer runs the Q# code after reaching a `fail` statement.</span></span>
<span data-ttu-id="4b5fb-153">Таким же, если мы выполним вызов `PositivityFact` , мы можем быть уверены, что его входные данные были положительными.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-153">Thus, if we proceed past a call to `PositivityFact`, we can be assured that its input was positive.</span></span>

<span data-ttu-id="4b5fb-154">Обратите внимание, что мы можем реализовать такое же поведение, как и при `PositivityFact` использовании [`Fact`](xref:microsoft.quantum.diagnostics.fact) функции из <xref:microsoft.quantum.diagnostics> пространства имен:</span><span class="sxs-lookup"><span data-stu-id="4b5fb-154">Note that we can implement the same behavior as `PositivityFact` using the [`Fact`](xref:microsoft.quantum.diagnostics.fact) function from the <xref:microsoft.quantum.diagnostics> namespace:</span></span>

```qsharp
    Fact(value > 0, "Expected a positive number.");
```

<span data-ttu-id="4b5fb-155">*Утверждения*, с другой стороны, используются аналогично факту, но могут зависеть от состояния целевого компьютера.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-155">*Assertions*, on the other hand, are used similarly to facts but may depend on the state of the target machine.</span></span> <span data-ttu-id="4b5fb-156">Соответственно, они определяются как операции, тогда как факты определяются как функции (как в предыдущем примере).</span><span class="sxs-lookup"><span data-stu-id="4b5fb-156">Correspondingly, they are defined as operations, whereas facts are defined as functions (as in the previous example).</span></span>
<span data-ttu-id="4b5fb-157">Чтобы понять различие, рассмотрим следующее применение факта в утверждении:</span><span class="sxs-lookup"><span data-stu-id="4b5fb-157">To understand the distinction, consider the following use of a fact within an assertion:</span></span>

```qsharp
operation AssertQubitsAreAvailable() : Unit
{
     Fact(GetQubitsAvailableToUse() > 0, "No qubits were actually available");
}
```

<span data-ttu-id="4b5fb-158">Здесь мы используем операцию, <xref:microsoft.quantum.environment.getqubitsavailabletouse> чтобы вернуть количество Кубитс, доступных для использования.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-158">Here, we are using the operation <xref:microsoft.quantum.environment.getqubitsavailabletouse> to return the number of qubits available to use.</span></span>
<span data-ttu-id="4b5fb-159">Так как это зависит от глобального состояния программы и среды выполнения, наше определение `AssertQubitsAreAvailable` должно также быть операцией.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-159">As this depends on the global state of the program and its execution environment, our definition of `AssertQubitsAreAvailable` must be an operation as well.</span></span>
<span data-ttu-id="4b5fb-160">Однако можно использовать это глобальное состояние, чтобы получить простое значение в `Bool` качестве входных данных для `Fact` функции.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-160">However, we can use that global state to yield a simple `Bool` value as input to the `Fact` function.</span></span>

<span data-ttu-id="4b5fb-161">[Версионного](xref:microsoft.quantum.libraries.standard.prelude), основываясь на этих идеях, предлагает два особенно полезных утверждения, <xref:microsoft.quantum.intrinsic.assert> которые <xref:microsoft.quantum.intrinsic.assertprob> моделируются как операции `()` .</span><span class="sxs-lookup"><span data-stu-id="4b5fb-161">[The prelude](xref:microsoft.quantum.libraries.standard.prelude), building on these ideas, offers two especially useful assertions, <xref:microsoft.quantum.intrinsic.assert> and <xref:microsoft.quantum.intrinsic.assertprob> both modeled as operations onto `()`.</span></span> <span data-ttu-id="4b5fb-162">Каждый из этих утверждений принимает Оператор Паули, описывающий определенное измерение интересов, тактовый регистр, на котором выполняется измерение, и гипотетический результат.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-162">These assertions each take a Pauli operator describing a particular measurement of interest, a quantum register on which a measurement is performed, and a hypothetical outcome.</span></span>
<span data-ttu-id="4b5fb-163">Целевые компьютеры, работающие с имитацией, не привязаны [к Теорема без клонирования](https://en.wikipedia.org/wiki/No-cloning_theorem)и могут выполнять такие измерения, не нарушая регистр, который передается в такие утверждения.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-163">Target machines which work by simulation are not bound by [the no-cloning theorem](https://en.wikipedia.org/wiki/No-cloning_theorem), and can perform such measurements without disturbing the register that passes to such assertions.</span></span>
<span data-ttu-id="4b5fb-164">Симулятор может, как и `PositivityFact` функция Previous, прекращать вычисление, если гипотетический результат не наблюдается на практике:</span><span class="sxs-lookup"><span data-stu-id="4b5fb-164">A simulator can then, similar to the `PositivityFact` function previous, stop computation if the hypothetical outcome is not observed in practice:</span></span>

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

<span data-ttu-id="4b5fb-165">На оборудовании физического такта, где Теорема без клонирования предотвращает исследование состояния такта, `Assert` операции и просто возвращают без какого-либо `AssertProb` `()` другого действия.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-165">On physical quantum hardware, where the no-cloning theorem prevents examination of a quantum state, the `Assert` and `AssertProb` operations simply return `()` with no other effect.</span></span>

<span data-ttu-id="4b5fb-166"><xref:microsoft.quantum.diagnostics>Пространство имен предоставляет несколько дополнительных функций `Assert` семейства, с помощью которых можно проверить более сложные условия.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-166">The <xref:microsoft.quantum.diagnostics> namespace provides several more functions of the `Assert` family, with which you can check more advanced conditions.</span></span> 

## <a name="dump-functions"></a><span data-ttu-id="4b5fb-167">Функции дампа</span><span class="sxs-lookup"><span data-stu-id="4b5fb-167">Dump Functions</span></span>

<span data-ttu-id="4b5fb-168">Для облегчения устранения неполадок в тактовых программах <xref:microsoft.quantum.diagnostics> пространство имен предлагает две функции, которые могут выводить дамп в файл текущее состояние целевого компьютера: <xref:microsoft.quantum.diagnostics.dumpmachine> и <xref:microsoft.quantum.diagnostics.dumpregister> .</span><span class="sxs-lookup"><span data-stu-id="4b5fb-168">To help troubleshooting quantum programs, the <xref:microsoft.quantum.diagnostics> namespace offers two functions that can dump into a file the current status of the target machine: <xref:microsoft.quantum.diagnostics.dumpmachine> and <xref:microsoft.quantum.diagnostics.dumpregister>.</span></span> <span data-ttu-id="4b5fb-169">Созданные выходные данные каждого из них зависят от целевого компьютера.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-169">The generated output of each depends on the target machine.</span></span>

### <a name="dumpmachine"></a><span data-ttu-id="4b5fb-170">DumpMachine</span><span class="sxs-lookup"><span data-stu-id="4b5fb-170">DumpMachine</span></span>

<span data-ttu-id="4b5fb-171">Симулятор такта с полным состоянием, распространяемый в составе пакета разработки тактов, записывает в файл [функцию Wave](https://en.wikipedia.org/wiki/Wave_function) всей тактовой системы, в виде одномерного массива комплексных чисел, в котором каждый элемент представляет амплитуду вероятности измерения вычислительного состояния $ \кет{н} $, где $ \кет{н} = \кет{B_ {n-1}... b_1b_0} $ для BITS $ \{ b_i \} $.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-171">The full-state quantum simulator distributed as part of the Quantum Development Kit writes into the file the [wave function](https://en.wikipedia.org/wiki/Wave_function) of the entire quantum system, as a one-dimensional array of complex numbers, in which each element represents the amplitude of the probability of measuring the computational basis state $\ket{n}$, where $\ket{n} = \ket{b_{n-1}...b_1b_0}$ for bits $\{b_i\}$.</span></span> <span data-ttu-id="4b5fb-172">Например, на компьютере, где только два выделенных Кубитс и в состоянии такта $ $ \бегин{алигн} \кет{\пси} = \фрак {1} {\скрт {2} } \кет {00} -\фрак{(1 + i)} {2} \кет {10} , \енд{алигн} $ $ вызов <xref:microsoft.quantum.diagnostics.dumpmachine> создает этот результат:</span><span class="sxs-lookup"><span data-stu-id="4b5fb-172">For example, on a machine with only two qubits allocated and in the quantum state $$ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10}, \end{align} $$ calling <xref:microsoft.quantum.diagnostics.dumpmachine> generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 0;1
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣2❭:    -0.500000 + -0.500000 i  ==     **********           [ 0.500000 ]   /     [ -2.35619 rad ]
∣3❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

<span data-ttu-id="4b5fb-173">Первая строка содержит комментарий с идентификаторами соответствующего Кубитс в значительном порядке.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-173">The first row provides a comment with the ids of the corresponding qubits in their significant order.</span></span>
<span data-ttu-id="4b5fb-174">Остальные строки описывают амплитуду вероятности по измерению вектора состояния базы данных $ \кет{н} $ в декартовой и полярной форматах.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-174">The rest of the rows describe the probability amplitude of measuring the basis state vector $\ket{n}$ in both Cartesian and polar formats.</span></span> <span data-ttu-id="4b5fb-175">Подробно для первой строки:</span><span class="sxs-lookup"><span data-stu-id="4b5fb-175">In detail for the first row:</span></span>

* <span data-ttu-id="4b5fb-176">**`∣0❭:`** Эта строка соответствует `0` состоянию вычислительного основания</span><span class="sxs-lookup"><span data-stu-id="4b5fb-176">**`∣0❭:`** this row corresponds to the `0` computational basis state</span></span>
* <span data-ttu-id="4b5fb-177">**`0.707107 +  0.000000 i`**: амплитуда вероятности в формате Декарт.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-177">**`0.707107 +  0.000000 i`**: the probability amplitude in Cartesian format.</span></span>
* <span data-ttu-id="4b5fb-178">**` == `**: `equal` знак разделяет оба эквивалентных представления.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-178">**` == `**: the `equal` sign separates both equivalent representations.</span></span>
* <span data-ttu-id="4b5fb-179">**`**********  `**: Графическое представление величины, количество `*` пропорционально вероятности измерения этого вектора состояния.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-179">**`**********  `**: A graphical representation of the magnitude, the number of `*` is proportionate to the probability of measuring this state vector.</span></span>
* <span data-ttu-id="4b5fb-180">**`[ 0.500000 ]`**: числовое значение величины.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-180">**`[ 0.500000 ]`**: the numeric value of the magnitude</span></span>
* <span data-ttu-id="4b5fb-181">**`    ---`**: Графическое представление фазы амплитуды (см. следующие выходные данные).</span><span class="sxs-lookup"><span data-stu-id="4b5fb-181">**`    ---`**: A graphical representation of the amplitude's phase (see the following output).</span></span>
* <span data-ttu-id="4b5fb-182">**`[ 0.0000 rad ]`**: числовое значение этапа (в радианах).</span><span class="sxs-lookup"><span data-stu-id="4b5fb-182">**`[ 0.0000 rad ]`**: the numeric value of the phase (in radians).</span></span>

<span data-ttu-id="4b5fb-183">Как величина, так и фаза отображаются с графическим представлением.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-183">Both the magnitude and the phase are displayed with a graphical representation.</span></span> <span data-ttu-id="4b5fb-184">Представление величины прямо вперед: в нем отображается полоска `*` , чем больше вероятность, чем увеличено на полосе.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-184">The magnitude representation is straight-forward: it shows a bar of `*`, the bigger the probability the bigger the bar will be.</span></span> <span data-ttu-id="4b5fb-185">Для этапа показаны следующие символы, представляющие угол на основе диапазонов:</span><span class="sxs-lookup"><span data-stu-id="4b5fb-185">For the phase, we show the following symbols to represent the angle based on ranges:</span></span>

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

<span data-ttu-id="4b5fb-186">В следующих примерах показаны `DumpMachine` некоторые распространенные состояния.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-186">The following examples show `DumpMachine` for some common states:</span></span>

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
  > <span data-ttu-id="4b5fb-187">Идентификатор кубит назначается во время выполнения и не обязательно соответствует порядку выделения кубит или его позиции в кубит регистре.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-187">The id of a qubit is assigned at runtime and is not necessarily aligned with the order in which the qubit was allocated or its position within a qubit register.</span></span>


#### <a name="visual-studio-2019"></a>[<span data-ttu-id="4b5fb-188">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="4b5fb-188">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

  > [!TIP]
  > <span data-ttu-id="4b5fb-189">Идентификатор кубит можно указать в Visual Studio, поместив точку останова в код и проверив значение переменной кубит, например:</span><span class="sxs-lookup"><span data-stu-id="4b5fb-189">You can locate a qubit id in Visual Studio by putting a breakpoint in your code and inspecting the value of a qubit variable, for example:</span></span>
  > 
  > ![показывать идентификатор кубит в Visual Studio](~/media/qubit_id.png)
  >
  > <span data-ttu-id="4b5fb-191">Кубит с индексом `0` с `register2` идентификатором ID = `3` , кубит с индексом `1` ID = `2` .</span><span class="sxs-lookup"><span data-stu-id="4b5fb-191">the qubit with index `0` on `register2` has id=`3`, the qubit with index `1` has id=`2`.</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="4b5fb-192">Командная строка и Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="4b5fb-192">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

  > [!TIP]
  > <span data-ttu-id="4b5fb-193">Вы можете узнать идентификатор кубит с помощью <xref:microsoft.quantum.intrinsic.message> функции и передать переменную кубит в сообщении, например:</span><span class="sxs-lookup"><span data-stu-id="4b5fb-193">You can locate a qubit id by using the <xref:microsoft.quantum.intrinsic.message> function and passing the qubit variable in the message, for example:</span></span>
  >
  > ```qsharp
  > Message($"0={register2[0]}; 1={register2[1]}");
  > ```
  > 
  > <span data-ttu-id="4b5fb-194">которые могут формировать этот результат:</span><span class="sxs-lookup"><span data-stu-id="4b5fb-194">which could generate this output:</span></span>
  >```
  > 0=q:3; 1=q:2
  >```
  > <span data-ttu-id="4b5fb-195">Это означает, что кубит с индексом с `0` `register2` идентификатором ID = `3` , кубит с индексом `1` ID = `2` .</span><span class="sxs-lookup"><span data-stu-id="4b5fb-195">which means that the qubit with index `0` on `register2` has id=`3`, the qubit with index `1` has id=`2`.</span></span>


***

<span data-ttu-id="4b5fb-196">Поскольку <xref:microsoft.quantum.diagnostics.dumpmachine> является частью <xref:microsoft.quantum.diagnostics> пространства имен, необходимо добавить `open` оператор для доступа к нему:</span><span class="sxs-lookup"><span data-stu-id="4b5fb-196">Since <xref:microsoft.quantum.diagnostics.dumpmachine> is part of the  <xref:microsoft.quantum.diagnostics> namespace, you must add an `open` statement to access it:</span></span>

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


### <a name="dumpregister"></a><span data-ttu-id="4b5fb-197">DumpRegister</span><span class="sxs-lookup"><span data-stu-id="4b5fb-197">DumpRegister</span></span>

<span data-ttu-id="4b5fb-198"><xref:microsoft.quantum.diagnostics.dumpregister>работает <xref:microsoft.quantum.diagnostics.dumpmachine> , как, за исключением того, что он также принимает массив Кубитс, чтобы ограничить объем информации, относящейся только к соответствующему Кубитс.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-198"><xref:microsoft.quantum.diagnostics.dumpregister> works like <xref:microsoft.quantum.diagnostics.dumpmachine>, except that it also takes an array of qubits to limit the amount of information to only that relevant to the corresponding qubits.</span></span>

<span data-ttu-id="4b5fb-199">Как и в <xref:microsoft.quantum.diagnostics.dumpmachine> случае, сведения, созданные в, <xref:microsoft.quantum.diagnostics.dumpregister> зависят от целевого компьютера.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-199">As with <xref:microsoft.quantum.diagnostics.dumpmachine>, the information generated by <xref:microsoft.quantum.diagnostics.dumpregister> depends on the target machine.</span></span> <span data-ttu-id="4b5fb-200">Для имитатора с полным состоянием он записывает в файл функцию Wave вплоть до глобального этапа подсистемы такта, созданной предоставленным Кубитс в том же формате, что и <xref:microsoft.quantum.diagnostics.dumpmachine> .</span><span class="sxs-lookup"><span data-stu-id="4b5fb-200">For the full-state quantum simulator it writes into the file the wave function up to a global phase of the quantum sub-system generated by the provided qubits in the same format as <xref:microsoft.quantum.diagnostics.dumpmachine>.</span></span>  <span data-ttu-id="4b5fb-201">Например, повторите попытку на компьютере с двумя выделенными Кубитс и в состоянии такта $ $ \бегин{алигн} \кет{\пси} = \фрак {1} {\скрт {2} } \кет {00} -\фрак{(1 + i)} {2} \кет {10} =-e ^ {-i \ PI/4} ((\фрак {1} {\скрт {2} } \кет {0} -\фрак{(1 + i)} {2} \кет {1} ) \otimes \frac{-(1 + i)} {\sqrt {2} } \ket {0} ). \end{align} $ $ вызов метода <xref:microsoft.quantum.diagnostics.dumpregister> для `qubit[0]` создает следующий результат:</span><span class="sxs-lookup"><span data-stu-id="4b5fb-201">For example, take again a machine with only two qubits allocated and in the quantum state $$ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10} = - e^{-i\pi/4} ( (\frac{1}{\sqrt{2}} \ket{0} - \frac{(1 + i)}{2} \ket{1} ) \otimes \frac{-(1 + i)}{\sqrt{2}} \ket{0} ) , \end{align} $$ calling <xref:microsoft.quantum.diagnostics.dumpregister> for `qubit[0]` generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:    -0.707107 + -0.707107 i  ==     ******************** [ 1.000000 ]  /      [ -2.35619 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

<span data-ttu-id="4b5fb-202">и вызов метода <xref:microsoft.quantum.diagnostics.dumpregister> для `qubit[1]` создает следующие выходные данные:</span><span class="sxs-lookup"><span data-stu-id="4b5fb-202">and calling <xref:microsoft.quantum.diagnostics.dumpregister> for `qubit[1]` generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 1
∣0❭:     0.707107 +  0.000000 i  ==     ***********          [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:    -0.500000 + -0.500000 i  ==     ***********          [ 0.500000 ]  /      [ -2.35619 rad ]
```

<span data-ttu-id="4b5fb-203">Как правило, состояние регистра, запутанными с другим регистром, находится в смешанном состоянии, а не в чистом состоянии.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-203">In general, the state of a register that is entangled with another register is a mixed state rather than a pure state.</span></span> <span data-ttu-id="4b5fb-204">В этом случае <xref:microsoft.quantum.diagnostics.dumpregister> выводит следующее сообщение:</span><span class="sxs-lookup"><span data-stu-id="4b5fb-204">In this case, <xref:microsoft.quantum.diagnostics.dumpregister> outputs the following message:</span></span>

```
Qubits provided (0;) are entangled with some other qubit.
```

<span data-ttu-id="4b5fb-205">В следующем примере показано, как можно использовать <xref:microsoft.quantum.diagnostics.dumpregister> и <xref:microsoft.quantum.diagnostics.dumpmachine> в коде Q #:</span><span class="sxs-lookup"><span data-stu-id="4b5fb-205">The following example shows you how you can use both <xref:microsoft.quantum.diagnostics.dumpregister> and <xref:microsoft.quantum.diagnostics.dumpmachine> in your Q# code:</span></span>

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

## <a name="debugging"></a><span data-ttu-id="4b5fb-206">Отладка</span><span class="sxs-lookup"><span data-stu-id="4b5fb-206">Debugging</span></span>

<span data-ttu-id="4b5fb-207">Поверх `Assert` функций и `Dump` операций, Q # поддерживает подмножество стандартных возможностей отладки Visual Studio: [Установка точек останова в строке](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), [пошаговое выполнение кода с помощью клавиши F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger)и [Проверка значений классических переменных](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) во время выполнения кода в симуляторе.</span><span class="sxs-lookup"><span data-stu-id="4b5fb-207">On top of `Assert` and `Dump` functions and operations, Q# supports a subset of standard Visual Studio debugging capabilities: [setting line breakpoints](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), [stepping through code using F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger), and [inspecting values of classic variables](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) are all possible during code execution on the simulator.</span></span>

<span data-ttu-id="4b5fb-208">Отладка в Visual Studio Code использует возможности отладки, предоставляемые C# для Visual Studio Code расширения на базе OmniSharp и требует установки [последней версии](https://marketplace.visualstudio.com/items?itemName=ms-vscode.csharp).</span><span class="sxs-lookup"><span data-stu-id="4b5fb-208">Debugging in Visual Studio Code leverages the debugging capabilities provided by the C# for Visual Studio Code extension powered by OmniSharp and requires installing the [latest version](https://marketplace.visualstudio.com/items?itemName=ms-vscode.csharp).</span></span> 
