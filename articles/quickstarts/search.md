---
title: Выполнение алгоритма поиска Гровер на Q# (Quantum Development Kit)
description: Создайте проект Q# с демонстрацией алгоритма Гровера, одного из самых известных квантовых алгоритмов.
author: cgranade
ms.author: chgranad@microsoft.com
ms.date: 10/19/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.search
ms.openlocfilehash: 0e64fcd56929fa33397c45bf1b2e99bf687eca6f
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/28/2020
ms.locfileid: "77906956"
---
# <a name="quickstart-implement-grovers-search-algorithm-in-q"></a>Краткое руководство. Реализация поиска по алгоритму Гровера на Q#

В этом кратком руководстве описано, как создать и применить алгоритм Гровера, который ускоряет поиск по неструктурированным данным.  Алгоритм Гровера считается одним из самых известных алгоритмов квантовых вычислений. Эта несложная реализация на Q# познакомит вас с преимуществами систем квантовых вычислений, в которых квантовые алгоритмы выражаются на высокоуровневых языках типа Q#.  В конце работы с этим руководством вы увидите, что ваша модель обнаруживает нужную строку в неупорядоченном списке записей намного быстрее, чем потребуется для полного просмотра списка на классическом компьютере.

Алгоритм Гровера ищет конкретные элементы в неструктурированном списке данных. Например, он позволяет ответить на следующие вопросы: Является ли карта, извлеченная наугад из колоды, тузом червей? Добавление меток для конкретного элемента называется _разметкой входных данных_.

По алгоритму поиска Гровера квантовый компьютер гарантированно потратит меньше шагов на такой поиск, чем количество элементов в просматриваемом списке, что невозможно гарантировать ни одним классическим алгоритмом. На одной колоде карт увеличение скорости пренебрежимо мало, но для списков с миллионами или миллиардами элементов разница становится значимой.

Алгоритм поиска Гровера можно реализовать всего в нескольких строках кода.

## <a name="prerequisites"></a>Предварительные требования

- [Microsoft Quantum Development Kit][install].

## <a name="what-does-grovers-search-algorithm-do"></a>Что же делает алгоритм поиска Гровера?

Алгоритм Гровера проверяет, является ли элемент списка искомым элементом. Для этого он создает квантовую суперпозицию индексов списка, где каждый коэффициент (амплитуда вероятности) соответствует вероятности того, что этот индекс является искомым элементом.

В основе алгоритма лежат два шага, которые постепенно увеличивают коэффициент индекса, пока амплитуда вероятности этого коэффициента не достигнет единицы.

Число добавочных увеличений заведомо меньше числа элементов в списке. Поэтому алгоритм поиска Гровера выполняет поиск за меньшее количество шагов, чем любой классический алгоритм.

![Функциональная схема для алгоритма поиска Гровера](~/media/grover.png)

## <a name="write-the-code"></a>Написание кода

1. Используя Quantum Development Kit, [создайте новый проект Q#](xref:microsoft.quantum.howto.createproject) с именем `Grover` в любой удобной среде разработки.

1. В файл `Operations.qs` этого проекта добавьте следующий код:

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/SimpleGrover.qs" range="4-40":::

1. Чтобы определить список, в котором выполняется поиск, создайте новый файл `Reflections.qs` и вставьте в него следующий код:

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/Reflections.qs" range="4-70":::

    Операция `ReflectAboutMarked` определяет помеченные входные данные, которые вы ищете: строка с чередованием нулей и единиц. В этом примере помеченные входные данные жестко прописаны в коде, но вы можете дополнить пример поиском других входных данных или обобщить для поиска любых входных данных.

1. Теперь запустите эту программу Q#, чтобы найти элемент с меткой `ReflectAboutMarked`.

    ### <a name="python-with-visual-studio-code-or-the-command-line"></a>[Вызов Python из Visual Studio Code или командной строки](#tab/tabid-python)

    Чтобы выполнить эту программу Q# из кода Python, сохраните следующий код в файл `host.py`:

    :::code language="python" source="~/quantum/samples/algorithms/simple-grover/host.py" range="9-14":::

    Теперь вы сможете запустить основную программу Python из командной строки следующим образом:

    ```bash
    $ python host.py
    Preparing Q# environment...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    [0, 1, 0, 1, 0]
    ```

    ### <a name="c-with-visual-studio-code-or-the-command-line"></a>[Вызов C# из Visual Studio Code или командной строки](#tab/tabid-csharp)

    Чтобы выполнить эту программу Q# из кода C#, измените `Driver.cs`, включив в него следующий код:

    :::code language="csharp" source="~/quantum/samples/algorithms/simple-grover/Host.cs" range="4-23":::

    Теперь вы сможете запустить основную программу C# из командной строки следующим образом:

    ```bash
    $ dotnet run
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Result: [Zero,One,Zero,One,Zero]

    Press any key to continue...
    ```

    ### <a name="c-with-visual-studio-2019"></a>[Вызов C# из Visual Studio 2019](#tab/tabid-vs2019)

    Чтобы выполнить эту программу Q# из кода C# в Visual Studio, измените `Driver.cs`, включив в него следующий код:

    :::code language="csharp" source="~/quantum/samples/algorithms/simple-grover/Host.cs" range="4-23":::

    Затем нажмите клавишу F5, чтобы запустить программу. Вы увидите новое всплывающее окно со следующими результатами: 

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

    Операция `ReflectAboutMarked` была вызвана только четыре раза, но программа на Q# смогла найти входные данные 01010 из $2^{5} = 32$ возможных вариантов!

## <a name="next-steps"></a>Дальнейшие действия

Если вам понравилось это краткое руководство, воспользуйтесь перечисленными ниже ресурсами, чтобы изучить другие варианты применения Q# для собственных квантовых приложений.

- [Вернуться руководству по началу работы с QDK](xref:microsoft.quantum.welcome)
- Попробуйте изучить более общий алгоритм поиска Гровера из [этого примера](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/database-search).
- [Более подробное знакомство с алгоритмом поиска Гровера в Quantum Katas](xref:microsoft.quantum.overview.katas)
- См. сведения о методике [усиления амплитуды](xref:microsoft.quantum.libraries.standard.algorithms#amplitude-amplification) в квантовых вычислениях, на которой основан алгоритм поиска Гровера.
- [Концепции квантовых вычислений](xref:microsoft.quantum.concepts.intro)
- [Примеры для Quantum Development Kit](https://docs.microsoft.com/samples/browse/?products=qdk)

<!-- LINKS -->

[install]: xref:microsoft.quantum.install
