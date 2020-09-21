---
title: Создание квантового генератора случайных чисел
description: Создайте Q# проект, демонстрирующий фундаментальные понятия о такте, такие как "геоположение", создав генератор тактов случайных чисел.
author: bromeg
ms.author: megbrow
ms.date: 10/25/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.qrng
no-loc:
- Q#
- $$v
ms.openlocfilehash: a0e8933e6a77d017db914e4bb969ea05f760a443
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834046"
---
# <a name="tutorial-implement-a-quantum-random-number-generator-in-q"></a><span data-ttu-id="710dd-103">Руководство по Реализация квантового генератора случайных чисел на языке Q\#</span><span class="sxs-lookup"><span data-stu-id="710dd-103">Tutorial: Implement a Quantum Random Number Generator in Q\#</span></span>

<span data-ttu-id="710dd-104">Простым примером алгоритма такта, написанного на Q# , является генератор тактовых случайных чисел.</span><span class="sxs-lookup"><span data-stu-id="710dd-104">A simple example of a quantum algorithm written in Q# is a quantum random number generator.</span></span> <span data-ttu-id="710dd-105">Этот алгоритм использует природу квантовой механики для получения случайного числа.</span><span class="sxs-lookup"><span data-stu-id="710dd-105">This algorithm leverages the nature of quantum mechanics to produce a random number.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="710dd-106">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="710dd-106">Prerequisites</span></span>

- <span data-ttu-id="710dd-107">[Microsoft Quantum Development Kit](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="710dd-107">The Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).</span></span>
- <span data-ttu-id="710dd-108">Создайте Q# проект для [ Q# приложения](xref:microsoft.quantum.install.standalone), с [ведущим приложением Python](xref:microsoft.quantum.install.python)или [ведущим приложением C#](xref:microsoft.quantum.install.cs).</span><span class="sxs-lookup"><span data-stu-id="710dd-108">Create a Q# project for either a [Q# application](xref:microsoft.quantum.install.standalone), with a [Python host program](xref:microsoft.quantum.install.python), or a [C# host program](xref:microsoft.quantum.install.cs).</span></span>

## <a name="write-a-no-locq-operation"></a><span data-ttu-id="710dd-109">Запись Q# операции</span><span class="sxs-lookup"><span data-stu-id="710dd-109">Write a Q# operation</span></span>

### <a name="no-locq-operation-code"></a><span data-ttu-id="710dd-110">Q# код операции</span><span class="sxs-lookup"><span data-stu-id="710dd-110">Q# operation code</span></span>

1. <span data-ttu-id="710dd-111">Замените содержимое файла Program.qs следующим кодом:</span><span class="sxs-lookup"><span data-stu-id="710dd-111">Replace the contents of the Program.qs file with the following code:</span></span>

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="3-15,34":::

<span data-ttu-id="710dd-112">Как упоминалось в статье [Основные сведения о квантовых вычислениях](xref:microsoft.quantum.overview.understanding), кубит представляет собой единицу квантовой информации и может находиться в состоянии суперпозиции.</span><span class="sxs-lookup"><span data-stu-id="710dd-112">As mentioned in our [Understanding quantum computing](xref:microsoft.quantum.overview.understanding) article, a qubit is a unit of quantum information that can be in superposition.</span></span> <span data-ttu-id="710dd-113">При измерении он всегда возвращает значение 0 или 1.</span><span class="sxs-lookup"><span data-stu-id="710dd-113">When measured, a qubit can only be either 0 or 1.</span></span> <span data-ttu-id="710dd-114">Однако при выполнении операции состояние кубит представляет вероятность считывания 0 или 1 с измерением.</span><span class="sxs-lookup"><span data-stu-id="710dd-114">However, when an operation is running, the state of the qubit represents the probability of reading either a 0 or a 1 with a measurement.</span></span> <span data-ttu-id="710dd-115">Такое вероятностное состояние называется суперпозицией.</span><span class="sxs-lookup"><span data-stu-id="710dd-115">This probabilistic state is known as superposition.</span></span> <span data-ttu-id="710dd-116">Эту вероятность мы можем применить для создания случайных чисел.</span><span class="sxs-lookup"><span data-stu-id="710dd-116">We can use this probability to generate random numbers.</span></span>

<span data-ttu-id="710dd-117">В нашей Q# операции мы представляем `Qubit` тип данных Native в Q# .</span><span class="sxs-lookup"><span data-stu-id="710dd-117">In our Q# operation, we introduce the `Qubit` datatype, native to Q#.</span></span> <span data-ttu-id="710dd-118">`Qubit` можно выделить инструкцией `using`.</span><span class="sxs-lookup"><span data-stu-id="710dd-118">We can only allocate a `Qubit` with a `using` statement.</span></span> <span data-ttu-id="710dd-119">Только что выделенный кубит всегда находится в состоянии `Zero`.</span><span class="sxs-lookup"><span data-stu-id="710dd-119">When it gets allocated, a qubit is always in the `Zero`  state.</span></span> 

