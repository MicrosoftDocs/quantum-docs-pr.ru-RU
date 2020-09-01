---
title: Разработка приложений Q#
author: KittyYeungQ
ms.author: kitty
ms.date: 4/24/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
no-loc:
- Q#
- $$v
ms.openlocfilehash: 6a287dd76162a05d72af7e9d1e46533425283e2a
ms.sourcegitcommit: 75c4edc7c410cc63dc8352e2a5bef44b433ed188
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/25/2020
ms.locfileid: "88863665"
---
# <a name="develop-with-no-locq-applications"></a><span data-ttu-id="b80c3-102">Разработка приложений Q#</span><span class="sxs-lookup"><span data-stu-id="b80c3-102">Develop with Q# applications</span></span>

<span data-ttu-id="b80c3-103">Программы Q# могут выполняться самостоятельно (без драйвера) на основном языке, например C#, F# или Python.</span><span class="sxs-lookup"><span data-stu-id="b80c3-103">Q# programs can be executed on their own, without a driver in a host language like C#, F#, or Python.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b80c3-104">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="b80c3-104">Prerequisites</span></span>

- [<span data-ttu-id="b80c3-105">Пакет SDK для .NET Core 3.1 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="b80c3-105">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

## <a name="installation"></a><span data-ttu-id="b80c3-106">Установка</span><span class="sxs-lookup"><span data-stu-id="b80c3-106">Installation</span></span>

<span data-ttu-id="b80c3-107">Вы можете создавать приложения Q# в любой интегрированной среде разработки. Но мы рекомендуем использовать для локальной разработки приложений Q# интегрированную среду разработки Visual Studio Code (VS Code) или Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b80c3-107">While you can build Q# applications in any IDE, we recommend using Visual Studio Code (VS Code) or Visual Studio IDE for developing your Q# applications locally.</span></span> <span data-ttu-id="b80c3-108">Для разработки в облаке с помощью веб-браузера мы рекомендуем использовать Visual Studio Codespaces.</span><span class="sxs-lookup"><span data-stu-id="b80c3-108">For developing in the Cloud via the web browser, we recommend Visual Studio Codespaces.</span></span> <span data-ttu-id="b80c3-109">При разработке в таких средах вам доступны широкие возможности расширения QDK, такие как предупреждения, выделение синтаксиса, шаблоны проектов и многие другие.</span><span class="sxs-lookup"><span data-stu-id="b80c3-109">Developing in these environments includes the rich functionality of the QDK extension, which includes warnings, syntax highlighting, project templates, and more.</span></span> 

<span data-ttu-id="b80c3-110">Чтобы настроить VS Code, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b80c3-110">To configure VS Code:</span></span>

1. <span data-ttu-id="b80c3-111">Скачайте и установите [VS Code](https://code.visualstudio.com/download) (Windows, Linux и Mac).</span><span class="sxs-lookup"><span data-stu-id="b80c3-111">Download and install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac).</span></span>
2. <span data-ttu-id="b80c3-112">Установите [Microsoft QDK для VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="b80c3-112">Install the [Microsoft QDK for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

<span data-ttu-id="b80c3-113">Чтобы настроить Visual Studio, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b80c3-113">To configure Visual Studio:</span></span>

1. <span data-ttu-id="b80c3-114">Скачайте и установите [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 или более новой версии с включенной рабочей нагрузкой кроссплатформенной разработки .NET Core.</span><span class="sxs-lookup"><span data-stu-id="b80c3-114">Download and install [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 or greater, with the .NET Core cross-platform development workload enabled.</span></span>
2. <span data-ttu-id="b80c3-115">Скачайте и установите [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span><span class="sxs-lookup"><span data-stu-id="b80c3-115">Download and install the [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span></span>

<span data-ttu-id="b80c3-116">Чтобы настроить Visual Studio Codespaces, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="b80c3-116">To configure Visual Studio Codespaces:</span></span>

1. <span data-ttu-id="b80c3-117">Создайте [учетную запись Azure](https://azure.microsoft.com/free/).</span><span class="sxs-lookup"><span data-stu-id="b80c3-117">Create an [Azure account](https://azure.microsoft.com/free/).</span></span>
2. <span data-ttu-id="b80c3-118">Создайте среду Codespaces.</span><span class="sxs-lookup"><span data-stu-id="b80c3-118">Create a Codespaces environment.</span></span> <span data-ttu-id="b80c3-119">Выполните инструкции из [этого краткого руководства](https://docs.microsoft.com/visualstudio/online/quickstarts/browser).</span><span class="sxs-lookup"><span data-stu-id="b80c3-119">Please follow the [quickstart guide](https://docs.microsoft.com/visualstudio/online/quickstarts/browser).</span></span> <span data-ttu-id="b80c3-120">При создании Codespaces рекомендуется ввести `microsoft/Quantum` в поле Git Repository (Репозиторий Git), чтобы загрузить параметры, связанные с QDK.</span><span class="sxs-lookup"><span data-stu-id="b80c3-120">When creating the Codespace, we recommend to enter `microsoft/Quantum` in the "Git Repository" field to load QDK-specific settings.</span></span>
3. <span data-ttu-id="b80c3-121">Теперь вы можете запустить новую среду и начать разработку в браузере с помощью [облачной интегрированной среды разработки Visual Studio Codespaces](https://online.visualstudio.com/environments).</span><span class="sxs-lookup"><span data-stu-id="b80c3-121">You can now launch your new environment and start developing in the browser via the [VS Codespaces Cloud IDE](https://online.visualstudio.com/environments).</span></span> <span data-ttu-id="b80c3-122">Кроме того, можно использовать локальную установку VS Code и использовать Codespaces в качестве [удаленной среды](https://docs.microsoft.com/visualstudio/online/how-to/vscode).</span><span class="sxs-lookup"><span data-stu-id="b80c3-122">Alternatively, it is possible to use your local installation of VS Code and use Codespaces as a [remote environment](https://docs.microsoft.com/visualstudio/online/how-to/vscode).</span></span>


<span data-ttu-id="b80c3-123">Чтобы установить QDK для другой среды, выполните в командной строке следующую команду:</span><span class="sxs-lookup"><span data-stu-id="b80c3-123">To install the QDK for another environment, enter at the command prompt:</span></span>

```dotnetcli
dotnet new -i Microsoft.Quantum.ProjectTemplates
```

## <a name="develop-with-no-locq"></a><span data-ttu-id="b80c3-124">Разработка на Q#</span><span class="sxs-lookup"><span data-stu-id="b80c3-124">Develop with Q#</span></span>

<span data-ttu-id="b80c3-125">Следуйте инструкциям на вкладке для вашей среды.</span><span class="sxs-lookup"><span data-stu-id="b80c3-125">Follow the instructions at the tab corresponding to your environment.</span></span>

### <a name="vs-code"></a>[<span data-ttu-id="b80c3-126">Код VS</span><span class="sxs-lookup"><span data-stu-id="b80c3-126">VS Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="b80c3-127">Чтобы создать новый проект, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b80c3-127">To create a new project:</span></span>

1. <span data-ttu-id="b80c3-128">Щелкните **Представление** -> **Палитра команд** и выберите **Q#: создать проект**.</span><span class="sxs-lookup"><span data-stu-id="b80c3-128">Click **View** -> **Command Palette** and select **Q#: Create New Project**.</span></span>
2. <span data-ttu-id="b80c3-129">Щелкните **Standalone console application** (Автономное консольное приложение).</span><span class="sxs-lookup"><span data-stu-id="b80c3-129">Click **Standalone console application**.</span></span>
3. <span data-ttu-id="b80c3-130">Перейдите к расположению, в котором нужно сохранить проект, и щелкните **Создать проект**.</span><span class="sxs-lookup"><span data-stu-id="b80c3-130">Navigate to the location to save the project and click **Create Project**.</span></span>
4. <span data-ttu-id="b80c3-131">После успешного создания проекта нажмите **Открыть новый проект...** в правом нижнем углу.</span><span class="sxs-lookup"><span data-stu-id="b80c3-131">When the project is successfully created, click **Open new project...** in the lower right.</span></span>
        
<span data-ttu-id="b80c3-132">Проверьте проект.</span><span class="sxs-lookup"><span data-stu-id="b80c3-132">Inspect the project.</span></span> <span data-ttu-id="b80c3-133">Вы увидите исходный файл с именем `Program.qs`, который представляет собой программу Q#, определяющую простую операцию вывода сообщения в консоль.</span><span class="sxs-lookup"><span data-stu-id="b80c3-133">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="b80c3-134">Чтобы запустить приложение, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="b80c3-134">To run the application:</span></span>
1. <span data-ttu-id="b80c3-135">Щелкните **Терминал** -> **Создать терминал**.</span><span class="sxs-lookup"><span data-stu-id="b80c3-135">Click **Terminal** -> **New Terminal**.</span></span>
2. <span data-ttu-id="b80c3-136">В командной строке терминала введите `dotnet run`.</span><span class="sxs-lookup"><span data-stu-id="b80c3-136">At the terminal prompt, enter `dotnet run`.</span></span>
3. <span data-ttu-id="b80c3-137">В окне консоли `Hello quantum world!` должен отобразиться следующий текст.</span><span class="sxs-lookup"><span data-stu-id="b80c3-137">You should see the following text in the output window `Hello quantum world!`</span></span>


> [!NOTE]
> <span data-ttu-id="b80c3-138">В настоящее время рабочие области с несколькими корневыми папками не поддерживаются в расширении Q# для VS Code.</span><span class="sxs-lookup"><span data-stu-id="b80c3-138">Workspaces with multiple root folders are not currently supported by the VS Code Q# extension.</span></span> <span data-ttu-id="b80c3-139">Если в одной рабочей области VS Code несколько проектов, все проекты нужно разместить в одной корневой папке.</span><span class="sxs-lookup"><span data-stu-id="b80c3-139">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

### <a name="visual-studio"></a>[<span data-ttu-id="b80c3-140">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b80c3-140">Visual Studio</span></span>](#tab/tabid-vs)

<span data-ttu-id="b80c3-141">Проверьте установку Visual Studio, создав приложение `Hello World` на Q#.</span><span class="sxs-lookup"><span data-stu-id="b80c3-141">Verify your Visual Studio installation by creating a Q# `Hello World` application.</span></span>

<span data-ttu-id="b80c3-142">Чтобы создать приложение на Q#:</span><span class="sxs-lookup"><span data-stu-id="b80c3-142">To create a new Q# application:</span></span>
1. <span data-ttu-id="b80c3-143">Откройте Visual Studio и щелкните **Файл** -> **Создать** -> **Проект**.</span><span class="sxs-lookup"><span data-stu-id="b80c3-143">Open Visual Studio and click **File** -> **New** -> **Project**.</span></span>
2. <span data-ttu-id="b80c3-144">Введите `Q#` в поле поиска, выберите **Q# Application** (Приложение Q#) и щелкните **Далее**.</span><span class="sxs-lookup"><span data-stu-id="b80c3-144">Type `Q#` in the search box, select **Q# Application** and click **Next**.</span></span>
3. <span data-ttu-id="b80c3-145">Введите имя и расположение приложения и щелкните **Создать**.</span><span class="sxs-lookup"><span data-stu-id="b80c3-145">Enter a name and location for your application and click **Create**.</span></span>


<span data-ttu-id="b80c3-146">Проверьте проект.</span><span class="sxs-lookup"><span data-stu-id="b80c3-146">Inspect the project.</span></span> <span data-ttu-id="b80c3-147">Вы увидите исходный файл с именем `Program.qs`, который представляет собой программу Q#, определяющую простую операцию вывода сообщения в консоль.</span><span class="sxs-lookup"><span data-stu-id="b80c3-147">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="b80c3-148">Чтобы запустить приложение, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="b80c3-148">To run the application:</span></span>
1. <span data-ttu-id="b80c3-149">Выберите **Отладка** -> **Запустить без отладки**.</span><span class="sxs-lookup"><span data-stu-id="b80c3-149">Select **Debug** -> **Start Without Debugging**.</span></span>
2. <span data-ttu-id="b80c3-150">В окне консоли должен отобразиться текст `Hello quantum world!`.</span><span class="sxs-lookup"><span data-stu-id="b80c3-150">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> <span data-ttu-id="b80c3-151">Если в одном решении Visual Studio несколько проектов, все включенные в него проекты нужно разместить в той же папке, что и решение, или в одной из вложенных в нее папок.</span><span class="sxs-lookup"><span data-stu-id="b80c3-151">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its sub-folders.</span></span>  

### <a name="other-editors-with-the-command-prompt"></a>[<span data-ttu-id="b80c3-152">Другие редакторы с командной строкой</span><span class="sxs-lookup"><span data-stu-id="b80c3-152">Other editors with the command prompt</span></span>](#tab/tabid-cmdline)

<span data-ttu-id="b80c3-153">Проверьте установку, создав на Q# приложение `Hello World`.</span><span class="sxs-lookup"><span data-stu-id="b80c3-153">Verify your installation by creating a Q# `Hello World` application.</span></span>

1. <span data-ttu-id="b80c3-154">Установите шаблоны проектов.</span><span class="sxs-lookup"><span data-stu-id="b80c3-154">Install the project templates.</span></span>

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

1. <span data-ttu-id="b80c3-155">Создайте новое приложение:</span><span class="sxs-lookup"><span data-stu-id="b80c3-155">Create a new application:</span></span>
    ```dotnetcli
    dotnet new console -lang Q# -o runSayHello
    ```

1. <span data-ttu-id="b80c3-156">Перейдите в каталог приложения:</span><span class="sxs-lookup"><span data-stu-id="b80c3-156">Navigate to the application directory:</span></span>
    ```dotnetcli
    cd runSayHello
    ```

    <span data-ttu-id="b80c3-157">Этот каталог теперь должен содержать файл `Program.qs`, который представляет собой программу Q#, определяющую простую операцию вывода сообщения в консоль.</span><span class="sxs-lookup"><span data-stu-id="b80c3-157">This directory should now contain a file `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span> <span data-ttu-id="b80c3-158">Вы можете изменить этот шаблон с помощью текстового редактора и перезаписать его собственными квантовыми приложениями.</span><span class="sxs-lookup"><span data-stu-id="b80c3-158">You can modfiy this template with a text editor and overwrite it with your own quantum applications.</span></span> 

1. <span data-ttu-id="b80c3-159">Запустите программу.</span><span class="sxs-lookup"><span data-stu-id="b80c3-159">Run the program:</span></span>
    ```dotnetcli
    dotnet run
    ```

1. <span data-ttu-id="b80c3-160">На экране должен появиться следующий текст: `Hello quantum world!`.</span><span class="sxs-lookup"><span data-stu-id="b80c3-160">You should see the following text printed: `Hello quantum world!`</span></span>

***

## <a name="next-steps"></a><span data-ttu-id="b80c3-161">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="b80c3-161">Next steps</span></span>

<span data-ttu-id="b80c3-162">После установки Quantum Development Kit в предпочитаемой среде вы можете написать и запустить [первую квантовую программу](xref:microsoft.quantum.quickstarts.qrng).</span><span class="sxs-lookup"><span data-stu-id="b80c3-162">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
