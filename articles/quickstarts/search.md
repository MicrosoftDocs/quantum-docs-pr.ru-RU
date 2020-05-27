---
title: Выполнение алгоритма поиска Гровер на Q# (Quantum Development Kit)
description: Создайте проект Q# с демонстрацией алгоритма Гровера, одного из самых известных квантовых алгоритмов.
author: cgranade
ms.author: chgranad@microsoft.com
ms.date: 10/19/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.search
ms.openlocfilehash: 9562e1937a2cac49d682cc0524d8fb29e276d95c
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2020
ms.locfileid: "83426809"
---
# <a name="tutorial-implement-grovers-search-algorithm-in-q"></a><span data-ttu-id="aa446-103">Руководство по Реализация поиска по алгоритму Гровера на Q\#</span><span class="sxs-lookup"><span data-stu-id="aa446-103">Tutorial: Implement Grover's search algorithm in Q\#</span></span>

<span data-ttu-id="aa446-104">В этом руководстве объясняется, как создать и применить алгоритм Гровера, который ускоряет поиск по неструктурированным данным.</span><span class="sxs-lookup"><span data-stu-id="aa446-104">In this tutorial, you can learn how to build and run Grover search to speed up the search of unstructured data.</span></span>  <span data-ttu-id="aa446-105">Алгоритм Гровера считается одним из самых известных алгоритмов квантовых вычислений. Эта несложная реализация на Q# познакомит вас с преимуществами систем квантовых вычислений, в которых квантовые алгоритмы выражаются на высокоуровневых языках типа Q#.</span><span class="sxs-lookup"><span data-stu-id="aa446-105">Grover's search is one of the most popular quantum computing algorithms, and this relatively small Q# implementation gives you a sense of some of the advantages of programming quantum solutions with a high-level Q# quantum programming language to express quantum algorithms.</span></span>  <span data-ttu-id="aa446-106">В конце работы с этим руководством вы увидите, что ваша модель обнаруживает нужную строку в неупорядоченном списке записей намного быстрее, чем потребуется для полного просмотра списка на классическом компьютере.</span><span class="sxs-lookup"><span data-stu-id="aa446-106">At the end of the guide, you will see the simulation output demonstrates successfully finding a specific string among a list of unordered entries in a fraction of the time it would take to search the whole list on a classical computer.</span></span>

<span data-ttu-id="aa446-107">Алгоритм Гровера ищет конкретные элементы в неструктурированном списке данных.</span><span class="sxs-lookup"><span data-stu-id="aa446-107">Grover's algorithm searches a list of unstructured data for specific items.</span></span> <span data-ttu-id="aa446-108">Например, он позволяет ответить на следующие вопросы: Является ли карта, извлеченная наугад из колоды, тузом червей?</span><span class="sxs-lookup"><span data-stu-id="aa446-108">For example, it can answer the question: Is this card drawn from a pack of cards an ace of hearts?</span></span> <span data-ttu-id="aa446-109">Добавление меток для конкретного элемента называется _разметкой входных данных_.</span><span class="sxs-lookup"><span data-stu-id="aa446-109">The labeling of the specific item is called _marked input_.</span></span>

<span data-ttu-id="aa446-110">По алгоритму поиска Гровера квантовый компьютер гарантированно потратит меньше шагов на такой поиск, чем количество элементов в просматриваемом списке, что невозможно гарантировать ни одним классическим алгоритмом.</span><span class="sxs-lookup"><span data-stu-id="aa446-110">Using Grover's search algorithm, a quantum computer is guaranteed to run this search in fewer steps than the number of items in the list that you're searching — something no classical algorithm can do.</span></span> <span data-ttu-id="aa446-111">На одной колоде карт увеличение скорости пренебрежимо мало, но для списков с миллионами или миллиардами элементов разница становится значимой.</span><span class="sxs-lookup"><span data-stu-id="aa446-111">The increased speed in the case of a pack of cards is negligible; however, in lists containing millions or billions of items, it becomes significant.</span></span>

<span data-ttu-id="aa446-112">Алгоритм поиска Гровера можно реализовать всего в нескольких строках кода.</span><span class="sxs-lookup"><span data-stu-id="aa446-112">You can build Grover's search algorithm with just a few lines of code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="aa446-113">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="aa446-113">Prerequisites</span></span>

- <span data-ttu-id="aa446-114">[Microsoft Quantum Development Kit][install].</span><span class="sxs-lookup"><span data-stu-id="aa446-114">The Microsoft [Quantum Development Kit][install].</span></span>

## <a name="what-does-grovers-search-algorithm-do"></a><span data-ttu-id="aa446-115">Что же делает алгоритм поиска Гровера?</span><span class="sxs-lookup"><span data-stu-id="aa446-115">What does Grover's search algorithm do?</span></span>

