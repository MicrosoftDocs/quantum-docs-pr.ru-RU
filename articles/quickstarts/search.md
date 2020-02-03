---
title: Выполнение алгоритма поиска Гровер на Q# (Quantum Development Kit)
description: Создайте проект Q# с демонстрацией алгоритма Гровера, одного из самых известных квантовых алгоритмов.
author: cgranade
ms.author: chgranad@microsoft.com
ms.date: 10/19/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.search
ms.openlocfilehash: c1fd578fdb3d56a7b48972e6ccc9b1605047fe36
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820357"
---
# <a name="quickstart-implement-grovers-search-algorithm-in-q"></a><span data-ttu-id="69404-103">Краткое руководство. Реализация поиска по алгоритму Гровера на Q#</span><span class="sxs-lookup"><span data-stu-id="69404-103">Quickstart: Implement Grover's search algorithm in Q#</span></span>

<span data-ttu-id="69404-104">В этом кратком руководстве описано, как создать и применить алгоритм Гровера, который ускоряет поиск по неструктурированным данным.</span><span class="sxs-lookup"><span data-stu-id="69404-104">In this Quickstart, you can learn how to build and run Grover search to speed up the search of unstructured data.</span></span>  <span data-ttu-id="69404-105">Алгоритм Гровера считается одним из самых известных алгоритмов квантовых вычислений. Эта несложная реализация на Q# познакомит вас с преимуществами систем квантовых вычислений, в которых квантовые алгоритмы выражаются на высокоуровневых языках типа Q#.</span><span class="sxs-lookup"><span data-stu-id="69404-105">Grover's search is one of the most popular quantum computing algorithms, and this relatively small Q# implementation gives you a sense of some of the advantages of programming quantum solutions with a high-level Q# quantum programming language to express quantum algorithms.</span></span>  <span data-ttu-id="69404-106">В конце работы с этим руководством вы увидите, что ваша модель обнаруживает нужную строку в неупорядоченном списке записей намного быстрее, чем потребуется для полного просмотра списка на классическом компьютере.</span><span class="sxs-lookup"><span data-stu-id="69404-106">At the end of the guide, you will see the simulation output demonstrates successfully finding a specific string among a list of onordered entries in a fraction of the time it would take to search the whole list on a classical computer.</span></span>

<span data-ttu-id="69404-107">Алгоритм Гровера ищет конкретные элементы в неструктурированном списке данных.</span><span class="sxs-lookup"><span data-stu-id="69404-107">Grover's algorithm searches a list of unstructured data for specific items.</span></span> <span data-ttu-id="69404-108">Например, он позволяет ответить на следующие вопросы: Является ли карта, извлеченная наугад из колоды, тузом червей?</span><span class="sxs-lookup"><span data-stu-id="69404-108">For example, it can answer the question: Is this card drawn from a pack of cards an ace of hearts?</span></span> <span data-ttu-id="69404-109">Добавление меток для конкретного элемента называется _разметкой входных данных_.</span><span class="sxs-lookup"><span data-stu-id="69404-109">The labeling of the specific item is called _marked input_.</span></span>

<span data-ttu-id="69404-110">По алгоритму поиска Гровера квантовый компьютер гарантированно потратит меньше шагов на такой поиск, чем количество элементов в просматриваемом списке, что невозможно гарантировать ни одним классическим алгоритмом.</span><span class="sxs-lookup"><span data-stu-id="69404-110">Using Grover's search algorithm, a quantum computer is guaranteed to run this search in fewer steps than the number of items in the list that you're searching — something no classical algorithm can do.</span></span> <span data-ttu-id="69404-111">На одной колоде карт увеличение скорости пренебрежимо мало, но для списков с миллионами или миллиардами элементов разница становится значимой.</span><span class="sxs-lookup"><span data-stu-id="69404-111">The increased speed in the case of a pack of cards is negligible; however, in lists containing millions or billions of items, it becomes significant.</span></span>

<span data-ttu-id="69404-112">Алгоритм поиска Гровера можно реализовать всего в нескольких строках кода.</span><span class="sxs-lookup"><span data-stu-id="69404-112">You can build Grover's search algorithm with just a few lines of code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="69404-113">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="69404-113">Prerequisites</span></span>

- <span data-ttu-id="69404-114">[Microsoft Quantum Development Kit][install].</span><span class="sxs-lookup"><span data-stu-id="69404-114">The Microsoft [Quantum Development Kit][install].</span></span>

## <a name="what-does-grovers-search-algorithm-do"></a><span data-ttu-id="69404-115">Что же делает алгоритм поиска Гровера?</span><span class="sxs-lookup"><span data-stu-id="69404-115">What does Grover's search algorithm do?</span></span>

