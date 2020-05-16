---
title: 'Разработка с помощью Q # и Python'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.python
ms.openlocfilehash: a8c5b9c25c069f98ef8eefd6cfbc36bf3376931c
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2020
ms.locfileid: "83426363"
---
# <a name="develop-with-q-and-python"></a><span data-ttu-id="9da93-102">Разработка с помощью Q # и Python</span><span class="sxs-lookup"><span data-stu-id="9da93-102">Develop with Q# and Python</span></span>

<span data-ttu-id="9da93-103">Установите КДК, чтобы разрабатывать ведущие программы Python для вызова операций Q #.</span><span class="sxs-lookup"><span data-stu-id="9da93-103">Install the QDK to develop Python host programs to call Q# operations.</span></span>

1. <span data-ttu-id="9da93-104">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="9da93-104">Pre-requisites</span></span>

    - <span data-ttu-id="9da93-105">[Python](https://www.python.org/downloads/) 3,6 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="9da93-105">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - <span data-ttu-id="9da93-106">Диспетчер пакетов Python [PIP](https://pip.pypa.io/en/stable/installing)</span><span class="sxs-lookup"><span data-stu-id="9da93-106">The [PIP](https://pip.pypa.io/en/stable/installing) Python package manager</span></span>
    - <span data-ttu-id="9da93-107">[Пакет SDK для .NET Core 3.1 или более поздней версии](https://www.microsoft.com/net/download).</span><span class="sxs-lookup"><span data-stu-id="9da93-107">[.NET Core SDK 3.1 or later](https://www.microsoft.com/net/download)</span></span>


1. <span data-ttu-id="9da93-108">Установите `qsharp` пакет, пакет Python, который обеспечивает взаимодействие между Q # и Python.</span><span class="sxs-lookup"><span data-stu-id="9da93-108">Install the `qsharp` package, a Python package that enables interop between Q# and Python.</span></span>

    ```bash
    pip install qsharp
    ```

1. <span data-ttu-id="9da93-109">Установите IQ #, ядро, используемое Jupyter и Python, которое предоставляет основные функциональные возможности для компиляции и выполнения операций Q #.</span><span class="sxs-lookup"><span data-stu-id="9da93-109">Install IQ#, a kernel used by Jupyter and Python that provides the core functionality for compiling and executing Q# operations.</span></span>

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```
  
1. <span data-ttu-id="9da93-110">Хотя Q # и Python можно использовать в любой интегрированной среде разработки, мы настоятельно рекомендуем использовать интегрированную среду разработки Visual Studio Code (VS Code) для приложений на основе Q # + Python.</span><span class="sxs-lookup"><span data-stu-id="9da93-110">While you can use Q# with Python in any IDE, we highly recommend using Visual Studio Code (VS Code) IDE for your Q# + Python applications.</span></span> <span data-ttu-id="9da93-111">С помощью Visual Studio Code и расширения КДК Visual Studio Code Вы получаете доступ к более широким функциональным возможностям.</span><span class="sxs-lookup"><span data-stu-id="9da93-111">By using Visual Studio Code and the QDK Visual Studio Code extension you gain access to richer functionality.</span></span>

    - <span data-ttu-id="9da93-112">Установка [VS Code](https://code.visualstudio.com/download) (Windows, Linux и Mac)</span><span class="sxs-lookup"><span data-stu-id="9da93-112">Install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac)</span></span>
    - <span data-ttu-id="9da93-113">Установите [расширение КДК для VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="9da93-113">Install the [QDK extension for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

1. <span data-ttu-id="9da93-114">Проверьте установку, создав приложение `Hello World`.</span><span class="sxs-lookup"><span data-stu-id="9da93-114">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="9da93-115">Создайте минимальную операцию Q#, создав файл с именем `Operation.qs` и добавив в него следующий код.</span><span class="sxs-lookup"><span data-stu-id="9da93-115">Create a minimal Q# operation, by creating a file called `Operation.qs`, and adding the following code to it:</span></span>

        ```qsharp
        namespace HelloWorld {
            open Microsoft.Quantum.Intrinsic;
            open Microsoft.Quantum.Canon;

            operation SayHello() : Unit {
                Message("Hello from quantum world!");
            }
        }
        ```

    - <span data-ttu-id="9da93-116">Создайте программу Python с именем `hello_world.py` для вызова операции `SayHello()` Q#.</span><span class="sxs-lookup"><span data-stu-id="9da93-116">Create a Python program called `hello_world.py` to call the Q# `SayHello()` operation:</span></span>

        ```python
        import qsharp

        from HelloWorld import SayHello

        SayHello.simulate()
        ```

    - <span data-ttu-id="9da93-117">Запустите программу.</span><span class="sxs-lookup"><span data-stu-id="9da93-117">Run the program:</span></span>

        ```bash
        python hello_world.py
        ```

    - <span data-ttu-id="9da93-118">Проверьте выходные данные.</span><span class="sxs-lookup"><span data-stu-id="9da93-118">Verify the output.</span></span> <span data-ttu-id="9da93-119">Программа должна вывести следующие строки:</span><span class="sxs-lookup"><span data-stu-id="9da93-119">Your program should output the following lines:</span></span>

        ```bash
        Hello from quantum world!
       ```


> [!NOTE]
> * <span data-ttu-id="9da93-120">Вы также можете использовать записные книжки Python Jupyter для написания классической программы Python и вызова операций Q # из ячеек.</span><span class="sxs-lookup"><span data-stu-id="9da93-120">You can also use Python Jupyter notebooks to write the classical Python program and call Q# operations from the cells.</span></span> <span data-ttu-id="9da93-121">Код Python — это просто обычная программа Python.</span><span class="sxs-lookup"><span data-stu-id="9da93-121">The Python code is just a normal Python program.</span></span>

## <a name="next-steps"></a><span data-ttu-id="9da93-122">Следующие шаги</span><span class="sxs-lookup"><span data-stu-id="9da93-122">Next steps</span></span>

<span data-ttu-id="9da93-123">После установки Quantum Development Kit в предпочитаемой среде вы можете написать и запустить [первую квантовую программу](xref:microsoft.quantum.quickstarts.qrng).</span><span class="sxs-lookup"><span data-stu-id="9da93-123">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
