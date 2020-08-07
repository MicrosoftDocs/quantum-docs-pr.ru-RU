---
title: Простая классификация с помощью библиотеки тактов Машинное обучение
description: Узнайте, как выполнить последовательное классификатор, написанный на Q# основе машинное обучение библиотеки тактов Microsoft КДК.
author: geduardo
ms.author: v-edsanc@microsoft.com
ms.date: 02/16/2020
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.basics
no-loc:
- Q#
- $$v
ms.openlocfilehash: f9c3e7ab85c0f0d1a6063e593607d35c5cb76936
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868973"
---
# <a name="basic-classification-classify-data-with-the-qdk"></a><span data-ttu-id="b40d5-103">Простая классификация: классификация данных с помощью КДК</span><span class="sxs-lookup"><span data-stu-id="b40d5-103">Basic classification: Classify data with the QDK</span></span>

<span data-ttu-id="b40d5-104">В этом кратком руководстве вы узнаете, как выполнить последовательное классификатор, написанный на Q# основе машинное обучение библиотеки тактов для КДК.</span><span class="sxs-lookup"><span data-stu-id="b40d5-104">In this Quickstart, you will learn how to execute a quantum sequential classifier written in Q# using the Quantum Machine Learning library of the QDK.</span></span> 

<span data-ttu-id="b40d5-105">В этом пошаговом окне мы будем использовать набор данных половинной Луны, используя структуру-классификатор, определенную в Q# .</span><span class="sxs-lookup"><span data-stu-id="b40d5-105">In this guide we will use the half-moon dataset, using a classifier structure defined in Q#.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b40d5-106">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="b40d5-106">Prerequisites</span></span>

- <span data-ttu-id="b40d5-107">[Microsoft Quantum Development Kit](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="b40d5-107">The Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).</span></span>
- <span data-ttu-id="b40d5-108">Создайте Q# проект для [хост-программы Python](xref:microsoft.quantum.install.python) или [управляющей программы C#](xref:microsoft.quantum.install.cs).</span><span class="sxs-lookup"><span data-stu-id="b40d5-108">Create a Q# project for either a [Python host program](xref:microsoft.quantum.install.python) or a [C# host program](xref:microsoft.quantum.install.cs).</span></span>

## <a name="host-program"></a><span data-ttu-id="b40d5-109">Ведущее приложение</span><span class="sxs-lookup"><span data-stu-id="b40d5-109">Host program</span></span>

<span data-ttu-id="b40d5-110">Программа размещения состоит из трех частей:</span><span class="sxs-lookup"><span data-stu-id="b40d5-110">Your host program consists of three parts:</span></span>

