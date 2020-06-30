---
title: Разработка на Q# и Python
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.python
ms.openlocfilehash: 6513acd5b9cdce15ce61ed2c0454f46e6a6d9bd0
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274149"
---
# <a name="develop-with-q-and-python"></a><span data-ttu-id="769dc-102">Разработка на Q# и Python</span><span class="sxs-lookup"><span data-stu-id="769dc-102">Develop with Q# and Python</span></span>

<span data-ttu-id="769dc-103">Установите пакет QDK, чтобы разрабатывать основные программы на Python для вызова операций Q#.</span><span class="sxs-lookup"><span data-stu-id="769dc-103">Install the QDK to develop Python host programs to call Q# operations.</span></span>

1. <span data-ttu-id="769dc-104">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="769dc-104">Prerequisites</span></span>

    - <span data-ttu-id="769dc-105">[Python](https://www.python.org/downloads/) 3.6 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="769dc-105">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - <span data-ttu-id="769dc-106">Диспетчер пакетов Python [PIP](https://pip.pypa.io/en/stable/installing)</span><span class="sxs-lookup"><span data-stu-id="769dc-106">The [PIP](https://pip.pypa.io/en/stable/installing) Python package manager</span></span>
    - [<span data-ttu-id="769dc-107">Пакет SDK для .NET Core 3.1</span><span class="sxs-lookup"><span data-stu-id="769dc-107">.NET Core SDK 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)


1. <span data-ttu-id="769dc-108">Установите `qsharp` — пакет Python, который обеспечивает взаимодействие между Q# и Python.</span><span class="sxs-lookup"><span data-stu-id="769dc-108">Install the `qsharp` package, a Python package that enables interop between Q# and Python.</span></span>

    ```
    pip install qsharp
    ```

1. <span data-ttu-id="769dc-109">Установите IQ# — ядро, которое в основном используется в Jupyter и Python и предоставляет основные функции для компиляции и выполнения операций Q#.</span><span class="sxs-lookup"><span data-stu-id="769dc-109">Install IQ#, a kernel used by Jupyter and Python that provides the core functionality for compiling and executing Q# operations.</span></span>

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > <span data-ttu-id="769dc-110">Если на шаге `dotnet iqsharp install` появляется сообщение об ошибке, откройте новое окно терминала и повторите попытку.</span><span class="sxs-lookup"><span data-stu-id="769dc-110">If you get an error during the `dotnet iqsharp install` step, open a new terminal window and try again.</span></span>
    > <span data-ttu-id="769dc-111">Если это не поможет, попробуйте найти установленное средство `dotnet-iqsharp` (в Windows это `dotnet-iqsharp.exe`) и воспользуйтесь следующей командой:</span><span class="sxs-lookup"><span data-stu-id="769dc-111">If this still doesn't work, try locating the installed `dotnet-iqsharp` tool (on Windows, `dotnet-iqsharp.exe`) and running:</span></span>
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > <span data-ttu-id="769dc-112">где `/path/to/dotnet-iqsharp` следует заменить абсолютным путем к средству `dotnet-iqsharp` в вашей файловой системе.</span><span class="sxs-lookup"><span data-stu-id="769dc-112">where `/path/to/dotnet-iqsharp` should be replaced by the absolute path to the `dotnet-iqsharp` tool in your file system.</span></span>
    > <span data-ttu-id="769dc-113">Обычно оно находится в `.dotnet/tools` в папке профиля пользователя.</span><span class="sxs-lookup"><span data-stu-id="769dc-113">Typically this will be under `.dotnet/tools` in your user profile folder.</span></span>
  
1. <span data-ttu-id="769dc-114">Хотя Q# можно использовать в коде на Python в любой интегрированной среде разработки, мы настоятельно рекомендуем использовать в качестве IDE для приложений на этих двух языках Visual Studio Code (VS Code).</span><span class="sxs-lookup"><span data-stu-id="769dc-114">While you can use Q# with Python in any IDE, we highly recommend using Visual Studio Code (VS Code) IDE for your Q# + Python applications.</span></span> <span data-ttu-id="769dc-115">При использовании Visual Studio Code с расширением QDK для Visual Studio Code вы получаете доступ к более широким функциональным возможностям.</span><span class="sxs-lookup"><span data-stu-id="769dc-115">By using Visual Studio Code and the QDK Visual Studio Code extension you gain access to richer functionality.</span></span>

    - <span data-ttu-id="769dc-116">Установите [VS Code](https://code.visualstudio.com/download) (Windows, Linux и Mac).</span><span class="sxs-lookup"><span data-stu-id="769dc-116">Install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac)</span></span>
    - <span data-ttu-id="769dc-117">Установите [расширение QDK для VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="769dc-117">Install the [QDK extension for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

1. <span data-ttu-id="769dc-118">Проверьте установку, создав приложение `Hello World`.</span><span class="sxs-lookup"><span data-stu-id="769dc-118">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="769dc-119">Создайте минимальную операцию Q#, создав файл с именем `Operation.qs` и добавив в него следующий код.</span><span class="sxs-lookup"><span data-stu-id="769dc-119">Create a minimal Q# operation, by creating a file called `Operation.qs`, and adding the following code to it:</span></span>

        ```qsharp
        namespace HelloWorld {
            open Microsoft.Quantum.Intrinsic;
            open Microsoft.Quantum.Canon;

            operation SayHello() : Unit {
                Message("Hello from quantum world!");
            }
        }
        ```

    - <span data-ttu-id="769dc-120">Создайте программу Python с именем `hello_world.py` для вызова операции `SayHello()` Q#.</span><span class="sxs-lookup"><span data-stu-id="769dc-120">Create a Python program called `hello_world.py` to call the Q# `SayHello()` operation:</span></span>

        ```python
        import qsharp

        from HelloWorld import SayHello

        SayHello.simulate()
        ```

    - <span data-ttu-id="769dc-121">Запустите программу.</span><span class="sxs-lookup"><span data-stu-id="769dc-121">Run the program:</span></span>

        ```
        python hello_world.py
        ```

    - <span data-ttu-id="769dc-122">Проверьте выходные данные.</span><span class="sxs-lookup"><span data-stu-id="769dc-122">Verify the output.</span></span> <span data-ttu-id="769dc-123">Программа должна вывести следующие строки:</span><span class="sxs-lookup"><span data-stu-id="769dc-123">Your program should output the following lines:</span></span>

        ```
        Hello from quantum world!
        ```


> [!NOTE]
> * <span data-ttu-id="769dc-124">Для написания классической программы Python и вызова операций Q# из ячеек можно также использовать записные книжки Jupyter Notebook для Python.</span><span class="sxs-lookup"><span data-stu-id="769dc-124">You can also use Python Jupyter notebooks to write the classical Python program and call Q# operations from the cells.</span></span> <span data-ttu-id="769dc-125">Код Python — это просто обычная программа Python.</span><span class="sxs-lookup"><span data-stu-id="769dc-125">The Python code is just a normal Python program.</span></span>

## <a name="next-steps"></a><span data-ttu-id="769dc-126">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="769dc-126">Next steps</span></span>

<span data-ttu-id="769dc-127">После установки Quantum Development Kit в предпочитаемой среде вы можете написать и запустить [первую квантовую программу](xref:microsoft.quantum.quickstarts.qrng).</span><span class="sxs-lookup"><span data-stu-id="769dc-127">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
