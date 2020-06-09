---
title: Обновление пакета средств разработки такта (КДК)
description: 'Описывает, как обновить проекты Q # и Microsoft Quantum Development Kit до текущей версии.'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: 89db1a671767b0cc083a251918bbeeed2b39b883
ms.sourcegitcommit: c8ebc5d7d8581444754f5d7bfaca2f25601f1b14
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2020
ms.locfileid: "84578187"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="b3856-103">Обновление Microsoft Quantum Development Kit (КДК)</span><span class="sxs-lookup"><span data-stu-id="b3856-103">Update the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="b3856-104">Узнайте, как обновить Microsoft Quantum Development Kit (КДК) до последней версии.</span><span class="sxs-lookup"><span data-stu-id="b3856-104">Learn how to update the Microsoft Quantum Development Kit (QDK) to the latest version.</span></span>

<span data-ttu-id="b3856-105">В этой статье предполагается, что у вас уже установлен КДК.</span><span class="sxs-lookup"><span data-stu-id="b3856-105">This article assumes that you already have the QDK installed.</span></span> <span data-ttu-id="b3856-106">Если вы устанавливаете в первый раз, обратитесь к [руководству по установке](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="b3856-106">If you are installing for the first time, then please refer to the [installation guide](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="b3856-107">Мы рекомендуем поддерживать последние версии КДК в актуальном состоянии.</span><span class="sxs-lookup"><span data-stu-id="b3856-107">We recommend keeping up to date with the latest QDK release.</span></span> <span data-ttu-id="b3856-108">Следуйте этому руководству по обновлению, чтобы выполнить обновление до последней версии КДК.</span><span class="sxs-lookup"><span data-stu-id="b3856-108">Follow this update guide to upgrade to the most recent QDK version.</span></span> <span data-ttu-id="b3856-109">Процесс состоит из двух частей:</span><span class="sxs-lookup"><span data-stu-id="b3856-109">The process consists of two parts:</span></span>
1. <span data-ttu-id="b3856-110">Обновление существующих файлов Q # и проектов для согласования кода с любым обновленным синтаксисом.</span><span class="sxs-lookup"><span data-stu-id="b3856-110">Updating your existing Q# files and projects to align your code with any updated syntax.</span></span>
2. <span data-ttu-id="b3856-111">Обновление самого КДК для выбранной среды разработки.</span><span class="sxs-lookup"><span data-stu-id="b3856-111">Updating the QDK itself for your chosen development environment.</span></span>

## <a name="updating-q-projects"></a><span data-ttu-id="b3856-112">Обновление проектов Q #</span><span class="sxs-lookup"><span data-stu-id="b3856-112">Updating Q# Projects</span></span> 

<span data-ttu-id="b3856-113">Независимо от того, используете ли вы C# или Python для размещения операций Q #, следуйте этим инструкциям, чтобы обновить проекты Q #.</span><span class="sxs-lookup"><span data-stu-id="b3856-113">Regardless of whether you are using C# or Python to host Q# operations, follow these instructions to update your Q# projects.</span></span>

1. <span data-ttu-id="b3856-114">Сначала убедитесь, что у вас установлена последняя версия [пакет SDK для .NET Core 3,1](https://dotnet.microsoft.com/download).</span><span class="sxs-lookup"><span data-stu-id="b3856-114">First, check that you have the latest version of the [.NET Core SDK 3.1](https://dotnet.microsoft.com/download).</span></span> <span data-ttu-id="b3856-115">В командной строке выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="b3856-115">Run the following command in the command prompt:</span></span>

    ```dotnetcli
    dotnet --version
    ```

    <span data-ttu-id="b3856-116">Убедитесь, что выходные данные имеют значение `3.1.100` или выше.</span><span class="sxs-lookup"><span data-stu-id="b3856-116">Verify the output is `3.1.100` or higher.</span></span> <span data-ttu-id="b3856-117">В противном случае установите [последнюю версию](https://dotnet.microsoft.com/download) и снова проверьте.</span><span class="sxs-lookup"><span data-stu-id="b3856-117">If not, install the [latest version](https://dotnet.microsoft.com/download) and check again.</span></span> <span data-ttu-id="b3856-118">Затем следуйте приведенным ниже инструкциям в зависимости от настроек (Visual Studio, Visual Studio Code или непосредственно в командной строке).</span><span class="sxs-lookup"><span data-stu-id="b3856-118">Then follow the instructions below depending on your setup (Visual Studio, Visual Studio Code, or directly the command line).</span></span>

### <a name="update-q-projects-in-visual-studio"></a><span data-ttu-id="b3856-119">Обновление проектов Q # в Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b3856-119">Update Q# projects in Visual Studio</span></span>
 
1. <span data-ttu-id="b3856-120">Обновление до последней версии Visual Studio 2019. инструкции см. [здесь](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) .</span><span class="sxs-lookup"><span data-stu-id="b3856-120">Update to the latest version of Visual Studio 2019, see [here](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) for instructions.</span></span>
2. <span data-ttu-id="b3856-121">Откройте решение в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b3856-121">Open your solution in Visual Studio.</span></span>
3. <span data-ttu-id="b3856-122">В меню выберите **Сборка**  ->  **Очистить решение**.</span><span class="sxs-lookup"><span data-stu-id="b3856-122">From the menu, select **Build** -> **Clean Solution**.</span></span>
4. <span data-ttu-id="b3856-123">В каждом из CSPROJ-файлов обновите целевую платформу до `netcoreapp3.1` (или, `netstandard2.1` если это проект библиотеки).</span><span class="sxs-lookup"><span data-stu-id="b3856-123">In each of your .csproj files, update the target framework to `netcoreapp3.1` (or `netstandard2.1` if it is a library project).</span></span>
    <span data-ttu-id="b3856-124">То есть измените строки формы:</span><span class="sxs-lookup"><span data-stu-id="b3856-124">That is, edit lines of the form:</span></span>

    ```xml
    <TargetFramework>netcoreapp3.1</TargetFramework>
    ```

    <span data-ttu-id="b3856-125">Дополнительные сведения об указании целевых платформ можно найти [здесь](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span><span class="sxs-lookup"><span data-stu-id="b3856-125">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>

5. <span data-ttu-id="b3856-126">В каждом из файлов CSPROJ задайте для пакета SDK значение `Microsoft.Quantum.Sdk` , как указано в строке ниже.</span><span class="sxs-lookup"><span data-stu-id="b3856-126">In each of the .csproj files, set the SDK to `Microsoft.Quantum.Sdk`, as indicated in the line below.</span></span> <span data-ttu-id="b3856-127">Обратите внимание, что номер версии должен быть последним доступным, и его можно определить, просмотрев [заметки о выпуске](https://docs.microsoft.com/quantum/relnotes/).</span><span class="sxs-lookup"><span data-stu-id="b3856-127">Please notice that the version number should be the latest available, and you can determine it by reviewing the [release notes](https://docs.microsoft.com/quantum/relnotes/).</span></span>

    ```xml
    <Project Sdk="Microsoft.Quantum.Sdk/0.11.2006.207">
    ```

6. <span data-ttu-id="b3856-128">Сохраните и закройте все файлы в решении.</span><span class="sxs-lookup"><span data-stu-id="b3856-128">Save and close all files in your solution.</span></span>

7. <span data-ttu-id="b3856-129">Выберите **инструменты**  ->  **Командная строка**  ->  **Командная строка разработчика**.</span><span class="sxs-lookup"><span data-stu-id="b3856-129">Select **Tools** -> **Command Line** -> **Developer Command Prompt**.</span></span> <span data-ttu-id="b3856-130">Кроме того, можно использовать консоль управления пакетами в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b3856-130">Alternatively, you can use the package management console in Visual Studio.</span></span>

8. <span data-ttu-id="b3856-131">Для каждого проекта в решении выполните следующую команду, чтобы **Удалить** этот пакет:</span><span class="sxs-lookup"><span data-stu-id="b3856-131">For each project in the solution, run the following command to **remove** this package:</span></span>

    ```dotnetcli
    dotnet remove [project_name].csproj package Microsoft.Quantum.Development.Kit
    ```

   <span data-ttu-id="b3856-132">Если в проектах используются любые пакеты Microsoft. тактов или Microsoft. Azure. тактов (например, Microsoft. тактов. numeric), выполните команду **Add** , чтобы обновить используемую версию.</span><span class="sxs-lookup"><span data-stu-id="b3856-132">If your projects use any other Microsoft.Quantum or Microsoft.Azure.Quantum packages (e.g. Microsoft.Quantum.Numerics), run the **add** command for these to update the version used.</span></span>

    ```dotnetcli
    dotnet add [project_name].csproj package [package_name]
    ```

9. <span data-ttu-id="b3856-133">Закройте командную строку и выберите **Сборка**сборка  ->  **решения** (не *not* выбирайте Перестроение решения).</span><span class="sxs-lookup"><span data-stu-id="b3856-133">Close the command prompt and select **Build** -> **Build Solution** (do *not* select Rebuild Solution).</span></span>

<span data-ttu-id="b3856-134">Теперь вы можете перейти к [обновлению расширения Visual Studio КДК](#update-visual-studio-qdk-extension).</span><span class="sxs-lookup"><span data-stu-id="b3856-134">You can now skip ahead to [update your Visual Studio QDK extension](#update-visual-studio-qdk-extension).</span></span>


### <a name="update-q-projects-in-visual-studio-code"></a><span data-ttu-id="b3856-135">Обновление проектов Q # в Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="b3856-135">Update Q# projects in Visual Studio Code</span></span>

1. <span data-ttu-id="b3856-136">В Visual Studio Code откройте папку, содержащую обновляемый проект.</span><span class="sxs-lookup"><span data-stu-id="b3856-136">In Visual Studio Code, open the folder containing the project to update.</span></span>
2. <span data-ttu-id="b3856-137">Выберите **терминал**  ->  **Новый терминал**.</span><span class="sxs-lookup"><span data-stu-id="b3856-137">Select **Terminal** -> **New Terminal**.</span></span>
3. <span data-ttu-id="b3856-138">Следуйте инструкциям по обновлению с помощью командной строки (непосредственно ниже).</span><span class="sxs-lookup"><span data-stu-id="b3856-138">Follow the instructions for updating using the command line (directly below).</span></span>

### <a name="update-q-projects-using-the-command-line"></a><span data-ttu-id="b3856-139">Обновление проектов Q # с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="b3856-139">Update Q# projects using the command line</span></span>

1. <span data-ttu-id="b3856-140">Перейдите к папке, содержащей основной файл проекта.</span><span class="sxs-lookup"><span data-stu-id="b3856-140">Navigate to the folder containing your main project file.</span></span>

2. <span data-ttu-id="b3856-141">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="b3856-141">Run the following command:</span></span>

    ```dotnetcli
    dotnet clean [project_name].csproj
    ```

3. <span data-ttu-id="b3856-142">Определите текущую версию КДК.</span><span class="sxs-lookup"><span data-stu-id="b3856-142">Determine the current version of the QDK.</span></span> <span data-ttu-id="b3856-143">Чтобы найти его, ознакомьтесь с [заметками о выпуске](https://docs.microsoft.com/quantum/relnotes/).</span><span class="sxs-lookup"><span data-stu-id="b3856-143">To find it, you can review the [release notes](https://docs.microsoft.com/quantum/relnotes/).</span></span> <span data-ttu-id="b3856-144">Версия будет иметь формат, аналогичный `0.11.2006.207` .</span><span class="sxs-lookup"><span data-stu-id="b3856-144">The version will be in a format similar to `0.11.2006.207`.</span></span>

4. <span data-ttu-id="b3856-145">В каждом из `.csproj` файлов выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b3856-145">In each of your `.csproj` files, go through the following steps:</span></span>

    - <span data-ttu-id="b3856-146">Обновите целевую платформу до `netcoreapp3.1` (или, `netstandard2.1` если это проект библиотеки).</span><span class="sxs-lookup"><span data-stu-id="b3856-146">Update the target framework to `netcoreapp3.1` (or `netstandard2.1` if it is a library project).</span></span> <span data-ttu-id="b3856-147">То есть измените строки формы:</span><span class="sxs-lookup"><span data-stu-id="b3856-147">That is, edit lines of the form:</span></span>

        ```xml
        <TargetFramework>netcoreapp3.1</TargetFramework>
        ```

        <span data-ttu-id="b3856-148">Дополнительные сведения об указании целевых платформ можно найти [здесь](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span><span class="sxs-lookup"><span data-stu-id="b3856-148">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>

    - <span data-ttu-id="b3856-149">Замените ссылку на пакет SDK в определении проекта.</span><span class="sxs-lookup"><span data-stu-id="b3856-149">Replace the reference to the SDK in the project definition.</span></span> <span data-ttu-id="b3856-150">Убедитесь, что номер версии соответствует значению, определенному на **шаге 3**.</span><span class="sxs-lookup"><span data-stu-id="b3856-150">Make sure that the version number corresponds to the value determined in **step 3**.</span></span>

        ```xml
        <Project Sdk="Microsoft.Quantum.Sdk/0.11.2006.207">
        ```

    - <span data-ttu-id="b3856-151">Удалите ссылку на пакет `Microsoft.Quantum.Development.Kit` , если он есть, который будет указан в следующей записи:</span><span class="sxs-lookup"><span data-stu-id="b3856-151">Remove the reference to package `Microsoft.Quantum.Development.Kit` if present, which will be specified in the following entry:</span></span>

        ```xml
        <PackageReference Include="Microsoft.Quantum.Development.Kit" Version="0.10.1910.3107" />
        ```

    - <span data-ttu-id="b3856-152">Обновите версию всех пакетов Microsoft тактов до последней выпущенной версии КДК (определяется на **шаге 3**).</span><span class="sxs-lookup"><span data-stu-id="b3856-152">Update the version of the all the Microsoft Quantum packages to the most recently released version of the QDK (determined in **step 3**).</span></span> <span data-ttu-id="b3856-153">Эти пакеты именуются со следующими шаблонами:</span><span class="sxs-lookup"><span data-stu-id="b3856-153">Those packages are named with the following patterns:</span></span>

        ```
        Microsoft.Quantum.*
        Microsoft.Azure.Quantum.*
        ```
    
        <span data-ttu-id="b3856-154">Ссылки на пакеты имеют следующий формат:</span><span class="sxs-lookup"><span data-stu-id="b3856-154">References to packages have the following format:</span></span>

        ```xml
        <PackageReference Include="Microsoft.Quantum.Compiler" Version="0.11.2006.207" />
        ```

    - <span data-ttu-id="b3856-155">Сохраните обновленный файл.</span><span class="sxs-lookup"><span data-stu-id="b3856-155">Save the updated file.</span></span>

    - <span data-ttu-id="b3856-156">Восстановите зависимости проекта, выполнив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b3856-156">Restore the dependencies of the project, by doing the following:</span></span>

        ```dotnetcli
        dotnet restore [project_name].csproj
        ```

4. <span data-ttu-id="b3856-157">Вернитесь к папке, содержащей основной проект, и выполните команду:</span><span class="sxs-lookup"><span data-stu-id="b3856-157">Navigate back to the folder containing your main project and run:</span></span>

    ```dotnetcli
    dotnet build [project_name].csproj
    ```

<span data-ttu-id="b3856-158">После обновления проектов Q # следуйте приведенным ниже инструкциям, чтобы обновить саму КДК.</span><span class="sxs-lookup"><span data-stu-id="b3856-158">With your Q# projects now updated, follow the instructions below to update the QDK itself.</span></span>

## <a name="updating-the-qdk"></a><span data-ttu-id="b3856-159">Обновление КДК</span><span class="sxs-lookup"><span data-stu-id="b3856-159">Updating the QDK</span></span>

<span data-ttu-id="b3856-160">Процесс обновления КДК зависит от языка и среды разработки.</span><span class="sxs-lookup"><span data-stu-id="b3856-160">The process to update the QDK varies depending on your development language and environment.</span></span>
<span data-ttu-id="b3856-161">Выберите среду разработки ниже.</span><span class="sxs-lookup"><span data-stu-id="b3856-161">Select your development environment below.</span></span>

* [<span data-ttu-id="b3856-162">Python: обновление расширения IQ</span><span class="sxs-lookup"><span data-stu-id="b3856-162">Python: update the IQ# extension</span></span>](#update-iq-for-python)
* [<span data-ttu-id="b3856-163">Записные книжки Jupyter: обновление расширения IQ</span><span class="sxs-lookup"><span data-stu-id="b3856-163">Jupyter Notebooks: update the IQ# extension</span></span>](#update-iq-for-jupyter-notebooks)
* [<span data-ttu-id="b3856-164">Visual Studio: обновление расширения КДК</span><span class="sxs-lookup"><span data-stu-id="b3856-164">Visual Studio: update the QDK extension</span></span>](#update-visual-studio-qdk-extension)
* [<span data-ttu-id="b3856-165">VS Code: обновление расширения КДК</span><span class="sxs-lookup"><span data-stu-id="b3856-165">VS Code: update the QDK extension</span></span>](#update-vs-code-qdk-extension)
* [<span data-ttu-id="b3856-166">Командная строка и C#: обновление шаблонов проектов</span><span class="sxs-lookup"><span data-stu-id="b3856-166">Command-line and C#: update project templates</span></span>](#c-using-the-dotnet-command-line-tool)


### <a name="update-iq-for-python"></a><span data-ttu-id="b3856-167">Обновление IQ # для Python</span><span class="sxs-lookup"><span data-stu-id="b3856-167">Update IQ# for Python</span></span>

1. <span data-ttu-id="b3856-168">Обновление `iqsharp` ядра</span><span class="sxs-lookup"><span data-stu-id="b3856-168">Update the `iqsharp` kernel</span></span> 

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. <span data-ttu-id="b3856-169">Проверка `iqsharp` версии</span><span class="sxs-lookup"><span data-stu-id="b3856-169">Verify the `iqsharp` version</span></span>

    ```dotnetcli
    dotnet iqsharp --version
    ```

    <span data-ttu-id="b3856-170">Вы должны увидеть следующий результат.</span><span class="sxs-lookup"><span data-stu-id="b3856-170">You should see the following output:</span></span>

    ```
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    <span data-ttu-id="b3856-171">Не беспокойтесь, если ваша `iqsharp` версия более высокая, она должна соответствовать [последнему выпуску](xref:microsoft.quantum.relnotes).</span><span class="sxs-lookup"><span data-stu-id="b3856-171">Don't worry if your `iqsharp` version is higher, it should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

3. <span data-ttu-id="b3856-172">Обновление `qsharp` пакета</span><span class="sxs-lookup"><span data-stu-id="b3856-172">Update the `qsharp` package</span></span>

    ```
    pip install qsharp --upgrade
    ```

4. <span data-ttu-id="b3856-173">Проверка `qsharp` версии</span><span class="sxs-lookup"><span data-stu-id="b3856-173">Verify the `qsharp` version</span></span>

    ```
    pip show qsharp
    ```

    <span data-ttu-id="b3856-174">Вы должны увидеть следующий результат.</span><span class="sxs-lookup"><span data-stu-id="b3856-174">You should see the following output:</span></span>

    ```
    Name: qsharp
    Version: 0.10.1912.501
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```

5. <span data-ttu-id="b3856-175">Выполните следующую команду из расположения `.qs` файлов</span><span class="sxs-lookup"><span data-stu-id="b3856-175">Run the following command from the location of your `.qs` files</span></span>

    ```
    python -c "import qsharp; qsharp.reload()"
    ```

6. <span data-ttu-id="b3856-176">Теперь вы можете использовать обновленную версию КДК для запуска существующих тактовых программ.</span><span class="sxs-lookup"><span data-stu-id="b3856-176">You can now use the updated QDK version to run your existing quantum programs.</span></span>

### <a name="update-iq-for-jupyter-notebooks"></a><span data-ttu-id="b3856-177">Обновление IQ # для записных книжек Jupyter</span><span class="sxs-lookup"><span data-stu-id="b3856-177">Update IQ# for Jupyter Notebooks</span></span>

1. <span data-ttu-id="b3856-178">Обновление `iqsharp` ядра</span><span class="sxs-lookup"><span data-stu-id="b3856-178">Update the `iqsharp` kernel</span></span>

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. <span data-ttu-id="b3856-179">Проверка `iqsharp` версии</span><span class="sxs-lookup"><span data-stu-id="b3856-179">Verify the `iqsharp` version</span></span>

    ```dotnetcli
    dotnet iqsharp --version
    ```

    <span data-ttu-id="b3856-180">Вывод приложения должен быть аналогичен приведенному ниже:</span><span class="sxs-lookup"><span data-stu-id="b3856-180">Your output should be similar to the following:</span></span>

    ```
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    <span data-ttu-id="b3856-181">Не беспокойтесь, если ваша `iqsharp` версия более высокая, она должна соответствовать [последнему выпуску](xref:microsoft.quantum.relnotes).</span><span class="sxs-lookup"><span data-stu-id="b3856-181">Don't worry if your `iqsharp` version is higher, it should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

3. <span data-ttu-id="b3856-182">Выполните следующую команду в ячейке Jupyter Notebook:</span><span class="sxs-lookup"><span data-stu-id="b3856-182">Run the following command from a cell in your Jupyter Notebook:</span></span>

    ```
    %workspace reload
    ```

4. <span data-ttu-id="b3856-183">Теперь можно открыть имеющуюся записную книжку Jupyter и запустить ее с помощью обновленного КДК.</span><span class="sxs-lookup"><span data-stu-id="b3856-183">You can now open an existing Jupyter notebook and run it with the updated QDK.</span></span>

### <a name="update-visual-studio-qdk-extension"></a><span data-ttu-id="b3856-184">Обновление расширения Visual Studio КДК</span><span class="sxs-lookup"><span data-stu-id="b3856-184">Update Visual Studio QDK extension</span></span>

1. <span data-ttu-id="b3856-185">Обновление расширения Q # Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b3856-185">Update the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="b3856-186">Visual Studio предложит принять обновления для [расширения тактовой задержки Visual Studio](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span><span class="sxs-lookup"><span data-stu-id="b3856-186">Visual Studio prompts you to accept updates to the [Quantum Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="b3856-187">Принять обновление</span><span class="sxs-lookup"><span data-stu-id="b3856-187">Accept the update</span></span>

    > [!NOTE]
    > <span data-ttu-id="b3856-188">Шаблоны проектов обновляются с помощью расширения.</span><span class="sxs-lookup"><span data-stu-id="b3856-188">The project templates are updated with the extension.</span></span> <span data-ttu-id="b3856-189">Обновленные шаблоны применяются только к только что созданным проектам.</span><span class="sxs-lookup"><span data-stu-id="b3856-189">The updated templates apply to newly created projects only.</span></span> <span data-ttu-id="b3856-190">Код для существующих проектов не обновляется при обновлении расширения.</span><span class="sxs-lookup"><span data-stu-id="b3856-190">The code for your existing projects is not updated when the extension is updated.</span></span>

### <a name="update-vs-code-qdk-extension"></a><span data-ttu-id="b3856-191">Обновление расширения VS Code КДК</span><span class="sxs-lookup"><span data-stu-id="b3856-191">Update VS Code QDK extension</span></span>

1. <span data-ttu-id="b3856-192">Обновление расширения тактового VS Code</span><span class="sxs-lookup"><span data-stu-id="b3856-192">Update the Quantum VS Code extension</span></span>

    - <span data-ttu-id="b3856-193">Перезапустить VS Code</span><span class="sxs-lookup"><span data-stu-id="b3856-193">Restart VS Code</span></span>
    - <span data-ttu-id="b3856-194">Перейдите на вкладку **расширения** .</span><span class="sxs-lookup"><span data-stu-id="b3856-194">Navigate to the **Extensions** tab</span></span>
    - <span data-ttu-id="b3856-195">Выберите **Microsoft Quantum Development Kit для расширения Visual Studio Code**</span><span class="sxs-lookup"><span data-stu-id="b3856-195">Select the **Microsoft Quantum Development Kit for Visual Studio Code** extension</span></span>
    - <span data-ttu-id="b3856-196">Перезагрузить расширение</span><span class="sxs-lookup"><span data-stu-id="b3856-196">Reload the extension</span></span>

2. <span data-ttu-id="b3856-197">Обновите шаблоны проекта такта:</span><span class="sxs-lookup"><span data-stu-id="b3856-197">Update the Quantum project templates:</span></span>

   - <span data-ttu-id="b3856-198">Перейти к **View**  ->  **палитре команд** просмотра</span><span class="sxs-lookup"><span data-stu-id="b3856-198">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="b3856-199">Выбор **Q #: Установка шаблонов проектов**</span><span class="sxs-lookup"><span data-stu-id="b3856-199">Select **Q#: Install project templates**</span></span>
   - <span data-ttu-id="b3856-200">Через несколько секунд должно появиться всплывающее окно с подтверждением успешной установки шаблонов проектов.</span><span class="sxs-lookup"><span data-stu-id="b3856-200">After a few seconds you should get a popup confirming "project templates installed successfully"</span></span>

### <a name="c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="b3856-201">C# с помощью `dotnet` программы командной строки</span><span class="sxs-lookup"><span data-stu-id="b3856-201">C#, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="b3856-202">Обновление шаблонов проектов тактов для .NET</span><span class="sxs-lookup"><span data-stu-id="b3856-202">Update the Quantum project templates for .NET</span></span>

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```