- <span data-ttu-id="b40d5-111">Загрузите набор данных и выберите набор параметров запуска для модели.</span><span class="sxs-lookup"><span data-stu-id="b40d5-111">Load the dataset and choose a set of starting parameters for your model.</span></span>
- <span data-ttu-id="b40d5-112">Выполните обучение, чтобы определить параметры и сдвиг модели.</span><span class="sxs-lookup"><span data-stu-id="b40d5-112">Execute training to determine the parameters and bias of the model.</span></span>
- <span data-ttu-id="b40d5-113">Проверка модели для определения ее точности</span><span class="sxs-lookup"><span data-stu-id="b40d5-113">Validate the model to determine its accuracy</span></span>

    ### <a name="python-with-visual-studio-code-or-the-command-line"></a>[<span data-ttu-id="b40d5-114">Вызов Python из Visual Studio Code или командной строки</span><span class="sxs-lookup"><span data-stu-id="b40d5-114">Python with Visual Studio Code or the Command Line</span></span>](#tab/tabid-python)

    <span data-ttu-id="b40d5-115">Чтобы запустить вас в Q# качестве классификатора из Python, сохраните следующий код как `host.py` .</span><span class="sxs-lookup"><span data-stu-id="b40d5-115">To run your the Q# classifier from Python, save the following code as `host.py`.</span></span> <span data-ttu-id="b40d5-116">Помните, что вам также нужен Q# файл `Training.qs` , описанный далее в этом руководстве.</span><span class="sxs-lookup"><span data-stu-id="b40d5-116">Remember that you also need the Q# file `Training.qs` that is explained later in this tutorial.</span></span>

    :::code language="python" source="~/quantum/samples/machine-learning/half-moons/host.py" range="3-42":::

    <span data-ttu-id="b40d5-117">Теперь вы сможете запустить основную программу Python из командной строки следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b40d5-117">You can then run your Python host program from the command line:</span></span>

    ```bash
    $ python host.py
    Preparing Q# environment...
    [...]
    Observed X.XX% misclassifications.
    ```

    ### <a name="c-with-visual-studio-code-or-the-command-line"></a>[<span data-ttu-id="b40d5-118">Вызов C# из Visual Studio Code или командной строки</span><span class="sxs-lookup"><span data-stu-id="b40d5-118">C# with Visual Studio Code or the Command Line</span></span>](#tab/tabid-csharp)

    <span data-ttu-id="b40d5-119">Чтобы запустить вас в Q# качестве классификатора из C#, сохраните следующий код как `Host.cs` .</span><span class="sxs-lookup"><span data-stu-id="b40d5-119">To run your the Q# classifier from C#, save the following code as `Host.cs`.</span></span> <span data-ttu-id="b40d5-120">Помните, что вам также нужен Q# файл `Training.qs` , описанный далее в этом руководстве.</span><span class="sxs-lookup"><span data-stu-id="b40d5-120">Remember that you also need the Q# file `Training.qs` that is explained later in this tutorial.</span></span>

    :::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="4-86":::

    <span data-ttu-id="b40d5-121">Теперь вы сможете запустить основную программу C# из командной строки следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b40d5-121">You can then run your C# host program from the command line:</span></span>

    ```bash
    $ dotnet run
    [...]
    Observed X.XX% misclassifications.
    ```

    ### <a name="c-with-visual-studio-2019"></a>[<span data-ttu-id="b40d5-122">Вызов C# из Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="b40d5-122">C# with Visual Studio 2019</span></span>](#tab/tabid-vs2019)

    <span data-ttu-id="b40d5-123">Чтобы запустить новую Q# программу из c# в Visual Studio, измените `Host.cs` для включения следующего кода c#.</span><span class="sxs-lookup"><span data-stu-id="b40d5-123">To run your new Q# program from C# in Visual Studio, modify `Host.cs` to include the following C# code.</span></span> <span data-ttu-id="b40d5-124">Помните, что вам также нужен Q# файл `Training.qs` , описанный далее в этом руководстве.</span><span class="sxs-lookup"><span data-stu-id="b40d5-124">Remember that you also need the Q# file `Training.qs` that is explained later in this tutorial.</span></span>

    :::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="4-86":::

    <span data-ttu-id="b40d5-125">Затем нажмите клавишу F5, чтобы запустить программу. Вы увидите новое всплывающее окно со следующими результатами:</span><span class="sxs-lookup"><span data-stu-id="b40d5-125">Then press F5, the program will start execution and a new windows will pop-up with the following results:</span></span> 

    ```bash
    $ dotnet run
    [...]
    Observed X.XX% misclassifications.
    ```
    ***

## <a name="q-classifier-code"></a><span data-ttu-id="b40d5-126">\#Код классификатора Q</span><span class="sxs-lookup"><span data-stu-id="b40d5-126">Q\# classifier code</span></span>

<span data-ttu-id="b40d5-127">Теперь давайте посмотрим, как определяются операции, вызванные ведущим приложением Q# .</span><span class="sxs-lookup"><span data-stu-id="b40d5-127">Now let's see how the operations invoked by the host program are defined in Q#.</span></span>
<span data-ttu-id="b40d5-128">Мы сохраняем следующий код в файле с именем `Training.qs` .</span><span class="sxs-lookup"><span data-stu-id="b40d5-128">We save the following code in a file named `Training.qs`.</span></span>

:::code language="qsharp" source="~/quantum/samples/machine-learning/half-moons/Training.qs" range="4-116":::

