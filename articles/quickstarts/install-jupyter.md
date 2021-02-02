---
title: Разработка с использованием записных книжек Jupyter Notebook для Q#
description: Сведения о том, как создавать приложения Q# с помощью записных книжек Jupyter Notebook.
author: bradben
ms.author: v-benbra
ms.date: 8/20/2020
ms.topic: quickstart
uid: microsoft.quantum.install.jupyter
no-loc:
- Q#
- $$v
ms.openlocfilehash: 4cef9b7252a2199b2ea995c4cf819a3582d9ca8f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844284"
---
# <a name="develop-with-q-jupyter-notebooks"></a><span data-ttu-id="cfd22-103">Разработка с использованием записных книжек Jupyter Notebook для Q#</span><span class="sxs-lookup"><span data-stu-id="cfd22-103">Develop with Q# Jupyter Notebooks</span></span>

<span data-ttu-id="cfd22-104">Установите QDK для разработки операций Q# с помощью записных книжек Jupyter Notebook для Q#.</span><span class="sxs-lookup"><span data-stu-id="cfd22-104">Install the QDK for developing Q# operations on Q# Jupyter Notebooks.</span></span>

<span data-ttu-id="cfd22-105">Записные книжки Jupyter Notebook обеспечивают выполнение кода на месте наряду с инструкциями, примечаниями и другим содержимым.</span><span class="sxs-lookup"><span data-stu-id="cfd22-105">Jupyter Notebooks allow running code in-place alongside instructions, notes, and other content.</span></span> <span data-ttu-id="cfd22-106">Эта среда идеально подходит для написания кода Q# со встроенными объяснениями или интерактивными учебниками по квантовым вычислениям.</span><span class="sxs-lookup"><span data-stu-id="cfd22-106">This environment is ideal for writing Q# code with embedded explanations or quantum computing interactive tutorials.</span></span> <span data-ttu-id="cfd22-107">Ниже описаны действия, которые помогут вам приступить к созданию собственных записных книжек Q#.</span><span class="sxs-lookup"><span data-stu-id="cfd22-107">Here's what you need to do to start creating your own Q# notebooks.</span></span>

## <a name="install-the-iq-jupyter-kernel"></a><span data-ttu-id="cfd22-108">Установка ядра IQ# для Jupyter</span><span class="sxs-lookup"><span data-stu-id="cfd22-108">Install the IQ# Jupyter kernel</span></span>

<span data-ttu-id="cfd22-109">IQ# (читается как "ай-кью-шарп") — это расширение, которое в основном используется в Jupyter и Python с пакетом SDK для .NET Core и предоставляет основные функции для компиляции и моделирования операций Q#.</span><span class="sxs-lookup"><span data-stu-id="cfd22-109">IQ# (pronounced i-q-sharp) is an extension primarily used by Jupyter and Python to the .NET Core SDK that provides the core functionality for compiling and simulating Q# operations.</span></span>

### <a name="install-using-conda-recommended"></a>[<span data-ttu-id="cfd22-110">Установка с помощью conda (рекомендуется)</span><span class="sxs-lookup"><span data-stu-id="cfd22-110">Install using conda (recommended)</span></span>](#tab/tabid-conda)

