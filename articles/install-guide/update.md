---
title: Сведения об обновлении Microsoft Quantum Development Kit (КДК)
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: fc430a77f88878437e662c5b54507f70f3c6e020
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/30/2019
ms.locfileid: "73185857"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="b6018-102">Обновление Microsoft Quantum Development Kit (КДК)</span><span class="sxs-lookup"><span data-stu-id="b6018-102">Update the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="b6018-103">Узнайте, как обновить Microsoft Quantum Development Kit (КДК) до последней версии.</span><span class="sxs-lookup"><span data-stu-id="b6018-103">Learn how to update the Microsoft Quantum Development Kit (QDK) to the latest version.</span></span>

<span data-ttu-id="b6018-104">В этой статье предполагается, что у вас уже установлен КДК.</span><span class="sxs-lookup"><span data-stu-id="b6018-104">This article assumes that you already have the QDK installed.</span></span> <span data-ttu-id="b6018-105">Если вы устанавливаете в первый раз, обратитесь к [руководству по установке](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="b6018-105">If you are installing for the first time, then please refer to the [installation guide](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="b6018-106">Действия по обновлению зависят от среды разработки.</span><span class="sxs-lookup"><span data-stu-id="b6018-106">The update steps depend on your development environment.</span></span> <span data-ttu-id="b6018-107">Выберите среду в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="b6018-107">Choose your environment from the following sections.</span></span>

## <a name="python"></a><span data-ttu-id="b6018-108">Python</span><span class="sxs-lookup"><span data-stu-id="b6018-108">Python</span></span>

1. <span data-ttu-id="b6018-109">Обновление ядра `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="b6018-109">Update the `iqsharp` kernel</span></span>

    ```bash
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="b6018-110">Проверка версии `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="b6018-110">Verify the `iqsharp` version</span></span>

    ```bash
    dotnet iqsharp --version
    ```

    <span data-ttu-id="b6018-111">Вы должны увидеть следующий результат.</span><span class="sxs-lookup"><span data-stu-id="b6018-111">You should see the following output:</span></span>

    ```bash
    iqsharp: 0.9.1909.3002
    Jupyter Core: 1.1.18837.0
    ```

1. <span data-ttu-id="b6018-112">Обновление пакета `qsharp`</span><span class="sxs-lookup"><span data-stu-id="b6018-112">Update the `qsharp` package</span></span>

    ```bash
    pip install qsharp --upgrade
    ```

1. <span data-ttu-id="b6018-113">Проверка версии `qsharp`</span><span class="sxs-lookup"><span data-stu-id="b6018-113">Verify the `qsharp` version</span></span>

    ```bash
    pip show qsharp
    ```

    <span data-ttu-id="b6018-114">Вы должны увидеть следующий результат.</span><span class="sxs-lookup"><span data-stu-id="b6018-114">You should see the following output:</span></span>

    ```bash
    Name: qsharp
    Version: 0.9.1909.3002
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```

1. <span data-ttu-id="b6018-115">Теперь вы можете использовать обновленную версию КДК для запуска существующих тактовых программ.</span><span class="sxs-lookup"><span data-stu-id="b6018-115">You can now use the updated QDK version to run your existing quantum programs.</span></span>

## <a name="jupyter-notebooks"></a><span data-ttu-id="b6018-116">Записные книжки Jupyter</span><span class="sxs-lookup"><span data-stu-id="b6018-116">Jupyter notebooks</span></span>

1. <span data-ttu-id="b6018-117">Обновление ядра `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="b6018-117">Update the `iqsharp` kernel</span></span>

    ```bash
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="b6018-118">Проверка версии `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="b6018-118">Verify the `iqsharp` version</span></span>

    ```bash
    dotnet iqsharp --version
    ```

    <span data-ttu-id="b6018-119">Вы должны увидеть следующий результат.</span><span class="sxs-lookup"><span data-stu-id="b6018-119">You should see the following output:</span></span>

    ```bash
    iqsharp: 0.9.1909.3002
    Jupyter Core: 1.1.18837.0
    ```

1. <span data-ttu-id="b6018-120">Теперь можно открыть имеющуюся записную книжку Jupyter и запустить ее с помощью обновленного КДК.</span><span class="sxs-lookup"><span data-stu-id="b6018-120">You can now open an existing Jupyter notebook and run it with the updated QDK.</span></span>

## <a name="c-on-windows-using-visual-studio"></a><span data-ttu-id="b6018-121">C#в Windows с помощью Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b6018-121">C# on Windows, using Visual Studio</span></span>

1. <span data-ttu-id="b6018-122">Обновление расширения Q # Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b6018-122">Update the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="b6018-123">Visual Studio предложит принять обновления для [расширения тактовой задержки Visual Studio](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span><span class="sxs-lookup"><span data-stu-id="b6018-123">Visual Studio prompts you to accept updates to the [Quantum Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="b6018-124">Принять обновление</span><span class="sxs-lookup"><span data-stu-id="b6018-124">Accept the update</span></span>

    > [!NOTE]
    > <span data-ttu-id="b6018-125">Шаблоны проектов обновляются с помощью расширения.</span><span class="sxs-lookup"><span data-stu-id="b6018-125">The project templates are updated with the extension.</span></span> <span data-ttu-id="b6018-126">Обновленные шаблоны применяются только к только что созданным проектам.</span><span class="sxs-lookup"><span data-stu-id="b6018-126">The updated templates apply to newly created projects only.</span></span> <span data-ttu-id="b6018-127">Код для существующих проектов не обновляется при обновлении расширения.</span><span class="sxs-lookup"><span data-stu-id="b6018-127">The code for your existing projects is not updated when the extension is updated.</span></span>

1. <span data-ttu-id="b6018-128">Обновление пакетов КДК</span><span class="sxs-lookup"><span data-stu-id="b6018-128">Update the QDK packages</span></span>

    - <span data-ttu-id="b6018-129">Открытие существующего приложения</span><span class="sxs-lookup"><span data-stu-id="b6018-129">Open an existing application</span></span>
    - <span data-ttu-id="b6018-130">Выберите **зависимости** в Обозреватель решений</span><span class="sxs-lookup"><span data-stu-id="b6018-130">Select **Dependencies** in the Solution Explorer</span></span>
    - <span data-ttu-id="b6018-131">Выберите **Управление пакетами NuGet** .</span><span class="sxs-lookup"><span data-stu-id="b6018-131">Select **Manage NuGet Packages**</span></span>
    - <span data-ttu-id="b6018-132">Обновление пакетов **Microsoft. тактов** до последней версии</span><span class="sxs-lookup"><span data-stu-id="b6018-132">Update the **Microsoft.Quantum** packages to the latest version</span></span>

1. <span data-ttu-id="b6018-133">Теперь вы можете запустить приложение с помощью последней версии КДК.</span><span class="sxs-lookup"><span data-stu-id="b6018-133">You can now run your application with the latest QDK.</span></span>

## <a name="c-using-vs-code"></a><span data-ttu-id="b6018-134">C#с помощью VS Code</span><span class="sxs-lookup"><span data-stu-id="b6018-134">C#, using VS Code</span></span>

1. <span data-ttu-id="b6018-135">Обновление расширения тактового VS Code</span><span class="sxs-lookup"><span data-stu-id="b6018-135">Update the Quantum VS Code extension</span></span>

    - <span data-ttu-id="b6018-136">Перезапустить VS Code</span><span class="sxs-lookup"><span data-stu-id="b6018-136">Restart VS Code</span></span>
    - <span data-ttu-id="b6018-137">Перейдите на вкладку **расширения** .</span><span class="sxs-lookup"><span data-stu-id="b6018-137">Navigate to the **Extensions** tab</span></span>
    - <span data-ttu-id="b6018-138">Выберите **Microsoft Quantum Development Kit для расширения Visual Studio Code**</span><span class="sxs-lookup"><span data-stu-id="b6018-138">Select the **Microsoft Quantum Development Kit for Visual Studio Code** extension</span></span>
    - <span data-ttu-id="b6018-139">Перезагрузить расширение</span><span class="sxs-lookup"><span data-stu-id="b6018-139">Reload the extension</span></span>

1. <span data-ttu-id="b6018-140">Обновите шаблоны проекта такта:</span><span class="sxs-lookup"><span data-stu-id="b6018-140">Update the Quantum project templates:</span></span>

   - <span data-ttu-id="b6018-141">Перейти к **просмотру** -> **палитре команд**</span><span class="sxs-lookup"><span data-stu-id="b6018-141">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="b6018-142">Выбор **Q #: Установка шаблонов проектов**</span><span class="sxs-lookup"><span data-stu-id="b6018-142">Select **Q#: Install project templates**</span></span>

1. <span data-ttu-id="b6018-143">Откройте существующее приложение в VS Code</span><span class="sxs-lookup"><span data-stu-id="b6018-143">Open an existing application in VS Code</span></span>

   - <span data-ttu-id="b6018-144">Изменение файла CSPROJ для добавления новых версий пакета</span><span class="sxs-lookup"><span data-stu-id="b6018-144">Edit the .csproj file to add the new package versions</span></span>

    ```xml
    <ItemGroup>
        <PackageReference Include="Microsoft.Quantum.Standard" Version="0.9.1909.3002" />
        <PackageReference Include="Microsoft.Quantum.Development.Kit" Version="0.9.1909.3002" />
    </ItemGroup>
    ```

    <span data-ttu-id="b6018-145">Если вы используете другие пакеты `Microsoft.Quantum`, обновите их.</span><span class="sxs-lookup"><span data-stu-id="b6018-145">If you use other `Microsoft.Quantum` packages, update these too.</span></span>

1. <span data-ttu-id="b6018-146">Теперь можно запустить приложение с обновленным КДК</span><span class="sxs-lookup"><span data-stu-id="b6018-146">You can now run your application with the updated QDK</span></span>

## <a name="c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="b6018-147">C#с помощью средства командной строки `dotnet`</span><span class="sxs-lookup"><span data-stu-id="b6018-147">C#, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="b6018-148">Обновление шаблонов проектов тактов для .NET</span><span class="sxs-lookup"><span data-stu-id="b6018-148">Update the Quantum project templates for .NET</span></span>

    ```bash
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

1. <span data-ttu-id="b6018-149">Обновление и запуск существующего приложения</span><span class="sxs-lookup"><span data-stu-id="b6018-149">Update and run an existing application</span></span>

    - <span data-ttu-id="b6018-150">Обновление версий пакета КДК в приложении</span><span class="sxs-lookup"><span data-stu-id="b6018-150">Update the QDK package versions in your application</span></span>

        ```bash
        dotnet add package Microsoft.Quantum.Development.Kit
        dotnet add package Microsoft.Quantum.Standard
        ```

        <span data-ttu-id="b6018-151">Если приложение использует другие пакеты `Microsoft.Quantum`, обновите их.</span><span class="sxs-lookup"><span data-stu-id="b6018-151">If your application uses any other `Microsoft.Quantum` packages, update these too.</span></span>

    - <span data-ttu-id="b6018-152">Выполнение приложения</span><span class="sxs-lookup"><span data-stu-id="b6018-152">Run the application</span></span>

        ```bash
        dotnet run
        ```

    - <span data-ttu-id="b6018-153">Приложение будет запущено с новыми версиями пакетов</span><span class="sxs-lookup"><span data-stu-id="b6018-153">Your application will run with the new package versions</span></span>

## <a name="whats-next"></a><span data-ttu-id="b6018-154">Что дальше?</span><span class="sxs-lookup"><span data-stu-id="b6018-154">What's next?</span></span>

<span data-ttu-id="b6018-155">После обновления пакета средств разработки тактов в предпочтительной среде можно продолжить разработку и запуск тактовых программ.</span><span class="sxs-lookup"><span data-stu-id="b6018-155">Now that you have updated the Quantum Development Kit in your preferred environment, you can continue to develop and run your quantum programs.</span></span> <span data-ttu-id="b6018-156">Если вы еще не написали программу, вы можете начать работу с [первой тактовой программой](xref:microsoft.quantum.write-program).</span><span class="sxs-lookup"><span data-stu-id="b6018-156">If you have not written a program yet, you can get started with [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
