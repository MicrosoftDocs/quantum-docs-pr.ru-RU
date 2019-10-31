---
title: Сведения об установке Microsoft Quantum Development Kit (QDK)
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: 3ec53934436b47908fd4d794a98933010f6059a7
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/29/2019
ms.locfileid: "73035282"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="69621-102">Установка Microsoft Quantum Development Kit (QDK)</span><span class="sxs-lookup"><span data-stu-id="69621-102">Install the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="69621-103">Узнайте, как установить Microsoft Quantum Development Kit (QDK), чтобы приступить к работе с квантовым программированием.</span><span class="sxs-lookup"><span data-stu-id="69621-103">Learn how to install the Microsoft Quantum Development Kit (QDK), so that you can get started with quantum programming.</span></span> <span data-ttu-id="69621-104">QDK состоит из следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="69621-104">The QDK consists of:</span></span>

- <span data-ttu-id="69621-105">язык программирования Q#;</span><span class="sxs-lookup"><span data-stu-id="69621-105">the Q# programming language</span></span>
- <span data-ttu-id="69621-106">набор библиотек, абстрагирующих сложные функции в Q#;</span><span class="sxs-lookup"><span data-stu-id="69621-106">a set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="69621-107">ведущее приложение (написанное на языке Python или .NET), которое запускает квантовые операции, написанные на языке Q#;</span><span class="sxs-lookup"><span data-stu-id="69621-107">a host application (written in Python or a .NET language) that runs quantum operations written in Q#</span></span>
- <span data-ttu-id="69621-108">средства для упрощения разработки.</span><span class="sxs-lookup"><span data-stu-id="69621-108">tools to facilitate your development</span></span>

<span data-ttu-id="69621-109">Этапы установки различаются в зависимости от выбранной среды разработки.</span><span class="sxs-lookup"><span data-stu-id="69621-109">Depending on your chosen development environment, there are different installation steps.</span></span> <span data-ttu-id="69621-110">Выберите среду из следующих разделов.</span><span class="sxs-lookup"><span data-stu-id="69621-110">Choose your environment from the sections below.</span></span>

## <a name="develop-with-python"></a><span data-ttu-id="69621-111">Разработка на языке Python</span><span class="sxs-lookup"><span data-stu-id="69621-111">Develop with Python</span></span>

