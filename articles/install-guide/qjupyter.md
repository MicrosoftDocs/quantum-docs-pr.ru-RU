---
title: Разработка на Q# + Jupyter Notebook
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: 9117794d6cf6f05fa34e05c21fad8977d0e76505
ms.sourcegitcommit: c8ebc5d7d8581444754f5d7bfaca2f25601f1b14
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2020
ms.locfileid: "84577826"
---
# <a name="develop-with-q-jupyter-notebooks"></a><span data-ttu-id="ee98e-102">Разработка на Q# + Jupyter Notebook</span><span class="sxs-lookup"><span data-stu-id="ee98e-102">Develop with Q# Jupyter Notebooks</span></span>

<span data-ttu-id="ee98e-103">Установите КДК для разработки операций Q # для записных книжек Q # Jupyter.</span><span class="sxs-lookup"><span data-stu-id="ee98e-103">Install the QDK for developing Q# operations on Q# Jupyter Notebooks.</span></span>

<span data-ttu-id="ee98e-104">Записные книжки Jupyter разрешают выполнение кода на месте наряду с инструкциями, примечаниями и другим содержимым.</span><span class="sxs-lookup"><span data-stu-id="ee98e-104">Jupyter Notebooks allow in-place code execution alongside instructions, notes, and other content.</span></span> <span data-ttu-id="ee98e-105">Эта среда идеально подходит для написания кода Q # с внедренными объяснениями или интерактивными учебниками по тактовым вычислениям.</span><span class="sxs-lookup"><span data-stu-id="ee98e-105">This environment is ideal for writing Q# code with embedded explanations or quantum computing interactive tutorials.</span></span> <span data-ttu-id="ee98e-106">Ниже описаны действия, которые помогут вам приступить к созданию собственных записных книжек Q#.</span><span class="sxs-lookup"><span data-stu-id="ee98e-106">Here's what you need to do to start creating your own Q# notebooks.</span></span>

<span data-ttu-id="ee98e-107">IQ# — это расширение, которое в основном используется в Jupyter и Python с пакетом SDK для .NET Core и предоставляет основные функции для компиляции и моделирования операций Q#.</span><span class="sxs-lookup"><span data-stu-id="ee98e-107">IQ# (pronounced i-q-sharp) is an extension primarily used by Jupyter and Python to the .NET Core SDK that provides the core functionality for compiling and simulating Q# operations.</span></span>

> [!NOTE]
> * <span data-ttu-id="ee98e-108">В записных книжках Q # Jupyter можно запустить только Q # Code, и операции нельзя вызывать из внешних программных узлов (например, файлов Python или C#).</span><span class="sxs-lookup"><span data-stu-id="ee98e-108">In Q# Jupyter Notebooks you can only run Q# code, and the operations cannot be called from external host programs (e.g. Python or C# files).</span></span> <span data-ttu-id="ee98e-109">Эта среда не подходит, если ваша цель заключается в том, чтобы объединить внешнюю программу классического узла с тактовой программой.</span><span class="sxs-lookup"><span data-stu-id="ee98e-109">This environment is not appropriate if your goal is to combine an external classical host program with the quantum program.</span></span>

