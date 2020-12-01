---
title: Разработка с помощью приложений Q# в интегрированной среде разработки
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
ms.openlocfilehash: eeb567dedc1b8123b32faf7ed3a42bb51f16a7d2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96228735"
---
# <a name="develop-with-no-locq-applications-in-an-ide"></a><span data-ttu-id="02155-103">Разработка с помощью приложений Q# в интегрированной среде разработки</span><span class="sxs-lookup"><span data-stu-id="02155-103">Develop with Q# applications in an IDE</span></span>

<span data-ttu-id="02155-104">Программы Q# могут выполняться самостоятельно (без драйвера) на основном языке, например C#, F# или Python.</span><span class="sxs-lookup"><span data-stu-id="02155-104">Q# programs can run on their own, without a driver in a host language like C#, F#, or Python.</span></span> <span data-ttu-id="02155-105">Приложения Q# можно разрабатывать в Visual Studio Code (VS Code), Visual Studio, Visual Studio Codespaces либо с помощью любого редактора или IDE, а затем запускать их из консоли .NET.</span><span class="sxs-lookup"><span data-stu-id="02155-105">You can develop Q# applications in Visual Studio Code (VS Code), Visual Studio, Visual Studio Codespaces, or with any editor/IDE and run applications from the .NET console.</span></span> 

## <a name="prerequisites-for-all-environments"></a><span data-ttu-id="02155-106">Необходимые условия для всех сред</span><span class="sxs-lookup"><span data-stu-id="02155-106">Prerequisites for all environments</span></span>

