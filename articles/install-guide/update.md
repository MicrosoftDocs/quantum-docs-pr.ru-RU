---
title: Сведения об обновлении Microsoft Quantum Development Kit (КДК)
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: f19285ae0e008b3460d06430a236f098d716e268
ms.sourcegitcommit: 5094c0a60cbafdee669c8728b92df281071259b9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2020
ms.locfileid: "77036327"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="fb334-102">Обновление Microsoft Quantum Development Kit (КДК)</span><span class="sxs-lookup"><span data-stu-id="fb334-102">Update the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="fb334-103">Узнайте, как обновить Microsoft Quantum Development Kit (КДК) до последней версии.</span><span class="sxs-lookup"><span data-stu-id="fb334-103">Learn how to update the Microsoft Quantum Development Kit (QDK) to the latest version.</span></span>

<span data-ttu-id="fb334-104">В этой статье предполагается, что у вас уже установлен КДК.</span><span class="sxs-lookup"><span data-stu-id="fb334-104">This article assumes that you already have the QDK installed.</span></span> <span data-ttu-id="fb334-105">Если вы устанавливаете в первый раз, обратитесь к [руководству по установке](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="fb334-105">If you are installing for the first time, then please refer to the [installation guide](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="fb334-106">Мы рекомендуем поддерживать последние версии КДК в актуальном состоянии.</span><span class="sxs-lookup"><span data-stu-id="fb334-106">We recommend keeping up to date with the latest QDK release.</span></span> <span data-ttu-id="fb334-107">Следуйте этому руководству по обновлению, чтобы выполнить обновление до последней версии КДК.</span><span class="sxs-lookup"><span data-stu-id="fb334-107">Follow this update guide to upgrade to the most recent QDK version.</span></span> <span data-ttu-id="fb334-108">Процесс состоит из двух частей:</span><span class="sxs-lookup"><span data-stu-id="fb334-108">The process consists of two parts:</span></span>
1. <span data-ttu-id="fb334-109">Обновление существующих файлов Q # и проектов для согласования кода с любым обновленным синтаксисом</span><span class="sxs-lookup"><span data-stu-id="fb334-109">updating your existing Q# files and projects to align your code with any updated syntax</span></span>
2. <span data-ttu-id="fb334-110">Обновление самого КДК для выбранной среды разработки</span><span class="sxs-lookup"><span data-stu-id="fb334-110">updating the QDK itself for your chosen development environment</span></span> 

## <a name="updating-q-projects"></a><span data-ttu-id="fb334-111">Обновление проектов Q #</span><span class="sxs-lookup"><span data-stu-id="fb334-111">Updating Q# Projects</span></span> 

<span data-ttu-id="fb334-112">Независимо от того, используете C# ли вы или Python для размещения операций q #, следуйте этим инструкциям, чтобы обновить проекты q #.</span><span class="sxs-lookup"><span data-stu-id="fb334-112">Regardless of whether you are using C# or Python to host Q# operations, follow these instructions to update your Q# projects.</span></span>

1. <span data-ttu-id="fb334-113">Сначала убедитесь, что у вас установлена последняя версия [пакет SDK для .NET Core 3,1](https://dotnet.microsoft.com/download).</span><span class="sxs-lookup"><span data-stu-id="fb334-113">First, check that you have the latest version of the [.NET Core SDK 3.1](https://dotnet.microsoft.com/download).</span></span> <span data-ttu-id="fb334-114">В командной строке выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="fb334-114">Run the following command in the command prompt:</span></span>

    ```dotnetcli
    dotnet --version
    ```

    <span data-ttu-id="fb334-115">Убедитесь, что выходные данные имеют `3.1.100` или выше.</span><span class="sxs-lookup"><span data-stu-id="fb334-115">Verify the output is `3.1.100` or higher.</span></span> <span data-ttu-id="fb334-116">В противном случае установите [последнюю версию](https://dotnet.microsoft.com/download) и снова проверьте.</span><span class="sxs-lookup"><span data-stu-id="fb334-116">If not, install the [latest version](https://dotnet.microsoft.com/download) and check again.</span></span> <span data-ttu-id="fb334-117">Затем следуйте приведенным ниже инструкциям в зависимости от настроек (Visual Studio, Visual Studio Code или непосредственно в командной строке).</span><span class="sxs-lookup"><span data-stu-id="fb334-117">Then follow the instructions below depending on your setup (Visual Studio, Visual Studio Code, or directly the command line).</span></span>

### <a name="update-q-projects-in-visual-studio"></a><span data-ttu-id="fb334-118">Обновление проектов Q # в Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fb334-118">Update Q# projects in Visual Studio</span></span>
 
1. <span data-ttu-id="fb334-119">Обновление до последней версии Visual Studio 2019. инструкции см. [здесь](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) .</span><span class="sxs-lookup"><span data-stu-id="fb334-119">Update to the latest version of Visual Studio 2019, see [here](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) for instructions</span></span>
2. <span data-ttu-id="fb334-120">Открытие решения в Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fb334-120">Open your solution in Visual Studio</span></span>
3. <span data-ttu-id="fb334-121">В меню выберите **сборка** -> **Очистить решение** .</span><span class="sxs-lookup"><span data-stu-id="fb334-121">From the menu, select **Build** -> **Clean Solution**</span></span>
4. <span data-ttu-id="fb334-122">В каждом из CSPROJ-файлов обновите целевую платформу до `netcoreapp3.0` (или `netstandard2.1`, если это проект библиотеки).</span><span class="sxs-lookup"><span data-stu-id="fb334-122">In each of your .csproj files, update the target framework to `netcoreapp3.0` (or `netstandard2.1` if it is a library project).</span></span>
    <span data-ttu-id="fb334-123">То есть измените строки формы:</span><span class="sxs-lookup"><span data-stu-id="fb334-123">That is, edit lines of the form:</span></span>

    ```xml
    <TargetFramework>netcoreapp3.0</TargetFramework>
    ```

    <span data-ttu-id="fb334-124">Дополнительные сведения об указании целевых платформ можно найти [здесь](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span><span class="sxs-lookup"><span data-stu-id="fb334-124">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>
5. <span data-ttu-id="fb334-125">Сохранение и закрытие всех файлов в решении</span><span class="sxs-lookup"><span data-stu-id="fb334-125">Save and close all files in your solution</span></span>
6. <span data-ttu-id="fb334-126">Выберите **инструменты** -> **командной строки** -> **Командная строка разработчика**</span><span class="sxs-lookup"><span data-stu-id="fb334-126">Select **Tools** -> **Command Line** -> **Developer Command Prompt**</span></span>
7. <span data-ttu-id="fb334-127">Для каждого проекта в решении выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="fb334-127">For each project in the solution, run the following command:</span></span>

    ```dotnetcli
    dotnet add [project_name].csproj package Microsoft.Quantum.Development.Kit
    ```

   <span data-ttu-id="fb334-128">Если в проектах используются любые другие пакеты Microsoft. тактов (например, Microsoft. тактов. numeric), выполните для них команду.</span><span class="sxs-lookup"><span data-stu-id="fb334-128">If your projects use any other Microsoft.Quantum packages (e.g. Microsoft.Quantum.Numerics), run the command for these too.</span></span>
8. <span data-ttu-id="fb334-129">Закройте командную строку и выберите **build** -> **Build Solution** ( *не* выбирайте Rebuild Solution).</span><span class="sxs-lookup"><span data-stu-id="fb334-129">Close the command prompt and select **Build** -> **Build Solution** (do *not* select Rebuild Solution)</span></span>

<span data-ttu-id="fb334-130">Теперь вы можете перейти к [обновлению расширения Visual Studio КДК](#update-visual-studio-qdk-extension).</span><span class="sxs-lookup"><span data-stu-id="fb334-130">You can now skip ahead to [update your Visual Studio QDK extension](#update-visual-studio-qdk-extension).</span></span>


### <a name="update-q-projects-in-visual-studio-code"></a><span data-ttu-id="fb334-131">Обновление проектов Q # в Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="fb334-131">Update Q# projects in Visual Studio Code</span></span>

1. <span data-ttu-id="fb334-132">В Visual Studio Code откройте папку, содержащую обновляемый проект.</span><span class="sxs-lookup"><span data-stu-id="fb334-132">In Visual Studio Code, open the folder containing the project to update</span></span>
2. <span data-ttu-id="fb334-133">Выберите **терминал** -> **Новый терминал**</span><span class="sxs-lookup"><span data-stu-id="fb334-133">Select **Terminal** -> **New Terminal**</span></span>
3. <span data-ttu-id="fb334-134">Следуйте инструкциям по обновлению с помощью командной строки (непосредственно ниже).</span><span class="sxs-lookup"><span data-stu-id="fb334-134">Follow the instructions for updating using the command line (directly below)</span></span>

### <a name="update-q-projects-using-the-command-line"></a><span data-ttu-id="fb334-135">Обновление проектов Q # с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="fb334-135">Update Q# projects using the command line</span></span>

1. <span data-ttu-id="fb334-136">Перейдите к папке, содержащей файл проекта</span><span class="sxs-lookup"><span data-stu-id="fb334-136">Navigate to the folder containing your project file</span></span>
2. <span data-ttu-id="fb334-137">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="fb334-137">Run the following command:</span></span>

    ```dotnetcli
    dotnet clean [project_name].csproj
    ```

3. <span data-ttu-id="fb334-138">В каждом из CSPROJ-файлов обновите целевую платформу до `netcoreapp3.0` (или `netstandard2.1`, если это проект библиотеки).</span><span class="sxs-lookup"><span data-stu-id="fb334-138">In each of your .csproj files, update the target framework to `netcoreapp3.0` (or `netstandard2.1` if it is a library project).</span></span>
    <span data-ttu-id="fb334-139">То есть измените строки формы:</span><span class="sxs-lookup"><span data-stu-id="fb334-139">That is, edit lines of the form:</span></span>

    ```xml
    <TargetFramework>netcoreapp3.0</TargetFramework>
    ```

    <span data-ttu-id="fb334-140">Дополнительные сведения об указании целевых платформ можно найти [здесь](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span><span class="sxs-lookup"><span data-stu-id="fb334-140">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>
4. <span data-ttu-id="fb334-141">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="fb334-141">Run the following command:</span></span>

    ```dotnetcli
    dotnet add package Microsoft.Quantum.Development.Kit
    ```

    <span data-ttu-id="fb334-142">Если в проекте используются любые другие пакеты Microsoft. тактов (например, Microsoft. тактов. numeric), выполните для них команду.</span><span class="sxs-lookup"><span data-stu-id="fb334-142">If your project uses any other Microsoft.Quantum packages (e.g. Microsoft.Quantum.Numerics), run the command for these too.</span></span>
5. <span data-ttu-id="fb334-143">Сохраните и закройте все файлы.</span><span class="sxs-lookup"><span data-stu-id="fb334-143">Save and close all files.</span></span>
6. <span data-ttu-id="fb334-144">Повторите 1-4 для каждой зависимости проекта, а затем вернитесь к папке, содержащей основной проект, и выполните команду:</span><span class="sxs-lookup"><span data-stu-id="fb334-144">Repeat 1-4 for each project dependency, then navigate back to the folder containing your main project and run:</span></span>

    ```dotnetcli
    dotnet build [project_name].csproj
    ```

<span data-ttu-id="fb334-145">После обновления проектов Q # следуйте приведенным ниже инструкциям, чтобы обновить саму КДК.</span><span class="sxs-lookup"><span data-stu-id="fb334-145">With your Q# projects now updated, follow the instructions below to update the QDK itself.</span></span>

## <a name="updating-the-qdk"></a><span data-ttu-id="fb334-146">Обновление КДК</span><span class="sxs-lookup"><span data-stu-id="fb334-146">Updating the QDK</span></span>

<span data-ttu-id="fb334-147">Процесс обновления КДК зависит от языка и среды разработки.</span><span class="sxs-lookup"><span data-stu-id="fb334-147">The process to update the QDK varies depending on your development language and environment.</span></span>
<span data-ttu-id="fb334-148">Выберите среду разработки ниже.</span><span class="sxs-lookup"><span data-stu-id="fb334-148">Select your development environment below.</span></span>

* [<span data-ttu-id="fb334-149">Python: обновление расширения IQ</span><span class="sxs-lookup"><span data-stu-id="fb334-149">Python: update the IQ# extension</span></span>](#update-iq-for-python)
* [<span data-ttu-id="fb334-150">Записные книжки Jupyter: обновление расширения IQ</span><span class="sxs-lookup"><span data-stu-id="fb334-150">Jupyter Notebooks: update the IQ# extension</span></span>](#update-iq-for-jupyter-notebooks)
* [<span data-ttu-id="fb334-151">Visual Studio: обновление расширения КДК</span><span class="sxs-lookup"><span data-stu-id="fb334-151">Visual Studio: update the QDK extension</span></span>](#update-visual-studio-qdk-extension)
* [<span data-ttu-id="fb334-152">VS Code: обновление расширения КДК</span><span class="sxs-lookup"><span data-stu-id="fb334-152">VS Code: update the QDK extension</span></span>](#update-vs-code-qdk-extension)
* [<span data-ttu-id="fb334-153">Командная строка и C#: обновление шаблонов проектов</span><span class="sxs-lookup"><span data-stu-id="fb334-153">Command-line and C#: update project templates</span></span>](#c-using-the-dotnet-command-line-tool)


### <a name="update-iq-for-python"></a><span data-ttu-id="fb334-154">Обновление IQ # для Python</span><span class="sxs-lookup"><span data-stu-id="fb334-154">Update IQ# for Python</span></span>

1. <span data-ttu-id="fb334-155">Обновление ядра `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="fb334-155">Update the `iqsharp` kernel</span></span> 

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. <span data-ttu-id="fb334-156">Проверка версии `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="fb334-156">Verify the `iqsharp` version</span></span>

    ```dotnetcli
    dotnet iqsharp --version
    ```

    <span data-ttu-id="fb334-157">Вы должны увидеть следующий результат.</span><span class="sxs-lookup"><span data-stu-id="fb334-157">You should see the following output:</span></span>

    ```bash
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    <span data-ttu-id="fb334-158">Не беспокойтесь, если ваша версия `iqsharp` более высокая, она должна соответствовать [последнему выпуску](xref:microsoft.quantum.relnotes).</span><span class="sxs-lookup"><span data-stu-id="fb334-158">Don't worry if your `iqsharp` version is higher, it should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

3. <span data-ttu-id="fb334-159">Обновление пакета `qsharp`</span><span class="sxs-lookup"><span data-stu-id="fb334-159">Update the `qsharp` package</span></span>

    ```bash
    pip install qsharp --upgrade
    ```

4. <span data-ttu-id="fb334-160">Проверка версии `qsharp`</span><span class="sxs-lookup"><span data-stu-id="fb334-160">Verify the `qsharp` version</span></span>

    ```bash
    pip show qsharp
    ```

    <span data-ttu-id="fb334-161">Вы должны увидеть следующий результат.</span><span class="sxs-lookup"><span data-stu-id="fb334-161">You should see the following output:</span></span>

    ```bash
    Name: qsharp
    Version: 0.10.1912.501
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```

5. <span data-ttu-id="fb334-162">Выполните следующую команду из расположения файлов `.qs`</span><span class="sxs-lookup"><span data-stu-id="fb334-162">Run the following command from the location of your `.qs` files</span></span>

    ```bash
    python -c "import qsharp; qsharp.reload()"
    ```

6. <span data-ttu-id="fb334-163">Теперь вы можете использовать обновленную версию КДК для запуска существующих тактовых программ.</span><span class="sxs-lookup"><span data-stu-id="fb334-163">You can now use the updated QDK version to run your existing quantum programs.</span></span>

### <a name="update-iq-for-jupyter-notebooks"></a><span data-ttu-id="fb334-164">Обновление IQ # для записных книжек Jupyter</span><span class="sxs-lookup"><span data-stu-id="fb334-164">Update IQ# for Jupyter Notebooks</span></span>

1. <span data-ttu-id="fb334-165">Обновление ядра `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="fb334-165">Update the `iqsharp` kernel</span></span>

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. <span data-ttu-id="fb334-166">Проверка версии `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="fb334-166">Verify the `iqsharp` version</span></span>

    ```dotnetcli
    dotnet iqsharp --version
    ```

    <span data-ttu-id="fb334-167">Вывод приложения должен быть аналогичен приведенному ниже:</span><span class="sxs-lookup"><span data-stu-id="fb334-167">Your output should be similar to the following:</span></span>

    ```bash
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    <span data-ttu-id="fb334-168">Не беспокойтесь, если ваша версия `iqsharp` более высокая, она должна соответствовать [последнему выпуску](xref:microsoft.quantum.relnotes).</span><span class="sxs-lookup"><span data-stu-id="fb334-168">Don't worry if your `iqsharp` version is higher, it should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

3. <span data-ttu-id="fb334-169">Выполните следующую команду в ячейке Jupyter Notebook:</span><span class="sxs-lookup"><span data-stu-id="fb334-169">Run the following command from a cell in your Jupyter Notebook:</span></span>

    ```
    %workspace reload
    ```

4. <span data-ttu-id="fb334-170">Теперь можно открыть имеющуюся записную книжку Jupyter и запустить ее с помощью обновленного КДК.</span><span class="sxs-lookup"><span data-stu-id="fb334-170">You can now open an existing Jupyter notebook and run it with the updated QDK.</span></span>

### <a name="update-visual-studio-qdk-extension"></a><span data-ttu-id="fb334-171">Обновление расширения Visual Studio КДК</span><span class="sxs-lookup"><span data-stu-id="fb334-171">Update Visual Studio QDK extension</span></span>

1. <span data-ttu-id="fb334-172">Обновление расширения Q # Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fb334-172">Update the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="fb334-173">Visual Studio предложит принять обновления для [расширения тактовой задержки Visual Studio](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span><span class="sxs-lookup"><span data-stu-id="fb334-173">Visual Studio prompts you to accept updates to the [Quantum Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="fb334-174">Принять обновление</span><span class="sxs-lookup"><span data-stu-id="fb334-174">Accept the update</span></span>

    > [!NOTE]
    > <span data-ttu-id="fb334-175">Шаблоны проектов обновляются с помощью расширения.</span><span class="sxs-lookup"><span data-stu-id="fb334-175">The project templates are updated with the extension.</span></span> <span data-ttu-id="fb334-176">Обновленные шаблоны применяются только к только что созданным проектам.</span><span class="sxs-lookup"><span data-stu-id="fb334-176">The updated templates apply to newly created projects only.</span></span> <span data-ttu-id="fb334-177">Код для существующих проектов не обновляется при обновлении расширения.</span><span class="sxs-lookup"><span data-stu-id="fb334-177">The code for your existing projects is not updated when the extension is updated.</span></span>

### <a name="update-vs-code-qdk-extension"></a><span data-ttu-id="fb334-178">Обновление расширения VS Code КДК</span><span class="sxs-lookup"><span data-stu-id="fb334-178">Update VS Code QDK extension</span></span>

1. <span data-ttu-id="fb334-179">Обновление расширения тактового VS Code</span><span class="sxs-lookup"><span data-stu-id="fb334-179">Update the Quantum VS Code extension</span></span>

    - <span data-ttu-id="fb334-180">Перезапустить VS Code</span><span class="sxs-lookup"><span data-stu-id="fb334-180">Restart VS Code</span></span>
    - <span data-ttu-id="fb334-181">Перейдите на вкладку **расширения** .</span><span class="sxs-lookup"><span data-stu-id="fb334-181">Navigate to the **Extensions** tab</span></span>
    - <span data-ttu-id="fb334-182">Выберите **Microsoft Quantum Development Kit для расширения Visual Studio Code**</span><span class="sxs-lookup"><span data-stu-id="fb334-182">Select the **Microsoft Quantum Development Kit for Visual Studio Code** extension</span></span>
    - <span data-ttu-id="fb334-183">Перезагрузить расширение</span><span class="sxs-lookup"><span data-stu-id="fb334-183">Reload the extension</span></span>

2. <span data-ttu-id="fb334-184">Обновите шаблоны проекта такта:</span><span class="sxs-lookup"><span data-stu-id="fb334-184">Update the Quantum project templates:</span></span>

   - <span data-ttu-id="fb334-185">Выберите **Представление** -> **Палитра команд**.</span><span class="sxs-lookup"><span data-stu-id="fb334-185">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="fb334-186">Выбор **Q #: Установка шаблонов проектов**</span><span class="sxs-lookup"><span data-stu-id="fb334-186">Select **Q#: Install project templates**</span></span>
   - <span data-ttu-id="fb334-187">Через несколько секунд должно появиться всплывающее окно с подтверждением успешной установки шаблонов проектов.</span><span class="sxs-lookup"><span data-stu-id="fb334-187">After a few seconds you should get a popup confirming "project templates installed successfully"</span></span>

### <a name="c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="fb334-188">C#с помощью средства командной строки `dotnet`</span><span class="sxs-lookup"><span data-stu-id="fb334-188">C#, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="fb334-189">Обновление шаблонов проектов тактов для .NET</span><span class="sxs-lookup"><span data-stu-id="fb334-189">Update the Quantum project templates for .NET</span></span>

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

## <a name="whats-next"></a><span data-ttu-id="fb334-190">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="fb334-190">What's next?</span></span>

<span data-ttu-id="fb334-191">После обновления пакета средств разработки тактов в предпочтительной среде можно продолжить разработку и запуск тактовых программ.</span><span class="sxs-lookup"><span data-stu-id="fb334-191">Now that you have updated the Quantum Development Kit in your preferred environment, you can continue to develop and run your quantum programs.</span></span> <span data-ttu-id="fb334-192">Если вы еще не написали программу, вы можете начать работу с [первой тактовой программой](xref:microsoft.quantum.write-program).</span><span class="sxs-lookup"><span data-stu-id="fb334-192">If you have not written a program yet, you can get started with [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
