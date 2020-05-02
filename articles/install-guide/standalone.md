---
title: 'Выполнять программы Q # без драйвера и языка узла'
author: KittyYeungQ
ms.author: kitty
ms.date: 4/24/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
ms.openlocfilehash: e83acaf10af952da06abf4737ad2ec91f1cf1b8e
ms.sourcegitcommit: db23885adb7ff76cbf8bd1160d401a4f0471e549
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/01/2020
ms.locfileid: "82706807"
---
# <a name="q-command-line-applications"></a><span data-ttu-id="3ef66-102">Q # приложения командной строки</span><span class="sxs-lookup"><span data-stu-id="3ef66-102">Q# Command Line Applications</span></span>

<span data-ttu-id="3ef66-103">Программы Q # могут выполняться самостоятельно, без драйвера на основном языке, например C#, F # или Python.</span><span class="sxs-lookup"><span data-stu-id="3ef66-103">Q# programs can be executed on their own, without a driver in a host language like C#, F#, or Python.</span></span>

## <a name="pre-requisites"></a><span data-ttu-id="3ef66-104">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="3ef66-104">Pre-requisites</span></span>

- <span data-ttu-id="3ef66-105">[Пакет SDK для .NET Core 3.1 или более поздней версии](https://www.microsoft.com/net/download).</span><span class="sxs-lookup"><span data-stu-id="3ef66-105">[.NET Core SDK 3.1 or later](https://www.microsoft.com/net/download)</span></span>

## <a name="installation"></a><span data-ttu-id="3ef66-106">Установка</span><span class="sxs-lookup"><span data-stu-id="3ef66-106">Installation</span></span>

<span data-ttu-id="3ef66-107">Хотя вы можете создавать приложения Q # в любой интегрированной среде разработки, мы настоятельно рекомендуем использовать Visual Studio Code (VS Code) или интегрированную среду разработки Visual Studio для приложений Q #.</span><span class="sxs-lookup"><span data-stu-id="3ef66-107">While you can build Q# command line applications in any IDE, we highly recommend using Visual Studio Code (VS Code) or Visual Studio IDE for your Q# applications.</span></span> <span data-ttu-id="3ef66-108">С помощью VS Code или Visual Studio и расширения КДК Visual Studio Code Вы получаете доступ к более широким функциональным возможностям.</span><span class="sxs-lookup"><span data-stu-id="3ef66-108">By using VS Code or Visual Studio and the QDK Visual Studio Code extension you gain access to richer functionality.</span></span>

- <span data-ttu-id="3ef66-109">Установка [VS Code](https://code.visualstudio.com/download) (Windows, Linux и Mac)</span><span class="sxs-lookup"><span data-stu-id="3ef66-109">Install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac)</span></span>
- <span data-ttu-id="3ef66-110">Установите [расширение КДК для VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode) или</span><span class="sxs-lookup"><span data-stu-id="3ef66-110">Install the [QDK extension for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode) OR</span></span>
- <span data-ttu-id="3ef66-111">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 с включенной рабочей нагрузкой кроссплатформенной разработки .NET Core.</span><span class="sxs-lookup"><span data-stu-id="3ef66-111">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, with the .NET Core cross-platform development workload enabled</span></span>
- <span data-ttu-id="3ef66-112">Скачивание и установка [расширения Visual Studio](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span><span class="sxs-lookup"><span data-stu-id="3ef66-112">Download and install the [Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>


## <a name="develop-with-q-using-vs-code"></a><span data-ttu-id="3ef66-113">Разработка с помощью Q # using VS Code</span><span class="sxs-lookup"><span data-stu-id="3ef66-113">Develop with Q# using VS Code</span></span>

<span data-ttu-id="3ef66-114">Установите шаблоны проектов Quantum.</span><span class="sxs-lookup"><span data-stu-id="3ef66-114">Install the Quantum project templates:</span></span>

- <span data-ttu-id="3ef66-115">Перейти к **View** -> **палитре команд** просмотра</span><span class="sxs-lookup"><span data-stu-id="3ef66-115">Go to **View** -> **Command Palette**</span></span>
- <span data-ttu-id="3ef66-116">Выбор **Q #: Установка шаблонов проектов**</span><span class="sxs-lookup"><span data-stu-id="3ef66-116">Select **Q#: Install project templates**</span></span>

<span data-ttu-id="3ef66-117">Теперь Quantum Development Kit установлен и готов к использованию в ваших приложениях и библиотеках.</span><span class="sxs-lookup"><span data-stu-id="3ef66-117">You now have the Quantum Development Kit installed and ready to use in your own applications and libraries.</span></span>
- <span data-ttu-id="3ef66-118">Создайте новый проект:</span><span class="sxs-lookup"><span data-stu-id="3ef66-118">Create a new project:</span></span>
  - <span data-ttu-id="3ef66-119">Перейти к **View** -> **палитре команд** просмотра</span><span class="sxs-lookup"><span data-stu-id="3ef66-119">Go to **View** -> **Command Palette**</span></span>
  - <span data-ttu-id="3ef66-120">Выберите **Q #: создать новый проект**</span><span class="sxs-lookup"><span data-stu-id="3ef66-120">Select **Q#: Create New Project**</span></span>
  - <span data-ttu-id="3ef66-121">Выберите **автономное консольное приложение**</span><span class="sxs-lookup"><span data-stu-id="3ef66-121">Select **Standalone console application**</span></span>
  - <span data-ttu-id="3ef66-122">Перейдите в расположение файловой системы, в котором необходимо создать приложение.</span><span class="sxs-lookup"><span data-stu-id="3ef66-122">Navigate to the location on the file system where you would like to create the application</span></span>
  - <span data-ttu-id="3ef66-123">После создания проекта нажмите кнопку **Open new project...** (Открыть новый проект...).</span><span class="sxs-lookup"><span data-stu-id="3ef66-123">Click on the **Open new project...** button, once the project has been created</span></span>
        
- <span data-ttu-id="3ef66-124">Проверьте проект.</span><span class="sxs-lookup"><span data-stu-id="3ef66-124">Inspect the project</span></span>
  - <span data-ttu-id="3ef66-125">Вы должны увидеть, что файл с `Program.qs` именем Created — это программа Q #, которая определяет простую операцию для вывода сообщения на консоль.</span><span class="sxs-lookup"><span data-stu-id="3ef66-125">You should see that a file called `Program.qs` created, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

- <span data-ttu-id="3ef66-126">Запустите приложение:</span><span class="sxs-lookup"><span data-stu-id="3ef66-126">Run the application:</span></span>
  - <span data-ttu-id="3ef66-127">Последовательно выберите **терминал** -> **Новый терминал** .</span><span class="sxs-lookup"><span data-stu-id="3ef66-127">Go to **Terminal** -> **New Terminal**</span></span>
  - <span data-ttu-id="3ef66-128">Введите `dotnet run`</span><span class="sxs-lookup"><span data-stu-id="3ef66-128">Enter `dotnet run`</span></span>
  - <span data-ttu-id="3ef66-129">В окне консоли `Hello quantum world!` должен отобразиться следующий текст.</span><span class="sxs-lookup"><span data-stu-id="3ef66-129">You should see the following text in the output window `Hello quantum world!`</span></span>


> [!NOTE]
> * <span data-ttu-id="3ef66-130">Сейчас рабочие области с несколькими корневыми папками не поддерживаются в расширении Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="3ef66-130">Workspaces with multiple root folders are not currently supported by the Visual Studio Code extension.</span></span> <span data-ttu-id="3ef66-131">Если в одной рабочей области VS Code несколько проектов, все проекты нужно разместить в одной корневой папке.</span><span class="sxs-lookup"><span data-stu-id="3ef66-131">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

## <a name="develop-with-q-using-visual-studio"></a><span data-ttu-id="3ef66-132">Разработка с помощью Q # с использованием Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3ef66-132">Develop with Q# using Visual Studio</span></span>

<span data-ttu-id="3ef66-133">Проверьте установку, создав приложение `Hello World`.</span><span class="sxs-lookup"><span data-stu-id="3ef66-133">Verify the installation by creating a `Hello World` application</span></span>

- <span data-ttu-id="3ef66-134">Создайте приложение Q#.</span><span class="sxs-lookup"><span data-stu-id="3ef66-134">Create a new Q# application</span></span>
  - <span data-ttu-id="3ef66-135">Переход к **файлу** -> **Новый** -> **проект**</span><span class="sxs-lookup"><span data-stu-id="3ef66-135">Go to **File** -> **New** -> **Project**</span></span>
  - <span data-ttu-id="3ef66-136">Введите `Q#` в поле поиска.</span><span class="sxs-lookup"><span data-stu-id="3ef66-136">Type `Q#` in the search box</span></span>
  - <span data-ttu-id="3ef66-137">Выберите **Приложение Q#**.</span><span class="sxs-lookup"><span data-stu-id="3ef66-137">Select **Q# Application**</span></span>
  - <span data-ttu-id="3ef66-138">Нажмите кнопку **Далее** .</span><span class="sxs-lookup"><span data-stu-id="3ef66-138">Select **Next**</span></span>
  - <span data-ttu-id="3ef66-139">Выберите имя и расположение для приложения.</span><span class="sxs-lookup"><span data-stu-id="3ef66-139">Choose a name and location for your application</span></span>
  - <span data-ttu-id="3ef66-140">Выберите **создать** .</span><span class="sxs-lookup"><span data-stu-id="3ef66-140">Select **Create**</span></span>

- <span data-ttu-id="3ef66-141">Проверьте проект.</span><span class="sxs-lookup"><span data-stu-id="3ef66-141">Inspect the project</span></span>
  - <span data-ttu-id="3ef66-142">Вы должны увидеть, что создан файл `Program.qs` с именем, который представляет собой программу Q #, которая определяет простую операцию для вывода сообщения на консоль.</span><span class="sxs-lookup"><span data-stu-id="3ef66-142">You should see that a file called `Program.qs` has been created, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

- <span data-ttu-id="3ef66-143">Выполнение приложения</span><span class="sxs-lookup"><span data-stu-id="3ef66-143">Run the application</span></span>
  - <span data-ttu-id="3ef66-144">Выберите **Отладка** -> **Запуск без отладки**</span><span class="sxs-lookup"><span data-stu-id="3ef66-144">Select **Debug** -> **Start Without Debugging**</span></span>
  - <span data-ttu-id="3ef66-145">В окне консоли должен отобразиться текст `Hello quantum world!`.</span><span class="sxs-lookup"><span data-stu-id="3ef66-145">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> * <span data-ttu-id="3ef66-146">Если в одном решении Visual Studio несколько проектов, все проекты, включенные в решение, нужно разместить в той же папке, что и решение, или в одной из вложенных в нее папок.</span><span class="sxs-lookup"><span data-stu-id="3ef66-146">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its subfolders.</span></span>  


## <a name="whats-next"></a><span data-ttu-id="3ef66-147">Что дальше?</span><span class="sxs-lookup"><span data-stu-id="3ef66-147">What's next?</span></span>

<span data-ttu-id="3ef66-148">После установки Quantum Development Kit в предпочитаемой среде вы можете написать и запустить [первую квантовую программу](xref:microsoft.quantum.write-program).</span><span class="sxs-lookup"><span data-stu-id="3ef66-148">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