<span data-ttu-id="69404-116">Алгоритм Гровера проверяет, является ли элемент списка искомым элементом.</span><span class="sxs-lookup"><span data-stu-id="69404-116">Grover's algorithm asks whether an item in a list is the one we are searching for.</span></span> <span data-ttu-id="69404-117">Для этого он создает квантовую суперпозицию индексов списка, где каждый коэффициент (амплитуда вероятности) соответствует вероятности того, что этот индекс является искомым элементом.</span><span class="sxs-lookup"><span data-stu-id="69404-117">It does this by constructing a quantum superposition of the indexes of the list with each coefficient, or probability amplitude, representing the probability of that specific index being the one you are looking for.</span></span>

<span data-ttu-id="69404-118">В основе алгоритма лежат два шага, которые постепенно увеличивают коэффициент индекса, пока амплитуда вероятности этого коэффициента не достигнет единицы.</span><span class="sxs-lookup"><span data-stu-id="69404-118">At the heart of the algorithm are two steps that incrementally boost the coefficient of the index that we are looking for, until the probability amplitude of that coefficient approaches one.</span></span>

<span data-ttu-id="69404-119">Число добавочных увеличений заведомо меньше числа элементов в списке.</span><span class="sxs-lookup"><span data-stu-id="69404-119">The number of incremental boosts is fewer than the number of items in the list.</span></span> <span data-ttu-id="69404-120">Поэтому алгоритм поиска Гровера выполняет поиск за меньшее количество шагов, чем любой классический алгоритм.</span><span class="sxs-lookup"><span data-stu-id="69404-120">This is why Grover's search algorithm performs the search in fewer steps than any classical algorithm.</span></span>

![Функциональная схема для алгоритма поиска Гровера](~/media/grover.png)

## <a name="write-the-code"></a><span data-ttu-id="69404-122">Написание кода</span><span class="sxs-lookup"><span data-stu-id="69404-122">Write the code</span></span>

