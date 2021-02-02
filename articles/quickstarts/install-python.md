---
title: Разработка на Q# и Python
description: Узнайте, как создавать приложения Q# с помощью Python.
author: bradben
ms.author: v-benbra
ms.date: 8/20/2020
ms.topic: quickstart
uid: microsoft.quantum.install.python
no-loc:
- Q#
- $$v
ms.openlocfilehash: 1ec40b6f1b7a8d9144860e3b8cfd554eb51bae81
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844269"
---
# <a name="develop-with-q-and-python"></a><span data-ttu-id="17e2c-103">Разработка на Q# и Python</span><span class="sxs-lookup"><span data-stu-id="17e2c-103">Develop with Q# and Python</span></span>

<span data-ttu-id="17e2c-104">Установите пакет QDK, чтобы разрабатывать ведущие программы на Python для вызова операций Q#.</span><span class="sxs-lookup"><span data-stu-id="17e2c-104">Install the QDK to develop Python host programs to call Q# operations.</span></span>

## <a name="install-the-qsharp-python-package"></a><span data-ttu-id="17e2c-105">Установка пакета Python `qsharp`</span><span class="sxs-lookup"><span data-stu-id="17e2c-105">Install the `qsharp` Python package</span></span>

### <a name="install-using-conda-recommended"></a>[<span data-ttu-id="17e2c-106">Установка с помощью conda (рекомендуется)</span><span class="sxs-lookup"><span data-stu-id="17e2c-106">Install using conda (recommended)</span></span>](#tab/tabid-conda)

