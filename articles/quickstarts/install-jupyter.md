---
title: Разработка с использованием записных книжек Jupyter Notebook с Q#
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: bbd1f58ba7de205e452be7bac72b5fd78e7acd56
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/21/2020
ms.locfileid: "86871456"
---
# <a name="develop-with-q-jupyter-notebooks"></a>Разработка с использованием записных книжек Jupyter Notebook с Q#

Установите QDK для разработки операций Q# для записных книжек Jupyter Notebook с Q#.

Записные книжки Jupyter Notebook разрешают выполнение кода на месте наряду с инструкциями, примечаниями и другим содержимым. Эта среда идеально подходит для написания кода Q# со встроенными объяснениями или интерактивными учебниками по квантовым вычислениям. Ниже описаны действия, которые помогут вам приступить к созданию собственных записных книжек Q#.

> [!NOTE]
> * При использовании Q# записные книжки Jupyter Notebook позволяют только выполнять код Q#. Вы не можете вызывать операции из внешних основных программ (например, файлов Python или C#). Эта среда не подходит, если вы намерены использовать классическую внешнюю основную программу в сочетании с квантовой программой.

## <a name="install-the-iq-jupyter-kernel"></a>Установка ядра IQ# для Jupyter

IQ# — это расширение, которое в основном используется в Jupyter и Python с пакетом SDK для .NET Core и предоставляет основные функции для компиляции и моделирования операций Q#.

### <a name="install-using-conda-recommended"></a>[Установка с помощью conda (рекомендуется)](#tab/tabid-conda)

1. Установите [Miniconda](https://docs.conda.io/en/latest/miniconda.html) или [Anaconda](https://www.anaconda.com/products/individual#Downloads). **Примечание.** Требуется 64-разрядная установка.

1. Откройте командную строку Anaconda.

   - Или же, если вы предпочитаете использовать PowerShell или pwsh, откройте оболочку и выполните команду `conda init powershell`, а затем закройте и повторно откройте оболочку.

1. Создайте и активируйте среду conda с именем `qsharp-env` и необходимыми пакетами (включая Jupyter Notebook и IQ#), выполнив следующие команды:

    ```
    conda create -n qsharp-env -c quantum-engineering qsharp notebook

    conda activate qsharp-env
    ```

1. Выполните команду `python -c "import qsharp"` в том же терминале, чтобы проверить установку и заполнить локальный кэш пакетов всеми необходимыми компонентами QDK.

### <a name="install-using-net-cli-advanced"></a>[Установка с помощью .NET CLI (расширенная)](#tab/tabid-dotnetcli)

1. Предварительные требования:

    - [Python](https://www.python.org/downloads/) 3.6 или более поздней версии
    - [Записная книжка Jupyter](https://jupyter.readthedocs.io/en/latest/install.html)
    - [Пакет SDK для .NET Core 3.1](https://dotnet.microsoft.com/download/dotnet-core/3.1)

1. Установите пакет `Microsoft.Quantum.IQSharp`.

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > Если на шаге `dotnet iqsharp install` появляется сообщение об ошибке, откройте новое окно терминала и повторите попытку.
    > Если это не поможет, попробуйте найти установленное средство `dotnet-iqsharp` (в Windows это `dotnet-iqsharp.exe`) и воспользуйтесь следующей командой:
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > где `/path/to/dotnet-iqsharp` следует заменить абсолютным путем к средству `dotnet-iqsharp` в вашей файловой системе.
    > Обычно оно находится в `.dotnet/tools` в папке профиля пользователя.
    
***

Вот и все! Теперь у вас есть ядро IQ# для Jupyter, которое предоставляет основные функции для компиляции и выполнения операций Q# из записных книжек Jupyter Notebook с Q#.

## <a name="create-your-first-q-notebook"></a>Создание первой записной книжки с Q#

Теперь вы можете проверить установку Jupyter Notebook с Q#, создав и выполнив простую операцию Q#.

1. В созданной во время установки среде (т. е. в созданной среде conda или Python, где вы установили Jupyter) выполните следующую команду, чтобы запустить сервер Jupyter Notebook:

    ```
    jupyter notebook
    ```

    - Если Jupyter Notebook не открывается автоматически в браузере, скопируйте URL-адрес из командной строки и вставьте его в браузер.

1. Выберите "Создать" → "Q#", чтобы создать записную книжку Jupyter Notebook с ядром Q#, и добавьте следующий код в ее первую ячейку:

    :::code language="qsharp" source="~/quantum/samples/interoperability/qrng/Qrng.qs" range="6-13":::

1. Запустите эту ячейку записной книжки.

    ![Ячейка Jupyter Notebook с кодом Q#](~/media/install-guide-jupyter.png)

    В выходных данных ячейки должно отобразиться `SampleQuantumRandomNumberGenerator`. При запуске в Jupyter Notebook код Q# компилируется, а ячейка выводит имена найденных операций.

1. В новой ячейке выполните только что созданную (в симуляторе) операцию с помощью команды `%simulate`.

    ![Ячейка Jupyter Notebook с магической командой %simulate](~/media/install-guide-jupyter-simulate.png)

    Вы должны увидеть результат вызванной операции. В этом случае (так как операция выдает случайный результат) вы увидите на экране `Zero` или `One`. Если выполнять ячейку повторно, каждый результат будет отображаться примерно в половине случаев.

## <a name="next-steps"></a>Дальнейшие действия

Теперь, когда вы установили QDK для записных книжек Jupyter Notebook c Q#, вы можете написать и запустить [свою первую квантовую программу](xref:microsoft.quantum.quickstarts.qrng), создав код Q# непосредственно в среде Jupyter Notebook.

Воспользуйтесь приведенными ниже ресурсами, чтобы ознакомиться с другими примерами использования записных книжек Jupyter Notebook с Q#.

- [Введение в Q# и Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/). В этой статье приводится пример записной книжки Jupyter Notebook с Q#, чтобы вы могли лучше понять, как использовать Q# в среде Jupyter.
- [Quantum Katas](xref:microsoft.quantum.overview.katas) — коллекция учебников с открытым кодом для обучения в произвольном темпе и наборы упражнений по программированию в виде записных книжек Jupyter Notebook с Q#. [Записные книжки из учебников Quantum Katas](https://github.com/microsoft/QuantumKatas#tutorial-topics) послужат хорошей отправной точкой. Коллекция Quantum Katas предназначена для обучения квантовым вычислениям с одновременным изучением программирования на Q# в произвольном темпе. Это отличный пример того, какого рода содержимое можно создать с помощью записных книжек Jupyter Notebook с Q#.