1. <span data-ttu-id="cfd22-111">Установите [Miniconda](https://docs.conda.io/en/latest/miniconda.html) или [Anaconda](https://www.anaconda.com/products/individual#Downloads).</span><span class="sxs-lookup"><span data-stu-id="cfd22-111">Install [Miniconda](https://docs.conda.io/en/latest/miniconda.html) or [Anaconda](https://www.anaconda.com/products/individual#Downloads).</span></span> <span data-ttu-id="cfd22-112">**Примечание.** Требуется 64-разрядная установка.</span><span class="sxs-lookup"><span data-stu-id="cfd22-112">**Note:** 64-bit installation required.</span></span>

1. <span data-ttu-id="cfd22-113">Откройте командную строку Anaconda.</span><span class="sxs-lookup"><span data-stu-id="cfd22-113">Open an Anaconda Prompt.</span></span>

   - <span data-ttu-id="cfd22-114">Или же, если вы предпочитаете использовать PowerShell или pwsh, откройте оболочку и выполните команду `conda init powershell`, а затем закройте и повторно откройте оболочку.</span><span class="sxs-lookup"><span data-stu-id="cfd22-114">Or, if you prefer to use PowerShell or pwsh: open a shell, run `conda init powershell`, then close and re-open the shell.</span></span>

1. <span data-ttu-id="cfd22-115">Создайте и активируйте среду conda с именем `qsharp-env` и необходимыми пакетами (включая Jupyter Notebook и IQ#), выполнив следующие команды:</span><span class="sxs-lookup"><span data-stu-id="cfd22-115">Create and activate a new conda environment named `qsharp-env` with the required packages (including Jupyter Notebook and IQ#) by running the following commands:</span></span>

    ```
    conda create -n qsharp-env -c quantum-engineering qsharp notebook

    conda activate qsharp-env
    ```

1. <span data-ttu-id="cfd22-116">Выполните команду `python -c "import qsharp"` в том же терминале, чтобы проверить установку и заполнить локальный кэш пакетов всеми необходимыми компонентами QDK.</span><span class="sxs-lookup"><span data-stu-id="cfd22-116">Run `python -c "import qsharp"` from the same terminal to verify your installation and populate your local package cache with all required QDK components.</span></span>

### <a name="install-using-net-cli-advanced"></a>[<span data-ttu-id="cfd22-117">Установка с помощью .NET CLI (расширенная)</span><span class="sxs-lookup"><span data-stu-id="cfd22-117">Install using .NET CLI (advanced)</span></span>](#tab/tabid-dotnetcli)

1. <span data-ttu-id="cfd22-118">Предварительные требования:</span><span class="sxs-lookup"><span data-stu-id="cfd22-118">Prerequisites:</span></span>

    - <span data-ttu-id="cfd22-119">[Python](https://www.python.org/downloads/) 3.6 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="cfd22-119">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - [<span data-ttu-id="cfd22-120">Записная книжка Jupyter</span><span class="sxs-lookup"><span data-stu-id="cfd22-120">Jupyter Notebook</span></span>](https://jupyter.readthedocs.io/en/latest/install.html)
    - [<span data-ttu-id="cfd22-121">Пакет SDK для .NET Core 3.1</span><span class="sxs-lookup"><span data-stu-id="cfd22-121">.NET Core SDK 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)

1. <span data-ttu-id="cfd22-122">Установите пакет `Microsoft.Quantum.IQSharp`.</span><span class="sxs-lookup"><span data-stu-id="cfd22-122">Install the `Microsoft.Quantum.IQSharp` package.</span></span>

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

> [!NOTE]
> <span data-ttu-id="cfd22-123">Если на шаге `dotnet iqsharp install` появляется сообщение об ошибке, откройте новое окно терминала и повторите попытку.</span><span class="sxs-lookup"><span data-stu-id="cfd22-123">If you get an error during the `dotnet iqsharp install` step, open a new terminal window and try again.</span></span>
> <span data-ttu-id="cfd22-124">Если это не поможет, попробуйте найти установленное средство `dotnet-iqsharp` (в Windows это `dotnet-iqsharp.exe`) и воспользуйтесь следующей командой:</span><span class="sxs-lookup"><span data-stu-id="cfd22-124">If this still doesn't work, try locating the installed `dotnet-iqsharp` tool (on Windows, `dotnet-iqsharp.exe`) and running:</span></span>
> ```
> /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
> ```
> <span data-ttu-id="cfd22-125">где `/path/to/dotnet-iqsharp` следует заменить абсолютным путем к средству `dotnet-iqsharp` в вашей файловой системе.</span><span class="sxs-lookup"><span data-stu-id="cfd22-125">where `/path/to/dotnet-iqsharp` should be replaced by the absolute path to the `dotnet-iqsharp` tool in your file system.</span></span>
> <span data-ttu-id="cfd22-126">Обычно оно находится в `.dotnet/tools` в папке профиля пользователя.</span><span class="sxs-lookup"><span data-stu-id="cfd22-126">Typically this will be under `.dotnet/tools` in your user profile folder.</span></span>
    
<span data-ttu-id="cfd22-127">\*\*_</span><span class="sxs-lookup"><span data-stu-id="cfd22-127">\*\*_</span></span>

<span data-ttu-id="cfd22-128">Вот и все!</span><span class="sxs-lookup"><span data-stu-id="cfd22-128">That's it!</span></span> <span data-ttu-id="cfd22-129">Теперь у вас есть ядро IQ# для Jupyter, которое предоставляет основные функции для компиляции и выполнения операций Q# из записных книжек Jupyter Notebook для Q#.</span><span class="sxs-lookup"><span data-stu-id="cfd22-129">You now have the IQ# kernel for Jupyter, which provides the core functionality for compiling and running Q# operations from Q# Jupyter Notebooks.</span></span>

## <a name="create-your-first-q-notebook"></a><span data-ttu-id="cfd22-130">Создание первой записной книжки для Q#</span><span class="sxs-lookup"><span data-stu-id="cfd22-130">Create your first Q# notebook</span></span>

<span data-ttu-id="cfd22-131">Теперь вы можете проверить установку Jupyter Notebook для Q#, создав и выполнив простую операцию Q#.</span><span class="sxs-lookup"><span data-stu-id="cfd22-131">Now you are ready to verify your Q# Jupyter Notebook installation by writing and running a simple Q# operation.</span></span>

1. <span data-ttu-id="cfd22-132">В созданной во время установки среде (т. е. в созданной среде conda или Python, где вы установили Jupyter) выполните следующую команду, чтобы запустить сервер Jupyter Notebook:</span><span class="sxs-lookup"><span data-stu-id="cfd22-132">From the environment you created during installation (i.e., either the conda environment you created, or the Python environment where you installed Jupyter), run the following command to start the Jupyter Notebook server:</span></span>

    ```
    jupyter notebook
    ```

    - <span data-ttu-id="cfd22-133">Если Jupyter Notebook не открывается автоматически в браузере, скопируйте URL-адрес из командной строки и вставьте его в браузер.</span><span class="sxs-lookup"><span data-stu-id="cfd22-133">If the Jupyter Notebook doesn't open automatically in your browser, copy and paste the URL provided by the command line into your browser.</span></span>

1. <span data-ttu-id="cfd22-134">Выберите *New → Q#* (Создать → Q#), чтобы создать записную книжку Jupyter Notebook с ядром Q#, и добавьте следующий код в ее первую ячейку:</span><span class="sxs-lookup"><span data-stu-id="cfd22-134">Choose _ *New → Q#*\* to create a Jupyter Notebook with a Q# kernel, and add the following code to the first notebook cell:</span></span>

    :::code language="qsharp" source="~/quantum/samples/interoperability/qrng/Qrng.qs" range="6-13":::

1. <span data-ttu-id="cfd22-135">Запустите эту ячейку записной книжки.</span><span class="sxs-lookup"><span data-stu-id="cfd22-135">Run this cell of the notebook:</span></span>

    ![Ячейка Jupyter Notebook с кодом Q#](~/media/install-guide-jupyter.png)

    <span data-ttu-id="cfd22-137">В выходных данных ячейки должно отобразиться `SampleQuantumRandomNumberGenerator`.</span><span class="sxs-lookup"><span data-stu-id="cfd22-137">You should see `SampleQuantumRandomNumberGenerator` in the output of the cell.</span></span> <span data-ttu-id="cfd22-138">При запуске в Jupyter Notebook код Q# компилируется, а ячейка выводит имена найденных операций.</span><span class="sxs-lookup"><span data-stu-id="cfd22-138">When running in Jupyter Notebook, the Q# code is compiled, and the cell outputs the name of any operations that it finds.</span></span>

1. <span data-ttu-id="cfd22-139">В новой ячейке выполните только что созданную (в симуляторе) операцию с помощью команды `%simulate`.</span><span class="sxs-lookup"><span data-stu-id="cfd22-139">In a new cell, run the operation you just created (in a simulator) by using the `%simulate` command:</span></span>

    ![Ячейка Jupyter Notebook с магической командой %simulate](~/media/install-guide-jupyter-simulate.png)

    <span data-ttu-id="cfd22-141">Вы должны увидеть результат вызванной операции.</span><span class="sxs-lookup"><span data-stu-id="cfd22-141">You should see the result of the operation you invoked.</span></span> <span data-ttu-id="cfd22-142">В этом случае (так как операция выдает случайный результат) вы увидите на экране `Zero` или `One`.</span><span class="sxs-lookup"><span data-stu-id="cfd22-142">In this case, because your operation generates a random result, you will see either `Zero` or `One` printed on the screen.</span></span> <span data-ttu-id="cfd22-143">Если выполнять ячейку повторно, каждый результат будет отображаться примерно в половине случаев.</span><span class="sxs-lookup"><span data-stu-id="cfd22-143">If you run the cell repeatedly, you should see each result approximately half the time.</span></span>

## <a name="next-steps"></a><span data-ttu-id="cfd22-144">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="cfd22-144">Next steps</span></span>

<span data-ttu-id="cfd22-145">Теперь, когда вы установили QDK для записных книжек Jupyter Notebook для Q#, вы можете написать и запустить [свою первую квантовую программу](xref:microsoft.quantum.quickstarts.qrng), создав код Q# непосредственно в среде Jupyter Notebook.</span><span class="sxs-lookup"><span data-stu-id="cfd22-145">Now that you have installed the QDK for Q# Jupyter Notebooks, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng) by writing Q# code directly within the Jupyter Notebook environment.</span></span>

<span data-ttu-id="cfd22-146">Воспользуйтесь приведенными ниже ресурсами, чтобы ознакомиться с другими примерами использования записных книжек Jupyter Notebook для Q#:</span><span class="sxs-lookup"><span data-stu-id="cfd22-146">For more examples of what you can do with Q# Jupyter Notebooks, please take a look at:</span></span>

- <span data-ttu-id="cfd22-147">[Введение в Q# и Jupyter Notebook.](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/)</span><span class="sxs-lookup"><span data-stu-id="cfd22-147">[Intro to Q# and Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/).</span></span> <span data-ttu-id="cfd22-148">В этой статье приводится пример записной книжки Jupyter Notebook для Q#, чтобы вы могли лучше понять, как использовать Q# в среде Jupyter.</span><span class="sxs-lookup"><span data-stu-id="cfd22-148">There you will find a Q# Jupyter Notebook that provides more details on how to use Q# in the Jupyter environment.</span></span>
- <span data-ttu-id="cfd22-149">[Quantum Katas](xref:microsoft.quantum.overview.katas) — коллекция учебников с открытым кодом для обучения в произвольном темпе и наборы упражнений по программированию в виде записных книжек Jupyter Notebook для Q#.</span><span class="sxs-lookup"><span data-stu-id="cfd22-149">[Quantum Katas](xref:microsoft.quantum.overview.katas), an open-source collection of self-paced tutorials and sets of programming exercises in the form of Q# Jupyter Notebooks.</span></span> <span data-ttu-id="cfd22-150">[Записные книжки из учебников Quantum Katas](https://github.com/microsoft/QuantumKatas#tutorial-topics) послужат хорошей отправной точкой.</span><span class="sxs-lookup"><span data-stu-id="cfd22-150">The [Quantum Katas tutorial notebooks](https://github.com/microsoft/QuantumKatas#tutorial-topics) are a good starting point.</span></span> <span data-ttu-id="cfd22-151">Коллекция Quantum Katas предназначена для обучения квантовым вычислениям с одновременным изучением программирования на Q#.</span><span class="sxs-lookup"><span data-stu-id="cfd22-151">The Quantum Katas are aimed at teaching you elements of quantum computing and Q# programming at the same time.</span></span> <span data-ttu-id="cfd22-152">Это отличный пример того, какого рода содержимое можно создать с помощью записных книжек Jupyter Notebook для Q#.</span><span class="sxs-lookup"><span data-stu-id="cfd22-152">They're an excellent example of what kind of content you can create with Q# Jupyter Notebooks.</span></span>