1. <span data-ttu-id="17e2c-107">Установите [Miniconda](https://docs.conda.io/en/latest/miniconda.html) или [Anaconda](https://www.anaconda.com/products/individual#Downloads).</span><span class="sxs-lookup"><span data-stu-id="17e2c-107">Install [Miniconda](https://docs.conda.io/en/latest/miniconda.html) or [Anaconda](https://www.anaconda.com/products/individual#Downloads).</span></span> <span data-ttu-id="17e2c-108">**Примечание.** Требуется 64-разрядная установка.</span><span class="sxs-lookup"><span data-stu-id="17e2c-108">**Note:** 64-bit installation required.</span></span>

1. <span data-ttu-id="17e2c-109">Откройте командную строку Anaconda.</span><span class="sxs-lookup"><span data-stu-id="17e2c-109">Open an Anaconda Prompt.</span></span>

   - <span data-ttu-id="17e2c-110">Или же, если вы предпочитаете использовать PowerShell или pwsh, откройте оболочку и выполните команду `conda init powershell`, а затем закройте и повторно откройте оболочку.</span><span class="sxs-lookup"><span data-stu-id="17e2c-110">Or, if you prefer to use PowerShell or pwsh: open a shell, run `conda init powershell`, then close and re-open the shell.</span></span>

1. <span data-ttu-id="17e2c-111">Создайте и активируйте среду conda с именем `qsharp-env` и необходимыми пакетами (включая Jupyter Notebook и IQ#), выполнив следующие команды:</span><span class="sxs-lookup"><span data-stu-id="17e2c-111">Create and activate a new conda environment named `qsharp-env` with the required packages (including Jupyter Notebook and IQ#) by running the following commands:</span></span>

    ```
    conda create -n qsharp-env -c quantum-engineering qsharp notebook

    conda activate qsharp-env
    ```

1. <span data-ttu-id="17e2c-112">Выполните команду `python -c "import qsharp"` в том же терминале, чтобы проверить установку и заполнить локальный кэш пакетов всеми необходимыми компонентами QDK.</span><span class="sxs-lookup"><span data-stu-id="17e2c-112">Run `python -c "import qsharp"` from the same terminal to verify your installation and populate your local package cache with all required QDK components.</span></span>

### <a name="install-using-net-cli-and-pip-advanced"></a>[<span data-ttu-id="17e2c-113">Установка с помощью .NET CLI и pip (расширенная)</span><span class="sxs-lookup"><span data-stu-id="17e2c-113">Install using .NET CLI and pip (advanced)</span></span>](#tab/tabid-dotnetcli)

1. <span data-ttu-id="17e2c-114">Предварительные требования:</span><span class="sxs-lookup"><span data-stu-id="17e2c-114">Prerequisites:</span></span>

    - <span data-ttu-id="17e2c-115">[Python](https://www.python.org/downloads/) 3.6 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="17e2c-115">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - <span data-ttu-id="17e2c-116">Диспетчер пакетов Python [PIP](https://pip.pypa.io/en/stable/installing)</span><span class="sxs-lookup"><span data-stu-id="17e2c-116">The [PIP](https://pip.pypa.io/en/stable/installing) Python package manager</span></span>
    - [<span data-ttu-id="17e2c-117">Пакет SDK для .NET Core 3.1</span><span class="sxs-lookup"><span data-stu-id="17e2c-117">.NET Core SDK 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)


1. <span data-ttu-id="17e2c-118">Установите `qsharp` — пакет Python, который обеспечивает взаимодействие между Q# и Python.</span><span class="sxs-lookup"><span data-stu-id="17e2c-118">Install the `qsharp` package, a Python package that enables interop between Q# and Python.</span></span>

    ```
    pip install qsharp
    ```

1. <span data-ttu-id="17e2c-119">Установите IQ# — ядро, которое используется в Jupyter и Python и предоставляет основные функции для компиляции и выполнения операций Q#.</span><span class="sxs-lookup"><span data-stu-id="17e2c-119">Install IQ#, a kernel used by Jupyter and Python that provides the core functionality for compiling and running Q# operations.</span></span>

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > <span data-ttu-id="17e2c-120">Если на шаге `dotnet iqsharp install` появляется сообщение об ошибке, откройте новое окно терминала и повторите попытку.</span><span class="sxs-lookup"><span data-stu-id="17e2c-120">If you get an error during the `dotnet iqsharp install` step, open a new terminal window and try again.</span></span>
    > <span data-ttu-id="17e2c-121">Если это не поможет, попробуйте найти установленное средство `dotnet-iqsharp` (в Windows это `dotnet-iqsharp.exe`) и воспользуйтесь следующей командой:</span><span class="sxs-lookup"><span data-stu-id="17e2c-121">If this still doesn't work, try locating the installed `dotnet-iqsharp` tool (on Windows, `dotnet-iqsharp.exe`) and running:</span></span>
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > <span data-ttu-id="17e2c-122">где `/path/to/dotnet-iqsharp` следует заменить абсолютным путем к средству `dotnet-iqsharp` в вашей файловой системе.</span><span class="sxs-lookup"><span data-stu-id="17e2c-122">where `/path/to/dotnet-iqsharp` should be replaced by the absolute path to the `dotnet-iqsharp` tool in your file system.</span></span>
    > <span data-ttu-id="17e2c-123">Обычно оно находится в `.dotnet/tools` в папке профиля пользователя.</span><span class="sxs-lookup"><span data-stu-id="17e2c-123">Typically this will be under `.dotnet/tools` in your user profile folder.</span></span>
    
<span data-ttu-id="17e2c-124">\*\*_</span><span class="sxs-lookup"><span data-stu-id="17e2c-124">\*\*_</span></span>

<span data-ttu-id="17e2c-125">Вот и все!</span><span class="sxs-lookup"><span data-stu-id="17e2c-125">That's it!</span></span> <span data-ttu-id="17e2c-126">Теперь у вас есть пакет Python `qsharp` и ядро IQ# для Jupyter, которое предоставляет основные функции для компиляции и выполнения операций Q# с помощью Python и позволяет применять записные книжки Jupyter Notebook для Q#.</span><span class="sxs-lookup"><span data-stu-id="17e2c-126">You now have both the `qsharp` Python package and the IQ# kernel for Jupyter, which provide the core functionality for compiling and running Q# operations from Python and allows you to use Q# Jupyter Notebooks.</span></span>

## <a name="choose-your-ide"></a><span data-ttu-id="17e2c-127">Выбор среды IDE</span><span class="sxs-lookup"><span data-stu-id="17e2c-127">Choose your IDE</span></span>

<span data-ttu-id="17e2c-128">Хотя Q# можно использовать в коде на Python в любой интегрированной среде разработки, мы настоятельно рекомендуем использовать в качестве IDE для приложений на этих двух языках (Python и Q#) Visual Studio Code (VS Code).</span><span class="sxs-lookup"><span data-stu-id="17e2c-128">While you can use Q# with Python in any IDE, we highly recommend using Visual Studio Code (VS Code) IDE for your Q# + Python applications.</span></span> <span data-ttu-id="17e2c-129">С помощью расширения Visual Studio Code для QDK вы можете использовать расширенные возможности, такие как предупреждения, выделение синтаксиса, шаблоны проектов и многое другие.</span><span class="sxs-lookup"><span data-stu-id="17e2c-129">With the QDK Visual Studio Code extension you gain access to richer functionality such as warnings, syntax highlighting, project templates, and more.</span></span>

<span data-ttu-id="17e2c-130">Если вы хотите использовать VS Code:</span><span class="sxs-lookup"><span data-stu-id="17e2c-130">If you would like to use VS Code:</span></span>

- <span data-ttu-id="17e2c-131">Установите [VS Code](https://code.visualstudio.com/download) (Windows, Linux и Mac).</span><span class="sxs-lookup"><span data-stu-id="17e2c-131">Install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac).</span></span>
- <span data-ttu-id="17e2c-132">Установите [расширение QDK для VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="17e2c-132">Install the [QDK extension for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

<span data-ttu-id="17e2c-133">Если вы хотите использовать другой редактор, воспользуйтесь инструкциями выше.</span><span class="sxs-lookup"><span data-stu-id="17e2c-133">If you would like to use a different editor, the instructions above have you all set.</span></span>

## <a name="write-your-first-q-program"></a><span data-ttu-id="17e2c-134">Написание первой программы на Q#</span><span class="sxs-lookup"><span data-stu-id="17e2c-134">Write your first Q# program</span></span>

<span data-ttu-id="17e2c-135">Теперь вы можете проверить установку пакета Python `qsharp`, создав и выполнив простую программу Q#.</span><span class="sxs-lookup"><span data-stu-id="17e2c-135">Now you are ready to verify your `qsharp` Python package installation by writing and running a simple Q# program.</span></span>

1. <span data-ttu-id="17e2c-136">Создайте минимальную операцию Q#, создав файл с именем `Operation.qs` и добавив в него следующий код:</span><span class="sxs-lookup"><span data-stu-id="17e2c-136">Create a minimal Q# operation by creating a file called `Operation.qs` and adding the following code to it:</span></span>

    :::code language="qsharp" source="~/quantum/samples/interoperability/qrng/Qrng.qs" range="3-14":::

1. <span data-ttu-id="17e2c-137">В той же папке, в которой находится файл `Operation.qs`, создайте программу Python с именем `host.py`, чтобы имитировать выполнение операции Q# Q# `SampleQuantumRandomNumberGenerator()`:</span><span class="sxs-lookup"><span data-stu-id="17e2c-137">In the same folder as `Operation.qs`, create a Python program called `host.py` to simulate the Q# `SampleQuantumRandomNumberGenerator()` operation:</span></span>

    ```python
    import qsharp
    from Qrng import SampleQuantumRandomNumberGenerator

    print(SampleQuantumRandomNumberGenerator.simulate())
    ```

1. <span data-ttu-id="17e2c-138">В созданной во время установки среде (т. е. в среде conda или Python, где вы установили `qsharp`) выполните следующую программу:</span><span class="sxs-lookup"><span data-stu-id="17e2c-138">From the environment you created during installation (i.e., the conda or Python environment where you installed `qsharp`), run the program:</span></span>

    ```
    python host.py
    ```

1. <span data-ttu-id="17e2c-139">Вы должны увидеть результат вызванной операции.</span><span class="sxs-lookup"><span data-stu-id="17e2c-139">You should see the result of the operation you invoked.</span></span> <span data-ttu-id="17e2c-140">В этом случае (так как операция выдает случайный результат) вы увидите на экране `0` или `1`.</span><span class="sxs-lookup"><span data-stu-id="17e2c-140">In this case, because your operation generates a random result, you will see either `0` or `1` printed on the screen.</span></span> <span data-ttu-id="17e2c-141">Если выполнять программу повторно, каждый результат будет отображаться примерно в половине случаев.</span><span class="sxs-lookup"><span data-stu-id="17e2c-141">If you run the program repeatedly, you should see each result approximately half the time.</span></span>

> [!NOTE]
> <span data-ttu-id="17e2c-142">_ Код Python — это просто обычная программа Python.</span><span class="sxs-lookup"><span data-stu-id="17e2c-142">_ The Python code is just a normal Python program.</span></span> <span data-ttu-id="17e2c-143">Вы можете использовать любую среду Python, в т. ч. записные книжки Jupyter Notebook для Python, для написания программы Python и вызова операций Q#.</span><span class="sxs-lookup"><span data-stu-id="17e2c-143">You can use any Python environment, including Python-based Jupyter Notebooks, to write the Python program and call Q# operations.</span></span> <span data-ttu-id="17e2c-144">Программа Python может импортировать операции Q# из любых файлов QS, расположенных в той же папке, что и код Python.</span><span class="sxs-lookup"><span data-stu-id="17e2c-144">The Python program can import Q# operations from any .qs files located in the same folder as the Python code itself.</span></span>

## <a name="next-steps"></a><span data-ttu-id="17e2c-145">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="17e2c-145">Next steps</span></span>

<span data-ttu-id="17e2c-146">Протестировав работу пакета средств разработки Quantum в используемой вами среде, вы можете выполнить инструкции из этого руководства, чтобы написать и запустить [свою первую квантовую программу](xref:microsoft.quantum.quickstarts.qrng).</span><span class="sxs-lookup"><span data-stu-id="17e2c-146">Now that you have tested the Quantum Development Kit in your preferred environment, you can follow this tutorial to write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
