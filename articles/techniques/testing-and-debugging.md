---
title: Тестирование и отладка программ
description: Узнайте, как использовать модульные тесты, факты и утверждения, а также функции сброса для тестирования и отладки квантовых программ.
author: tcNickolas
ms.author: mamykhai@microsoft.com
uid: microsoft.quantum.techniques.testing-and-debugging
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: caf15b7273b7efed1da87a2edd62c06cd4357593
ms.sourcegitcommit: b6b8459eb654040f1e19f66411b29fc9e48e95c9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2020
ms.locfileid: "82030588"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="e2c3b-103">Тестирование и отладка</span><span class="sxs-lookup"><span data-stu-id="e2c3b-103">Testing and Debugging</span></span>

<span data-ttu-id="e2c3b-104">Как и в классическом программировании, важно иметь возможность проверить, что квантовые программы действуют так, как предполагалось, и быть в состоянии диагностировать квантовую программу, которая неверна.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-104">As with classical programming, it is essential to be able to check that quantum programs act as intended, and to be able to diagnose a quantum program that is incorrect.</span></span>
<span data-ttu-id="e2c3b-105">В этом разделе мы рассмотрим инструменты, предлагаемые «Зенитом» для тестирования и отладки квантовых программ.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-105">In this section, we cover the tools offered by Q# for testing and debugging quantum programs.</span></span>

## <a name="unit-tests"></a><span data-ttu-id="e2c3b-106">Модульные тесты</span><span class="sxs-lookup"><span data-stu-id="e2c3b-106">Unit Tests</span></span>

<span data-ttu-id="e2c3b-107">Один из распространенных подходов к тестированию классических программ заключается в написании небольших программ, называемых *модульных тестов,* которые заражают код в библиотеке, и сравнивают его выход с ожидаемым выходом.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-107">One common approach to testing classical programs is to write small programs called *unit tests* which run code in a library and compare its output to some expected output.</span></span>
<span data-ttu-id="e2c3b-108">Например, мы можем захотеть, чтобы убедиться, что `Square(2)` возвращается, `4`так как мы *знаем, априори,* что $ 2 и 4 $ 4 .</span><span class="sxs-lookup"><span data-stu-id="e2c3b-108">For instance, we may want to ensure that `Square(2)` returns `4`, since we know *a priori* that $2^2 = 4$.</span></span>

