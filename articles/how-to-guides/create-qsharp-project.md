---
title: 'Узнайте, как создать проект Q # с помощью пакета средств разработки такта (КДК).'
description: 'Инициализация проекта для разработки на такте с помощью КДК и Q # в выбранной среде разработки'
author: natke
ms.author: nakersha
ms.date: 10/19/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.howto.createproject
ms.openlocfilehash: 8af8e3288aab731520ede984d5f89644de292385
ms.sourcegitcommit: c8ebc5d7d8581444754f5d7bfaca2f25601f1b14
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2020
ms.locfileid: "84578217"
---
# <a name="create-a-q-project-in-your-development-environment"></a><span data-ttu-id="0b68e-103">Создание проекта Q # в среде разработки</span><span class="sxs-lookup"><span data-stu-id="0b68e-103">Create a Q# project in your development environment</span></span>

<span data-ttu-id="0b68e-104">Узнайте, как создать проект Q # с помощью КДК.</span><span class="sxs-lookup"><span data-stu-id="0b68e-104">Learn how to create a Q# project with the QDK.</span></span>

<span data-ttu-id="0b68e-105">Проект Q # содержит файлы Q #, содержащие тактовый код, а также ведущее приложение для запуска тактовой программы.</span><span class="sxs-lookup"><span data-stu-id="0b68e-105">A Q# project contains Q# files containing quantum code, as well as a host program to run the quantum program.</span></span> <span data-ttu-id="0b68e-106">Вы можете написать ведущее приложение на языках .NET, таких как C# или Python.</span><span class="sxs-lookup"><span data-stu-id="0b68e-106">You can write the host program in .NET languages such as C#, or in Python.</span></span> <span data-ttu-id="0b68e-107">Можно также запустить Q # Code в Jupyter Notebook с помощью ядра IQ #.</span><span class="sxs-lookup"><span data-stu-id="0b68e-107">You can also run Q# code in a Jupyter Notebook using the IQ# kernel.</span></span>

<span data-ttu-id="0b68e-108">Выберите среду разработки и язык в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="0b68e-108">Choose your development environment and language from the sections below:</span></span>

