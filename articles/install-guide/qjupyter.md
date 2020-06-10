---
title: Разработка на Q# + Jupyter Notebook
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: b80d95a160b5f46c1132d3428ba32ad6dcd5656e
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630334"
---
# <a name="develop-with-q-jupyter-notebooks"></a><span data-ttu-id="61f83-102">Разработка на Q# + Jupyter Notebook</span><span class="sxs-lookup"><span data-stu-id="61f83-102">Develop with Q# Jupyter Notebooks</span></span>

<span data-ttu-id="61f83-103">Установите КДК для разработки операций Q # для записных книжек Q # Jupyter.</span><span class="sxs-lookup"><span data-stu-id="61f83-103">Install the QDK for developing Q# operations on Q# Jupyter Notebooks.</span></span>

<span data-ttu-id="61f83-104">Записные книжки Jupyter разрешают выполнение кода на месте наряду с инструкциями, примечаниями и другим содержимым.</span><span class="sxs-lookup"><span data-stu-id="61f83-104">Jupyter Notebooks allow in-place code execution alongside instructions, notes, and other content.</span></span> <span data-ttu-id="61f83-105">Эта среда идеально подходит для написания кода Q # с внедренными объяснениями или интерактивными учебниками по тактовым вычислениям.</span><span class="sxs-lookup"><span data-stu-id="61f83-105">This environment is ideal for writing Q# code with embedded explanations or quantum computing interactive tutorials.</span></span> <span data-ttu-id="61f83-106">Ниже описаны действия, которые помогут вам приступить к созданию собственных записных книжек Q#.</span><span class="sxs-lookup"><span data-stu-id="61f83-106">Here's what you need to do to start creating your own Q# notebooks.</span></span>

<span data-ttu-id="61f83-107">IQ# — это расширение, которое в основном используется в Jupyter и Python с пакетом SDK для .NET Core и предоставляет основные функции для компиляции и моделирования операций Q#.</span><span class="sxs-lookup"><span data-stu-id="61f83-107">IQ# (pronounced i-q-sharp) is an extension primarily used by Jupyter and Python to the .NET Core SDK that provides the core functionality for compiling and simulating Q# operations.</span></span>

> [!NOTE]
> * <span data-ttu-id="61f83-108">В записных книжках Q # Jupyter можно запустить только Q # Code, и операции нельзя вызывать из внешних программных узлов (например, файлов Python или C#).</span><span class="sxs-lookup"><span data-stu-id="61f83-108">In Q# Jupyter Notebooks you can only run Q# code, and the operations cannot be called from external host programs (e.g. Python or C# files).</span></span> <span data-ttu-id="61f83-109">Эта среда не подходит, если ваша цель заключается в том, чтобы объединить внешнюю программу классического узла с тактовой программой.</span><span class="sxs-lookup"><span data-stu-id="61f83-109">This environment is not appropriate if your goal is to combine an external classical host program with the quantum program.</span></span>

