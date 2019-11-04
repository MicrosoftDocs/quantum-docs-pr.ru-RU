---
title: 'Узнайте, как создать проект Q # с помощью пакета средств разработки такта (КДК).'
description: 'Инициализация проекта для разработки на такте с помощью КДК и Q # в выбранной среде разработки'
author: natke
ms.author: nakersha
ms.date: 10/19/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.howto.createproject
ms.openlocfilehash: b4bec5e7a174b7e2d588331dd2093c7b23a728b0
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2019
ms.locfileid: "73444180"
---
# <a name="create-a-q-project-in-your-development-environment"></a><span data-ttu-id="bfbf0-103">Создание проекта Q # в среде разработки</span><span class="sxs-lookup"><span data-stu-id="bfbf0-103">Create a Q# project in your development environment</span></span>

<span data-ttu-id="bfbf0-104">Узнайте, как создать проект Q # с помощью КДК.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-104">Learn how to create a Q# project with the QDK.</span></span>

<span data-ttu-id="bfbf0-105">Проект Q # содержит файлы Q #, содержащие тактовый код, а также ведущее приложение для запуска тактовой программы.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-105">A Q# project contains Q# files containing quantum code, as well as a host program to run the quantum program.</span></span> <span data-ttu-id="bfbf0-106">Вы можете написать ведущее приложение на языках .NET C#, например, или в Python.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-106">You can write the host program in .NET languages such as C#, or in Python.</span></span> <span data-ttu-id="bfbf0-107">Вы также можете выполнить код Q # в записной книжке Jupyter с помощью ядра IQ #.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-107">You can also run Q# code in a Jupyter notebook using the IQ# kernel.</span></span>

<span data-ttu-id="bfbf0-108">Выберите среду разработки и язык в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bfbf0-108">Choose your development environment and language from the sections below:</span></span>

