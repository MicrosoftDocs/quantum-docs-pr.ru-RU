---
title: Разработка с использованием записных книжек Jupyter Notebook с Q#
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: 5c613d29c03525d29893307684f13ccd32d4d4eb
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274161"
---
# <a name="develop-with-q-jupyter-notebooks"></a><span data-ttu-id="cf137-102">Разработка с использованием записных книжек Jupyter Notebook с Q#</span><span class="sxs-lookup"><span data-stu-id="cf137-102">Develop with Q# Jupyter Notebooks</span></span>

<span data-ttu-id="cf137-103">Установите QDK для разработки операций Q# для записных книжек Jupyter Notebook с Q#.</span><span class="sxs-lookup"><span data-stu-id="cf137-103">Install the QDK for developing Q# operations on Q# Jupyter Notebooks.</span></span>

<span data-ttu-id="cf137-104">Записные книжки Jupyter Notebook разрешают выполнение кода на месте наряду с инструкциями, примечаниями и другим содержимым.</span><span class="sxs-lookup"><span data-stu-id="cf137-104">Jupyter Notebooks allow in-place code execution alongside instructions, notes, and other content.</span></span> <span data-ttu-id="cf137-105">Эта среда идеально подходит для написания кода Q# со встроенными объяснениями или интерактивными учебниками по квантовым вычислениям.</span><span class="sxs-lookup"><span data-stu-id="cf137-105">This environment is ideal for writing Q# code with embedded explanations or quantum computing interactive tutorials.</span></span> <span data-ttu-id="cf137-106">Ниже описаны действия, которые помогут вам приступить к созданию собственных записных книжек Q#.</span><span class="sxs-lookup"><span data-stu-id="cf137-106">Here's what you need to do to start creating your own Q# notebooks.</span></span>

<span data-ttu-id="cf137-107">IQ# — это расширение, которое в основном используется в Jupyter и Python с пакетом SDK для .NET Core и предоставляет основные функции для компиляции и моделирования операций Q#.</span><span class="sxs-lookup"><span data-stu-id="cf137-107">IQ# (pronounced i-q-sharp) is an extension primarily used by Jupyter and Python to the .NET Core SDK that provides the core functionality for compiling and simulating Q# operations.</span></span>

> [!NOTE]
> * <span data-ttu-id="cf137-108">Записные книжки Jupyter Notebook позволяют только выполнять код Q#. Вызывать операции Q# из внешних основных программ (например, файлов Python или C#) невозможно.</span><span class="sxs-lookup"><span data-stu-id="cf137-108">In Q# Jupyter Notebooks you can only run Q# code, and the operations cannot be called from external host programs (e.g. Python or C# files).</span></span> <span data-ttu-id="cf137-109">Эта среда не подходит, если вы намерены использовать классическую внешнюю основную программу в сочетании с квантовой программой.</span><span class="sxs-lookup"><span data-stu-id="cf137-109">This environment is not appropriate if your goal is to combine an external classical host program with the quantum program.</span></span>

