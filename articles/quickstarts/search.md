---
title: Выполнение алгоритма поиска Гровер на Q# (Quantum Development Kit)
description: Создайте проект Q# с демонстрацией алгоритма Гровера, одного из самых известных квантовых алгоритмов.
author: cgranade
ms.author: chgranad@microsoft.com
ms.date: 10/19/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.search
ms.openlocfilehash: 9e4c53b4d5159cf07f0654603c1d477ad09eb7c6
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327413"
---
# <a name="tutorial-implement-grovers-search-algorithm-in-q"></a><span data-ttu-id="e1f10-103">Руководство по Реализация поиска по алгоритму Гровера на Q\#</span><span class="sxs-lookup"><span data-stu-id="e1f10-103">Tutorial: Implement Grover's search algorithm in Q\#</span></span>

<span data-ttu-id="e1f10-104">В этом руководстве объясняется, как создать и применить алгоритм Гровера, который ускоряет поиск по неструктурированным данным.</span><span class="sxs-lookup"><span data-stu-id="e1f10-104">In this tutorial, you can learn how to build and run Grover search to speed up the search of unstructured data.</span></span>  <span data-ttu-id="e1f10-105">Алгоритм Гровера считается одним из самых известных алгоритмов квантовых вычислений. Эта несложная реализация на Q# познакомит вас с преимуществами систем квантовых вычислений, в которых квантовые алгоритмы выражаются на высокоуровневых языках типа Q#.</span><span class="sxs-lookup"><span data-stu-id="e1f10-105">Grover's search is one of the most popular quantum computing algorithms, and this relatively small Q# implementation gives you a sense of some of the advantages of programming quantum solutions with a high-level Q# quantum programming language to express quantum algorithms.</span></span>  <span data-ttu-id="e1f10-106">В конце работы с этим руководством вы увидите, что ваша модель обнаруживает нужную строку в неупорядоченном списке записей намного быстрее, чем потребуется для полного просмотра списка на классическом компьютере.</span><span class="sxs-lookup"><span data-stu-id="e1f10-106">At the end of the guide, you will see the simulation output demonstrates successfully finding a specific string among a list of unordered entries in a fraction of the time it would take to search the whole list on a classical computer.</span></span>

<span data-ttu-id="e1f10-107">Алгоритм Гровера ищет конкретные элементы в неструктурированном списке данных.</span><span class="sxs-lookup"><span data-stu-id="e1f10-107">Grover's algorithm searches a list of unstructured data for specific items.</span></span> <span data-ttu-id="e1f10-108">Например, он позволяет ответить на следующие вопросы: Является ли карта, извлеченная наугад из колоды, тузом червей?</span><span class="sxs-lookup"><span data-stu-id="e1f10-108">For example, it can answer the question: Is this card drawn from a pack of cards an ace of hearts?</span></span> <span data-ttu-id="e1f10-109">Добавление меток для конкретного элемента называется _разметкой входных данных_.</span><span class="sxs-lookup"><span data-stu-id="e1f10-109">The labeling of the specific item is called _marked input_.</span></span>

<span data-ttu-id="e1f10-110">По алгоритму поиска Гровера квантовый компьютер гарантированно потратит меньше шагов на такой поиск, чем количество элементов в просматриваемом списке, что невозможно гарантировать ни одним классическим алгоритмом.</span><span class="sxs-lookup"><span data-stu-id="e1f10-110">Using Grover's search algorithm, a quantum computer is guaranteed to run this search in fewer steps than the number of items in the list that you're searching — something no classical algorithm can do.</span></span> <span data-ttu-id="e1f10-111">На одной колоде карт увеличение скорости пренебрежимо мало, но для списков с миллионами или миллиардами элементов разница становится значимой.</span><span class="sxs-lookup"><span data-stu-id="e1f10-111">The increased speed in the case of a pack of cards is negligible; however, in lists containing millions or billions of items, it becomes significant.</span></span>

<span data-ttu-id="e1f10-112">Алгоритм поиска Гровера можно реализовать всего в нескольких строках кода.</span><span class="sxs-lookup"><span data-stu-id="e1f10-112">You can build Grover's search algorithm with just a few lines of code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e1f10-113">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="e1f10-113">Prerequisites</span></span>

- <span data-ttu-id="e1f10-114">[Microsoft Quantum Development Kit][install].</span><span class="sxs-lookup"><span data-stu-id="e1f10-114">The Microsoft [Quantum Development Kit][install].</span></span>

## <a name="what-does-grovers-search-algorithm-do"></a><span data-ttu-id="e1f10-115">Что же делает алгоритм поиска Гровера?</span><span class="sxs-lookup"><span data-stu-id="e1f10-115">What does Grover's search algorithm do?</span></span>

