---
title: Простая классификация с помощью библиотеки тактов Машинное обучение
description: 'Узнайте, как выполнить последовательное классификатор, написанный в Q # с помощью библиотеки Машинное обучениеа тактовой частоты для Microsoft КДК.'
author: geduardo
ms.author: v-edsanc@microsoft.com
ms.date: 02/16/2020
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.basics
ms.openlocfilehash: f42e3e4492f934d7a8f03d4fec6fa0de765401d7
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/28/2020
ms.locfileid: "77909931"
---
# <a name="basic-classification-classify-data-with-the-qdk"></a><span data-ttu-id="b6784-103">Простая классификация: классификация данных с помощью КДК</span><span class="sxs-lookup"><span data-stu-id="b6784-103">Basic classification: Classify data with the QDK</span></span>

<span data-ttu-id="b6784-104">В этом кратком руководстве вы узнаете, как выполнить последовательное классификатор, написанный в Q #, используя Машинное обучение библиотеку тактовой частоты для КДК.</span><span class="sxs-lookup"><span data-stu-id="b6784-104">In this Quickstart, you will learn how to execute a quantum sequential classifier written in Q# using the Quantum Machine Learning library of the QDK.</span></span> 

<span data-ttu-id="b6784-105">В этом пошаговом окне мы будем использовать набор данных половинной Луны, используя структуру классификатора, определенную в Q #.</span><span class="sxs-lookup"><span data-stu-id="b6784-105">In this guide we will use the half-moon dataset, using a classifier structure defined in Q#.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b6784-106">предварительные требования</span><span class="sxs-lookup"><span data-stu-id="b6784-106">Prerequisites</span></span>

