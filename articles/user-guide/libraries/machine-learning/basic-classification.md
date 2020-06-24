---
title: Простая классификация с помощью библиотеки тактов Машинное обучение
description: 'Узнайте, как выполнить последовательное классификатор, написанный в Q # с помощью библиотеки Машинное обучениеа тактовой частоты для Microsoft КДК.'
author: geduardo
ms.author: v-edsanc@microsoft.com
ms.date: 02/16/2020
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.basics
ms.openlocfilehash: 1d2538fd164c4c61c2712978d3b5c57b0eb766e6
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275788"
---
# <a name="basic-classification-classify-data-with-the-qdk"></a><span data-ttu-id="c4c5c-103">Простая классификация: классификация данных с помощью КДК</span><span class="sxs-lookup"><span data-stu-id="c4c5c-103">Basic classification: Classify data with the QDK</span></span>

<span data-ttu-id="c4c5c-104">В этом кратком руководстве вы узнаете, как выполнить последовательное классификатор, написанный в Q #, используя Машинное обучение библиотеку тактовой частоты для КДК.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-104">In this Quickstart, you will learn how to execute a quantum sequential classifier written in Q# using the Quantum Machine Learning library of the QDK.</span></span> 

<span data-ttu-id="c4c5c-105">В этом пошаговом окне мы будем использовать набор данных половинной Луны, используя структуру классификатора, определенную в Q #.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-105">In this guide we will use the half-moon dataset, using a classifier structure defined in Q#.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c4c5c-106">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="c4c5c-106">Prerequisites</span></span>

- <span data-ttu-id="c4c5c-107">[Microsoft Quantum Development Kit](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="c4c5c-107">The Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).</span></span>
- <span data-ttu-id="c4c5c-108">Создайте проект Q # для [хост-программы Python](xref:microsoft.quantum.install.python) или [управляющей программы C#](xref:microsoft.quantum.install.cs).</span><span class="sxs-lookup"><span data-stu-id="c4c5c-108">Create a Q# project for either a [Python host program](xref:microsoft.quantum.install.python) or a [C# host program](xref:microsoft.quantum.install.cs).</span></span>

## <a name="host-program"></a><span data-ttu-id="c4c5c-109">Ведущее приложение</span><span class="sxs-lookup"><span data-stu-id="c4c5c-109">Host program</span></span>

<span data-ttu-id="c4c5c-110">Программа размещения состоит из трех частей:</span><span class="sxs-lookup"><span data-stu-id="c4c5c-110">Your host program consists of three parts:</span></span>

- <span data-ttu-id="c4c5c-111">Загрузите набор данных и выберите набор параметров запуска для модели.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-111">Load the dataset and choose a set of starting parameters for your model.</span></span>
- <span data-ttu-id="c4c5c-112">Выполните обучение, чтобы определить параметры и сдвиг модели.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-112">Execute training to determine the parameters and bias of the model.</span></span>
- <span data-ttu-id="c4c5c-113">Проверка модели для определения ее точности</span><span class="sxs-lookup"><span data-stu-id="c4c5c-113">Validate the model to determine its accuracy</span></span>

    ### <a name="python-with-visual-studio-code-or-the-command-line"></a>[<span data-ttu-id="c4c5c-114">Вызов Python из Visual Studio Code или командной строки</span><span class="sxs-lookup"><span data-stu-id="c4c5c-114">Python with Visual Studio Code or the Command Line</span></span>](#tab/tabid-python)

    <span data-ttu-id="c4c5c-115">Чтобы запустить из Python классификатор Q #, сохраните следующий код как `host.py` .</span><span class="sxs-lookup"><span data-stu-id="c4c5c-115">To run your the Q# classifier from Python, save the following code as `host.py`.</span></span> <span data-ttu-id="c4c5c-116">Помните, что вам также нужен файл Q # `Training.qs` , описанный далее в этом руководстве.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-116">Remember that you also need the Q# file `Training.qs` that is explained later in this tutorial.</span></span>

    :::code language="python" source="~/quantum/samples/machine-learning/half-moons/host.py" range="3-42":::

    <span data-ttu-id="c4c5c-117">Теперь вы сможете запустить основную программу Python из командной строки следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c4c5c-117">You can then run your Python host program from the command line:</span></span>

    ```bash
    $ python host.py
    Preparing Q# environment...
    [...]
    Observed X.XX% misclassifications.
    ```

    ### <a name="c-with-visual-studio-code-or-the-command-line"></a>[<span data-ttu-id="c4c5c-118">Вызов C# из Visual Studio Code или командной строки</span><span class="sxs-lookup"><span data-stu-id="c4c5c-118">C# with Visual Studio Code or the Command Line</span></span>](#tab/tabid-csharp)

    <span data-ttu-id="c4c5c-119">Чтобы запустить вас в качестве классификатора Q # из C#, сохраните следующий код как `Host.cs` .</span><span class="sxs-lookup"><span data-stu-id="c4c5c-119">To run your the Q# classifier from C#, save the following code as `Host.cs`.</span></span> <span data-ttu-id="c4c5c-120">Помните, что вам также нужен файл Q # `Training.qs` , описанный далее в этом руководстве.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-120">Remember that you also need the Q# file `Training.qs` that is explained later in this tutorial.</span></span>

    :::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="4-86":::

    <span data-ttu-id="c4c5c-121">Теперь вы сможете запустить основную программу C# из командной строки следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c4c5c-121">You can then run your C# host program from the command line:</span></span>

    ```bash
    $ dotnet run
    [...]
    Observed X.XX% misclassifications.
    ```

    ### <a name="c-with-visual-studio-2019"></a>[<span data-ttu-id="c4c5c-122">Вызов C# из Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="c4c5c-122">C# with Visual Studio 2019</span></span>](#tab/tabid-vs2019)

    <span data-ttu-id="c4c5c-123">Чтобы запустить новую программу Q # из C# в Visual Studio, измените `Host.cs` для включения следующего кода c#.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-123">To run your new Q# program from C# in Visual Studio, modify `Host.cs` to include the following C# code.</span></span> <span data-ttu-id="c4c5c-124">Помните, что вам также нужен файл Q # `Training.qs` , описанный далее в этом руководстве.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-124">Remember that you also need the Q# file `Training.qs` that is explained later in this tutorial.</span></span>

    :::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="4-86":::

    <span data-ttu-id="c4c5c-125">Затем нажмите клавишу F5, чтобы запустить программу. Вы увидите новое всплывающее окно со следующими результатами:</span><span class="sxs-lookup"><span data-stu-id="c4c5c-125">Then press F5, the program will start execution and a new windows will pop-up with the following results:</span></span> 

    ```bash
    $ dotnet run
    [...]
    Observed X.XX% misclassifications.
    ```
    ***

