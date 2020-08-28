---
title: Способы запуска Q# программы
description: Общие сведения о различных способах запуска Q# программ. Из командной строки, Q# записные книжки Jupyter и классические хост-программы на языке Python или .NET.
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 05/15/2020
ms.topic: article
uid: microsoft.quantum.guide.host-programs
no-loc:
- Q#
- $$v
ms.openlocfilehash: f1eca44dabd72cd107d72d3b9e3ad1081c19c27d
ms.sourcegitcommit: 11bd357baeb6ab53a402882979e75964d0869b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2020
ms.locfileid: "88992196"
---
# <a name="ways-to-run-a-no-locq-program"></a><span data-ttu-id="5de3e-104">Способы запуска Q# программы</span><span class="sxs-lookup"><span data-stu-id="5de3e-104">Ways to run a Q# program</span></span>

<span data-ttu-id="5de3e-105">Один из самых сильных достоинств набора разработки такта — это гибкость в различных платформах и средах разработки.</span><span class="sxs-lookup"><span data-stu-id="5de3e-105">One of the Quantum Development Kit's greatest strengths is its flexibility across platforms and development environments.</span></span>
<span data-ttu-id="5de3e-106">Однако это также означает, что новые Q# Пользователи, возможно, будут путать или перегружены множеством параметров, приведенных в [install guide](xref:microsoft.quantum.install)этом разделе.</span><span class="sxs-lookup"><span data-stu-id="5de3e-106">However, this also means that new Q# users may find themselves confused or overwhelmed by the numerous options found in the [install guide](xref:microsoft.quantum.install).</span></span>
<span data-ttu-id="5de3e-107">На этой странице объясняется, что происходит при Q# запуске программы, и сравниваются различные способы, которые могут сделать пользователи.</span><span class="sxs-lookup"><span data-stu-id="5de3e-107">On this page, we explain what happens when a Q# program is run, and compare the different ways in which users can do so.</span></span>

<span data-ttu-id="5de3e-108">Основное отличие состоит в том, что Q# можно запустить:</span><span class="sxs-lookup"><span data-stu-id="5de3e-108">A primary distinction is that Q# can be run:</span></span>
- <span data-ttu-id="5de3e-109">в качестве автономного приложения, где Q# — единственный применяемый язык, и программа вызывается напрямую.</span><span class="sxs-lookup"><span data-stu-id="5de3e-109">as a standalone application, where Q# is the only language involved and the program is invoked directly.</span></span> <span data-ttu-id="5de3e-110">В этой категории есть два метода:</span><span class="sxs-lookup"><span data-stu-id="5de3e-110">Two methods actually fall in this category:</span></span>
  - <span data-ttu-id="5de3e-111">интерфейс командной строки</span><span class="sxs-lookup"><span data-stu-id="5de3e-111">the command-line interface</span></span>
  - <span data-ttu-id="5de3e-112">Q# Записные книжки Jupyter</span><span class="sxs-lookup"><span data-stu-id="5de3e-112">Q# Jupyter Notebooks</span></span>