<span data-ttu-id="aa446-116">Алгоритм Гровера проверяет, является ли элемент списка искомым элементом.</span><span class="sxs-lookup"><span data-stu-id="aa446-116">Grover's algorithm asks whether an item in a list is the one we are searching for.</span></span> <span data-ttu-id="aa446-117">Для этого он создает квантовую суперпозицию индексов списка, где каждый коэффициент (амплитуда вероятности) соответствует вероятности того, что этот индекс является искомым элементом.</span><span class="sxs-lookup"><span data-stu-id="aa446-117">It does this by constructing a quantum superposition of the indexes of the list with each coefficient, or probability amplitude, representing the probability of that specific index being the one you are looking for.</span></span>

<span data-ttu-id="aa446-118">В основе алгоритма лежат два шага, которые постепенно увеличивают коэффициент индекса, пока амплитуда вероятности этого коэффициента не достигнет единицы.</span><span class="sxs-lookup"><span data-stu-id="aa446-118">At the heart of the algorithm are two steps that incrementally boost the coefficient of the index that we are looking for, until the probability amplitude of that coefficient approaches one.</span></span>

<span data-ttu-id="aa446-119">Число добавочных увеличений заведомо меньше числа элементов в списке.</span><span class="sxs-lookup"><span data-stu-id="aa446-119">The number of incremental boosts is fewer than the number of items in the list.</span></span> <span data-ttu-id="aa446-120">Поэтому алгоритм поиска Гровера выполняет поиск за меньшее количество шагов, чем любой классический алгоритм.</span><span class="sxs-lookup"><span data-stu-id="aa446-120">This is why Grover's search algorithm performs the search in fewer steps than any classical algorithm.</span></span>

![Функциональная схема для алгоритма поиска Гровера](~/media/grover.png)

## <a name="write-the-code"></a><span data-ttu-id="aa446-122">Написание кода</span><span class="sxs-lookup"><span data-stu-id="aa446-122">Write the code</span></span>

