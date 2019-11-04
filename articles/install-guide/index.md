---
title: Сведения об установке Microsoft Quantum Development Kit (QDK)
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: 2a098d89f13278d7137bf182a184a74afb9393be
ms.sourcegitcommit: 2ca4755d1a63431e3cb2d2918a10ad477ec2e368
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2019
ms.locfileid: "73462869"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a>Установка Microsoft Quantum Development Kit (QDK)

Узнайте, как установить Microsoft Quantum Development Kit (QDK), чтобы приступить к работе с квантовым программированием. QDK состоит из следующих компонентов:

- язык программирования Q#;
- набор библиотек, абстрагирующих сложные функции в Q#;
- ведущее приложение (написанное на языке Python или .NET), которое запускает квантовые операции, написанные на языке Q#;
- средства для упрощения разработки.

Этапы установки различаются в зависимости от выбранной среды разработки. Выберите среду из следующих разделов.

## <a name="develop-with-python"></a>Разработка на языке Python

Пакет Q# для Python позволяет легко моделировать операции и функции Q# в Python. IQ# — это расширение, которое в основном используется в Jupyter и Python и предоставляет основные функции для компиляции и моделирования операций Q#.

1. Предварительные требования

    - [Python](https://www.python.org/downloads/) 3.6 или более поздней версии
    - Диспетчер пакетов Python [PIP](https://pip.pypa.io/en/stable/installing)
    - [Пакет SDK для .NET Core 3.0 или более поздней версии](https://www.microsoft.com/net/download)

1. Установите пакет `iqsharp`.

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. Установите пакет `qsharp`.

    ```bash
    pip install qsharp
    ```

1. Проверьте установку, создав приложение `Hello World`.

    - Создайте минимальную операцию Q#, создав файл с именем `Operation.qs` и добавив в него следующий код.

        ```qsharp
        namespace HelloWorld
        {
            open Microsoft.Quantum.Intrinsic;
            open Microsoft.Quantum.Canon;

            operation SayHello() : Result {
                Message("Hello from quantum world!");
                return Zero;
            }
        }
        ```

    - Создайте программу Python с именем `hello_world.py` для вызова операции `SayHello()` Q#.

        ```python
        import qsharp

        from HelloWorld import SayHello

        SayHello.simulate()
        ```

    - Запустите программу.

        ```bash
        python hello_world.py
        ```

    - Проверьте выходные данные. Программа должна вывести следующие строки:

        ```bash
        Hello from quantum world!
       0
       ```

## <a name="develop-with-jupyter-notebooks"></a>Разработка с использованием записных книжек Jupyter

Jupyter Notebook — это широко используемое в образовательных учреждениях, научных лабораториях и интерактивном программировании решение. Оно позволяет выполнять код локально, включая код Q#, инструкции, примечания и другое содержимое.  Ниже описаны действия, которые помогут вам приступить к созданию собственных записных книжек Q#.

IQ# — это расширение, которое в основном используется в Jupyter и Python с пакетом SDK для .NET Core и предоставляет основные функции для компиляции и моделирования операций Q#.


1. Предварительные требования

    - [Python](https://www.python.org/downloads/) 3.6 или более поздней версии
    - [Записная книжка Jupyter](https://jupyter.readthedocs.io/en/latest/install.html)
    - [Пакет SDK для .NET Core 3.0 или более поздней версии](https://www.microsoft.com/net/download)

1. Установите пакет `iqsharp`.

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. Проверьте установку, создав приложение `Hello World`.

    - Выполните следующую команду, чтобы запустить сервер записных книжек.

        ```bash
        jupyter notebook
        ```

    - Перейдите по URL-адресу, указанному в командной строке. Пример: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85 ]

    - Создайте записную книжку Jupyter с ядром Q# и добавьте следующий код в первую ячейку записной книжки.

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - Запустите эту ячейку записной книжки.

        ![Ячейка записной книжки Jupyter с кодом Q#](~/media/install-guide-jupyter.png)

        В выходных данных ячейки должно отобразиться `SayHello`. При запуске в записных книжках Jupyter компилируется код Q#, а записная книжка выводит имя найденных операций.


    - В новой ячейке смоделируйте выполнение операции, которую вы только что создали, на квантовом компьютере. Для этого используйте магическую команду `%simulate`:

        ![Ячейка записной книжки Jupyter с магической командой %simulate](~/media/install-guide-jupyter-simulate.png)

        Сообщение должно отобразиться на экране вместе с результатом вызванной операции (в нашем примере это пустое значение).


## <a name="develop-with-c-on-windows-using-visual-studio"></a>Разработка на языке C# в Windows с помощью Visual Studio

Visual Studio обеспечивает обширную среду для разработки программ Q# с такими возможностями, как завершение кода и выделение синтаксиса, которые помогают разработчикам создавать приложения.  Расширение Q# Visual Studio содержит шаблоны для файлов и проектов Q#, а также предоставляет возможность выделения синтаксиса и поддержку IntelliSense.


1. Предварительные требования

    - [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 с включенной рабочей нагрузкой кроссплатформенной разработки .NET Core.

1. Установите расширение Visual Studio.

    - Скачайте [расширение Visual Studio](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).
    - Добавьте расширение в Visual Studio.

1. Проверьте установку, создав приложение `Hello World`.

    - Создайте приложение Q#.

        - Выберите **Файл** -> **Создать** -> **Проект**.
        - Введите `Q#` в поле поиска.
        - Выберите **Приложение Q#** .
        - Щелкните **Далее**.
        - Выберите имя и расположение для приложения.
        - Нажмите кнопку **Создать**

    - Проверьте проект.

        Должны быть созданы два файла: `Driver.cs` — ведущее приложение C#; и `Operation.qs` — программа Q#, которая определяет простую операцию вывода сообщения в консоль.

    - Выполнение приложения

        - Выберите **Отладка** -> **Запустить без отладки**.
        - В окне консоли должен отобразиться текст `Hello quantum world!`.

> [!NOTE]
> * Если в одном решении Visual Studio несколько проектов, все проекты, включенные в решение, нужно разместить в той же папке, что и решение, или в одной из вложенных в нее папок.  

## <a name="develop-with-c-using-visual-studio-code"></a>Разработка с помощью C# и Visual Studio Code

Visual Studio Code (VS Code) обеспечивает обширную среду для разработки программ Q# в разных вычислительных средах, включая Windows, Linux и Mac, с такими возможностями, как завершение кода и выделение синтаксиса, которые помогают разработчикам создавать приложения.  Расширение Q# VS Code предоставляет возможность выделения синтаксиса и фрагменты кода Q#.

1. Предварительные требования

   - [Код VS](https://code.visualstudio.com/download)
   - [Пакет SDK для .NET Core 3.0 или более поздней версии](https://www.microsoft.com/net/download)

1. Установите расширение Quantum VS Code.

    - Установите [расширение VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).

1. Установите шаблоны проектов Quantum.

   - Выберите **Представление** -> **Палитра команд**.
   - Выберите **Q#: Install project templates** (Q#: установить шаблоны проектов).

    Теперь Quantum Development Kit установлен и готов к использованию в ваших приложениях и библиотеках.

1. Проверьте установку, создав приложение `Hello World`.

    - Создайте новый проект:

        - Выберите **Представление** -> **Палитра команд**.
        - Выберите **Q#: Create New Project**(Q#: создать проект).
        - Перейдите в расположение файловой системы, в котором необходимо создать приложение.
        - После создания проекта нажмите кнопку **Open new project...** (Открыть новый проект...).

    - Запустите приложение:

        - Выберите **Отладка** -> **Запустить без отладки**.
        - В окне консоли `Hello quantum world!` должен отобразиться следующий текст.

> [!NOTE]
> * > * Сейчас рабочие области с несколькими корневыми папками не поддерживаются в расширении Visual Studio Code. Если в одной рабочей области VS Code несколько проектов, все проекты нужно разместить в одной корневой папке.

## <a name="develop-with-c-using-the-dotnet-command-line-tool"></a>Разработка на языке C# с помощью программы командной строки `dotnet`

Разумеется, вы можете создавать и запускать программы Q# и из командной строки. Для этого просто установите шаблоны проектов на основе пакетов QDK и SDK для .NET Core. 

1. Предварительные требования

    - [Пакет SDK для .NET Core 3.0 или более поздней версии](https://www.microsoft.com/net/download)

1. Установите шаблоны проектов Quantum для .NET.

    ```bash
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

    Теперь Quantum Development Kit установлен и готов к использованию в ваших приложениях и библиотеках.

1. Проверьте установку, создав приложение `Hello World`.

    - Создание приложения

       ```bash
       dotnet new console -lang Q# -o runSayHello
       ```

    - Перейдите в новый каталог приложения

       ```bash
       cd runSayHello
       ```

    Должны быть созданы два файла, а также файлы проекта приложения: файл Q# (`Operation.qs`) и файл узла C# (`Driver.cs`).

    - Выполнение приложения

        ```bash
        dotnet run
        ```

        Вы должны увидеть следующий результат: `Hello quantum world!`.

## <a name="whats-next"></a>Что дальше?

После установки Quantum Development Kit в предпочитаемой среде вы можете написать и запустить [первую квантовую программу](xref:microsoft.quantum.write-program).
