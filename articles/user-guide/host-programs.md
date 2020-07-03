---
title: 'Способы запуска программы Q #'
description: 'Обзор различных способов выполнения Q # Programs. Из командной строки, Q # Jupyter Notebooks и классических ведущих приложений на языке Python или .NET.'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 05/15/2020
ms.topic: article
uid: microsoft.quantum.guide.host-programs
ms.openlocfilehash: 132c138d7c392ed2b4bd3d0079180b68adae4cfc
ms.sourcegitcommit: a3775921db1dc5c653c97b8fa8fe2c0ddd5261ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2020
ms.locfileid: "85887736"
---
# <a name="ways-to-run-a-q-program"></a><span data-ttu-id="54c23-104">Способы запуска программы Q #</span><span class="sxs-lookup"><span data-stu-id="54c23-104">Ways to run a Q# program</span></span>

<span data-ttu-id="54c23-105">Один из самых сильных достоинств набора разработки такта — это гибкость в различных платформах и средах разработки.</span><span class="sxs-lookup"><span data-stu-id="54c23-105">One of the Quantum Development Kit's greatest strengths is its flexibility across platforms and development environments.</span></span>
<span data-ttu-id="54c23-106">Однако это также означает, что новые пользователи Q # могут найти их в замешательстве или в подавляющем множестве вариантов, приведенных в этом [разделе.](xref:microsoft.quantum.install)</span><span class="sxs-lookup"><span data-stu-id="54c23-106">However, this also means that new Q# users may find themselves confused or overwhelmed by the numerous options found in the [install guide](xref:microsoft.quantum.install).</span></span>
<span data-ttu-id="54c23-107">На этой странице объясняется, что происходит при запуске программы Q #, и сравниваются различные способы, которые могут сделать пользователи.</span><span class="sxs-lookup"><span data-stu-id="54c23-107">On this page, we explain what happens when a Q# program is run, and compare the different ways in which users can do so.</span></span>

<span data-ttu-id="54c23-108">Основное отличие состоит в том, что Q # может быть запущен:</span><span class="sxs-lookup"><span data-stu-id="54c23-108">A primary distinction is that Q# can be run:</span></span>
- <span data-ttu-id="54c23-109">в качестве автономного приложения, где Q # — это единственный применяемый язык, и программа вызывается напрямую.</span><span class="sxs-lookup"><span data-stu-id="54c23-109">as a standalone application, where Q# is the only language involved and the program is invoked directly.</span></span> <span data-ttu-id="54c23-110">В этой категории есть два метода:</span><span class="sxs-lookup"><span data-stu-id="54c23-110">Two methods actually fall in this category:</span></span>
  - <span data-ttu-id="54c23-111">интерфейс командной строки</span><span class="sxs-lookup"><span data-stu-id="54c23-111">the command line interface</span></span>
  - <span data-ttu-id="54c23-112">Записные книжки Jupyter Notebook для Q#</span><span class="sxs-lookup"><span data-stu-id="54c23-112">Q# Jupyter Notebooks</span></span>