* [<span data-ttu-id="bfbf0-109">Python</span><span class="sxs-lookup"><span data-stu-id="bfbf0-109">Python</span></span>](#create-a-python-project)
* [<span data-ttu-id="bfbf0-110">Записные книжки Jupyter</span><span class="sxs-lookup"><span data-stu-id="bfbf0-110">Jupyter notebooks</span></span>](#create-a-jupyter-notebook-project)
* [<span data-ttu-id="bfbf0-111">C#с помощью Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bfbf0-111">C# with Visual Studio</span></span>](#create-a-c-project-on-windows-using-visual-studio)
* [<span data-ttu-id="bfbf0-112">C#с VS Code</span><span class="sxs-lookup"><span data-stu-id="bfbf0-112">C# with VS Code</span></span>](#create-a-c-project-using-vs-code)
* [<span data-ttu-id="bfbf0-113">C#с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="bfbf0-113">C# with the command line</span></span>](#create-a-c-project-using-the-dotnet-command-line-tool)

## <a name="create-a-python-project"></a><span data-ttu-id="bfbf0-114">Создание проекта Python</span><span class="sxs-lookup"><span data-stu-id="bfbf0-114">Create a Python project</span></span>

1. <span data-ttu-id="bfbf0-115">Технические условия</span><span class="sxs-lookup"><span data-stu-id="bfbf0-115">Pre-requisites</span></span>

     * <span data-ttu-id="bfbf0-116">[Пакет средств разработки тактов для Python](xref:microsoft.quantum.install#develop-with-python)</span><span class="sxs-lookup"><span data-stu-id="bfbf0-116">The [Quantum Development Kit for Python](xref:microsoft.quantum.install#develop-with-python)</span></span>

1. <span data-ttu-id="bfbf0-117">Создайте папку для проекта и перейдите к этой папке.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-117">Create a folder for your project, and navigate to that folder</span></span>

1. <span data-ttu-id="bfbf0-118">Создайте файл Q # с именем `Operation.qs`и добавьте в него код Q #.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-118">Create a Q# file called `Operation.qs`, and add your Q# code to it.</span></span> <span data-ttu-id="bfbf0-119">Пример.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-119">For example:</span></span>

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

1. <span data-ttu-id="bfbf0-120">Создайте файл узла Python с именем `host.py`, чтобы вызвать операцию Q #.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-120">Create a python host file called `host.py` to call your Q# operation.</span></span> <span data-ttu-id="bfbf0-121">Пример.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-121">For example:</span></span>

    ```python
    import qsharp

    from HelloWorld import SayHello

    SayHello.simulate()
    ```

1. <span data-ttu-id="bfbf0-122">Запустите программу.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-122">Run the program:</span></span>

    ```bash
    python host.py
    ```

1. <span data-ttu-id="bfbf0-123">Проверьте выходные данные.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-123">Verify the output.</span></span> <span data-ttu-id="bfbf0-124">Программа должна вывести следующие строки:</span><span class="sxs-lookup"><span data-stu-id="bfbf0-124">Your program should output the following lines:</span></span>

    ```bash
    Hello from quantum world!
    0
    ```

<span data-ttu-id="bfbf0-125">Теперь вы можете продолжить разработку тактовой программы.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-125">You can now continue to develop your quantum program.</span></span>

## <a name="create-a-jupyter-notebook-project"></a><span data-ttu-id="bfbf0-126">Создание проекта Jupyter Notebook</span><span class="sxs-lookup"><span data-stu-id="bfbf0-126">Create a Jupyter Notebook project</span></span>

1. <span data-ttu-id="bfbf0-127">Технические условия</span><span class="sxs-lookup"><span data-stu-id="bfbf0-127">Pre-requisites</span></span>

    * <span data-ttu-id="bfbf0-128">[Набор средств разработки тактов для записных книжек Jupyter](xref:microsoft.quantum.install#develop-with-jupyter-notebooks)</span><span class="sxs-lookup"><span data-stu-id="bfbf0-128">The [Quantum Development Kit for Jupyter notebooks](xref:microsoft.quantum.install#develop-with-jupyter-notebooks)</span></span>

1. <span data-ttu-id="bfbf0-129">Выполните следующую команду, чтобы запустить сервер записных книжек.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-129">Run the following command to start the notebook server:</span></span>

    ```bash
    jupyter notebook
    ```

1. <span data-ttu-id="bfbf0-130">Перейдите по URL-адресу, указанному в командной строке.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-130">Browse to the URL shown on the command line.</span></span> <span data-ttu-id="bfbf0-131">Пример: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85 ]</span><span class="sxs-lookup"><span data-stu-id="bfbf0-131">For example: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85]</span></span>

1. <span data-ttu-id="bfbf0-132">В браузере появится страница Jupyter.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-132">A Jupyter page appears in the browser.</span></span> <span data-ttu-id="bfbf0-133">На вкладке **файлы** выберите **создать** > **Q #** , чтобы создать записную книжку Jupyter с ядром Q #.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-133">On the **Files** tab, select **New** > **Q#** to create a Jupyter notebook with a Q# kernel.</span></span> <span data-ttu-id="bfbf0-134">Добавьте следующий код в первую ячейку записной книжки:</span><span class="sxs-lookup"><span data-stu-id="bfbf0-134">Add the following code to the first notebook cell:</span></span>

    ```qsharp
    operation SayHello() : Unit {
        Message("Hello from quantum world!");
    }
    ```

1. <span data-ttu-id="bfbf0-135">Выберите **ячейка** > **Запуск ячеек** для запуска записной книжки.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-135">Select **Cell** > **Run Cells** to run the notebook.</span></span> <span data-ttu-id="bfbf0-136">`SayHello` скоро появится в выходных данных ячейки:</span><span class="sxs-lookup"><span data-stu-id="bfbf0-136">`SayHello` will soon appear in the cell output:</span></span>

    ![Ячейка записной книжки Jupyter с кодом Q #](~/media/install-guide-jupyter.png)

    <span data-ttu-id="bfbf0-138">При запуске в записных книжках Jupyter компилируется код Q #, а Записная книжка выводит имя найденных операций.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-138">When running in Jupyter Notebooks, the Q# code is compiled, and the notebook outputs the name of the operation(s) that it finds.</span></span>

1. <span data-ttu-id="bfbf0-139">В новой ячейке имитируйте выполнение на компьютере-такте операции, которую вы только что создали, используя магическую `%simulate`:</span><span class="sxs-lookup"><span data-stu-id="bfbf0-139">In a new cell, simulate the execution in a quantum computer of the operation you just created by using the `%simulate` magic:</span></span>

    ![Jupyter ячейка записной книжки с% имитировать волшебность](~/media/install-guide-jupyter-simulate.png)

    <span data-ttu-id="bfbf0-141">Сообщение должно отобразиться на экране вместе с результатом вызванной операции (в данном случае это пустое значение).</span><span class="sxs-lookup"><span data-stu-id="bfbf0-141">You should see the message printed on the screen along with the result of the operation you invoked (in this case, empty).</span></span>

<span data-ttu-id="bfbf0-142">Теперь можно добавить другие операции Q #, чтобы продолжить разработку тактов.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-142">You can now add other Q# operations to continue your quantum development.</span></span>

## <a name="create-a-c-project-on-windows-using-visual-studio"></a><span data-ttu-id="bfbf0-143">Создание C# проекта в Windows с помощью Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bfbf0-143">Create a C# project on Windows, using Visual Studio</span></span>

1. <span data-ttu-id="bfbf0-144">Технические условия</span><span class="sxs-lookup"><span data-stu-id="bfbf0-144">Pre-requisites</span></span>

    * <span data-ttu-id="bfbf0-145">[Пакет средств разработки тактов для Visual Studio](xref:microsoft.quantum.install#develop-with-c-on-windows-using-visual-studio)</span><span class="sxs-lookup"><span data-stu-id="bfbf0-145">The [Quantum Development Kit for Visual Studio](xref:microsoft.quantum.install#develop-with-c-on-windows-using-visual-studio)</span></span>

1. <span data-ttu-id="bfbf0-146">Создайте приложение Q#.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-146">Create a new Q# application</span></span>

    * <span data-ttu-id="bfbf0-147">Выберите **Файл** -> **Создать** -> **Проект**.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-147">Go to **File** -> **New** -> **Project**</span></span>
    * <span data-ttu-id="bfbf0-148">Введите `Q#` в поле поиска.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-148">Type `Q#` in the search box</span></span>
    * <span data-ttu-id="bfbf0-149">Выберите **Приложение Q#** .</span><span class="sxs-lookup"><span data-stu-id="bfbf0-149">Select **Q# Application**</span></span>
    * <span data-ttu-id="bfbf0-150">Щелкните **Далее**.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-150">Select **Next**</span></span>
    * <span data-ttu-id="bfbf0-151">Выберите имя и расположение для приложения.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-151">Choose a name and location for your application</span></span>
    * <span data-ttu-id="bfbf0-152">Нажмите кнопку **Создать**</span><span class="sxs-lookup"><span data-stu-id="bfbf0-152">Select **Create**</span></span>

1. <span data-ttu-id="bfbf0-153">Проверьте проект.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-153">Inspect the project</span></span>

    <span data-ttu-id="bfbf0-154">Должны быть созданы два файла: `Driver.cs` — ведущее приложение C#; и `Operation.qs` — программа Q#, которая определяет простую операцию вывода сообщения в консоль.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-154">You should see that two files have been created: `Driver.cs`, which is the C# host application; and `Operation.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

1. <span data-ttu-id="bfbf0-155">Выполнение приложения</span><span class="sxs-lookup"><span data-stu-id="bfbf0-155">Run the application</span></span>

    * <span data-ttu-id="bfbf0-156">Выберите **Отладка** -> **Запустить без отладки**.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-156">Select **Debug** -> **Start Without Debugging**</span></span>
    * <span data-ttu-id="bfbf0-157">В окне консоли должен отобразиться текст `Hello quantum world!`.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-157">You should see the text `Hello quantum world!` printed to a console window.</span></span>

<span data-ttu-id="bfbf0-158">Теперь вы можете продолжить разработку тактов с помощью Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-158">You can now continue your quantum development using Visual Studio</span></span>

> [!NOTE]
> * <span data-ttu-id="bfbf0-159">Если в одном решении Visual Studio несколько проектов, все проекты, включенные в решение, нужно разместить в той же папке, что и решение, или в одной из вложенных в нее папок.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-159">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its subfolders.</span></span>  

## <a name="create-a-c-project-using-vs-code"></a><span data-ttu-id="bfbf0-160">Создание C# проекта с помощью VS Code</span><span class="sxs-lookup"><span data-stu-id="bfbf0-160">Create a C# project, using VS Code</span></span>

1. <span data-ttu-id="bfbf0-161">Технические условия</span><span class="sxs-lookup"><span data-stu-id="bfbf0-161">Pre-requisites</span></span>

    * <span data-ttu-id="bfbf0-162">[Пакет средств разработки тактов для VS Code](xref:microsoft.quantum.install#develop-with-c-using-visual-studio-code)</span><span class="sxs-lookup"><span data-stu-id="bfbf0-162">The [Quantum Development Kit for VS Code](xref:microsoft.quantum.install#develop-with-c-using-visual-studio-code)</span></span>

1. <span data-ttu-id="bfbf0-163">Создайте новый проект:</span><span class="sxs-lookup"><span data-stu-id="bfbf0-163">Create a new project:</span></span>

    * <span data-ttu-id="bfbf0-164">Выберите **Представление** -> **Палитра команд**.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-164">Go to **View** -> **Command Palette**</span></span>
    * <span data-ttu-id="bfbf0-165">Выберите **Q #: создать новый проект**</span><span class="sxs-lookup"><span data-stu-id="bfbf0-165">Select **Q#: Create New Project**</span></span>
    * <span data-ttu-id="bfbf0-166">Перейдите в расположение файловой системы, в котором необходимо создать приложение.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-166">Navigate to the location on the file system where you would like to create the application</span></span>
    * <span data-ttu-id="bfbf0-167">После создания проекта нажмите кнопку **Open new project...** (Открыть новый проект...).</span><span class="sxs-lookup"><span data-stu-id="bfbf0-167">Click on the **Open new project...** button, once the project has been created</span></span>

1. <span data-ttu-id="bfbf0-168">Запустите приложение:</span><span class="sxs-lookup"><span data-stu-id="bfbf0-168">Run the application:</span></span>

    * <span data-ttu-id="bfbf0-169">Выберите **Отладка** -> **Запустить без отладки**.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-169">Go to **Debug** -> **Start Without Debugging**</span></span>
    * <span data-ttu-id="bfbf0-170">В окне консоли `Hello quantum world!` должен отобразиться следующий текст.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-170">You should see the following text in the output window `Hello quantum world!`</span></span>

<span data-ttu-id="bfbf0-171">Теперь можно продолжить разработку тактов с помощью Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-171">You can now continue your quantum development using Visual Studio Code.</span></span>

> [!NOTE]
> * <span data-ttu-id="bfbf0-172">Сейчас рабочие области с несколькими корневыми папками не поддерживаются в расширении Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-172">Workspaces with multiple root folders are not currently supported by the Visual Studio Code extension.</span></span> <span data-ttu-id="bfbf0-173">Если в одной рабочей области VS Code несколько проектов, все проекты нужно разместить в одной корневой папке.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-173">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

## <a name="create-a-c-project-using-the-dotnet-command-line-tool"></a><span data-ttu-id="bfbf0-174">Создание C# проекта с помощью средства командной строки `dotnet`</span><span class="sxs-lookup"><span data-stu-id="bfbf0-174">Create a C# project, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="bfbf0-175">Технические условия</span><span class="sxs-lookup"><span data-stu-id="bfbf0-175">Pre-requisites</span></span>

    * <span data-ttu-id="bfbf0-176">[Пакет средств разработки тактов для командной строки](xref:microsoft.quantum.install#develop-with-c-using-the-dotnet-command-line-tool)</span><span class="sxs-lookup"><span data-stu-id="bfbf0-176">The [Quantum Development Kit for the Command Line](xref:microsoft.quantum.install#develop-with-c-using-the-dotnet-command-line-tool)</span></span>

1. <span data-ttu-id="bfbf0-177">Создание приложения</span><span class="sxs-lookup"><span data-stu-id="bfbf0-177">Create a new application</span></span>

    ```bash
    dotnet new console -lang Q# -o <project name>
    ```

1. <span data-ttu-id="bfbf0-178">Перейдите в новый каталог приложения</span><span class="sxs-lookup"><span data-stu-id="bfbf0-178">Navigate to the new application directory</span></span>

    ```bash
    cd <project name>
    ```

    <span data-ttu-id="bfbf0-179">Должны быть созданы два файла, а также файлы проекта приложения: файл Q# (`Operation.qs`) и файл узла C# (`Driver.cs`).</span><span class="sxs-lookup"><span data-stu-id="bfbf0-179">You should see that two files have been created, along with the project files of the application: a Q# file (`Operation.qs`) and a C# host file (`Driver.cs`).</span></span>

1. <span data-ttu-id="bfbf0-180">Выполнение приложения</span><span class="sxs-lookup"><span data-stu-id="bfbf0-180">Run the application</span></span>

    ```bash
    dotnet run
    ```

    <span data-ttu-id="bfbf0-181">Вы должны увидеть следующий результат: `Hello quantum world!`.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-181">You should see the following output: `Hello quantum world!`</span></span>

<span data-ttu-id="bfbf0-182">Теперь вы можете продолжить разработку тактов с помощью средств командной строки.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-182">You now continue your quantum development, using command line tools.</span></span>

## <a name="whats-next"></a><span data-ttu-id="bfbf0-183">Что дальше?</span><span class="sxs-lookup"><span data-stu-id="bfbf0-183">What's next?</span></span>

<span data-ttu-id="bfbf0-184">После создания проекта в предпочитаемой среде можно продолжить разработку тактов.</span><span class="sxs-lookup"><span data-stu-id="bfbf0-184">Now that you have created a project in your preferred environment, you can continue your quantum development.</span></span>