<span data-ttu-id="b40d5-129">Наиболее важными функциями и операциями, определенными в приведенном выше коде, являются:</span><span class="sxs-lookup"><span data-stu-id="b40d5-129">The most important functions and operations defined in the code above are:</span></span>

- <span data-ttu-id="b40d5-130">`ClassifierStructure() : ControlledRotation[]`. в этой функции мы устанавливаем структуру модели канала, добавляя уровни контролируемого шлюза, который мы будем рассматривать.</span><span class="sxs-lookup"><span data-stu-id="b40d5-130">`ClassifierStructure() : ControlledRotation[]` : in this function we set the structure of our circuit model by adding the layers of the controlled gates we consider.</span></span> <span data-ttu-id="b40d5-131">Этот шаг аналогичен объявлению уровней нейронов в последовательной модели глубокого обучения.</span><span class="sxs-lookup"><span data-stu-id="b40d5-131">This step is analogous to the declaration of layers of neurons in a sequential deep learning model.</span></span>
- <span data-ttu-id="b40d5-132">`TrainHalfMoonModel() : (Double[], Double)`: Эта операция является основной частью кода и определяет обучение.</span><span class="sxs-lookup"><span data-stu-id="b40d5-132">`TrainHalfMoonModel() : (Double[], Double)` : this operation is the core part of the code and defines the training.</span></span> <span data-ttu-id="b40d5-133">Здесь мы загружаем образцы из набора данных, входящего в библиотеку, мы устанавливаем параметры Hyper и начальные параметры для обучения и начнем обучение, вызывая операцию, `TrainSequentialClassifier` входящую в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="b40d5-133">Here we load the samples from the dataset included in the library, we set the hyper parameters and the initial parameters for the training and we start the training by calling the operation `TrainSequentialClassifier` included in the library.</span></span> <span data-ttu-id="b40d5-134">Он выводит параметры и сдвиг, определяющие классификатор.</span><span class="sxs-lookup"><span data-stu-id="b40d5-134">It outputs the parameters and the bias that determine the classifier.</span></span>
- <span data-ttu-id="b40d5-135">`ValidateHalfMoonModel(parameters : Double[], bias : Double) : Int`: Эта операция определяет процесс проверки для оценки модели.</span><span class="sxs-lookup"><span data-stu-id="b40d5-135">`ValidateHalfMoonModel(parameters : Double[], bias : Double) : Int` : this operation defines the validation process to evaluate the model.</span></span> <span data-ttu-id="b40d5-136">Здесь мы загружаем примеры для проверки, количество измерений на выборку и допуск.</span><span class="sxs-lookup"><span data-stu-id="b40d5-136">Here we load the samples for validation, the number of measurements per sample and the tolerance.</span></span> <span data-ttu-id="b40d5-137">Он выводит количество неправильной классификации для выбранного пакета выборки для проверки.</span><span class="sxs-lookup"><span data-stu-id="b40d5-137">It outputs the number of misclassifications on the chosen batch of samples for validation.</span></span>

## <a name="next-steps"></a><span data-ttu-id="b40d5-138">Дальнейшие шаги</span><span class="sxs-lookup"><span data-stu-id="b40d5-138">Next steps</span></span>

<span data-ttu-id="b40d5-139">Во первых, вы можете поэкспериментировать с кодом и попробовать изменить некоторые параметры, чтобы увидеть, как он влияет на обучение.</span><span class="sxs-lookup"><span data-stu-id="b40d5-139">First, you can play with the code and try to change some parameters to see how it affects the training.</span></span> <span data-ttu-id="b40d5-140">Затем, в следующем руководстве, [Создайте свой собственный классификатор](xref:microsoft.quantum.libraries.machine-learning.design), вы узнаете, как определить структуру классификатора.</span><span class="sxs-lookup"><span data-stu-id="b40d5-140">Then, in the next tutorial, [Design your own classifier](xref:microsoft.quantum.libraries.machine-learning.design),  you will learn how to define the structure of the classifier.</span></span>
