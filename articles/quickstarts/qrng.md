---
title: Создание квантового генератора случайных чисел
description: Создайте проект Q#, который демонстрирует фундаментальные квантовые понятия, например суперпозицию, на примере квантового генератора случайных чисел.
author: bromeg
ms.author: megbrow@microsoft.com
ms.date: 10/25/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.qrng
ms.openlocfilehash: 5a433606f08f4c6a4ab7b5df67a7f0c30d2b3f0d
ms.sourcegitcommit: db23885adb7ff76cbf8bd1160d401a4f0471e549
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/01/2020
ms.locfileid: "82683008"
---
# <a name="quickstart-implement-a-quantum-random-number-generator-in-q"></a><span data-ttu-id="2cc23-103">Краткое руководство. Реализация квантового генератора случайных чисел на языке Q\#</span><span class="sxs-lookup"><span data-stu-id="2cc23-103">Quickstart: Implement a Quantum Random Number Generator in Q\#</span></span>

<span data-ttu-id="2cc23-104">Простой пример квантового алгоритма на языке Q#, который моделирует генератор случайных чисел.</span><span class="sxs-lookup"><span data-stu-id="2cc23-104">A simple example of a quantum algorithm written in Q# is a quantum random number generator.</span></span> <span data-ttu-id="2cc23-105">Этот алгоритм использует природу квантовой механики для получения случайного числа.</span><span class="sxs-lookup"><span data-stu-id="2cc23-105">This algorithm leverages the nature of quantum mechanics to produce a random number.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2cc23-106">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="2cc23-106">Prerequisites</span></span>

