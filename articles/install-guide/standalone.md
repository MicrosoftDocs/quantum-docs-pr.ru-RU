---
title: 'Разработка с помощью Q # приложения командной строки'
author: KittyYeungQ
ms.author: kitty
ms.date: 4/24/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
ms.openlocfilehash: 4311ebf9f72254485a20ba721ea2ce19163f4371
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630261"
---
# <a name="develop-with-q-command-line-applications"></a><span data-ttu-id="283db-102">Разработка с помощью Q # приложения командной строки</span><span class="sxs-lookup"><span data-stu-id="283db-102">Develop with Q# command line applications</span></span>

<span data-ttu-id="283db-103">Программы Q # могут выполняться самостоятельно, без драйвера на основном языке, например C#, F # или Python.</span><span class="sxs-lookup"><span data-stu-id="283db-103">Q# programs can be executed on their own, without a driver in a host language like C#, F#, or Python.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="283db-104">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="283db-104">Prerequisites</span></span>

- <span data-ttu-id="283db-105">[Пакет SDK для .NET Core 3.1 или более поздней версии](https://www.microsoft.com/net/download).</span><span class="sxs-lookup"><span data-stu-id="283db-105">[.NET Core SDK 3.1 or later](https://www.microsoft.com/net/download)</span></span>

## <a name="installation"></a><span data-ttu-id="283db-106">Установка</span><span class="sxs-lookup"><span data-stu-id="283db-106">Installation</span></span>

<span data-ttu-id="283db-107">Вы можете создавать приложения Q # в любой интегрированной среде разработки, для приложений Q # рекомендуется использовать Visual Studio Code (VS Code) или интегрированную среду разработки Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="283db-107">While you can build Q# command line applications in any IDE, we recommend using Visual Studio Code (VS Code) or Visual Studio IDE for your Q# applications.</span></span> <span data-ttu-id="283db-108">Разработка в этих средствах обеспечивает доступ к широким функциональным возможностям.</span><span class="sxs-lookup"><span data-stu-id="283db-108">Developing in these tools provides access to rich functionality.</span></span>

<span data-ttu-id="283db-109">Чтобы настроить VS Code, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="283db-109">To configure VS Code:</span></span>

1. <span data-ttu-id="283db-110">Скачайте и установите [VS Code](https://code.visualstudio.com/download) (Windows, Linux и Mac).</span><span class="sxs-lookup"><span data-stu-id="283db-110">Download and install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac).</span></span>
2. <span data-ttu-id="283db-111">Установите [Microsoft КДК для VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="283db-111">Install the [Microsoft QDK for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

<span data-ttu-id="283db-112">Чтобы настроить Visual Studio, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="283db-112">To configure Visual Studio:</span></span>

1. <span data-ttu-id="283db-113">Скачайте и установите [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16,3 или более поздней версии с включенной рабочей нагрузкой кросс-платформенной разработки .NET Core.</span><span class="sxs-lookup"><span data-stu-id="283db-113">Download and install [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 or greater, with the .NET Core cross-platform development workload enabled.</span></span>
2. <span data-ttu-id="283db-114">Скачайте и установите [Microsoft КДК](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span><span class="sxs-lookup"><span data-stu-id="283db-114">Download and install the [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span></span>


## <a name="develop-with-q-using-vs-code"></a><span data-ttu-id="283db-115">Разработка с помощью Q # using VS Code</span><span class="sxs-lookup"><span data-stu-id="283db-115">Develop with Q# using VS Code</span></span>

<span data-ttu-id="283db-116">Установите шаблоны проектов Q #:</span><span class="sxs-lookup"><span data-stu-id="283db-116">Install the Q# project templates:</span></span>

1. <span data-ttu-id="283db-117">Откройте VS Code.</span><span class="sxs-lookup"><span data-stu-id="283db-117">Open VS Code.</span></span>
2. <span data-ttu-id="283db-118">Нажмите кнопку **Просмотреть**  ->  **палитру команд**.</span><span class="sxs-lookup"><span data-stu-id="283db-118">Click **View** -> **Command Palette**.</span></span>
3. <span data-ttu-id="283db-119">Выберите **Q #: установить шаблоны проектов**.</span><span class="sxs-lookup"><span data-stu-id="283db-119">Select **Q#: Install project templates**.</span></span>

<span data-ttu-id="283db-120">Когда **шаблоны проектов успешно установлены** , КДК готов к использованию с собственными приложениями и библиотеками.</span><span class="sxs-lookup"><span data-stu-id="283db-120">When **Project templates installed successfully** displays, the QDK is ready to use with your own applications and libraries.</span></span>

<span data-ttu-id="283db-121">Чтобы создать новый проект, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="283db-121">To create a new project:</span></span>

1. <span data-ttu-id="283db-122">Щелкните **Просмотреть**  ->  **палитру команд** и выберите **Q #: создать новый проект**.</span><span class="sxs-lookup"><span data-stu-id="283db-122">Click **View** -> **Command Palette** and select **Q#: Create New Project**.</span></span>
2. <span data-ttu-id="283db-123">Щелкните **автономное консольное приложение**.</span><span class="sxs-lookup"><span data-stu-id="283db-123">Click **Standalone console application**.</span></span>
3. <span data-ttu-id="283db-124">Перейдите в папку, в которой нужно сохранить проект, и нажмите кнопку **создать проект**.</span><span class="sxs-lookup"><span data-stu-id="283db-124">Navigate to the location to save the project and click **Create Project**.</span></span>
4. <span data-ttu-id="283db-125">После успешного создания проекта нажмите кнопку **открыть новый проект...** в правом нижнем углу.</span><span class="sxs-lookup"><span data-stu-id="283db-125">When the project is successfully created, click **Open new project...** in the lower right.</span></span>
        
<span data-ttu-id="283db-126">Проверьте проект.</span><span class="sxs-lookup"><span data-stu-id="283db-126">Inspect the project.</span></span> <span data-ttu-id="283db-127">Вы увидите исходный файл с именем `Program.qs` , который представляет собой программу Q #, которая определяет простую операцию для вывода сообщения на консоль.</span><span class="sxs-lookup"><span data-stu-id="283db-127">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="283db-128">Чтобы запустить приложение, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="283db-128">To run the application:</span></span>
1. <span data-ttu-id="283db-129">Щелкните **терминал**  ->  **создать терминал**.</span><span class="sxs-lookup"><span data-stu-id="283db-129">Click **Terminal** -> **New Terminal**.</span></span>
2. <span data-ttu-id="283db-130">В командной строке терминала введите `dotnet run` .</span><span class="sxs-lookup"><span data-stu-id="283db-130">At the terminal prompt, enter `dotnet run`.</span></span>
3. <span data-ttu-id="283db-131">В окне консоли `Hello quantum world!` должен отобразиться следующий текст.</span><span class="sxs-lookup"><span data-stu-id="283db-131">You should see the following text in the output window `Hello quantum world!`</span></span>


> [!NOTE]
> <span data-ttu-id="283db-132">В настоящее время расширение VS Code Q # не поддерживает рабочие области с несколькими корневыми папками.</span><span class="sxs-lookup"><span data-stu-id="283db-132">Workspaces with multiple root folders are not currently supported by the VS Code Q# extension.</span></span> <span data-ttu-id="283db-133">Если в одной рабочей области VS Code несколько проектов, все проекты нужно разместить в одной корневой папке.</span><span class="sxs-lookup"><span data-stu-id="283db-133">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

## <a name="develop-with-q-using-visual-studio"></a><span data-ttu-id="283db-134">Разработка с помощью Q # с использованием Visual Studio</span><span class="sxs-lookup"><span data-stu-id="283db-134">Develop with Q# using Visual Studio</span></span>

<span data-ttu-id="283db-135">Проверьте установку Visual Studio, создав приложение Q # `Hello World` .</span><span class="sxs-lookup"><span data-stu-id="283db-135">Verify your Visual Studio installation by creating a Q# `Hello World` application.</span></span>

<span data-ttu-id="283db-136">Чтобы создать новое приложение Q #, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="283db-136">To create a new Q# application:</span></span>
1. <span data-ttu-id="283db-137">Откройте Visual Studio и выберите **файл**  ->  **создать**  ->  **проект**.</span><span class="sxs-lookup"><span data-stu-id="283db-137">Open Visual Studio and click **File** -> **New** -> **Project**.</span></span>
2. <span data-ttu-id="283db-138">Введите `Q#` в поле поиска, выберите **Q # Application** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="283db-138">Type `Q#` in the search box, select **Q# Application** and click **Next**.</span></span>
3. <span data-ttu-id="283db-139">Введите имя и расположение приложения и нажмите кнопку **создать**.</span><span class="sxs-lookup"><span data-stu-id="283db-139">Enter a name and location for your application and click **Create**.</span></span>


<span data-ttu-id="283db-140">Проверьте проект.</span><span class="sxs-lookup"><span data-stu-id="283db-140">Inspect the project.</span></span> <span data-ttu-id="283db-141">Вы увидите исходный файл с именем `Program.qs` , который представляет собой программу Q #, которая определяет простую операцию для вывода сообщения на консоль.</span><span class="sxs-lookup"><span data-stu-id="283db-141">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="283db-142">Чтобы запустить приложение, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="283db-142">To run the application:</span></span>
1. <span data-ttu-id="283db-143">Выберите **Отладка**  ->  **Запуск без отладки**.</span><span class="sxs-lookup"><span data-stu-id="283db-143">Select **Debug** -> **Start Without Debugging**.</span></span>
2. <span data-ttu-id="283db-144">В окне консоли должен отобразиться текст `Hello quantum world!`.</span><span class="sxs-lookup"><span data-stu-id="283db-144">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> <span data-ttu-id="283db-145">Если в одном решении Visual Studio имеется несколько проектов, все проекты, содержащиеся в решении, должны находиться в той же папке, что и решение, или в одной из вложенных папок.</span><span class="sxs-lookup"><span data-stu-id="283db-145">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its sub-folders.</span></span>  


## <a name="next-steps"></a><span data-ttu-id="283db-146">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="283db-146">Next steps</span></span>

<span data-ttu-id="283db-147">После установки Quantum Development Kit в предпочитаемой среде вы можете написать и запустить [первую квантовую программу](xref:microsoft.quantum.quickstarts.qrng).</span><span class="sxs-lookup"><span data-stu-id="283db-147">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