1. <span data-ttu-id="ee98e-110">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="ee98e-110">Pre-requisites</span></span>

    - <span data-ttu-id="ee98e-111">[Python](https://www.python.org/downloads/) 3,6 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="ee98e-111">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - [<span data-ttu-id="ee98e-112">Jupyter Notebook</span><span class="sxs-lookup"><span data-stu-id="ee98e-112">Jupyter Notebook</span></span>](https://jupyter.readthedocs.io/en/latest/install.html)
    - [<span data-ttu-id="ee98e-113">Пакет SDK для .NET Core 3,1</span><span class="sxs-lookup"><span data-stu-id="ee98e-113">.NET Core SDK 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)

1. <span data-ttu-id="ee98e-114">Установите пакет `iqsharp`.</span><span class="sxs-lookup"><span data-stu-id="ee98e-114">Install the `iqsharp` package</span></span>

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="ee98e-115">Проверьте установку, создав приложение `Hello World`.</span><span class="sxs-lookup"><span data-stu-id="ee98e-115">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="ee98e-116">Выполните следующую команду, чтобы запустить сервер записных книжек.</span><span class="sxs-lookup"><span data-stu-id="ee98e-116">Run the following command to start the notebook server:</span></span>

        ```
        jupyter notebook
        ```

    - <span data-ttu-id="ee98e-117">Чтобы открыть Jupyter Notebook, скопируйте и вставьте URL-адрес, предоставленный командной строкой, в браузер.</span><span class="sxs-lookup"><span data-stu-id="ee98e-117">To open the Jupyter Notebook, copy and paste the URL provided by the command line into your browser.</span></span>

    - <span data-ttu-id="ee98e-118">Создайте Jupyter Notebook с ядром Q # и добавьте следующий код в первую ячейку записной книжки:</span><span class="sxs-lookup"><span data-stu-id="ee98e-118">Create a Jupyter Notebook with a Q# kernel, and add the following code to the first notebook cell:</span></span>

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - <span data-ttu-id="ee98e-119">Запустите эту ячейку записной книжки.</span><span class="sxs-lookup"><span data-stu-id="ee98e-119">Run this cell of the notebook:</span></span>

        ![Jupyter Notebook ячейку с кодом Q #](~/media/install-guide-jupyter.png)

        <span data-ttu-id="ee98e-121">В выходных данных ячейки должно отобразиться `SayHello`.</span><span class="sxs-lookup"><span data-stu-id="ee98e-121">You should see `SayHello` in the output of the cell.</span></span> <span data-ttu-id="ee98e-122">При выполнении в Jupyter Notebook компилируется код Q #, а Записная книжка выводит имя найденных операций.</span><span class="sxs-lookup"><span data-stu-id="ee98e-122">When running in Jupyter Notebook, the Q# code is compiled, and the notebook outputs the name of the operation(s) that it finds.</span></span>


    - <span data-ttu-id="ee98e-123">В новой ячейке выполните только что созданную операцию (в симуляторе) с помощью `%simulate` команды:</span><span class="sxs-lookup"><span data-stu-id="ee98e-123">In a new cell, execute the operation you just created (in a simulator) by using the `%simulate` command:</span></span>

        ![Jupyter Notebook ячейка с% имитировать волшебное магическое](~/media/install-guide-jupyter-simulate.png)

        <span data-ttu-id="ee98e-125">Сообщение должно отобразиться на экране вместе с результатом вызванной операции (здесь мы видим пустой кортеж, `()` так как наша операция просто возвращает `Unit` тип).</span><span class="sxs-lookup"><span data-stu-id="ee98e-125">You should see the message printed on the screen along with the result of the operation you invoked (here, we see the empty tuple `()` because our operation simply returns a `Unit` type).</span></span>

## <a name="next-steps"></a><span data-ttu-id="ee98e-126">Дальнейшие шаги</span><span class="sxs-lookup"><span data-stu-id="ee98e-126">Next steps</span></span>

<span data-ttu-id="ee98e-127">Теперь, когда вы установили КДК для записных книжек "Q # Jupyter", вы можете написать и запустить [первую тактовую программу](xref:microsoft.quantum.quickstarts.qrng) , написав код Q # непосредственно в среде Jupyter Notebook.</span><span class="sxs-lookup"><span data-stu-id="ee98e-127">Now that you have installed the QDK for Q# Jupyter Notebooks, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng) by writing your Q# code directly within the Jupyter Notebook environment.</span></span>

<span data-ttu-id="ee98e-128">Дополнительные примеры того, что можно делать с записными книжками Q # Jupyter, см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="ee98e-128">For more examples of what you can do with Q# Jupyter Notebooks, please take a look at:</span></span>
- <span data-ttu-id="ee98e-129">[Введение в вопросы и ответы # и Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/).</span><span class="sxs-lookup"><span data-stu-id="ee98e-129">[Intro to Q# and Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/).</span></span> <span data-ttu-id="ee98e-130">Здесь вы найдете вопрос # Jupyter Notebook, в котором показано, как использовать Q # в этой среде.</span><span class="sxs-lookup"><span data-stu-id="ee98e-130">There you will find a Q# Jupyter Notebook that shows how to use Q# in this environment.</span></span>
- <span data-ttu-id="ee98e-131">[Тактовый Катас](xref:microsoft.quantum.overview.katas), коллекция руководств для самостоятельного обучения и наборы программных упражнений в виде Q # Jupyter Notebooks.</span><span class="sxs-lookup"><span data-stu-id="ee98e-131">[Quantum Katas](xref:microsoft.quantum.overview.katas), an open-source collection of self-paced tutorials and sets of programming exercises in the form of Q# Jupyter Notebooks.</span></span> <span data-ttu-id="ee98e-132">Хорошим отправной точкой являются [записные книжки](https://github.com/microsoft/QuantumKatas#tutorial-topics) , посвященные созданию Катас тактов.</span><span class="sxs-lookup"><span data-stu-id="ee98e-132">The [Quantum Katas tutorial notebooks](https://github.com/microsoft/QuantumKatas#tutorial-topics) are a good starting point.</span></span> <span data-ttu-id="ee98e-133">Тактовая Катас предназначена для обучения элементам тактовых вычислений и программированию Q # в одно и то же время.</span><span class="sxs-lookup"><span data-stu-id="ee98e-133">The Quantum Katas are aimed at teaching you elements of quantum computing and Q# programming at the same time.</span></span> <span data-ttu-id="ee98e-134">Это отличный пример того, какой тип содержимого можно создать с помощью записных книжек Q # Jupyter.</span><span class="sxs-lookup"><span data-stu-id="ee98e-134">They're an excellent example of what kind of content you can create with Q# Jupyter Notebooks.</span></span>