- <span data-ttu-id="54c23-113">с помощью дополнительной *основной программы*, написанной на Python или на языке .NET (например, C# или F #), который затем вызывает программу и может обрабатывать возвращенные результаты.</span><span class="sxs-lookup"><span data-stu-id="54c23-113">with an additional *host program*, written in Python or a .NET language (e.g. C# or F#), which then invokes the program and can further process returned results.</span></span>

<span data-ttu-id="54c23-114">Чтобы лучше понять эти процессы и их различия, рассмотрим простую программу Q # и Сравните способы их выполнения.</span><span class="sxs-lookup"><span data-stu-id="54c23-114">To best understand these processes and their differences, we consider a simple Q# program and compare the ways it can be executed.</span></span>

## <a name="basic-q-program"></a><span data-ttu-id="54c23-115">Базовая программа Q #</span><span class="sxs-lookup"><span data-stu-id="54c23-115">Basic Q# program</span></span>

<span data-ttu-id="54c23-116">Базовая программа-тактовая частота может состоять из подготовки Кубит в равной части Штатов $ \кет {0} $ and $ \кет {1} $, ее измерения и возврата результата, который будет случайным или одним из этих двух состояний с одинаковой вероятностью.</span><span class="sxs-lookup"><span data-stu-id="54c23-116">A basic quantum program might consist of preparing a qubit in an equal superposition of states $\ket{0}$ and $\ket{1}$, measuring it, and returning the result, which will be randomly either one of these two states with equal probability.</span></span>
<span data-ttu-id="54c23-117">В самом деле, этот процесс является ядром краткого руководства [генератора случайных чисел](xref:microsoft.quantum.quickstarts.qrng) .</span><span class="sxs-lookup"><span data-stu-id="54c23-117">Indeed, this process is at the core of the [quantum random number generator](xref:microsoft.quantum.quickstarts.qrng) quickstart.</span></span>

<span data-ttu-id="54c23-118">В Q # это будет выполнено с помощью следующего кода:</span><span class="sxs-lookup"><span data-stu-id="54c23-118">In Q#, this would be performed by the following code:</span></span>

```qsharp
        using (q = Qubit()) {    // allocates qubit for use (automatically in |0>)
            H(q);                // puts qubit in superposition of |0> and |1>
            return MResetZ(q);   // measures qubit, returns result (and resets it to |0> before deallocation)
        }
```

<span data-ttu-id="54c23-119">Однако этот код не может быть выполнен с помощью Q #.</span><span class="sxs-lookup"><span data-stu-id="54c23-119">However, this code alone can't be executed by Q#.</span></span>
<span data-ttu-id="54c23-120">Для этого ему нужно сделать тело [операции](xref:microsoft.quantum.guide.basics#q-operations-and-functions), которое затем выполняется при вызове---либо напрямую, либо другой операцией.</span><span class="sxs-lookup"><span data-stu-id="54c23-120">For that, it needs to make up the body of an [operation](xref:microsoft.quantum.guide.basics#q-operations-and-functions), which is then executed when called---either directly or by another operation.</span></span> <span data-ttu-id="54c23-121">Таким образом, можно написать операцию следующего вида:</span><span class="sxs-lookup"><span data-stu-id="54c23-121">Hence, you can write an operation of the following form:</span></span>
```qsharp
    operation MeasureSuperposition() : Result {
        using (q = Qubit()) {
            H(q);
            return MResetZ(q);
        }
    }
```
<span data-ttu-id="54c23-122">Вы определили операцию, `MeasureSuperposition` которая не принимает входные данные и возвращает значение типа [result](xref:microsoft.quantum.guide.types).</span><span class="sxs-lookup"><span data-stu-id="54c23-122">You have defined an operation, `MeasureSuperposition`, which takes no inputs and returns a value of type [Result](xref:microsoft.quantum.guide.types).</span></span>

<span data-ttu-id="54c23-123">Хотя примеры на этой странице состоят только из *операций*q #, все концепции, которые мы будем обсуждать, относятся к *функциям*q #, и поэтому мы вместе называемся *вызываемыми*.</span><span class="sxs-lookup"><span data-stu-id="54c23-123">While the examples on this page only consist of Q# *operations*, all of the concepts we will discuss pertain equally to Q# *functions*, and therefore we refer to them collectively as *callables*.</span></span> <span data-ttu-id="54c23-124">Их различия обсуждаются в разделе [Q # основы: операции и функции](xref:microsoft.quantum.guide.basics#q-operations-and-functions), а дополнительные сведения об их определении можно найти в разделе [операции и функции](xref:microsoft.quantum.guide.operationsfunctions).</span><span class="sxs-lookup"><span data-stu-id="54c23-124">Their differences are discussed at [Q# basics: operations and functions](xref:microsoft.quantum.guide.basics#q-operations-and-functions), and more details on defining them can be found at [Operations and functions](xref:microsoft.quantum.guide.operationsfunctions).</span></span>

### <a name="callable-defined-in-a-q-file"></a><span data-ttu-id="54c23-125">Вызываемый в файле Q #</span><span class="sxs-lookup"><span data-stu-id="54c23-125">Callable defined in a Q# file</span></span>

<span data-ttu-id="54c23-126">Вызываемый метод — это именно то, что вызывается и выполняется в Q #.</span><span class="sxs-lookup"><span data-stu-id="54c23-126">The callable is precisely what's called and run by Q#.</span></span>
<span data-ttu-id="54c23-127">Однако для этого требуется еще несколько дополнений к полному `*.qs` файлу Q #.</span><span class="sxs-lookup"><span data-stu-id="54c23-127">However, it requires a few more additions to comprise a full `*.qs` Q# file.</span></span>

<span data-ttu-id="54c23-128">Все типы Q # и вызываемые методы (как определяемые, так и встроенные в язык) определяются в *пространствах имен*, которые предоставляют полные имена, на которые затем можно ссылаться.</span><span class="sxs-lookup"><span data-stu-id="54c23-128">All Q# types and callables (both those you define and those intrinsic to the language) are defined within *namespaces*, which provide each a full name that can then be referenced.</span></span>

<span data-ttu-id="54c23-129">Например, [`H`](xref:microsoft.quantum.intrinsic.h) операции и находятся [`MResetZ`](xref:microsoft.quantum.measurement.mresetz) в [`Microsoft.Quantum.Instrinsic`](xref:microsoft.quantum.intrinsic) [`Microsoft.Quantum.Measurement`](xref:microsoft.quantum.measurement) пространствах имен и (в составе [стандартных библиотек Q #](xref:microsoft.quantum.qsharplibintro)).</span><span class="sxs-lookup"><span data-stu-id="54c23-129">For example, the [`H`](xref:microsoft.quantum.intrinsic.h) and [`MResetZ`](xref:microsoft.quantum.measurement.mresetz) operations are found in the [`Microsoft.Quantum.Instrinsic`](xref:microsoft.quantum.intrinsic) and [`Microsoft.Quantum.Measurement`](xref:microsoft.quantum.measurement) namespaces (part of the [Q# Standard Libraries](xref:microsoft.quantum.qsharplibintro)).</span></span>
<span data-ttu-id="54c23-130">Таким образом, они всегда могут вызываться с помощью *полных* имен `Microsoft.Quantum.Intrinsic.H(<qubit>)` , `Microsoft.Quantum.Measurement.MResetZ(<qubit>)` но всегда это приведет к очень небыстрому выполнению кода.</span><span class="sxs-lookup"><span data-stu-id="54c23-130">As such, they can always be called via their *full* names, `Microsoft.Quantum.Intrinsic.H(<qubit>)` and `Microsoft.Quantum.Measurement.MResetZ(<qubit>)`, but always doing this would lead to very cluttered code.</span></span>

<span data-ttu-id="54c23-131">Вместо этого `open` инструкции позволяют ссылаться на вызываемые команды с более кратким сокращенным именем, как мы сделали в теле операции выше.</span><span class="sxs-lookup"><span data-stu-id="54c23-131">Instead, `open` statements allow callables to be referenced with more concise shorthand, as we've done in the operation body above.</span></span>
<span data-ttu-id="54c23-132">Таким образом, полный файл Q #, содержащий нашу операцию, состоит из определения нашего пространства имен, открытия пространств имен для этих вызываемых операций, а затем нашей операции:</span><span class="sxs-lookup"><span data-stu-id="54c23-132">The full Q# file containing our operation would therefore consist of defining our own namespace, opening the namespaces for those callables our operation uses, and then our operation:</span></span>

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
> <span data-ttu-id="54c23-133">Пространства имен могут также быть *псевдонимами* при открытии, что может оказаться полезным, если имена вызываемых и типов в двух пространствах имен конфликтуют.</span><span class="sxs-lookup"><span data-stu-id="54c23-133">Namespaces can also be *aliased* when opened, which can be helpful if callable/type names in two namespaces conflict.</span></span>
> <span data-ttu-id="54c23-134">Например, можно использовать `open Microsoft.Quantum.Instrinsic as NamespaceWithH;` метод выше, а затем вызвать `H` через `NamespaceWithH.H(<qubit>)` .</span><span class="sxs-lookup"><span data-stu-id="54c23-134">For example, we could instead use `open Microsoft.Quantum.Instrinsic as NamespaceWithH;` above, and then call `H` via `NamespaceWithH.H(<qubit>)`.</span></span>

> [!NOTE]
> <span data-ttu-id="54c23-135">Единственным исключением является [`Microsoft.Quantum.Core`](xref:microsoft.quantum.core) пространство имен, которое всегда открывается автоматически.</span><span class="sxs-lookup"><span data-stu-id="54c23-135">One exception to all of this is the [`Microsoft.Quantum.Core`](xref:microsoft.quantum.core) namespace, which is always automatically opened.</span></span>
> <span data-ttu-id="54c23-136">Таким образом, вызываемые, например, [`Length`](xref:microsoft.quantum.core.length) всегда можно использовать напрямую.</span><span class="sxs-lookup"><span data-stu-id="54c23-136">Therefore, callables like [`Length`](xref:microsoft.quantum.core.length) can always be used directly.</span></span>

### <a name="execution-on-target-machines"></a><span data-ttu-id="54c23-137">Выполнение на целевых компьютерах</span><span class="sxs-lookup"><span data-stu-id="54c23-137">Execution on target machines</span></span>

<span data-ttu-id="54c23-138">Теперь общая модель выполнения программы Q # становится ясной.</span><span class="sxs-lookup"><span data-stu-id="54c23-138">Now the general execution model of a Q# program becomes clear.</span></span>

<br/>
<img src="../media/hostprograms_general_execution_model.png" alt="Q# program execution diagram" width="400">

<span data-ttu-id="54c23-139">Во – первых, конкретный вызываемый тип имеет доступ к любым другим вызываемым и типам, определенным в том же пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="54c23-139">Firstly, the specific callable to be executed has access to any other callables and types defined in the same namespace.</span></span>
<span data-ttu-id="54c23-140">Он также обращается к ним из любой [библиотеки Q #](xref:microsoft.quantum.libraries), но на них должны быть ссылки либо с помощью полного имени, либо с помощью `open` инструкций, описанных выше.</span><span class="sxs-lookup"><span data-stu-id="54c23-140">It also access those from any of the [Q# libraries](xref:microsoft.quantum.libraries), but those must be referenced either via their full name, or through the use of `open` statements described above.</span></span>

<span data-ttu-id="54c23-141">Затем сам вызываемый объект выполняется на *[целевом компьютере](xref:microsoft.quantum.machines)*.</span><span class="sxs-lookup"><span data-stu-id="54c23-141">The callable itself is then executed on a *[target machine](xref:microsoft.quantum.machines)*.</span></span>
<span data-ttu-id="54c23-142">Такие целевые компьютеры могут быть реальным оборудованием такта или несколькими симуляторами, доступными в составе КДК.</span><span class="sxs-lookup"><span data-stu-id="54c23-142">Such target machines can be actual quantum hardware or the multiple simulators available as part of the QDK.</span></span>
<span data-ttu-id="54c23-143">Для наших целей наиболее полезным целевым компьютером является экземпляр [симулятора полного состояния](xref:microsoft.quantum.machines.full-state-simulator), `QuantumSimulator` который вычисляет поведение программы так, как если бы оно выполнялось на компьютере такта без помех.</span><span class="sxs-lookup"><span data-stu-id="54c23-143">For our purposes here, the most useful target machine is an instance of the [full-state simulator](xref:microsoft.quantum.machines.full-state-simulator), `QuantumSimulator`, which calculates the program's behavior as if it were being executed on a noise-free quantum computer.</span></span>

<span data-ttu-id="54c23-144">До сих пор мы описывали, что происходит при выполнении определенного вызова Q #.</span><span class="sxs-lookup"><span data-stu-id="54c23-144">So far, we've described what happens when a specific Q# callable is being executed.</span></span>
<span data-ttu-id="54c23-145">Независимо от того, используется ли Q # в автономном приложении или с ведущим приложением, этот общий процесс является более или менее---поэтому гибкость КДК.</span><span class="sxs-lookup"><span data-stu-id="54c23-145">Regardless of whether Q# is used in a standalone application or with a host program, this general process is more or less the same---hence the QDK's flexibility.</span></span>
<span data-ttu-id="54c23-146">Различия между различными способами вызова пакета разработки тактов, таким образом, показывают, *как* выполняется вызов Q # вызываемого метода и каким образом возвращаются любые результаты.</span><span class="sxs-lookup"><span data-stu-id="54c23-146">The differences between the different ways of calling into the Quantum Development Kit therefore reveal themselves in *how* that Q# callable is called to be executed, and in what manner any results are returned.</span></span>
<span data-ttu-id="54c23-147">В частности, различия связаны с</span><span class="sxs-lookup"><span data-stu-id="54c23-147">More specifically, the differences revolve around</span></span> 
1. <span data-ttu-id="54c23-148">Указывает, какую Q # вызываемый вызов должен выполняться,</span><span class="sxs-lookup"><span data-stu-id="54c23-148">indicating which Q# callable is to be executed,</span></span>
2. <span data-ttu-id="54c23-149">как предоставляются потенциальные вызываемые аргументы,</span><span class="sxs-lookup"><span data-stu-id="54c23-149">how potential callable arguments are provided,</span></span>
3. <span data-ttu-id="54c23-150">Указание целевого компьютера, на котором выполняется, и</span><span class="sxs-lookup"><span data-stu-id="54c23-150">specifying the target machine on which to execute it, and</span></span>
4. <span data-ttu-id="54c23-151">возвращаемые результаты.</span><span class="sxs-lookup"><span data-stu-id="54c23-151">how any results are returned.</span></span>

<span data-ttu-id="54c23-152">Сначала мы обсудим, как это делается с помощью автономного приложения Q # из командной строки, а затем приступите к работе с ведущими программами Python и C#.</span><span class="sxs-lookup"><span data-stu-id="54c23-152">First, we discuss how this is done with the Q# standalone application from the command line, and then proceed to using Python and C# host programs.</span></span>
<span data-ttu-id="54c23-153">Мы зарезервировани автономное приложение Q # Jupyter записных книжек для последнего, так как в отличие от первых трех, основная функциональность не центрируется вокруг локального файла Q #.</span><span class="sxs-lookup"><span data-stu-id="54c23-153">We reserve the standalone application of Q# Jupyter Notebooks for last, because unlike the first three, it's primary functionality does not center around a local Q# file.</span></span>

> [!NOTE]
> <span data-ttu-id="54c23-154">Хотя мы не продемонстрируем его в этих примерах, одно соответствие между методами выполнения заключается в том, что все сообщения, выводимые из программы Q # ( [`Message`](xref:microsoft.quantum.intrinsic.message) например, или [`DumpMachine`](xref:microsoft.quantum.diagnostics.dumpmachine) ), обычно всегда будут напечатаны в соответствующей консоли.</span><span class="sxs-lookup"><span data-stu-id="54c23-154">Although we don't illustrate it in these examples, one commonality between the execution methods is that any messages printed from inside the Q# program (by way of [`Message`](xref:microsoft.quantum.intrinsic.message) or [`DumpMachine`](xref:microsoft.quantum.diagnostics.dumpmachine), for example) will typically always be printed to the respective console.</span></span>

## <a name="q-from-the-command-line"></a><span data-ttu-id="54c23-155">Q # из командной строки</span><span class="sxs-lookup"><span data-stu-id="54c23-155">Q# from the command line</span></span>
<span data-ttu-id="54c23-156">Один из самых простых способов приступить к написанию программ Q # заключается в том, чтобы не беспокоиться о отдельных файлах и на втором языке.</span><span class="sxs-lookup"><span data-stu-id="54c23-156">One of the easiest ways to get started writing Q# programs is to avoid worrying about separate files and a second language altogether.</span></span>
<span data-ttu-id="54c23-157">Использование Visual Studio Code или Visual Studio с расширением КДК позволяет легко работать с вызываемыми вызовами Q # только из одного файла Q #.</span><span class="sxs-lookup"><span data-stu-id="54c23-157">Using Visual Studio Code or Visual Studio with the QDK extension allows for a seamless work flow in which we run Q# callables from only a single Q# file.</span></span>

<span data-ttu-id="54c23-158">Для этого в конечном итоге будет вызвано выполнение программы путем ввода</span><span class="sxs-lookup"><span data-stu-id="54c23-158">For this, we will ultimately invoke the program's execution by entering</span></span>
```dotnetcli
dotnet run
```
<span data-ttu-id="54c23-159">в командной строке.</span><span class="sxs-lookup"><span data-stu-id="54c23-159">in the command line.</span></span>
<span data-ttu-id="54c23-160">Самый простой рабочий процесс заключается в том, что расположение каталога терминала совпадает с файлом Q #, который можно легко обрабатывать наряду с редактированием файла Q # с помощью интегрированного терминала в VS Code, например.</span><span class="sxs-lookup"><span data-stu-id="54c23-160">The simplest workflow is when the terminal's directory location is the same as the Q# file, which can be easily handled alongside Q# file editing by using the integrated terminal in VS Code, for example.</span></span>
<span data-ttu-id="54c23-161">Однако [ `dotnet run` команда](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) принимает множество параметров, и программа также может запускаться из другого расположения, просто указав `--project <PATH>` расположение файла Q #.</span><span class="sxs-lookup"><span data-stu-id="54c23-161">However, the [`dotnet run` command](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) accepts numerous options, and the program can also be run from a different location by simply providing `--project <PATH>` with the location of the Q# file.</span></span>


### <a name="add-entry-point-to-q-file"></a><span data-ttu-id="54c23-162">Добавить точку входа в Q # файл</span><span class="sxs-lookup"><span data-stu-id="54c23-162">Add entry point to Q# file</span></span>

<span data-ttu-id="54c23-163">Большинство файлов Q # будет содержать несколько вызываемых, поэтому, естественно, нам нужно позволить компилятору знать *, какую* вызываемую команду выполнить при вводе `dotnet run` команды.</span><span class="sxs-lookup"><span data-stu-id="54c23-163">Most Q# files will contain more than one callable, so naturally we need to let the compiler know *which* callable to execute when we provide the `dotnet run` command.</span></span>
<span data-ttu-id="54c23-164">Это делается простым изменением самого файла Q #:</span><span class="sxs-lookup"><span data-stu-id="54c23-164">This is done with a simple change to the Q# file itself:</span></span> 
    - <span data-ttu-id="54c23-165">Добавьте строку `@EntryPoint()` непосредственно перед вызываемым.</span><span class="sxs-lookup"><span data-stu-id="54c23-165">add a line with `@EntryPoint()` directly preceding the callable.</span></span>

<span data-ttu-id="54c23-166">Следовательно, наш файл, приведенный выше, стал</span><span class="sxs-lookup"><span data-stu-id="54c23-166">Our file from above would therefore become</span></span>
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

<span data-ttu-id="54c23-167">Теперь вызов `dotnet run` из командной строки ведет к `MeasureSuperposition` выполнению, а возвращаемое значение затем распечатывается непосредственно в терминале.</span><span class="sxs-lookup"><span data-stu-id="54c23-167">Now, a call of `dotnet run` from the command line leads to `MeasureSuperposition` being run, and the returned value is then printed directly to the terminal.</span></span>
<span data-ttu-id="54c23-168">Таким образом, вы увидите `One` или `Zero` печатаете.</span><span class="sxs-lookup"><span data-stu-id="54c23-168">So, you will see either `One` or `Zero` printed.</span></span> 

<span data-ttu-id="54c23-169">Обратите внимание, что при наличии нескольких вызываемых, определенных ниже, `MeasureSuperposition` будет выполняться только запуск.</span><span class="sxs-lookup"><span data-stu-id="54c23-169">Note that it doesn't matter if you have more callables defined below it, only `MeasureSuperposition` will be run.</span></span>
<span data-ttu-id="54c23-170">Кроме того, нет проблем, если вызываемый объект включает [Комментарии к документации](xref:microsoft.quantum.guide.filestructure#documentation-comments) до объявления, `@EntryPoint()` атрибут можно просто поместить над ними.</span><span class="sxs-lookup"><span data-stu-id="54c23-170">Additionally, it's no problem if your callable includes [documentation comments](xref:microsoft.quantum.guide.filestructure#documentation-comments) before its declaration, the `@EntryPoint()` attribute can be simply placed above them.</span></span>

### <a name="callable-arguments"></a><span data-ttu-id="54c23-171">Вызываемые аргументы</span><span class="sxs-lookup"><span data-stu-id="54c23-171">Callable arguments</span></span>

<span data-ttu-id="54c23-172">До сих пор мы рассматривали только операцию, которая не принимает входные данные.</span><span class="sxs-lookup"><span data-stu-id="54c23-172">So far, we've only considered an operation that takes no inputs.</span></span>
<span data-ttu-id="54c23-173">Предположим, что мы хотели выполнить аналогичную операцию, но на нескольких Кубитс---число, предоставленное в качестве аргумента.</span><span class="sxs-lookup"><span data-stu-id="54c23-173">Suppose we wanted to perform a similar operation, but on multiple qubits---the number of which is provided as an argument.</span></span>
<span data-ttu-id="54c23-174">Такую операцию можно написать так:</span><span class="sxs-lookup"><span data-stu-id="54c23-174">Such an operation could be written as</span></span>
```qsharp
    operation MeasureSuperpositionArray(n : Int) : Result[] {
        using (qubits = Qubit[n]) {              // allocate a register of n qubits
            ApplyToEach(H, qubits);              // apply H to each qubit in the register
            return ForEach(MResetZ, qubits);     // perform MResetZ on each qubit, returns the resulting array
        }
    }
```
<span data-ttu-id="54c23-175">, где возвращаемое значение является массивом результатов измерения.</span><span class="sxs-lookup"><span data-stu-id="54c23-175">where the returned value is an array of the measurement results.</span></span>
<span data-ttu-id="54c23-176">Обратите внимание, что [`ApplyToEach`](xref:microsoft.quantum.canon.applytoeach) и [`ForEach`](xref:microsoft.quantum.arrays.foreach) находятся в [`Microsoft.Quantum.Canon`](xref:microsoft.quantum.canon) [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) пространствах имен и, для каждого из которых требуются дополнительные `open` инструкции.</span><span class="sxs-lookup"><span data-stu-id="54c23-176">Note that [`ApplyToEach`](xref:microsoft.quantum.canon.applytoeach) and [`ForEach`](xref:microsoft.quantum.arrays.foreach) are in the [`Microsoft.Quantum.Canon`](xref:microsoft.quantum.canon) and [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) namespaces, requiring additional `open` statements for each.</span></span>

<span data-ttu-id="54c23-177">Если переместить `@EntryPoint()` атрибут в перед этой новой операцией (Обратите внимание, что в файле может быть только одна строка), попытка запустить ее с помощью просто `dotnet run` приведет к появлении сообщения об ошибке, которое указывает, какие дополнительные параметры командной строки требуются и как их выразить.</span><span class="sxs-lookup"><span data-stu-id="54c23-177">If we move the `@EntryPoint()` attribute to precede this new operation (note there can only be one such line in a file), attempting to run it with simply `dotnet run` results in an error message which indicates what additional command line options are required, and how to express them.</span></span>

<span data-ttu-id="54c23-178">В действительности в командной строке используется общий формат `dotnet run [options]` , а в нем предоставляются вызываемые аргументы.</span><span class="sxs-lookup"><span data-stu-id="54c23-178">The general format for the command line is actually `dotnet run [options]`, and callable arguments are provided there.</span></span>
<span data-ttu-id="54c23-179">В этом случае аргумент `n` отсутствует и показывает, что необходимо предоставить параметр `-n <n>` .</span><span class="sxs-lookup"><span data-stu-id="54c23-179">In this case, the argument `n` is missing, and it shows that we need to provide the option `-n <n>`.</span></span> <span data-ttu-id="54c23-180">Для запуска `MeasureSuperpositionArray` для `n=4` Кубитс мы используем</span><span class="sxs-lookup"><span data-stu-id="54c23-180">To run `MeasureSuperpositionArray` for `n=4` qubits, we therefore use</span></span>

```dotnetcli
dotnet run -n 4
```

<span data-ttu-id="54c23-181">выдается результат, аналогичный</span><span class="sxs-lookup"><span data-stu-id="54c23-181">yielding an output similar to</span></span>

```output
[Zero,One,One,One]
```

<span data-ttu-id="54c23-182">Этот курс распространяется на несколько аргументов.</span><span class="sxs-lookup"><span data-stu-id="54c23-182">This of course extends to multiple arguments.</span></span>

> [!NOTE]
> <span data-ttu-id="54c23-183">Имена аргументов, определенные в `camelCase` , немного изменяются компилятором для принятия в качестве входных данных Q #.</span><span class="sxs-lookup"><span data-stu-id="54c23-183">Argument names defined in `camelCase` are slightly altered by the compiler to be accepted as Q# inputs.</span></span> <span data-ttu-id="54c23-184">Например, если вместо `n` используется имя, указанное `numQubits` выше, то эти входные данные будут предоставлены в командной строке с помощью `--num-qubits 4` вместо `-n 4` .</span><span class="sxs-lookup"><span data-stu-id="54c23-184">For example, if instead of `n`, we used the name `numQubits` above, then this input would be provided in the command line via `--num-qubits 4` instead of `-n 4`.</span></span>

<span data-ttu-id="54c23-185">В сообщении об ошибке также содержатся другие параметры, которые можно использовать, включая изменение целевого компьютера.</span><span class="sxs-lookup"><span data-stu-id="54c23-185">The error message also provides other options which can be used, including how to change the target machine.</span></span>

### <a name="different-target-machines"></a><span data-ttu-id="54c23-186">Разные целевые компьютеры</span><span class="sxs-lookup"><span data-stu-id="54c23-186">Different target machines</span></span>

<span data-ttu-id="54c23-187">По мере того, как выходные данные наших операций были ожидаемыми результатами их действия над реальным Кубитс, ясно, что целевой компьютер по умолчанию из командной строки является симулятором куаунтум полного состояния `QuantumSimulator` .</span><span class="sxs-lookup"><span data-stu-id="54c23-187">As the outputs from our operations thus far have been the expected results of their action on real qubits, it's clear that the default target machine from the command line is the full-state quauntum simulator, `QuantumSimulator`.</span></span>
<span data-ttu-id="54c23-188">Однако можно указать, что вызываемые функции должны выполняться на определенном целевом компьютере с параметром `--simulator` (или сокращенным `-s` ).</span><span class="sxs-lookup"><span data-stu-id="54c23-188">However, we can instruct callables to be run on a specific target machine with the option `--simulator` (or the shorthand `-s`).</span></span>

<span data-ttu-id="54c23-189">Например, мы можем запустить его на [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) :</span><span class="sxs-lookup"><span data-stu-id="54c23-189">For example, we could run it on [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator):</span></span>

```dotnetcli
dotnet run -n 4 -s ResourcesEstimator
```

<span data-ttu-id="54c23-190">Затем напечатанные выходные данные</span><span class="sxs-lookup"><span data-stu-id="54c23-190">The printed output is then</span></span>

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

<span data-ttu-id="54c23-191">Дополнительные сведения о том, что означают эти метрики, см. в разделе [Resource оценщик: сообщаемые метрики](xref:microsoft.quantum.machines.resources-estimator#metrics-reported).</span><span class="sxs-lookup"><span data-stu-id="54c23-191">For details on what these metrics indicate, see [Resource estimator: metrics reported](xref:microsoft.quantum.machines.resources-estimator#metrics-reported).</span></span>

### <a name="command-line-execution-summary"></a><span data-ttu-id="54c23-192">Сводка выполнения командной строки</span><span class="sxs-lookup"><span data-stu-id="54c23-192">Command line execution summary</span></span>
<br/>
<img src="../media/hostprograms_command_line_diagram.png" alt="Q# program from command line" width="700">

### <a name="non-q-dotnet-run-options"></a><span data-ttu-id="54c23-193">Параметры, отличные от Q # `dotnet run`</span><span class="sxs-lookup"><span data-stu-id="54c23-193">Non-Q# `dotnet run` options</span></span>

<span data-ttu-id="54c23-194">Как мы вкратце упоминали выше с помощью `--project` параметра, [ `dotnet run` команда](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) также принимает параметры, не связанные с вызываемыми аргументами Q #.</span><span class="sxs-lookup"><span data-stu-id="54c23-194">As we briefly mentioned above with the `--project` option, the [`dotnet run` command](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) also accepts options unrelated to the Q# callable arguments.</span></span>
<span data-ttu-id="54c23-195">При предоставлении обоих типов параметров `dotnet` необходимо сначала указать параметры, а `--` затем разделителем, а затем Параметры Q #.</span><span class="sxs-lookup"><span data-stu-id="54c23-195">If providing both kinds of options, the `dotnet`-specific options must be provided first, followed by a delimeter `--`, and then the Q#-specific options.</span></span>
<span data-ttu-id="54c23-196">Например, указании пути вместе с числом Кубитс для операции выше, можно выполнить с помощью `dotnet run --project <PATH> -- -n <n>` .</span><span class="sxs-lookup"><span data-stu-id="54c23-196">For example, specifiying a path along with a number qubits for the operation above would be executed via `dotnet run --project <PATH> -- -n <n>`.</span></span>

## <a name="q-with-host-programs"></a><span data-ttu-id="54c23-197">Q # с ведущими программами</span><span class="sxs-lookup"><span data-stu-id="54c23-197">Q# with host programs</span></span>

<span data-ttu-id="54c23-198">С помощью нашего файла Q # вместо вызова операции или функции непосредственно из командной строки следует использовать *управляющую программу* на другом классическом языке.</span><span class="sxs-lookup"><span data-stu-id="54c23-198">With our Q# file in hand, an alternative to calling an operation or function directly from the command line is to use a *host program* in another classical language.</span></span> <span data-ttu-id="54c23-199">В частности, это можно сделать с помощью Python или языка .NET, такого как C# или F # (для краткости мы будем подробно описать только C#).</span><span class="sxs-lookup"><span data-stu-id="54c23-199">Specifically, this can be done with either Python or a .NET language such as C# or F# (for the sake of brevity we will only detail C# here).</span></span>
<span data-ttu-id="54c23-200">Для обеспечения взаимодействия требуется небольшая Настройка, но эти сведения можно найти в [руководствах по установке](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="54c23-200">A little more setup is required to enable the interoperability, but those details can be found in the [install guides](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="54c23-201">В двух словах ситуация теперь включает файл программы узла (например, `*.py` или `*.cs` ) в том же расположении, что и файл Q #.</span><span class="sxs-lookup"><span data-stu-id="54c23-201">In a nutshell, the situation now includes a host program file (e.g. `*.py` or `*.cs`) in the same location as our Q# file.</span></span>
<span data-ttu-id="54c23-202">Теперь она *работает, и* в процессе ее выполнения она может вызывать конкретные операции и функции q # из файла Q #.</span><span class="sxs-lookup"><span data-stu-id="54c23-202">It's now the *host* program that gets run, and in the course of its execution it can call specific Q# operations and functions from the Q# file.</span></span>
<span data-ttu-id="54c23-203">Ядро взаимодействия основано на компиляторе Q #, делающем содержимое файла Q # доступным для хост-программы, чтобы их можно было вызывать.</span><span class="sxs-lookup"><span data-stu-id="54c23-203">The core of the interoperability is based on the Q# compiler making the contents of the Q# file accessible to the host program so that they can be called.</span></span>

<span data-ttu-id="54c23-204">Одним из основных преимуществ использования основной программы является то, что классические данные, возвращаемые программой Q #, затем можно обрабатывать на основном языке.</span><span class="sxs-lookup"><span data-stu-id="54c23-204">One of the main benefits of using a host program is that the classical data returned by the Q# program can then be further processed in the host language.</span></span>
<span data-ttu-id="54c23-205">Это может состоять из сложной обработки данных (например, не может быть выполнена внутри Q #), а затем вызывать дальнейшие действия Q # на основе этих результатов или что-то простое, например отобразить результаты Q #.</span><span class="sxs-lookup"><span data-stu-id="54c23-205">This could consist of some advanced data processing (e.g. something that can't be performed internally in Q#), and then calling further Q# actions based on those results, or something as simple as plotting the Q# results.</span></span>

<span data-ttu-id="54c23-206">Общая схема показана здесь, и мы рассмотрим конкретные реализации для Python и C# ниже.</span><span class="sxs-lookup"><span data-stu-id="54c23-206">The general scheme is shown here, and we discuss the specific implementations for Python and C# below.</span></span> <span data-ttu-id="54c23-207">Пример использования программы F # Host можно найти в [примерах взаимодействия с .NET](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet).</span><span class="sxs-lookup"><span data-stu-id="54c23-207">A sample using an F# host program can be found at the [.NET interoperability samples](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet).</span></span>

<br/>
<img src="../media/hostprograms_host_program_diagram.png" alt="Q# program from a host program" width="700">

> [!NOTE]
> <span data-ttu-id="54c23-208">`@EntryPoint()`Атрибут, используемый для приложений командной строки Q #, нельзя использовать с ведущими программами.</span><span class="sxs-lookup"><span data-stu-id="54c23-208">The `@EntryPoint()` attribute used for Q# command line applications cannot be used with host programs.</span></span>
> <span data-ttu-id="54c23-209">При наличии в файле Q #, вызываемом узлом, возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="54c23-209">An error will be raised if it is present in the Q# file being called by a host.</span></span> 

<span data-ttu-id="54c23-210">Для работы с разными ведущими программами не требуется вносить изменения в `*.qs` файл Q #.</span><span class="sxs-lookup"><span data-stu-id="54c23-210">To work with different host programs, there are no changes required to a `*.qs` Q# file.</span></span>
<span data-ttu-id="54c23-211">Следующие реализации основной программы работают с одним и тем же файлом Q #:</span><span class="sxs-lookup"><span data-stu-id="54c23-211">The following host program implementations all work with the same Q# file:</span></span>

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

<span data-ttu-id="54c23-212">Выберите вкладку, соответствующую интересующему языку узла.</span><span class="sxs-lookup"><span data-stu-id="54c23-212">Select the tab corresponding to your host language of interest.</span></span>

### <a name="python"></a>[<span data-ttu-id="54c23-213">Python</span><span class="sxs-lookup"><span data-stu-id="54c23-213">Python</span></span>](#tab/tabid-python)
<span data-ttu-id="54c23-214">Главное приложение Python создается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="54c23-214">A Python host program is constructed as follows:</span></span>
1. <span data-ttu-id="54c23-215">Импортируйте `qsharp` модуль, который регистрирует загрузчик модуля для взаимодействия Q #.</span><span class="sxs-lookup"><span data-stu-id="54c23-215">Import the `qsharp` module, which registers the module loader for Q# interoperability.</span></span> 
    <span data-ttu-id="54c23-216">Это позволяет пространствам имен Q # отображаться как модули Python, из которых можно импортировать вызываемые вопросы Q #.</span><span class="sxs-lookup"><span data-stu-id="54c23-216">This allows Q# namespaces to appear as Python modules, from which we can "import" Q# callables.</span></span>
    <span data-ttu-id="54c23-217">Обратите внимание, что технически не вызываемые функции Q #, которые импортируются, а представляют собой заглушки Python, которые позволяют вызывать их.</span><span class="sxs-lookup"><span data-stu-id="54c23-217">Note that it is technically not the Q# callables themselves which are imported, but rather Python stubs which allow calling into them.</span></span>
    <span data-ttu-id="54c23-218">Они ведут себя как объекты классов Python, на которых мы используем методы для указания целевых компьютеров для отправки операции для выполнения.</span><span class="sxs-lookup"><span data-stu-id="54c23-218">These then behave as objects of Python classes, on which we use methods to specify the target machines to send the operation to for execution.</span></span>

2. <span data-ttu-id="54c23-219">Импортируйте эти вызываемые вопросы Q #, которые будут напрямую вызывать---в этом случае `MeasureSuperposition` и `MeasureSuperpositionArray` .</span><span class="sxs-lookup"><span data-stu-id="54c23-219">Import those Q# callables which we will directly invoke---in this case, `MeasureSuperposition` and `MeasureSuperpositionArray`.</span></span>
    ```python
    import qsharp
    from NamespaceName import MeasureSuperposition, MeasureSuperpositionArray
    ```
    <span data-ttu-id="54c23-220">`qsharp`После импорта модуля можно также импортировать вызываемые модули непосредственно из пространств имен библиотеки Q #.</span><span class="sxs-lookup"><span data-stu-id="54c23-220">With the `qsharp` module imported, you can also import callables directly from the Q# library namespaces.</span></span>

3. <span data-ttu-id="54c23-221">Помимо любого другого кода Python теперь можно вызывать эти вызовы на конкретных целевых компьютерах и присваивать их переменным (если они возвращают значение) для дальнейшего использования.</span><span class="sxs-lookup"><span data-stu-id="54c23-221">Among any other Python code, you can now call those callables on specific target machines, and assign their returns to variables (if they return a value) for further use.</span></span>

#### <a name="specifying-target-machines"></a><span data-ttu-id="54c23-222">Указание целевых компьютеров</span><span class="sxs-lookup"><span data-stu-id="54c23-222">Specifying target machines</span></span>
<span data-ttu-id="54c23-223">Вызов операции для выполнения на определенном целевом компьютере выполняется с помощью различных методов Python для импортированного объекта.</span><span class="sxs-lookup"><span data-stu-id="54c23-223">Calling an operation to be run on a specific target machine is done via different Python methods on the imported object.</span></span>
<span data-ttu-id="54c23-224">Например, `.simulate(<args>)` использует `QuantumSimulator` для выполнения операции, тогда как `.estimate_resources(<args>)` это делается в `ResourcesEstimator` .</span><span class="sxs-lookup"><span data-stu-id="54c23-224">For example, `.simulate(<args>)`, uses the `QuantumSimulator` to run the operation, whereas `.estimate_resources(<args>)` does so on the `ResourcesEstimator`.</span></span>

#### <a name="passing-inputs-to-q"></a><span data-ttu-id="54c23-225">Передача входных данных в Q\#</span><span class="sxs-lookup"><span data-stu-id="54c23-225">Passing inputs to Q\#</span></span>
<span data-ttu-id="54c23-226">Аргументы для вызываемого параметра Q # должны быть предоставлены в виде аргумента ключевого слова, где ключевое слово — это имя аргумента в определении Q #.</span><span class="sxs-lookup"><span data-stu-id="54c23-226">Arguments for the Q# callable should be provided in the form of a keyword argument, where the keyword is the argument name in the Q# callable definition.</span></span>
<span data-ttu-id="54c23-227">Это `MeasureSuperpositionArray.simulate(n=4)` допустимо, тогда как `MeasureSuperpositionArray.simulate(4)` вызовет ошибку.</span><span class="sxs-lookup"><span data-stu-id="54c23-227">That is, `MeasureSuperpositionArray.simulate(n=4)` is valid, whereas `MeasureSuperpositionArray.simulate(4)` would throw an error.</span></span>

<span data-ttu-id="54c23-228">Таким образом, ведущее приложение Python</span><span class="sxs-lookup"><span data-stu-id="54c23-228">Therefore, the Python host program</span></span> 

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

<span data-ttu-id="54c23-229">выводит результат следующего вида:</span><span class="sxs-lookup"><span data-stu-id="54c23-229">results in an output like the following:</span></span>

```python
Single qubit:
1
{'CNOT': 0, 'QubitClifford': 1, 'R': 0, 'Measure': 1, 'T': 0, 'Depth': 0, 'Width': 1, 'BorrowedWidth': 0}

Multiple qubits:
[0, 1, 1, 1]
{'CNOT': 0, 'QubitClifford': 4, 'R': 0, 'Measure': 4, 'T': 0, 'Depth': 0, 'Width': 4, 'BorrowedWidth': 0}
```

### <a name="c"></a>[<span data-ttu-id="54c23-230">C#</span><span class="sxs-lookup"><span data-stu-id="54c23-230">C#</span></span>](#tab/tabid-csharp)

<span data-ttu-id="54c23-231">Управляющая программа C# имеет несколько компонентов и тесно работает с некоторыми компонентами КДК, например симуляторами, которые сами по себе основаны на C#.</span><span class="sxs-lookup"><span data-stu-id="54c23-231">A C# host program has multiple components, and works very closely with some components of the QDK, such as the simulators, which are themselves built on C#.</span></span>

<span data-ttu-id="54c23-232">Компилятор Q # работает здесь, создавая имя пространства имен C# с эквивалентным именем из пространства имен Q # в нашем файле Q #.</span><span class="sxs-lookup"><span data-stu-id="54c23-232">The Q# compiler works here by generating an equivalently named C# namespace from the Q# namespace in our Q# file.</span></span>
<span data-ttu-id="54c23-233">В дальнейшем он создает класс C# с эквивалентным именем для каждого из определенных вызываемых из Q # или типов.</span><span class="sxs-lookup"><span data-stu-id="54c23-233">It further generates an equivalently named C# class for each of the Q# callables or types defined therein.</span></span>

<span data-ttu-id="54c23-234">Во первых, мы делаем классы, используемые в нашей основной программе, доступными с `using` инструкциями, которые примерно аналогом на `open` инструкции в нашем файле Q #:</span><span class="sxs-lookup"><span data-stu-id="54c23-234">First, we make any classes used in our host program available with `using` statements, which are roughly analagous to the `open` statements in our Q# file:</span></span>

```csharp
using System;
using System.Threading.Tasks;
using Microsoft.Quantum.Simulation.Simulators;    // contains the target machines (e.g. QuantumSimulator, ResourcesEstimator)
using NamespaceName;                              // make the Q# namespace available
```

<span data-ttu-id="54c23-235">Далее мы объявляем пространство имен C#, несколько других битов и частей (см. полный блок кода ниже), а затем любое классическое программирование, которое нам бы хотелось (например, вычисление аргументов для вызываемых параметров Q #).</span><span class="sxs-lookup"><span data-stu-id="54c23-235">Next, we declare our C# namespace, a few other bits and pieces (see the full code block below), and then any classical programming we would like (e.g. computing arguments for the Q# callables).</span></span>
<span data-ttu-id="54c23-236">В нашем случае Последнее не требуется, но пример такого использования можно найти в [примере взаимодействия с .NET](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet).</span><span class="sxs-lookup"><span data-stu-id="54c23-236">The latter isn't necessary in our case, but an example of such usage can be found at the  [.NET interoperability sample](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet).</span></span>

#### <a name="target-machines"></a><span data-ttu-id="54c23-237">Целевые компьютеры</span><span class="sxs-lookup"><span data-stu-id="54c23-237">Target machines</span></span>

<span data-ttu-id="54c23-238">Вернемся к Q #, нам нужно создать экземпляр целевого компьютера, на котором будут выполняться наши операции.</span><span class="sxs-lookup"><span data-stu-id="54c23-238">Getting back to Q#, we must create an instance of whatever target machine we will execute our operations on.</span></span>

```csharp
            using var sim = new QuantumSimulator();
```

<span data-ttu-id="54c23-239">Использование других целевых компьютеров настолько просто, как создание экземпляра другого, хотя способ выполнения этих и обработки возвратов может немного отличаться.</span><span class="sxs-lookup"><span data-stu-id="54c23-239">Using other target machines is as simple as instantiating a different one, although the manner of doing so and processing the returns can be slightly different.</span></span>
<span data-ttu-id="54c23-240">Для краткости мы подносимся к [`QuantumSimulator`](xref:microsoft.quantum.machines.full-state-simulator) Now и включаем приведенный [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) [ниже](#including-the-resources-estimator).</span><span class="sxs-lookup"><span data-stu-id="54c23-240">For brevity, we stick to the [`QuantumSimulator`](xref:microsoft.quantum.machines.full-state-simulator) for now, and include the [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) [below](#including-the-resources-estimator).</span></span>

<span data-ttu-id="54c23-241">Каждый класс C#, созданный из операций Q #, имеет `Run` метод, первый аргумент которого должен быть экземпляром целевого компьютера.</span><span class="sxs-lookup"><span data-stu-id="54c23-241">Each C# class generated from the Q# operations have a `Run` method, the first argument of which must be the target machine instance.</span></span>
<span data-ttu-id="54c23-242">Итак, для запуска `MeasureSuperposition` в `QuantumSimulator` мы используем `MeasureSuperposition.Run(sim)` .</span><span class="sxs-lookup"><span data-stu-id="54c23-242">So, to run `MeasureSuperposition` on the `QuantumSimulator`, we use `MeasureSuperposition.Run(sim)`.</span></span>
<span data-ttu-id="54c23-243">Возвращаемые результаты могут быть назначены переменным в C#:</span><span class="sxs-lookup"><span data-stu-id="54c23-243">The returned results can then be assigned to variables in C#:</span></span>

```csharp
            var singleQubitResult = await MeasureSuperposition.Run(sim);
```

> [!NOTE]
> <span data-ttu-id="54c23-244">`Run`Метод выполняется асинхронно, так как это будет так для реального аппаратного оборудования, и поэтому `await` ключевое слово блокирует дальнейшее выполнение до завершения задачи.</span><span class="sxs-lookup"><span data-stu-id="54c23-244">The `Run` method is executed asynchronously because this will be the case for real quantum hardware, and therefore the `await` keyword blocks further execution until the task completes.</span></span>

<span data-ttu-id="54c23-245">Если вызываемый метод Q # не содержит возвращаемых значений (т. е. тип возвращаемого значения `Unit` ), то выполнение можно выполнять таким же образом, не назначая его переменной.</span><span class="sxs-lookup"><span data-stu-id="54c23-245">If the Q# callable does not have any returns (i.e. has return type `Unit`), then the execution can still be done in the same manner without assigning it to a variable.</span></span>
<span data-ttu-id="54c23-246">В этом случае вся строка будет просто состоять из</span><span class="sxs-lookup"><span data-stu-id="54c23-246">In that case, the entire line would simply consist of</span></span> 
```csharp
await <callable>.Run(<simulator>);
```

#### <a name="arguments"></a><span data-ttu-id="54c23-247">Аргументы</span><span class="sxs-lookup"><span data-stu-id="54c23-247">Arguments</span></span>

<span data-ttu-id="54c23-248">Все аргументы вызываемого аргумента Q # просто передаются как дополнительные аргументы, объект после на целевой компьютер.</span><span class="sxs-lookup"><span data-stu-id="54c23-248">Any arguments to the Q# callable are simply passed as additional arguments afer the target machine.</span></span>
<span data-ttu-id="54c23-249">Следовательно, результаты `MeasureSuperpositionArray` в `n=4` Кубитс будут выбирались через</span><span class="sxs-lookup"><span data-stu-id="54c23-249">Hence the results of `MeasureSuperpositionArray` on `n=4` qubits would fetched via</span></span> 

```csharp
            var multiQubitResult = await MeasureSuperpositionArray.Run(sim, 4);
```

<span data-ttu-id="54c23-250">Таким образом, полная управляющая программа C# может выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="54c23-250">A full C# host program could thus look like</span></span>

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

<span data-ttu-id="54c23-251">В расположении файла C# приложение может быть запущено из командной строки путем ввода</span><span class="sxs-lookup"><span data-stu-id="54c23-251">At the location of the C# file, the host program can be run from the command line by entering</span></span>
```dotnetcli
dotnet run
```
<span data-ttu-id="54c23-252">и в этом случае выходные данные будут записаны в консоль аналогично</span><span class="sxs-lookup"><span data-stu-id="54c23-252">and in this case you will see output written to the console similar to</span></span> 
```output
Single qubit result: One
Multiple qubit result: [One,One,Zero,Zero]
```

> [!NOTE]
> <span data-ttu-id="54c23-253">Из-за взаимодействия компилятора с пространствами имен можно было бы сделать так, чтобы вызываемые директивы Q # были доступны без `using NamespaceName;` оператора, и просто сопоставлять заголовок пространства имен C# с ним.</span><span class="sxs-lookup"><span data-stu-id="54c23-253">Due to the compiler's interoperability with namespaces, we could alternatively make our Q# callables available without the `using NamespaceName;` statement, and simply matching the C# namespace title to it.</span></span>
> <span data-ttu-id="54c23-254">Это происходит путем замены `namespace host` на `namespace NamespaceName` .</span><span class="sxs-lookup"><span data-stu-id="54c23-254">That is, by replacing `namespace host` with `namespace NamespaceName`.</span></span>

#### <a name="including-the-resources-estimator"></a><span data-ttu-id="54c23-255">Включение средства оценки ресурсов</span><span class="sxs-lookup"><span data-stu-id="54c23-255">Including the resources estimator</span></span>

<span data-ttu-id="54c23-256">[`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator)Для получения выходных данных требуется немного другая реализация.</span><span class="sxs-lookup"><span data-stu-id="54c23-256">The [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) requires a slightly different implementation to retrieve the output.</span></span>

<span data-ttu-id="54c23-257">Во-первых, вместо того, чтобы создавать экземпляры в качестве переменных с помощью `using` оператора (как мы делаем с `QuantumSimulator` ), мы более просто создаем экземпляры объектов класса с помощью</span><span class="sxs-lookup"><span data-stu-id="54c23-257">Firstly, instead of instantiating them as a variable with a `using` statement (as we do with the `QuantumSimulator`), we more directly instantiate objects of the class via</span></span>

```csharp
            var estimatorSingleQ = new ResourcesEstimator();
            var estimatorMultiQ = new ResourcesEstimator();
```

<span data-ttu-id="54c23-258">Обратите внимание, что вместо одного целевого симулятора, используемого несколькими операциями Q #, мы создали один экземпляр для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="54c23-258">Notice that instead of a single target simulator to be used by multiple Q# operations, we have instantiated one for each.</span></span> <span data-ttu-id="54c23-259">Это связано с тем, что сами объекты изменяются при использовании в качестве целевых компьютеров, после чего их результаты можно извлечь с помощью метода класса `.ToTSV()` .</span><span class="sxs-lookup"><span data-stu-id="54c23-259">This is because the objects themselves are modified when used as target machines, and their results can then be retrieved afterwards with the class method `.ToTSV()`.</span></span>

<span data-ttu-id="54c23-260">Чтобы выполнить операции с помощью оценщиков ресурсов, мы используем</span><span class="sxs-lookup"><span data-stu-id="54c23-260">To run the operations on the resource estimators, we use</span></span>

```csharp
            await MeasureSuperposition.Run(estimatorSingleQ);
            await MeasureSuperpositionArray.Run(estimatorMultiQ, 4);
```
<span data-ttu-id="54c23-261">а затем получить результаты в виде значений с разделителями-табуляциями (TSV) с помощью `estimatorSingleQ.ToTSV()` и `estimatorMultiQ.ToTSV()` .</span><span class="sxs-lookup"><span data-stu-id="54c23-261">and then fetch the results as tab-separated-values (TSV) with `estimatorSingleQ.ToTSV()` and `estimatorMultiQ.ToTSV()`.</span></span>

<span data-ttu-id="54c23-262">Таким образом, полная управляющая программа C#, `QuantumSimulator` которая использует и, и `ResourcesEstimator` может принимать форму:</span><span class="sxs-lookup"><span data-stu-id="54c23-262">So, a full C# host program making use of both the `QuantumSimulator` and `ResourcesEstimator` could take the form:</span></span>

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


<span data-ttu-id="54c23-263">что выдаст результат, аналогичный</span><span class="sxs-lookup"><span data-stu-id="54c23-263">which would yield output similar to</span></span>

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

## <a name="q-jupyter-notebooks"></a><span data-ttu-id="54c23-264">Записные книжки Jupyter Notebook для Q#</span><span class="sxs-lookup"><span data-stu-id="54c23-264">Q# Jupyter Notebooks</span></span>
<span data-ttu-id="54c23-265">Q # Jupyter записные книжки используют ядро IQ #, которое позволяет определять, компилировать и выполнять вызываемые вопросы в одной записной книжке---все вместе с инструкциями, примечаниями и другим содержимым.</span><span class="sxs-lookup"><span data-stu-id="54c23-265">Q# Jupyter Notebooks make use of the IQ# kernel, which allows you to define, compile, and run Q# callables in a single notebook---all alongside instructions, notes, and other content.</span></span>
<span data-ttu-id="54c23-266">Это означает, что хотя можно импортировать и использовать содержимое `*.qs` файлов Q #, они не являются обязательными в модели выполнения.</span><span class="sxs-lookup"><span data-stu-id="54c23-266">This means that while it is possible to import and use the contents of `*.qs` Q# files, they are not necessary in the execution model.</span></span>

<span data-ttu-id="54c23-267">Здесь мы подробно рассмотрим выполнение операций Q #, описанных выше, но более обширные общие сведения об использовании записных книжек Q # Jupyter приведены в статье [q # и Jupyter Notebooks](https://github.com/microsoft/Quantum/blob/master/samples/getting-started/intro-to-iqsharp/Notebook.ipynb).</span><span class="sxs-lookup"><span data-stu-id="54c23-267">Here, we will detail how to run the Q# operations defined above, but a more broad introduction to using Q# Jupyter Notebooks is provided at [Intro to Q# and Jupyter Notebooks](https://github.com/microsoft/Quantum/blob/master/samples/getting-started/intro-to-iqsharp/Notebook.ipynb).</span></span>

### <a name="defining-operations"></a><span data-ttu-id="54c23-268">Определение операций</span><span class="sxs-lookup"><span data-stu-id="54c23-268">Defining operations</span></span>

<span data-ttu-id="54c23-269">В Jupyter Notebook Q # вы вводите Q # Code точно так же, как в пространстве имен файла Q #.</span><span class="sxs-lookup"><span data-stu-id="54c23-269">In a Q# Jupyter Notebook, you enter Q# code just as we would from inside the namespace of a Q# file.</span></span>

<span data-ttu-id="54c23-270">Таким образом, можно обеспечить доступ к вызываемым функциям из [стандартных библиотек Q #](xref:microsoft.quantum.qsharplibintro) с помощью `open` операторов для соответствующих пространств имен.</span><span class="sxs-lookup"><span data-stu-id="54c23-270">So, we can enable access to callables from the [Q# standard libraries](xref:microsoft.quantum.qsharplibintro) with `open` statements for their respective namespaces.</span></span>
<span data-ttu-id="54c23-271">При выполнении ячейки с такой инструкцией определения из этих пространств имен доступны во всей рабочей области.</span><span class="sxs-lookup"><span data-stu-id="54c23-271">Upon running a cell with such a statement, the definitions from those namespaces are available throughout the workspace.</span></span>

> [!NOTE]
> <span data-ttu-id="54c23-272">Вызываемые из [Microsoft. тактов. внутренних](xref:microsoft.quantum.intrinsic) и [Microsoft. тактов. Canon](xref:microsoft.quantum.canon) (например [`H`](xref:microsoft.quantum.intrinsic.h) , и [`ApplyToEach`](xref:microsoft.quantum.canon.applytoeach) ) автоматически доступны для операций, определенных в ячейках в записных книжках Q # Jupyter.</span><span class="sxs-lookup"><span data-stu-id="54c23-272">Callables from [Microsoft.Quantum.Intrinsic](xref:microsoft.quantum.intrinsic) and [Microsoft.Quantum.Canon](xref:microsoft.quantum.canon) (e.g. [`H`](xref:microsoft.quantum.intrinsic.h) and [`ApplyToEach`](xref:microsoft.quantum.canon.applytoeach)) are automatically available to operations defined within cells in Q# Jupyter Notebooks.</span></span>
> <span data-ttu-id="54c23-273">Однако это не верно для кода, который помещается из внешних исходных файлов Q # (процесс, показанный в [Введение в Q # и Jupyter Notebooks](https://github.com/microsoft/Quantum/blob/master/samples/getting-started/intro-to-iqsharp/Notebook.ipynb)).</span><span class="sxs-lookup"><span data-stu-id="54c23-273">However, this is not true for code brought in from external Q# source files (a process shown at [Intro to Q# and Jupyter Notebooks](https://github.com/microsoft/Quantum/blob/master/samples/getting-started/intro-to-iqsharp/Notebook.ipynb)).</span></span> 
> 

<span data-ttu-id="54c23-274">Аналогично, для определения операций требуется только написание кода Q # и выполнение ячейки.</span><span class="sxs-lookup"><span data-stu-id="54c23-274">Similarly, defining operations requires only writing the Q# code and running the cell.</span></span>

<img src="../media/hostprograms_jupyter_op_def_crop.png" alt="Jupyter cell defining Q# operations" width="600">

<span data-ttu-id="54c23-275">Затем в выходных данных перечисляются операции, которые затем могут быть вызваны из будущих ячеек.</span><span class="sxs-lookup"><span data-stu-id="54c23-275">The output then lists those operations, which can then be called from future cells.</span></span>

### <a name="target-machines"></a><span data-ttu-id="54c23-276">Целевые компьютеры</span><span class="sxs-lookup"><span data-stu-id="54c23-276">Target machines</span></span>

<span data-ttu-id="54c23-277">Функциональные возможности выполнения операций на конкретных целевых компьютерах предоставляются с помощью [команд IQ # Magic](xref:microsoft.quantum.guide.quickref.iqsharp).</span><span class="sxs-lookup"><span data-stu-id="54c23-277">The functionality to run operations on specific target machines is provided via [IQ# Magic Commands](xref:microsoft.quantum.guide.quickref.iqsharp).</span></span>
<span data-ttu-id="54c23-278">Например, `%simulate` `QuantumSimulator` использует, и `%estimate` используется `ResourcesEstimator` :</span><span class="sxs-lookup"><span data-stu-id="54c23-278">For example, `%simulate` makes use of the `QuantumSimulator`, and `%estimate` uses the `ResourcesEstimator`:</span></span>

<img src="../media/hostprograms_jupyter_no_args_sim_est_crop.png" alt="Simulate and estimate resources Jupyter cell" width="500">

### <a name="passing-inputs-to-functions-and-operations"></a><span data-ttu-id="54c23-279">Передача входных данных в функции и операции</span><span class="sxs-lookup"><span data-stu-id="54c23-279">Passing inputs to functions and operations</span></span>

<span data-ttu-id="54c23-280">В настоящее время команды Magic Execution можно использовать только с операциями, не принимающими аргументов.</span><span class="sxs-lookup"><span data-stu-id="54c23-280">Currently the execution magic commands can only be used with operations that take no arguments.</span></span> <span data-ttu-id="54c23-281">Поэтому для запуска `MeasureSuperpositionArray` необходимо определить операцию "оболочки", которая затем вызывает операцию с аргументами:</span><span class="sxs-lookup"><span data-stu-id="54c23-281">So, to run `MeasureSuperpositionArray`, we need to define a "wrapper" operation which then calls the operation with the arguments:</span></span>

<img src="../media/hostprograms_jupyter_wrapper_def_sim_crop.png" alt="Wrapper function and simulate Jupyter cell" width="550">

<span data-ttu-id="54c23-282">Эту операцию можно использовать аналогично с `%estimate` и другими командами выполнения.</span><span class="sxs-lookup"><span data-stu-id="54c23-282">This operation can of course be used similarly with `%estimate` and other execution commands.</span></span>
