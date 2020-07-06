---
title: Разработка приложений Q# для командной строки
author: KittyYeungQ
ms.author: kitty
ms.date: 4/24/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
ms.openlocfilehash: 15015d1673f47faf5a13dde516f834916b4319d6
ms.sourcegitcommit: a3775921db1dc5c653c97b8fa8fe2c0ddd5261ff
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2020
ms.locfileid: "85884286"
---
# <a name="develop-with-q-command-line-applications"></a><span data-ttu-id="1e2c3-102">Разработка приложений Q# для командной строки</span><span class="sxs-lookup"><span data-stu-id="1e2c3-102">Develop with Q# command line applications</span></span>

<span data-ttu-id="1e2c3-103">Программы Q# могут выполняться самостоятельно (без драйвера) на основном языке, например C#, F# или Python.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-103">Q# programs can be executed on their own, without a driver in a host language like C#, F#, or Python.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1e2c3-104">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="1e2c3-104">Prerequisites</span></span>

- [<span data-ttu-id="1e2c3-105">Пакет SDK для .NET Core 3.1 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="1e2c3-105">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

## <a name="installation"></a><span data-ttu-id="1e2c3-106">Установка</span><span class="sxs-lookup"><span data-stu-id="1e2c3-106">Installation</span></span>

<span data-ttu-id="1e2c3-107">Вы можете создавать приложения Q# для командной строки в любой интегрированной среде разработки. Мы рекомендуем использовать для них интегрированную среду разработки Visual Studio Code (VS Code) или Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-107">While you can build Q# command line applications in any IDE, we recommend using Visual Studio Code (VS Code) or Visual Studio IDE for your Q# applications.</span></span> <span data-ttu-id="1e2c3-108">При разработке в таких средах вам доступны широкие возможности расширения QDK, такие как предупреждения, выделение синтаксиса, шаблоны проектов и многие другие.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-108">Developing in these environments includes the rich functionality of the QDK extension, which includes warnings, syntax highlighting, project templates, and more.</span></span>

<span data-ttu-id="1e2c3-109">Чтобы настроить VS Code, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-109">To configure VS Code:</span></span>

1. <span data-ttu-id="1e2c3-110">Скачайте и установите [VS Code](https://code.visualstudio.com/download) (Windows, Linux и Mac).</span><span class="sxs-lookup"><span data-stu-id="1e2c3-110">Download and install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac).</span></span>
2. <span data-ttu-id="1e2c3-111">Установите [Microsoft QDK для VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="1e2c3-111">Install the [Microsoft QDK for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

<span data-ttu-id="1e2c3-112">Чтобы настроить Visual Studio, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-112">To configure Visual Studio:</span></span>

1. <span data-ttu-id="1e2c3-113">Скачайте и установите [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 или более новой версии с включенной рабочей нагрузкой кроссплатформенной разработки .NET Core.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-113">Download and install [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 or greater, with the .NET Core cross-platform development workload enabled.</span></span>
2. <span data-ttu-id="1e2c3-114">Скачайте и установите [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span><span class="sxs-lookup"><span data-stu-id="1e2c3-114">Download and install the [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span></span>

<span data-ttu-id="1e2c3-115">Чтобы установить QDK для другой среды, выполните в командной строке следующую команду:</span><span class="sxs-lookup"><span data-stu-id="1e2c3-115">To install the QDK for another environment, enter in the command line:</span></span>

```dotnetcli
dotnet new -i Microsoft.Quantum.ProjectTemplates
```

## <a name="develop-with-q"></a><span data-ttu-id="1e2c3-116">Разработка на Q#</span><span class="sxs-lookup"><span data-stu-id="1e2c3-116">Develop with Q#</span></span>

<span data-ttu-id="1e2c3-117">Следуйте инструкциям на вкладке для вашей среды.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-117">Follow the instructions at the tab corresponding to your environment.</span></span>

### <a name="vs-code"></a>[<span data-ttu-id="1e2c3-118">Код VS</span><span class="sxs-lookup"><span data-stu-id="1e2c3-118">VS Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="1e2c3-119">Установите шаблоны проектов Q#.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-119">Install the Q# project templates:</span></span>

1. <span data-ttu-id="1e2c3-120">Откройте VS Code.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-120">Open VS Code.</span></span>
2. <span data-ttu-id="1e2c3-121">Выберите **Представление** -> **Палитра команд**.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-121">Click **View** -> **Command Palette**.</span></span>
3. <span data-ttu-id="1e2c3-122">Выберите **Q#: Install project templates** (Q#: установить шаблоны проектов).</span><span class="sxs-lookup"><span data-stu-id="1e2c3-122">Select **Q#: Install project templates**.</span></span>

<span data-ttu-id="1e2c3-123">Когда отобразится сообщение **Project templates installed successfully** (Шаблоны проектов успешно установлены), пакет QDK будет готов к использованию с вашими собственными приложениями и библиотеками.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-123">When **Project templates installed successfully** displays, the QDK is ready to use with your own applications and libraries.</span></span>

<span data-ttu-id="1e2c3-124">Чтобы создать новый проект, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-124">To create a new project:</span></span>

1. <span data-ttu-id="1e2c3-125">Щелкните **Представление** -> **Палитра команд** и выберите **Q#: создать проект**.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-125">Click **View** -> **Command Palette** and select **Q#: Create New Project**.</span></span>
2. <span data-ttu-id="1e2c3-126">Щелкните **Standalone console application** (Автономное консольное приложение).</span><span class="sxs-lookup"><span data-stu-id="1e2c3-126">Click **Standalone console application**.</span></span>
3. <span data-ttu-id="1e2c3-127">Перейдите к расположению, в котором нужно сохранить проект, и щелкните **Создать проект**.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-127">Navigate to the location to save the project and click **Create Project**.</span></span>
4. <span data-ttu-id="1e2c3-128">После успешного создания проекта нажмите **Открыть новый проект...** в правом нижнем углу.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-128">When the project is successfully created, click **Open new project...** in the lower right.</span></span>
        
<span data-ttu-id="1e2c3-129">Проверьте проект.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-129">Inspect the project.</span></span> <span data-ttu-id="1e2c3-130">Вы увидите исходный файл с именем `Program.qs`, который представляет собой программу Q#, определяющую простую операцию вывода сообщения в консоль.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-130">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="1e2c3-131">Чтобы запустить приложение, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="1e2c3-131">To run the application:</span></span>
1. <span data-ttu-id="1e2c3-132">Щелкните **Терминал** -> **Создать терминал**.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-132">Click **Terminal** -> **New Terminal**.</span></span>
2. <span data-ttu-id="1e2c3-133">В командной строке терминала введите `dotnet run`.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-133">At the terminal prompt, enter `dotnet run`.</span></span>
3. <span data-ttu-id="1e2c3-134">В окне консоли `Hello quantum world!` должен отобразиться следующий текст.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-134">You should see the following text in the output window `Hello quantum world!`</span></span>


> [!NOTE]
> <span data-ttu-id="1e2c3-135">Сейчас рабочие области с несколькими корневыми папками не поддерживаются в расширении Q# для VS Code.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-135">Workspaces with multiple root folders are not currently supported by the VS Code Q# extension.</span></span> <span data-ttu-id="1e2c3-136">Если в одной рабочей области VS Code несколько проектов, все проекты нужно разместить в одной корневой папке.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-136">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

### <a name="visual-studio"></a>[<span data-ttu-id="1e2c3-137">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1e2c3-137">Visual Studio</span></span>](#tab/tabid-vs)

<span data-ttu-id="1e2c3-138">Проверьте установку Visual Studio, создав приложение `Hello World` на Q#.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-138">Verify your Visual Studio installation by creating a Q# `Hello World` application.</span></span>

<span data-ttu-id="1e2c3-139">Чтобы создать приложение на Q#, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-139">To create a new Q# application:</span></span>
1. <span data-ttu-id="1e2c3-140">Откройте Visual Studio и щелкните **Файл** -> **Создать** -> **Проект**.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-140">Open Visual Studio and click **File** -> **New** -> **Project**.</span></span>
2. <span data-ttu-id="1e2c3-141">Введите `Q#` в поле поиска, выберите **Q# Application** (Приложение Q#) и щелкните **Далее**.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-141">Type `Q#` in the search box, select **Q# Application** and click **Next**.</span></span>
3. <span data-ttu-id="1e2c3-142">Введите имя и расположение приложения и щелкните **Создать**.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-142">Enter a name and location for your application and click **Create**.</span></span>


<span data-ttu-id="1e2c3-143">Проверьте проект.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-143">Inspect the project.</span></span> <span data-ttu-id="1e2c3-144">Вы увидите исходный файл с именем `Program.qs`, который представляет собой программу Q#, определяющую простую операцию вывода сообщения в консоль.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-144">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="1e2c3-145">Чтобы запустить приложение, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="1e2c3-145">To run the application:</span></span>
1. <span data-ttu-id="1e2c3-146">Выберите **Отладка** -> **Запустить без отладки**.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-146">Select **Debug** -> **Start Without Debugging**.</span></span>
2. <span data-ttu-id="1e2c3-147">В окне консоли должен отобразиться текст `Hello quantum world!`.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-147">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> <span data-ttu-id="1e2c3-148">Если в одном решении Visual Studio несколько проектов, все включенные в него проекты нужно разместить в той же папке, что и решение, или в одной из вложенных в нее папок.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-148">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its sub-folders.</span></span>  

### <a name="other-editors-with-the-command-line"></a>[<span data-ttu-id="1e2c3-149">Другие редакторы с командной строкой</span><span class="sxs-lookup"><span data-stu-id="1e2c3-149">Other editors with the command line</span></span>](#tab/tabid-cmdline)

<span data-ttu-id="1e2c3-150">Проверьте установку, создав на Q# приложение `Hello World`.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-150">Verify your installation by creating a Q# `Hello World` application.</span></span>

1. <span data-ttu-id="1e2c3-151">Создайте новое приложение:</span><span class="sxs-lookup"><span data-stu-id="1e2c3-151">Create a new application:</span></span>
    ```dotnetcli
    dotnet new console -lang Q# -o runSayHello
    ```

2. <span data-ttu-id="1e2c3-152">Перейдите в каталог приложения:</span><span class="sxs-lookup"><span data-stu-id="1e2c3-152">Navigate to the application directory:</span></span>
    ```dotnetcli
    cd runSayHello
    ```

    <span data-ttu-id="1e2c3-153">Этот каталог теперь должен содержать файл `Program.qs`, который представляет собой программу Q#, определяющую простую операцию вывода сообщения в консоль.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-153">This directory should now contain a file `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span> <span data-ttu-id="1e2c3-154">Вы можете изменить этот шаблон с помощью текстового редактора и перезаписать его собственными квантовыми приложениями.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-154">You can modfiy this template with a text editor and overwrite it with your own quantum applications.</span></span> 

3. <span data-ttu-id="1e2c3-155">Запустите программу.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-155">Run the program:</span></span>
    ```dotnetcli
    dotnet run
    ```

4. <span data-ttu-id="1e2c3-156">На экране должен появиться следующий текст: `Hello quantum world!`.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-156">You should see the following text printed: `Hello quantum world!`</span></span>

***

## <a name="next-steps"></a><span data-ttu-id="1e2c3-157">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="1e2c3-157">Next steps</span></span>

<span data-ttu-id="1e2c3-158">После установки Quantum Development Kit в предпочитаемой среде вы можете написать и запустить [первую квантовую программу](xref:microsoft.quantum.quickstarts.qrng).</span><span class="sxs-lookup"><span data-stu-id="1e2c3-158">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