- [<span data-ttu-id="02155-107">Пакет SDK для .NET Core 3.1 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="02155-107">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

## <a name="installation"></a><span data-ttu-id="02155-108">Установка</span><span class="sxs-lookup"><span data-stu-id="02155-108">Installation</span></span>

<span data-ttu-id="02155-109">Вы можете создавать приложения Q# в любой интегрированной среде разработки. Но мы рекомендуем использовать для локальной разработки приложений Q# интегрированную среду разработки Visual Studio Code (VS Code) или Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="02155-109">While you can build Q# applications in any IDE, we recommend using Visual Studio Code (VS Code) or Visual Studio IDE for developing your Q# applications locally.</span></span> <span data-ttu-id="02155-110">Для разработки в облаке с помощью веб-браузера мы рекомендуем использовать Visual Studio Codespaces.</span><span class="sxs-lookup"><span data-stu-id="02155-110">For developing in the Cloud via the web browser, we recommend Visual Studio Codespaces.</span></span> <span data-ttu-id="02155-111">При разработке в таких средах вам доступны возможности расширения QDK, такие как предупреждения, выделение синтаксиса, шаблоны проектов и пр.</span><span class="sxs-lookup"><span data-stu-id="02155-111">Developing in these environments leverages the rich functionality of the QDK extension, which includes warnings, syntax highlighting, project templates, and more.</span></span> 

### <a name="to-configure-for-vs-code"></a><span data-ttu-id="02155-112">Чтобы настроить VS Code, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="02155-112">To configure for VS Code:</span></span>

1. <span data-ttu-id="02155-113">Скачайте и установите [VS Code](https://code.visualstudio.com/download) (Windows, Linux и Mac).</span><span class="sxs-lookup"><span data-stu-id="02155-113">Download and install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac).</span></span>
2. <span data-ttu-id="02155-114">Установите [Microsoft QDK для VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="02155-114">Install the [Microsoft QDK for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

### <a name="to-configure-for-visual-studio"></a><span data-ttu-id="02155-115">Чтобы настроить Visual Studio, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="02155-115">To configure for Visual Studio:</span></span>

1. <span data-ttu-id="02155-116">Скачайте и установите [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 или более новой версии с включенной рабочей нагрузкой кроссплатформенной разработки .NET Core.</span><span class="sxs-lookup"><span data-stu-id="02155-116">Download and install [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 or greater, with the .NET Core cross-platform development workload enabled.</span></span>
2. <span data-ttu-id="02155-117">Скачайте и установите [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span><span class="sxs-lookup"><span data-stu-id="02155-117">Download and install the [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span></span>

### <a name="to-configure-for-another-environment"></a><span data-ttu-id="02155-118">Чтобы настроить другую среду, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="02155-118">To configure for another environment:</span></span> 

1. <span data-ttu-id="02155-119">В командной строке введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="02155-119">Enter the following at the command prompt</span></span>

```dotnetcli
dotnet new -i Microsoft.Quantum.ProjectTemplates
```

### <a name="to-configure-for-visual-studio-codespaces"></a><span data-ttu-id="02155-120">Чтобы настроить Visual Studio Codespaces, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="02155-120">To configure for Visual Studio Codespaces:</span></span>

1. <span data-ttu-id="02155-121">Создайте [учетную запись Azure](https://azure.microsoft.com/free/).</span><span class="sxs-lookup"><span data-stu-id="02155-121">Create an [Azure account](https://azure.microsoft.com/free/).</span></span>
2. <span data-ttu-id="02155-122">Создайте среду Codespaces.</span><span class="sxs-lookup"><span data-stu-id="02155-122">Create a Codespaces environment.</span></span> <span data-ttu-id="02155-123">Выполните инструкции из [этого краткого руководства](https://docs.microsoft.com/visualstudio/codespaces/quickstarts/browser).</span><span class="sxs-lookup"><span data-stu-id="02155-123">Please follow the [quickstart guide](https://docs.microsoft.com/visualstudio/codespaces/quickstarts/browser).</span></span> <span data-ttu-id="02155-124">При создании Codespaces рекомендуется ввести `microsoft/Quantum` в поле Git Repository (Репозиторий Git), чтобы загрузить параметры, связанные с QDK.</span><span class="sxs-lookup"><span data-stu-id="02155-124">When creating the Codespace, we recommend to enter `microsoft/Quantum` in the "Git Repository" field to load QDK-specific settings.</span></span>
3. <span data-ttu-id="02155-125">Теперь вы можете запустить новую среду и начать разработку в браузере с помощью [облачной интегрированной среды разработки Visual Studio Codespaces](https://online.visualstudio.com/environments).</span><span class="sxs-lookup"><span data-stu-id="02155-125">You can now launch your new environment and start developing in the browser via the [VS Codespaces Cloud IDE](https://online.visualstudio.com/environments).</span></span> <span data-ttu-id="02155-126">Кроме того, можно использовать локальную установку VS Code и использовать Codespaces в качестве [удаленной среды](https://docs.microsoft.com/visualstudio/online/how-to/vscode).</span><span class="sxs-lookup"><span data-stu-id="02155-126">Alternatively, it is possible to use your local installation of VS Code and use Codespaces as a [remote environment](https://docs.microsoft.com/visualstudio/online/how-to/vscode).</span></span>

## <a name="develop-with-no-locq"></a><span data-ttu-id="02155-127">Разработка на Q#</span><span class="sxs-lookup"><span data-stu-id="02155-127">Develop with Q#</span></span>

<span data-ttu-id="02155-128">Следуйте инструкциям на вкладке для вашей среды разработки.</span><span class="sxs-lookup"><span data-stu-id="02155-128">Follow the instructions on the tab corresponding to your development environment.</span></span>

### <a name="vs-code"></a>[<span data-ttu-id="02155-129">Код VS</span><span class="sxs-lookup"><span data-stu-id="02155-129">VS Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="02155-130">Чтобы создать новый проект, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="02155-130">To create a new project:</span></span>

1. <span data-ttu-id="02155-131">Щелкните **Представление** -> **Палитра команд** и выберите **Q#: создать проект**.</span><span class="sxs-lookup"><span data-stu-id="02155-131">Click **View** -> **Command Palette** and select **Q#: Create New Project**.</span></span>
2. <span data-ttu-id="02155-132">Щелкните **Standalone console application** (Автономное консольное приложение).</span><span class="sxs-lookup"><span data-stu-id="02155-132">Click **Standalone console application**.</span></span>
3. <span data-ttu-id="02155-133">Перейдите к расположению, чтобы сохранить проект.</span><span class="sxs-lookup"><span data-stu-id="02155-133">Navigate to the location to save the project.</span></span> <span data-ttu-id="02155-134">Введите имя проекта и щелкните **Создать проект**.</span><span class="sxs-lookup"><span data-stu-id="02155-134">Enter the project name and click **Create Project**.</span></span>
4. <span data-ttu-id="02155-135">После успешного создания проекта нажмите **Открыть новый проект...** в правом нижнем углу.</span><span class="sxs-lookup"><span data-stu-id="02155-135">When the project is successfully created, click **Open new project...** in the lower right.</span></span>

<span data-ttu-id="02155-136">Проверьте проект.</span><span class="sxs-lookup"><span data-stu-id="02155-136">Inspect the project.</span></span> <span data-ttu-id="02155-137">Вы увидите исходный файл с именем `Program.qs`, который представляет собой программу Q#, определяющую простую операцию вывода сообщения в консоль.</span><span class="sxs-lookup"><span data-stu-id="02155-137">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="02155-138">Чтобы запустить приложение, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="02155-138">To run the application:</span></span>

1. <span data-ttu-id="02155-139">Щелкните **Терминал** -> **Создать терминал**.</span><span class="sxs-lookup"><span data-stu-id="02155-139">Click **Terminal** -> **New Terminal**.</span></span>
2. <span data-ttu-id="02155-140">В командной строке терминала введите `dotnet run`.</span><span class="sxs-lookup"><span data-stu-id="02155-140">At the terminal prompt, enter `dotnet run`.</span></span>
3. <span data-ttu-id="02155-141">В окне консоли `Hello quantum world!` должен отобразиться следующий текст.</span><span class="sxs-lookup"><span data-stu-id="02155-141">You should see the following text in the output window `Hello quantum world!`</span></span>

> [!NOTE]
> <span data-ttu-id="02155-142">В настоящее время рабочие области с несколькими корневыми папками не поддерживаются в расширении Q# для VS Code.</span><span class="sxs-lookup"><span data-stu-id="02155-142">Workspaces with multiple root folders are not currently supported by the VS Code Q# extension.</span></span> <span data-ttu-id="02155-143">Если в одной рабочей области VS Code несколько проектов, все проекты нужно разместить в одной корневой папке.</span><span class="sxs-lookup"><span data-stu-id="02155-143">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

### <a name="visual-studio"></a>[<span data-ttu-id="02155-144">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="02155-144">Visual Studio</span></span>](#tab/tabid-vs)

<span data-ttu-id="02155-145">Проверьте установку Visual Studio, создав приложение `Hello World` на Q#.</span><span class="sxs-lookup"><span data-stu-id="02155-145">Verify your Visual Studio installation by creating a Q# `Hello World` application.</span></span>

<span data-ttu-id="02155-146">Чтобы создать приложение на Q#:</span><span class="sxs-lookup"><span data-stu-id="02155-146">To create a new Q# application:</span></span>

1. <span data-ttu-id="02155-147">Откройте Visual Studio и щелкните **Файл** -> **Создать** -> **Проект**.</span><span class="sxs-lookup"><span data-stu-id="02155-147">Open Visual Studio and click **File** -> **New** -> **Project**.</span></span>
2. <span data-ttu-id="02155-148">Введите `Q#` в поле поиска, выберите **Q# Application** (Приложение Q#) и щелкните **Далее**.</span><span class="sxs-lookup"><span data-stu-id="02155-148">Type `Q#` in the search box, select **Q# Application** and click **Next**.</span></span>
3. <span data-ttu-id="02155-149">Введите имя и расположение приложения и щелкните **Создать**.</span><span class="sxs-lookup"><span data-stu-id="02155-149">Enter a name and location for your application and click **Create**.</span></span>


<span data-ttu-id="02155-150">Проверьте проект.</span><span class="sxs-lookup"><span data-stu-id="02155-150">Inspect the project.</span></span> <span data-ttu-id="02155-151">Вы увидите исходный файл с именем `Program.qs`, который представляет собой программу Q#, определяющую простую операцию вывода сообщения в консоль.</span><span class="sxs-lookup"><span data-stu-id="02155-151">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="02155-152">Чтобы запустить приложение, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="02155-152">To run the application:</span></span>

1. <span data-ttu-id="02155-153">Выберите **Отладка** -> **Запустить без отладки**.</span><span class="sxs-lookup"><span data-stu-id="02155-153">Select **Debug** -> **Start Without Debugging**.</span></span>
2. <span data-ttu-id="02155-154">В окне консоли должен отобразиться текст `Hello quantum world!`.</span><span class="sxs-lookup"><span data-stu-id="02155-154">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> <span data-ttu-id="02155-155">Если в одном решении Visual Studio несколько проектов, все включенные в него проекты нужно разместить в той же папке, что и решение, или в одной из вложенных в нее папок.</span><span class="sxs-lookup"><span data-stu-id="02155-155">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its sub-folders.</span></span>  

### <a name="other-editors-with-the-command-prompt"></a>[<span data-ttu-id="02155-156">Другие редакторы с командной строкой</span><span class="sxs-lookup"><span data-stu-id="02155-156">Other editors with the command prompt</span></span>](#tab/tabid-cmdline)

<span data-ttu-id="02155-157">Проверьте установку, создав на Q# приложение `Hello World`.</span><span class="sxs-lookup"><span data-stu-id="02155-157">Verify your installation by creating a Q# `Hello World` application.</span></span>

1. <span data-ttu-id="02155-158">Создайте новое приложение:</span><span class="sxs-lookup"><span data-stu-id="02155-158">Create a new application:</span></span>

    ```dotnetcli
    dotnet new console -lang Q# -o runSayHello
    ```

1. <span data-ttu-id="02155-159">Перейдите в каталог приложения:</span><span class="sxs-lookup"><span data-stu-id="02155-159">Navigate to the application directory:</span></span>

    ```dotnetcli
    cd runSayHello
    ```

    <span data-ttu-id="02155-160">Этот каталог теперь должен содержать файл `Program.qs`, который представляет собой программу Q#, определяющую простую операцию вывода сообщения в консоль.</span><span class="sxs-lookup"><span data-stu-id="02155-160">This directory should now contain a file `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span> <span data-ttu-id="02155-161">Вы можете изменить этот шаблон с помощью текстового редактора и перезаписать его собственными квантовыми приложениями.</span><span class="sxs-lookup"><span data-stu-id="02155-161">You can modfiy this template with a text editor and overwrite it with your own quantum applications.</span></span> 

1. <span data-ttu-id="02155-162">Запустите программу.</span><span class="sxs-lookup"><span data-stu-id="02155-162">Run the program:</span></span>

    ```dotnetcli
    dotnet run
    ```

1. <span data-ttu-id="02155-163">На экране должен появиться следующий текст: `Hello quantum world!`.</span><span class="sxs-lookup"><span data-stu-id="02155-163">You should see the following text printed: `Hello quantum world!`</span></span>

***

## <a name="next-steps"></a><span data-ttu-id="02155-164">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="02155-164">Next steps</span></span>

<span data-ttu-id="02155-165">После установки Quantum Development Kit в предпочитаемой среде вы можете написать и запустить [первую квантовую программу](xref:microsoft.quantum.quickstarts.qrng).</span><span class="sxs-lookup"><span data-stu-id="02155-165">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
