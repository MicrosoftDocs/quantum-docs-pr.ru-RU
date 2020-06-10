---
title: 'Разработка с помощью Q # и Python'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.python
ms.openlocfilehash: 1ae208e7047cb040fb44945a59c3cc6508a09723
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630283"
---
# <a name="develop-with-q-and-python"></a><span data-ttu-id="a73dd-102">Разработка с помощью Q # и Python</span><span class="sxs-lookup"><span data-stu-id="a73dd-102">Develop with Q# and Python</span></span>

<span data-ttu-id="a73dd-103">Установите КДК, чтобы разрабатывать ведущие программы Python для вызова операций Q #.</span><span class="sxs-lookup"><span data-stu-id="a73dd-103">Install the QDK to develop Python host programs to call Q# operations.</span></span>

1. <span data-ttu-id="a73dd-104">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="a73dd-104">Prerequisites</span></span>

    - <span data-ttu-id="a73dd-105">[Python](https://www.python.org/downloads/) 3,6 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="a73dd-105">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - <span data-ttu-id="a73dd-106">Диспетчер пакетов Python [PIP](https://pip.pypa.io/en/stable/installing)</span><span class="sxs-lookup"><span data-stu-id="a73dd-106">The [PIP](https://pip.pypa.io/en/stable/installing) Python package manager</span></span>
    - [<span data-ttu-id="a73dd-107">Пакет SDK для .NET Core 3,1</span><span class="sxs-lookup"><span data-stu-id="a73dd-107">.NET Core SDK 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)


1. <span data-ttu-id="a73dd-108">Установите `qsharp` пакет, пакет Python, который обеспечивает взаимодействие между Q # и Python.</span><span class="sxs-lookup"><span data-stu-id="a73dd-108">Install the `qsharp` package, a Python package that enables interop between Q# and Python.</span></span>

    ```
    pip install qsharp
    ```

1. <span data-ttu-id="a73dd-109">Установите IQ #, ядро, используемое Jupyter и Python, которое предоставляет основные функциональные возможности для компиляции и выполнения операций Q #.</span><span class="sxs-lookup"><span data-stu-id="a73dd-109">Install IQ#, a kernel used by Jupyter and Python that provides the core functionality for compiling and executing Q# operations.</span></span>

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > <span data-ttu-id="a73dd-110">Если на шаге появляется сообщение об ошибке `dotnet iqsharp install` , откройте новое окно терминала и повторите попытку.</span><span class="sxs-lookup"><span data-stu-id="a73dd-110">If you get an error during the `dotnet iqsharp install` step, open a new terminal window and try again.</span></span>
    > <span data-ttu-id="a73dd-111">Если это не поможет, попробуйте найти установленное `dotnet-iqsharp` средство (в Windows `dotnet-iqsharp.exe` ) и запустить:</span><span class="sxs-lookup"><span data-stu-id="a73dd-111">If this still doesn't work, try locating the installed `dotnet-iqsharp` tool (on Windows, `dotnet-iqsharp.exe`) and running:</span></span>
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > <span data-ttu-id="a73dd-112">где `/path/to/dotnet-iqsharp` следует заменить абсолютным путем к `dotnet-iqsharp` средству в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="a73dd-112">where `/path/to/dotnet-iqsharp` should be replaced by the absolute path to the `dotnet-iqsharp` tool in your file system.</span></span>
    > <span data-ttu-id="a73dd-113">Обычно это будет находиться `.dotnet/tools` в папке профиля пользователя.</span><span class="sxs-lookup"><span data-stu-id="a73dd-113">Typically this will be under `.dotnet/tools` in your user profile folder.</span></span>
  
1. <span data-ttu-id="a73dd-114">Хотя Q # и Python можно использовать в любой интегрированной среде разработки, мы настоятельно рекомендуем использовать интегрированную среду разработки Visual Studio Code (VS Code) для приложений на основе Q # + Python.</span><span class="sxs-lookup"><span data-stu-id="a73dd-114">While you can use Q# with Python in any IDE, we highly recommend using Visual Studio Code (VS Code) IDE for your Q# + Python applications.</span></span> <span data-ttu-id="a73dd-115">С помощью Visual Studio Code и расширения КДК Visual Studio Code Вы получаете доступ к более широким функциональным возможностям.</span><span class="sxs-lookup"><span data-stu-id="a73dd-115">By using Visual Studio Code and the QDK Visual Studio Code extension you gain access to richer functionality.</span></span>

    - <span data-ttu-id="a73dd-116">Установка [VS Code](https://code.visualstudio.com/download) (Windows, Linux и Mac)</span><span class="sxs-lookup"><span data-stu-id="a73dd-116">Install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac)</span></span>
    - <span data-ttu-id="a73dd-117">Установите [расширение КДК для VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="a73dd-117">Install the [QDK extension for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

1. <span data-ttu-id="a73dd-118">Проверьте установку, создав приложение `Hello World`.</span><span class="sxs-lookup"><span data-stu-id="a73dd-118">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="a73dd-119">Создайте минимальную операцию Q#, создав файл с именем `Operation.qs` и добавив в него следующий код.</span><span class="sxs-lookup"><span data-stu-id="a73dd-119">Create a minimal Q# operation, by creating a file called `Operation.qs`, and adding the following code to it:</span></span>

        ```qsharp
        namespace HelloWorld {
            open Microsoft.Quantum.Intrinsic;
            open Microsoft.Quantum.Canon;

            operation SayHello() : Unit {
                Message("Hello from quantum world!");
            }
        }
        ```

    - <span data-ttu-id="a73dd-120">Создайте программу Python с именем `hello_world.py` для вызова операции `SayHello()` Q#.</span><span class="sxs-lookup"><span data-stu-id="a73dd-120">Create a Python program called `hello_world.py` to call the Q# `SayHello()` operation:</span></span>

        ```python
        import qsharp

        from HelloWorld import SayHello

        SayHello.simulate()
        ```

    - <span data-ttu-id="a73dd-121">Запустите программу.</span><span class="sxs-lookup"><span data-stu-id="a73dd-121">Run the program:</span></span>

        ```
        python hello_world.py
        ```

    - <span data-ttu-id="a73dd-122">Проверьте выходные данные.</span><span class="sxs-lookup"><span data-stu-id="a73dd-122">Verify the output.</span></span> <span data-ttu-id="a73dd-123">Программа должна вывести следующие строки:</span><span class="sxs-lookup"><span data-stu-id="a73dd-123">Your program should output the following lines:</span></span>

        ```
        Hello from quantum world!
        ```


> [!NOTE]
> * <span data-ttu-id="a73dd-124">Вы также можете использовать записные книжки Python Jupyter для написания классической программы Python и вызова операций Q # из ячеек.</span><span class="sxs-lookup"><span data-stu-id="a73dd-124">You can also use Python Jupyter notebooks to write the classical Python program and call Q# operations from the cells.</span></span> <span data-ttu-id="a73dd-125">Код Python — это просто обычная программа Python.</span><span class="sxs-lookup"><span data-stu-id="a73dd-125">The Python code is just a normal Python program.</span></span>

## <a name="next-steps"></a><span data-ttu-id="a73dd-126">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="a73dd-126">Next steps</span></span>

<span data-ttu-id="a73dd-127">После установки Quantum Development Kit в предпочитаемой среде вы можете написать и запустить [первую квантовую программу](xref:microsoft.quantum.quickstarts.qrng).</span><span class="sxs-lookup"><span data-stu-id="a73dd-127">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