<span data-ttu-id="710dd-120">С помощью операции `H` мы можем перевести `Qubit` в состояние суперпозиции.</span><span class="sxs-lookup"><span data-stu-id="710dd-120">Using the `H` operation, we are able to put our `Qubit` in superposition.</span></span> <span data-ttu-id="710dd-121">Чтобы измерить кубит, т. е. определить его значение, используется специальная операция `M`.</span><span class="sxs-lookup"><span data-stu-id="710dd-121">To measure a qubit and read its value, you use the `M` intrinsic operation.</span></span>

<span data-ttu-id="710dd-122">Каждый раз, когда мы переводим `Qubit` в состояние суперпозиции и измеряем его, мы получаем разные значения.</span><span class="sxs-lookup"><span data-stu-id="710dd-122">By putting our `Qubit` in superposition and measuring it, our result will be a different value each time the code is invoked.</span></span>

<span data-ttu-id="710dd-123">При отмене выделения `Qubit` необходимо явным образом вернуть ему состояние `Zero`. В противном случае симулятор вернет ошибку при выполнении.</span><span class="sxs-lookup"><span data-stu-id="710dd-123">When a `Qubit` is deallocated it must be explicitly set back to the `Zero` state, otherwise the simulator will report a runtime error.</span></span> <span data-ttu-id="710dd-124">Для этого проще всего вызвать `Reset`.</span><span class="sxs-lookup"><span data-stu-id="710dd-124">An easy way to achieve this is invoking `Reset`.</span></span>

### <a name="visualizing-the-code-with-the-bloch-sphere"></a><span data-ttu-id="710dd-125">Визуализация кода в формате сферы Блоха</span><span class="sxs-lookup"><span data-stu-id="710dd-125">Visualizing the code with the Bloch sphere</span></span>

<span data-ttu-id="710dd-126">В сфере Блоха северный полюс соответствует классическому значению **0**, а южный — классическому значению **1**.</span><span class="sxs-lookup"><span data-stu-id="710dd-126">In the Bloch sphere, the north pole represents the classical value **0** and the south pole represents the classical value **1**.</span></span> <span data-ttu-id="710dd-127">Любое состояние суперпозиции обозначается точкой на этой сфере (или стрелкой на схеме).</span><span class="sxs-lookup"><span data-stu-id="710dd-127">Any superposition can be represented by a point on the sphere (represented by an arrow).</span></span> <span data-ttu-id="710dd-128">Чем ближе конец этой стрелки к одному из полюсов, тем выше вероятность схлопывания этого кубита при измерении в то классическое состояние, которое соответствует этому полюсу.</span><span class="sxs-lookup"><span data-stu-id="710dd-128">The closer the end of the arrow to a pole the higher the probability the qubit collapses into the classical value assigned to that pole when measured.</span></span> <span data-ttu-id="710dd-129">В примере ниже красная стрелка обозначает состояние с более высокой вероятностью получить значение **0** при измерении кубита.</span><span class="sxs-lookup"><span data-stu-id="710dd-129">For example, the qubit state represented by the red arrow below has a higher probability of giving the value **0** if we measure it.</span></span>

<img src="~/media/qrng-Bloch.png" width="175" alt="A qubit state with a high probability of measuring zero">

<span data-ttu-id="710dd-130">Мы можем использовать это представление для визуализации работы нашего кода.</span><span class="sxs-lookup"><span data-stu-id="710dd-130">We can use this representation to visualize what the code is doing:</span></span>

* <span data-ttu-id="710dd-131">Для начала мы инициализируем кубит в состоянии **0** и применим `H`, чтобы создать состояние суперпозиции с равной вероятностью получить значения **0** и **1**.</span><span class="sxs-lookup"><span data-stu-id="710dd-131">First we start with a qubit initialized in the state **0** and apply `H` to create a superposition in which the probabilities for **0** and **1** are the same.</span></span>

<img src="~/media/qrng-H.png" width="450" alt="Preparing a qubit in superposition">

* <span data-ttu-id="710dd-132">Затем мы измерим состояние кубита и сохраним выходное значение:</span><span class="sxs-lookup"><span data-stu-id="710dd-132">Then we measure the qubit and save the output:</span></span>

<img src="~/media/qrng-meas.png" width="450" alt="Measuring a qubit and saving the output">

<span data-ttu-id="710dd-133">Так как исход этого измерения является полностью случайным, можно считать, что мы получили случайный бит.</span><span class="sxs-lookup"><span data-stu-id="710dd-133">Since the outcome of the measurement is completely random, we have obtained a random bit.</span></span> <span data-ttu-id="710dd-134">Вызывая эту операцию несколько раз, мы получим большое целое число.</span><span class="sxs-lookup"><span data-stu-id="710dd-134">We can call this operation several times to create integers.</span></span> <span data-ttu-id="710dd-135">Например, три вызова этой операции возвращают три случайных бита, позволяя создать трехбитовое число (т. е. случайное число в диапазоне от 0 до 7).</span><span class="sxs-lookup"><span data-stu-id="710dd-135">For example, if we call the operation three times to obtain three random bits, we can build random 3-bit numbers (that is, a random number between 0 and 7).</span></span>


