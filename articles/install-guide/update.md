---
title: Сведения об обновлении Microsoft Quantum Development Kit (КДК)
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: ebf1f15d65a12c921cd3f04e4111d463d1060f8e
ms.sourcegitcommit: c93fea5980d1d46fbda1e7c7153831b9337134bf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2019
ms.locfileid: "73463282"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="f458d-102">Обновление Microsoft Quantum Development Kit (КДК)</span><span class="sxs-lookup"><span data-stu-id="f458d-102">Update the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="f458d-103">Узнайте, как обновить Microsoft Quantum Development Kit (КДК) до последней версии.</span><span class="sxs-lookup"><span data-stu-id="f458d-103">Learn how to update the Microsoft Quantum Development Kit (QDK) to the latest version.</span></span>

<span data-ttu-id="f458d-104">В этой статье предполагается, что у вас уже установлен КДК.</span><span class="sxs-lookup"><span data-stu-id="f458d-104">This article assumes that you already have the QDK installed.</span></span> <span data-ttu-id="f458d-105">Если вы устанавливаете в первый раз, обратитесь к [руководству по установке](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="f458d-105">If you are installing for the first time, then please refer to the [installation guide](xref:microsoft.quantum.install).</span></span>


## <a name="updating-q-projects"></a><span data-ttu-id="f458d-106">Обновление проектов Q #</span><span class="sxs-lookup"><span data-stu-id="f458d-106">Updating Q# Projects</span></span> 

1. <span data-ttu-id="f458d-107">Сначала установите последнюю версию [пакет SDK для .NET Core 3,0](https://dotnet.microsoft.com/download) и выполните в командной строке следующую команду:</span><span class="sxs-lookup"><span data-stu-id="f458d-107">First, install the latest version of the [.NET Core SDK 3.0](https://dotnet.microsoft.com/download) and run the following command in the command prompt:</span></span>
```bash
dotnet --version
```
 <span data-ttu-id="f458d-108">Убедитесь, что для выходных данных задано значение 3.0.100 или выше, а затем следуйте приведенным ниже инструкциям в зависимости от настроек.</span><span class="sxs-lookup"><span data-stu-id="f458d-108">Verify the output is 3.0.100 or higher, then follow the instructions below depending on your setup.</span></span>

### <a name="in-visual-studio"></a><span data-ttu-id="f458d-109">В Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f458d-109">In Visual Studio</span></span>
 
 1. <span data-ttu-id="f458d-110">Обновление до последней версии Visual Studio 2019. инструкции см. [здесь](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) .</span><span class="sxs-lookup"><span data-stu-id="f458d-110">Update to the latest version of Visual Studio 2019, see [here](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) for instructions</span></span>
 2. <span data-ttu-id="f458d-111">Открытие решения в Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f458d-111">Open your solution in Visual Studio</span></span>
 3. <span data-ttu-id="f458d-112">В меню выберите Сборка > Очистить решение.</span><span class="sxs-lookup"><span data-stu-id="f458d-112">From the menu, select Build > Clean Solution</span></span> 
 4. <span data-ttu-id="f458d-113">[Обновите целевую платформу](https://docs.microsoft.com/visualstudio/ide/visual-studio-multi-targeting-overview?view=vs-2019#change-the-target-framework) в каждом из CSPROJ-файлов до версии netcoreapp 3.0 (или netstandard 2.1, если это проект библиотеки).</span><span class="sxs-lookup"><span data-stu-id="f458d-113">[Update the target framework](https://docs.microsoft.com/visualstudio/ide/visual-studio-multi-targeting-overview?view=vs-2019#change-the-target-framework) in each of your .csproj files to netcoreapp3.0 (or netstandard2.1 if it is a library project)</span></span>
 5. <span data-ttu-id="f458d-114">Сохранение и закрытие всех файлов в решении</span><span class="sxs-lookup"><span data-stu-id="f458d-114">Save and close all files in your solution</span></span>
 6. <span data-ttu-id="f458d-115">Выберите Инструменты > командной строки > Командная строка разработчика</span><span class="sxs-lookup"><span data-stu-id="f458d-115">Select Tools > Command Line > Developer Command Prompt</span></span>
 7. <span data-ttu-id="f458d-116">Для каждого проекта в решении выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="f458d-116">For each project in the solution, run the following command:</span></span>
 ```bash
 dotnet add [project_name].csproj package Microsoft.Quantum.Development.Kit
 ```
<span data-ttu-id="f458d-117">Если в проектах используются другие пакеты Microsoft. тактов, выполните эту команду.</span><span class="sxs-lookup"><span data-stu-id="f458d-117">If your projects use any other Microsoft.Quantum packages, run the command for these too.</span></span> 
 8. <span data-ttu-id="f458d-118">Закройте командную строку и выберите Сборка > сборка решения (не *выбирайте* Перестроение решения, так как перестроение первоначально завершится сбоем).</span><span class="sxs-lookup"><span data-stu-id="f458d-118">Close the command prompt and select Build > Build Solution (do *not* select Rebuild Solution, as rebuilding will initially fail)</span></span>

### <a name="in-visual-studio-code"></a><span data-ttu-id="f458d-119">В Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="f458d-119">In Visual Studio Code</span></span>

1. <span data-ttu-id="f458d-120">В Visual Studio Code откройте папку, содержащую обновляемый проект.</span><span class="sxs-lookup"><span data-stu-id="f458d-120">In Visual Studio Code, open the folder containing the project to update</span></span>
1. <span data-ttu-id="f458d-121">Выберите терминал > новый терминал</span><span class="sxs-lookup"><span data-stu-id="f458d-121">Select Terminal > New Terminal</span></span>
1. <span data-ttu-id="f458d-122">Следуйте инструкциям по обновлению с помощью командной строки.</span><span class="sxs-lookup"><span data-stu-id="f458d-122">Follow the instructions for updating using the command line</span></span>

### <a name="using-the-command-line"></a><span data-ttu-id="f458d-123">Использование командной строки</span><span class="sxs-lookup"><span data-stu-id="f458d-123">Using the command line</span></span>

1. <span data-ttu-id="f458d-124">Перейдите к папке, содержащей файл проекта</span><span class="sxs-lookup"><span data-stu-id="f458d-124">Navigate to the folder containing your project file</span></span>
2. <span data-ttu-id="f458d-125">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="f458d-125">Run the following command:</span></span>
```bash
dotnet clean [project_name].csproj
```

3. <span data-ttu-id="f458d-126">[Обновите целевую платформу](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks) в каждом из CSPROJ-файлов до версии netcoreapp 3.0 (или netstandard 2.1, если это проект библиотеки).</span><span class="sxs-lookup"><span data-stu-id="f458d-126">[Update the target framework](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks) in each of your .csproj files to netcoreapp3.0 (or netstandard2.1 if it is a library project)</span></span>
4. <span data-ttu-id="f458d-127">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="f458d-127">Run the following command:</span></span>
```bash
dotnet add package Microsoft.Quantum.Development.Kit
```
<span data-ttu-id="f458d-128">Если в проекте используются другие пакеты Microsoft. тактов, выполните эту команду.</span><span class="sxs-lookup"><span data-stu-id="f458d-128">if your project uses any other Microsoft.Quantum packages, run the command for these too.</span></span>

5. <span data-ttu-id="f458d-129">Сохранить и закрыть все файлы</span><span class="sxs-lookup"><span data-stu-id="f458d-129">Save and close all files</span></span>
6. <span data-ttu-id="f458d-130">Повторите 1-4 для каждой зависимости проекта, а затем вернитесь к папке, содержащей основной проект, и выполните команду:</span><span class="sxs-lookup"><span data-stu-id="f458d-130">Repeat 1-4 for each project dependency, then navigate back to the folder containing your main project and run:</span></span>
```bash
dotnet build [project_name].csproj
```

## <a name="update-iq-for-python"></a><span data-ttu-id="f458d-131">Обновление IQ # для Python</span><span class="sxs-lookup"><span data-stu-id="f458d-131">Update IQ# for Python</span></span>

1. <span data-ttu-id="f458d-132">Обновление ядра `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="f458d-132">Update the `iqsharp` kernel</span></span>

    ```bash
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="f458d-133">Проверка версии `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="f458d-133">Verify the `iqsharp` version</span></span>

    ```bash
    dotnet iqsharp --version
    ```

    <span data-ttu-id="f458d-134">Вы должны увидеть следующий результат.</span><span class="sxs-lookup"><span data-stu-id="f458d-134">You should see the following output:</span></span>

    ```bash
    iqsharp: 0.10.1911.307
    Jupyter Core: 1.2.20112.0
    ```

1. <span data-ttu-id="f458d-135">Обновление пакета `qsharp`</span><span class="sxs-lookup"><span data-stu-id="f458d-135">Update the `qsharp` package</span></span>

    ```bash
    pip install qsharp --upgrade
    ```

1. <span data-ttu-id="f458d-136">Проверка версии `qsharp`</span><span class="sxs-lookup"><span data-stu-id="f458d-136">Verify the `qsharp` version</span></span>

    ```bash
    pip show qsharp
    ```

    <span data-ttu-id="f458d-137">Вы должны увидеть следующий результат.</span><span class="sxs-lookup"><span data-stu-id="f458d-137">You should see the following output:</span></span>

    ```bash
    Name: qsharp
    Version: 0.10.1911.307
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```
1. <span data-ttu-id="f458d-138">Выполните следующую команду из расположения файлов `.qs`</span><span class="sxs-lookup"><span data-stu-id="f458d-138">Run the following command from the location of your `.qs` files</span></span>
    ```bash
    python -c "import qsharp; qsharp.reload()"
    ```

1. <span data-ttu-id="f458d-139">Теперь вы можете использовать обновленную версию КДК для запуска существующих тактовых программ.</span><span class="sxs-lookup"><span data-stu-id="f458d-139">You can now use the updated QDK version to run your existing quantum programs.</span></span>

## <a name="update-iq-for-jupyter-notebooks"></a><span data-ttu-id="f458d-140">Обновление IQ # для записных книжек Jupyter</span><span class="sxs-lookup"><span data-stu-id="f458d-140">Update IQ# for Jupyter notebooks</span></span>

1. <span data-ttu-id="f458d-141">Обновление ядра `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="f458d-141">Update the `iqsharp` kernel</span></span>

    ```bash
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="f458d-142">Проверка версии `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="f458d-142">Verify the `iqsharp` version</span></span>

    ```bash
    dotnet iqsharp --version
    ```

    <span data-ttu-id="f458d-143">Вы должны увидеть следующий результат.</span><span class="sxs-lookup"><span data-stu-id="f458d-143">You should see the following output:</span></span>

    ```bash
    iqsharp: 0.10.1911.307
    Jupyter Core: 1.2.20112.0
    ```
1. <span data-ttu-id="f458d-144">Выполните следующую команду в ячейке Jupyter Notebook:</span><span class="sxs-lookup"><span data-stu-id="f458d-144">Run the following command from a cell in your Jupyter Notebook:</span></span>
    ```
    %workspace reload
    ```

1. <span data-ttu-id="f458d-145">Теперь можно открыть имеющуюся записную книжку Jupyter и запустить ее с помощью обновленного КДК.</span><span class="sxs-lookup"><span data-stu-id="f458d-145">You can now open an existing Jupyter notebook and run it with the updated QDK.</span></span>

## <a name="update-visual-studio-qdk-extension"></a><span data-ttu-id="f458d-146">Обновление расширения Visual Studio КДК</span><span class="sxs-lookup"><span data-stu-id="f458d-146">Update Visual Studio QDK extension</span></span>

1. <span data-ttu-id="f458d-147">Обновление расширения Q # Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f458d-147">Update the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="f458d-148">Visual Studio предложит принять обновления для [расширения тактовой задержки Visual Studio](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span><span class="sxs-lookup"><span data-stu-id="f458d-148">Visual Studio prompts you to accept updates to the [Quantum Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="f458d-149">Принять обновление</span><span class="sxs-lookup"><span data-stu-id="f458d-149">Accept the update</span></span>

    > [!NOTE]
    > <span data-ttu-id="f458d-150">Шаблоны проектов обновляются с помощью расширения.</span><span class="sxs-lookup"><span data-stu-id="f458d-150">The project templates are updated with the extension.</span></span> <span data-ttu-id="f458d-151">Обновленные шаблоны применяются только к только что созданным проектам.</span><span class="sxs-lookup"><span data-stu-id="f458d-151">The updated templates apply to newly created projects only.</span></span> <span data-ttu-id="f458d-152">Код для существующих проектов не обновляется при обновлении расширения.</span><span class="sxs-lookup"><span data-stu-id="f458d-152">The code for your existing projects is not updated when the extension is updated.</span></span>

## <a name="update-vs-code-qdk-extension"></a><span data-ttu-id="f458d-153">Обновление расширения VS Code КДК</span><span class="sxs-lookup"><span data-stu-id="f458d-153">Update VS Code QDK extension</span></span>

1. <span data-ttu-id="f458d-154">Обновление расширения тактового VS Code</span><span class="sxs-lookup"><span data-stu-id="f458d-154">Update the Quantum VS Code extension</span></span>

    - <span data-ttu-id="f458d-155">Перезапустить VS Code</span><span class="sxs-lookup"><span data-stu-id="f458d-155">Restart VS Code</span></span>
    - <span data-ttu-id="f458d-156">Перейдите на вкладку **расширения** .</span><span class="sxs-lookup"><span data-stu-id="f458d-156">Navigate to the **Extensions** tab</span></span>
    - <span data-ttu-id="f458d-157">Выберите **Microsoft Quantum Development Kit для расширения Visual Studio Code**</span><span class="sxs-lookup"><span data-stu-id="f458d-157">Select the **Microsoft Quantum Development Kit for Visual Studio Code** extension</span></span>
    - <span data-ttu-id="f458d-158">Перезагрузить расширение</span><span class="sxs-lookup"><span data-stu-id="f458d-158">Reload the extension</span></span>

1. <span data-ttu-id="f458d-159">Обновите шаблоны проекта такта:</span><span class="sxs-lookup"><span data-stu-id="f458d-159">Update the Quantum project templates:</span></span>

   - <span data-ttu-id="f458d-160">Выберите **Представление** -> **Палитра команд**.</span><span class="sxs-lookup"><span data-stu-id="f458d-160">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="f458d-161">Выбор **Q #: Установка шаблонов проектов**</span><span class="sxs-lookup"><span data-stu-id="f458d-161">Select **Q#: Install project templates**</span></span>

## <a name="c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="f458d-162">C#с помощью средства командной строки `dotnet`</span><span class="sxs-lookup"><span data-stu-id="f458d-162">C#, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="f458d-163">Обновление шаблонов проектов тактов для .NET</span><span class="sxs-lookup"><span data-stu-id="f458d-163">Update the Quantum project templates for .NET</span></span>

    ```bash
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

## <a name="whats-next"></a><span data-ttu-id="f458d-164">Что дальше?</span><span class="sxs-lookup"><span data-stu-id="f458d-164">What's next?</span></span>

<span data-ttu-id="f458d-165">После обновления пакета средств разработки тактов в предпочтительной среде можно продолжить разработку и запуск тактовых программ.</span><span class="sxs-lookup"><span data-stu-id="f458d-165">Now that you have updated the Quantum Development Kit in your preferred environment, you can continue to develop and run your quantum programs.</span></span> <span data-ttu-id="f458d-166">Если вы еще не написали программу, вы можете начать работу с [первой тактовой программой](xref:microsoft.quantum.write-program).</span><span class="sxs-lookup"><span data-stu-id="f458d-166">If you have not written a program yet, you can get started with [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