1. <span data-ttu-id="aa446-123">Используя Quantum Development Kit, [создайте новый проект Q#](xref:microsoft.quantum.howto.createproject) с именем `Grover` в любой удобной среде разработки.</span><span class="sxs-lookup"><span data-stu-id="aa446-123">Using the Quantum Development Kit, [create a new Q# project](xref:microsoft.quantum.howto.createproject) called `Grover`, in your development environment of choice.</span></span>

1. <span data-ttu-id="aa446-124">В файл `Program.qs` этого проекта добавьте следующий код:</span><span class="sxs-lookup"><span data-stu-id="aa446-124">Add the following code to the `Program.qs` file in your new project:</span></span>

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/SimpleGrover.qs" range="4-41":::

1. <span data-ttu-id="aa446-125">Чтобы определить список, в котором выполняется поиск, создайте новый файл `Reflections.qs` и вставьте в него следующий код:</span><span class="sxs-lookup"><span data-stu-id="aa446-125">To define the list that we're searching, create a new file `Reflections.qs`, and paste in the following code:</span></span>

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/Reflections.qs" range="4-70":::

    <span data-ttu-id="aa446-126">Операция `ReflectAboutMarked` определяет помеченные входные данные, которые вы ищете: строка с чередованием нулей и единиц.</span><span class="sxs-lookup"><span data-stu-id="aa446-126">The `ReflectAboutMarked` operation defines the marked input that you are searching for: the string of alternating zeros and ones.</span></span> <span data-ttu-id="aa446-127">В этом примере помеченные входные данные жестко прописаны в коде, но вы можете дополнить пример поиском других входных данных или обобщить для поиска любых входных данных.</span><span class="sxs-lookup"><span data-stu-id="aa446-127">This sample hard-codes the marked input, and can be extended to search for different inputs or generalized for any input.</span></span>

1. <span data-ttu-id="aa446-128">Теперь запустите эту программу Q#, чтобы найти элемент с меткой `ReflectAboutMarked`.</span><span class="sxs-lookup"><span data-stu-id="aa446-128">Next, run your new Q# program to find the item marked by `ReflectAboutMarked`.</span></span>

### <a name="q-command-line-applications-with-visual-studio-or-visual-studio-code"></a><span data-ttu-id="aa446-129">Приложения командной строки Q# в Visual Studio или Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="aa446-129">Q# command line applications with Visual Studio or Visual Studio Code</span></span>

<span data-ttu-id="aa446-130">Исполняемый файл будет выполнять операцию или функцию, помеченную атрибутом `@EntryPoint()`, в симуляторе или оценщике ресурсов в зависимости от конфигурации проекта и параметров командной строки.</span><span class="sxs-lookup"><span data-stu-id="aa446-130">The executable will run the operation or function marked with the `@EntryPoint()` attribute on a simulator or resource estimator, depending on the project configuration and command-line options.</span></span>

<span data-ttu-id="aa446-131">В Visual Studio просто нажмите клавиши CTRL+F5, чтобы выполнить скрипт.</span><span class="sxs-lookup"><span data-stu-id="aa446-131">In Visual Studio, simply press Ctrl + F5 to execute the script.</span></span>

<span data-ttu-id="aa446-132">При первом выполнении в VS Code нужно создать файл `Program.qs`. Для этого введите следующую команду в окне терминала:</span><span class="sxs-lookup"><span data-stu-id="aa446-132">In VS Code, build the `Program.qs` the first time by typing the below in the terminal:</span></span>

```Command line
dotnet build
```

<span data-ttu-id="aa446-133">Для последующих выполнений его не нужно создавать повторно.</span><span class="sxs-lookup"><span data-stu-id="aa446-133">For subsequent runs, there is no need to build it again.</span></span> <span data-ttu-id="aa446-134">Для выполнения введите следующую команду и нажмите клавишу ВВОД:</span><span class="sxs-lookup"><span data-stu-id="aa446-134">To run it, type the following command and press enter:</span></span>

```Command line
dotnet run --no-build
```

<span data-ttu-id="aa446-135">В окне терминала должно появиться следующее сообщение:</span><span class="sxs-lookup"><span data-stu-id="aa446-135">You should see the following message displayed in the terminal:</span></span>

```
operations.qs:
This operation applies Grover's algorithm to search all possible inputs to an operation to find a particular marked state.
Usage:
operations.qs [options] [command]

--n-qubits <n-qubits> (REQUIRED)
-s, --simulator <simulator>         The name of the simulator to use.
--version                           Show version information
-?, -h, --help                      Show help and usage information
Commands:
```

<span data-ttu-id="aa446-136">Это связано с тем, что вы не указали нужное количество кубитов. Поэтому терминал сообщает о командах, доступных для исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="aa446-136">This is because you didn't specify the number of qubits you wanted to use, so the terminal tells you the commands available for the executable.</span></span> <span data-ttu-id="aa446-137">Если мы хотим использовать 5 кубитов, нужно ввести следующее:</span><span class="sxs-lookup"><span data-stu-id="aa446-137">If we want to use 5 qubits we should type:</span></span>

```Command line
dotnet run --n-qubits 5
```

<span data-ttu-id="aa446-138">После нажатия клавиши ВВОД должен отобразиться следующий результат:</span><span class="sxs-lookup"><span data-stu-id="aa446-138">Pressing enter you should see the following output:</span></span>

```
Reflecting about marked state...
Reflecting about marked state...
Reflecting about marked state...
Reflecting about marked state...
[Zero,One,Zero,One,Zero]
```

## <a name="next-steps"></a><span data-ttu-id="aa446-139">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="aa446-139">Next steps</span></span>

<span data-ttu-id="aa446-140">Если вам понравилось это руководство, воспользуйтесь перечисленными ниже ресурсами, чтобы изучить другие варианты применения Q# для собственных квантовых приложений:</span><span class="sxs-lookup"><span data-stu-id="aa446-140">If you enjoyed this tutorial, check out some of the resources below to learn more about how you can use Q# to write your own quantum applications:</span></span>

- [<span data-ttu-id="aa446-141">Вернуться руководству по началу работы с QDK</span><span class="sxs-lookup"><span data-stu-id="aa446-141">Back to the Getting Started with QDK guide</span></span>](xref:microsoft.quantum.welcome)
- <span data-ttu-id="aa446-142">Попробуйте изучить более общий алгоритм поиска Гровера из [этого примера](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/database-search).</span><span class="sxs-lookup"><span data-stu-id="aa446-142">Try a more general Grover's search algorithm [sample](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/database-search)</span></span>
- [<span data-ttu-id="aa446-143">Более подробное знакомство с алгоритмом поиска Гровера в Quantum Katas</span><span class="sxs-lookup"><span data-stu-id="aa446-143">Learn more about Grover's search with the Quantum Katas</span></span>](xref:microsoft.quantum.overview.katas)
- <span data-ttu-id="aa446-144">См. сведения о методике [усиления амплитуды][amplitude-amplification] в квантовых вычислениях, на которой основан алгоритм поиска Гровера.</span><span class="sxs-lookup"><span data-stu-id="aa446-144">Read more about [Amplitude amplification][amplitude-amplification], the quantum computing technique behind Grover's search algorithm</span></span>
- [<span data-ttu-id="aa446-145">Концепции квантовых вычислений</span><span class="sxs-lookup"><span data-stu-id="aa446-145">Quantum computing concepts</span></span>](xref:microsoft.quantum.concepts.intro)
- [<span data-ttu-id="aa446-146">Примеры для Quantum Development Kit</span><span class="sxs-lookup"><span data-stu-id="aa446-146">Quantum Development Kit Samples</span></span>](https://docs.microsoft.com/samples/browse/?products=qdk)

<!-- LINKS -->

[install]: xref:microsoft.quantum.install
[amplitude-amplification]: xref:microsoft.quantum.libraries.standard.algorithms#amplitude-amplification
