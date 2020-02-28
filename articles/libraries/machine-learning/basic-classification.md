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
# <a name="basic-classification-classify-data-with-the-qdk"></a>Простая классификация: классификация данных с помощью КДК

В этом кратком руководстве вы узнаете, как выполнить последовательное классификатор, написанный в Q #, используя Машинное обучение библиотеку тактовой частоты для КДК. 

В этом пошаговом окне мы будем использовать набор данных половинной Луны, используя структуру классификатора, определенную в Q #.

## <a name="prerequisites"></a>предварительные требования

- [Microsoft Quantum Development Kit](xref:microsoft.quantum.install).
- [Создание проекта Q#](xref:microsoft.quantum.howto.createproject)

## <a name="host-program"></a>Ведущее приложение

Программа размещения состоит из трех частей:

- Загрузите набор данных и выберите набор параметров запуска для модели.
- Выполните обучение, чтобы определить параметры и сдвиг модели.
- Проверка модели для определения ее точности

    ### <a name="python-with-visual-studio-code-or-the-command-line"></a>[Вызов Python из Visual Studio Code или командной строки](#tab/tabid-python)

    Чтобы запустить из Python классификатор Q #, сохраните следующий код как `host.py`. Помните, что вам также потребуется файл Q # `Training.qs`, который объясняется далее в этом руководстве.

    :::code language="python" source="~/quantum/samples/machine-learning/half-moons/host.py" range="3-42":::

    Теперь вы сможете запустить основную программу Python из командной строки следующим образом:

    ```bash
    $ python host.py
    Preparing Q# environment...
    [...]
    Observed X.XX% misclassifications.
    ```

    ### <a name="c-with-visual-studio-code-or-the-command-line"></a>[Вызов C# из Visual Studio Code или командной строки](#tab/tabid-csharp)

    Чтобы запустить, что вы являетесь классификатором Q # C#из, сохраните следующий код как `Host.cs`. Помните, что вам также потребуется файл Q # `Training.qs`, который объясняется далее в этом руководстве.

    :::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="4-86":::

    Теперь вы сможете запустить основную программу C# из командной строки следующим образом:

    ```bash
    $ dotnet run
    [...]
    Observed X.XX% misclassifications.
    ```

    ### <a name="c-with-visual-studio-2019"></a>[Вызов C# из Visual Studio 2019](#tab/tabid-vs2019)

    Чтобы запустить новую программу Q # из C# в Visual Studio, измените `Host.cs`, включив в него следующий C# код. Помните, что вам также потребуется файл Q # `Training.qs`, который объясняется далее в этом руководстве.

    :::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="4-86":::

    Затем нажмите клавишу F5, чтобы запустить программу. Вы увидите новое всплывающее окно со следующими результатами: 

    ```bash
    $ dotnet run
    [...]
    Observed X.XX% misclassifications.
    ```
    ***

## <a name="q-classifier-code"></a>Q\# код классификатора

Теперь давайте посмотрим, как операции, вызываемые ведущим приложением, определяются в Q #.
Мы сохраняем следующий код в файле с именем `Training.qs`.

:::code language="qsharp" source="~/quantum/samples/machine-learning/half-moons/Training.qs" range="4-116":::

Наиболее важными функциями и операциями, определенными в приведенном выше коде, являются:

- `ClassifierStructure() : ControlledRotation[]`. в этой функции мы устанавливаем структуру модели канала, добавляя уровни контролируемого шлюза, который мы будем рассматривать. Этот шаг аналогичен объявлению уровней нейронов в последовательной модели глубокого обучения.
- `TrainHalfMoonModel() : TrainWineModel() : (Double[], Double)`: Эта операция является основной частью кода и определяет обучение. Здесь мы загружаем образцы из набора данных, входящего в библиотеку, мы устанавливаем параметры Hyper и начальные параметры для обучения, а также начнем обучение, вызвав операцию `TrainSequentialClassifier`, которая включена в библиотеку. Он выводит параметры и сдвиг, определяющие классификатор.
- `ValidateHalfMoonModel(parameters : Double[], bias : Double) : Int`: Эта операция определяет процесс проверки для оценки модели. Здесь мы загружаем примеры для проверки, количество измерений на выборку и допуск. Он выводит количество неправильной классификации для выбранного пакета выборки для проверки.

## <a name="next-steps"></a>Дальнейшие действия

Во первых, вы можете поэкспериментировать с кодом и попробовать изменить некоторые параметры, чтобы увидеть, как он влияет на обучение. Затем, в следующем руководстве, [Создайте свой собственный классификатор](xref:microsoft.quantum.libraries.machine-learning.design), вы узнаете, как определить структуру классификатора.