1. <span data-ttu-id="cf137-110">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="cf137-110">Prerequisites</span></span>

    - <span data-ttu-id="cf137-111">[Python](https://www.python.org/downloads/) 3.6 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="cf137-111">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - [<span data-ttu-id="cf137-112">Записная книжка Jupyter</span><span class="sxs-lookup"><span data-stu-id="cf137-112">Jupyter Notebook</span></span>](https://jupyter.readthedocs.io/en/latest/install.html)
    - [<span data-ttu-id="cf137-113">Пакет SDK для .NET Core 3.1</span><span class="sxs-lookup"><span data-stu-id="cf137-113">.NET Core SDK 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)

1. <span data-ttu-id="cf137-114">Установите пакет `iqsharp`.</span><span class="sxs-lookup"><span data-stu-id="cf137-114">Install the `iqsharp` package</span></span>

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > <span data-ttu-id="cf137-115">Если на шаге `dotnet iqsharp install` появляется сообщение об ошибке, откройте новое окно терминала и повторите попытку.</span><span class="sxs-lookup"><span data-stu-id="cf137-115">If you get an error during the `dotnet iqsharp install` step, open a new terminal window and try again.</span></span>
    > <span data-ttu-id="cf137-116">Если это не поможет, попробуйте найти установленное средство `dotnet-iqsharp` (в Windows это `dotnet-iqsharp.exe`) и воспользуйтесь следующей командой:</span><span class="sxs-lookup"><span data-stu-id="cf137-116">If this still doesn't work, try locating the installed `dotnet-iqsharp` tool (on Windows, `dotnet-iqsharp.exe`) and running:</span></span>
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > <span data-ttu-id="cf137-117">где `/path/to/dotnet-iqsharp` следует заменить абсолютным путем к средству `dotnet-iqsharp` в вашей файловой системе.</span><span class="sxs-lookup"><span data-stu-id="cf137-117">where `/path/to/dotnet-iqsharp` should be replaced by the absolute path to the `dotnet-iqsharp` tool in your file system.</span></span>
    > <span data-ttu-id="cf137-118">Обычно оно находится в `.dotnet/tools` в папке профиля пользователя.</span><span class="sxs-lookup"><span data-stu-id="cf137-118">Typically this will be under `.dotnet/tools` in your user profile folder.</span></span>

1. <span data-ttu-id="cf137-119">Проверьте установку, создав приложение `Hello World`.</span><span class="sxs-lookup"><span data-stu-id="cf137-119">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="cf137-120">Выполните следующую команду, чтобы запустить сервер записных книжек.</span><span class="sxs-lookup"><span data-stu-id="cf137-120">Run the following command to start the notebook server:</span></span>

        ```
        jupyter notebook
        ```

    - <span data-ttu-id="cf137-121">Чтобы открыть Jupyter Notebook, скопируйте URL-адрес из командной строки и вставьте его в браузер.</span><span class="sxs-lookup"><span data-stu-id="cf137-121">To open the Jupyter Notebook, copy and paste the URL provided by the command line into your browser.</span></span>

    - <span data-ttu-id="cf137-122">Создайте записную книжку Jupyter Notebook с ядром Q# и добавьте следующий код в ее первую ячейку.</span><span class="sxs-lookup"><span data-stu-id="cf137-122">Create a Jupyter Notebook with a Q# kernel, and add the following code to the first notebook cell:</span></span>

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - <span data-ttu-id="cf137-123">Запустите эту ячейку записной книжки.</span><span class="sxs-lookup"><span data-stu-id="cf137-123">Run this cell of the notebook:</span></span>

        ![Ячейка Jupyter Notebook с кодом Q#](~/media/install-guide-jupyter.png)

        <span data-ttu-id="cf137-125">В выходных данных ячейки должно отобразиться `SayHello`.</span><span class="sxs-lookup"><span data-stu-id="cf137-125">You should see `SayHello` in the output of the cell.</span></span> <span data-ttu-id="cf137-126">При запуске в Jupyter Notebook компилируется код Q#, а записная книжка выводит имя найденных операций.</span><span class="sxs-lookup"><span data-stu-id="cf137-126">When running in Jupyter Notebook, the Q# code is compiled, and the notebook outputs the name of the operation(s) that it finds.</span></span>


    - <span data-ttu-id="cf137-127">В новой ячейке выполните только что созданную (в симуляторе) операцию с помощью команды `%simulate`.</span><span class="sxs-lookup"><span data-stu-id="cf137-127">In a new cell, execute the operation you just created (in a simulator) by using the `%simulate` command:</span></span>

        ![Ячейка Jupyter Notebook с магической командой %simulate](~/media/install-guide-jupyter-simulate.png)

        <span data-ttu-id="cf137-129">Сообщение должно отобразиться на экране вместе с результатом вызванной операции (в данном случае получен пустой кортеж `()`, поскольку операция просто возвращает тип `Unit`).</span><span class="sxs-lookup"><span data-stu-id="cf137-129">You should see the message printed on the screen along with the result of the operation you invoked (here, we see the empty tuple `()` because our operation simply returns a `Unit` type).</span></span>

## <a name="next-steps"></a><span data-ttu-id="cf137-130">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="cf137-130">Next steps</span></span>

<span data-ttu-id="cf137-131">Теперь, когда вы установили QDK для записных книжек Jupyter Notebook c Q#, вы можете написать и запустить [свою первую квантовую программу](xref:microsoft.quantum.quickstarts.qrng), создав код Q# непосредственно в среде Jupyter Notebook.</span><span class="sxs-lookup"><span data-stu-id="cf137-131">Now that you have installed the QDK for Q# Jupyter Notebooks, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng) by writing your Q# code directly within the Jupyter Notebook environment.</span></span>

<span data-ttu-id="cf137-132">Воспользуйтесь приведенными ниже ресурсами, чтобы ознакомиться с другими примерами использования записных книжек Jupyter Notebook с Q#.</span><span class="sxs-lookup"><span data-stu-id="cf137-132">For more examples of what you can do with Q# Jupyter Notebooks, please take a look at:</span></span>
- <span data-ttu-id="cf137-133">[Введение в Q# и Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/).</span><span class="sxs-lookup"><span data-stu-id="cf137-133">[Intro to Q# and Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/).</span></span> <span data-ttu-id="cf137-134">Здесь вы найдете записную книжку Jupyter Notebook с Q#, в которой демонстрируется использование Q# в этой среде.</span><span class="sxs-lookup"><span data-stu-id="cf137-134">There you will find a Q# Jupyter Notebook that shows how to use Q# in this environment.</span></span>
- <span data-ttu-id="cf137-135">[Quantum Katas](xref:microsoft.quantum.overview.katas) — коллекция учебников с открытым кодом для обучения в произвольном темпе и наборы упражнений по программированию в виде записных книжек Jupyter Notebook с Q#.</span><span class="sxs-lookup"><span data-stu-id="cf137-135">[Quantum Katas](xref:microsoft.quantum.overview.katas), an open-source collection of self-paced tutorials and sets of programming exercises in the form of Q# Jupyter Notebooks.</span></span> <span data-ttu-id="cf137-136">[Записные книжки из учебников Quantum Katas](https://github.com/microsoft/QuantumKatas#tutorial-topics) послужат хорошей отправной точкой.</span><span class="sxs-lookup"><span data-stu-id="cf137-136">The [Quantum Katas tutorial notebooks](https://github.com/microsoft/QuantumKatas#tutorial-topics) are a good starting point.</span></span> <span data-ttu-id="cf137-137">Коллекция Quantum Katas предназначена для обучения квантовым вычислениям с одновременным изучением программирования на Q# в произвольном темпе.</span><span class="sxs-lookup"><span data-stu-id="cf137-137">The Quantum Katas are aimed at teaching you elements of quantum computing and Q# programming at the same time.</span></span> <span data-ttu-id="cf137-138">Это отличный пример того, какого рода содержимое можно создать с помощью записных книжек Jupyter Notebook с Q#.</span><span class="sxs-lookup"><span data-stu-id="cf137-138">They're an excellent example of what kind of content you can create with Q# Jupyter Notebooks.</span></span>