- <span data-ttu-id="2cc23-107">[Microsoft Quantum Development Kit](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="2cc23-107">The Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).</span></span>
- [<span data-ttu-id="2cc23-108">Создание проекта Q#</span><span class="sxs-lookup"><span data-stu-id="2cc23-108">Create a Q# Project</span></span>](xref:microsoft.quantum.howto.createproject)

## <a name="write-a-q-operation"></a><span data-ttu-id="2cc23-109">Создание операции Q#</span><span class="sxs-lookup"><span data-stu-id="2cc23-109">Write a Q# operation</span></span>

### <a name="q-operation-code"></a><span data-ttu-id="2cc23-110">Код операции Q#</span><span class="sxs-lookup"><span data-stu-id="2cc23-110">Q# operation code</span></span>

1. <span data-ttu-id="2cc23-111">Замените содержимое файла Program.qs следующим кодом:</span><span class="sxs-lookup"><span data-stu-id="2cc23-111">Replace the contents of the Program.qs file with the following code:</span></span>

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="3-15,34":::

<span data-ttu-id="2cc23-112">Как упоминалось в статье [Сведения о квантовых вычислениях](xref:microsoft.quantum.overview.what), кубит представляет собой единицу квантовой информации и может находиться в состоянии суперпозиции.</span><span class="sxs-lookup"><span data-stu-id="2cc23-112">As mentioned in our [What is Quantum Computing?](xref:microsoft.quantum.overview.what) article, a qubit is a unit of quantum information that can be in superposition.</span></span> <span data-ttu-id="2cc23-113">При измерении он всегда возвращает значение 0 или 1.</span><span class="sxs-lookup"><span data-stu-id="2cc23-113">When measured, a qubit can only be either 0 or 1.</span></span> <span data-ttu-id="2cc23-114">Но во время выполнения состояние кубита отражает вероятность получить значение 0 или 1 при измерении.</span><span class="sxs-lookup"><span data-stu-id="2cc23-114">However, during execution the state of the qubit represents the probability of reading either a 0 or a 1 with a measurement.</span></span> <span data-ttu-id="2cc23-115">Такое вероятностное состояние называется суперпозицией.</span><span class="sxs-lookup"><span data-stu-id="2cc23-115">This probabilistic state is known as superposition.</span></span> <span data-ttu-id="2cc23-116">Эту вероятность мы можем применить для создания случайных чисел.</span><span class="sxs-lookup"><span data-stu-id="2cc23-116">We can use this probability to generate random numbers.</span></span>

<span data-ttu-id="2cc23-117">Мы создадим операцию Q#, в которой используется тип данных `Qubit`,уникальный для языка Q#.</span><span class="sxs-lookup"><span data-stu-id="2cc23-117">In our Q# operation, we introduce the `Qubit` datatype, native to Q#.</span></span> <span data-ttu-id="2cc23-118">`Qubit` можно выделить инструкцией `using`.</span><span class="sxs-lookup"><span data-stu-id="2cc23-118">We can only allocate a `Qubit` with a `using` statement.</span></span> <span data-ttu-id="2cc23-119">Только что выделенный кубит всегда находится в состоянии `Zero`.</span><span class="sxs-lookup"><span data-stu-id="2cc23-119">When it gets allocated, a qubit is always in the `Zero`  state.</span></span> 

<span data-ttu-id="2cc23-120">С помощью операции `H` мы можем перевести `Qubit` в состояние суперпозиции.</span><span class="sxs-lookup"><span data-stu-id="2cc23-120">Using the `H` operation, we are able to put our `Qubit` in superposition.</span></span> <span data-ttu-id="2cc23-121">Чтобы измерить кубит, т. е. определить его значение, используется специальная операция `M`.</span><span class="sxs-lookup"><span data-stu-id="2cc23-121">To measure a qubit and read its value, you use the `M` intrinsic operation.</span></span>

<span data-ttu-id="2cc23-122">Каждый раз, когда мы переводим `Qubit` в состояние суперпозиции и измеряем его, мы получаем разные значения.</span><span class="sxs-lookup"><span data-stu-id="2cc23-122">By putting our `Qubit` in superposition and measuring it, our result will be a different value each time the code is invoked.</span></span>

<span data-ttu-id="2cc23-123">При отмене выделения `Qubit` необходимо явным образом вернуть ему состояние `Zero`. В противном случае симулятор вернет ошибку при выполнении.</span><span class="sxs-lookup"><span data-stu-id="2cc23-123">When a `Qubit` is de-allocated it must be explicitly set back to the `Zero` state, otherwise the simulator will report a runtime error.</span></span> <span data-ttu-id="2cc23-124">Для этого проще всего вызвать `Reset`.</span><span class="sxs-lookup"><span data-stu-id="2cc23-124">An easy way to achieve this is invoking `Reset`.</span></span>

### <a name="visualizing-the-code-with-the-bloch-sphere"></a><span data-ttu-id="2cc23-125">Визуализация кода в формате сферы Блоха</span><span class="sxs-lookup"><span data-stu-id="2cc23-125">Visualizing the code with the Bloch sphere</span></span>

<span data-ttu-id="2cc23-126">В сфере Блоха северный полюс соответствует классическому значению **0**, а южный — классическому значению **1**.</span><span class="sxs-lookup"><span data-stu-id="2cc23-126">In the Bloch sphere, the north pole represents the classical value **0** and the south pole represents the classical value **1**.</span></span> <span data-ttu-id="2cc23-127">Любое состояние суперпозиции обозначается точкой на этой сфере (или стрелкой на схеме).</span><span class="sxs-lookup"><span data-stu-id="2cc23-127">Any superposition can be represented by a point on the sphere (represented by an arrow).</span></span> <span data-ttu-id="2cc23-128">Чем ближе конец этой стрелки к одному из полюсов, тем выше вероятность схлопывания этого кубита при измерении в то классическое состояние, которое соответствует этому полюсу.</span><span class="sxs-lookup"><span data-stu-id="2cc23-128">The closer the end of the arrow to a pole the higher the probability the qubit collapses into the classical value assigned to that pole when measured.</span></span> <span data-ttu-id="2cc23-129">В примере ниже красная стрелка обозначает состояние с более высокой вероятностью получить значение **0** при измерении кубита.</span><span class="sxs-lookup"><span data-stu-id="2cc23-129">For example, the qubit state represented by the red arrow below has a higher probability of giving the value **0** if we measure it.</span></span>

<img src="~/media/qrng-Bloch.png" width="175" alt="A qubit state with a high probability of measuring zero">

<span data-ttu-id="2cc23-130">Мы можем использовать это представление для визуализации работы нашего кода.</span><span class="sxs-lookup"><span data-stu-id="2cc23-130">We can use this representation to visualize what the code is doing:</span></span>

* <span data-ttu-id="2cc23-131">Для начала мы инициализируем кубит в состоянии **0** и применим `H`, чтобы создать состояние суперпозиции с равной вероятностью получить значения **0** и **1**.</span><span class="sxs-lookup"><span data-stu-id="2cc23-131">First we start with a qubit initialized in the state **0** and apply `H` to create a superposition in which the probabilities for **0** and **1** are the same.</span></span>

<img src="~/media/qrng-H.png" width="450" alt="Preparing a qubit in superposition">

* <span data-ttu-id="2cc23-132">Затем мы измерим состояние кубита и сохраним выходное значение:</span><span class="sxs-lookup"><span data-stu-id="2cc23-132">Then we measure the qubit and save the output:</span></span>

<img src="~/media/qrng-meas.png" width="450" alt="Measuring a qubit and saving the output">

<span data-ttu-id="2cc23-133">Так как исход этого измерения является полностью случайным, можно считать, что мы получили случайный бит.</span><span class="sxs-lookup"><span data-stu-id="2cc23-133">Since the outcome of the measurement is completely random, we have obtained a random bit.</span></span> <span data-ttu-id="2cc23-134">Вызывая эту операцию несколько раз, мы получим большое целое число.</span><span class="sxs-lookup"><span data-stu-id="2cc23-134">We can call this operation several times to create integers.</span></span> <span data-ttu-id="2cc23-135">Например, три вызова этой операции возвращают три случайных бита, позволяя создать трехбитовое число (т. е. случайное число в диапазоне от 0 до 7).</span><span class="sxs-lookup"><span data-stu-id="2cc23-135">For example, if we call the operation three times to obtain three random bits, we can build random 3-bit numbers (that is, a random number between 0 and 7).</span></span>


## <a name="creating-a-complete-random-number-generator"></a><span data-ttu-id="2cc23-136">Создание комплексного генератора случайных чисел</span><span class="sxs-lookup"><span data-stu-id="2cc23-136">Creating a complete random number generator</span></span>

<span data-ttu-id="2cc23-137">Теперь, когда у нас есть операция Q#, создающая случайные биты, мы можем использовать ее для создания комплексного квантового генератора случайных чисел.</span><span class="sxs-lookup"><span data-stu-id="2cc23-137">Now that we have a Q# operation that generates random bits, we can use it to build a complete quantum random number generator.</span></span> <span data-ttu-id="2cc23-138">Мы можем использовать приложения командной строки Q# или основную программу.</span><span class="sxs-lookup"><span data-stu-id="2cc23-138">We can use the Q# command line applications or use a host program.</span></span>



### <a name="q-command-line-applications-with-visual-studio-or-visual-studio-code"></a>[<span data-ttu-id="2cc23-139">Приложения командной строки Q# в Visual Studio или Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="2cc23-139">Q# command line applications with Visual Studio or Visual Studio Code</span></span>](#tab/tabid-qsharp)

<span data-ttu-id="2cc23-140">Чтобы создать полное приложение командной строки Q#, добавьте в программу Q# следующую точку входа:</span><span class="sxs-lookup"><span data-stu-id="2cc23-140">To create the full Q# command line application, add the following entry point to your Q# program:</span></span> 

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="17-33":::

<span data-ttu-id="2cc23-141">Исполняемый файл будет выполнять операцию или функцию, помеченную атрибутом `@EntryPoint()`, в симуляторе или оценщике ресурсов в зависимости от конфигурации проекта и параметров командной строки.</span><span class="sxs-lookup"><span data-stu-id="2cc23-141">The executable will run the operation or function marked with the `@EntryPoint()` attribute on a simulator or resource estimator, depending on the project configuration and command-line options.</span></span>

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="3-34":::

<span data-ttu-id="2cc23-142">В Visual Studio просто нажмите клавиши CTRL+F5, чтобы выполнить скрипт.</span><span class="sxs-lookup"><span data-stu-id="2cc23-142">In Visual Studio, simply press Ctrl + F5 to execute the script.</span></span>

<span data-ttu-id="2cc23-143">При первом выполнении в VS Code нужно создать файл Program.qs. Для этого введите следующую команду в окне терминала:</span><span class="sxs-lookup"><span data-stu-id="2cc23-143">In VS Code, build the Program.qs the first time by typing the below in the terminal:</span></span>

```dotnetcli
dotnet build
```

<span data-ttu-id="2cc23-144">Для последующих выполнений файл не нужно создавать повторно.</span><span class="sxs-lookup"><span data-stu-id="2cc23-144">For subsequent runs, there is no need to build it again.</span></span> <span data-ttu-id="2cc23-145">Для выполнения введите следующую команду и нажмите клавишу ВВОД:</span><span class="sxs-lookup"><span data-stu-id="2cc23-145">To run it, type the following command and press enter:</span></span>

```dotnetcli
dotnet run --no-build
```

### <a name="python-with-visual-studio-code-or-the-command-line"></a>[<span data-ttu-id="2cc23-146">Вызов Python из Visual Studio Code или командной строки</span><span class="sxs-lookup"><span data-stu-id="2cc23-146">Python with Visual Studio Code or the Command Line</span></span>](#tab/tabid-python)

<span data-ttu-id="2cc23-147">Чтобы выполнить эту программу Q# из кода Python, сохраните следующий код в файл `host.py`:</span><span class="sxs-lookup"><span data-stu-id="2cc23-147">To run your new Q# program from Python, save the following code as `host.py`:</span></span>

:::code language="python" source="~/quantum/samples/interoperability/qrng/host.py" range="11-30":::

<span data-ttu-id="2cc23-148">Теперь вы сможете запустить основную программу Python из командной строки следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2cc23-148">You can then run your Python host program from the command line:</span></span>

```bash
$ python host.py
Preparing Q# environment...
..The random number generated is 42
```

### <a name="c-with-visual-studio-code-or-visual-studio"></a>[<span data-ttu-id="2cc23-149">C# с Visual Studio Code или Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2cc23-149">C# with Visual Studio Code or Visual Studio</span></span>](#tab/tabid-csharp)

<span data-ttu-id="2cc23-150">Чтобы выполнить эту программу Q# из кода C#, измените `Driver.cs`, включив в него следующий код:</span><span class="sxs-lookup"><span data-stu-id="2cc23-150">To run your new Q# program from C#, modify `Driver.cs` to include the following C# code:</span></span>

:::code language="csharp" source="~/quantum/samples/interoperability/qrng/Host.cs" range="4-39":::

<span data-ttu-id="2cc23-151">Теперь вы сможете запустить основную программу C# из командной строки следующим образом (в Visual Studio можно нажать клавишу F5):</span><span class="sxs-lookup"><span data-stu-id="2cc23-151">You can then run your C# host program from the command line (in Visual Studio you should press F5):</span></span>

```bash
$ dotnet run
The random number generated is 42
```

***
