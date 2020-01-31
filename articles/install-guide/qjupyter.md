---
title: 'Разработка с помощью Q # Jupyter Notebooks'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: b7276f9b273f601f30e4938018398353b6a9102d
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "76831075"
---
# <a name="develop-with-q-jupyter-notebooks"></a><span data-ttu-id="2a6fc-102">Разработка с помощью Q # Jupyter Notebooks</span><span class="sxs-lookup"><span data-stu-id="2a6fc-102">Develop with Q# Jupyter notebooks</span></span>

<span data-ttu-id="2a6fc-103">Установите КДК для разработки операций Q # для записных книжек Q # Jupyter.</span><span class="sxs-lookup"><span data-stu-id="2a6fc-103">Install the QDK for developing Q# operations on Q# Jupyter Notebooks.</span></span>

<span data-ttu-id="2a6fc-104">Записные книжки Jupyter разрешают выполнение кода на месте наряду с инструкциями, примечаниями и другим содержимым.</span><span class="sxs-lookup"><span data-stu-id="2a6fc-104">Jupyter Notebooks allow in-place code execution alongside instructions, notes, and other content.</span></span> <span data-ttu-id="2a6fc-105">Эта среда идеально подходит для написания кода Q # с внедренными объяснениями или интерактивными учебниками по тактовым вычислениям.</span><span class="sxs-lookup"><span data-stu-id="2a6fc-105">This environment is ideal for writing Q# code with embedded explanations or quantum computing interactive tutorials.</span></span> <span data-ttu-id="2a6fc-106">Ниже описаны действия, которые помогут вам приступить к созданию собственных записных книжек Q#.</span><span class="sxs-lookup"><span data-stu-id="2a6fc-106">Here's what you need to do to start creating your own Q# notebooks.</span></span>

<span data-ttu-id="2a6fc-107">IQ# — это расширение, которое в основном используется в Jupyter и Python с пакетом SDK для .NET Core и предоставляет основные функции для компиляции и моделирования операций Q#.</span><span class="sxs-lookup"><span data-stu-id="2a6fc-107">IQ# (pronounced i-q-sharp) is an extension primarily used by Jupyter and Python to the .NET Core SDK that provides the core functionality for compiling and simulating Q# operations.</span></span>

> [!NOTE]
> * <span data-ttu-id="2a6fc-108">В записных книжках Q # Jupyter можно запустить только Q # Code, а операции нельзя вызывать из внешних программных узлов (например, Python C# или файлов).</span><span class="sxs-lookup"><span data-stu-id="2a6fc-108">In Q# Jupyter Notebooks you can only run Q# code, and the operations cannot be called from external host programs (e.g. Python or C# files).</span></span> <span data-ttu-id="2a6fc-109">Эта среда не подходит, если ваша цель заключается в том, чтобы объединить внешнюю программу классического узла с тактовой программой.</span><span class="sxs-lookup"><span data-stu-id="2a6fc-109">This environment is not appropriate if your goal is to combine an external classical host program with the quantum program.</span></span>

1. <span data-ttu-id="2a6fc-110">Технические условия</span><span class="sxs-lookup"><span data-stu-id="2a6fc-110">Pre-requisites</span></span>

    - <span data-ttu-id="2a6fc-111">[Python](https://www.python.org/downloads/) 3.6 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="2a6fc-111">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - [<span data-ttu-id="2a6fc-112">Записная книжка Jupyter</span><span class="sxs-lookup"><span data-stu-id="2a6fc-112">Jupyter Notebook</span></span>](https://jupyter.readthedocs.io/en/latest/install.html)
    - [<span data-ttu-id="2a6fc-113">Пакет SDK для .NET Core 3,1 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="2a6fc-113">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="2a6fc-114">Установите пакет `iqsharp`.</span><span class="sxs-lookup"><span data-stu-id="2a6fc-114">Install the `iqsharp` package</span></span>

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="2a6fc-115">Проверьте установку, создав приложение `Hello World`.</span><span class="sxs-lookup"><span data-stu-id="2a6fc-115">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="2a6fc-116">Выполните следующую команду, чтобы запустить сервер записных книжек.</span><span class="sxs-lookup"><span data-stu-id="2a6fc-116">Run the following command to start the notebook server:</span></span>

        ```bash
        jupyter notebook
        ```

    - <span data-ttu-id="2a6fc-117">Чтобы открыть записную книжку Jupyter, скопируйте и вставьте в браузер URL-адрес, предоставленный командной строкой.</span><span class="sxs-lookup"><span data-stu-id="2a6fc-117">To open the Jupyter notebook copy and paste the URL provided by the command line into your browser.</span></span>

    - <span data-ttu-id="2a6fc-118">Создайте записную книжку Jupyter с ядром Q# и добавьте следующий код в первую ячейку записной книжки.</span><span class="sxs-lookup"><span data-stu-id="2a6fc-118">Create a Jupyter notebook with a Q# kernel, and add the following code to the first notebook cell:</span></span>

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - <span data-ttu-id="2a6fc-119">Запустите эту ячейку записной книжки.</span><span class="sxs-lookup"><span data-stu-id="2a6fc-119">Run this cell of the notebook:</span></span>

        ![Ячейка записной книжки Jupyter с кодом Q#](~/media/install-guide-jupyter.png)

        <span data-ttu-id="2a6fc-121">В выходных данных ячейки должно отобразиться `SayHello`.</span><span class="sxs-lookup"><span data-stu-id="2a6fc-121">You should see `SayHello` in the output of the cell.</span></span> <span data-ttu-id="2a6fc-122">При запуске в записных книжках Jupyter компилируется код Q#, а записная книжка выводит имя найденных операций.</span><span class="sxs-lookup"><span data-stu-id="2a6fc-122">When running in jupyter notebooks, the Q# code is compiled, and the notebook outputs the name of the operation(s) that it finds.</span></span>


    - <span data-ttu-id="2a6fc-123">В новой ячейке выполните только что созданную операцию (в симуляторе) с помощью команды `%simulate`.</span><span class="sxs-lookup"><span data-stu-id="2a6fc-123">In a new cell, execute the operation you just created (in a simulator) by using the `%simulate` command:</span></span>

        ![Ячейка записной книжки Jupyter с магической командой %simulate](~/media/install-guide-jupyter-simulate.png)

        <span data-ttu-id="2a6fc-125">Сообщение должно отобразиться на экране вместе с результатом вызванной операции (здесь отображается пустой кортеж `()` так как наша операция просто возвращает тип `Unit`).</span><span class="sxs-lookup"><span data-stu-id="2a6fc-125">You should see the message printed on the screen along with the result of the operation you invoked (here, we see the empty tuple `()` because our operation simply returns a `Unit` type).</span></span>

## <a name="whats-next"></a><span data-ttu-id="2a6fc-126">Что дальше?</span><span class="sxs-lookup"><span data-stu-id="2a6fc-126">What's next?</span></span>

<span data-ttu-id="2a6fc-127">После установки Quantum Development Kit в предпочитаемой среде вы можете написать и запустить [первую квантовую программу](xref:microsoft.quantum.write-program).</span><span class="sxs-lookup"><span data-stu-id="2a6fc-127">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
