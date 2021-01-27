---
title: Создание квантового генератора случайных чисел
description: Создайте Q# проект, демонстрирующий фундаментальные понятия о такте, такие как "геоположение", создав генератор тактов случайных чисел.
author: bromeg
ms.author: megbrow
ms.date: 10/25/2019
ms.topic: tutorial
uid: microsoft.quantum.quickstarts.qrng
no-loc:
- Q#
- $$v
ms.openlocfilehash: f36db426a8f0479580117cce44a67ad3a053d5de
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856353"
---
# <a name="tutorial-implement-a-quantum-random-number-generator-in-q"></a>Руководство по Реализация квантового генератора случайных чисел на языке Q\#

Простым примером алгоритма такта, написанного на Q# , является генератор тактовых случайных чисел. Этот алгоритм использует природу квантовой механики для получения случайного числа.

## <a name="prerequisites"></a>Предварительные требования

- [Microsoft Quantum Development Kit](xref:microsoft.quantum.install).
- Создайте Q# проект для [ Q# приложения](xref:microsoft.quantum.install.standalone), с [ведущим приложением Python](xref:microsoft.quantum.install.python)или [ведущим приложением C#](xref:microsoft.quantum.install.cs).

## <a name="write-a-no-locq-operation"></a>Запись Q# операции

### <a name="no-locq-operation-code"></a>Q# код операции

1. Замените содержимое файла Program.qs следующим кодом:

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="3-15,34":::

Как упоминалось в статье [Основные сведения о квантовых вычислениях](xref:microsoft.quantum.overview.understanding), кубит представляет собой единицу квантовой информации и может находиться в состоянии суперпозиции. При измерении он всегда возвращает значение 0 или 1. Однако перед измерением состояние кубит представляет вероятность считывания 0 или 1 с помощью измерения. Такое вероятностное состояние называется суперпозицией. Эту вероятность мы можем применить для создания случайных чисел.

В нашей Q# операции мы представляем `Qubit` тип данных Native в Q# . `Qubit` можно выделить инструкцией `using`. Только что выделенный кубит всегда находится в состоянии `Zero`. 

С помощью операции `H` мы можем перевести `Qubit` в состояние суперпозиции. Чтобы измерить кубит, т. е. определить его значение, используется специальная операция `M`.

Каждый раз, когда мы переводим `Qubit` в состояние суперпозиции и измеряем его, мы получаем разные значения.

При отмене выделения `Qubit` необходимо явным образом вернуть ему состояние `Zero`. В противном случае симулятор вернет ошибку при выполнении. Для этого проще всего вызвать `Reset`.

### <a name="visualizing-the-code-with-the-bloch-sphere"></a>Визуализация кода в формате сферы Блоха

В сфере Блоха северный полюс соответствует классическому значению **0**, а южный — классическому значению **1**. Любое состояние суперпозиции обозначается точкой на этой сфере (или стрелкой на схеме). Чем ближе конец этой стрелки к одному из полюсов, тем выше вероятность схлопывания этого кубита при измерении в то классическое состояние, которое соответствует этому полюсу. В примере ниже красная стрелка обозначает состояние с более высокой вероятностью получить значение **0** при измерении кубита.

<img src="~/media/qrng-Bloch.png" width="175" alt="A qubit state with a high probability of measuring zero">

Мы можем использовать это представление для визуализации работы нашего кода.

* Для начала мы инициализируем кубит в состоянии **0** и применим `H`, чтобы создать состояние суперпозиции с равной вероятностью получить значения **0** и **1**.

<img src="~/media/qrng-H.png" width="450" alt="Preparing a qubit in superposition">

* Затем мы измерим состояние кубита и сохраним выходное значение:

<img src="~/media/qrng-meas.png" width="450" alt="Measuring a qubit and saving the output">

Так как исход этого измерения является полностью случайным, можно считать, что мы получили случайный бит. Вызывая эту операцию несколько раз, мы получим большое целое число. Например, три вызова этой операции возвращают три случайных бита, позволяя создать трехбитовое число (т. е. случайное число в диапазоне от 0 до 7).


## <a name="creating-a-complete-random-number-generator"></a>Создание комплексного генератора случайных чисел

Теперь, когда у нас есть Q# операция, создающая случайные биты, мы можем использовать ее для создания полноценного генератора случайных чисел такта. Мы можем использовать Q# приложение или использовать управляющую программу.



### <a name="no-locq-applications-with-visual-studio-or-visual-studio-code"></a>[Q# приложения с Visual Studio или Visual Studio Code](#tab/tabid-qsharp)

Чтобы создать полное Q# приложение, добавьте в программу следующую точку входа Q# : 

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="17-33":::

Программа запустит операцию или функцию, помеченную `@EntryPoint()` атрибутом для симулятора или оценщика ресурсов, в зависимости от конфигурации проекта и параметров командной строки.

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="3-34":::

В Visual Studio просто нажмите клавиши CTRL + F5, чтобы запустить сценарий.

При первом выполнении в VS Code нужно создать файл Program.qs. Для этого введите следующую команду в окне терминала:

```dotnetcli
dotnet build
```

Для последующих выполнений файл не нужно создавать повторно. Для выполнения введите следующую команду и нажмите клавишу ВВОД:

```dotnetcli
dotnet run --no-build
```

### <a name="python-with-visual-studio-code-or-the-command-prompt"></a>[Python с Visual Studio Code или из командной строки](#tab/tabid-python)

Чтобы запустить новую Q# программу из Python, сохраните следующий код `host.py` :

:::code language="python" source="~/quantum/samples/interoperability/qrng/host.py" range="11-30":::

Затем можно запустить ведущее приложение Python из командной строки:

```bash
$ python host.py
Preparing Q# environment...
..The random number generated is 42
```

### <a name="c-with-visual-studio-code-or-visual-studio"></a>[C# с Visual Studio Code или Visual Studio](#tab/tabid-csharp)

Чтобы запустить новую Q# программу из c#, измените, `Driver.cs` включив в нее следующий код c#:

:::code language="csharp" source="~/quantum/samples/interoperability/qrng/Host.cs" range="4-39":::

Затем можно запустить ведущее приложение C# из командной строки (в Visual Studio следует нажать клавишу F5):

```bash
$ dotnet run
The random number generated is 42
```

***
