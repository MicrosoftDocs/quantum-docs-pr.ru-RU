---
title: 'Разработка с помощью Q # +C#'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.cs
ms.openlocfilehash: 7803846279f230f5fc0ee8424bd39be735a650ca
ms.sourcegitcommit: 5094c0a60cbafdee669c8728b92df281071259b9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2020
ms.locfileid: "77036293"
---
# <a name="develop-with-q--c"></a><span data-ttu-id="7f421-102">Разработка с помощью Q # +C#</span><span class="sxs-lookup"><span data-stu-id="7f421-102">Develop with Q# + C#</span></span>

<span data-ttu-id="7f421-103">Установите КДК для разработки C# программ размещения, чтобы вызвать операции Q #.</span><span class="sxs-lookup"><span data-stu-id="7f421-103">Install the QDK to develop C# host programs to call Q# operations.</span></span>

<span data-ttu-id="7f421-104">Функция Q # разработана для корректного воспроизведения с помощью языков .NET, C#а именно.</span><span class="sxs-lookup"><span data-stu-id="7f421-104">Q# is built to play well with .NET languages--specifically C#.</span></span> <span data-ttu-id="7f421-105">Вы можете работать с этой парой в разных средах разработки:</span><span class="sxs-lookup"><span data-stu-id="7f421-105">You can work with this pairing inside different development environments:</span></span>