- <span data-ttu-id="b6784-107">[Microsoft Quantum Development Kit](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="b6784-107">The Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).</span></span>
- [<span data-ttu-id="b6784-108">Создание проекта Q#</span><span class="sxs-lookup"><span data-stu-id="b6784-108">Create a Q# Project</span></span>](xref:microsoft.quantum.howto.createproject)

## <a name="host-program"></a><span data-ttu-id="b6784-109">Ведущее приложение</span><span class="sxs-lookup"><span data-stu-id="b6784-109">Host program</span></span>

<span data-ttu-id="b6784-110">Программа размещения состоит из трех частей:</span><span class="sxs-lookup"><span data-stu-id="b6784-110">Your host program consists of three parts:</span></span>

- <span data-ttu-id="b6784-111">Загрузите набор данных и выберите набор параметров запуска для модели.</span><span class="sxs-lookup"><span data-stu-id="b6784-111">Load the dataset and choose a set of starting parameters for your model.</span></span>
- <span data-ttu-id="b6784-112">Выполните обучение, чтобы определить параметры и сдвиг модели.</span><span class="sxs-lookup"><span data-stu-id="b6784-112">Execute training to determine the parameters and bias of the model.</span></span>
- <span data-ttu-id="b6784-113">Проверка модели для определения ее точности</span><span class="sxs-lookup"><span data-stu-id="b6784-113">Validate the model to determine its accuracy</span></span>

    ### <a name="python-with-visual-studio-code-or-the-command-line"></a>[<span data-ttu-id="b6784-114">Вызов Python из Visual Studio Code или командной строки</span><span class="sxs-lookup"><span data-stu-id="b6784-114">Python with Visual Studio Code or the Command Line</span></span>](#tab/tabid-python)

    <span data-ttu-id="b6784-115">Чтобы запустить из Python классификатор Q #, сохраните следующий код как `host.py`.</span><span class="sxs-lookup"><span data-stu-id="b6784-115">To run your the Q# classifier from Python, save the following code as `host.py`.</span></span> <span data-ttu-id="b6784-116">Помните, что вам также потребуется файл Q # `Training.qs`, который объясняется далее в этом руководстве.</span><span class="sxs-lookup"><span data-stu-id="b6784-116">Remember that you also need the Q# file `Training.qs` that is explained later in this tutorial.</span></span>

    :::code language="python" source="~/quantum/samples/machine-learning/half-moons/host.py" range="3-42":::

    <span data-ttu-id="b6784-117">Теперь вы сможете запустить основную программу Python из командной строки следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b6784-117">You can then run your Python host program from the command line:</span></span>

    ```bash
    $ python host.py
    Preparing Q# environment...
    [...]
    Observed X.XX% misclassifications.
    ```

    ### <a name="c-with-visual-studio-code-or-the-command-line"></a>[<span data-ttu-id="b6784-118">Вызов C# из Visual Studio Code или командной строки</span><span class="sxs-lookup"><span data-stu-id="b6784-118">C# with Visual Studio Code or the Command Line</span></span>](#tab/tabid-csharp)

    <span data-ttu-id="b6784-119">Чтобы запустить, что вы являетесь классификатором Q # C#из, сохраните следующий код как `Host.cs`.</span><span class="sxs-lookup"><span data-stu-id="b6784-119">To run your the Q# classifier from C#, save the following code as `Host.cs`.</span></span> <span data-ttu-id="b6784-120">Помните, что вам также потребуется файл Q # `Training.qs`, который объясняется далее в этом руководстве.</span><span class="sxs-lookup"><span data-stu-id="b6784-120">Remember that you also need the Q# file `Training.qs` that is explained later in this tutorial.</span></span>

    :::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="4-86":::

    <span data-ttu-id="b6784-121">Теперь вы сможете запустить основную программу C# из командной строки следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b6784-121">You can then run your C# host program from the command line:</span></span>

    ```bash
    $ dotnet run
    [...]
    Observed X.XX% misclassifications.
    ```

    ### <a name="c-with-visual-studio-2019"></a>[<span data-ttu-id="b6784-122">Вызов C# из Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="b6784-122">C# with Visual Studio 2019</span></span>](#tab/tabid-vs2019)

    <span data-ttu-id="b6784-123">Чтобы запустить новую программу Q # из C# в Visual Studio, измените `Host.cs`, включив в него следующий C# код.</span><span class="sxs-lookup"><span data-stu-id="b6784-123">To run your new Q# program from C# in Visual Studio, modify `Host.cs` to include the following C# code.</span></span> <span data-ttu-id="b6784-124">Помните, что вам также потребуется файл Q # `Training.qs`, который объясняется далее в этом руководстве.</span><span class="sxs-lookup"><span data-stu-id="b6784-124">Remember that you also need the Q# file `Training.qs` that is explained later in this tutorial.</span></span>

    :::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="4-86":::

    <span data-ttu-id="b6784-125">Затем нажмите клавишу F5, чтобы запустить программу. Вы увидите новое всплывающее окно со следующими результатами:</span><span class="sxs-lookup"><span data-stu-id="b6784-125">Then press F5, the program will start execution and a new windows will pop-up with the following results:</span></span> 

    ```bash
    $ dotnet run
    [...]
    Observed X.XX% misclassifications.
    ```
    ***

## <a name="q-classifier-code"></a><span data-ttu-id="b6784-126">Q\# код классификатора</span><span class="sxs-lookup"><span data-stu-id="b6784-126">Q\# classifier code</span></span>

<span data-ttu-id="b6784-127">Теперь давайте посмотрим, как операции, вызываемые ведущим приложением, определяются в Q #.</span><span class="sxs-lookup"><span data-stu-id="b6784-127">Now let's see how the operations invoked by the host program are defined in Q#.</span></span>
<span data-ttu-id="b6784-128">Мы сохраняем следующий код в файле с именем `Training.qs`.</span><span class="sxs-lookup"><span data-stu-id="b6784-128">We save the following code in a file named `Training.qs`.</span></span>

:::code language="qsharp" source="~/quantum/samples/machine-learning/half-moons/Training.qs" range="4-116":::

<span data-ttu-id="b6784-129">Наиболее важными функциями и операциями, определенными в приведенном выше коде, являются:</span><span class="sxs-lookup"><span data-stu-id="b6784-129">The most important functions and operations defined in the code above are:</span></span>

- <span data-ttu-id="b6784-130">`ClassifierStructure() : ControlledRotation[]`. в этой функции мы устанавливаем структуру модели канала, добавляя уровни контролируемого шлюза, который мы будем рассматривать.</span><span class="sxs-lookup"><span data-stu-id="b6784-130">`ClassifierStructure() : ControlledRotation[]` : in this function we set the structure of our circuit model by adding the layers of the controlled gates we consider.</span></span> <span data-ttu-id="b6784-131">Этот шаг аналогичен объявлению уровней нейронов в последовательной модели глубокого обучения.</span><span class="sxs-lookup"><span data-stu-id="b6784-131">This step is analogous to the declaration of layers of neurons in a sequential deep learning model.</span></span>
- <span data-ttu-id="b6784-132">`TrainHalfMoonModel() : TrainWineModel() : (Double[], Double)`: Эта операция является основной частью кода и определяет обучение.</span><span class="sxs-lookup"><span data-stu-id="b6784-132">`TrainHalfMoonModel() : TrainWineModel() : (Double[], Double)` : this operation is the core part of the code and defines the training.</span></span> <span data-ttu-id="b6784-133">Здесь мы загружаем образцы из набора данных, входящего в библиотеку, мы устанавливаем параметры Hyper и начальные параметры для обучения, а также начнем обучение, вызвав операцию `TrainSequentialClassifier`, которая включена в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="b6784-133">Here we load the samples from the dataset included in the library, we set the hyper parameters and the initial parameters for the training and we start the training by calling the operation `TrainSequentialClassifier` included in the library.</span></span> <span data-ttu-id="b6784-134">Он выводит параметры и сдвиг, определяющие классификатор.</span><span class="sxs-lookup"><span data-stu-id="b6784-134">It outputs the parameters and the bias that determine the classifier.</span></span>
- <span data-ttu-id="b6784-135">`ValidateHalfMoonModel(parameters : Double[], bias : Double) : Int`: Эта операция определяет процесс проверки для оценки модели.</span><span class="sxs-lookup"><span data-stu-id="b6784-135">`ValidateHalfMoonModel(parameters : Double[], bias : Double) : Int` : this operation defines the validation process to evaluate the model.</span></span> <span data-ttu-id="b6784-136">Здесь мы загружаем примеры для проверки, количество измерений на выборку и допуск.</span><span class="sxs-lookup"><span data-stu-id="b6784-136">Here we load the samples for validation, the number of measurements per sample and the tolerance.</span></span> <span data-ttu-id="b6784-137">Он выводит количество неправильной классификации для выбранного пакета выборки для проверки.</span><span class="sxs-lookup"><span data-stu-id="b6784-137">It outputs the number of misclassifications on the chosen batch of samples for validation.</span></span>

## <a name="next-steps"></a><span data-ttu-id="b6784-138">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="b6784-138">Next steps</span></span>

<span data-ttu-id="b6784-139">Во первых, вы можете поэкспериментировать с кодом и попробовать изменить некоторые параметры, чтобы увидеть, как он влияет на обучение.</span><span class="sxs-lookup"><span data-stu-id="b6784-139">First, you can play with the code and try to change some parameters to see how it affects the training.</span></span> <span data-ttu-id="b6784-140">Затем, в следующем руководстве, [Создайте свой собственный классификатор](xref:microsoft.quantum.libraries.machine-learning.design), вы узнаете, как определить структуру классификатора.</span><span class="sxs-lookup"><span data-stu-id="b6784-140">Then, in the next tutorial, [Design your own classifier](xref:microsoft.quantum.libraries.machine-learning.design),  you will learn how to define the structure of the classifier.</span></span>