1. <span data-ttu-id="69404-123">Используя Quantum Development Kit, [создайте новый проект Q#](xref:microsoft.quantum.howto.createproject) с именем `Grover` в любой удобной среде разработки.</span><span class="sxs-lookup"><span data-stu-id="69404-123">Using the Quantum Development Kit, [create a new Q# project](xref:microsoft.quantum.howto.createproject) called `Grover`, in your development environment of choice.</span></span>

1. <span data-ttu-id="69404-124">В файл `Operations.qs` этого проекта добавьте следующий код:</span><span class="sxs-lookup"><span data-stu-id="69404-124">Add the following code to the `Operations.qs` file in your new project:</span></span>

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/SimpleGrover.qs" range="4-23" highlight="5,27":::

1. <span data-ttu-id="69404-125">Чтобы определить список, в котором выполняется поиск, создайте новый файл `Reflections.qs` и вставьте в него следующий код:</span><span class="sxs-lookup"><span data-stu-id="69404-125">To define the list that we're searching, create a new file `Reflections.qs`, and paste in the following code:</span></span>

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/Reflections.qs" range="4-70":::

    <span data-ttu-id="69404-126">Операция `ReflectAboutMarked` определяет помеченные входные данные, которые вы ищете: строка с чередованием нулей и единиц.</span><span class="sxs-lookup"><span data-stu-id="69404-126">The `ReflectAboutMarked` operation defines the marked input that you are searching for: the string of alternating zeros and ones.</span></span> <span data-ttu-id="69404-127">В этом примере помеченные входные данные жестко прописаны в коде, но вы можете дополнить пример поиском других входных данных или обобщить для поиска любых входных данных.</span><span class="sxs-lookup"><span data-stu-id="69404-127">This sample hard-codes the marked input, and can be extended to search for different inputs or generalized for any input.</span></span>

1. <span data-ttu-id="69404-128">Теперь запустите эту программу Q#, чтобы найти элемент с меткой `ReflectAboutMarked`.</span><span class="sxs-lookup"><span data-stu-id="69404-128">Next, run your new Q# program to find the item marked by `ReflectAboutMarked`.</span></span>

    ### <a name="python-with-visual-studio-code-or-the-command-linetabtabid-python"></a>[<span data-ttu-id="69404-129">Вызов Python из Visual Studio Code или командной строки</span><span class="sxs-lookup"><span data-stu-id="69404-129">Python with Visual Studio Code or the Command Line</span></span>](#tab/tabid-python)

    <span data-ttu-id="69404-130">Чтобы выполнить эту программу Q# из кода Python, сохраните следующий код в файл `host.py`:</span><span class="sxs-lookup"><span data-stu-id="69404-130">To run your new Q# program from Python, save the following code as `host.py`:</span></span>

    :::code language="python" source="~/quantum/samples/algorithms/simple-grover/host.py" range="9-14":::

    <span data-ttu-id="69404-131">Теперь вы сможете запустить основную программу Python из командной строки следующим образом:</span><span class="sxs-lookup"><span data-stu-id="69404-131">You can then run your Python host program from the command line:</span></span>

    ```bash
    $ python host.py
    Preparing Q# environment...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    [0, 1, 0, 1, 0]
    ```

    ### <a name="c-with-visual-studio-code-or-the-command-linetabtabid-csharp"></a>[<span data-ttu-id="69404-132">Вызов C# из Visual Studio Code или командной строки</span><span class="sxs-lookup"><span data-stu-id="69404-132">C# with Visual Studio Code or the Command Line</span></span>](#tab/tabid-csharp)

    <span data-ttu-id="69404-133">Чтобы выполнить эту программу Q# из кода C#, измените `Driver.cs`, включив в него следующий код:</span><span class="sxs-lookup"><span data-stu-id="69404-133">To run your new Q# program from C#, modify `Driver.cs` to include the following C# code:</span></span>

    :::code language="csharp" source="~/quantum/samples/algorithms/simple-grover/Host.cs" range="4-23":::

    <span data-ttu-id="69404-134">Теперь вы сможете запустить основную программу C# из командной строки следующим образом:</span><span class="sxs-lookup"><span data-stu-id="69404-134">You can then run your C# host program from the command line:</span></span>

    ```bash
    $ dotnet run
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Result: [Zero,One,Zero,One,Zero]

    Press any key to continue...
    ```

    ### <a name="c-with-visual-studio-2019tabtabid-vs2019"></a>[<span data-ttu-id="69404-135">Вызов C# из Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="69404-135">C# with Visual Studio 2019</span></span>](#tab/tabid-vs2019)

    <span data-ttu-id="69404-136">Чтобы выполнить эту программу Q# из кода C# в Visual Studio, измените `Driver.cs`, включив в него следующий код:</span><span class="sxs-lookup"><span data-stu-id="69404-136">To run your new Q# program from C# in Visual Studio, modify `Driver.cs` to include the following C# code:</span></span>

    :::code language="csharp" source="~/quantum/samples/algorithms/simple-grover/Host.cs" range="4-23":::

    <span data-ttu-id="69404-137">Затем нажмите клавишу F5, чтобы запустить программу. Вы увидите новое всплывающее окно со следующими результатами:</span><span class="sxs-lookup"><span data-stu-id="69404-137">Then press F5, the program will start execution and a new windows will pop-up with the following results:</span></span> 

    ```bash
    $ dotnet run
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Result: [Zero,One,Zero,One,Zero]

    Press any key to continue...
    ```
    ***

    <span data-ttu-id="69404-138">Операция `ReflectAboutMarked` была вызвана только четыре раза, но программа на Q# смогла найти входные данные 01010 из $2^{5} = 32$ возможных вариантов!</span><span class="sxs-lookup"><span data-stu-id="69404-138">The `ReflectAboutMarked` operation is called only four times, but your Q# program was able to find the "01010" input amongst $2^{5} = 32$ possible inputs!</span></span>

## <a name="next-steps"></a><span data-ttu-id="69404-139">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="69404-139">Next steps</span></span>

<span data-ttu-id="69404-140">Если вам понравилось это краткое руководство, воспользуйтесь перечисленными ниже ресурсами, чтобы изучить другие варианты применения Q# для собственных квантовых приложений.</span><span class="sxs-lookup"><span data-stu-id="69404-140">If you enjoyed this quickstart, check out some of the resources below to learn more about how you can use Q# to write your own quantum applications:</span></span>

- [<span data-ttu-id="69404-141">Вернуться руководству по началу работы с QDK</span><span class="sxs-lookup"><span data-stu-id="69404-141">Back to the Getting Started with QDK guide</span></span>](xref:microsoft.quantum.welcome)
- <span data-ttu-id="69404-142">Попробуйте изучить более общий алгоритм поиска Гровера из [этого примера](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/database-search).</span><span class="sxs-lookup"><span data-stu-id="69404-142">Try a more general Grover's search algorithm [sample](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/database-search)</span></span>
- [<span data-ttu-id="69404-143">Более подробное знакомство с алгоритмом поиска Гровера в Quantum Katas</span><span class="sxs-lookup"><span data-stu-id="69404-143">Learn more about Grover's search with the Quantum Katas</span></span>](xref:microsoft.quantum.overview.katas)
- <span data-ttu-id="69404-144">См. сведения о методике [усиления амплитуды](xref:microsoft.quantum.libraries.standard.algorithms#amplitude-amplification) в квантовых вычислениях, на которой основан алгоритм поиска Гровера.</span><span class="sxs-lookup"><span data-stu-id="69404-144">Read more about [Amplitude amplification](xref:microsoft.quantum.libraries.standard.algorithms#amplitude-amplification), the quantum computing technique behind Grover's search algorithm</span></span>
- [<span data-ttu-id="69404-145">Концепции квантовых вычислений</span><span class="sxs-lookup"><span data-stu-id="69404-145">Quantum computing concepts</span></span>](xref:microsoft.quantum.concepts.intro)
- [<span data-ttu-id="69404-146">Примеры для Quantum Development Kit</span><span class="sxs-lookup"><span data-stu-id="69404-146">Quantum Development Kit Samples</span></span>](https://docs.microsoft.com/samples/browse/?products=qdk)

<!-- LINKS -->

[install]: xref:microsoft.quantum.install
