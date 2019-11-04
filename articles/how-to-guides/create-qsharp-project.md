---
title: 'Узнайте, как создать проект Q # с помощью пакета средств разработки такта (КДК).'
description: 'Инициализация проекта для разработки на такте с помощью КДК и Q # в выбранной среде разработки'
author: natke
ms.author: nakersha
ms.date: 10/19/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.howto.createproject
ms.openlocfilehash: b4bec5e7a174b7e2d588331dd2093c7b23a728b0
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2019
ms.locfileid: "73444180"
---
# <a name="create-a-q-project-in-your-development-environment"></a>Создание проекта Q # в среде разработки

Узнайте, как создать проект Q # с помощью КДК.

Проект Q # содержит файлы Q #, содержащие тактовый код, а также ведущее приложение для запуска тактовой программы. Вы можете написать ведущее приложение на языках .NET C#, например, или в Python. Вы также можете выполнить код Q # в записной книжке Jupyter с помощью ядра IQ #.

Выберите среду разработки и язык в следующих разделах:

* [Python](#create-a-python-project)
* [Записные книжки Jupyter](#create-a-jupyter-notebook-project)
* [C#с помощью Visual Studio](#create-a-c-project-on-windows-using-visual-studio)
* [C#с VS Code](#create-a-c-project-using-vs-code)
* [C#с помощью командной строки](#create-a-c-project-using-the-dotnet-command-line-tool)

## <a name="create-a-python-project"></a>Создание проекта Python

1. Технические условия

     * [Пакет средств разработки тактов для Python](xref:microsoft.quantum.install#develop-with-python)

1. Создайте папку для проекта и перейдите к этой папке.

1. Создайте файл Q # с именем `Operation.qs`и добавьте в него код Q #. Пример.

    ```qsharp
    namespace HelloWorld {
        open Microsoft.Quantum.Intrinsic;
        open Microsoft.Quantum.Canon;

        operation SayHello() : Result {
            Message("Hello from quantum world!");
            return Zero;
        }
    }
    ```

1. Создайте файл узла Python с именем `host.py`, чтобы вызвать операцию Q #. Пример.

    ```python
    import qsharp

    from HelloWorld import SayHello

    SayHello.simulate()
    ```

1. Запустите программу.

    ```bash
    python host.py
    ```

1. Проверьте выходные данные. Программа должна вывести следующие строки:

    ```bash
    Hello from quantum world!
    0
    ```

Теперь вы можете продолжить разработку тактовой программы.

## <a name="create-a-jupyter-notebook-project"></a>Создание проекта Jupyter Notebook

1. Технические условия

    * [Набор средств разработки тактов для записных книжек Jupyter](xref:microsoft.quantum.install#develop-with-jupyter-notebooks)

1. Выполните следующую команду, чтобы запустить сервер записных книжек.

    ```bash
    jupyter notebook
    ```

1. Перейдите по URL-адресу, указанному в командной строке. Пример: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85 ]

1. В браузере появится страница Jupyter. На вкладке **файлы** выберите **создать** > **Q #** , чтобы создать записную книжку Jupyter с ядром Q #. Добавьте следующий код в первую ячейку записной книжки:

    ```qsharp
    operation SayHello() : Unit {
        Message("Hello from quantum world!");
    }
    ```

1. Выберите **ячейка** > **Запуск ячеек** для запуска записной книжки. `SayHello` скоро появится в выходных данных ячейки:

    ![Ячейка записной книжки Jupyter с кодом Q #](~/media/install-guide-jupyter.png)

    При запуске в записных книжках Jupyter компилируется код Q #, а Записная книжка выводит имя найденных операций.

1. В новой ячейке имитируйте выполнение на компьютере-такте операции, которую вы только что создали, используя магическую `%simulate`:

    ![Jupyter ячейка записной книжки с% имитировать волшебность](~/media/install-guide-jupyter-simulate.png)

    Сообщение должно отобразиться на экране вместе с результатом вызванной операции (в данном случае это пустое значение).

Теперь можно добавить другие операции Q #, чтобы продолжить разработку тактов.

## <a name="create-a-c-project-on-windows-using-visual-studio"></a>Создание C# проекта в Windows с помощью Visual Studio

1. Технические условия

    * [Пакет средств разработки тактов для Visual Studio](xref:microsoft.quantum.install#develop-with-c-on-windows-using-visual-studio)

1. Создайте приложение Q#.

    * Выберите **Файл** -> **Создать** -> **Проект**.
    * Введите `Q#` в поле поиска.
    * Выберите **Приложение Q#** .
    * Щелкните **Далее**.
    * Выберите имя и расположение для приложения.
    * Нажмите кнопку **Создать**

1. Проверьте проект.

    Должны быть созданы два файла: `Driver.cs` — ведущее приложение C#; и `Operation.qs` — программа Q#, которая определяет простую операцию вывода сообщения в консоль.

1. Выполнение приложения

    * Выберите **Отладка** -> **Запустить без отладки**.
    * В окне консоли должен отобразиться текст `Hello quantum world!`.

Теперь вы можете продолжить разработку тактов с помощью Visual Studio.

> [!NOTE]
> * Если в одном решении Visual Studio несколько проектов, все проекты, включенные в решение, нужно разместить в той же папке, что и решение, или в одной из вложенных в нее папок.  

## <a name="create-a-c-project-using-vs-code"></a>Создание C# проекта с помощью VS Code

1. Технические условия

    * [Пакет средств разработки тактов для VS Code](xref:microsoft.quantum.install#develop-with-c-using-visual-studio-code)

1. Создайте новый проект:

    * Выберите **Представление** -> **Палитра команд**.
    * Выберите **Q #: создать новый проект**
    * Перейдите в расположение файловой системы, в котором необходимо создать приложение.
    * После создания проекта нажмите кнопку **Open new project...** (Открыть новый проект...).

1. Запустите приложение:

    * Выберите **Отладка** -> **Запустить без отладки**.
    * В окне консоли `Hello quantum world!` должен отобразиться следующий текст.

Теперь можно продолжить разработку тактов с помощью Visual Studio Code.

> [!NOTE]
> * Сейчас рабочие области с несколькими корневыми папками не поддерживаются в расширении Visual Studio Code. Если в одной рабочей области VS Code несколько проектов, все проекты нужно разместить в одной корневой папке.

## <a name="create-a-c-project-using-the-dotnet-command-line-tool"></a>Создание C# проекта с помощью средства командной строки `dotnet`

1. Технические условия

    * [Пакет средств разработки тактов для командной строки](xref:microsoft.quantum.install#develop-with-c-using-the-dotnet-command-line-tool)

1. Создание приложения

    ```bash
    dotnet new console -lang Q# -o <project name>
    ```

1. Перейдите в новый каталог приложения

    ```bash
    cd <project name>
    ```

    Должны быть созданы два файла, а также файлы проекта приложения: файл Q# (`Operation.qs`) и файл узла C# (`Driver.cs`).

1. Выполнение приложения

    ```bash
    dotnet run
    ```

    Вы должны увидеть следующий результат: `Hello quantum world!`.

Теперь вы можете продолжить разработку тактов с помощью средств командной строки.

## <a name="whats-next"></a>Что дальше?

После создания проекта в предпочитаемой среде можно продолжить разработку тактов.