1. <span data-ttu-id="61f83-110">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="61f83-110">Prerequisites</span></span>

    - <span data-ttu-id="61f83-111">[Python](https://www.python.org/downloads/) 3,6 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="61f83-111">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - [<span data-ttu-id="61f83-112">Jupyter Notebook</span><span class="sxs-lookup"><span data-stu-id="61f83-112">Jupyter Notebook</span></span>](https://jupyter.readthedocs.io/en/latest/install.html)
    - [<span data-ttu-id="61f83-113">Пакет SDK для .NET Core 3,1</span><span class="sxs-lookup"><span data-stu-id="61f83-113">.NET Core SDK 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)

1. <span data-ttu-id="61f83-114">Установите пакет `iqsharp`.</span><span class="sxs-lookup"><span data-stu-id="61f83-114">Install the `iqsharp` package</span></span>

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > <span data-ttu-id="61f83-115">Если на шаге появляется сообщение об ошибке `dotnet iqsharp install` , откройте новое окно терминала и повторите попытку.</span><span class="sxs-lookup"><span data-stu-id="61f83-115">If you get an error during the `dotnet iqsharp install` step, open a new terminal window and try again.</span></span>
    > <span data-ttu-id="61f83-116">Если это не поможет, попробуйте найти установленное `dotnet-iqsharp` средство (в Windows `dotnet-iqsharp.exe` ) и запустить:</span><span class="sxs-lookup"><span data-stu-id="61f83-116">If this still doesn't work, try locating the installed `dotnet-iqsharp` tool (on Windows, `dotnet-iqsharp.exe`) and running:</span></span>
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > <span data-ttu-id="61f83-117">где `/path/to/dotnet-iqsharp` следует заменить абсолютным путем к `dotnet-iqsharp` средству в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="61f83-117">where `/path/to/dotnet-iqsharp` should be replaced by the absolute path to the `dotnet-iqsharp` tool in your file system.</span></span>
    > <span data-ttu-id="61f83-118">Обычно это будет находиться `.dotnet/tools` в папке профиля пользователя.</span><span class="sxs-lookup"><span data-stu-id="61f83-118">Typically this will be under `.dotnet/tools` in your user profile folder.</span></span>

1. <span data-ttu-id="61f83-119">Проверьте установку, создав приложение `Hello World`.</span><span class="sxs-lookup"><span data-stu-id="61f83-119">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="61f83-120">Выполните следующую команду, чтобы запустить сервер записных книжек.</span><span class="sxs-lookup"><span data-stu-id="61f83-120">Run the following command to start the notebook server:</span></span>

        ```
        jupyter notebook
        ```

    - <span data-ttu-id="61f83-121">Чтобы открыть Jupyter Notebook, скопируйте и вставьте URL-адрес, предоставленный командной строкой, в браузер.</span><span class="sxs-lookup"><span data-stu-id="61f83-121">To open the Jupyter Notebook, copy and paste the URL provided by the command line into your browser.</span></span>

    - <span data-ttu-id="61f83-122">Создайте Jupyter Notebook с ядром Q # и добавьте следующий код в первую ячейку записной книжки:</span><span class="sxs-lookup"><span data-stu-id="61f83-122">Create a Jupyter Notebook with a Q# kernel, and add the following code to the first notebook cell:</span></span>

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - <span data-ttu-id="61f83-123">Запустите эту ячейку записной книжки.</span><span class="sxs-lookup"><span data-stu-id="61f83-123">Run this cell of the notebook:</span></span>

        ![Jupyter Notebook ячейку с кодом Q #](~/media/install-guide-jupyter.png)

        <span data-ttu-id="61f83-125">В выходных данных ячейки должно отобразиться `SayHello`.</span><span class="sxs-lookup"><span data-stu-id="61f83-125">You should see `SayHello` in the output of the cell.</span></span> <span data-ttu-id="61f83-126">При выполнении в Jupyter Notebook компилируется код Q #, а Записная книжка выводит имя найденных операций.</span><span class="sxs-lookup"><span data-stu-id="61f83-126">When running in Jupyter Notebook, the Q# code is compiled, and the notebook outputs the name of the operation(s) that it finds.</span></span>


    - <span data-ttu-id="61f83-127">В новой ячейке выполните только что созданную операцию (в симуляторе) с помощью `%simulate` команды:</span><span class="sxs-lookup"><span data-stu-id="61f83-127">In a new cell, execute the operation you just created (in a simulator) by using the `%simulate` command:</span></span>

        ![Jupyter Notebook ячейка с% имитировать волшебное магическое](~/media/install-guide-jupyter-simulate.png)

        <span data-ttu-id="61f83-129">Сообщение должно отобразиться на экране вместе с результатом вызванной операции (здесь мы видим пустой кортеж, `()` так как наша операция просто возвращает `Unit` тип).</span><span class="sxs-lookup"><span data-stu-id="61f83-129">You should see the message printed on the screen along with the result of the operation you invoked (here, we see the empty tuple `()` because our operation simply returns a `Unit` type).</span></span>

## <a name="next-steps"></a><span data-ttu-id="61f83-130">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="61f83-130">Next steps</span></span>

<span data-ttu-id="61f83-131">Теперь, когда вы установили КДК для записных книжек "Q # Jupyter", вы можете написать и запустить [первую тактовую программу](xref:microsoft.quantum.quickstarts.qrng) , написав код Q # непосредственно в среде Jupyter Notebook.</span><span class="sxs-lookup"><span data-stu-id="61f83-131">Now that you have installed the QDK for Q# Jupyter Notebooks, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng) by writing your Q# code directly within the Jupyter Notebook environment.</span></span>

<span data-ttu-id="61f83-132">Дополнительные примеры того, что можно делать с записными книжками Q # Jupyter, см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="61f83-132">For more examples of what you can do with Q# Jupyter Notebooks, please take a look at:</span></span>
- <span data-ttu-id="61f83-133">[Введение в вопросы и ответы # и Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/).</span><span class="sxs-lookup"><span data-stu-id="61f83-133">[Intro to Q# and Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/).</span></span> <span data-ttu-id="61f83-134">Здесь вы найдете вопрос # Jupyter Notebook, в котором показано, как использовать Q # в этой среде.</span><span class="sxs-lookup"><span data-stu-id="61f83-134">There you will find a Q# Jupyter Notebook that shows how to use Q# in this environment.</span></span>
- <span data-ttu-id="61f83-135">[Тактовый Катас](xref:microsoft.quantum.overview.katas), коллекция руководств для самостоятельного обучения и наборы программных упражнений в виде Q # Jupyter Notebooks.</span><span class="sxs-lookup"><span data-stu-id="61f83-135">[Quantum Katas](xref:microsoft.quantum.overview.katas), an open-source collection of self-paced tutorials and sets of programming exercises in the form of Q# Jupyter Notebooks.</span></span> <span data-ttu-id="61f83-136">Хорошим отправной точкой являются [записные книжки](https://github.com/microsoft/QuantumKatas#tutorial-topics) , посвященные созданию Катас тактов.</span><span class="sxs-lookup"><span data-stu-id="61f83-136">The [Quantum Katas tutorial notebooks](https://github.com/microsoft/QuantumKatas#tutorial-topics) are a good starting point.</span></span> <span data-ttu-id="61f83-137">Тактовая Катас предназначена для обучения элементам тактовых вычислений и программированию Q # в одно и то же время.</span><span class="sxs-lookup"><span data-stu-id="61f83-137">The Quantum Katas are aimed at teaching you elements of quantum computing and Q# programming at the same time.</span></span> <span data-ttu-id="61f83-138">Это отличный пример того, какой тип содержимого можно создать с помощью записных книжек Q # Jupyter.</span><span class="sxs-lookup"><span data-stu-id="61f83-138">They're an excellent example of what kind of content you can create with Q# Jupyter Notebooks.</span></span>