## <a name="creating-a-complete-random-number-generator"></a><span data-ttu-id="710dd-136">Создание комплексного генератора случайных чисел</span><span class="sxs-lookup"><span data-stu-id="710dd-136">Creating a complete random number generator</span></span>

<span data-ttu-id="710dd-137">Теперь, когда у нас есть Q# операция, создающая случайные биты, мы можем использовать ее для создания полноценного генератора случайных чисел такта.</span><span class="sxs-lookup"><span data-stu-id="710dd-137">Now that we have a Q# operation that generates random bits, we can use it to build a complete quantum random number generator.</span></span> <span data-ttu-id="710dd-138">Мы можем использовать Q# приложение или использовать управляющую программу.</span><span class="sxs-lookup"><span data-stu-id="710dd-138">We can use a Q# application or use a host program.</span></span>



### <a name="no-locq-applications-with-visual-studio-or-visual-studio-code"></a>[<span data-ttu-id="710dd-139">Q# приложения с Visual Studio или Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="710dd-139">Q# applications with Visual Studio or Visual Studio Code</span></span>](#tab/tabid-qsharp)

<span data-ttu-id="710dd-140">Чтобы создать полное Q# приложение, добавьте в программу следующую точку входа Q# :</span><span class="sxs-lookup"><span data-stu-id="710dd-140">To create the full Q# application, add the following entry point to your Q# program:</span></span> 

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="17-33":::

<span data-ttu-id="710dd-141">Программа запустит операцию или функцию, помеченную `@EntryPoint()` атрибутом для симулятора или оценщика ресурсов, в зависимости от конфигурации проекта и параметров командной строки.</span><span class="sxs-lookup"><span data-stu-id="710dd-141">The program will run the operation or function marked with the `@EntryPoint()` attribute on a simulator or resource estimator, depending on the project configuration and command-line options.</span></span>

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="3-34":::

<span data-ttu-id="710dd-142">В Visual Studio просто нажмите клавиши CTRL + F5, чтобы запустить сценарий.</span><span class="sxs-lookup"><span data-stu-id="710dd-142">In Visual Studio, simply press Ctrl + F5 to run the script.</span></span>

<span data-ttu-id="710dd-143">При первом выполнении в VS Code нужно создать файл Program.qs. Для этого введите следующую команду в окне терминала:</span><span class="sxs-lookup"><span data-stu-id="710dd-143">In VS Code, build the Program.qs the first time by typing the below in the terminal:</span></span>

```dotnetcli
dotnet build
```

<span data-ttu-id="710dd-144">Для последующих выполнений файл не нужно создавать повторно.</span><span class="sxs-lookup"><span data-stu-id="710dd-144">For subsequent runs, there is no need to build it again.</span></span> <span data-ttu-id="710dd-145">Для выполнения введите следующую команду и нажмите клавишу ВВОД:</span><span class="sxs-lookup"><span data-stu-id="710dd-145">To run it, type the following command and press enter:</span></span>

```dotnetcli
dotnet run --no-build
```

### <a name="python-with-visual-studio-code-or-the-command-prompt"></a>[<span data-ttu-id="710dd-146">Python с Visual Studio Code или из командной строки</span><span class="sxs-lookup"><span data-stu-id="710dd-146">Python with Visual Studio Code or the command prompt</span></span>](#tab/tabid-python)

<span data-ttu-id="710dd-147">Чтобы запустить новую Q# программу из Python, сохраните следующий код `host.py` :</span><span class="sxs-lookup"><span data-stu-id="710dd-147">To run your new Q# program from Python, save the following code as `host.py`:</span></span>

:::code language="python" source="~/quantum/samples/interoperability/qrng/host.py" range="11-30":::

<span data-ttu-id="710dd-148">Затем можно запустить ведущее приложение Python из командной строки:</span><span class="sxs-lookup"><span data-stu-id="710dd-148">You can then run your Python host program from the command prompt:</span></span>

```bash
$ python host.py
Preparing Q# environment...
..The random number generated is 42
```

### <a name="c-with-visual-studio-code-or-visual-studio"></a>[<span data-ttu-id="710dd-149">C# с Visual Studio Code или Visual Studio</span><span class="sxs-lookup"><span data-stu-id="710dd-149">C# with Visual Studio Code or Visual Studio</span></span>](#tab/tabid-csharp)

<span data-ttu-id="710dd-150">Чтобы запустить новую Q# программу из c#, измените, `Driver.cs` включив в нее следующий код c#:</span><span class="sxs-lookup"><span data-stu-id="710dd-150">To run your new Q# program from C#, modify `Driver.cs` to include the following C# code:</span></span>

:::code language="csharp" source="~/quantum/samples/interoperability/qrng/Host.cs" range="4-39":::

<span data-ttu-id="710dd-151">Затем можно запустить ведущее приложение C# из командной строки (в Visual Studio следует нажать клавишу F5):</span><span class="sxs-lookup"><span data-stu-id="710dd-151">You can then run your C# host program from the command prompt (in Visual Studio you should press F5):</span></span>

```bash
$ dotnet run
The random number generated is 42
```

***