- [<span data-ttu-id="7f421-106">Вопросы и ответы C# # + использование Visual Studio (Windows)</span><span class="sxs-lookup"><span data-stu-id="7f421-106">Q# + C# using Visual Studio (Windows)</span></span>](#VS)
- [<span data-ttu-id="7f421-107">Q # + C# использование Visual Studio Code (Windows, Linux и Mac)</span><span class="sxs-lookup"><span data-stu-id="7f421-107">Q# + C# using Visual Studio Code (Windows, Linux and Mac)</span></span>](#VSC)
- [<span data-ttu-id="7f421-108">Q # + C# использование программы командной строки `dotnet`</span><span class="sxs-lookup"><span data-stu-id="7f421-108">Q# + C# using the `dotnet` command-line tool</span></span>](#command)

## <span data-ttu-id="7f421-109">Разработка с помощью Q # C# + и Visual Studio <a name="VS"></a></span><span class="sxs-lookup"><span data-stu-id="7f421-109">Develop with Q# + C# using Visual Studio <a name="VS"></a></span></span>

<span data-ttu-id="7f421-110">Visual Studio предлагает обширную среду для разработки программ Q #.</span><span class="sxs-lookup"><span data-stu-id="7f421-110">Visual Studio offers a rich environment for developing Q# programs.</span></span> <span data-ttu-id="7f421-111">Расширение Q # Visual Studio содержит шаблоны для Q # файлов и проектов, а также выделения синтаксиса, завершения кода и поддержки IntelliSense.</span><span class="sxs-lookup"><span data-stu-id="7f421-111">The Q# Visual Studio extension contains templates for Q# files and projects as well as syntax highlighting, code completion and IntelliSense support.</span></span>


1. <span data-ttu-id="7f421-112">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="7f421-112">Pre-requisites</span></span>

    - <span data-ttu-id="7f421-113">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 с включенной рабочей нагрузкой кроссплатформенной разработки .NET Core.</span><span class="sxs-lookup"><span data-stu-id="7f421-113">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, with the .NET Core cross-platform development workload enabled</span></span>

1. <span data-ttu-id="7f421-114">Установите расширение Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7f421-114">Install the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="7f421-115">Скачивание и установка [расширения Visual Studio](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span><span class="sxs-lookup"><span data-stu-id="7f421-115">Download and install the [Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>

1. <span data-ttu-id="7f421-116">Проверьте установку, создав приложение `Hello World`.</span><span class="sxs-lookup"><span data-stu-id="7f421-116">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="7f421-117">Создайте приложение Q#.</span><span class="sxs-lookup"><span data-stu-id="7f421-117">Create a new Q# application</span></span>

        - <span data-ttu-id="7f421-118">Выберите **Файл** -> **Создать** -> **Проект**.</span><span class="sxs-lookup"><span data-stu-id="7f421-118">Go to **File** -> **New** -> **Project**</span></span>
        - <span data-ttu-id="7f421-119">Введите `Q#` в поле поиска.</span><span class="sxs-lookup"><span data-stu-id="7f421-119">Type `Q#` in the search box</span></span>
        - <span data-ttu-id="7f421-120">Выберите **Приложение Q#** .</span><span class="sxs-lookup"><span data-stu-id="7f421-120">Select **Q# Application**</span></span>
        - <span data-ttu-id="7f421-121">Щелкните **Далее**.</span><span class="sxs-lookup"><span data-stu-id="7f421-121">Select **Next**</span></span>
        - <span data-ttu-id="7f421-122">Выберите имя и расположение для приложения.</span><span class="sxs-lookup"><span data-stu-id="7f421-122">Choose a name and location for your application</span></span>
        - <span data-ttu-id="7f421-123">Нажмите кнопку **Создать**</span><span class="sxs-lookup"><span data-stu-id="7f421-123">Select **Create**</span></span>

    - <span data-ttu-id="7f421-124">Проверьте проект.</span><span class="sxs-lookup"><span data-stu-id="7f421-124">Inspect the project</span></span>

        <span data-ttu-id="7f421-125">Должны быть созданы два файла: `Driver.cs` — ведущее приложение C#; и `Operation.qs` — программа Q#, которая определяет простую операцию вывода сообщения в консоль.</span><span class="sxs-lookup"><span data-stu-id="7f421-125">You should see that two files have been created: `Driver.cs`, which is the C# host application; and `Operation.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

    - <span data-ttu-id="7f421-126">Выполнение приложения</span><span class="sxs-lookup"><span data-stu-id="7f421-126">Run the application</span></span>

        - <span data-ttu-id="7f421-127">Выберите **Отладка** -> **Запустить без отладки**.</span><span class="sxs-lookup"><span data-stu-id="7f421-127">Select **Debug** -> **Start Without Debugging**</span></span>
        - <span data-ttu-id="7f421-128">В окне консоли должен отобразиться текст `Hello quantum world!`.</span><span class="sxs-lookup"><span data-stu-id="7f421-128">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> * <span data-ttu-id="7f421-129">Если в одном решении Visual Studio несколько проектов, все проекты, включенные в решение, нужно разместить в той же папке, что и решение, или в одной из вложенных в нее папок.</span><span class="sxs-lookup"><span data-stu-id="7f421-129">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its subfolders.</span></span>  

## <span data-ttu-id="7f421-130">Разработка с помощью Q # C# + Visual Studio Code <a name="VSC"></a></span><span class="sxs-lookup"><span data-stu-id="7f421-130">Develop with Q# + C# using Visual Studio Code <a name="VSC"></a></span></span>

<span data-ttu-id="7f421-131">Visual Studio Code (VS Code) предоставляет обширную среду для разработки программ Q # в Windows, Linux и Mac.</span><span class="sxs-lookup"><span data-stu-id="7f421-131">Visual Studio Code (VS Code) offers a rich environment for developing Q# programs on Windows, Linux and Mac.</span></span>  <span data-ttu-id="7f421-132">Расширение Q # VS Code включает поддержку выделения синтаксиса Q #, завершения кода и фрагментов кода Q #.</span><span class="sxs-lookup"><span data-stu-id="7f421-132">The Q# VS Code extension includes support for Q# syntax highlighting, code completion, and Q# code snippets.</span></span>

1. <span data-ttu-id="7f421-133">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="7f421-133">Pre-requisites</span></span>

   - [<span data-ttu-id="7f421-134">Код VS</span><span class="sxs-lookup"><span data-stu-id="7f421-134">VS Code</span></span>](https://code.visualstudio.com/download)
   - [<span data-ttu-id="7f421-135">Пакет SDK для .NET Core 3,1 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="7f421-135">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="7f421-136">Установите расширение Quantum VS Code.</span><span class="sxs-lookup"><span data-stu-id="7f421-136">Install the Quantum VS Code extension</span></span>

    - <span data-ttu-id="7f421-137">Установите [расширение VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="7f421-137">Install the [VS Code extension](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)</span></span>

1. <span data-ttu-id="7f421-138">Установите шаблоны проектов Quantum.</span><span class="sxs-lookup"><span data-stu-id="7f421-138">Install the Quantum project templates:</span></span>

   - <span data-ttu-id="7f421-139">Выберите **Представление** -> **Палитра команд**.</span><span class="sxs-lookup"><span data-stu-id="7f421-139">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="7f421-140">Выбор **Q #: Установка шаблонов проектов**</span><span class="sxs-lookup"><span data-stu-id="7f421-140">Select **Q#: Install project templates**</span></span>

    <span data-ttu-id="7f421-141">Теперь Quantum Development Kit установлен и готов к использованию в ваших приложениях и библиотеках.</span><span class="sxs-lookup"><span data-stu-id="7f421-141">You now have the Quantum Development Kit installed and ready to use in your own applications and libraries.</span></span>

1. <span data-ttu-id="7f421-142">Проверьте установку, создав приложение `Hello World`.</span><span class="sxs-lookup"><span data-stu-id="7f421-142">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="7f421-143">Создайте новый проект:</span><span class="sxs-lookup"><span data-stu-id="7f421-143">Create a new project:</span></span>

        - <span data-ttu-id="7f421-144">Выберите **Представление** -> **Палитра команд**.</span><span class="sxs-lookup"><span data-stu-id="7f421-144">Go to **View** -> **Command Palette**</span></span>
        - <span data-ttu-id="7f421-145">Выберите **Q #: создать новый проект**</span><span class="sxs-lookup"><span data-stu-id="7f421-145">Select **Q#: Create New Project**</span></span>
        - <span data-ttu-id="7f421-146">Выберите **автономное консольное приложение**</span><span class="sxs-lookup"><span data-stu-id="7f421-146">Select **Standalone console application**</span></span>
        - <span data-ttu-id="7f421-147">Перейдите в расположение файловой системы, в котором необходимо создать приложение.</span><span class="sxs-lookup"><span data-stu-id="7f421-147">Navigate to the location on the file system where you would like to create the application</span></span>
        - <span data-ttu-id="7f421-148">После создания проекта нажмите кнопку **Open new project...** (Открыть новый проект...).</span><span class="sxs-lookup"><span data-stu-id="7f421-148">Click on the **Open new project...** button, once the project has been created</span></span>

    - <span data-ttu-id="7f421-149">Если вы еще не установили C# расширение для VS Code, появится всплывающее окно.</span><span class="sxs-lookup"><span data-stu-id="7f421-149">If you don't already have the C# extension for VS Code installed, a pop-up will appear.</span></span> <span data-ttu-id="7f421-150">Установите расширение.</span><span class="sxs-lookup"><span data-stu-id="7f421-150">Install the extension.</span></span> 

    - <span data-ttu-id="7f421-151">Запустите приложение:</span><span class="sxs-lookup"><span data-stu-id="7f421-151">Run the application:</span></span>

        - <span data-ttu-id="7f421-152">Последовательно выберите **терминал** -> **Новый терминал** .</span><span class="sxs-lookup"><span data-stu-id="7f421-152">Go to **Terminal** -> **New Terminal**</span></span>
        - <span data-ttu-id="7f421-153">Введите `dotnet run`</span><span class="sxs-lookup"><span data-stu-id="7f421-153">Enter `dotnet run`</span></span>
        - <span data-ttu-id="7f421-154">В окне консоли `Hello quantum world!` должен отобразиться следующий текст.</span><span class="sxs-lookup"><span data-stu-id="7f421-154">You should see the following text in the output window `Hello quantum world!`</span></span>


> [!NOTE]
> * <span data-ttu-id="7f421-155">Сейчас рабочие области с несколькими корневыми папками не поддерживаются в расширении Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="7f421-155">Workspaces with multiple root folders are not currently supported by the Visual Studio Code extension.</span></span> <span data-ttu-id="7f421-156">Если в одной рабочей области VS Code несколько проектов, все проекты нужно разместить в одной корневой папке.</span><span class="sxs-lookup"><span data-stu-id="7f421-156">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

## <span data-ttu-id="7f421-157">Разработка с использованием Q # C# + с помощью средства командной строки `dotnet`<a name="command"></a></span><span class="sxs-lookup"><span data-stu-id="7f421-157">Develop with Q# + C# using the `dotnet` command-line tool <a name="command"></a></span></span>

<span data-ttu-id="7f421-158">Разумеется, вы можете создавать и запускать программы Q# и из командной строки. Для этого просто установите шаблоны проектов на основе пакетов QDK и SDK для .NET Core.</span><span class="sxs-lookup"><span data-stu-id="7f421-158">Of course, you can also build and run Q# programs from the command line by simply installing the .NET Core SDK and the QDK project templates.</span></span> 

1. <span data-ttu-id="7f421-159">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="7f421-159">Pre-requisites</span></span>

    - [<span data-ttu-id="7f421-160">Пакет SDK для .NET Core 3,1 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="7f421-160">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="7f421-161">Установите шаблоны проектов Quantum для .NET.</span><span class="sxs-lookup"><span data-stu-id="7f421-161">Install the Quantum project templates for .NET</span></span>

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

    <span data-ttu-id="7f421-162">Теперь Quantum Development Kit установлен и готов к использованию в ваших приложениях и библиотеках.</span><span class="sxs-lookup"><span data-stu-id="7f421-162">You now have the Quantum Development Kit installed and ready to use in your own applications and libraries.</span></span>

1. <span data-ttu-id="7f421-163">Проверьте установку, создав приложение `Hello World`.</span><span class="sxs-lookup"><span data-stu-id="7f421-163">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="7f421-164">Создание приложения</span><span class="sxs-lookup"><span data-stu-id="7f421-164">Create a new application</span></span>

       ```dotnetcli
       dotnet new console -lang "Q#" -o runSayHello
       ```

    - <span data-ttu-id="7f421-165">Перейдите в новый каталог приложения</span><span class="sxs-lookup"><span data-stu-id="7f421-165">Navigate to the new application directory</span></span>

       ```bash
       cd runSayHello
       ```

    <span data-ttu-id="7f421-166">Должны быть созданы два файла, а также файлы проекта приложения: файл Q# (`Operation.qs`) и файл узла C# (`Driver.cs`).</span><span class="sxs-lookup"><span data-stu-id="7f421-166">You should see that two files have been created, along with the project files of the application: a Q# file (`Operation.qs`) and a C# host file (`Driver.cs`).</span></span>

    - <span data-ttu-id="7f421-167">Выполнение приложения</span><span class="sxs-lookup"><span data-stu-id="7f421-167">Run the application</span></span>

        ```dotnetcli
        dotnet run
        ```

        <span data-ttu-id="7f421-168">Вы должны увидеть следующий результат: `Hello quantum world!`.</span><span class="sxs-lookup"><span data-stu-id="7f421-168">You should see the following output: `Hello quantum world!`</span></span>

    
## <a name="whats-next"></a><span data-ttu-id="7f421-169">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="7f421-169">What's next?</span></span>

<span data-ttu-id="7f421-170">После установки Quantum Development Kit в предпочитаемой среде вы можете написать и запустить [первую квантовую программу](xref:microsoft.quantum.write-program).</span><span class="sxs-lookup"><span data-stu-id="7f421-170">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