<span data-ttu-id="e1f10-116">Алгоритм Гровера проверяет, является ли элемент списка искомым элементом.</span><span class="sxs-lookup"><span data-stu-id="e1f10-116">Grover's algorithm asks whether an item in a list is the one we are searching for.</span></span> <span data-ttu-id="e1f10-117">Для этого он создает квантовую суперпозицию индексов списка, где каждый коэффициент (амплитуда вероятности) соответствует вероятности того, что этот индекс является искомым элементом.</span><span class="sxs-lookup"><span data-stu-id="e1f10-117">It does this by constructing a quantum superposition of the indexes of the list with each coefficient, or probability amplitude, representing the probability of that specific index being the one you are looking for.</span></span>

<span data-ttu-id="e1f10-118">В основе алгоритма лежат два шага, которые постепенно увеличивают коэффициент индекса, пока амплитуда вероятности этого коэффициента не достигнет единицы.</span><span class="sxs-lookup"><span data-stu-id="e1f10-118">At the heart of the algorithm are two steps that incrementally boost the coefficient of the index that we are looking for, until the probability amplitude of that coefficient approaches one.</span></span>

<span data-ttu-id="e1f10-119">Число добавочных увеличений заведомо меньше числа элементов в списке.</span><span class="sxs-lookup"><span data-stu-id="e1f10-119">The number of incremental boosts is fewer than the number of items in the list.</span></span> <span data-ttu-id="e1f10-120">Поэтому алгоритм поиска Гровера выполняет поиск за меньшее количество шагов, чем любой классический алгоритм.</span><span class="sxs-lookup"><span data-stu-id="e1f10-120">This is why Grover's search algorithm performs the search in fewer steps than any classical algorithm.</span></span>

![Функциональная схема для алгоритма поиска Гровера](~/media/grover.png)

## <a name="write-the-code"></a><span data-ttu-id="e1f10-122">Написание кода</span><span class="sxs-lookup"><span data-stu-id="e1f10-122">Write the code</span></span>

