---
title: Разработка приложений Q#
description: Сведения о том, как создать приложение Q#, запускаемое из командной строки.
author: bradben
ms.author: v-benbra
ms.date: 8/20/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
no-loc:
- Q#
- $$v
ms.openlocfilehash: 68f530d80e5c5f40dc2bcbb185879c3cb6f93f91
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834420"
---
# <a name="develop-with-no-locq-applications"></a><span data-ttu-id="1a99a-103">Разработка приложений Q#</span><span class="sxs-lookup"><span data-stu-id="1a99a-103">Develop with Q# applications</span></span>

<span data-ttu-id="1a99a-104">Следуйте инструкциям на вкладке для вашей среды.</span><span class="sxs-lookup"><span data-stu-id="1a99a-104">Follow the instructions at the tab corresponding to your environment.</span></span>

<span data-ttu-id="1a99a-105">Программы Q# могут выполняться самостоятельно (без драйвера) на основном языке, например C#, F# или Python.</span><span class="sxs-lookup"><span data-stu-id="1a99a-105">Q# programs can run on their own, without a driver in a host language like C#, F#, or Python.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1a99a-106">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="1a99a-106">Prerequisites</span></span>

- [<span data-ttu-id="1a99a-107">Пакет SDK для .NET Core 3.1 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="1a99a-107">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

## <a name="installation"></a><span data-ttu-id="1a99a-108">Установка</span><span class="sxs-lookup"><span data-stu-id="1a99a-108">Installation</span></span>

<span data-ttu-id="1a99a-109">Вы можете создавать приложения Q# в любой интегрированной среде разработки. Но мы рекомендуем использовать для локальной разработки приложений Q# интегрированную среду разработки Visual Studio Code (VS Code) или Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="1a99a-109">While you can build Q# applications in any IDE, we recommend using Visual Studio Code (VS Code) or Visual Studio IDE for developing your Q# applications locally.</span></span> <span data-ttu-id="1a99a-110">Для разработки в облаке с помощью веб-браузера мы рекомендуем использовать Visual Studio Codespaces.</span><span class="sxs-lookup"><span data-stu-id="1a99a-110">For developing in the Cloud via the web browser, we recommend Visual Studio Codespaces.</span></span> <span data-ttu-id="1a99a-111">При разработке в таких средах вам доступны широкие возможности расширения QDK, такие как предупреждения, выделение синтаксиса, шаблоны проектов и многие другие.</span><span class="sxs-lookup"><span data-stu-id="1a99a-111">Developing in these environments includes the rich functionality of the QDK extension, which includes warnings, syntax highlighting, project templates, and more.</span></span> 

<span data-ttu-id="1a99a-112">Чтобы настроить VS Code, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1a99a-112">To configure VS Code:</span></span>

1. <span data-ttu-id="1a99a-113">Скачайте и установите [VS Code](https://code.visualstudio.com/download) (Windows, Linux и Mac).</span><span class="sxs-lookup"><span data-stu-id="1a99a-113">Download and install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac).</span></span>
2. <span data-ttu-id="1a99a-114">Установите [Microsoft QDK для VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="1a99a-114">Install the [Microsoft QDK for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

<span data-ttu-id="1a99a-115">Чтобы настроить Visual Studio, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1a99a-115">To configure Visual Studio:</span></span>

1. <span data-ttu-id="1a99a-116">Скачайте и установите [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 или более новой версии с включенной рабочей нагрузкой кроссплатформенной разработки .NET Core.</span><span class="sxs-lookup"><span data-stu-id="1a99a-116">Download and install [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 or greater, with the .NET Core cross-platform development workload enabled.</span></span>
2. <span data-ttu-id="1a99a-117">Скачайте и установите [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span><span class="sxs-lookup"><span data-stu-id="1a99a-117">Download and install the [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span></span>

<span data-ttu-id="1a99a-118">Чтобы настроить Visual Studio Codespaces, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="1a99a-118">To configure Visual Studio Codespaces:</span></span>

1. <span data-ttu-id="1a99a-119">Создайте [учетную запись Azure](https://azure.microsoft.com/free/).</span><span class="sxs-lookup"><span data-stu-id="1a99a-119">Create an [Azure account](https://azure.microsoft.com/free/).</span></span>
2. <span data-ttu-id="1a99a-120">Создайте среду Codespaces.</span><span class="sxs-lookup"><span data-stu-id="1a99a-120">Create a Codespaces environment.</span></span> <span data-ttu-id="1a99a-121">Выполните инструкции из [этого краткого руководства](https://docs.microsoft.com/visualstudio/codespaces/quickstarts/browser).</span><span class="sxs-lookup"><span data-stu-id="1a99a-121">Please follow the [quickstart guide](https://docs.microsoft.com/visualstudio/codespaces/quickstarts/browser).</span></span> <span data-ttu-id="1a99a-122">При создании Codespaces рекомендуется ввести `microsoft/Quantum` в поле Git Repository (Репозиторий Git), чтобы загрузить параметры, связанные с QDK.</span><span class="sxs-lookup"><span data-stu-id="1a99a-122">When creating the Codespace, we recommend to enter `microsoft/Quantum` in the "Git Repository" field to load QDK-specific settings.</span></span>
3. <span data-ttu-id="1a99a-123">Теперь вы можете запустить новую среду и начать разработку в браузере с помощью [облачной интегрированной среды разработки Visual Studio Codespaces](https://online.visualstudio.com/environments).</span><span class="sxs-lookup"><span data-stu-id="1a99a-123">You can now launch your new environment and start developing in the browser via the [VS Codespaces Cloud IDE](https://online.visualstudio.com/environments).</span></span> <span data-ttu-id="1a99a-124">Кроме того, можно использовать локальную установку VS Code и использовать Codespaces в качестве [удаленной среды](https://docs.microsoft.com/visualstudio/online/how-to/vscode).</span><span class="sxs-lookup"><span data-stu-id="1a99a-124">Alternatively, it is possible to use your local installation of VS Code and use Codespaces as a [remote environment](https://docs.microsoft.com/visualstudio/online/how-to/vscode).</span></span>


<span data-ttu-id="1a99a-125">Чтобы установить QDK для другой среды, выполните в командной строке следующую команду:</span><span class="sxs-lookup"><span data-stu-id="1a99a-125">To install the QDK for another environment, enter the following at the command prompt:</span></span>

```dotnetcli
dotnet new -i Microsoft.Quantum.ProjectTemplates
```

## <a name="develop-with-no-locq"></a><span data-ttu-id="1a99a-126">Разработка на Q#</span><span class="sxs-lookup"><span data-stu-id="1a99a-126">Develop with Q#</span></span>

<span data-ttu-id="1a99a-127">Следуйте инструкциям на вкладке для вашей среды.</span><span class="sxs-lookup"><span data-stu-id="1a99a-127">Follow the instructions on the tab corresponding to your environment.</span></span>

### <a name="vs-code"></a>[<span data-ttu-id="1a99a-128">Код VS</span><span class="sxs-lookup"><span data-stu-id="1a99a-128">VS Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="1a99a-129">Чтобы создать новый проект, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1a99a-129">To create a new project:</span></span>

1. <span data-ttu-id="1a99a-130">Щелкните **Представление** -> **Палитра команд** и выберите **Q#: создать проект**.</span><span class="sxs-lookup"><span data-stu-id="1a99a-130">Click **View** -> **Command Palette** and select **Q#: Create New Project**.</span></span>
2. <span data-ttu-id="1a99a-131">Щелкните **Standalone console application** (Автономное консольное приложение).</span><span class="sxs-lookup"><span data-stu-id="1a99a-131">Click **Standalone console application**.</span></span>
3. <span data-ttu-id="1a99a-132">Перейдите к расположению, в котором нужно сохранить проект, и щелкните **Создать проект**.</span><span class="sxs-lookup"><span data-stu-id="1a99a-132">Navigate to the location to save the project and click **Create Project**.</span></span>
4. <span data-ttu-id="1a99a-133">После успешного создания проекта нажмите **Открыть новый проект...** в правом нижнем углу.</span><span class="sxs-lookup"><span data-stu-id="1a99a-133">When the project is successfully created, click **Open new project...** in the lower right.</span></span>

<span data-ttu-id="1a99a-134">Проверьте проект.</span><span class="sxs-lookup"><span data-stu-id="1a99a-134">Inspect the project.</span></span> <span data-ttu-id="1a99a-135">Вы увидите исходный файл с именем `Program.qs`, который представляет собой программу Q#, определяющую простую операцию вывода сообщения в консоль.</span><span class="sxs-lookup"><span data-stu-id="1a99a-135">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="1a99a-136">Чтобы запустить приложение, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="1a99a-136">To run the application:</span></span>

1. <span data-ttu-id="1a99a-137">Щелкните **Терминал** -> **Создать терминал**.</span><span class="sxs-lookup"><span data-stu-id="1a99a-137">Click **Terminal** -> **New Terminal**.</span></span>
2. <span data-ttu-id="1a99a-138">В командной строке терминала введите `dotnet run`.</span><span class="sxs-lookup"><span data-stu-id="1a99a-138">At the terminal prompt, enter `dotnet run`.</span></span>
3. <span data-ttu-id="1a99a-139">В окне консоли `Hello quantum world!` должен отобразиться следующий текст.</span><span class="sxs-lookup"><span data-stu-id="1a99a-139">You should see the following text in the output window `Hello quantum world!`</span></span>

> [!NOTE]
> <span data-ttu-id="1a99a-140">В настоящее время рабочие области с несколькими корневыми папками не поддерживаются в расширении Q# для VS Code.</span><span class="sxs-lookup"><span data-stu-id="1a99a-140">Workspaces with multiple root folders are not currently supported by the VS Code Q# extension.</span></span> <span data-ttu-id="1a99a-141">Если в одной рабочей области VS Code несколько проектов, все проекты нужно разместить в одной корневой папке.</span><span class="sxs-lookup"><span data-stu-id="1a99a-141">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

### <a name="visual-studio"></a>[<span data-ttu-id="1a99a-142">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1a99a-142">Visual Studio</span></span>](#tab/tabid-vs)

<span data-ttu-id="1a99a-143">Проверьте установку Visual Studio, создав приложение `Hello World` на Q#.</span><span class="sxs-lookup"><span data-stu-id="1a99a-143">Verify your Visual Studio installation by creating a Q# `Hello World` application.</span></span>

<span data-ttu-id="1a99a-144">Чтобы создать приложение на Q#:</span><span class="sxs-lookup"><span data-stu-id="1a99a-144">To create a new Q# application:</span></span>

1. <span data-ttu-id="1a99a-145">Откройте Visual Studio и щелкните **Файл** -> **Создать** -> **Проект**.</span><span class="sxs-lookup"><span data-stu-id="1a99a-145">Open Visual Studio and click **File** -> **New** -> **Project**.</span></span>
2. <span data-ttu-id="1a99a-146">Введите `Q#` в поле поиска, выберите **Q# Application** (Приложение Q#) и щелкните **Далее**.</span><span class="sxs-lookup"><span data-stu-id="1a99a-146">Type `Q#` in the search box, select **Q# Application** and click **Next**.</span></span>
3. <span data-ttu-id="1a99a-147">Введите имя и расположение приложения и щелкните **Создать**.</span><span class="sxs-lookup"><span data-stu-id="1a99a-147">Enter a name and location for your application and click **Create**.</span></span>


<span data-ttu-id="1a99a-148">Проверьте проект.</span><span class="sxs-lookup"><span data-stu-id="1a99a-148">Inspect the project.</span></span> <span data-ttu-id="1a99a-149">Вы увидите исходный файл с именем `Program.qs`, который представляет собой программу Q#, определяющую простую операцию вывода сообщения в консоль.</span><span class="sxs-lookup"><span data-stu-id="1a99a-149">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="1a99a-150">Чтобы запустить приложение, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="1a99a-150">To run the application:</span></span>

1. <span data-ttu-id="1a99a-151">Выберите **Отладка** -> **Запустить без отладки**.</span><span class="sxs-lookup"><span data-stu-id="1a99a-151">Select **Debug** -> **Start Without Debugging**.</span></span>
2. <span data-ttu-id="1a99a-152">В окне консоли должен отобразиться текст `Hello quantum world!`.</span><span class="sxs-lookup"><span data-stu-id="1a99a-152">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> <span data-ttu-id="1a99a-153">Если в одном решении Visual Studio несколько проектов, все включенные в него проекты нужно разместить в той же папке, что и решение, или в одной из вложенных в нее папок.</span><span class="sxs-lookup"><span data-stu-id="1a99a-153">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its sub-folders.</span></span>  

### <a name="other-editors-with-the-command-prompt"></a>[<span data-ttu-id="1a99a-154">Другие редакторы с командной строкой</span><span class="sxs-lookup"><span data-stu-id="1a99a-154">Other editors with the command prompt</span></span>](#tab/tabid-cmdline)

<span data-ttu-id="1a99a-155">Проверьте установку, создав на Q# приложение `Hello World`.</span><span class="sxs-lookup"><span data-stu-id="1a99a-155">Verify your installation by creating a Q# `Hello World` application.</span></span>

1. <span data-ttu-id="1a99a-156">Установите шаблоны проектов.</span><span class="sxs-lookup"><span data-stu-id="1a99a-156">Install the project templates.</span></span>

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

1. <span data-ttu-id="1a99a-157">Создайте новое приложение:</span><span class="sxs-lookup"><span data-stu-id="1a99a-157">Create a new application:</span></span>

    ```dotnetcli
    dotnet new console -lang Q# -o runSayHello
    ```

1. <span data-ttu-id="1a99a-158">Перейдите в каталог приложения:</span><span class="sxs-lookup"><span data-stu-id="1a99a-158">Navigate to the application directory:</span></span>

    ```dotnetcli
    cd runSayHello
    ```

    <span data-ttu-id="1a99a-159">Этот каталог теперь должен содержать файл `Program.qs`, который представляет собой программу Q#, определяющую простую операцию вывода сообщения в консоль.</span><span class="sxs-lookup"><span data-stu-id="1a99a-159">This directory should now contain a file `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span> <span data-ttu-id="1a99a-160">Вы можете изменить этот шаблон с помощью текстового редактора и перезаписать его собственными квантовыми приложениями.</span><span class="sxs-lookup"><span data-stu-id="1a99a-160">You can modfiy this template with a text editor and overwrite it with your own quantum applications.</span></span> 

1. <span data-ttu-id="1a99a-161">Запустите программу.</span><span class="sxs-lookup"><span data-stu-id="1a99a-161">Run the program:</span></span>

    ```dotnetcli
    dotnet run
    ```

1. <span data-ttu-id="1a99a-162">На экране должен появиться следующий текст: `Hello quantum world!`.</span><span class="sxs-lookup"><span data-stu-id="1a99a-162">You should see the following text printed: `Hello quantum world!`</span></span>

***

## <a name="next-steps"></a><span data-ttu-id="1a99a-163">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="1a99a-163">Next steps</span></span>

<span data-ttu-id="1a99a-164">После установки Quantum Development Kit в предпочитаемой среде вы можете написать и запустить [первую квантовую программу](xref:microsoft.quantum.quickstarts.qrng).</span><span class="sxs-lookup"><span data-stu-id="1a99a-164">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
