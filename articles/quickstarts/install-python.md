---
title: Разработка на Q# и Python
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.python
ms.openlocfilehash: 7fbbb81b1ee51bff74b287745bf4447004a0254c
ms.sourcegitcommit: a3775921db1dc5c653c97b8fa8fe2c0ddd5261ff
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2020
ms.locfileid: "85885536"
---
# <a name="develop-with-q-and-python"></a>Разработка на Q# и Python

Установите пакет QDK, чтобы разрабатывать основные программы на Python для вызова операций Q#.

## <a name="install-the-qsharp-python-package"></a>Установка пакета Python `qsharp`

### <a name="install-using-conda-recommended"></a>[Установка с помощью conda (рекомендуется)](#tab/tabid-conda)

1. Установите [Miniconda](https://docs.conda.io/en/latest/miniconda.html) или [Anaconda](https://www.anaconda.com/products/individual#Downloads).

1. Откройте командную строку Anaconda.

   - Или же, если вы предпочитаете использовать PowerShell или pwsh, откройте оболочку и выполните команду `conda init powershell`, а затем закройте и повторно откройте оболочку.

1. Создайте и активируйте среду conda с именем `qsharp-env` и необходимыми пакетами (включая Jupyter Notebook и IQ#), выполнив следующие команды:

    ```
    conda create -n qsharp-env -c quantum-engineering qsharp notebook

    conda activate qsharp-env
    ```

1. Выполните команду `python -c "import qsharp"` в том же терминале, чтобы проверить установку и заполнить локальный кэш пакетов всеми необходимыми компонентами QDK.

### <a name="install-using-net-cli-and-pip-advanced"></a>[Установка с помощью .NET CLI и pip (расширенная)](#tab/tabid-dotnetcli)

1. Предварительные требования:

    - [Python](https://www.python.org/downloads/) 3.6 или более поздней версии
    - Диспетчер пакетов Python [PIP](https://pip.pypa.io/en/stable/installing)
    - [Пакет SDK для .NET Core 3.1](https://dotnet.microsoft.com/download/dotnet-core/3.1)


1. Установите `qsharp` — пакет Python, который обеспечивает взаимодействие между Q# и Python.

    ```
    pip install qsharp
    ```

1. Установите IQ# — ядро, которое в основном используется в Jupyter и Python и предоставляет основные функции для компиляции и выполнения операций Q#.

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

Вот и все! Теперь у вас есть пакет Python `qsharp` и ядро IQ# для Jupyter, которое предоставляет основные функции для компиляции и выполнения операций Q# с помощью Python и позволяет использовать записные книжки Jupyter Notebook с Q#.

## <a name="choose-your-ide"></a>Выбор среды IDE

Хотя Q# можно использовать в коде на Python в любой интегрированной среде разработки, мы настоятельно рекомендуем использовать в качестве IDE для приложений на этих двух языках Visual Studio Code (VS Code). С помощью расширения Visual Studio Code для QDK вы можете использовать расширенные возможности, такие как предупреждения, выделение синтаксиса, шаблоны проектов и многое другие.

Если вы хотите использовать VS Code:

- Установите [VS Code](https://code.visualstudio.com/download) (Windows, Linux и Mac).
- Установите [расширение QDK для VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).

Если вы хотите использовать другой редактор, воспользуйтесь инструкциями выше.

## <a name="write-your-first-q-program"></a>Написание первой программы Q#

Теперь вы можете проверить установку пакета Python `qsharp`, создав и выполнив простую программу Q#.

1. Создайте минимальную операцию Q#, создав файл с именем `Operation.qs` и добавив в него следующий код:

    :::code language="qsharp" source="~/quantum/samples/interoperability/qrng/Qrng.qs" range="3-14":::

1. В той же папке, в которой находится файл `Operation.qs`, создайте программу Python с именем `host.py`, чтобы имитировать выполнение операции Q# `SampleQuantumRandomNumberGenerator()`:

    ```python
    import qsharp
    from Qrng import SampleQuantumRandomNumberGenerator

    SampleQuantumRandomNumberGenerator.simulate()
    ```

1. В созданной во время установки среде (т. е. в среде conda или Python, где вы установили `qsharp`) выполните следующую программу:

    ```
    python host.py
    ```

1. Вы должны увидеть результат вызванной операции. В этом случае (так как операция выдает случайный результат) вы увидите на экране `Zero` или `One`. Если выполнять программу повторно, каждый результат будет отображаться примерно в половине случаев.

> [!NOTE]
> * Код Python — это просто обычная программа Python. Вы можете использовать любую среду Python, в т. ч. записные книжки Jupyter Notebook с Python, для написания программы Python и вызова операций Q#. Программа Python может импортировать операции Q# из любых файлов QS, расположенных в той же папке, что и код Python.

## <a name="next-steps"></a>Дальнейшие действия

Установив пакет Quantum Development Kit в используемой вами среде, вы можете выполнить инструкции из этого руководства, чтобы написать и запустить [свою первую квантовую программу](xref:microsoft.quantum.quickstarts.qrng).
