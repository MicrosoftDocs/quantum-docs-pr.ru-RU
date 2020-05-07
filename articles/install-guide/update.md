---
title: Сведения об обновлении Microsoft Quantum Development Kit (КДК)
description: 'Описывает, как обновить проекты Q # и Microsoft Quantum Development Kit до текущей версии.'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: bf6d6d3d80af485b555429f25b125bfea685bebf
ms.sourcegitcommit: c57c271ab73f75f165401651fad2b5bc143e9c8f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/06/2020
ms.locfileid: "82862213"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="89a28-103">Обновление Microsoft Quantum Development Kit (КДК)</span><span class="sxs-lookup"><span data-stu-id="89a28-103">Update the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="89a28-104">Узнайте, как обновить Microsoft Quantum Development Kit (КДК) до последней версии.</span><span class="sxs-lookup"><span data-stu-id="89a28-104">Learn how to update the Microsoft Quantum Development Kit (QDK) to the latest version.</span></span>

<span data-ttu-id="89a28-105">В этой статье предполагается, что у вас уже установлен КДК.</span><span class="sxs-lookup"><span data-stu-id="89a28-105">This article assumes that you already have the QDK installed.</span></span> <span data-ttu-id="89a28-106">Если вы устанавливаете в первый раз, обратитесь к [руководству по установке](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="89a28-106">If you are installing for the first time, then please refer to the [installation guide](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="89a28-107">Мы рекомендуем поддерживать последние версии КДК в актуальном состоянии.</span><span class="sxs-lookup"><span data-stu-id="89a28-107">We recommend keeping up to date with the latest QDK release.</span></span> <span data-ttu-id="89a28-108">Следуйте этому руководству по обновлению, чтобы выполнить обновление до последней версии КДК.</span><span class="sxs-lookup"><span data-stu-id="89a28-108">Follow this update guide to upgrade to the most recent QDK version.</span></span> <span data-ttu-id="89a28-109">Процесс состоит из двух частей:</span><span class="sxs-lookup"><span data-stu-id="89a28-109">The process consists of two parts:</span></span>
1. <span data-ttu-id="89a28-110">Обновление существующих файлов Q # и проектов для согласования кода с любым обновленным синтаксисом</span><span class="sxs-lookup"><span data-stu-id="89a28-110">updating your existing Q# files and projects to align your code with any updated syntax</span></span>
2. <span data-ttu-id="89a28-111">Обновление самого КДК для выбранной среды разработки</span><span class="sxs-lookup"><span data-stu-id="89a28-111">updating the QDK itself for your chosen development environment</span></span> 

## <a name="updating-q-projects"></a><span data-ttu-id="89a28-112">Обновление проектов Q #</span><span class="sxs-lookup"><span data-stu-id="89a28-112">Updating Q# Projects</span></span> 

<span data-ttu-id="89a28-113">Независимо от того, используете ли вы C# или Python для размещения операций Q #, следуйте этим инструкциям, чтобы обновить проекты Q #.</span><span class="sxs-lookup"><span data-stu-id="89a28-113">Regardless of whether you are using C# or Python to host Q# operations, follow these instructions to update your Q# projects.</span></span>

1. <span data-ttu-id="89a28-114">Сначала убедитесь, что у вас установлена последняя версия [пакет SDK для .NET Core 3,1](https://dotnet.microsoft.com/download).</span><span class="sxs-lookup"><span data-stu-id="89a28-114">First, check that you have the latest version of the [.NET Core SDK 3.1](https://dotnet.microsoft.com/download).</span></span> <span data-ttu-id="89a28-115">В командной строке выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="89a28-115">Run the following command in the command prompt:</span></span>

    ```dotnetcli
    dotnet --version
    ```

    <span data-ttu-id="89a28-116">Убедитесь, что выходные `3.1.100` данные имеют значение или выше.</span><span class="sxs-lookup"><span data-stu-id="89a28-116">Verify the output is `3.1.100` or higher.</span></span> <span data-ttu-id="89a28-117">В противном случае установите [последнюю версию](https://dotnet.microsoft.com/download) и снова проверьте.</span><span class="sxs-lookup"><span data-stu-id="89a28-117">If not, install the [latest version](https://dotnet.microsoft.com/download) and check again.</span></span> <span data-ttu-id="89a28-118">Затем следуйте приведенным ниже инструкциям в зависимости от настроек (Visual Studio, Visual Studio Code или непосредственно в командной строке).</span><span class="sxs-lookup"><span data-stu-id="89a28-118">Then follow the instructions below depending on your setup (Visual Studio, Visual Studio Code, or directly the command line).</span></span>

### <a name="update-q-projects-in-visual-studio"></a><span data-ttu-id="89a28-119">Обновление проектов Q # в Visual Studio</span><span class="sxs-lookup"><span data-stu-id="89a28-119">Update Q# projects in Visual Studio</span></span>
 
1. <span data-ttu-id="89a28-120">Обновление до последней версии Visual Studio 2019. инструкции см. [здесь](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) .</span><span class="sxs-lookup"><span data-stu-id="89a28-120">Update to the latest version of Visual Studio 2019, see [here](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) for instructions</span></span>
2. <span data-ttu-id="89a28-121">Открытие решения в Visual Studio</span><span class="sxs-lookup"><span data-stu-id="89a28-121">Open your solution in Visual Studio</span></span>
3. <span data-ttu-id="89a28-122">В меню выберите **Сборка** -> **Очистить решение** .</span><span class="sxs-lookup"><span data-stu-id="89a28-122">From the menu, select **Build** -> **Clean Solution**</span></span>
4. <span data-ttu-id="89a28-123">В каждом из CSPROJ-файлов обновите целевую платформу до `netcoreapp3.1` (или `netstandard2.1` , если это проект библиотеки).</span><span class="sxs-lookup"><span data-stu-id="89a28-123">In each of your .csproj files, update the target framework to `netcoreapp3.1` (or `netstandard2.1` if it is a library project).</span></span>
    <span data-ttu-id="89a28-124">То есть измените строки формы:</span><span class="sxs-lookup"><span data-stu-id="89a28-124">That is, edit lines of the form:</span></span>

    ```xml
    <TargetFramework>netcoreapp3.1</TargetFramework>
    ```

    <span data-ttu-id="89a28-125">Дополнительные сведения об указании целевых платформ можно найти [здесь](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span><span class="sxs-lookup"><span data-stu-id="89a28-125">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>
5. <span data-ttu-id="89a28-126">Сохранение и закрытие всех файлов в решении</span><span class="sxs-lookup"><span data-stu-id="89a28-126">Save and close all files in your solution</span></span>
6. <span data-ttu-id="89a28-127">Выберите **инструменты** -> **Командная строка** -> **Командная строка разработчика**</span><span class="sxs-lookup"><span data-stu-id="89a28-127">Select **Tools** -> **Command Line** -> **Developer Command Prompt**</span></span>
7. <span data-ttu-id="89a28-128">Для каждого проекта в решении выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="89a28-128">For each project in the solution, run the following command:</span></span>

    ```dotnetcli
    dotnet add [project_name].csproj package Microsoft.Quantum.Development.Kit
    ```

   <span data-ttu-id="89a28-129">Если в проектах используются любые другие пакеты Microsoft. тактов (например, Microsoft. тактов. numeric), выполните для них команду.</span><span class="sxs-lookup"><span data-stu-id="89a28-129">If your projects use any other Microsoft.Quantum packages (e.g. Microsoft.Quantum.Numerics), run the command for these too.</span></span>
8. <span data-ttu-id="89a28-130">Закройте командную строку и выберите **Сборка** -> сборка**решения** (не *выбирайте* Перестроение решения).</span><span class="sxs-lookup"><span data-stu-id="89a28-130">Close the command prompt and select **Build** -> **Build Solution** (do *not* select Rebuild Solution)</span></span>

<span data-ttu-id="89a28-131">Теперь вы можете перейти к [обновлению расширения Visual Studio КДК](#update-visual-studio-qdk-extension).</span><span class="sxs-lookup"><span data-stu-id="89a28-131">You can now skip ahead to [update your Visual Studio QDK extension](#update-visual-studio-qdk-extension).</span></span>


### <a name="update-q-projects-in-visual-studio-code"></a><span data-ttu-id="89a28-132">Обновление проектов Q # в Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="89a28-132">Update Q# projects in Visual Studio Code</span></span>

1. <span data-ttu-id="89a28-133">В Visual Studio Code откройте папку, содержащую обновляемый проект.</span><span class="sxs-lookup"><span data-stu-id="89a28-133">In Visual Studio Code, open the folder containing the project to update</span></span>
2. <span data-ttu-id="89a28-134">Выберите **терминал** -> **Новый терминал**</span><span class="sxs-lookup"><span data-stu-id="89a28-134">Select **Terminal** -> **New Terminal**</span></span>
3. <span data-ttu-id="89a28-135">Следуйте инструкциям по обновлению с помощью командной строки (непосредственно ниже).</span><span class="sxs-lookup"><span data-stu-id="89a28-135">Follow the instructions for updating using the command line (directly below)</span></span>

### <a name="update-q-projects-using-the-command-line"></a><span data-ttu-id="89a28-136">Обновление проектов Q # с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="89a28-136">Update Q# projects using the command line</span></span>

1. <span data-ttu-id="89a28-137">Перейдите к папке, содержащей файл проекта</span><span class="sxs-lookup"><span data-stu-id="89a28-137">Navigate to the folder containing your project file</span></span>
2. <span data-ttu-id="89a28-138">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="89a28-138">Run the following command:</span></span>

    ```dotnetcli
    dotnet clean [project_name].csproj
    ```

3. <span data-ttu-id="89a28-139">В каждом из CSPROJ-файлов обновите целевую платформу до `netcoreapp3.1` (или `netstandard2.1` , если это проект библиотеки).</span><span class="sxs-lookup"><span data-stu-id="89a28-139">In each of your .csproj files, update the target framework to `netcoreapp3.1` (or `netstandard2.1` if it is a library project).</span></span>
    <span data-ttu-id="89a28-140">То есть измените строки формы:</span><span class="sxs-lookup"><span data-stu-id="89a28-140">That is, edit lines of the form:</span></span>

    ```xml
    <TargetFramework>netcoreapp3.1</TargetFramework>
    ```

    <span data-ttu-id="89a28-141">Дополнительные сведения об указании целевых платформ можно найти [здесь](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span><span class="sxs-lookup"><span data-stu-id="89a28-141">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>
4. <span data-ttu-id="89a28-142">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="89a28-142">Run the following command:</span></span>

    ```dotnetcli
    dotnet add package Microsoft.Quantum.Development.Kit
    ```

    <span data-ttu-id="89a28-143">Если в проекте используются любые другие пакеты Microsoft. тактов (например, Microsoft. тактов. numeric), выполните для них команду.</span><span class="sxs-lookup"><span data-stu-id="89a28-143">If your project uses any other Microsoft.Quantum packages (e.g. Microsoft.Quantum.Numerics), run the command for these too.</span></span>
5. <span data-ttu-id="89a28-144">Сохраните и закройте все файлы.</span><span class="sxs-lookup"><span data-stu-id="89a28-144">Save and close all files.</span></span>
6. <span data-ttu-id="89a28-145">Повторите 1-4 для каждой зависимости проекта, а затем вернитесь к папке, содержащей основной проект, и выполните команду:</span><span class="sxs-lookup"><span data-stu-id="89a28-145">Repeat 1-4 for each project dependency, then navigate back to the folder containing your main project and run:</span></span>

    ```dotnetcli
    dotnet build [project_name].csproj
    ```

<span data-ttu-id="89a28-146">После обновления проектов Q # следуйте приведенным ниже инструкциям, чтобы обновить саму КДК.</span><span class="sxs-lookup"><span data-stu-id="89a28-146">With your Q# projects now updated, follow the instructions below to update the QDK itself.</span></span>

## <a name="updating-the-qdk"></a><span data-ttu-id="89a28-147">Обновление КДК</span><span class="sxs-lookup"><span data-stu-id="89a28-147">Updating the QDK</span></span>

<span data-ttu-id="89a28-148">Процесс обновления КДК зависит от языка и среды разработки.</span><span class="sxs-lookup"><span data-stu-id="89a28-148">The process to update the QDK varies depending on your development language and environment.</span></span>
<span data-ttu-id="89a28-149">Выберите среду разработки ниже.</span><span class="sxs-lookup"><span data-stu-id="89a28-149">Select your development environment below.</span></span>

* [<span data-ttu-id="89a28-150">Python: обновление расширения IQ</span><span class="sxs-lookup"><span data-stu-id="89a28-150">Python: update the IQ# extension</span></span>](#update-iq-for-python)
* [<span data-ttu-id="89a28-151">Записные книжки Jupyter: обновление расширения IQ</span><span class="sxs-lookup"><span data-stu-id="89a28-151">Jupyter Notebooks: update the IQ# extension</span></span>](#update-iq-for-jupyter-notebooks)
* [<span data-ttu-id="89a28-152">Visual Studio: обновление расширения КДК</span><span class="sxs-lookup"><span data-stu-id="89a28-152">Visual Studio: update the QDK extension</span></span>](#update-visual-studio-qdk-extension)
* [<span data-ttu-id="89a28-153">VS Code: обновление расширения КДК</span><span class="sxs-lookup"><span data-stu-id="89a28-153">VS Code: update the QDK extension</span></span>](#update-vs-code-qdk-extension)
* [<span data-ttu-id="89a28-154">Командная строка и C#: обновление шаблонов проектов</span><span class="sxs-lookup"><span data-stu-id="89a28-154">Command-line and C#: update project templates</span></span>](#c-using-the-dotnet-command-line-tool)


### <a name="update-iq-for-python"></a><span data-ttu-id="89a28-155">Обновление IQ # для Python</span><span class="sxs-lookup"><span data-stu-id="89a28-155">Update IQ# for Python</span></span>

1. <span data-ttu-id="89a28-156">Обновление `iqsharp` ядра</span><span class="sxs-lookup"><span data-stu-id="89a28-156">Update the `iqsharp` kernel</span></span> 

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. <span data-ttu-id="89a28-157">Проверка `iqsharp` версии</span><span class="sxs-lookup"><span data-stu-id="89a28-157">Verify the `iqsharp` version</span></span>

    ```dotnetcli
    dotnet iqsharp --version
    ```

    <span data-ttu-id="89a28-158">Должны выводиться следующие данные:</span><span class="sxs-lookup"><span data-stu-id="89a28-158">You should see the following output:</span></span>

    ```bash
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    <span data-ttu-id="89a28-159">Не беспокойтесь, если `iqsharp` ваша версия более высокая, она должна соответствовать [последнему выпуску](xref:microsoft.quantum.relnotes).</span><span class="sxs-lookup"><span data-stu-id="89a28-159">Don't worry if your `iqsharp` version is higher, it should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

3. <span data-ttu-id="89a28-160">Обновление `qsharp` пакета</span><span class="sxs-lookup"><span data-stu-id="89a28-160">Update the `qsharp` package</span></span>

    ```bash
    pip install qsharp --upgrade
    ```

4. <span data-ttu-id="89a28-161">Проверка `qsharp` версии</span><span class="sxs-lookup"><span data-stu-id="89a28-161">Verify the `qsharp` version</span></span>

    ```bash
    pip show qsharp
    ```

    <span data-ttu-id="89a28-162">Должны выводиться следующие данные:</span><span class="sxs-lookup"><span data-stu-id="89a28-162">You should see the following output:</span></span>

    ```bash
    Name: qsharp
    Version: 0.10.1912.501
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```

5. <span data-ttu-id="89a28-163">Выполните следующую команду из расположения `.qs` файлов</span><span class="sxs-lookup"><span data-stu-id="89a28-163">Run the following command from the location of your `.qs` files</span></span>

    ```bash
    python -c "import qsharp; qsharp.reload()"
    ```

6. <span data-ttu-id="89a28-164">Теперь вы можете использовать обновленную версию КДК для запуска существующих тактовых программ.</span><span class="sxs-lookup"><span data-stu-id="89a28-164">You can now use the updated QDK version to run your existing quantum programs.</span></span>

### <a name="update-iq-for-jupyter-notebooks"></a><span data-ttu-id="89a28-165">Обновление IQ # для записных книжек Jupyter</span><span class="sxs-lookup"><span data-stu-id="89a28-165">Update IQ# for Jupyter Notebooks</span></span>

1. <span data-ttu-id="89a28-166">Обновление `iqsharp` ядра</span><span class="sxs-lookup"><span data-stu-id="89a28-166">Update the `iqsharp` kernel</span></span>

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. <span data-ttu-id="89a28-167">Проверка `iqsharp` версии</span><span class="sxs-lookup"><span data-stu-id="89a28-167">Verify the `iqsharp` version</span></span>

    ```dotnetcli
    dotnet iqsharp --version
    ```

    <span data-ttu-id="89a28-168">Вывод приложения должен быть аналогичен приведенному ниже:</span><span class="sxs-lookup"><span data-stu-id="89a28-168">Your output should be similar to the following:</span></span>

    ```bash
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    <span data-ttu-id="89a28-169">Не беспокойтесь, если `iqsharp` ваша версия более высокая, она должна соответствовать [последнему выпуску](xref:microsoft.quantum.relnotes).</span><span class="sxs-lookup"><span data-stu-id="89a28-169">Don't worry if your `iqsharp` version is higher, it should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

3. <span data-ttu-id="89a28-170">Выполните следующую команду в ячейке Jupyter Notebook:</span><span class="sxs-lookup"><span data-stu-id="89a28-170">Run the following command from a cell in your Jupyter Notebook:</span></span>

    ```
    %workspace reload
    ```

4. <span data-ttu-id="89a28-171">Теперь можно открыть имеющуюся записную книжку Jupyter и запустить ее с помощью обновленного КДК.</span><span class="sxs-lookup"><span data-stu-id="89a28-171">You can now open an existing Jupyter notebook and run it with the updated QDK.</span></span>

### <a name="update-visual-studio-qdk-extension"></a><span data-ttu-id="89a28-172">Обновление расширения Visual Studio КДК</span><span class="sxs-lookup"><span data-stu-id="89a28-172">Update Visual Studio QDK extension</span></span>

1. <span data-ttu-id="89a28-173">Обновление расширения Q # Visual Studio</span><span class="sxs-lookup"><span data-stu-id="89a28-173">Update the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="89a28-174">Visual Studio предложит принять обновления для [расширения тактовой задержки Visual Studio](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span><span class="sxs-lookup"><span data-stu-id="89a28-174">Visual Studio prompts you to accept updates to the [Quantum Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="89a28-175">Принять обновление</span><span class="sxs-lookup"><span data-stu-id="89a28-175">Accept the update</span></span>

    > [!NOTE]
    > <span data-ttu-id="89a28-176">Шаблоны проектов обновляются с помощью расширения.</span><span class="sxs-lookup"><span data-stu-id="89a28-176">The project templates are updated with the extension.</span></span> <span data-ttu-id="89a28-177">Обновленные шаблоны применяются только к только что созданным проектам.</span><span class="sxs-lookup"><span data-stu-id="89a28-177">The updated templates apply to newly created projects only.</span></span> <span data-ttu-id="89a28-178">Код для существующих проектов не обновляется при обновлении расширения.</span><span class="sxs-lookup"><span data-stu-id="89a28-178">The code for your existing projects is not updated when the extension is updated.</span></span>

### <a name="update-vs-code-qdk-extension"></a><span data-ttu-id="89a28-179">Обновление расширения VS Code КДК</span><span class="sxs-lookup"><span data-stu-id="89a28-179">Update VS Code QDK extension</span></span>

1. <span data-ttu-id="89a28-180">Обновление расширения тактового VS Code</span><span class="sxs-lookup"><span data-stu-id="89a28-180">Update the Quantum VS Code extension</span></span>

    - <span data-ttu-id="89a28-181">Перезапустить VS Code</span><span class="sxs-lookup"><span data-stu-id="89a28-181">Restart VS Code</span></span>
    - <span data-ttu-id="89a28-182">Перейдите на вкладку **расширения** .</span><span class="sxs-lookup"><span data-stu-id="89a28-182">Navigate to the **Extensions** tab</span></span>
    - <span data-ttu-id="89a28-183">Выберите **Microsoft Quantum Development Kit для расширения Visual Studio Code**</span><span class="sxs-lookup"><span data-stu-id="89a28-183">Select the **Microsoft Quantum Development Kit for Visual Studio Code** extension</span></span>
    - <span data-ttu-id="89a28-184">Перезагрузить расширение</span><span class="sxs-lookup"><span data-stu-id="89a28-184">Reload the extension</span></span>

2. <span data-ttu-id="89a28-185">Обновите шаблоны проекта такта:</span><span class="sxs-lookup"><span data-stu-id="89a28-185">Update the Quantum project templates:</span></span>

   - <span data-ttu-id="89a28-186">Перейти к **View** -> **палитре команд** просмотра</span><span class="sxs-lookup"><span data-stu-id="89a28-186">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="89a28-187">Выбор **Q #: Установка шаблонов проектов**</span><span class="sxs-lookup"><span data-stu-id="89a28-187">Select **Q#: Install project templates**</span></span>
   - <span data-ttu-id="89a28-188">Через несколько секунд должно появиться всплывающее окно с подтверждением успешной установки шаблонов проектов.</span><span class="sxs-lookup"><span data-stu-id="89a28-188">After a few seconds you should get a popup confirming "project templates installed successfully"</span></span>

### <a name="c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="89a28-189">C# с помощью программы `dotnet` командной строки</span><span class="sxs-lookup"><span data-stu-id="89a28-189">C#, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="89a28-190">Обновление шаблонов проектов тактов для .NET</span><span class="sxs-lookup"><span data-stu-id="89a28-190">Update the Quantum project templates for .NET</span></span>

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

## <a name="whats-next"></a><span data-ttu-id="89a28-191">Что дальше?</span><span class="sxs-lookup"><span data-stu-id="89a28-191">What's next?</span></span>

<span data-ttu-id="89a28-192">После обновления пакета средств разработки тактов в предпочтительной среде можно продолжить разработку и запуск тактовых программ.</span><span class="sxs-lookup"><span data-stu-id="89a28-192">Now that you have updated the Quantum Development Kit in your preferred environment, you can continue to develop and run your quantum programs.</span></span> <span data-ttu-id="89a28-193">Если вы еще не написали программу, вы можете начать работу с [первой тактовой программой](xref:microsoft.quantum.write-program).</span><span class="sxs-lookup"><span data-stu-id="89a28-193">If you have not written a program yet, you can get started with [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
