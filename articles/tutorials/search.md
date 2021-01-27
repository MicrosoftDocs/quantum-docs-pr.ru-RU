---
title: Запуск алгоритма поиска Гровер в Q# -тактовой среде
description: Создайте Q# проект, демонстрирующий алгоритм Гровер, один из канонических алгоритмов такта.
author: cgranade
ms.author: chgranad
ms.date: 10/19/2019
ms.topic: tutorial
uid: microsoft.quantum.quickstarts.search
no-loc:
- Q#
- $$v
ms.openlocfilehash: 5e0398338ff710decc0f3038c07c9b7d39514195
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856633"
---
# <a name="tutorial-implement-grovers-search-algorithm-in-q"></a><span data-ttu-id="e33f8-103">Руководство по Реализация поиска по алгоритму Гровера на Q\#</span><span class="sxs-lookup"><span data-stu-id="e33f8-103">Tutorial: Implement Grover's search algorithm in Q\#</span></span>

<span data-ttu-id="e33f8-104">В этом руководстве объясняется, как создать и применить алгоритм Гровера, который ускоряет поиск по неструктурированным данным.</span><span class="sxs-lookup"><span data-stu-id="e33f8-104">In this tutorial, you can learn how to build and run Grover search to speed up the search of unstructured data.</span></span>  <span data-ttu-id="e33f8-105">Поиск в Гровер является одним из самых популярных алгоритмов тактовой задержки, и эта относительно небольшая Q# реализация позволяет понять некоторые из преимуществ разработки тактовых решений с использованием высокоуровневого Q# языкового программирования для вычисления тактовых алгоритмов.</span><span class="sxs-lookup"><span data-stu-id="e33f8-105">Grover's search is one of the most popular quantum computing algorithms, and this relatively small Q# implementation gives you a sense of some of the advantages of programming quantum solutions with a high-level Q# quantum programming language to express quantum algorithms.</span></span>  <span data-ttu-id="e33f8-106">В конце работы с этим руководством вы увидите, что ваша модель обнаруживает нужную строку в неупорядоченном списке записей намного быстрее, чем потребуется для полного просмотра списка на классическом компьютере.</span><span class="sxs-lookup"><span data-stu-id="e33f8-106">At the end of the guide, you will see the simulation output demonstrates successfully finding a specific string among a list of unordered entries in a fraction of the time it would take to search the whole list on a classical computer.</span></span>

<span data-ttu-id="e33f8-107">Алгоритм Гровера ищет конкретные элементы в неструктурированном списке данных.</span><span class="sxs-lookup"><span data-stu-id="e33f8-107">Grover's algorithm searches a list of unstructured data for specific items.</span></span> <span data-ttu-id="e33f8-108">Например, он позволяет ответить на следующие вопросы: Является ли карта, извлеченная наугад из колоды, тузом червей?</span><span class="sxs-lookup"><span data-stu-id="e33f8-108">For example, it can answer the question: Is this card drawn from a pack of cards an ace of hearts?</span></span> <span data-ttu-id="e33f8-109">Добавление меток для конкретного элемента называется _разметкой входных данных_.</span><span class="sxs-lookup"><span data-stu-id="e33f8-109">The labeling of the specific item is called _marked input_.</span></span>

<span data-ttu-id="e33f8-110">По алгоритму поиска Гровера квантовый компьютер гарантированно потратит меньше шагов на такой поиск, чем количество элементов в просматриваемом списке, что невозможно гарантировать ни одним классическим алгоритмом.</span><span class="sxs-lookup"><span data-stu-id="e33f8-110">Using Grover's search algorithm, a quantum computer is guaranteed to run this search in fewer steps than the number of items in the list that you're searching — something no classical algorithm can do.</span></span> <span data-ttu-id="e33f8-111">На одной колоде карт увеличение скорости пренебрежимо мало, но для списков с миллионами или миллиардами элементов разница становится значимой.</span><span class="sxs-lookup"><span data-stu-id="e33f8-111">The increased speed in the case of a pack of cards is negligible; however, in lists containing millions or billions of items, it becomes significant.</span></span>

<span data-ttu-id="e33f8-112">Алгоритм поиска Гровера можно реализовать всего в нескольких строках кода.</span><span class="sxs-lookup"><span data-stu-id="e33f8-112">You can build Grover's search algorithm with just a few lines of code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e33f8-113">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="e33f8-113">Prerequisites</span></span>

- <span data-ttu-id="e33f8-114">[Microsoft Quantum Development Kit][install].</span><span class="sxs-lookup"><span data-stu-id="e33f8-114">The Microsoft [Quantum Development Kit][install].</span></span>

## <a name="what-does-grovers-search-algorithm-do"></a><span data-ttu-id="e33f8-115">Что же делает алгоритм поиска Гровера?</span><span class="sxs-lookup"><span data-stu-id="e33f8-115">What does Grover's search algorithm do?</span></span>