* [<span data-ttu-id="0b68e-109">Python</span><span class="sxs-lookup"><span data-stu-id="0b68e-109">Python</span></span>](#create-a-python-project)
* [<span data-ttu-id="0b68e-110">Записные книжки Jupyter Notebook для Q#</span><span class="sxs-lookup"><span data-stu-id="0b68e-110">Q# Jupyter Notebooks</span></span>](#create-a-q-jupyter-notebook-project)
* [<span data-ttu-id="0b68e-111">C# с Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0b68e-111">C# with Visual Studio</span></span>](#create-a-c-project-on-windows-using-visual-studio)
* [<span data-ttu-id="0b68e-112">C# с VS Code</span><span class="sxs-lookup"><span data-stu-id="0b68e-112">C# with VS Code</span></span>](#create-a-c-project-using-vs-code)
* [<span data-ttu-id="0b68e-113">C# с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="0b68e-113">C# with the command line</span></span>](#create-a-c-project-using-the-dotnet-command-line-tool)

## <a name="create-a-python-project"></a><span data-ttu-id="0b68e-114">Создание проекта Python</span><span class="sxs-lookup"><span data-stu-id="0b68e-114">Create a Python project</span></span>

1. <span data-ttu-id="0b68e-115">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="0b68e-115">Pre-requisites</span></span>

     * <span data-ttu-id="0b68e-116">Установка [пакета средств разработки тактов для Python](xref:microsoft.quantum.install.python)</span><span class="sxs-lookup"><span data-stu-id="0b68e-116">Install the [Quantum Development Kit for Python](xref:microsoft.quantum.install.python)</span></span>

1. <span data-ttu-id="0b68e-117">Создайте папку для проекта и перейдите к этой папке.</span><span class="sxs-lookup"><span data-stu-id="0b68e-117">Create a folder for your project, and navigate to that folder</span></span>

1. <span data-ttu-id="0b68e-118">Создайте файл Q # с именем `Operation.qs` и добавьте в него код q #.</span><span class="sxs-lookup"><span data-stu-id="0b68e-118">Create a Q# file called `Operation.qs`, and add your Q# code to it.</span></span> <span data-ttu-id="0b68e-119">Пример.</span><span class="sxs-lookup"><span data-stu-id="0b68e-119">For example:</span></span>

    ```qsharp
    namespace HelloWorld {
        open Microsoft.Quantum.Intrinsic;
        open Microsoft.Quantum.Canon;

        operation SayHello() : Result {
            Message("Hello from quantum world!");
            return Zero;
        }
    }
    ```

1. <span data-ttu-id="0b68e-120">Создайте файл узла Python с именем `host.py` для вызова операции Q #.</span><span class="sxs-lookup"><span data-stu-id="0b68e-120">Create a python host file called `host.py` to call your Q# operation.</span></span> <span data-ttu-id="0b68e-121">Пример.</span><span class="sxs-lookup"><span data-stu-id="0b68e-121">For example:</span></span>

    ```python
    import qsharp

    from HelloWorld import SayHello

    SayHello.simulate()
    ```

1. <span data-ttu-id="0b68e-122">Запустите программу.</span><span class="sxs-lookup"><span data-stu-id="0b68e-122">Run the program:</span></span>

    ```
    python host.py
    ```

1. <span data-ttu-id="0b68e-123">Проверьте выходные данные.</span><span class="sxs-lookup"><span data-stu-id="0b68e-123">Verify the output.</span></span> <span data-ttu-id="0b68e-124">Программа должна вывести следующие строки:</span><span class="sxs-lookup"><span data-stu-id="0b68e-124">Your program should output the following lines:</span></span>

    ```
    Hello from quantum world!
    0
    ```

<span data-ttu-id="0b68e-125">Теперь вы можете продолжить разработку тактовой программы.</span><span class="sxs-lookup"><span data-stu-id="0b68e-125">You can now continue to develop your quantum program.</span></span>

## <a name="create-a-q-jupyter-notebook-project"></a><span data-ttu-id="0b68e-126">Создание проекта Q # Jupyter Notebook</span><span class="sxs-lookup"><span data-stu-id="0b68e-126">Create a Q# Jupyter Notebook project</span></span>

1. <span data-ttu-id="0b68e-127">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="0b68e-127">Pre-requisites</span></span>

    * <span data-ttu-id="0b68e-128">Установка [пакета средств разработки тактов для записных книжек Jupyter](xref:microsoft.quantum.install.jupyter)</span><span class="sxs-lookup"><span data-stu-id="0b68e-128">Install the [Quantum Development Kit for Jupyter Notebooks](xref:microsoft.quantum.install.jupyter)</span></span>

1. <span data-ttu-id="0b68e-129">Выполните следующую команду, чтобы запустить сервер записных книжек.</span><span class="sxs-lookup"><span data-stu-id="0b68e-129">Run the following command to start the notebook server:</span></span>

    ```
    jupyter notebook
    ```

1. <span data-ttu-id="0b68e-130">Перейдите по URL-адресу, указанному в командной строке.</span><span class="sxs-lookup"><span data-stu-id="0b68e-130">Browse to the URL shown on the command line.</span></span> <span data-ttu-id="0b68e-131">Пример: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85]</span><span class="sxs-lookup"><span data-stu-id="0b68e-131">For example: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85]</span></span>

1. <span data-ttu-id="0b68e-132">В браузере появится страница Jupyter.</span><span class="sxs-lookup"><span data-stu-id="0b68e-132">A Jupyter page appears in the browser.</span></span> <span data-ttu-id="0b68e-133">На вкладке **файлы** выберите **создать**  >  **Q #** , чтобы создать Jupyter Notebook с ядром Q #.</span><span class="sxs-lookup"><span data-stu-id="0b68e-133">On the **Files** tab, select **New** > **Q#** to create a Jupyter Notebook with a Q# kernel.</span></span> <span data-ttu-id="0b68e-134">Добавьте следующий код в первую ячейку записной книжки:</span><span class="sxs-lookup"><span data-stu-id="0b68e-134">Add the following code to the first notebook cell:</span></span>

    ```qsharp
    operation SayHello() : Unit {
        Message("Hello from quantum world!");
    }
    ```

1. <span data-ttu-id="0b68e-135">Выберите **ячейку**  >  **Запуск ячеек** для запуска записной книжки.</span><span class="sxs-lookup"><span data-stu-id="0b68e-135">Select **Cell** > **Run Cells** to run the notebook.</span></span> <span data-ttu-id="0b68e-136">`SayHello`Вскоре появится в ячейке выходных данных:</span><span class="sxs-lookup"><span data-stu-id="0b68e-136">`SayHello` will soon appear in the cell output:</span></span>

    ![Jupyter Notebook ячейку с кодом Q #](~/media/install-guide-jupyter.png)

    <span data-ttu-id="0b68e-138">При запуске в записных книжках Jupyter компилируется код Q #, а Записная книжка выводит имя найденных операций.</span><span class="sxs-lookup"><span data-stu-id="0b68e-138">When running in Jupyter Notebooks, the Q# code is compiled, and the notebook outputs the name of the operation(s) that it finds.</span></span>

1. <span data-ttu-id="0b68e-139">В новой ячейке смоделируйте выполнение операции, которую вы только что создали, на квантовом компьютере. Для этого используйте магическую команду `%simulate`:</span><span class="sxs-lookup"><span data-stu-id="0b68e-139">In a new cell, simulate the execution in a quantum computer of the operation you just created by using the `%simulate` magic:</span></span>

    ![Jupyter Notebook ячейка с% имитировать волшебное магическое](~/media/install-guide-jupyter-simulate.png)

    <span data-ttu-id="0b68e-141">Сообщение должно отобразиться на экране вместе с результатом вызванной операции (в нашем примере это пустое значение).</span><span class="sxs-lookup"><span data-stu-id="0b68e-141">You should see the message printed on the screen along with the result of the operation you invoked (in this case, empty).</span></span>

<span data-ttu-id="0b68e-142">Теперь можно добавить другие операции Q #, чтобы продолжить разработку тактов.</span><span class="sxs-lookup"><span data-stu-id="0b68e-142">You can now add other Q# operations to continue your quantum development.</span></span>

## <a name="create-a-c-project-on-windows-using-visual-studio"></a><span data-ttu-id="0b68e-143">Создание проекта C# в Windows с помощью Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0b68e-143">Create a C# project on Windows, using Visual Studio</span></span>

1. <span data-ttu-id="0b68e-144">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="0b68e-144">Pre-requisites</span></span>

    * <span data-ttu-id="0b68e-145">Установка [расширения пакета разработки тактов для Visual Studio](xref:microsoft.quantum.install.cs)</span><span class="sxs-lookup"><span data-stu-id="0b68e-145">Install the [Quantum Development Kit extension for Visual Studio](xref:microsoft.quantum.install.cs)</span></span>

1. <span data-ttu-id="0b68e-146">Создайте приложение Q#.</span><span class="sxs-lookup"><span data-stu-id="0b68e-146">Create a new Q# application</span></span>

    * <span data-ttu-id="0b68e-147">Переход к **файлу**  ->  **Новый**  ->  **проект**</span><span class="sxs-lookup"><span data-stu-id="0b68e-147">Go to **File** -> **New** -> **Project**</span></span>
    * <span data-ttu-id="0b68e-148">Введите `Q#` в поле поиска.</span><span class="sxs-lookup"><span data-stu-id="0b68e-148">Type `Q#` in the search box</span></span>
    * <span data-ttu-id="0b68e-149">Выберите **Приложение Q#**.</span><span class="sxs-lookup"><span data-stu-id="0b68e-149">Select **Q# Application**</span></span>
    * <span data-ttu-id="0b68e-150">Щелкните **Далее**.</span><span class="sxs-lookup"><span data-stu-id="0b68e-150">Select **Next**</span></span>
    * <span data-ttu-id="0b68e-151">Выберите имя и расположение для приложения.</span><span class="sxs-lookup"><span data-stu-id="0b68e-151">Choose a name and location for your application</span></span>
    * <span data-ttu-id="0b68e-152">Нажмите кнопку **Создать**</span><span class="sxs-lookup"><span data-stu-id="0b68e-152">Select **Create**</span></span>

1. <span data-ttu-id="0b68e-153">Проверьте проект.</span><span class="sxs-lookup"><span data-stu-id="0b68e-153">Inspect the project</span></span>

    <span data-ttu-id="0b68e-154">Должны быть созданы два файла: `Driver.cs` — ведущее приложение C#; и `Operation.qs` — программа Q#, которая определяет простую операцию вывода сообщения в консоль.</span><span class="sxs-lookup"><span data-stu-id="0b68e-154">You should see that two files have been created: `Driver.cs`, which is the C# host application; and `Operation.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

1. <span data-ttu-id="0b68e-155">Выполнение приложения</span><span class="sxs-lookup"><span data-stu-id="0b68e-155">Run the application</span></span>

    * <span data-ttu-id="0b68e-156">Выберите **Отладка**  ->  **Запуск без отладки**</span><span class="sxs-lookup"><span data-stu-id="0b68e-156">Select **Debug** -> **Start Without Debugging**</span></span>
    * <span data-ttu-id="0b68e-157">В окне консоли должен отобразиться текст `Hello quantum world!`.</span><span class="sxs-lookup"><span data-stu-id="0b68e-157">You should see the text `Hello quantum world!` printed to a console window.</span></span>

<span data-ttu-id="0b68e-158">Теперь вы можете продолжить разработку тактов с помощью Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0b68e-158">You can now continue your quantum development using Visual Studio</span></span>

> [!NOTE]
> * <span data-ttu-id="0b68e-159">Если в одном решении Visual Studio несколько проектов, все проекты, включенные в решение, нужно разместить в той же папке, что и решение, или в одной из вложенных в нее папок.</span><span class="sxs-lookup"><span data-stu-id="0b68e-159">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its subfolders.</span></span>  

## <a name="create-a-c-project-using-vs-code"></a><span data-ttu-id="0b68e-160">Создание проекта C# с помощью VS Code</span><span class="sxs-lookup"><span data-stu-id="0b68e-160">Create a C# project, using VS Code</span></span>

1. <span data-ttu-id="0b68e-161">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="0b68e-161">Pre-requisites</span></span>

    * <span data-ttu-id="0b68e-162">Установка [расширения пакета разработки такта для VS Code](xref:microsoft.quantum.install.cs)</span><span class="sxs-lookup"><span data-stu-id="0b68e-162">Install the [Quantum Development Kit extension for VS Code](xref:microsoft.quantum.install.cs)</span></span>

1. <span data-ttu-id="0b68e-163">Создайте новый проект:</span><span class="sxs-lookup"><span data-stu-id="0b68e-163">Create a new project:</span></span>

    * <span data-ttu-id="0b68e-164">Перейти к **View**  ->  **палитре команд** просмотра</span><span class="sxs-lookup"><span data-stu-id="0b68e-164">Go to **View** -> **Command Palette**</span></span>
    * <span data-ttu-id="0b68e-165">Выберите **Q #: создать новый проект**</span><span class="sxs-lookup"><span data-stu-id="0b68e-165">Select **Q#: Create New Project**</span></span>
    * <span data-ttu-id="0b68e-166">Выберите **автономное консольное приложение**</span><span class="sxs-lookup"><span data-stu-id="0b68e-166">Select **Standalone console application**</span></span>
    * <span data-ttu-id="0b68e-167">Перейдите в расположение файловой системы, в котором необходимо создать приложение.</span><span class="sxs-lookup"><span data-stu-id="0b68e-167">Navigate to the location on the file system where you would like to create the application</span></span>
    * <span data-ttu-id="0b68e-168">После создания проекта нажмите кнопку **Open new project...** (Открыть новый проект...).</span><span class="sxs-lookup"><span data-stu-id="0b68e-168">Click on the **Open new project...** button, once the project has been created</span></span>

1. <span data-ttu-id="0b68e-169">Запустите приложение:</span><span class="sxs-lookup"><span data-stu-id="0b68e-169">Run the application:</span></span>

    * <span data-ttu-id="0b68e-170">Последовательно выберите **терминал**  ->  **Новый терминал** .</span><span class="sxs-lookup"><span data-stu-id="0b68e-170">Go to **Terminal** -> **New Terminal**</span></span>
    * <span data-ttu-id="0b68e-171">Введите `dotnet run`</span><span class="sxs-lookup"><span data-stu-id="0b68e-171">Enter `dotnet run`</span></span>
    * <span data-ttu-id="0b68e-172">В окне консоли `Hello quantum world!` должен отобразиться следующий текст.</span><span class="sxs-lookup"><span data-stu-id="0b68e-172">You should see the following text in the output window `Hello quantum world!`</span></span>

<span data-ttu-id="0b68e-173">Теперь можно продолжить разработку тактов с помощью Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="0b68e-173">You can now continue your quantum development using Visual Studio Code.</span></span>

> [!NOTE]
> * <span data-ttu-id="0b68e-174">Сейчас рабочие области с несколькими корневыми папками не поддерживаются в расширении Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="0b68e-174">Workspaces with multiple root folders are not currently supported by the Visual Studio Code extension.</span></span> <span data-ttu-id="0b68e-175">Если в одной рабочей области VS Code несколько проектов, все проекты нужно разместить в одной корневой папке.</span><span class="sxs-lookup"><span data-stu-id="0b68e-175">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

## <a name="create-a-c-project-using-the-dotnet-command-line-tool"></a><span data-ttu-id="0b68e-176">Создание проекта C# с помощью `dotnet` программы командной строки</span><span class="sxs-lookup"><span data-stu-id="0b68e-176">Create a C# project, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="0b68e-177">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="0b68e-177">Pre-requisites</span></span>

    * <span data-ttu-id="0b68e-178">Установка [пакета средств разработки тактов для командной строки](xref:microsoft.quantum.install.standalone)</span><span class="sxs-lookup"><span data-stu-id="0b68e-178">Install the [Quantum Development Kit for the command line](xref:microsoft.quantum.install.standalone)</span></span>

1. <span data-ttu-id="0b68e-179">Создание приложения</span><span class="sxs-lookup"><span data-stu-id="0b68e-179">Create a new application</span></span>

    ```dotnetcli
    dotnet new console -lang Q# -o <project name>
    ```

1. <span data-ttu-id="0b68e-180">Перейдите в новый каталог приложения</span><span class="sxs-lookup"><span data-stu-id="0b68e-180">Navigate to the new application directory</span></span>

    ```
    cd <project name>
    ```

    <span data-ttu-id="0b68e-181">Должны быть созданы два файла, а также файлы проекта приложения: файл Q# (`Operation.qs`) и файл узла C# (`Driver.cs`).</span><span class="sxs-lookup"><span data-stu-id="0b68e-181">You should see that two files have been created, along with the project files of the application: a Q# file (`Operation.qs`) and a C# host file (`Driver.cs`).</span></span>

1. <span data-ttu-id="0b68e-182">Выполнение приложения</span><span class="sxs-lookup"><span data-stu-id="0b68e-182">Run the application</span></span>

    ```dotnetcli
    dotnet run
    ```

    <span data-ttu-id="0b68e-183">Вы должны увидеть следующий результат: `Hello quantum world!`.</span><span class="sxs-lookup"><span data-stu-id="0b68e-183">You should see the following output: `Hello quantum world!`</span></span>

<span data-ttu-id="0b68e-184">Теперь вы можете продолжить разработку тактов с помощью средств командной строки.</span><span class="sxs-lookup"><span data-stu-id="0b68e-184">You now continue your quantum development, using command line tools.</span></span>

## <a name="next-steps"></a><span data-ttu-id="0b68e-185">Дальнейшие шаги</span><span class="sxs-lookup"><span data-stu-id="0b68e-185">Next steps</span></span>

<span data-ttu-id="0b68e-186">После создания проекта в предпочитаемой среде можно продолжить разработку тактов.</span><span class="sxs-lookup"><span data-stu-id="0b68e-186">Now that you have created a project in your preferred environment, you can continue your quantum development.</span></span>