1. <span data-ttu-id="69621-112">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="69621-112">Pre-requisites</span></span>

    - <span data-ttu-id="69621-113">[Python](https://www.python.org/downloads/) 3.6 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="69621-113">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - <span data-ttu-id="69621-114">Диспетчер пакетов Python [PIP](https://pip.pypa.io/en/stable/installing)</span><span class="sxs-lookup"><span data-stu-id="69621-114">The [PIP](https://pip.pypa.io/en/stable/installing) Python package manager</span></span>
    - [<span data-ttu-id="69621-115">Пакет SDK для .NET Core 2.1 или более поздних версий</span><span class="sxs-lookup"><span data-stu-id="69621-115">.NET Core SDK 2.1 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="69621-116">Установите пакет `iqsharp`.</span><span class="sxs-lookup"><span data-stu-id="69621-116">Install the `iqsharp` package</span></span>

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="69621-117">Установите пакет `qsharp`.</span><span class="sxs-lookup"><span data-stu-id="69621-117">Install the `qsharp` package</span></span>

    ```bash
    pip install qsharp
    ```

1. <span data-ttu-id="69621-118">Проверьте установку, создав приложение `Hello World`.</span><span class="sxs-lookup"><span data-stu-id="69621-118">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="69621-119">Создайте минимальную операцию Q#, создав файл с именем `Operation.qs` и добавив в него следующий код.</span><span class="sxs-lookup"><span data-stu-id="69621-119">Create a minimal Q# operation, by creating a file called `Operation.qs`, and adding the following code to it:</span></span>

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

    - <span data-ttu-id="69621-120">Создайте программу Python с именем `hello_world.py` для вызова операции `SayHello()` Q#.</span><span class="sxs-lookup"><span data-stu-id="69621-120">Create a Python program called `hello_world.py` to call the Q# `SayHello()` operation:</span></span>

        ```python
        import qsharp

        from HelloWorld import SayHello

        SayHello.simulate()
        ```

    - <span data-ttu-id="69621-121">Запустите программу.</span><span class="sxs-lookup"><span data-stu-id="69621-121">Run the program:</span></span>

        ```bash
        python hello_world.py
        ```

    - <span data-ttu-id="69621-122">Проверьте выходные данные.</span><span class="sxs-lookup"><span data-stu-id="69621-122">Verify the output.</span></span> <span data-ttu-id="69621-123">Программа должна вывести следующие строки:</span><span class="sxs-lookup"><span data-stu-id="69621-123">Your program should output the following lines:</span></span>

        ```bash
        Hello from quantum world!
       0
       ```

## <a name="develop-with-jupyter-notebooks"></a><span data-ttu-id="69621-124">Разработка с использованием записных книжек Jupyter</span><span class="sxs-lookup"><span data-stu-id="69621-124">Develop with Jupyter notebooks</span></span>

1. <span data-ttu-id="69621-125">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="69621-125">Pre-requisites</span></span>

    - <span data-ttu-id="69621-126">[Python](https://www.python.org/downloads/) 3.6 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="69621-126">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - [<span data-ttu-id="69621-127">Записная книжка Jupyter</span><span class="sxs-lookup"><span data-stu-id="69621-127">Jupyter Notebook</span></span>](https://jupyter.readthedocs.io/en/latest/install.html)
    - [<span data-ttu-id="69621-128">Пакет SDK для .NET Core 2.1 или более поздних версий</span><span class="sxs-lookup"><span data-stu-id="69621-128">.NET Core SDK 2.1 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="69621-129">Установите пакет `iqsharp`.</span><span class="sxs-lookup"><span data-stu-id="69621-129">Install the `iqsharp` package</span></span>

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="69621-130">Проверьте установку, создав приложение `Hello World`.</span><span class="sxs-lookup"><span data-stu-id="69621-130">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="69621-131">Выполните следующую команду, чтобы запустить сервер записных книжек.</span><span class="sxs-lookup"><span data-stu-id="69621-131">Run the following command to start the notebook server:</span></span>

        ```bash
        jupyter notebook
        ```

    - <span data-ttu-id="69621-132">Перейдите по URL-адресу, указанному в командной строке.</span><span class="sxs-lookup"><span data-stu-id="69621-132">Browse to the URL shown on the command line.</span></span> <span data-ttu-id="69621-133">Пример: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85 ]</span><span class="sxs-lookup"><span data-stu-id="69621-133">For example: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85]</span></span>

    - <span data-ttu-id="69621-134">Создайте записную книжку Jupyter с ядром Q# и добавьте следующий код в первую ячейку записной книжки.</span><span class="sxs-lookup"><span data-stu-id="69621-134">Create a Jupyter notebook with a Q# kernel, and add the following code to the first notebook cell:</span></span>

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - <span data-ttu-id="69621-135">Запустите эту ячейку записной книжки.</span><span class="sxs-lookup"><span data-stu-id="69621-135">Run this cell of the notebook:</span></span>

        ![Ячейка записной книжки Jupyter](~/media/install-guide-jupyter.png)

        <span data-ttu-id="69621-137">В выходных данных ячейки должно отобразиться `SayHello`.</span><span class="sxs-lookup"><span data-stu-id="69621-137">You should see `SayHello` in the output of the cell.</span></span> <span data-ttu-id="69621-138">При запуске в записных книжках Jupyter компилируется код Q#, а записная книжка выводит имя найденных операций.</span><span class="sxs-lookup"><span data-stu-id="69621-138">When running in jupyter notebooks, the Q# code is compiled, and the notebook outputs the name of the operation(s) that it finds.</span></span>

## <a name="develop-with-c-on-windows-using-visual-studio"></a><span data-ttu-id="69621-139">Разработка на языке C# в Windows с помощью Visual Studio</span><span class="sxs-lookup"><span data-stu-id="69621-139">Develop with C# on Windows, using Visual Studio</span></span>

1. <span data-ttu-id="69621-140">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="69621-140">Pre-requisites</span></span>

    - <span data-ttu-id="69621-141">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 с включенной рабочей нагрузкой кроссплатформенной разработки .NET Core.</span><span class="sxs-lookup"><span data-stu-id="69621-141">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, with the .NET Core cross-platform development workload enabled</span></span>

1. <span data-ttu-id="69621-142">Установите расширение Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="69621-142">Install the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="69621-143">Скачайте [расширение Visual Studio](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span><span class="sxs-lookup"><span data-stu-id="69621-143">Download the [Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="69621-144">Добавьте расширение в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="69621-144">Add the extension to Visual Studio</span></span>

1. <span data-ttu-id="69621-145">Проверьте установку, создав приложение `Hello World`.</span><span class="sxs-lookup"><span data-stu-id="69621-145">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="69621-146">Создайте приложение Q#.</span><span class="sxs-lookup"><span data-stu-id="69621-146">Create a new Q# application</span></span>

        - <span data-ttu-id="69621-147">Выберите **Файл** -> **Создать** -> **Проект**.</span><span class="sxs-lookup"><span data-stu-id="69621-147">Go to **File** -> **New** -> **Project**</span></span>
        - <span data-ttu-id="69621-148">Введите `Q#` в поле поиска.</span><span class="sxs-lookup"><span data-stu-id="69621-148">Type `Q#` in the search box</span></span>
        - <span data-ttu-id="69621-149">Выберите **Приложение Q#** .</span><span class="sxs-lookup"><span data-stu-id="69621-149">Select **Q# Application**</span></span>
        - <span data-ttu-id="69621-150">Щелкните **Далее**.</span><span class="sxs-lookup"><span data-stu-id="69621-150">Select **Next**</span></span>
        - <span data-ttu-id="69621-151">Выберите имя и расположение для приложения.</span><span class="sxs-lookup"><span data-stu-id="69621-151">Choose a name and location for your application</span></span>
        - <span data-ttu-id="69621-152">Нажмите кнопку **Создать**</span><span class="sxs-lookup"><span data-stu-id="69621-152">Select **Create**</span></span>

    - <span data-ttu-id="69621-153">Проверьте проект.</span><span class="sxs-lookup"><span data-stu-id="69621-153">Inspect the project</span></span>

        <span data-ttu-id="69621-154">Должны быть созданы два файла: `Driver.cs` — ведущее приложение C#; и `Operation.qs` — программа Q#, которая определяет простую операцию вывода сообщения в консоль.</span><span class="sxs-lookup"><span data-stu-id="69621-154">You should see that two files have been created: `Driver.cs`, which is the C# host application; and `Operation.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

    - <span data-ttu-id="69621-155">Выполнение приложения</span><span class="sxs-lookup"><span data-stu-id="69621-155">Run the application</span></span>

        - <span data-ttu-id="69621-156">Выберите **Отладка** -> **Запустить без отладки**.</span><span class="sxs-lookup"><span data-stu-id="69621-156">Select **Debug** -> **Start Without Debugging**</span></span>
        - <span data-ttu-id="69621-157">В окне консоли должен отобразиться текст `Hello quantum world!`.</span><span class="sxs-lookup"><span data-stu-id="69621-157">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> * <span data-ttu-id="69621-158">Если в одном решении Visual Studio несколько проектов, все проекты, включенные в решение, нужно разместить в той же папке, что и решение, или в одной из вложенных в нее папок.</span><span class="sxs-lookup"><span data-stu-id="69621-158">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its subfolders.</span></span>  

## <a name="develop-with-c-using-vs-code"></a><span data-ttu-id="69621-159">Разработка на языке C# с помощью VS Code</span><span class="sxs-lookup"><span data-stu-id="69621-159">Develop with C#, using VS Code</span></span>

1. <span data-ttu-id="69621-160">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="69621-160">Pre-requisites</span></span>

   - [<span data-ttu-id="69621-161">Код VS</span><span class="sxs-lookup"><span data-stu-id="69621-161">VS Code</span></span>](https://code.visualstudio.com/download)
   - [<span data-ttu-id="69621-162">Пакет SDK для .NET Core 2.1 или более поздних версий</span><span class="sxs-lookup"><span data-stu-id="69621-162">.NET Core SDK 2.1 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="69621-163">Установите расширение Quantum VS Code.</span><span class="sxs-lookup"><span data-stu-id="69621-163">Install the Quantum VS Code extension</span></span>

    - <span data-ttu-id="69621-164">Установите [расширение VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="69621-164">Install the [VS Code extension](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)</span></span>

1. <span data-ttu-id="69621-165">Установите шаблоны проектов Quantum.</span><span class="sxs-lookup"><span data-stu-id="69621-165">Install the Quantum project templates:</span></span>

   - <span data-ttu-id="69621-166">Выберите **Представление** -> **Палитра команд**.</span><span class="sxs-lookup"><span data-stu-id="69621-166">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="69621-167">Выберите **Q#: Install project templates** (Q#: установить шаблоны проектов).</span><span class="sxs-lookup"><span data-stu-id="69621-167">Select **Q#: Install project templates**</span></span>

    <span data-ttu-id="69621-168">Теперь Quantum Development Kit установлен и готов к использованию в ваших приложениях и библиотеках.</span><span class="sxs-lookup"><span data-stu-id="69621-168">You now have the Quantum Development Kit installed and ready to use in your own applications and libraries.</span></span>

1. <span data-ttu-id="69621-169">Проверьте установку, создав приложение `Hello World`.</span><span class="sxs-lookup"><span data-stu-id="69621-169">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="69621-170">Создайте новый проект:</span><span class="sxs-lookup"><span data-stu-id="69621-170">Create a new project:</span></span>

        - <span data-ttu-id="69621-171">Выберите **Представление** -> **Палитра команд**.</span><span class="sxs-lookup"><span data-stu-id="69621-171">Go to **View** -> **Command Palette**</span></span>
        - <span data-ttu-id="69621-172">Выберите **Q#: Create New Project**(Q#: создать проект).</span><span class="sxs-lookup"><span data-stu-id="69621-172">Select **Q#: Create New Project**</span></span>
        - <span data-ttu-id="69621-173">Перейдите в расположение файловой системы, в котором необходимо создать приложение.</span><span class="sxs-lookup"><span data-stu-id="69621-173">Navigate to the location on the file system where you would like to create the application</span></span>
        - <span data-ttu-id="69621-174">После создания проекта нажмите кнопку **Open new project...** (Открыть новый проект...).</span><span class="sxs-lookup"><span data-stu-id="69621-174">Click on the **Open new project...** button, once the project has been created</span></span>

    - <span data-ttu-id="69621-175">Запустите приложение:</span><span class="sxs-lookup"><span data-stu-id="69621-175">Run the application:</span></span>

        - <span data-ttu-id="69621-176">Выберите **Отладка** -> **Запустить без отладки**.</span><span class="sxs-lookup"><span data-stu-id="69621-176">Go to **Debug** -> **Start Without Debugging**</span></span>
        - <span data-ttu-id="69621-177">В окне консоли `Hello quantum world!` должен отобразиться следующий текст.</span><span class="sxs-lookup"><span data-stu-id="69621-177">You should see the following text in the output window `Hello quantum world!`</span></span>

> [!NOTE]
> * > * <span data-ttu-id="69621-178">Сейчас рабочие области с несколькими корневыми папками не поддерживаются в расширении Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="69621-178">Workspaces with multiple root folders are not currently supported by the Visual Studio Code extension.</span></span> <span data-ttu-id="69621-179">Если в одной рабочей области VS Code несколько проектов, все проекты нужно разместить в одной корневой папке.</span><span class="sxs-lookup"><span data-stu-id="69621-179">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

## <a name="develop-with-c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="69621-180">Разработка на языке C# с помощью программы командной строки `dotnet`</span><span class="sxs-lookup"><span data-stu-id="69621-180">Develop with C#, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="69621-181">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="69621-181">Pre-requisites</span></span>

    - [<span data-ttu-id="69621-182">Пакет SDK для .NET Core 2.1 или более поздних версий</span><span class="sxs-lookup"><span data-stu-id="69621-182">.NET Core SDK 2.1 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="69621-183">Установите шаблоны проектов Quantum для .NET.</span><span class="sxs-lookup"><span data-stu-id="69621-183">Install the Quantum project templates for .NET</span></span>

    ```bash
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

    <span data-ttu-id="69621-184">Теперь Quantum Development Kit установлен и готов к использованию в ваших приложениях и библиотеках.</span><span class="sxs-lookup"><span data-stu-id="69621-184">You now have the Quantum Development Kit installed and ready to use in your own applications and libraries.</span></span>

1. <span data-ttu-id="69621-185">Проверьте установку, создав приложение `Hello World`.</span><span class="sxs-lookup"><span data-stu-id="69621-185">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="69621-186">Создание приложения</span><span class="sxs-lookup"><span data-stu-id="69621-186">Create a new application</span></span>

       ```bash
       dotnet new console -lang Q# -o runSayHello
       ```

    - <span data-ttu-id="69621-187">Перейдите в новый каталог приложения</span><span class="sxs-lookup"><span data-stu-id="69621-187">Navigate to the new application directory</span></span>

       ```bash
       cd runSayHello
       ```

    <span data-ttu-id="69621-188">Должны быть созданы два файла, а также файлы проекта приложения: файл Q# (`Operation.qs`) и файл узла C# (`Driver.cs`).</span><span class="sxs-lookup"><span data-stu-id="69621-188">You should see that two files have been created, along with the project files of the application: a Q# file (`Operation.qs`) and a C# host file (`Driver.cs`).</span></span>

    - <span data-ttu-id="69621-189">Выполнение приложения</span><span class="sxs-lookup"><span data-stu-id="69621-189">Run the application</span></span>

        ```bash
        dotnet run
        ```

        <span data-ttu-id="69621-190">Вы должны увидеть следующий результат: `Hello quantum world!`.</span><span class="sxs-lookup"><span data-stu-id="69621-190">You should see the following output: `Hello quantum world!`</span></span>

## <a name="whats-next"></a><span data-ttu-id="69621-191">Что дальше?</span><span class="sxs-lookup"><span data-stu-id="69621-191">What's next?</span></span>

<span data-ttu-id="69621-192">После установки Quantum Development Kit в предпочитаемой среде вы можете написать и запустить [первую квантовую программу](xref:microsoft.quantum.write-program).</span><span class="sxs-lookup"><span data-stu-id="69621-192">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