<span data-ttu-id="e33f8-116">Алгоритм Гровера проверяет, является ли элемент списка искомым элементом.</span><span class="sxs-lookup"><span data-stu-id="e33f8-116">Grover's algorithm asks whether an item in a list is the one we are searching for.</span></span> <span data-ttu-id="e33f8-117">Для этого он создает квантовую суперпозицию индексов списка, где каждый коэффициент (амплитуда вероятности) соответствует вероятности того, что этот индекс является искомым элементом.</span><span class="sxs-lookup"><span data-stu-id="e33f8-117">It does this by constructing a quantum superposition of the indexes of the list with each coefficient, or probability amplitude, representing the probability of that specific index being the one you are looking for.</span></span>

<span data-ttu-id="e33f8-118">В основе алгоритма лежат два шага, которые постепенно увеличивают коэффициент индекса, пока амплитуда вероятности этого коэффициента не достигнет единицы.</span><span class="sxs-lookup"><span data-stu-id="e33f8-118">At the heart of the algorithm are two steps that incrementally boost the coefficient of the index that we are looking for, until the probability amplitude of that coefficient approaches one.</span></span>

<span data-ttu-id="e33f8-119">Число добавочных увеличений заведомо меньше числа элементов в списке.</span><span class="sxs-lookup"><span data-stu-id="e33f8-119">The number of incremental boosts is fewer than the number of items in the list.</span></span> <span data-ttu-id="e33f8-120">Поэтому алгоритм поиска Гровера выполняет поиск за меньшее количество шагов, чем любой классический алгоритм.</span><span class="sxs-lookup"><span data-stu-id="e33f8-120">This is why Grover's search algorithm performs the search in fewer steps than any classical algorithm.</span></span>

![Функциональная схема для алгоритма поиска Гровера](~/media/grover.png)

## <a name="write-the-code"></a><span data-ttu-id="e33f8-122">Написание кода</span><span class="sxs-lookup"><span data-stu-id="e33f8-122">Write the code</span></span>

