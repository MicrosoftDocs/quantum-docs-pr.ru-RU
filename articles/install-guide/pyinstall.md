---
title: 'Разработка с помощью Q # + Python'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.python
ms.openlocfilehash: 1e40c2dddeaf4fad41693c976493f10fffffa139
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "76831007"
---
# <a name="develop-with-q--python"></a><span data-ttu-id="48d88-102">Разработка с помощью Q # + Python</span><span class="sxs-lookup"><span data-stu-id="48d88-102">Develop with Q# + Python</span></span>

<span data-ttu-id="48d88-103">Установите КДК, чтобы разрабатывать ведущие программы Python для вызова операций Q #.</span><span class="sxs-lookup"><span data-stu-id="48d88-103">Install the QDK to develop Python host programs to call Q# operations.</span></span>

1. <span data-ttu-id="48d88-104">Технические условия</span><span class="sxs-lookup"><span data-stu-id="48d88-104">Pre-requisites</span></span>

    - <span data-ttu-id="48d88-105">[Python](https://www.python.org/downloads/) 3.6 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="48d88-105">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - <span data-ttu-id="48d88-106">Диспетчер пакетов Python [PIP](https://pip.pypa.io/en/stable/installing)</span><span class="sxs-lookup"><span data-stu-id="48d88-106">The [PIP](https://pip.pypa.io/en/stable/installing) Python package manager</span></span>
    - [<span data-ttu-id="48d88-107">Пакет SDK для .NET Core 3,1 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="48d88-107">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)


1. <span data-ttu-id="48d88-108">Установите пакет `qsharp` — пакет Python, который обеспечивает взаимодействие между Q # и Python.</span><span class="sxs-lookup"><span data-stu-id="48d88-108">Install the `qsharp` package, a Python package that enables interop between Q# and Python.</span></span>

    ```bash
    pip install qsharp
    ```

1. <span data-ttu-id="48d88-109">Установите `iqsharp`, ядро, используемое Jupyter и Python, которое предоставляет основные функциональные возможности для компиляции и выполнения операций Q #.</span><span class="sxs-lookup"><span data-stu-id="48d88-109">Install `iqsharp`, a kernel used by Jupyter and Python that provides the core functionality for compiling and executing Q# operations.</span></span>

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```
  
1. <span data-ttu-id="48d88-110">Хотя Q # и Python можно использовать в любой интегрированной среде разработки, мы настоятельно рекомендуем использовать интегрированную среду разработки Visual Studio Code (VS Code) для приложений на основе Q # + Python.</span><span class="sxs-lookup"><span data-stu-id="48d88-110">While you can use Q# with Python in any IDE, we highly recommend using Visual Studio Code (VS Code) IDE for your Q# + Python applications.</span></span> <span data-ttu-id="48d88-111">С помощью Visual Studio Code и расширения КДК Visual Studio Code Вы получаете доступ к более широким функциональным возможностям.</span><span class="sxs-lookup"><span data-stu-id="48d88-111">By using Visual Studio Code and the QDK Visual Studio Code extension you gain access to richer functionality.</span></span>

    - <span data-ttu-id="48d88-112">Установка [VS Code](https://code.visualstudio.com/download) (Windows, Linux и Mac)</span><span class="sxs-lookup"><span data-stu-id="48d88-112">Install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac)</span></span>
    - <span data-ttu-id="48d88-113">Установите [расширение КДК для VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="48d88-113">Install the [QDK extension for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

1. <span data-ttu-id="48d88-114">Проверьте установку, создав приложение `Hello World`.</span><span class="sxs-lookup"><span data-stu-id="48d88-114">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="48d88-115">Создайте минимальную операцию Q#, создав файл с именем `Operation.qs` и добавив в него следующий код.</span><span class="sxs-lookup"><span data-stu-id="48d88-115">Create a minimal Q# operation, by creating a file called `Operation.qs`, and adding the following code to it:</span></span>

        ```qsharp
        namespace HelloWorld {
            open Microsoft.Quantum.Intrinsic;
            open Microsoft.Quantum.Canon;

            operation SayHello() : Unit {
                Message("Hello from quantum world!");
            }
        }
        ```

    - <span data-ttu-id="48d88-116">Создайте программу Python с именем `hello_world.py` для вызова операции `SayHello()` Q#.</span><span class="sxs-lookup"><span data-stu-id="48d88-116">Create a Python program called `hello_world.py` to call the Q# `SayHello()` operation:</span></span>

        ```python
        import qsharp

        from HelloWorld import SayHello

        SayHello.simulate()
        ```

    - <span data-ttu-id="48d88-117">Запустите программу.</span><span class="sxs-lookup"><span data-stu-id="48d88-117">Run the program:</span></span>

        ```bash
        python hello_world.py
        ```

    - <span data-ttu-id="48d88-118">Проверьте выходные данные.</span><span class="sxs-lookup"><span data-stu-id="48d88-118">Verify the output.</span></span> <span data-ttu-id="48d88-119">Программа должна вывести следующие строки:</span><span class="sxs-lookup"><span data-stu-id="48d88-119">Your program should output the following lines:</span></span>

        ```bash
        Hello from quantum world!
       ```


> [!NOTE]
> * <span data-ttu-id="48d88-120">Вы также можете использовать записные книжки Python Jupyter для написания классической программы Python и вызова операций Q # из ячеек.</span><span class="sxs-lookup"><span data-stu-id="48d88-120">You can also use Python Jupyter notebooks to write the classical Python program and call Q# operations from the cells.</span></span> <span data-ttu-id="48d88-121">Код Python — это просто обычная программа Python.</span><span class="sxs-lookup"><span data-stu-id="48d88-121">The Python code is just a normal Python program.</span></span>

## <a name="whats-next"></a><span data-ttu-id="48d88-122">Что дальше?</span><span class="sxs-lookup"><span data-stu-id="48d88-122">What's next?</span></span>

<span data-ttu-id="48d88-123">После установки Quantum Development Kit в предпочитаемой среде вы можете написать и запустить [первую квантовую программу](xref:microsoft.quantum.write-program).</span><span class="sxs-lookup"><span data-stu-id="48d88-123">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