1. <span data-ttu-id="e1f10-123">Используя пакет средств разработки Quantum, [создайте новый проект Q# для приложения командной строки](xref:microsoft.quantum.install.standalone).</span><span class="sxs-lookup"><span data-stu-id="e1f10-123">Using the Quantum Development Kit, [create a new Q# project for the command line application](xref:microsoft.quantum.install.standalone).</span></span> <span data-ttu-id="e1f10-124">Присвойте проекту имя `Grover`.</span><span class="sxs-lookup"><span data-stu-id="e1f10-124">Title the project `Grover`.</span></span>

1. <span data-ttu-id="e1f10-125">В файл `Program.qs` этого проекта добавьте следующий код:</span><span class="sxs-lookup"><span data-stu-id="e1f10-125">Add the following code to the `Program.qs` file in your new project:</span></span>

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/SimpleGrover.qs" range="4-41":::

1. <span data-ttu-id="e1f10-126">Чтобы определить список, в котором выполняется поиск, создайте новый файл `Reflections.qs` и вставьте в него следующий код:</span><span class="sxs-lookup"><span data-stu-id="e1f10-126">To define the list that we're searching, create a new file `Reflections.qs`, and paste in the following code:</span></span>

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/Reflections.qs" range="4-70":::

    <span data-ttu-id="e1f10-127">Операция `ReflectAboutMarked` определяет помеченные входные данные, которые вы ищете: строка с чередованием нулей и единиц.</span><span class="sxs-lookup"><span data-stu-id="e1f10-127">The `ReflectAboutMarked` operation defines the marked input that you are searching for: the string of alternating zeros and ones.</span></span> <span data-ttu-id="e1f10-128">В этом примере помеченные входные данные жестко прописаны в коде, но вы можете дополнить пример поиском других входных данных или обобщить для поиска любых входных данных.</span><span class="sxs-lookup"><span data-stu-id="e1f10-128">This sample hard-codes the marked input, and can be extended to search for different inputs or generalized for any input.</span></span>

1. <span data-ttu-id="e1f10-129">Теперь запустите эту программу Q#, чтобы найти элемент с меткой `ReflectAboutMarked`.</span><span class="sxs-lookup"><span data-stu-id="e1f10-129">Next, run your new Q# program to find the item marked by `ReflectAboutMarked`.</span></span>

### <a name="q-command-line-applications-with-visual-studio-or-visual-studio-code"></a><span data-ttu-id="e1f10-130">Приложения командной строки Q# в Visual Studio или Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="e1f10-130">Q# command line applications with Visual Studio or Visual Studio Code</span></span>

<span data-ttu-id="e1f10-131">Исполняемый файл будет выполнять операцию или функцию, помеченную атрибутом `@EntryPoint()`, в симуляторе или оценщике ресурсов в зависимости от конфигурации проекта и параметров командной строки.</span><span class="sxs-lookup"><span data-stu-id="e1f10-131">The executable will run the operation or function marked with the `@EntryPoint()` attribute on a simulator or resource estimator, depending on the project configuration and command-line options.</span></span>

<span data-ttu-id="e1f10-132">В Visual Studio просто нажмите клавиши CTRL+F5, чтобы выполнить скрипт.</span><span class="sxs-lookup"><span data-stu-id="e1f10-132">In Visual Studio, simply press Ctrl + F5 to execute the script.</span></span>

<span data-ttu-id="e1f10-133">При первом выполнении в VS Code нужно создать файл `Program.qs`. Для этого введите следующую команду в окне терминала:</span><span class="sxs-lookup"><span data-stu-id="e1f10-133">In VS Code, build the `Program.qs` the first time by typing the below in the terminal:</span></span>

```Command line
dotnet build
```

<span data-ttu-id="e1f10-134">Для последующих выполнений его не нужно создавать повторно.</span><span class="sxs-lookup"><span data-stu-id="e1f10-134">For subsequent runs, there is no need to build it again.</span></span> <span data-ttu-id="e1f10-135">Для выполнения введите следующую команду и нажмите клавишу ВВОД:</span><span class="sxs-lookup"><span data-stu-id="e1f10-135">To run it, type the following command and press enter:</span></span>

```Command line
dotnet run --no-build
```

<span data-ttu-id="e1f10-136">В окне терминала должно появиться следующее сообщение:</span><span class="sxs-lookup"><span data-stu-id="e1f10-136">You should see the following message displayed in the terminal:</span></span>

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

<span data-ttu-id="e1f10-137">Это связано с тем, что вы не указали нужное количество кубитов. Поэтому терминал сообщает о командах, доступных для исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="e1f10-137">This is because you didn't specify the number of qubits you wanted to use, so the terminal tells you the commands available for the executable.</span></span> <span data-ttu-id="e1f10-138">Если мы хотим использовать 5 кубитов, нужно ввести следующее:</span><span class="sxs-lookup"><span data-stu-id="e1f10-138">If we want to use 5 qubits we should type:</span></span>

```Command line
dotnet run --n-qubits 5
```

<span data-ttu-id="e1f10-139">После нажатия клавиши ВВОД должен отобразиться следующий результат:</span><span class="sxs-lookup"><span data-stu-id="e1f10-139">Pressing enter you should see the following output:</span></span>

```
Reflecting about marked state...
Reflecting about marked state...
Reflecting about marked state...
Reflecting about marked state...
[Zero,One,Zero,One,Zero]
```

## <a name="next-steps"></a><span data-ttu-id="e1f10-140">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="e1f10-140">Next steps</span></span>

<span data-ttu-id="e1f10-141">Если вам понравилось это руководство, воспользуйтесь перечисленными ниже ресурсами, чтобы изучить другие варианты применения Q# для собственных квантовых приложений:</span><span class="sxs-lookup"><span data-stu-id="e1f10-141">If you enjoyed this tutorial, check out some of the resources below to learn more about how you can use Q# to write your own quantum applications:</span></span>

- [<span data-ttu-id="e1f10-142">Вернуться руководству по началу работы с QDK</span><span class="sxs-lookup"><span data-stu-id="e1f10-142">Back to the Getting Started with QDK guide</span></span>](xref:microsoft.quantum.welcome)
- <span data-ttu-id="e1f10-143">Попробуйте изучить более общий алгоритм поиска Гровера из [этого примера](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/database-search).</span><span class="sxs-lookup"><span data-stu-id="e1f10-143">Try a more general Grover's search algorithm [sample](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/database-search)</span></span>
- [<span data-ttu-id="e1f10-144">Более подробное знакомство с алгоритмом поиска Гровера в Quantum Katas</span><span class="sxs-lookup"><span data-stu-id="e1f10-144">Learn more about Grover's search with the Quantum Katas</span></span>](xref:microsoft.quantum.overview.katas)
- <span data-ttu-id="e1f10-145">См. сведения о методике [усиления амплитуды][amplitude-amplification] в квантовых вычислениях, на которой основан алгоритм поиска Гровера.</span><span class="sxs-lookup"><span data-stu-id="e1f10-145">Read more about [Amplitude amplification][amplitude-amplification], the quantum computing technique behind Grover's search algorithm</span></span>
- [<span data-ttu-id="e1f10-146">Концепции квантовых вычислений</span><span class="sxs-lookup"><span data-stu-id="e1f10-146">Quantum computing concepts</span></span>](xref:microsoft.quantum.concepts.intro)
- [<span data-ttu-id="e1f10-147">Примеры для Quantum Development Kit</span><span class="sxs-lookup"><span data-stu-id="e1f10-147">Quantum Development Kit Samples</span></span>](https://docs.microsoft.com/samples/browse/?products=qdk)

<!-- LINKS -->

[install]: xref:microsoft.quantum.install
[amplitude-amplification]: xref:microsoft.quantum.libraries.standard.algorithms#amplitude-amplification
