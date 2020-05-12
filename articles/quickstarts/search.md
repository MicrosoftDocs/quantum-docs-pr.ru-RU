---
title: Выполнение алгоритма поиска Гровер на Q# (Quantum Development Kit)
description: Создайте проект Q# с демонстрацией алгоритма Гровера, одного из самых известных квантовых алгоритмов.
author: cgranade
ms.author: chgranad@microsoft.com
ms.date: 10/19/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.search
ms.openlocfilehash: c67ccd16957ceef694552bdd9c073ba5a35d8aaf
ms.sourcegitcommit: db23885adb7ff76cbf8bd1160d401a4f0471e549
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/01/2020
ms.locfileid: "82686829"
---
# <a name="quickstart-implement-grovers-search-algorithm-in-q"></a>Краткое руководство. Реализация поиска по алгоритму Гровера на Q\#

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

1. В файл `Program.qs` этого проекта добавьте следующий код:

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/SimpleGrover.qs" range="4-41":::

1. Чтобы определить список, в котором выполняется поиск, создайте новый файл `Reflections.qs` и вставьте в него следующий код:

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/Reflections.qs" range="4-70":::

    Операция `ReflectAboutMarked` определяет помеченные входные данные, которые вы ищете: строка с чередованием нулей и единиц. В этом примере помеченные входные данные жестко прописаны в коде, но вы можете дополнить пример поиском других входных данных или обобщить для поиска любых входных данных.

1. Теперь запустите эту программу Q#, чтобы найти элемент с меткой `ReflectAboutMarked`.

### <a name="q-command-line-applications-with-visual-studio-or-visual-studio-code"></a>Приложения командной строки Q# в Visual Studio или Visual Studio Code

Исполняемый файл будет выполнять операцию или функцию, помеченную атрибутом `@EntryPoint()`, в симуляторе или оценщике ресурсов в зависимости от конфигурации проекта и параметров командной строки.

В Visual Studio просто нажмите клавиши CTRL+F5, чтобы выполнить скрипт.

При первом выполнении в VS Code нужно создать файл `Program.qs`. Для этого введите следующую команду в окне терминала:

```Command line
dotnet build
```

Для последующих выполнений его не нужно создавать повторно. Для выполнения введите следующую команду и нажмите клавишу ВВОД:

```Command line
dotnet run --no-build
```

В окне терминала должно появиться следующее сообщение:

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

Это связано с тем, что вы не указали нужное количество кубитов. Поэтому терминал сообщает о командах, доступных для исполняемого файла. Если мы хотим использовать 5 кубитов, нужно ввести следующее:

```Command line
dotnet run --n-qubits 5
```

После нажатия клавиши ВВОД должен отобразиться следующий результат:

```
Reflecting about marked state...
Reflecting about marked state...
Reflecting about marked state...
Reflecting about marked state...
[Zero,One,Zero,One,Zero]
```

## <a name="next-steps"></a>Дальнейшие действия

Если вам понравилось это краткое руководство, воспользуйтесь перечисленными ниже ресурсами, чтобы изучить другие варианты применения Q# для собственных квантовых приложений.

- [Вернуться руководству по началу работы с QDK](xref:microsoft.quantum.welcome)
- Попробуйте изучить более общий алгоритм поиска Гровера из [этого примера](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/database-search).
- [Более подробное знакомство с алгоритмом поиска Гровера в Quantum Katas](xref:microsoft.quantum.overview.katas)
- См. сведения о методике [усиления амплитуды][amplitude-amplification] в квантовых вычислениях, на которой основан алгоритм поиска Гровера.
- [Концепции квантовых вычислений](xref:microsoft.quantum.concepts.intro)
- [Примеры для Quantum Development Kit](https://docs.microsoft.com/samples/browse/?products=qdk)

<!-- LINKS -->

[install]: xref:microsoft.quantum.install
[amplitude-amplification]: xref:microsoft.quantum.libraries.standard.algorithms#amplitude-amplification