## <a name="q-classifier-code"></a><span data-ttu-id="c4c5c-126">\#Код классификатора Q</span><span class="sxs-lookup"><span data-stu-id="c4c5c-126">Q\# classifier code</span></span>

<span data-ttu-id="c4c5c-127">Теперь давайте посмотрим, как операции, вызываемые ведущим приложением, определяются в Q #.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-127">Now let's see how the operations invoked by the host program are defined in Q#.</span></span>
<span data-ttu-id="c4c5c-128">Мы сохраняем следующий код в файле с именем `Training.qs` .</span><span class="sxs-lookup"><span data-stu-id="c4c5c-128">We save the following code in a file named `Training.qs`.</span></span>

:::code language="qsharp" source="~/quantum/samples/machine-learning/half-moons/Training.qs" range="4-116":::

<span data-ttu-id="c4c5c-129">Наиболее важными функциями и операциями, определенными в приведенном выше коде, являются:</span><span class="sxs-lookup"><span data-stu-id="c4c5c-129">The most important functions and operations defined in the code above are:</span></span>

- <span data-ttu-id="c4c5c-130">`ClassifierStructure() : ControlledRotation[]`. в этой функции мы устанавливаем структуру модели канала, добавляя уровни контролируемого шлюза, который мы будем рассматривать.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-130">`ClassifierStructure() : ControlledRotation[]` : in this function we set the structure of our circuit model by adding the layers of the controlled gates we consider.</span></span> <span data-ttu-id="c4c5c-131">Этот шаг аналогичен объявлению уровней нейронов в последовательной модели глубокого обучения.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-131">This step is analogous to the declaration of layers of neurons in a sequential deep learning model.</span></span>
- <span data-ttu-id="c4c5c-132">`TrainHalfMoonModel() : (Double[], Double)`: Эта операция является основной частью кода и определяет обучение.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-132">`TrainHalfMoonModel() : (Double[], Double)` : this operation is the core part of the code and defines the training.</span></span> <span data-ttu-id="c4c5c-133">Здесь мы загружаем образцы из набора данных, входящего в библиотеку, мы устанавливаем параметры Hyper и начальные параметры для обучения и начнем обучение, вызывая операцию, `TrainSequentialClassifier` входящую в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-133">Here we load the samples from the dataset included in the library, we set the hyper parameters and the initial parameters for the training and we start the training by calling the operation `TrainSequentialClassifier` included in the library.</span></span> <span data-ttu-id="c4c5c-134">Он выводит параметры и сдвиг, определяющие классификатор.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-134">It outputs the parameters and the bias that determine the classifier.</span></span>
- <span data-ttu-id="c4c5c-135">`ValidateHalfMoonModel(parameters : Double[], bias : Double) : Int`: Эта операция определяет процесс проверки для оценки модели.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-135">`ValidateHalfMoonModel(parameters : Double[], bias : Double) : Int` : this operation defines the validation process to evaluate the model.</span></span> <span data-ttu-id="c4c5c-136">Здесь мы загружаем примеры для проверки, количество измерений на выборку и допуск.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-136">Here we load the samples for validation, the number of measurements per sample and the tolerance.</span></span> <span data-ttu-id="c4c5c-137">Он выводит количество неправильной классификации для выбранного пакета выборки для проверки.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-137">It outputs the number of misclassifications on the chosen batch of samples for validation.</span></span>

## <a name="next-steps"></a><span data-ttu-id="c4c5c-138">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="c4c5c-138">Next steps</span></span>

<span data-ttu-id="c4c5c-139">Во первых, вы можете поэкспериментировать с кодом и попробовать изменить некоторые параметры, чтобы увидеть, как он влияет на обучение.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-139">First, you can play with the code and try to change some parameters to see how it affects the training.</span></span> <span data-ttu-id="c4c5c-140">Затем, в следующем руководстве, [Создайте свой собственный классификатор](xref:microsoft.quantum.libraries.machine-learning.design), вы узнаете, как определить структуру классификатора.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-140">Then, in the next tutorial, [Design your own classifier](xref:microsoft.quantum.libraries.machine-learning.design),  you will learn how to define the structure of the classifier.</span></span>
