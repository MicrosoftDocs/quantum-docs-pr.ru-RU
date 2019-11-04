---
title: Сведения об установке Microsoft Quantum Development Kit (QDK)
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: 2a098d89f13278d7137bf182a184a74afb9393be
ms.sourcegitcommit: 2ca4755d1a63431e3cb2d2918a10ad477ec2e368
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2019
ms.locfileid: "73462869"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="9e7c9-102">Установка Microsoft Quantum Development Kit (QDK)</span><span class="sxs-lookup"><span data-stu-id="9e7c9-102">Install the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="9e7c9-103">Узнайте, как установить Microsoft Quantum Development Kit (QDK), чтобы приступить к работе с квантовым программированием.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-103">Learn how to install the Microsoft Quantum Development Kit (QDK), so that you can get started with quantum programming.</span></span> <span data-ttu-id="9e7c9-104">QDK состоит из следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="9e7c9-104">The QDK consists of:</span></span>

- <span data-ttu-id="9e7c9-105">язык программирования Q#;</span><span class="sxs-lookup"><span data-stu-id="9e7c9-105">the Q# programming language</span></span>
- <span data-ttu-id="9e7c9-106">набор библиотек, абстрагирующих сложные функции в Q#;</span><span class="sxs-lookup"><span data-stu-id="9e7c9-106">a set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="9e7c9-107">ведущее приложение (написанное на языке Python или .NET), которое запускает квантовые операции, написанные на языке Q#;</span><span class="sxs-lookup"><span data-stu-id="9e7c9-107">a host application (written in Python or a .NET language) that runs quantum operations written in Q#</span></span>
- <span data-ttu-id="9e7c9-108">средства для упрощения разработки.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-108">tools to facilitate your development</span></span>

<span data-ttu-id="9e7c9-109">Этапы установки различаются в зависимости от выбранной среды разработки.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-109">Depending on your chosen development environment, there are different installation steps.</span></span> <span data-ttu-id="9e7c9-110">Выберите среду из следующих разделов.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-110">Choose your environment from the sections below.</span></span>

## <a name="develop-with-python"></a><span data-ttu-id="9e7c9-111">Разработка на языке Python</span><span class="sxs-lookup"><span data-stu-id="9e7c9-111">Develop with Python</span></span>

<span data-ttu-id="9e7c9-112">Пакет Q# для Python позволяет легко моделировать операции и функции Q# в Python.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-112">The qsharp package for Python makes it easy to simulate Q# operations and functions from within Python.</span></span> <span data-ttu-id="9e7c9-113">IQ# — это расширение, которое в основном используется в Jupyter и Python и предоставляет основные функции для компиляции и моделирования операций Q#.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-113">IQ# (pronounced i-q-sharp) is an extension primarily used by Jupyter and Python that provides the core functionality for compiling and simulating Q# operations.</span></span>