<span data-ttu-id="e2c3b-109">Поддерживает создание модульных тестов для квантовых программ, которые могут быть выполнены в качестве тестов в рамках модульного тестирования [xUnit.](https://xunit.github.io/)</span><span class="sxs-lookup"><span data-stu-id="e2c3b-109">Q# supports creating unit tests for quantum programs, and which can be executed as tests within the [xUnit](https://xunit.github.io/) unit testing framework.</span></span>

### <a name="creating-a-test-project"></a><span data-ttu-id="e2c3b-110">Создание тестового проекта</span><span class="sxs-lookup"><span data-stu-id="e2c3b-110">Creating a Test Project</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="e2c3b-111">Визуальная студия 2019</span><span class="sxs-lookup"><span data-stu-id="e2c3b-111">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="e2c3b-112">Откройте Visual Studio 2019.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-112">Open Visual Studio 2019.</span></span> <span data-ttu-id="e2c3b-113">Перейти `File` в меню `New`  >  `Project...`и выбрать .</span><span class="sxs-lookup"><span data-stu-id="e2c3b-113">Go to the `File` menu and select `New` > `Project...`.</span></span>
<span data-ttu-id="e2c3b-114">В правом верхнем углу `Q#`ивыберите `Q# Test Project` шаблон.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-114">In the upper right corner, search for `Q#`, and select the `Q# Test Project` template.</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="e2c3b-115">Командная строка и Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="e2c3b-115">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="e2c3b-116">Из вашей любимой командной строки выполнить следующую команду:</span><span class="sxs-lookup"><span data-stu-id="e2c3b-116">From your favorite command line, run the following command:</span></span>
```bash
$ dotnet new xunit -lang Q# -o Tests
$ cd Tests
$ code . # To open in Visual Studio Code
```

****

<span data-ttu-id="e2c3b-117">Ваш новый проект будет `Tests.qs`иметь единый файл, который обеспечивает удобное место для определения новых модульных тестов.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-117">Your new project will have a single file `Tests.qs`, which provides a convenient place to define new Q# unit tests.</span></span>
<span data-ttu-id="e2c3b-118">Первоначально этот файл содержит `AllocateQubit` один образец модульного теста, который проверяет,{0}что вновь выделенный кубит находится в состоянии $ $ и печатает сообщение:</span><span class="sxs-lookup"><span data-stu-id="e2c3b-118">Initially this file contains one sample unit test `AllocateQubit` which checks that a newly allocated qubit is in the $\ket{0}$ state and prints a message:</span></span>

```qsharp
    @Test("QuantumSimulator")
    operation AllocateQubit () : Unit {

        using (qubit = Qubit()) {
            Assert([PauliZ], [qubit], Zero, "Newly allocated qubit must be in the |0⟩ state.");
        }
        
        Message("Test passed");
    }
```

<span data-ttu-id="e2c3b-119">:новое: Любая операция или функция, которая `Unit` принимает `Unit` аргумент типа и возвращает `@Test("...")` сярприза, может быть помечена как модульный тест через атрибут.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-119">:new: Any Q# operation or function that takes an argument of type `Unit` and returns `Unit` can be marked as a unit test via the `@Test("...")` attribute.</span></span> <span data-ttu-id="e2c3b-120">Аргумент к этому `"QuantumSimulator"` атрибуту, выше, определяет цель, на которой выполняется тест.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-120">The argument to that attribute, `"QuantumSimulator"` above, specifies the target on which the test is executed.</span></span> <span data-ttu-id="e2c3b-121">Один тест может быть выполнен на нескольких мишенях.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-121">A single test can be executed on multiple targets.</span></span> <span data-ttu-id="e2c3b-122">Например, добавьте `@Test("ResourcesEstimator")` `AllocateQubit`атрибут выше .</span><span class="sxs-lookup"><span data-stu-id="e2c3b-122">For example, add an attribute `@Test("ResourcesEstimator")` above `AllocateQubit`.</span></span> 
```qsharp
    @Test("QuantumSimulator")
    @Test("ResourcesEstimator")
    operation AllocateQubit () : Unit {
        ...
```
<span data-ttu-id="e2c3b-123">Сохранить файл и выполнить все тесты.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-123">Save the file and execute all tests.</span></span> <span data-ttu-id="e2c3b-124">Теперь должно быть два модульных теста, один из которых выполняется на Квантовом Симуляторе, и один, где он выполняется в ResourceEstimator.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-124">There should now be two unit tests, one where AllocateQubit is executed on the QuantumSimulator, and one where it is executed in the ResourceEstimator.</span></span> 

<span data-ttu-id="e2c3b-125">Компилятор распознает встроенные цели «КвантоваяСимулятор», «ToffoliSimulator» и «ResourcesEstimator» в качестве действительных целей выполнения для модульных тестов.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-125">The Q# compiler recognizes the built-in targets "QuantumSimulator", "ToffoliSimulator", and "ResourcesEstimator" as valid execution targets for unit tests.</span></span> <span data-ttu-id="e2c3b-126">Также можно указать любое полностью квалифицированное имя для определения пользовательской цели выполнения.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-126">It is also possible to specify any fully qualified name to define a custom execution target.</span></span> 

### <a name="running-q-unit-tests"></a><span data-ttu-id="e2c3b-127">Запуск юнитовых тестов</span><span class="sxs-lookup"><span data-stu-id="e2c3b-127">Running Q# Unit Tests</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="e2c3b-128">Визуальная студия 2019</span><span class="sxs-lookup"><span data-stu-id="e2c3b-128">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="e2c3b-129">В качестве одноразовой установки за `Test` решение, `Test Settings`  >  `Default Processor Architecture`  > перейдите в меню и выберите. `X64`</span><span class="sxs-lookup"><span data-stu-id="e2c3b-129">As a one-time per-solution setup, go to `Test` menu and select `Test Settings` > `Default Processor Architecture` > `X64`.</span></span>

> [!TIP]
> <span data-ttu-id="e2c3b-130">Настройка архитектуры процессора по умолчанию для`.suo`Visual Studio хранится в вариантах решения () файл для каждого решения.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-130">The default processor architecture setting for Visual Studio is stored in the solution options (`.suo`) file for each solution.</span></span>
> <span data-ttu-id="e2c3b-131">Если вы удалите этот файл, `X64` то вам нужно будет выбрать в качестве архитектуры процессора снова.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-131">If you delete this file, then you will need to select `X64` as your processor architecture again.</span></span>

<span data-ttu-id="e2c3b-132">Создайте проект, перейдите `Test` в `Windows`  >  `Test Explorer`меню и выберите .</span><span class="sxs-lookup"><span data-stu-id="e2c3b-132">Build the project, go to the `Test` menu and select `Windows` > `Test Explorer`.</span></span> <span data-ttu-id="e2c3b-133">`AllocateQubit`появится в списке тестов в `Not Run Tests` группе.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-133">`AllocateQubit` will show up in the list of tests in the `Not Run Tests` group.</span></span> <span data-ttu-id="e2c3b-134">Выберите `Run All` или запустите этот индивидуальный тест, и он должен пройти!</span><span class="sxs-lookup"><span data-stu-id="e2c3b-134">Select `Run All` or run this individual test, and it should pass!</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="e2c3b-135">Командная строка и Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="e2c3b-135">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="e2c3b-136">Для выполнения тестов перейдите в папку проекта `Tests.csproj`(папку, содержащую) и выполнить команду:</span><span class="sxs-lookup"><span data-stu-id="e2c3b-136">To run tests, navigate to the project folder (the folder which contains `Tests.csproj`), and execute the command:</span></span>

```bash
$ dotnet restore
$ dotnet test
```

<span data-ttu-id="e2c3b-137">Должен отобразиться результат, аналогичный приведенному ниже.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-137">You should get output similar to the following:</span></span>

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

<span data-ttu-id="e2c3b-138">Единие тесты могут быть отфильтрованы в зависимости от их имени и/или цели выполнения:</span><span class="sxs-lookup"><span data-stu-id="e2c3b-138">Unit tests can be filtered according to their name and/or the execution target:</span></span>

```bash 
$ dotnet test --filter "Target=QuantumSimulator"
$ dotnet test --filter "Name=AllocateQubit"
```


***

<span data-ttu-id="e2c3b-139">Внутренняя функция <xref:microsoft.quantum.intrinsic.message> имеет тип `(String -> Unit)` и позволяет создавать диагностические сообщения.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-139">The intrinsic function <xref:microsoft.quantum.intrinsic.message> has type `(String -> Unit)` and enables the creation of diagnostic messages.</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="e2c3b-140">Визуальная студия 2019</span><span class="sxs-lookup"><span data-stu-id="e2c3b-140">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="e2c3b-141">После выполнения теста в тестовом explorer и нажатия на тест появится панель с информацией о выполнении теста: Пройденный/Невыполненный статус, прошедшее время и ссылка "Выход".</span><span class="sxs-lookup"><span data-stu-id="e2c3b-141">After you execute a test in Test Explorer and click on the test, a panel will appear with information about test execution: Passed/Failed status, elapsed time and an "Output" link.</span></span> <span data-ttu-id="e2c3b-142">При нажатии на ссылку "Выход" результат теста откроется в новом окне.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-142">If you click the "Output" link, test output will open in a new window.</span></span>

![выход теста](~/media/unit-test-output.png)

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="e2c3b-144">Командная строка и Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="e2c3b-144">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="e2c3b-145">Статус пропуска/неудачи для каждого теста печатается на консоли `dotnet test`.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-145">The pass/fail status for each test is printed to the console by `dotnet test`.</span></span>
<span data-ttu-id="e2c3b-146">Для неудачных тестов выходы также печатаются на консоли, чтобы помочь диагностировать сбой.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-146">For failing tests, the outputs are also printed to the console to help diagnose the failure.</span></span>

***

## <a name="facts-and-assertions"></a><span data-ttu-id="e2c3b-147">Факты и утверждения</span><span class="sxs-lookup"><span data-stu-id="e2c3b-147">Facts and Assertions</span></span>

<span data-ttu-id="e2c3b-148">Так как функции в «Кью» не имеют _логических_ побочных эффектов, любые `()` _другие виды_ эффектов выполнения функции, тип вывода которой является пустым tuple, никогда не могут наблюдаться в рамках программы.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-148">Because functions in Q# have no _logical_ side effects, any _other kinds_ of effects of executing a function whose output type is the empty tuple `()` can never be observed from within a Q# program.</span></span>
<span data-ttu-id="e2c3b-149">То есть, целевая машина может выбрать `()` не выполнять любую функцию, которая возвращается с гарантией того, что это упущение не изменит поведение любого следующего кода.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-149">That is, a target machine can choose not to execute any function which returns `()` with the guarantee that this omission will not modify the behavior of any following Q# code.</span></span>
<span data-ttu-id="e2c3b-150">Это делает `()` возвращение функций `Unit`(т.е.) полезным инструментом для встраивания утверждений и отладки логики в программы.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-150">This makes functions returning `()` (i.e. `Unit`) a useful tool for embedding assertions and debugging logic into Q# programs.</span></span> 

<span data-ttu-id="e2c3b-151">Рассмотрим простой пример:</span><span class="sxs-lookup"><span data-stu-id="e2c3b-151">Let's consider a simple example:</span></span>

```qsharp
function PositivityFact(value : Double) : Unit 
{
    if (value <= 0) 
    {
        fail "Expected a positive number.";
    }
}
```

<span data-ttu-id="e2c3b-152">В данном случае `fail` ключевое слово указывает на то, что вычисление не должно продолжаться, что приводит к исключению в целевой машине, работающей в программе.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-152">Here, the keyword `fail` indicates that the computation should not proceed, raising an exception in the target machine running the Q# program.</span></span>
<span data-ttu-id="e2c3b-153">По определению, сбой такого рода не может наблюдаться изнутри, так `fail` как после достижения оператора код не запускается.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-153">By definition, a failure of this kind cannot be observed from within Q#, as no further Q# code is run after a `fail` statement is reached.</span></span>
<span data-ttu-id="e2c3b-154">Таким образом, если мы `PositivityFact`протянем мимо призыва к, мы можем быть уверены, что его вклад был положительным.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-154">Thus, if we proceed past a call to `PositivityFact`, we can be assured by that its input was positive.</span></span>

<span data-ttu-id="e2c3b-155">Обратите внимание, что мы `PositivityFact` можем [`Fact`](xref:microsoft.quantum.diagnostics.fact) реализовать то <xref:microsoft.quantum.diagnostics> же поведение, что и использование функции из пространства имен:</span><span class="sxs-lookup"><span data-stu-id="e2c3b-155">Note that we can implement the same behavior as `PositivityFact` using the [`Fact`](xref:microsoft.quantum.diagnostics.fact) function from the <xref:microsoft.quantum.diagnostics> namespace:</span></span>

```qsharp
    Fact(value > 0, "Expected a positive number.");
```

<span data-ttu-id="e2c3b-156">*Утверждения,* с другой стороны, используются аналогично фактам, но могут зависеть от состояния целевой машины.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-156">*Assertions*, on the other hand, are used similarly to facts, but may be dependent on the state of the target machine.</span></span> <span data-ttu-id="e2c3b-157">Соответственно, они определяются как операции, в то время как факты определяются как функции (как указано выше).</span><span class="sxs-lookup"><span data-stu-id="e2c3b-157">Correspondingly, they are defined as operations, whereas facts are defined as functions (as above).</span></span>
<span data-ttu-id="e2c3b-158">Чтобы понять различие, рассмотрим следующее использование факта в утверждении:</span><span class="sxs-lookup"><span data-stu-id="e2c3b-158">To understand the distinction, consider the following use of a fact within an assertion:</span></span>

```qsharp
operation AssertQubitsAreAvailable() : Unit
{
     Fact(GetQubitsAvailableToUse() > 0, "No qubits were actually available");
}
```

<span data-ttu-id="e2c3b-159">Здесь мы используем операцию, <xref:microsoft.quantum.environment.getqubitsavailabletouse> чтобы вернуть количество кубитов, доступных для использования.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-159">Here, we are using the operation <xref:microsoft.quantum.environment.getqubitsavailabletouse> to return the number of qubits available to use.</span></span>
<span data-ttu-id="e2c3b-160">Поскольку это явно зависит от глобального состояния программы и `AssertQubitsAreAvailable` ее условия исполнения, наше определение должно быть операцией.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-160">As this clearly depends on the global state of the program and its execution environment, our definition of  `AssertQubitsAreAvailable` must be an operation as well.</span></span>
<span data-ttu-id="e2c3b-161">Тем не менее, мы можем использовать `Bool` это глобальное `Fact` состояние, чтобы дать простое значение в качестве вклада в функцию.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-161">However, we can use that global state to yield a simple `Bool` value as input to the `Fact` function.</span></span>

<span data-ttu-id="e2c3b-162">Опираясь на эти идеи, [прелюдия](xref:microsoft.quantum.libraries.standard.prelude) предлагает <xref:microsoft.quantum.intrinsic.assert> <xref:microsoft.quantum.intrinsic.assertprob> два особенно полезных `()`утверждений, и оба моделируется как операции на .</span><span class="sxs-lookup"><span data-stu-id="e2c3b-162">Building on these ideas, [the prelude](xref:microsoft.quantum.libraries.standard.prelude) offers two especially useful assertions, <xref:microsoft.quantum.intrinsic.assert> and <xref:microsoft.quantum.intrinsic.assertprob> both modeled as operations onto `()`.</span></span> <span data-ttu-id="e2c3b-163">Каждый из этих утверждений принимает оператора Паули, описывающего конкретное измерение интереса, квантовый регистр, на котором должно быть выполнено измерение, и гипотетический результат.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-163">These assertions each take a Pauli operator describing a particular measurement of interest, a quantum register on which a measurement is to be performed, and a hypothetical outcome.</span></span>
<span data-ttu-id="e2c3b-164">На целевых машинах, которые работают по симуляции, мы не связаны [теоремой неклонирования,](https://en.wikipedia.org/wiki/No-cloning_theorem)и можем выполнять такие измерения, не нарушая регистр, передаваемый таким утверждениям.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-164">On target machines which work by simulation, we are not bound by [the no-cloning theorem](https://en.wikipedia.org/wiki/No-cloning_theorem), and can perform such measurements without disturbing the register passed to such assertions.</span></span>
<span data-ttu-id="e2c3b-165">Тренажер может затем, подобно `PositivityFact` функции выше, прервать вычисления, если гипотетический результат не будет наблюдаться на практике:</span><span class="sxs-lookup"><span data-stu-id="e2c3b-165">A simulator can then, similar to the `PositivityFact` function above, abort computation if the hypothetical outcome would not be observed in practice:</span></span>

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

<span data-ttu-id="e2c3b-166">На физическом квантовом оборудовании, где теорема `Assert` без `AssertProb` клонирования `()` препятствует изучению квантового состояния, и операции просто возвращаются без каких-либо других эффектов.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-166">On physical quantum hardware, where the no-cloning theorem prevents examination of quantum state, the `Assert` and `AssertProb` operations simply return `()` with no other effect.</span></span>

<span data-ttu-id="e2c3b-167">Пространство <xref:microsoft.quantum.diagnostics> имен предоставляет еще несколько функций `Assert` семейства, которые позволяют нам проверить более продвинутые условия.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-167">The <xref:microsoft.quantum.diagnostics> namespace provides several more functions of the `Assert` family which allow us to check more advanced conditions.</span></span> 

## <a name="dump-functions"></a><span data-ttu-id="e2c3b-168">Функции свалки</span><span class="sxs-lookup"><span data-stu-id="e2c3b-168">Dump Functions</span></span>

<span data-ttu-id="e2c3b-169">Чтобы помочь устранять <xref:microsoft.quantum.diagnostics> квантовые программы, пространство имен предлагает две функции, которые могут сбросить в файл текущее состояние целевой машины: <xref:microsoft.quantum.diagnostics.dumpmachine> и <xref:microsoft.quantum.diagnostics.dumpregister>.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-169">To help troubleshooting quantum programs, the <xref:microsoft.quantum.diagnostics> namespace offers two functions that can dump into a file the current status of the target machine: <xref:microsoft.quantum.diagnostics.dumpmachine> and <xref:microsoft.quantum.diagnostics.dumpregister>.</span></span> <span data-ttu-id="e2c3b-170">Генерируемый выход каждого зависит от целевой машины.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-170">The generated output of each depends on the target machine.</span></span>

### <a name="dumpmachine"></a><span data-ttu-id="e2c3b-171">DumpMachine</span><span class="sxs-lookup"><span data-stu-id="e2c3b-171">DumpMachine</span></span>

<span data-ttu-id="e2c3b-172">Полное состояние квантового симулятора, распределенного как часть Квантового набора разработки, записывает в файл [волновую функцию](https://en.wikipedia.org/wiki/Wave_function) всей квантовой системы, как одномерный массив сложных чисел, в котором каждый элемент представляет амплитуду вероятности измерения вычислительной основы состояния $'ket'n's$, где $'ket'n b_» b_1b_0 $ за биты\{\}$ b_i $.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-172">The full-state quantum simulator distributed as part of the Quantum Development Kit writes into the file the [wave function](https://en.wikipedia.org/wiki/Wave_function) of the entire quantum system, as a one-dimensional array of complex numbers, in which each element represents the amplitude of the probability of measuring the computational basis state $\ket{n}$, where $\ket{n} = \ket{b_{n-1}...b_1b_0}$ for bits $\{b_i\}$.</span></span> <span data-ttu-id="e2c3b-173">Например, на машине, в котором выделено всего два кубитов, и в квантовом состоянии $${2}(начало){00} «кет»-пси»{2} {1}(кет) — «фрак» <xref:microsoft.quantum.diagnostics.dumpmachine> (1 й) »кет{10}, «конец»выровняйте»$$</span><span class="sxs-lookup"><span data-stu-id="e2c3b-173">For example, on a machine with only two qubits allocated and in the quantum state $$ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10}, \end{align} $$ calling <xref:microsoft.quantum.diagnostics.dumpmachine> generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 0;1
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣2❭:    -0.500000 + -0.500000 i  ==     **********           [ 0.500000 ]   /     [ -2.35619 rad ]
∣3❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

<span data-ttu-id="e2c3b-174">Первый ряд содержит комментарий с идентизациями соответствующих кубитов в их значительном порядке.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-174">The first row provides a comment with the IDs of the corresponding qubits in their significant order.</span></span>
<span data-ttu-id="e2c3b-175">Остальные строки описывают амплитуду вероятности измерения вектора состояния основы в как в картезийском, так и в полярном форматах.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-175">The rest of the rows describe the probability amplitude of measuring the basis state vector $\ket{n}$ in both Cartesian and polar formats.</span></span> <span data-ttu-id="e2c3b-176">Подробно для первого ряда:</span><span class="sxs-lookup"><span data-stu-id="e2c3b-176">In detail for the first row:</span></span>

* <span data-ttu-id="e2c3b-177">**`∣0❭:`** эта строка соответствует `0` состоянию вычислительной основы</span><span class="sxs-lookup"><span data-stu-id="e2c3b-177">**`∣0❭:`** this row corresponds to the `0` computational basis state</span></span>
* <span data-ttu-id="e2c3b-178">**`0.707107 +  0.000000 i`**: амплитуда вероятности в декартовом формате.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-178">**`0.707107 +  0.000000 i`**: the probability amplitude in Cartesian format.</span></span>
* <span data-ttu-id="e2c3b-179">**` == `**: `equal` знак разрежывает оба эквивалентных представления.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-179">**` == `**: the `equal` sign seperates both equivalent representations.</span></span>
* <span data-ttu-id="e2c3b-180">**`**********  `**: Графическое представление величины, количество `*` пропорционально вероятности измерения этого вектора состояния.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-180">**`**********  `**: A graphical representation of the magnitude, the number of `*` is proportionate to the probability of measuring this state vector.</span></span>
* <span data-ttu-id="e2c3b-181">**`[ 0.500000 ]`**: численное значение величины</span><span class="sxs-lookup"><span data-stu-id="e2c3b-181">**`[ 0.500000 ]`**: the numeric value of the magnitude</span></span>
* <span data-ttu-id="e2c3b-182">**`    ---`**: Графическое представление фазы амплитуды (см. ниже).</span><span class="sxs-lookup"><span data-stu-id="e2c3b-182">**`    ---`**: A graphical representation of the amplitude's phase (see below).</span></span>
* <span data-ttu-id="e2c3b-183">**`[ 0.0000 rad ]`**: численное значение фазы (в радиане).</span><span class="sxs-lookup"><span data-stu-id="e2c3b-183">**`[ 0.0000 rad ]`**: the numeric value of the phase (in radians).</span></span>

<span data-ttu-id="e2c3b-184">И величина, и фаза отображаются с графическим представлением.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-184">Both the magnitude and the phase are displayed with a graphical representation.</span></span> <span data-ttu-id="e2c3b-185">Представление величины прямо вперед: он показывает `*`бар , тем больше вероятность больше бар будет.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-185">The magnitude representation is straight-forward: it shows a bar of `*`, the bigger the probability the bigger the bar will be.</span></span> <span data-ttu-id="e2c3b-186">На этапе мы показываем следующие символы для представления угла на основе диапазонов:</span><span class="sxs-lookup"><span data-stu-id="e2c3b-186">For the phase, we show the following symbols to represent the angle based on ranges:</span></span>

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

<span data-ttu-id="e2c3b-187">Ниже приведены `DumpMachine` следующие примеры для некоторых общих состояний:</span><span class="sxs-lookup"><span data-stu-id="e2c3b-187">The following examples show `DumpMachine` for some common states:</span></span>

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
  > <span data-ttu-id="e2c3b-188">Идентификатор кубита назначается во время выполнения, и он не обязательно выравнивается с порядком, в котором был выделен кубит, или его положением в регистре кубита.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-188">The id of a qubit is assigned at runtime and it's not necessarily aligned with the order in which the qubit was allocated or its position within a qubit register.</span></span>


#### <a name="visual-studio-2019"></a>[<span data-ttu-id="e2c3b-189">Визуальная студия 2019</span><span class="sxs-lookup"><span data-stu-id="e2c3b-189">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

  > [!TIP]
  > <span data-ttu-id="e2c3b-190">Вы можете выяснить идентификатор qubit в Visual Studio, поставив точку разрыва в коде и проинспектируя значение переменной кубита, например:</span><span class="sxs-lookup"><span data-stu-id="e2c3b-190">You can figure out a qubit id in Visual Studio by putting a breakpoint in your code and inspecting the value of a qubit variable, for example:</span></span>
  > 
  > ![показать кубит ID в визуальной студии](~/media/qubit_id.png)
  >
  > <span data-ttu-id="e2c3b-192">кубит с `0` индексом `register2` на`3`имеет id ' `1` ,`2`кубит с индексом имеет идентификатор .</span><span class="sxs-lookup"><span data-stu-id="e2c3b-192">the qubit with index `0` on `register2` has id=`3`, the qubit with index `1` has id=`2`.</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="e2c3b-193">Командная строка и Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="e2c3b-193">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

  > [!TIP]
  > <span data-ttu-id="e2c3b-194">Вы можете выяснить идентификатор qubit, используя <xref:microsoft.quantum.intrinsic.message> функцию и передавая переменную кубита в сообщении, например:</span><span class="sxs-lookup"><span data-stu-id="e2c3b-194">You can figure out a qubit id by using the <xref:microsoft.quantum.intrinsic.message> function and passing the qubit variable in the message, for example:</span></span>
  >
  > ```qsharp
  > Message($"0={register2[0]}; 1={register2[1]}");
  > ```
  > 
  > <span data-ttu-id="e2c3b-195">которые могут генерировать этот выход:</span><span class="sxs-lookup"><span data-stu-id="e2c3b-195">which could generate this output:</span></span>
  >```
  > 0=q:3; 1=q:2
  >```
  > <span data-ttu-id="e2c3b-196">это означает, что кубит `register2` с`3`индексом `0` на имеет `1` id`2`' , кубит с индексом имеет идентификатор .</span><span class="sxs-lookup"><span data-stu-id="e2c3b-196">which means that the qubit with index `0` on `register2` has id=`3`, the qubit with index `1` has id=`2`.</span></span>


***

<span data-ttu-id="e2c3b-197"><xref:microsoft.quantum.diagnostics.dumpmachine>является частью <xref:microsoft.quantum.diagnostics> пространства имен, поэтому для того, `open` чтобы использовать его, необходимо добавить заявление:</span><span class="sxs-lookup"><span data-stu-id="e2c3b-197"><xref:microsoft.quantum.diagnostics.dumpmachine> is part of the  <xref:microsoft.quantum.diagnostics> namespace, so in order to use it you must add an `open` statement:</span></span>

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


### <a name="dumpregister"></a><span data-ttu-id="e2c3b-198">DumpRegister</span><span class="sxs-lookup"><span data-stu-id="e2c3b-198">DumpRegister</span></span>

<span data-ttu-id="e2c3b-199"><xref:microsoft.quantum.diagnostics.dumpregister>работает, <xref:microsoft.quantum.diagnostics.dumpmachine>как , за исключением он также занимает массив кубитов ограничить объем информации только, что отношение к соответствующим кубитов.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-199"><xref:microsoft.quantum.diagnostics.dumpregister> works like <xref:microsoft.quantum.diagnostics.dumpmachine>, except it also takes an array of qubits to limit the amount of information to only that relevant to the corresponding qubits.</span></span>

<span data-ttu-id="e2c3b-200">Как <xref:microsoft.quantum.diagnostics.dumpmachine>и в том, что информация, генерируемая, <xref:microsoft.quantum.diagnostics.dumpregister> зависит от целевой машины.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-200">As with <xref:microsoft.quantum.diagnostics.dumpmachine>, the information generated by <xref:microsoft.quantum.diagnostics.dumpregister> depends on the target machine.</span></span> <span data-ttu-id="e2c3b-201">Для полного состояния квантового симулятора он записывает в файл волновой функции до глобальной фазы <xref:microsoft.quantum.diagnostics.dumpmachine>квантовой подсистемы, генерируемой предоставленными кубитов в том же формате, что и .</span><span class="sxs-lookup"><span data-stu-id="e2c3b-201">For the full-state quantum simulator it writes into the file the wave function up to a global phase of the quantum sub-system generated by the provided qubits in the same format as <xref:microsoft.quantum.diagnostics.dumpmachine>.</span></span>  <span data-ttu-id="e2c3b-202">Например, взять еще раз машину с выделением только двух кубитов, а в квантовом{1}состоянии $$ (начало{00} выровнять) (кет-пси){10} {1}{2}{0} {2} {1} {2}{0} {2}{2} ) ( («frac»sqrt , «кет» ( «frac» (1) »кет» (кет) «время» (frac) --(1) » » » кврт кет ) , <xref:microsoft.quantum.diagnostics.dumpregister> `qubit[0]` «конец»-выровнял»$, требуя для генерации этого вывода:</span><span class="sxs-lookup"><span data-stu-id="e2c3b-202">For example, take again a machine with only two qubits allocated and in the quantum state $$ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10} = - e^{-i\pi/4} ( (\frac{1}{\sqrt{2}} \ket{0} - \frac{(1 + i)}{2} \ket{1} ) \otimes \frac{-(1 + i)}{\sqrt{2}} \ket{0} ) , \end{align} $$ calling <xref:microsoft.quantum.diagnostics.dumpregister> for `qubit[0]` generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:    -0.707107 + -0.707107 i  ==     ******************** [ 1.000000 ]  /      [ -2.35619 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

<span data-ttu-id="e2c3b-203">и <xref:microsoft.quantum.diagnostics.dumpregister> призыв `qubit[1]` к генерирует этот выход:</span><span class="sxs-lookup"><span data-stu-id="e2c3b-203">and calling <xref:microsoft.quantum.diagnostics.dumpregister> for `qubit[1]` generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 1
∣0❭:     0.707107 +  0.000000 i  ==     ***********          [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:    -0.500000 + -0.500000 i  ==     ***********          [ 0.500000 ]  /      [ -2.35619 rad ]
```

<span data-ttu-id="e2c3b-204">В целом состояние регистра, запутавого с другим регистром, является не чистым, а смешанным состоянием.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-204">In general, the state of a register that is entangled with another register is a mixed state rather than a pure state.</span></span> <span data-ttu-id="e2c3b-205">В этом <xref:microsoft.quantum.diagnostics.dumpregister> случае выводит следующее сообщение:</span><span class="sxs-lookup"><span data-stu-id="e2c3b-205">In this case, <xref:microsoft.quantum.diagnostics.dumpregister> outputs the following message:</span></span>

```
Qubits provided (0;) are entangled with some other qubit.
```

<span data-ttu-id="e2c3b-206">Следующий пример показывает, как <xref:microsoft.quantum.diagnostics.dumpregister> можно <xref:microsoft.quantum.diagnostics.dumpmachine> использовать как, так и в коде:</span><span class="sxs-lookup"><span data-stu-id="e2c3b-206">The following example shows you how you can use both <xref:microsoft.quantum.diagnostics.dumpregister> and <xref:microsoft.quantum.diagnostics.dumpmachine> in your Q# code:</span></span>

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

## <a name="debugging"></a><span data-ttu-id="e2c3b-207">Отладка</span><span class="sxs-lookup"><span data-stu-id="e2c3b-207">Debugging</span></span>

<span data-ttu-id="e2c3b-208">Помимо `Assert` `Dump` функций и операций, компания поддерживает подмножество стандартных возможностей отладки Visual Studio: [настройка точек разрыва строки,](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints) [прохождение кода с помощью F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger) и [проверка значений классических переменных](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) — все это возможно во время выполнения кода на симуляторе.</span><span class="sxs-lookup"><span data-stu-id="e2c3b-208">On top of `Assert` and `Dump` functions and operations, Q# supports a subset of standard Visual Studio debugging capabilities: [setting line breakpoints](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), [stepping through code using F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger) and [inspecting values of classic variables](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) are all possible during code execution on the simulator.</span></span>

<span data-ttu-id="e2c3b-209">Отладка в Visual Studio Code использует возможности отладки, предоставляемые СЗ для расширения Visual Studio Code, работающего на OmniSharp, и требует установки [последней версии.](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp)</span><span class="sxs-lookup"><span data-stu-id="e2c3b-209">Debugging in Visual Studio Code leverages the debugging capabilities provided by the C# for Visual Studio Code extension powered by OmniSharp and requires installing the [latest version](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp).</span></span> 