1. <span data-ttu-id="e33f8-123">С помощью пакета средств разработки такта [Создайте новый Q# проект для приложения](xref:microsoft.quantum.install.standalone).</span><span class="sxs-lookup"><span data-stu-id="e33f8-123">Using the Quantum Development Kit, [create a new Q# project for the application](xref:microsoft.quantum.install.standalone).</span></span> <span data-ttu-id="e33f8-124">Присвойте проекту имя `Grover`.</span><span class="sxs-lookup"><span data-stu-id="e33f8-124">Title the project `Grover`.</span></span>

1. <span data-ttu-id="e33f8-125">В файл `Program.qs` этого проекта добавьте следующий код:</span><span class="sxs-lookup"><span data-stu-id="e33f8-125">Add the following code to the `Program.qs` file in your new project:</span></span>

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/SimpleGrover.qs" range="4-41":::

1. <span data-ttu-id="e33f8-126">Чтобы определить список, в котором выполняется поиск, создайте новый файл `Reflections.qs` и вставьте в него следующий код:</span><span class="sxs-lookup"><span data-stu-id="e33f8-126">To define the list that we're searching, create a new file `Reflections.qs`, and paste in the following code:</span></span>

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/Reflections.qs" range="4-70":::

    <span data-ttu-id="e33f8-127">Операция `ReflectAboutMarked` определяет помеченные входные данные, которые вы ищете: строка с чередованием нулей и единиц.</span><span class="sxs-lookup"><span data-stu-id="e33f8-127">The `ReflectAboutMarked` operation defines the marked input that you are searching for: the string of alternating zeros and ones.</span></span> <span data-ttu-id="e33f8-128">В этом примере помеченные входные данные жестко прописаны в коде, но вы можете дополнить пример поиском других входных данных или обобщить для поиска любых входных данных.</span><span class="sxs-lookup"><span data-stu-id="e33f8-128">This sample hard-codes the marked input, and can be extended to search for different inputs or generalized for any input.</span></span>

1. <span data-ttu-id="e33f8-129">Затем запустите новую программу, Q# чтобы найти элемент, помеченный `ReflectAboutMarked` .</span><span class="sxs-lookup"><span data-stu-id="e33f8-129">Next, run your new Q# program to find the item marked by `ReflectAboutMarked`.</span></span>

### <a name="no-locq-applications-with-visual-studio-or-visual-studio-code"></a><span data-ttu-id="e33f8-130">Q# приложения с Visual Studio или Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="e33f8-130">Q# applications with Visual Studio or Visual Studio Code</span></span>

<span data-ttu-id="e33f8-131">Программа запустит операцию или функцию, помеченную `@EntryPoint()` атрибутом для симулятора или оценщика ресурсов, в зависимости от конфигурации проекта и параметров командной строки.</span><span class="sxs-lookup"><span data-stu-id="e33f8-131">The program will run the operation or function marked with the `@EntryPoint()` attribute on a simulator or resource estimator, depending on the project configuration and command-line options.</span></span>

<span data-ttu-id="e33f8-132">В Visual Studio просто нажмите клавиши CTRL + F5, чтобы запустить сценарий.</span><span class="sxs-lookup"><span data-stu-id="e33f8-132">In Visual Studio, simply press Ctrl + F5 to run the script.</span></span>

<span data-ttu-id="e33f8-133">При первом выполнении в VS Code нужно создать файл `Program.qs`. Для этого введите следующую команду в окне терминала:</span><span class="sxs-lookup"><span data-stu-id="e33f8-133">In VS Code, build the `Program.qs` the first time by typing the below in the terminal:</span></span>

```Command line
dotnet build
```

<span data-ttu-id="e33f8-134">Для последующих выполнений его не нужно создавать повторно.</span><span class="sxs-lookup"><span data-stu-id="e33f8-134">For subsequent runs, there is no need to build it again.</span></span> <span data-ttu-id="e33f8-135">Для выполнения введите следующую команду и нажмите клавишу ВВОД:</span><span class="sxs-lookup"><span data-stu-id="e33f8-135">To run it, type the following command and press enter:</span></span>

```Command line
dotnet run --no-build
```

<span data-ttu-id="e33f8-136">В окне терминала должно появиться следующее сообщение:</span><span class="sxs-lookup"><span data-stu-id="e33f8-136">You should see the following message displayed in the terminal:</span></span>

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

<span data-ttu-id="e33f8-137">Это связано с тем, что вы не указали нужное количество Кубитс, поэтому терминал отображает команды, доступные для исполняемой программы.</span><span class="sxs-lookup"><span data-stu-id="e33f8-137">This is because you didn't specify the number of qubits you wanted to use, so the terminal shows you the commands available for the executable program.</span></span> <span data-ttu-id="e33f8-138">Если мы хотим использовать 5 Кубитс, необходимо ввести:</span><span class="sxs-lookup"><span data-stu-id="e33f8-138">If we want to use 5 qubits, we should type:</span></span>

```Command line
dotnet run --n-qubits 5
```

<span data-ttu-id="e33f8-139">После нажатия клавиши ВВОД должен отобразиться следующий результат:</span><span class="sxs-lookup"><span data-stu-id="e33f8-139">Pressing enter you should see the following output:</span></span>

```
Reflecting about marked state...
Reflecting about marked state...
Reflecting about marked state...
Reflecting about marked state...
[Zero,One,Zero,One,Zero]
```

## <a name="next-steps"></a><span data-ttu-id="e33f8-140">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="e33f8-140">Next steps</span></span>

<span data-ttu-id="e33f8-141">Если вы понравилась вам в этом руководстве, ознакомьтесь с некоторыми из приведенных ниже ресурсов, чтобы узнать больше о том, как можно использовать Q# для написания собственных приложений для работы с тактами:</span><span class="sxs-lookup"><span data-stu-id="e33f8-141">If you enjoyed this tutorial, check out some of the resources below to learn more about how you can use Q# to write your own quantum applications:</span></span>

- [<span data-ttu-id="e33f8-142">Вернуться руководству по началу работы с QDK</span><span class="sxs-lookup"><span data-stu-id="e33f8-142">Back to the Getting Started with QDK guide</span></span>](xref:microsoft.quantum.welcome)
- <span data-ttu-id="e33f8-143">Попробуйте изучить более общий алгоритм поиска Гровера из [этого примера](https://github.com/microsoft/Quantum/tree/main/samples/algorithms/database-search).</span><span class="sxs-lookup"><span data-stu-id="e33f8-143">Try a more general Grover's search algorithm [sample](https://github.com/microsoft/Quantum/tree/main/samples/algorithms/database-search)</span></span>
- [<span data-ttu-id="e33f8-144">Более подробное знакомство с алгоритмом поиска Гровера в Quantum Katas</span><span class="sxs-lookup"><span data-stu-id="e33f8-144">Learn more about Grover's search with the Quantum Katas</span></span>](xref:microsoft.quantum.overview.katas)
- <span data-ttu-id="e33f8-145">См. сведения о методике [усиления амплитуды][amplitude-amplification] в квантовых вычислениях, на которой основан алгоритм поиска Гровера.</span><span class="sxs-lookup"><span data-stu-id="e33f8-145">Read more about [Amplitude amplification][amplitude-amplification], the quantum computing technique behind Grover's search algorithm</span></span>
- [<span data-ttu-id="e33f8-146">Концепции квантовых вычислений</span><span class="sxs-lookup"><span data-stu-id="e33f8-146">Quantum computing concepts</span></span>](xref:microsoft.quantum.concepts.intro)
- [<span data-ttu-id="e33f8-147">Примеры для Quantum Development Kit</span><span class="sxs-lookup"><span data-stu-id="e33f8-147">Quantum Development Kit Samples</span></span>](https://docs.microsoft.com/samples/browse/?products=qdk)

<!-- LINKS -->

[install]: xref:microsoft.quantum.install
[amplitude-amplification]: xref:microsoft.quantum.libraries.standard.algorithms#amplitude-amplification