1. <span data-ttu-id="9e7c9-114">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="9e7c9-114">Pre-requisites</span></span>

    - <span data-ttu-id="9e7c9-115">[Python](https://www.python.org/downloads/) 3.6 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="9e7c9-115">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - <span data-ttu-id="9e7c9-116">Диспетчер пакетов Python [PIP](https://pip.pypa.io/en/stable/installing)</span><span class="sxs-lookup"><span data-stu-id="9e7c9-116">The [PIP](https://pip.pypa.io/en/stable/installing) Python package manager</span></span>
    - [<span data-ttu-id="9e7c9-117">Пакет SDK для .NET Core 3.0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="9e7c9-117">.NET Core SDK 3.0 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="9e7c9-118">Установите пакет `iqsharp`.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-118">Install the `iqsharp` package</span></span>

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="9e7c9-119">Установите пакет `qsharp`.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-119">Install the `qsharp` package</span></span>

    ```bash
    pip install qsharp
    ```

1. <span data-ttu-id="9e7c9-120">Проверьте установку, создав приложение `Hello World`.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-120">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="9e7c9-121">Создайте минимальную операцию Q#, создав файл с именем `Operation.qs` и добавив в него следующий код.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-121">Create a minimal Q# operation, by creating a file called `Operation.qs`, and adding the following code to it:</span></span>

        ```qsharp
        namespace HelloWorld
        {
            open Microsoft.Quantum.Intrinsic;
            open Microsoft.Quantum.Canon;

            operation SayHello() : Result {
                Message("Hello from quantum world!");
                return Zero;
            }
        }
        ```

    - <span data-ttu-id="9e7c9-122">Создайте программу Python с именем `hello_world.py` для вызова операции `SayHello()` Q#.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-122">Create a Python program called `hello_world.py` to call the Q# `SayHello()` operation:</span></span>

        ```python
        import qsharp

        from HelloWorld import SayHello

        SayHello.simulate()
        ```

    - <span data-ttu-id="9e7c9-123">Запустите программу.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-123">Run the program:</span></span>

        ```bash
        python hello_world.py
        ```

    - <span data-ttu-id="9e7c9-124">Проверьте выходные данные.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-124">Verify the output.</span></span> <span data-ttu-id="9e7c9-125">Программа должна вывести следующие строки:</span><span class="sxs-lookup"><span data-stu-id="9e7c9-125">Your program should output the following lines:</span></span>

        ```bash
        Hello from quantum world!
       0
       ```

## <a name="develop-with-jupyter-notebooks"></a><span data-ttu-id="9e7c9-126">Разработка с использованием записных книжек Jupyter</span><span class="sxs-lookup"><span data-stu-id="9e7c9-126">Develop with Jupyter notebooks</span></span>

<span data-ttu-id="9e7c9-127">Jupyter Notebook — это широко используемое в образовательных учреждениях, научных лабораториях и интерактивном программировании решение. Оно позволяет выполнять код локально, включая код Q#, инструкции, примечания и другое содержимое.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-127">A favorite of academic settings, scientific labs, and online-based collaborative programming, Jupyter Notebooks offer in-place code execution—now including Q# code—along with instructions, notes, and other content.</span></span>  <span data-ttu-id="9e7c9-128">Ниже описаны действия, которые помогут вам приступить к созданию собственных записных книжек Q#.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-128">Here's what you need to do to start creating your own Q# notebooks.</span></span>

<span data-ttu-id="9e7c9-129">IQ# — это расширение, которое в основном используется в Jupyter и Python с пакетом SDK для .NET Core и предоставляет основные функции для компиляции и моделирования операций Q#.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-129">IQ# (pronounced i-q-sharp) is an extension primarily used by Jupyter and Python to the .NET Core SDK that provides the core functionality for compiling and simulating Q# operations.</span></span>


1. <span data-ttu-id="9e7c9-130">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="9e7c9-130">Pre-requisites</span></span>

    - <span data-ttu-id="9e7c9-131">[Python](https://www.python.org/downloads/) 3.6 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="9e7c9-131">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - [<span data-ttu-id="9e7c9-132">Записная книжка Jupyter</span><span class="sxs-lookup"><span data-stu-id="9e7c9-132">Jupyter Notebook</span></span>](https://jupyter.readthedocs.io/en/latest/install.html)
    - [<span data-ttu-id="9e7c9-133">Пакет SDK для .NET Core 3.0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="9e7c9-133">.NET Core SDK 3.0 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="9e7c9-134">Установите пакет `iqsharp`.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-134">Install the `iqsharp` package</span></span>

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="9e7c9-135">Проверьте установку, создав приложение `Hello World`.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-135">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="9e7c9-136">Выполните следующую команду, чтобы запустить сервер записных книжек.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-136">Run the following command to start the notebook server:</span></span>

        ```bash
        jupyter notebook
        ```

    - <span data-ttu-id="9e7c9-137">Перейдите по URL-адресу, указанному в командной строке.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-137">Browse to the URL shown on the command line.</span></span> <span data-ttu-id="9e7c9-138">Пример: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85 ]</span><span class="sxs-lookup"><span data-stu-id="9e7c9-138">For example: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85]</span></span>

    - <span data-ttu-id="9e7c9-139">Создайте записную книжку Jupyter с ядром Q# и добавьте следующий код в первую ячейку записной книжки.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-139">Create a Jupyter notebook with a Q# kernel, and add the following code to the first notebook cell:</span></span>

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - <span data-ttu-id="9e7c9-140">Запустите эту ячейку записной книжки.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-140">Run this cell of the notebook:</span></span>

        ![Ячейка записной книжки Jupyter с кодом Q#](~/media/install-guide-jupyter.png)

        <span data-ttu-id="9e7c9-142">В выходных данных ячейки должно отобразиться `SayHello`.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-142">You should see `SayHello` in the output of the cell.</span></span> <span data-ttu-id="9e7c9-143">При запуске в записных книжках Jupyter компилируется код Q#, а записная книжка выводит имя найденных операций.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-143">When running in jupyter notebooks, the Q# code is compiled, and the notebook outputs the name of the operation(s) that it finds.</span></span>


    - <span data-ttu-id="9e7c9-144">В новой ячейке смоделируйте выполнение операции, которую вы только что создали, на квантовом компьютере. Для этого используйте магическую команду `%simulate`:</span><span class="sxs-lookup"><span data-stu-id="9e7c9-144">In a new cell, simulate the execution in a quantum computer of the operation you just created by using the `%simulate` magic:</span></span>

        ![Ячейка записной книжки Jupyter с магической командой %simulate](~/media/install-guide-jupyter-simulate.png)

        <span data-ttu-id="9e7c9-146">Сообщение должно отобразиться на экране вместе с результатом вызванной операции (в нашем примере это пустое значение).</span><span class="sxs-lookup"><span data-stu-id="9e7c9-146">You should see the message printed on the screen along with the result of the operation you invoked (in this case, empty).</span></span>


## <a name="develop-with-c-on-windows-using-visual-studio"></a><span data-ttu-id="9e7c9-147">Разработка на языке C# в Windows с помощью Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9e7c9-147">Develop with C# on Windows, using Visual Studio</span></span>

<span data-ttu-id="9e7c9-148">Visual Studio обеспечивает обширную среду для разработки программ Q# с такими возможностями, как завершение кода и выделение синтаксиса, которые помогают разработчикам создавать приложения.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-148">Visual Studio offers a rich environment for developing Q# programs, offering great features like code completion and syntax highlighting that guide the developer in building their applications.</span></span>  <span data-ttu-id="9e7c9-149">Расширение Q# Visual Studio содержит шаблоны для файлов и проектов Q#, а также предоставляет возможность выделения синтаксиса и поддержку IntelliSense.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-149">The Q# Visual Studio extension contains templates for Q# files and projects as well as syntax highlighting and IntelliSense support.</span></span>


1. <span data-ttu-id="9e7c9-150">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="9e7c9-150">Pre-requisites</span></span>

    - <span data-ttu-id="9e7c9-151">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 с включенной рабочей нагрузкой кроссплатформенной разработки .NET Core.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-151">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, with the .NET Core cross-platform development workload enabled</span></span>

1. <span data-ttu-id="9e7c9-152">Установите расширение Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-152">Install the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="9e7c9-153">Скачайте [расширение Visual Studio](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span><span class="sxs-lookup"><span data-stu-id="9e7c9-153">Download the [Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="9e7c9-154">Добавьте расширение в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-154">Add the extension to Visual Studio</span></span>

1. <span data-ttu-id="9e7c9-155">Проверьте установку, создав приложение `Hello World`.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-155">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="9e7c9-156">Создайте приложение Q#.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-156">Create a new Q# application</span></span>

        - <span data-ttu-id="9e7c9-157">Выберите **Файл** -> **Создать** -> **Проект**.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-157">Go to **File** -> **New** -> **Project**</span></span>
        - <span data-ttu-id="9e7c9-158">Введите `Q#` в поле поиска.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-158">Type `Q#` in the search box</span></span>
        - <span data-ttu-id="9e7c9-159">Выберите **Приложение Q#** .</span><span class="sxs-lookup"><span data-stu-id="9e7c9-159">Select **Q# Application**</span></span>
        - <span data-ttu-id="9e7c9-160">Щелкните **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-160">Select **Next**</span></span>
        - <span data-ttu-id="9e7c9-161">Выберите имя и расположение для приложения.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-161">Choose a name and location for your application</span></span>
        - <span data-ttu-id="9e7c9-162">Нажмите кнопку **Создать**</span><span class="sxs-lookup"><span data-stu-id="9e7c9-162">Select **Create**</span></span>

    - <span data-ttu-id="9e7c9-163">Проверьте проект.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-163">Inspect the project</span></span>

        <span data-ttu-id="9e7c9-164">Должны быть созданы два файла: `Driver.cs` — ведущее приложение C#; и `Operation.qs` — программа Q#, которая определяет простую операцию вывода сообщения в консоль.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-164">You should see that two files have been created: `Driver.cs`, which is the C# host application; and `Operation.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

    - <span data-ttu-id="9e7c9-165">Выполнение приложения</span><span class="sxs-lookup"><span data-stu-id="9e7c9-165">Run the application</span></span>

        - <span data-ttu-id="9e7c9-166">Выберите **Отладка** -> **Запустить без отладки**.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-166">Select **Debug** -> **Start Without Debugging**</span></span>
        - <span data-ttu-id="9e7c9-167">В окне консоли должен отобразиться текст `Hello quantum world!`.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-167">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> * <span data-ttu-id="9e7c9-168">Если в одном решении Visual Studio несколько проектов, все проекты, включенные в решение, нужно разместить в той же папке, что и решение, или в одной из вложенных в нее папок.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-168">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its subfolders.</span></span>  

## <a name="develop-with-c-using-visual-studio-code"></a><span data-ttu-id="9e7c9-169">Разработка с помощью C# и Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="9e7c9-169">Develop with C#, using Visual Studio Code</span></span>

<span data-ttu-id="9e7c9-170">Visual Studio Code (VS Code) обеспечивает обширную среду для разработки программ Q# в разных вычислительных средах, включая Windows, Linux и Mac, с такими возможностями, как завершение кода и выделение синтаксиса, которые помогают разработчикам создавать приложения.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-170">Visual Studio Code (VS Code) offers a rich environment for developing Q# programs across many multiple computer environments, including Windows, Linux and Mac, offering great features like code completion and syntax highlighting that guide the developer in building their applications.</span></span>  <span data-ttu-id="9e7c9-171">Расширение Q# VS Code предоставляет возможность выделения синтаксиса и фрагменты кода Q#.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-171">The Q# VS Code extension contains syntax highlighting, and Q# code snippets.</span></span>

1. <span data-ttu-id="9e7c9-172">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="9e7c9-172">Pre-requisites</span></span>

   - [<span data-ttu-id="9e7c9-173">Код VS</span><span class="sxs-lookup"><span data-stu-id="9e7c9-173">VS Code</span></span>](https://code.visualstudio.com/download)
   - [<span data-ttu-id="9e7c9-174">Пакет SDK для .NET Core 3.0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="9e7c9-174">.NET Core SDK 3.0 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="9e7c9-175">Установите расширение Quantum VS Code.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-175">Install the Quantum VS Code extension</span></span>

    - <span data-ttu-id="9e7c9-176">Установите [расширение VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="9e7c9-176">Install the [VS Code extension](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)</span></span>

1. <span data-ttu-id="9e7c9-177">Установите шаблоны проектов Quantum.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-177">Install the Quantum project templates:</span></span>

   - <span data-ttu-id="9e7c9-178">Выберите **Представление** -> **Палитра команд**.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-178">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="9e7c9-179">Выберите **Q#: Install project templates** (Q#: установить шаблоны проектов).</span><span class="sxs-lookup"><span data-stu-id="9e7c9-179">Select **Q#: Install project templates**</span></span>

    <span data-ttu-id="9e7c9-180">Теперь Quantum Development Kit установлен и готов к использованию в ваших приложениях и библиотеках.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-180">You now have the Quantum Development Kit installed and ready to use in your own applications and libraries.</span></span>

1. <span data-ttu-id="9e7c9-181">Проверьте установку, создав приложение `Hello World`.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-181">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="9e7c9-182">Создайте новый проект:</span><span class="sxs-lookup"><span data-stu-id="9e7c9-182">Create a new project:</span></span>

        - <span data-ttu-id="9e7c9-183">Выберите **Представление** -> **Палитра команд**.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-183">Go to **View** -> **Command Palette**</span></span>
        - <span data-ttu-id="9e7c9-184">Выберите **Q#: Create New Project**(Q#: создать проект).</span><span class="sxs-lookup"><span data-stu-id="9e7c9-184">Select **Q#: Create New Project**</span></span>
        - <span data-ttu-id="9e7c9-185">Перейдите в расположение файловой системы, в котором необходимо создать приложение.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-185">Navigate to the location on the file system where you would like to create the application</span></span>
        - <span data-ttu-id="9e7c9-186">После создания проекта нажмите кнопку **Open new project...** (Открыть новый проект...).</span><span class="sxs-lookup"><span data-stu-id="9e7c9-186">Click on the **Open new project...** button, once the project has been created</span></span>

    - <span data-ttu-id="9e7c9-187">Запустите приложение:</span><span class="sxs-lookup"><span data-stu-id="9e7c9-187">Run the application:</span></span>

        - <span data-ttu-id="9e7c9-188">Выберите **Отладка** -> **Запустить без отладки**.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-188">Go to **Debug** -> **Start Without Debugging**</span></span>
        - <span data-ttu-id="9e7c9-189">В окне консоли `Hello quantum world!` должен отобразиться следующий текст.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-189">You should see the following text in the output window `Hello quantum world!`</span></span>

> [!NOTE]
> * > * <span data-ttu-id="9e7c9-190">Сейчас рабочие области с несколькими корневыми папками не поддерживаются в расширении Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-190">Workspaces with multiple root folders are not currently supported by the Visual Studio Code extension.</span></span> <span data-ttu-id="9e7c9-191">Если в одной рабочей области VS Code несколько проектов, все проекты нужно разместить в одной корневой папке.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-191">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

## <a name="develop-with-c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="9e7c9-192">Разработка на языке C# с помощью программы командной строки `dotnet`</span><span class="sxs-lookup"><span data-stu-id="9e7c9-192">Develop with C#, using the `dotnet` command-line tool</span></span>

<span data-ttu-id="9e7c9-193">Разумеется, вы можете создавать и запускать программы Q# и из командной строки. Для этого просто установите шаблоны проектов на основе пакетов QDK и SDK для .NET Core.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-193">Of course, you can also build and run Q# programs from the command line by simply installing the .NET Core SDK and the QDK project templates.</span></span> 

1. <span data-ttu-id="9e7c9-194">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="9e7c9-194">Pre-requisites</span></span>

    - [<span data-ttu-id="9e7c9-195">Пакет SDK для .NET Core 3.0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="9e7c9-195">.NET Core SDK 3.0 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="9e7c9-196">Установите шаблоны проектов Quantum для .NET.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-196">Install the Quantum project templates for .NET</span></span>

    ```bash
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

    <span data-ttu-id="9e7c9-197">Теперь Quantum Development Kit установлен и готов к использованию в ваших приложениях и библиотеках.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-197">You now have the Quantum Development Kit installed and ready to use in your own applications and libraries.</span></span>

1. <span data-ttu-id="9e7c9-198">Проверьте установку, создав приложение `Hello World`.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-198">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="9e7c9-199">Создание приложения</span><span class="sxs-lookup"><span data-stu-id="9e7c9-199">Create a new application</span></span>

       ```bash
       dotnet new console -lang Q# -o runSayHello
       ```

    - <span data-ttu-id="9e7c9-200">Перейдите в новый каталог приложения</span><span class="sxs-lookup"><span data-stu-id="9e7c9-200">Navigate to the new application directory</span></span>

       ```bash
       cd runSayHello
       ```

    <span data-ttu-id="9e7c9-201">Должны быть созданы два файла, а также файлы проекта приложения: файл Q# (`Operation.qs`) и файл узла C# (`Driver.cs`).</span><span class="sxs-lookup"><span data-stu-id="9e7c9-201">You should see that two files have been created, along with the project files of the application: a Q# file (`Operation.qs`) and a C# host file (`Driver.cs`).</span></span>

    - <span data-ttu-id="9e7c9-202">Выполнение приложения</span><span class="sxs-lookup"><span data-stu-id="9e7c9-202">Run the application</span></span>

        ```bash
        dotnet run
        ```

        <span data-ttu-id="9e7c9-203">Вы должны увидеть следующий результат: `Hello quantum world!`.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-203">You should see the following output: `Hello quantum world!`</span></span>

## <a name="whats-next"></a><span data-ttu-id="9e7c9-204">Что дальше?</span><span class="sxs-lookup"><span data-stu-id="9e7c9-204">What's next?</span></span>

<span data-ttu-id="9e7c9-205">После установки Quantum Development Kit в предпочитаемой среде вы можете написать и запустить [первую квантовую программу](xref:microsoft.quantum.write-program).</span><span class="sxs-lookup"><span data-stu-id="9e7c9-205">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