- <span data-ttu-id="5de3e-113">с помощью дополнительной *основной программы*, написанной на Python или на языке .NET (например, C# или F #), который затем вызывает программу и может обрабатывать возвращенные результаты.</span><span class="sxs-lookup"><span data-stu-id="5de3e-113">with an additional *host program*, written in Python or a .NET language (e.g. C# or F#), which then invokes the program and can further process returned results.</span></span>

<span data-ttu-id="5de3e-114">Чтобы лучше понять эти процессы и их различия, рассмотрим простую Q# программу и Сравните способы их выполнения.</span><span class="sxs-lookup"><span data-stu-id="5de3e-114">To best understand these processes and their differences, we consider a simple Q# program and compare the ways it can be executed.</span></span>

## <a name="basic-no-locq-program"></a><span data-ttu-id="5de3e-115">Базовая Q# программа</span><span class="sxs-lookup"><span data-stu-id="5de3e-115">Basic Q# program</span></span>

<span data-ttu-id="5de3e-116">Базовая программа-тактовая частота может состоять из подготовки Кубит в равной части Штатов $ \кет {0} $ and $ \кет {1} $, ее измерения и возврата результата, который будет случайным или одним из этих двух состояний с одинаковой вероятностью.</span><span class="sxs-lookup"><span data-stu-id="5de3e-116">A basic quantum program might consist of preparing a qubit in an equal superposition of states $\ket{0}$ and $\ket{1}$, measuring it, and returning the result, which will be randomly either one of these two states with equal probability.</span></span>
<span data-ttu-id="5de3e-117">В самом деле, этот процесс является ядром краткого руководства [генератора случайных чисел](xref:microsoft.quantum.quickstarts.qrng) .</span><span class="sxs-lookup"><span data-stu-id="5de3e-117">Indeed, this process is at the core of the [quantum random number generator](xref:microsoft.quantum.quickstarts.qrng) quickstart.</span></span>

<span data-ttu-id="5de3e-118">В Q# это будет выполнено с помощью следующего кода:</span><span class="sxs-lookup"><span data-stu-id="5de3e-118">In Q#, this would be performed by the following code:</span></span>

```qsharp
        using (q = Qubit()) {    // allocates qubit for use (automatically in |0>)
            H(q);                // puts qubit in superposition of |0> and |1>
            return MResetZ(q);   // measures qubit, returns result (and resets it to |0> before deallocation)
        }
```

<span data-ttu-id="5de3e-119">Однако этот код не может быть выполнен с помощью Q# .</span><span class="sxs-lookup"><span data-stu-id="5de3e-119">However, this code alone can't be executed by Q#.</span></span>
<span data-ttu-id="5de3e-120">Для этого ему нужно сделать тело [операции](xref:microsoft.quantum.guide.basics#q-operations-and-functions), которое затем выполняется при вызове---либо напрямую, либо другой операцией.</span><span class="sxs-lookup"><span data-stu-id="5de3e-120">For that, it needs to make up the body of an [operation](xref:microsoft.quantum.guide.basics#q-operations-and-functions), which is then executed when called---either directly or by another operation.</span></span> <span data-ttu-id="5de3e-121">Таким образом, можно написать операцию следующего вида:</span><span class="sxs-lookup"><span data-stu-id="5de3e-121">Hence, you can write an operation of the following form:</span></span>
```qsharp
    operation MeasureSuperposition() : Result {
        using (q = Qubit()) {
            H(q);
            return MResetZ(q);
        }
    }
```
<span data-ttu-id="5de3e-122">Вы определили операцию, `MeasureSuperposition` которая не принимает входные данные и возвращает значение типа [result](xref:microsoft.quantum.guide.types).</span><span class="sxs-lookup"><span data-stu-id="5de3e-122">You have defined an operation, `MeasureSuperposition`, which takes no inputs and returns a value of type [Result](xref:microsoft.quantum.guide.types).</span></span>

<span data-ttu-id="5de3e-123">Хотя примеры на этой странице состоят только из Q# *операций*, все концепции, которые мы будем обсуждать, будут одинаковыми по отношению к Q# *функциям*, и, следовательно, они вместе называются *вызываемыми*.</span><span class="sxs-lookup"><span data-stu-id="5de3e-123">While the examples on this page only consist of Q# *operations*, all of the concepts we will discuss pertain equally to Q# *functions*, and therefore we refer to them collectively as *callables*.</span></span> <span data-ttu-id="5de3e-124">Их различия обсуждаются в разделе Основные сведения об [ Q# операциях и функциях](xref:microsoft.quantum.guide.basics#q-operations-and-functions). Дополнительные сведения о их определении можно найти в разделе [операции и функции](xref:microsoft.quantum.guide.operationsfunctions).</span><span class="sxs-lookup"><span data-stu-id="5de3e-124">Their differences are discussed at [Q# basics: operations and functions](xref:microsoft.quantum.guide.basics#q-operations-and-functions), and more details on defining them can be found at [Operations and functions](xref:microsoft.quantum.guide.operationsfunctions).</span></span>

### <a name="callable-defined-in-a-no-locq-file"></a><span data-ttu-id="5de3e-125">Вызываемый в Q# файле</span><span class="sxs-lookup"><span data-stu-id="5de3e-125">Callable defined in a Q# file</span></span>

<span data-ttu-id="5de3e-126">Вызываемый метод — это именно то, что вызывается и выполняется с помощью Q# .</span><span class="sxs-lookup"><span data-stu-id="5de3e-126">The callable is precisely what's called and run by Q#.</span></span>
<span data-ttu-id="5de3e-127">Однако требуется еще несколько дополнений для составления полного `*.qs` Q# файла.</span><span class="sxs-lookup"><span data-stu-id="5de3e-127">However, it requires a few more additions to comprise a full `*.qs` Q# file.</span></span>

<span data-ttu-id="5de3e-128">Все Q# типы и вызываемые объекты (как определяемые пользователем, так и встроенные в язык) определяются в *пространствах имен*, которые предоставляют полные имена, на которые затем можно ссылаться.</span><span class="sxs-lookup"><span data-stu-id="5de3e-128">All Q# types and callables (both those you define and those intrinsic to the language) are defined within *namespaces*, which provide each a full name that can then be referenced.</span></span>

<span data-ttu-id="5de3e-129">Например, [`H`](xref:microsoft.quantum.intrinsic.h) операции и находятся [`MResetZ`](xref:microsoft.quantum.measurement.mresetz) в [`Microsoft.Quantum.Instrinsic`](xref:microsoft.quantum.intrinsic) [`Microsoft.Quantum.Measurement`](xref:microsoft.quantum.measurement) пространствах имен и (в составе [ Q# стандартных библиотек](xref:microsoft.quantum.qsharplibintro)).</span><span class="sxs-lookup"><span data-stu-id="5de3e-129">For example, the [`H`](xref:microsoft.quantum.intrinsic.h) and [`MResetZ`](xref:microsoft.quantum.measurement.mresetz) operations are found in the [`Microsoft.Quantum.Instrinsic`](xref:microsoft.quantum.intrinsic) and [`Microsoft.Quantum.Measurement`](xref:microsoft.quantum.measurement) namespaces (part of the [Q# Standard Libraries](xref:microsoft.quantum.qsharplibintro)).</span></span>
<span data-ttu-id="5de3e-130">Таким образом, они всегда могут вызываться с помощью *полных* имен `Microsoft.Quantum.Intrinsic.H(<qubit>)` , `Microsoft.Quantum.Measurement.MResetZ(<qubit>)` но всегда это приведет к очень небыстрому выполнению кода.</span><span class="sxs-lookup"><span data-stu-id="5de3e-130">As such, they can always be called via their *full* names, `Microsoft.Quantum.Intrinsic.H(<qubit>)` and `Microsoft.Quantum.Measurement.MResetZ(<qubit>)`, but always doing this would lead to very cluttered code.</span></span>

<span data-ttu-id="5de3e-131">Вместо этого `open` инструкции позволяют ссылаться на вызываемые команды с более кратким сокращенным именем, как мы сделали в теле операции выше.</span><span class="sxs-lookup"><span data-stu-id="5de3e-131">Instead, `open` statements allow callables to be referenced with more concise shorthand, as we've done in the operation body above.</span></span>
<span data-ttu-id="5de3e-132">Поэтому полный Q# файл, содержащий нашу операцию, состоит из определения нашего пространства имен, открытия пространств имен для этих вызываемых операций, а затем нашей операции:</span><span class="sxs-lookup"><span data-stu-id="5de3e-132">The full Q# file containing our operation would therefore consist of defining our own namespace, opening the namespaces for those callables our operation uses, and then our operation:</span></span>

```qsharp
namespace NamespaceName {
    open Microsoft.Quantum.Intrinsic;     // for the H operation
    open Microsoft.Quantum.Measurement;   // for MResetZ

    operation MeasureSuperposition() : Result {
        using (q = Qubit()) { 
            H(q);
            return MResetZ(q);
        }
    }
}
```

> [!NOTE]
> <span data-ttu-id="5de3e-133">Пространства имен могут также быть *псевдонимами* при открытии, что может оказаться полезным, если имена вызываемых и типов в двух пространствах имен конфликтуют.</span><span class="sxs-lookup"><span data-stu-id="5de3e-133">Namespaces can also be *aliased* when opened, which can be helpful if callable/type names in two namespaces conflict.</span></span>
> <span data-ttu-id="5de3e-134">Например, можно использовать `open Microsoft.Quantum.Instrinsic as NamespaceWithH;` метод выше, а затем вызвать `H` через `NamespaceWithH.H(<qubit>)` .</span><span class="sxs-lookup"><span data-stu-id="5de3e-134">For example, we could instead use `open Microsoft.Quantum.Instrinsic as NamespaceWithH;` above, and then call `H` via `NamespaceWithH.H(<qubit>)`.</span></span>

> [!NOTE]
> <span data-ttu-id="5de3e-135">Единственным исключением является [`Microsoft.Quantum.Core`](xref:microsoft.quantum.core) пространство имен, которое всегда открывается автоматически.</span><span class="sxs-lookup"><span data-stu-id="5de3e-135">One exception to all of this is the [`Microsoft.Quantum.Core`](xref:microsoft.quantum.core) namespace, which is always automatically opened.</span></span>
> <span data-ttu-id="5de3e-136">Таким образом, вызываемые, например, [`Length`](xref:microsoft.quantum.core.length) всегда можно использовать напрямую.</span><span class="sxs-lookup"><span data-stu-id="5de3e-136">Therefore, callables like [`Length`](xref:microsoft.quantum.core.length) can always be used directly.</span></span>

### <a name="execution-on-target-machines"></a><span data-ttu-id="5de3e-137">Выполнение на целевых компьютерах</span><span class="sxs-lookup"><span data-stu-id="5de3e-137">Execution on target machines</span></span>

<span data-ttu-id="5de3e-138">Теперь общая модель выполнения Q# программы становится ясной.</span><span class="sxs-lookup"><span data-stu-id="5de3e-138">Now the general execution model of a Q# program becomes clear.</span></span>

<br/>
<img src="../media/hostprograms_general_execution_model.png" alt="Q# program execution diagram" width="400">

<span data-ttu-id="5de3e-139">Во – первых, конкретный вызываемый тип имеет доступ к любым другим вызываемым и типам, определенным в том же пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="5de3e-139">Firstly, the specific callable to be executed has access to any other callables and types defined in the same namespace.</span></span>
<span data-ttu-id="5de3e-140">Он также обращается к ним из любой [ Q# библиотеки](xref:microsoft.quantum.libraries), но на них должна ссылаться либо по полному имени, либо с помощью инструкций, `open` описанных выше.</span><span class="sxs-lookup"><span data-stu-id="5de3e-140">It also access those from any of the [Q# libraries](xref:microsoft.quantum.libraries), but those must be referenced either via their full name, or through the use of `open` statements described above.</span></span>

<span data-ttu-id="5de3e-141">Затем сам вызываемый объект выполняется на *[целевом компьютере](xref:microsoft.quantum.machines)*.</span><span class="sxs-lookup"><span data-stu-id="5de3e-141">The callable itself is then executed on a *[target machine](xref:microsoft.quantum.machines)*.</span></span>
<span data-ttu-id="5de3e-142">Такие целевые компьютеры могут быть реальным оборудованием такта или несколькими симуляторами, доступными в составе КДК.</span><span class="sxs-lookup"><span data-stu-id="5de3e-142">Such target machines can be actual quantum hardware or the multiple simulators available as part of the QDK.</span></span>
<span data-ttu-id="5de3e-143">Для наших целей наиболее полезным целевым компьютером является экземпляр [симулятора полного состояния](xref:microsoft.quantum.machines.full-state-simulator), `QuantumSimulator` который вычисляет поведение программы так, как если бы оно выполнялось на компьютере такта без помех.</span><span class="sxs-lookup"><span data-stu-id="5de3e-143">For our purposes here, the most useful target machine is an instance of the [full-state simulator](xref:microsoft.quantum.machines.full-state-simulator), `QuantumSimulator`, which calculates the program's behavior as if it were being executed on a noise-free quantum computer.</span></span>

<span data-ttu-id="5de3e-144">До сих пор мы описывали, что происходит при Q# выполнении определенного вызываемого типа.</span><span class="sxs-lookup"><span data-stu-id="5de3e-144">So far, we've described what happens when a specific Q# callable is being executed.</span></span>
<span data-ttu-id="5de3e-145">Независимо от того Q# , используется ли в автономном приложении или основной программе, этот общий процесс является более или менее---поэтому гибкость КДК.</span><span class="sxs-lookup"><span data-stu-id="5de3e-145">Regardless of whether Q# is used in a standalone application or with a host program, this general process is more or less the same---hence the QDK's flexibility.</span></span>
<span data-ttu-id="5de3e-146">Различия между различными способами вызова пакета разработки тактов, таким образом, показывают, *как* Q# вызываемый метод вызывается и в каком порядке возвращаются любые результаты.</span><span class="sxs-lookup"><span data-stu-id="5de3e-146">The differences between the different ways of calling into the Quantum Development Kit therefore reveal themselves in *how* that Q# callable is called to be executed, and in what manner any results are returned.</span></span>
<span data-ttu-id="5de3e-147">В частности, различия связаны с</span><span class="sxs-lookup"><span data-stu-id="5de3e-147">More specifically, the differences revolve around</span></span> 
1. <span data-ttu-id="5de3e-148">, указывающий, какие Q# вызываемые должны выполняться,</span><span class="sxs-lookup"><span data-stu-id="5de3e-148">indicating which Q# callable is to be executed,</span></span>
2. <span data-ttu-id="5de3e-149">как предоставляются потенциальные вызываемые аргументы,</span><span class="sxs-lookup"><span data-stu-id="5de3e-149">how potential callable arguments are provided,</span></span>
3. <span data-ttu-id="5de3e-150">Указание целевого компьютера, на котором выполняется, и</span><span class="sxs-lookup"><span data-stu-id="5de3e-150">specifying the target machine on which to execute it, and</span></span>
4. <span data-ttu-id="5de3e-151">возвращаемые результаты.</span><span class="sxs-lookup"><span data-stu-id="5de3e-151">how any results are returned.</span></span>

<span data-ttu-id="5de3e-152">Сначала мы обсудим, как это делается с помощью Q# автономного приложения из командной строки, а затем приступите к использованию хост-программ Python и C#.</span><span class="sxs-lookup"><span data-stu-id="5de3e-152">First, we discuss how this is done with the Q# standalone application from the command prompt, and then proceed to using Python and C# host programs.</span></span>
<span data-ttu-id="5de3e-153">Мы зарезервировани автономное приложение Q# записных книжек Jupyter для последнего, так как в отличие от первых трех, основная функциональность не располагается вокруг локального Q# файла.</span><span class="sxs-lookup"><span data-stu-id="5de3e-153">We reserve the standalone application of Q# Jupyter Notebooks for last, because unlike the first three, it's primary functionality does not center around a local Q# file.</span></span>

> [!NOTE]
> <span data-ttu-id="5de3e-154">Хотя мы не продемонстрируем его в этих примерах, одно унифицированное различие между методами выполнения заключается в том, что все сообщения, выводимые из Q# программы ( [`Message`](xref:microsoft.quantum.intrinsic.message) например, или [`DumpMachine`](xref:microsoft.quantum.diagnostics.dumpmachine) ), обычно всегда будут выводиться в соответствующую консоль.</span><span class="sxs-lookup"><span data-stu-id="5de3e-154">Although we don't illustrate it in these examples, one commonality between the execution methods is that any messages printed from inside the Q# program (by way of [`Message`](xref:microsoft.quantum.intrinsic.message) or [`DumpMachine`](xref:microsoft.quantum.diagnostics.dumpmachine), for example) will typically always be printed to the respective console.</span></span>

## <a name="no-locq-from-the-command-prompt"></a><span data-ttu-id="5de3e-155">Q# из командной строки</span><span class="sxs-lookup"><span data-stu-id="5de3e-155">Q# from the command prompt</span></span>
<span data-ttu-id="5de3e-156">Одним из самых простых способов приступить к написанию Q# программ является избежание беспокойства отдельным файлам и второго языка.</span><span class="sxs-lookup"><span data-stu-id="5de3e-156">One of the easiest ways to get started writing Q# programs is to avoid worrying about separate files and a second language altogether.</span></span>
<span data-ttu-id="5de3e-157">Использование Visual Studio Code или Visual Studio с расширением КДК обеспечивает простой рабочий процесс, в котором мы выполняем Q# вызываемые из одного Q# файла.</span><span class="sxs-lookup"><span data-stu-id="5de3e-157">Using Visual Studio Code or Visual Studio with the QDK extension allows for a seamless work flow in which we run Q# callables from only a single Q# file.</span></span>

<span data-ttu-id="5de3e-158">Для этого в конечном итоге будет вызвано выполнение программы путем ввода</span><span class="sxs-lookup"><span data-stu-id="5de3e-158">For this, we will ultimately invoke the program's execution by entering</span></span>
```dotnetcli
dotnet run
```
<span data-ttu-id="5de3e-159">в командной строке.</span><span class="sxs-lookup"><span data-stu-id="5de3e-159">at the command prompt.</span></span>
<span data-ttu-id="5de3e-160">Самый простой рабочий процесс заключается в том, что расположение каталога терминала совпадает с именем Q# файла, что может быть легко обработано вместе Q# с редактированием файлов с помощью интегрированного терминала в VS Code, например.</span><span class="sxs-lookup"><span data-stu-id="5de3e-160">The simplest workflow is when the terminal's directory location is the same as the Q# file, which can be easily handled alongside Q# file editing by using the integrated terminal in VS Code, for example.</span></span>
<span data-ttu-id="5de3e-161">Однако [ `dotnet run` команда](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) принимает множество параметров, и программа также может быть запущена из другого расположения, просто предоставляя `--project <PATH>` расположение Q# файла.</span><span class="sxs-lookup"><span data-stu-id="5de3e-161">However, the [`dotnet run` command](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) accepts numerous options, and the program can also be run from a different location by simply providing `--project <PATH>` with the location of the Q# file.</span></span>


### <a name="add-entry-point-to-no-locq-file"></a><span data-ttu-id="5de3e-162">Добавить точку входа в Q# файл</span><span class="sxs-lookup"><span data-stu-id="5de3e-162">Add entry point to Q# file</span></span>

<span data-ttu-id="5de3e-163">Большинство Q# файлов будет содержать несколько вызываемых, поэтому, естественно, нам нужно сообщить компилятору, *какую* вызываемую команду выполнить при предоставлении `dotnet run` команды.</span><span class="sxs-lookup"><span data-stu-id="5de3e-163">Most Q# files will contain more than one callable, so naturally we need to let the compiler know *which* callable to execute when we provide the `dotnet run` command.</span></span>
<span data-ttu-id="5de3e-164">Это делается простым изменением Q# самого файла:</span><span class="sxs-lookup"><span data-stu-id="5de3e-164">This is done with a simple change to the Q# file itself:</span></span> 
    - <span data-ttu-id="5de3e-165">Добавьте строку `@EntryPoint()` непосредственно перед вызываемым.</span><span class="sxs-lookup"><span data-stu-id="5de3e-165">add a line with `@EntryPoint()` directly preceding the callable.</span></span>

<span data-ttu-id="5de3e-166">Следовательно, наш файл, приведенный выше, стал</span><span class="sxs-lookup"><span data-stu-id="5de3e-166">Our file from above would therefore become</span></span>
```qsharp
namespace NamespaceName {
    open Microsoft.Quantum.Intrinsic;     // for the H operation
    open Microsoft.Quantum.Measurement;   // for MResetZ

    @EntryPoint()
    operation MeasureSuperposition() : Result {
        using (q = Qubit()) { 
            H(q);
            return MResetZ(q);
        }
    }
}
```

<span data-ttu-id="5de3e-167">Теперь вызов `dotnet run` из командной строки ведет к `MeasureSuperposition` выполнению, а возвращаемое значение затем распечатывается непосредственно в терминале.</span><span class="sxs-lookup"><span data-stu-id="5de3e-167">Now, a call of `dotnet run` from the command prompt leads to `MeasureSuperposition` being run, and the returned value is then printed directly to the terminal.</span></span>
<span data-ttu-id="5de3e-168">Таким образом, вы увидите `One` или `Zero` печатаете.</span><span class="sxs-lookup"><span data-stu-id="5de3e-168">So, you will see either `One` or `Zero` printed.</span></span> 

<span data-ttu-id="5de3e-169">Обратите внимание, что при наличии нескольких вызываемых, определенных ниже, `MeasureSuperposition` будет выполняться только запуск.</span><span class="sxs-lookup"><span data-stu-id="5de3e-169">Note that it doesn't matter if you have more callables defined below it, only `MeasureSuperposition` will be run.</span></span>
<span data-ttu-id="5de3e-170">Кроме того, нет проблем, если вызываемый объект включает [Комментарии к документации](xref:microsoft.quantum.guide.filestructure#documentation-comments) до объявления, `@EntryPoint()` атрибут можно просто поместить над ними.</span><span class="sxs-lookup"><span data-stu-id="5de3e-170">Additionally, it's no problem if your callable includes [documentation comments](xref:microsoft.quantum.guide.filestructure#documentation-comments) before its declaration, the `@EntryPoint()` attribute can be simply placed above them.</span></span>

### <a name="callable-arguments"></a><span data-ttu-id="5de3e-171">Вызываемые аргументы</span><span class="sxs-lookup"><span data-stu-id="5de3e-171">Callable arguments</span></span>

<span data-ttu-id="5de3e-172">До сих пор мы рассматривали только операцию, которая не принимает входные данные.</span><span class="sxs-lookup"><span data-stu-id="5de3e-172">So far, we've only considered an operation that takes no inputs.</span></span>
<span data-ttu-id="5de3e-173">Предположим, что мы хотели выполнить аналогичную операцию, но на нескольких Кубитс---число, предоставленное в качестве аргумента.</span><span class="sxs-lookup"><span data-stu-id="5de3e-173">Suppose we wanted to perform a similar operation, but on multiple qubits---the number of which is provided as an argument.</span></span>
<span data-ttu-id="5de3e-174">Такую операцию можно написать так:</span><span class="sxs-lookup"><span data-stu-id="5de3e-174">Such an operation could be written as</span></span>
```qsharp
    operation MeasureSuperpositionArray(n : Int) : Result[] {
        using (qubits = Qubit[n]) {              // allocate a register of n qubits
            ApplyToEach(H, qubits);              // apply H to each qubit in the register
            return ForEach(MResetZ, qubits);     // perform MResetZ on each qubit, returns the resulting array
        }
    }
```
<span data-ttu-id="5de3e-175">, где возвращаемое значение является массивом результатов измерения.</span><span class="sxs-lookup"><span data-stu-id="5de3e-175">where the returned value is an array of the measurement results.</span></span>
<span data-ttu-id="5de3e-176">Обратите внимание, что [`ApplyToEach`](xref:microsoft.quantum.canon.applytoeach) и [`ForEach`](xref:microsoft.quantum.arrays.foreach) находятся в [`Microsoft.Quantum.Canon`](xref:microsoft.quantum.canon) [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) пространствах имен и, для каждого из которых требуются дополнительные `open` инструкции.</span><span class="sxs-lookup"><span data-stu-id="5de3e-176">Note that [`ApplyToEach`](xref:microsoft.quantum.canon.applytoeach) and [`ForEach`](xref:microsoft.quantum.arrays.foreach) are in the [`Microsoft.Quantum.Canon`](xref:microsoft.quantum.canon) and [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) namespaces, requiring additional `open` statements for each.</span></span>

<span data-ttu-id="5de3e-177">Если переместить `@EntryPoint()` атрибут перед этой новой операцией (Обратите внимание, что в файле может быть только одна строка), попытка запустить ее с помощью просто приведет к `dotnet run` появлении сообщения об ошибке, которое указывает, какие дополнительные параметры командной строки требуются и как их выразить.</span><span class="sxs-lookup"><span data-stu-id="5de3e-177">If we move the `@EntryPoint()` attribute to precede this new operation (note there can only be one such line in a file), attempting to run it with simply `dotnet run` results in an error message which indicates what additional command-line options are required, and how to express them.</span></span>

<span data-ttu-id="5de3e-178">В действительности в командной строке используется общий формат `dotnet run [options]` , а в нем предоставляются вызываемые аргументы.</span><span class="sxs-lookup"><span data-stu-id="5de3e-178">The general format for the command line is actually `dotnet run [options]`, and callable arguments are provided there.</span></span>
<span data-ttu-id="5de3e-179">В этом случае аргумент `n` отсутствует и показывает, что необходимо предоставить параметр `-n <n>` .</span><span class="sxs-lookup"><span data-stu-id="5de3e-179">In this case, the argument `n` is missing, and it shows that we need to provide the option `-n <n>`.</span></span> <span data-ttu-id="5de3e-180">Для запуска `MeasureSuperpositionArray` для `n=4` Кубитс мы используем</span><span class="sxs-lookup"><span data-stu-id="5de3e-180">To run `MeasureSuperpositionArray` for `n=4` qubits, we therefore use</span></span>

```dotnetcli
dotnet run -n 4
```

<span data-ttu-id="5de3e-181">выдается результат, аналогичный</span><span class="sxs-lookup"><span data-stu-id="5de3e-181">yielding an output similar to</span></span>

```output
[Zero,One,One,One]
```

<span data-ttu-id="5de3e-182">Этот курс распространяется на несколько аргументов.</span><span class="sxs-lookup"><span data-stu-id="5de3e-182">This of course extends to multiple arguments.</span></span>

> [!NOTE]
> <span data-ttu-id="5de3e-183">Имена аргументов, определенные в `camelCase` , немного изменяются компилятором для приема Q# входных данных.</span><span class="sxs-lookup"><span data-stu-id="5de3e-183">Argument names defined in `camelCase` are slightly altered by the compiler to be accepted as Q# inputs.</span></span> <span data-ttu-id="5de3e-184">Например, если вместо `n` используется имя, указанное `numQubits` выше, то эти входные данные будут предоставлены в командной строке с помощью `--num-qubits 4` вместо `-n 4` .</span><span class="sxs-lookup"><span data-stu-id="5de3e-184">For example, if instead of `n`, we used the name `numQubits` above, then this input would be provided in the command line via `--num-qubits 4` instead of `-n 4`.</span></span>

<span data-ttu-id="5de3e-185">В сообщении об ошибке также содержатся другие параметры, которые можно использовать, включая изменение целевого компьютера.</span><span class="sxs-lookup"><span data-stu-id="5de3e-185">The error message also provides other options which can be used, including how to change the target machine.</span></span>

### <a name="different-target-machines"></a><span data-ttu-id="5de3e-186">Разные целевые компьютеры</span><span class="sxs-lookup"><span data-stu-id="5de3e-186">Different target machines</span></span>

<span data-ttu-id="5de3e-187">Поскольку выходные данные наших операций, до сих пор, были ожидаемыми результатами их действия над реальным Кубитс, ясно, что целевой компьютер по умолчанию из командной строки — это имитатор такта полного состояния, `QuantumSimulator` .</span><span class="sxs-lookup"><span data-stu-id="5de3e-187">As the outputs from our operations thus far have been the expected results of their action on real qubits, it's clear that the default target machine from the command line is the full-state quantum simulator, `QuantumSimulator`.</span></span>
<span data-ttu-id="5de3e-188">Однако можно указать, что вызываемые функции должны выполняться на определенном целевом компьютере с параметром `--simulator` (или сокращенным `-s` ).</span><span class="sxs-lookup"><span data-stu-id="5de3e-188">However, we can instruct callables to be run on a specific target machine with the option `--simulator` (or the shorthand `-s`).</span></span>

<span data-ttu-id="5de3e-189">Например, мы можем запустить его на [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) :</span><span class="sxs-lookup"><span data-stu-id="5de3e-189">For example, we could run it on [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator):</span></span>

```dotnetcli
dotnet run -n 4 -s ResourcesEstimator
```

<span data-ttu-id="5de3e-190">Затем напечатанные выходные данные</span><span class="sxs-lookup"><span data-stu-id="5de3e-190">The printed output is then</span></span>

```output
Metric          Sum
CNOT            0
QubitClifford   4
R               0
Measure         4
T               0
Depth           0
Width           4
BorrowedWidth   0
```

<span data-ttu-id="5de3e-191">Дополнительные сведения о том, что означают эти метрики, см. в разделе [Resource оценщик: сообщаемые метрики](xref:microsoft.quantum.machines.resources-estimator#metrics-reported).</span><span class="sxs-lookup"><span data-stu-id="5de3e-191">For details on what these metrics indicate, see [Resource estimator: metrics reported](xref:microsoft.quantum.machines.resources-estimator#metrics-reported).</span></span>

### <a name="command-line-execution-summary"></a><span data-ttu-id="5de3e-192">Сводка выполнения командной строки</span><span class="sxs-lookup"><span data-stu-id="5de3e-192">Command line execution summary</span></span>
<br/>
<img src="../media/hostprograms_command_line_diagram.png" alt="Q# program from command line" width="700">

### <a name="non-no-locq-dotnet-run-options"></a><span data-ttu-id="5de3e-193">Без Q# `dotnet run` параметров</span><span class="sxs-lookup"><span data-stu-id="5de3e-193">Non-Q# `dotnet run` options</span></span>

<span data-ttu-id="5de3e-194">Как мы вкратце упоминали выше с помощью `--project` параметра, [ `dotnet run` команда](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) также принимает параметры, не связанные с Q# вызываемыми аргументами.</span><span class="sxs-lookup"><span data-stu-id="5de3e-194">As we briefly mentioned above with the `--project` option, the [`dotnet run` command](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) also accepts options unrelated to the Q# callable arguments.</span></span>
<span data-ttu-id="5de3e-195">При указании обоих типов параметров `dotnet` необходимо сначала указать параметры, а `--` затем разделителем, а затем Q# Параметры.</span><span class="sxs-lookup"><span data-stu-id="5de3e-195">If providing both kinds of options, the `dotnet`-specific options must be provided first, followed by a delimeter `--`, and then the Q#-specific options.</span></span>
<span data-ttu-id="5de3e-196">Например, указании пути вместе с числом Кубитс для операции выше, можно выполнить с помощью `dotnet run --project <PATH> -- -n <n>` .</span><span class="sxs-lookup"><span data-stu-id="5de3e-196">For example, specifiying a path along with a number qubits for the operation above would be executed via `dotnet run --project <PATH> -- -n <n>`.</span></span>

## <a name="no-locq-with-host-programs"></a><span data-ttu-id="5de3e-197">Q# с ведущими программами</span><span class="sxs-lookup"><span data-stu-id="5de3e-197">Q# with host programs</span></span>

<span data-ttu-id="5de3e-198">С помощью нашего Q# файла, альтернативой вызову операции или функции непосредственно из командной строки, является использование *основной программы* на другом классическом языке.</span><span class="sxs-lookup"><span data-stu-id="5de3e-198">With our Q# file in hand, an alternative to calling an operation or function directly from the command prompt is to use a *host program* in another classical language.</span></span> <span data-ttu-id="5de3e-199">В частности, это можно сделать с помощью Python или языка .NET, такого как C# или F # (для краткости мы будем подробно описать только C#).</span><span class="sxs-lookup"><span data-stu-id="5de3e-199">Specifically, this can be done with either Python or a .NET language such as C# or F# (for the sake of brevity we will only detail C# here).</span></span>
<span data-ttu-id="5de3e-200">Для обеспечения взаимодействия требуется небольшая Настройка, но эти сведения можно найти в [руководствах по установке](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="5de3e-200">A little more setup is required to enable the interoperability, but those details can be found in the [install guides](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="5de3e-201">В двух словах ситуация теперь включает файл программы узла (например, `*.py` или `*.cs` ) в том же расположении, что и наш Q# файл.</span><span class="sxs-lookup"><span data-stu-id="5de3e-201">In a nutshell, the situation now includes a host program file (e.g. `*.py` or `*.cs`) in the same location as our Q# file.</span></span>
<span data-ttu-id="5de3e-202">Теперь она выполняется *ведущим* приложением, и в процессе ее выполнения он может вызывать определенные Q# операции и функции из Q# файла.</span><span class="sxs-lookup"><span data-stu-id="5de3e-202">It's now the *host* program that gets run, and in the course of its execution it can call specific Q# operations and functions from the Q# file.</span></span>
<span data-ttu-id="5de3e-203">Ядро взаимодействия основано на том, что Q# компилятор делает содержимое Q# файла доступным для основной программы, чтобы их можно было вызывать.</span><span class="sxs-lookup"><span data-stu-id="5de3e-203">The core of the interoperability is based on the Q# compiler making the contents of the Q# file accessible to the host program so that they can be called.</span></span>

<span data-ttu-id="5de3e-204">Одним из основных преимуществ использования основной программы является то, что классические данные, возвращаемые программой, Q# можно затем обрабатывать на основном языке.</span><span class="sxs-lookup"><span data-stu-id="5de3e-204">One of the main benefits of using a host program is that the classical data returned by the Q# program can then be further processed in the host language.</span></span>
<span data-ttu-id="5de3e-205">Это может состоять из некоторых расширенных операций обработки данных (например, которые не могут быть выполнены внутри Q# ), а затем вызывают дальнейшие Q# действия на основе этих результатов или что-то простое, например, для отображения Q# результатов.</span><span class="sxs-lookup"><span data-stu-id="5de3e-205">This could consist of some advanced data processing (e.g. something that can't be performed internally in Q#), and then calling further Q# actions based on those results, or something as simple as plotting the Q# results.</span></span>

<span data-ttu-id="5de3e-206">Общая схема показана здесь, и мы рассмотрим конкретные реализации для Python и C# ниже.</span><span class="sxs-lookup"><span data-stu-id="5de3e-206">The general scheme is shown here, and we discuss the specific implementations for Python and C# below.</span></span> <span data-ttu-id="5de3e-207">Пример использования программы F # Host можно найти в [примерах взаимодействия с .NET](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet).</span><span class="sxs-lookup"><span data-stu-id="5de3e-207">A sample using an F# host program can be found at the [.NET interoperability samples](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet).</span></span>

<br/>
<img src="../media/hostprograms_host_program_diagram.png" alt="Q# program from a host program" width="700">

> [!NOTE]
> <span data-ttu-id="5de3e-208">`@EntryPoint()`Атрибут, используемый для Q# приложений, нельзя использовать с ведущими программами.</span><span class="sxs-lookup"><span data-stu-id="5de3e-208">The `@EntryPoint()` attribute used for Q# applications cannot be used with host programs.</span></span>
> <span data-ttu-id="5de3e-209">При наличии в Q# файле, вызываемом узлом, возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="5de3e-209">An error will be raised if it is present in the Q# file being called by a host.</span></span> 

<span data-ttu-id="5de3e-210">Для работы с разными ведущими программами не требуется вносить изменения в `*.qs` Q# файл.</span><span class="sxs-lookup"><span data-stu-id="5de3e-210">To work with different host programs, there are no changes required to a `*.qs` Q# file.</span></span>
<span data-ttu-id="5de3e-211">Следующие реализации основной программы работают с одним и тем же Q# файлом:</span><span class="sxs-lookup"><span data-stu-id="5de3e-211">The following host program implementations all work with the same Q# file:</span></span>

```qsharp
namespace NamespaceName {
    open Microsoft.Quantum.Intrinsic;     // contains H
    open Microsoft.Quantum.Measurement;   // MResetZ
    open Microsoft.Quantum.Canon;         // ApplyToEach
    open Microsoft.Quantum.Arrays;        // ForEach

    operation MeasureSuperposition() : Result {
        using (q = Qubit()) { 
            H(q);
            return MResetZ(q);
        }
    }

    operation MeasureSuperpositionArray(n : Int) : Result[] {
        using (qubits = Qubit[n]) {  
            ApplyToEach(H, qubits); 
            return ForEach(MResetZ, qubits);    
        }
    }
}
```

<span data-ttu-id="5de3e-212">Выберите вкладку, соответствующую интересующему языку узла.</span><span class="sxs-lookup"><span data-stu-id="5de3e-212">Select the tab corresponding to your host language of interest.</span></span>

### <a name="python"></a>[<span data-ttu-id="5de3e-213">Python</span><span class="sxs-lookup"><span data-stu-id="5de3e-213">Python</span></span>](#tab/tabid-python)
<span data-ttu-id="5de3e-214">Главное приложение Python создается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5de3e-214">A Python host program is constructed as follows:</span></span>
1. <span data-ttu-id="5de3e-215">Импортируйте `qsharp` модуль, который регистрирует загрузчик модуля для Q# взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="5de3e-215">Import the `qsharp` module, which registers the module loader for Q# interoperability.</span></span> 
    <span data-ttu-id="5de3e-216">Это позволяет Q# Отображать пространства имен в виде модулей Python, из которых можно импортировать Q# вызываемые.</span><span class="sxs-lookup"><span data-stu-id="5de3e-216">This allows Q# namespaces to appear as Python modules, from which we can "import" Q# callables.</span></span>
    <span data-ttu-id="5de3e-217">Обратите внимание, что он технически не является Q# самим вызываемыми методами, а только заглушками Python, которые позволяют вызывать их.</span><span class="sxs-lookup"><span data-stu-id="5de3e-217">Note that it is technically not the Q# callables themselves which are imported, but rather Python stubs which allow calling into them.</span></span>
    <span data-ttu-id="5de3e-218">Они ведут себя как объекты классов Python, на которых мы используем методы для указания целевых компьютеров для отправки операции для выполнения.</span><span class="sxs-lookup"><span data-stu-id="5de3e-218">These then behave as objects of Python classes, on which we use methods to specify the target machines to send the operation to for execution.</span></span>

2. <span data-ttu-id="5de3e-219">Импортируйте эти Q# вызываемые вызовы, которые будут напрямую вызывать---в этом случае `MeasureSuperposition` и `MeasureSuperpositionArray` .</span><span class="sxs-lookup"><span data-stu-id="5de3e-219">Import those Q# callables which we will directly invoke---in this case, `MeasureSuperposition` and `MeasureSuperpositionArray`.</span></span>
    ```python
    import qsharp
    from NamespaceName import MeasureSuperposition, MeasureSuperpositionArray
    ```
    <span data-ttu-id="5de3e-220">`qsharp`После импорта модуля можно также импортировать вызываемые модули непосредственно из Q# пространств имен библиотеки.</span><span class="sxs-lookup"><span data-stu-id="5de3e-220">With the `qsharp` module imported, you can also import callables directly from the Q# library namespaces.</span></span>

3. <span data-ttu-id="5de3e-221">Помимо любого другого кода Python теперь можно вызывать эти вызовы на конкретных целевых компьютерах и присваивать их переменным (если они возвращают значение) для дальнейшего использования.</span><span class="sxs-lookup"><span data-stu-id="5de3e-221">Among any other Python code, you can now call those callables on specific target machines, and assign their returns to variables (if they return a value) for further use.</span></span>

#### <a name="specifying-target-machines"></a><span data-ttu-id="5de3e-222">Указание целевых компьютеров</span><span class="sxs-lookup"><span data-stu-id="5de3e-222">Specifying target machines</span></span>
<span data-ttu-id="5de3e-223">Вызов операции для выполнения на определенном целевом компьютере выполняется с помощью различных методов Python для импортированного объекта.</span><span class="sxs-lookup"><span data-stu-id="5de3e-223">Calling an operation to be run on a specific target machine is done via different Python methods on the imported object.</span></span>
<span data-ttu-id="5de3e-224">Например, `.simulate(<args>)` использует `QuantumSimulator` для выполнения операции, тогда как `.estimate_resources(<args>)` это делается в `ResourcesEstimator` .</span><span class="sxs-lookup"><span data-stu-id="5de3e-224">For example, `.simulate(<args>)`, uses the `QuantumSimulator` to run the operation, whereas `.estimate_resources(<args>)` does so on the `ResourcesEstimator`.</span></span>

#### <a name="passing-inputs-to-q"></a><span data-ttu-id="5de3e-225">Передача входных данных в Q\#</span><span class="sxs-lookup"><span data-stu-id="5de3e-225">Passing inputs to Q\#</span></span>
<span data-ttu-id="5de3e-226">Аргументы для Q# вызываемого элемента должны быть указаны в виде аргумента ключевого слова, где ключевое слово является именем аргумента в Q# вызываемом определении.</span><span class="sxs-lookup"><span data-stu-id="5de3e-226">Arguments for the Q# callable should be provided in the form of a keyword argument, where the keyword is the argument name in the Q# callable definition.</span></span>
<span data-ttu-id="5de3e-227">Это `MeasureSuperpositionArray.simulate(n=4)` допустимо, тогда как `MeasureSuperpositionArray.simulate(4)` вызовет ошибку.</span><span class="sxs-lookup"><span data-stu-id="5de3e-227">That is, `MeasureSuperpositionArray.simulate(n=4)` is valid, whereas `MeasureSuperpositionArray.simulate(4)` would throw an error.</span></span>

<span data-ttu-id="5de3e-228">Таким образом, ведущее приложение Python</span><span class="sxs-lookup"><span data-stu-id="5de3e-228">Therefore, the Python host program</span></span> 

```python
import qsharp
from NamespaceName import MeasureSuperposition, MeasureSuperpositionArray

single_qubit_result = MeasureSuperposition.simulate()
single_qubit_resources = MeasureSuperposition.estimate_resources()

multi_qubit_result = MeasureSuperpositionArray.simulate(n=4)
multi_qubit_resources = MeasureSuperpositionArray.estimate_resources(n=4)

print('Single qubit:\n' + str(single_qubit_result))
print(single_qubit_resources)

print('\nMultiple qubits:\n' + str(multi_qubit_result))
print(multi_qubit_resources)
```

<span data-ttu-id="5de3e-229">выводит результат следующего вида:</span><span class="sxs-lookup"><span data-stu-id="5de3e-229">results in an output like the following:</span></span>

```output
Single qubit:
1
{'CNOT': 0, 'QubitClifford': 1, 'R': 0, 'Measure': 1, 'T': 0, 'Depth': 0, 'Width': 1, 'BorrowedWidth': 0}

Multiple qubits:
[0, 1, 1, 1]
{'CNOT': 0, 'QubitClifford': 4, 'R': 0, 'Measure': 4, 'T': 0, 'Depth': 0, 'Width': 4, 'BorrowedWidth': 0}
```

#### <a name="using-no-locq-code-from-other-projects-or-packages"></a><span data-ttu-id="5de3e-230">Использование Q# кода из других проектов или пакетов</span><span class="sxs-lookup"><span data-stu-id="5de3e-230">Using Q# code from other projects or packages</span></span>

<span data-ttu-id="5de3e-231">По умолчанию `import qsharp` команда загружает все `.qs` файлы из текущей папки и делает их Q# операции и функции доступными для использования внутри скрипта Python.</span><span class="sxs-lookup"><span data-stu-id="5de3e-231">By default, the `import qsharp` command loads all of the `.qs` files in the current folder and makes their Q# operations and functions available for use from inside the Python script.</span></span>

<span data-ttu-id="5de3e-232">Чтобы загрузить Q# код из другой папки, можно использовать [ `qsharp.projects` API](https://docs.microsoft.com/python/qsharp-core/qsharp.projects.projects) для добавления ссылки на `.csproj` файл для Q# проекта (то есть проекта, который ссылается на `Microsoft.Quantum.Sdk` ).</span><span class="sxs-lookup"><span data-stu-id="5de3e-232">To load Q# code from another folder, the [`qsharp.projects` API](https://docs.microsoft.com/python/qsharp-core/qsharp.projects.projects) can be used to add a reference to a `.csproj` file for a Q# project (that is, a project that references `Microsoft.Quantum.Sdk`).</span></span>
<span data-ttu-id="5de3e-233">Эта команда компилирует все `.qs` файлы в папке, содержащей и вложенные в `.csproj` нее папки.</span><span class="sxs-lookup"><span data-stu-id="5de3e-233">This command will compile any `.qs` files in the folder containing the `.csproj` and its subfolders.</span></span> <span data-ttu-id="5de3e-234">Кроме того, будут рекурсивно загружены все пакеты, на которые имеются ссылки через `PackageReference` или Q# проекты, упоминаемые `ProjectReference` в этом `.csproj` файле.</span><span class="sxs-lookup"><span data-stu-id="5de3e-234">It will also recursively load any packages referenced via `PackageReference` or Q# projects referenced via `ProjectReference` in that `.csproj` file.</span></span>

<span data-ttu-id="5de3e-235">Например, следующий код Python импортирует внешний проект, ссылаясь на его путь относительно текущей папки и вызывает одну из ее Q# операций:</span><span class="sxs-lookup"><span data-stu-id="5de3e-235">As an example, the following Python code imports an external project, referencing its path relative to the current folder, and invokes one of its Q# operations:</span></span>

```python
import qsharp
qsharp.projects.add("../qrng/Qrng.csproj")
from Qrng import SampleQuantumRandomNumberGenerator
print(f"Qrng result: {SampleQuantumRandomNumberGenerator.simulate()}")
```

<span data-ttu-id="5de3e-236">В результате результат будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5de3e-236">This results in output like the following:</span></span>

```output
Adding reference to project: ../qrng/Qrng.csproj
Qrng result: 0
```

<span data-ttu-id="5de3e-237">Для загрузки внешних пакетов Q# , содержащих код, используйте [ `qsharp.packages` API](https://docs.microsoft.com/python/qsharp-core/qsharp.packages.packages).</span><span class="sxs-lookup"><span data-stu-id="5de3e-237">To load external packages containing Q# code, use the [`qsharp.packages` API](https://docs.microsoft.com/python/qsharp-core/qsharp.packages.packages).</span></span>

<span data-ttu-id="5de3e-238">Если Q# код в текущей папке зависит от внешних проектов или пакетов, при выполнении могут возникнуть ошибки `import qsharp` , так как зависимости еще не загружены.</span><span class="sxs-lookup"><span data-stu-id="5de3e-238">If the Q# code in the current folder depends on external projects or packages, you may see errors when running `import qsharp`, since the dependencies have not yet been loaded.</span></span>
<span data-ttu-id="5de3e-239">Чтобы загрузить необходимые внешние пакеты или Q# проекты во время выполнения `import qsharp` команды, убедитесь, что папка с скриптом Python содержит `.csproj` файл, на который ссылается `Microsoft.Quantum.Sdk` .</span><span class="sxs-lookup"><span data-stu-id="5de3e-239">To load required external packages or Q# projects during the `import qsharp` command, ensure that the folder with the Python script contains a `.csproj` file which references `Microsoft.Quantum.Sdk`.</span></span> <span data-ttu-id="5de3e-240">В этом `.csproj` случае добавьте свойство в `<IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>` `<PropertyGroup>` .</span><span class="sxs-lookup"><span data-stu-id="5de3e-240">In that `.csproj`, add the property `<IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>` to the `<PropertyGroup>`.</span></span> <span data-ttu-id="5de3e-241">Это позволит Q# выполнить рекурсивную загрузку любых `ProjectReference` `PackageReference` элементов, найденных в `.csproj` ходе выполнения `import qsharp` команды.</span><span class="sxs-lookup"><span data-stu-id="5de3e-241">This will instruct IQ# to recursively load any `ProjectReference` or `PackageReference` items found in that `.csproj` during the `import qsharp` command.</span></span>

<span data-ttu-id="5de3e-242">Например, вот простой `.csproj` файл, который вызывает Q# автоматическую загрузку `Microsoft.Quantum.Chemistry` пакета:</span><span class="sxs-lookup"><span data-stu-id="5de3e-242">For example, here is a simple `.csproj` file that causes IQ# to automatically load the `Microsoft.Quantum.Chemistry` package:</span></span>

```xml
<Project Sdk="Microsoft.Quantum.Sdk/0.12.20072031">
    <PropertyGroup>
        <OutputType>Library</OutputType>
        <TargetFramework>netstandard2.1</TargetFramework>
        <IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>
    </PropertyGroup>
    <ItemGroup>
        <PackageReference Include="Microsoft.Quantum.Chemistry" Version="0.12.20072031" />
    </ItemGroup>
</Project>
```

> [!NOTE]
> <span data-ttu-id="5de3e-243">В настоящее время это пользовательское `<IQSharpLoadAutomatically>` свойство является обязательным для узлов Python, но в будущем это может стать поведением по умолчанию для `.csproj` файла, расположенного в той же папке, что и скрипт Python.</span><span class="sxs-lookup"><span data-stu-id="5de3e-243">Currently this custom `<IQSharpLoadAutomatically>` property is required by Python hosts, but in the future, this may become the default behavior for a `.csproj` file located in the same folder as the Python script.</span></span>

> [!NOTE]
> <span data-ttu-id="5de3e-244">В настоящее время `<QsharpCompile>` параметр в службах `.csproj` игнорируется узлами Python, и все `.qs` файлы в папке `.csproj` (включая вложенные папки) загружаются и компилируются.</span><span class="sxs-lookup"><span data-stu-id="5de3e-244">Currently the `<QsharpCompile>` setting in the `.csproj` is ignored by Python hosts, and all `.qs` files in the folder of the `.csproj` (including subfolders) are loaded and compiled.</span></span> <span data-ttu-id="5de3e-245">Поддержка `.csproj` параметров будет улучшена в будущем (Дополнительные сведения см. в разделе [икшарп # 277](https://github.com/microsoft/iqsharp/issues/277) ).</span><span class="sxs-lookup"><span data-stu-id="5de3e-245">Support for `.csproj` settings will be improved in the future (see [iqsharp#277](https://github.com/microsoft/iqsharp/issues/277) for more details).</span></span>


### <a name="c"></a>[<span data-ttu-id="5de3e-246">C#</span><span class="sxs-lookup"><span data-stu-id="5de3e-246">C#</span></span>](#tab/tabid-csharp)

<span data-ttu-id="5de3e-247">Управляющая программа C# имеет несколько компонентов и тесно работает с некоторыми компонентами КДК, например симуляторами, которые сами по себе основаны на C#.</span><span class="sxs-lookup"><span data-stu-id="5de3e-247">A C# host program has multiple components, and works very closely with some components of the QDK, such as the simulators, which are themselves built on C#.</span></span>

<span data-ttu-id="5de3e-248">Q#Компилятор работает здесь, создавая имя пространства имен C# с эквивалентным именем из Q# пространства имен в нашем Q# файле.</span><span class="sxs-lookup"><span data-stu-id="5de3e-248">The Q# compiler works here by generating an equivalently named C# namespace from the Q# namespace in our Q# file.</span></span>
<span data-ttu-id="5de3e-249">Он дополнительно создает класс C# с эквивалентным именем для каждого из Q# вызываемых или определенных типов.</span><span class="sxs-lookup"><span data-stu-id="5de3e-249">It further generates an equivalently named C# class for each of the Q# callables or types defined therein.</span></span>

<span data-ttu-id="5de3e-250">Во первых, мы делаем классы, используемые в нашей основной программе, доступными с `using` инструкциями, которые примерно аналогом на `open` инструкции в нашем Q# файле:</span><span class="sxs-lookup"><span data-stu-id="5de3e-250">First, we make any classes used in our host program available with `using` statements, which are roughly analagous to the `open` statements in our Q# file:</span></span>

```csharp
using System;
using System.Threading.Tasks;
using Microsoft.Quantum.Simulation.Simulators;    // contains the target machines (e.g. QuantumSimulator, ResourcesEstimator)
using NamespaceName;                              // make the Q# namespace available
```

<span data-ttu-id="5de3e-251">Далее мы объявляем пространство имен C#, несколько других битов и частей (см. полный блок кода ниже), а затем любое классическое программирование, которое нам бы хотелось (например, вычисление аргументов для Q# вызываемых элементов).</span><span class="sxs-lookup"><span data-stu-id="5de3e-251">Next, we declare our C# namespace, a few other bits and pieces (see the full code block below), and then any classical programming we would like (e.g. computing arguments for the Q# callables).</span></span>
<span data-ttu-id="5de3e-252">В нашем случае Последнее не требуется, но пример такого использования можно найти в  [примере взаимодействия с .NET](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet).</span><span class="sxs-lookup"><span data-stu-id="5de3e-252">The latter isn't necessary in our case, but an example of such usage can be found at the  [.NET interoperability sample](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet).</span></span>

#### <a name="target-machines"></a><span data-ttu-id="5de3e-253">Целевые компьютеры</span><span class="sxs-lookup"><span data-stu-id="5de3e-253">Target machines</span></span>

<span data-ttu-id="5de3e-254">Чтобы вернуться к Q# , необходимо создать экземпляр целевого компьютера, на котором будут выполняться наши операции.</span><span class="sxs-lookup"><span data-stu-id="5de3e-254">Getting back to Q#, we must create an instance of whatever target machine we will execute our operations on.</span></span>

```csharp
            using var sim = new QuantumSimulator();
```

<span data-ttu-id="5de3e-255">Использование других целевых компьютеров настолько просто, как создание экземпляра другого, хотя способ выполнения этих и обработки возвратов может немного отличаться.</span><span class="sxs-lookup"><span data-stu-id="5de3e-255">Using other target machines is as simple as instantiating a different one, although the manner of doing so and processing the returns can be slightly different.</span></span>
<span data-ttu-id="5de3e-256">Для краткости мы подносимся к [`QuantumSimulator`](xref:microsoft.quantum.machines.full-state-simulator) Now и включаем приведенный [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) [ниже](#including-the-resources-estimator).</span><span class="sxs-lookup"><span data-stu-id="5de3e-256">For brevity, we stick to the [`QuantumSimulator`](xref:microsoft.quantum.machines.full-state-simulator) for now, and include the [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) [below](#including-the-resources-estimator).</span></span>

<span data-ttu-id="5de3e-257">Каждый класс C#, созданный из Q# операций, имеет `Run` метод, первый аргумент которого должен быть экземпляром целевого компьютера.</span><span class="sxs-lookup"><span data-stu-id="5de3e-257">Each C# class generated from the Q# operations have a `Run` method, the first argument of which must be the target machine instance.</span></span>
<span data-ttu-id="5de3e-258">Итак, для запуска `MeasureSuperposition` в `QuantumSimulator` мы используем `MeasureSuperposition.Run(sim)` .</span><span class="sxs-lookup"><span data-stu-id="5de3e-258">So, to run `MeasureSuperposition` on the `QuantumSimulator`, we use `MeasureSuperposition.Run(sim)`.</span></span>
<span data-ttu-id="5de3e-259">Возвращаемые результаты могут быть назначены переменным в C#:</span><span class="sxs-lookup"><span data-stu-id="5de3e-259">The returned results can then be assigned to variables in C#:</span></span>

```csharp
            var singleQubitResult = await MeasureSuperposition.Run(sim);
```

> [!NOTE]
> <span data-ttu-id="5de3e-260">`Run`Метод выполняется асинхронно, так как это будет так для реального аппаратного оборудования, и поэтому `await` ключевое слово блокирует дальнейшее выполнение до завершения задачи.</span><span class="sxs-lookup"><span data-stu-id="5de3e-260">The `Run` method is executed asynchronously because this will be the case for real quantum hardware, and therefore the `await` keyword blocks further execution until the task completes.</span></span>

<span data-ttu-id="5de3e-261">Если вызываемый объект не содержит возвращаемых значений Q# (т. е. тип возвращаемого значения `Unit` ), то выполнение можно выполнять таким же образом, не назначая его переменной.</span><span class="sxs-lookup"><span data-stu-id="5de3e-261">If the Q# callable does not have any returns (i.e. has return type `Unit`), then the execution can still be done in the same manner without assigning it to a variable.</span></span>
<span data-ttu-id="5de3e-262">В этом случае вся строка будет просто состоять из</span><span class="sxs-lookup"><span data-stu-id="5de3e-262">In that case, the entire line would simply consist of</span></span> 
```csharp
await <callable>.Run(<simulator>);
```

#### <a name="arguments"></a><span data-ttu-id="5de3e-263">Аргументы</span><span class="sxs-lookup"><span data-stu-id="5de3e-263">Arguments</span></span>

<span data-ttu-id="5de3e-264">Все аргументы для Q# вызываемого объекта просто передаются как дополнительные аргументы, объект после на целевой компьютер.</span><span class="sxs-lookup"><span data-stu-id="5de3e-264">Any arguments to the Q# callable are simply passed as additional arguments afer the target machine.</span></span>
<span data-ttu-id="5de3e-265">Следовательно, результаты `MeasureSuperpositionArray` в `n=4` Кубитс будут выбирались через</span><span class="sxs-lookup"><span data-stu-id="5de3e-265">Hence the results of `MeasureSuperpositionArray` on `n=4` qubits would fetched via</span></span> 

```csharp
            var multiQubitResult = await MeasureSuperpositionArray.Run(sim, 4);
```

<span data-ttu-id="5de3e-266">Таким образом, полная управляющая программа C# может выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5de3e-266">A full C# host program could thus look like</span></span>

```csharp
using System;
using System.Threading.Tasks;
using Microsoft.Quantum.Simulation.Simulators;
using NamespaceName;

namespace host
{
    static class Program
    {
        static async Task Main(string[] args)
        {
            using var sim = new QuantumSimulator();

            var singleQubitResult = await MeasureSuperposition.Run(sim);
            var multiQubitResult = await MeasureSuperpositionArray.Run(sim, 4);

            Console.WriteLine($"Single qubit result: {singleQubitResult}");
            Console.WriteLine($"Multiple qubit result: {multiQubitResult}");
        }
    }
}
```

<span data-ttu-id="5de3e-267">В расположении файла C# можно запустить ведущее приложение из командной строки, введя</span><span class="sxs-lookup"><span data-stu-id="5de3e-267">At the location of the C# file, the host program can be run from the command prompt by entering</span></span>
```dotnetcli
dotnet run
```
<span data-ttu-id="5de3e-268">и в этом случае выходные данные будут записаны в консоль аналогично</span><span class="sxs-lookup"><span data-stu-id="5de3e-268">and in this case you will see output written to the console similar to</span></span> 
```output
Single qubit result: One
Multiple qubit result: [One,One,Zero,Zero]
```

> [!NOTE]
> <span data-ttu-id="5de3e-269">Из-за взаимодействия компилятора с пространствами имен можно было бы сделать Q# вызываемые возможности доступными без `using NamespaceName;` инструкции и просто сопоставлять заголовок пространства имен C# с ним.</span><span class="sxs-lookup"><span data-stu-id="5de3e-269">Due to the compiler's interoperability with namespaces, we could alternatively make our Q# callables available without the `using NamespaceName;` statement, and simply matching the C# namespace title to it.</span></span>
> <span data-ttu-id="5de3e-270">Это происходит путем замены `namespace host` на `namespace NamespaceName` .</span><span class="sxs-lookup"><span data-stu-id="5de3e-270">That is, by replacing `namespace host` with `namespace NamespaceName`.</span></span>

#### <a name="including-the-resources-estimator"></a><span data-ttu-id="5de3e-271">Включение средства оценки ресурсов</span><span class="sxs-lookup"><span data-stu-id="5de3e-271">Including the resources estimator</span></span>

<span data-ttu-id="5de3e-272">[`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator)Для получения выходных данных требуется немного другая реализация.</span><span class="sxs-lookup"><span data-stu-id="5de3e-272">The [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) requires a slightly different implementation to retrieve the output.</span></span>

<span data-ttu-id="5de3e-273">Во-первых, вместо того, чтобы создавать экземпляры в качестве переменных с помощью `using` оператора (как мы делаем с `QuantumSimulator` ), мы более просто создаем экземпляры объектов класса с помощью</span><span class="sxs-lookup"><span data-stu-id="5de3e-273">Firstly, instead of instantiating them as a variable with a `using` statement (as we do with the `QuantumSimulator`), we more directly instantiate objects of the class via</span></span>

```csharp
            var estimatorSingleQ = new ResourcesEstimator();
            var estimatorMultiQ = new ResourcesEstimator();
```

<span data-ttu-id="5de3e-274">Обратите внимание, что вместо одного целевого симулятора, используемого несколькими Q# операциями, мы создали по одному экземпляру для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="5de3e-274">Notice that instead of a single target simulator to be used by multiple Q# operations, we have instantiated one for each.</span></span> <span data-ttu-id="5de3e-275">Это связано с тем, что сами объекты изменяются при использовании в качестве целевых компьютеров, после чего их результаты можно извлечь с помощью метода класса `.ToTSV()` .</span><span class="sxs-lookup"><span data-stu-id="5de3e-275">This is because the objects themselves are modified when used as target machines, and their results can then be retrieved afterwards with the class method `.ToTSV()`.</span></span>

<span data-ttu-id="5de3e-276">Чтобы выполнить операции с помощью оценщиков ресурсов, мы используем</span><span class="sxs-lookup"><span data-stu-id="5de3e-276">To run the operations on the resource estimators, we use</span></span>

```csharp
            await MeasureSuperposition.Run(estimatorSingleQ);
            await MeasureSuperpositionArray.Run(estimatorMultiQ, 4);
```
<span data-ttu-id="5de3e-277">а затем получить результаты в виде значений с разделителями-табуляциями (TSV) с помощью `estimatorSingleQ.ToTSV()` и `estimatorMultiQ.ToTSV()` .</span><span class="sxs-lookup"><span data-stu-id="5de3e-277">and then fetch the results as tab-separated-values (TSV) with `estimatorSingleQ.ToTSV()` and `estimatorMultiQ.ToTSV()`.</span></span>

<span data-ttu-id="5de3e-278">Таким образом, полная управляющая программа C#, `QuantumSimulator` которая использует и, и `ResourcesEstimator` может принимать форму:</span><span class="sxs-lookup"><span data-stu-id="5de3e-278">So, a full C# host program making use of both the `QuantumSimulator` and `ResourcesEstimator` could take the form:</span></span>

```csharp
using System;
using System.Threading.Tasks;
using Microsoft.Quantum.Simulation.Simulators;
using NamespaceName;

namespace host
{
    static class Program
    {
        static async Task Main(string[] args)
        {
            using var sim = new QuantumSimulator();
            var estimatorSingleQ = new ResourcesEstimator();
            var estimatorMultiQ = new ResourcesEstimator();

            var singleQubitResult = await MeasureSuperposition.Run(sim);
            var multiQubitResult = await MeasureSuperpositionArray.Run(sim, 4);

            await MeasureSuperposition.Run(estimatorSingleQ);
            await MeasureSuperpositionArray.Run(estimatorMultiQ, 4);

            Console.WriteLine($"Single qubit result: {singleQubitResult}");
            Console.WriteLine("Single qubit resources:");
            Console.WriteLine(estimatorSingleQ.ToTSV());

            Console.WriteLine($"\nMultiple qubit result: {multiQubitResult}");
            Console.WriteLine("Multiple qubit resources:");
            Console.WriteLine(estimatorMultiQ.ToTSV());
        }
    }
}
```


<span data-ttu-id="5de3e-279">что выдаст результат, аналогичный</span><span class="sxs-lookup"><span data-stu-id="5de3e-279">which would yield output similar to</span></span>

```output
Single qubit result: One
Single qubit resources:
Metric          Sum
CNOT            0
QubitClifford   1
R               0
Measure         1
T               0
Depth           0
Width           1
BorrowedWidth   0

Multiple qubit result: [One,One,One,Zero]
Multiple qubit resources:
Metric          Sum
CNOT            0
QubitClifford   4
R               0
Measure         4
T               0
Depth           0
Width           4
BorrowedWidth   0
```

***

## <a name="no-locq-jupyter-notebooks"></a><span data-ttu-id="5de3e-280">Q# Записные книжки Jupyter</span><span class="sxs-lookup"><span data-stu-id="5de3e-280">Q# Jupyter Notebooks</span></span>
<span data-ttu-id="5de3e-281">Q# Записные книжки Jupyter используют Q# ядро I, которое позволяет определять, компилировать и выполнять Q# вызываемые объекты в одной записной книжке---все вместе с инструкциями, примечаниями и другим содержимым.</span><span class="sxs-lookup"><span data-stu-id="5de3e-281">Q# Jupyter Notebooks make use of the IQ# kernel, which allows you to define, compile, and run Q# callables in a single notebook---all alongside instructions, notes, and other content.</span></span>
<span data-ttu-id="5de3e-282">Это означает, что хотя можно импортировать и использовать содержимое `*.qs` Q# файлов, они не являются обязательными в модели выполнения.</span><span class="sxs-lookup"><span data-stu-id="5de3e-282">This means that while it is possible to import and use the contents of `*.qs` Q# files, they are not necessary in the execution model.</span></span>

<span data-ttu-id="5de3e-283">Здесь мы подробно расскажу, как выполнять Q# операции, описанные выше, но более широкие общие сведения об использовании Q# записных книжек Jupyter предоставляются по адресу [ Q# и Jupyter записным книжкам](https://github.com/microsoft/Quantum/blob/master/samples/getting-started/intro-to-iqsharp/Notebook.ipynb).</span><span class="sxs-lookup"><span data-stu-id="5de3e-283">Here, we will detail how to run the Q# operations defined above, but a more broad introduction to using Q# Jupyter Notebooks is provided at [Intro to Q# and Jupyter Notebooks](https://github.com/microsoft/Quantum/blob/master/samples/getting-started/intro-to-iqsharp/Notebook.ipynb).</span></span>

### <a name="defining-operations"></a><span data-ttu-id="5de3e-284">Определение операций</span><span class="sxs-lookup"><span data-stu-id="5de3e-284">Defining operations</span></span>

<span data-ttu-id="5de3e-285">В Q# Jupyter Notebook вы вводите Q# код так же, как и в пространстве имен Q# файла.</span><span class="sxs-lookup"><span data-stu-id="5de3e-285">In a Q# Jupyter Notebook, you enter Q# code just as we would from inside the namespace of a Q# file.</span></span>

<span data-ttu-id="5de3e-286">Таким образом, можно включить доступ к вызываемым из [ Q# стандартных библиотек](xref:microsoft.quantum.qsharplibintro) с `open` инструкциями для соответствующих пространств имен.</span><span class="sxs-lookup"><span data-stu-id="5de3e-286">So, we can enable access to callables from the [Q# standard libraries](xref:microsoft.quantum.qsharplibintro) with `open` statements for their respective namespaces.</span></span>
<span data-ttu-id="5de3e-287">При выполнении ячейки с такой инструкцией определения из этих пространств имен доступны во всей рабочей области.</span><span class="sxs-lookup"><span data-stu-id="5de3e-287">Upon running a cell with such a statement, the definitions from those namespaces are available throughout the workspace.</span></span>

> [!NOTE]
> <span data-ttu-id="5de3e-288">Вызываемые из [Microsoft. тактов. внутренних](xref:microsoft.quantum.intrinsic) и [Microsoft. тактов. Canon](xref:microsoft.quantum.canon) (например [`H`](xref:microsoft.quantum.intrinsic.h) , и [`ApplyToEach`](xref:microsoft.quantum.canon.applytoeach) ) автоматически доступны для операций, определенных в ячейках в Q# записных книжках Jupyter.</span><span class="sxs-lookup"><span data-stu-id="5de3e-288">Callables from [Microsoft.Quantum.Intrinsic](xref:microsoft.quantum.intrinsic) and [Microsoft.Quantum.Canon](xref:microsoft.quantum.canon) (e.g. [`H`](xref:microsoft.quantum.intrinsic.h) and [`ApplyToEach`](xref:microsoft.quantum.canon.applytoeach)) are automatically available to operations defined within cells in Q# Jupyter Notebooks.</span></span>
> <span data-ttu-id="5de3e-289">Однако это не верно для кода, который добавляется из внешних Q# исходных файлов (процесс, показанный в [ Q# Jupyter и записных книжках](https://github.com/microsoft/Quantum/blob/master/samples/getting-started/intro-to-iqsharp/Notebook.ipynb)).</span><span class="sxs-lookup"><span data-stu-id="5de3e-289">However, this is not true for code brought in from external Q# source files (a process shown at [Intro to Q# and Jupyter Notebooks](https://github.com/microsoft/Quantum/blob/master/samples/getting-started/intro-to-iqsharp/Notebook.ipynb)).</span></span> 
> 

<span data-ttu-id="5de3e-290">Аналогично, для определения операций требуется только написание Q# кода и выполнение ячейки.</span><span class="sxs-lookup"><span data-stu-id="5de3e-290">Similarly, defining operations requires only writing the Q# code and running the cell.</span></span>

<img src="../media/hostprograms_jupyter_op_def_crop.png" alt="Jupyter cell defining Q# operations" width="773">

<span data-ttu-id="5de3e-291">Затем в выходных данных перечисляются операции, которые затем могут быть вызваны из будущих ячеек.</span><span class="sxs-lookup"><span data-stu-id="5de3e-291">The output then lists those operations, which can then be called from future cells.</span></span>

### <a name="target-machines"></a><span data-ttu-id="5de3e-292">Целевые компьютеры</span><span class="sxs-lookup"><span data-stu-id="5de3e-292">Target machines</span></span>

<span data-ttu-id="5de3e-293">Функциональные возможности выполнения операций на конкретных целевых компьютерах предоставляются с помощью [ Q# волшебных команд](xref:microsoft.quantum.guide.quickref.iqsharp).</span><span class="sxs-lookup"><span data-stu-id="5de3e-293">The functionality to run operations on specific target machines is provided via [IQ# Magic Commands](xref:microsoft.quantum.guide.quickref.iqsharp).</span></span>
<span data-ttu-id="5de3e-294">Например, `%simulate` `QuantumSimulator` использует, и `%estimate` используется `ResourcesEstimator` :</span><span class="sxs-lookup"><span data-stu-id="5de3e-294">For example, `%simulate` makes use of the `QuantumSimulator`, and `%estimate` uses the `ResourcesEstimator`:</span></span>

<img src="../media/hostprograms_jupyter_no_args_sim_est_crop.png" alt="Jupyter cell simulating a Q# operation and running resource estimation" width="773">

### <a name="passing-inputs-to-functions-and-operations"></a><span data-ttu-id="5de3e-295">Передача входных данных в функции и операции</span><span class="sxs-lookup"><span data-stu-id="5de3e-295">Passing inputs to functions and operations</span></span>

<span data-ttu-id="5de3e-296">Для передачи входных данных в Q# операции аргументы могут передаваться в качестве `key=value` пар в команду выполнения Magic.</span><span class="sxs-lookup"><span data-stu-id="5de3e-296">To pass inputs to the Q# operations, the arguments can be passed as `key=value` pairs to the execution magic command.</span></span>
<span data-ttu-id="5de3e-297">Итак, для запуска `MeasureSuperpositionArray` с четырьмя Кубитс можно выполнить `%simulate MeasureSuperpositionArray n=4` следующее:</span><span class="sxs-lookup"><span data-stu-id="5de3e-297">So, to run `MeasureSuperpositionArray` with four qubits, we can run `%simulate MeasureSuperpositionArray n=4`:</span></span>

<img src="../media/hostprograms_jupyter_args_sim_crop.png" alt="Jupyter cell simulating a Q# operation with arguments" width="773">

<span data-ttu-id="5de3e-298">Этот шаблон можно использовать аналогично с `%estimate` и другими командами выполнения.</span><span class="sxs-lookup"><span data-stu-id="5de3e-298">This pattern can be used similarly with `%estimate` and other execution commands.</span></span>

### <a name="using-no-locq-code-from-other-projects-or-packages"></a><span data-ttu-id="5de3e-299">Использование Q# кода из других проектов или пакетов</span><span class="sxs-lookup"><span data-stu-id="5de3e-299">Using Q# code from other projects or packages</span></span>

<span data-ttu-id="5de3e-300">По умолчанию Q# Jupyter Notebook загружает все файлы из `.qs` текущей папки и делает их Q# операции и функции доступными для использования внутри записной книжки.</span><span class="sxs-lookup"><span data-stu-id="5de3e-300">By default, a Q# Jupyter Notebook loads all of the `.qs` files in the current folder and makes their Q# operations and functions available for use from inside the notebook.</span></span> <span data-ttu-id="5de3e-301">В [ `%who` команде Magic](xref:microsoft.quantum.iqsharp.magic-ref.who) перечислены все доступные в настоящее время Q# операции и функции.</span><span class="sxs-lookup"><span data-stu-id="5de3e-301">The [`%who` magic command](xref:microsoft.quantum.iqsharp.magic-ref.who) lists all currently-available Q# operations and functions.</span></span>

<span data-ttu-id="5de3e-302">Чтобы загрузить Q# код из другой папки, можно использовать [ `%project` команду Magic](xref:microsoft.quantum.iqsharp.magic-ref.project) , чтобы добавить ссылку на `.csproj` файл для Q# проекта (то есть проект, на который ссылается `Microsoft.Quantum.Sdk` ).</span><span class="sxs-lookup"><span data-stu-id="5de3e-302">To load Q# code from another folder, the [`%project` magic command](xref:microsoft.quantum.iqsharp.magic-ref.project) can be used to add a reference to a `.csproj` file for a Q# project (that is, a project that references `Microsoft.Quantum.Sdk`).</span></span> <span data-ttu-id="5de3e-303">Эта команда компилирует все `.qs` файлы в папке, содержащей папку `.csproj` (и вложенные папки).</span><span class="sxs-lookup"><span data-stu-id="5de3e-303">This command will compile any `.qs` files in the folder containing the `.csproj` (and subfolders).</span></span> <span data-ttu-id="5de3e-304">Кроме того, будут рекурсивно загружены все пакеты, на которые имеются ссылки через `PackageReference` или Q# проекты, упоминаемые `ProjectReference` в этом `.csproj` файле.</span><span class="sxs-lookup"><span data-stu-id="5de3e-304">It will also recursively load any packages referenced via `PackageReference` or Q# projects referenced via `ProjectReference` in that `.csproj` file.</span></span> 

<span data-ttu-id="5de3e-305">Например, в следующих ячейках имитируется Q# операция из внешнего проекта, на который ссылается путь к проекту по отношению к текущей папке:</span><span class="sxs-lookup"><span data-stu-id="5de3e-305">As an example, the following cells simulate a Q# operation from an external project, where the project path is referenced relative to the current folder:</span></span>

<img src="../media/hostprograms_jupyter_project_crop.png" alt="Jupyter cell simulating a Q# operation from an external project" width="773">

<span data-ttu-id="5de3e-306">Чтобы загрузить внешние пакеты Q# , содержащие код, используйте [ `%package` команду Magic](xref:microsoft.quantum.iqsharp.magic-ref.package).</span><span class="sxs-lookup"><span data-stu-id="5de3e-306">To load external packages containing Q# code, use the [`%package` magic command](xref:microsoft.quantum.iqsharp.magic-ref.package).</span></span>
<span data-ttu-id="5de3e-307">При загрузке пакета будут также доступны любые пользовательские команды Magic или отображаемые кодировщики, содержащиеся в сборках, которые являются частью пакета.</span><span class="sxs-lookup"><span data-stu-id="5de3e-307">Loading a package will also make available any custom magic commands or display encoders that are contained in any assemblies that are part of the package.</span></span>

<span data-ttu-id="5de3e-308">Чтобы загрузить внешние пакеты или Q# проекты в записную книжку инициализацию времени, убедитесь, что в папке записной книжки есть `.csproj` файл, на который ссылается `Microsoft.Quantum.Sdk` .</span><span class="sxs-lookup"><span data-stu-id="5de3e-308">To load external packages or Q# projects at notebook intialization time, ensure that the notebook folder contains a `.csproj` file which references `Microsoft.Quantum.Sdk`.</span></span> <span data-ttu-id="5de3e-309">В этом `.csproj` случае добавьте свойство в `<IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>` `<PropertyGroup>` .</span><span class="sxs-lookup"><span data-stu-id="5de3e-309">In that `.csproj`, add the property `<IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>` to the `<PropertyGroup>`.</span></span> <span data-ttu-id="5de3e-310">Это позволит Q# выполнить рекурсивную загрузку любых `ProjectReference` `PackageReference` элементов, найденных в, `.csproj` во время загрузки записной книжки.</span><span class="sxs-lookup"><span data-stu-id="5de3e-310">This will instruct IQ# to recursively load any `ProjectReference` or `PackageReference` items found in that `.csproj` at notebook load time.</span></span>

<span data-ttu-id="5de3e-311">Например, вот простой `.csproj` файл, который вызывает Q# автоматическую загрузку `Microsoft.Quantum.Chemistry` пакета:</span><span class="sxs-lookup"><span data-stu-id="5de3e-311">For example, here is a simple `.csproj` file that causes IQ# to automatically load the `Microsoft.Quantum.Chemistry` package:</span></span>

```xml
<Project Sdk="Microsoft.Quantum.Sdk/0.12.20072031">
    <PropertyGroup>
        <OutputType>Library</OutputType>
        <TargetFramework>netstandard2.1</TargetFramework>
        <IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>
    </PropertyGroup>
    <ItemGroup>
        <PackageReference Include="Microsoft.Quantum.Chemistry" Version="0.12.20072031" />
    </ItemGroup>
</Project>
```

> [!NOTE]
> <span data-ttu-id="5de3e-312">В настоящее время это пользовательское `<IQSharpLoadAutomatically>` свойство является обязательным для Q# Jupyter Notebook узлов, но в будущем это может стать поведением по умолчанию для `.csproj` файла, расположенного в той же папке, что и файл записной книжки.</span><span class="sxs-lookup"><span data-stu-id="5de3e-312">Currently this custom `<IQSharpLoadAutomatically>` property is required by Q# Jupyter Notebook hosts, but in the future, this may become the default behavior for a `.csproj` file located in the same folder as the notebook file.</span></span>

> [!NOTE]
> <span data-ttu-id="5de3e-313">В настоящее время `<QsharpCompile>` параметр в службах `.csproj` игнорируется Q# Jupyter Notebook узлами, а все `.qs` файлы в папке `.csproj` (включая вложенные папки) загружаются и компилируются.</span><span class="sxs-lookup"><span data-stu-id="5de3e-313">Currently the `<QsharpCompile>` setting in the `.csproj` is ignored by Q# Jupyter Notebook hosts, and all `.qs` files in the folder of the `.csproj` (including subfolders) are loaded and compiled.</span></span> <span data-ttu-id="5de3e-314">Поддержка `.csproj` параметров будет улучшена в будущем (Дополнительные сведения см. в разделе [икшарп # 277](https://github.com/microsoft/iqsharp/issues/277) ).</span><span class="sxs-lookup"><span data-stu-id="5de3e-314">Support for `.csproj` settings will be improved in the future (see [iqsharp#277](https://github.com/microsoft/iqsharp/issues/277) for more details).</span></span>
