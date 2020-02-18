---
title: 'Разработка с помощью Q # +C#'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.cs
ms.openlocfilehash: 7803846279f230f5fc0ee8424bd39be735a650ca
ms.sourcegitcommit: 5094c0a60cbafdee669c8728b92df281071259b9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2020
ms.locfileid: "77036293"
---
# <a name="develop-with-q--c"></a>Разработка с помощью Q # +C#

Установите КДК для разработки C# программ размещения, чтобы вызвать операции Q #.

Функция Q # разработана для корректного воспроизведения с помощью языков .NET, C#а именно. Вы можете работать с этой парой в разных средах разработки:

- [Вопросы и ответы C# # + использование Visual Studio (Windows)](#VS)
- [Q # + C# использование Visual Studio Code (Windows, Linux и Mac)](#VSC)
- [Q # + C# использование программы командной строки `dotnet`](#command)

## Разработка с помощью Q # C# + и Visual Studio <a name="VS"></a>

Visual Studio предлагает обширную среду для разработки программ Q #. Расширение Q # Visual Studio содержит шаблоны для Q # файлов и проектов, а также выделения синтаксиса, завершения кода и поддержки IntelliSense.


1. Предварительные требования

    - [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 с включенной рабочей нагрузкой кроссплатформенной разработки .NET Core.

1. Установите расширение Visual Studio.

    - Скачивание и установка [расширения Visual Studio](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)

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

## Разработка с помощью Q # C# + Visual Studio Code <a name="VSC"></a>

Visual Studio Code (VS Code) предоставляет обширную среду для разработки программ Q # в Windows, Linux и Mac.  Расширение Q # VS Code включает поддержку выделения синтаксиса Q #, завершения кода и фрагментов кода Q #.

1. Предварительные требования

   - [Код VS](https://code.visualstudio.com/download)
   - [Пакет SDK для .NET Core 3,1 или более поздней версии](https://www.microsoft.com/net/download)

1. Установите расширение Quantum VS Code.

    - Установите [расширение VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).

1. Установите шаблоны проектов Quantum.

   - Выберите **Представление** -> **Палитра команд**.
   - Выбор **Q #: Установка шаблонов проектов**

    Теперь Quantum Development Kit установлен и готов к использованию в ваших приложениях и библиотеках.

1. Проверьте установку, создав приложение `Hello World`.

    - Создайте новый проект:

        - Выберите **Представление** -> **Палитра команд**.
        - Выберите **Q #: создать новый проект**
        - Выберите **автономное консольное приложение**
        - Перейдите в расположение файловой системы, в котором необходимо создать приложение.
        - После создания проекта нажмите кнопку **Open new project...** (Открыть новый проект...).

    - Если вы еще не установили C# расширение для VS Code, появится всплывающее окно. Установите расширение. 

    - Запустите приложение:

        - Последовательно выберите **терминал** -> **Новый терминал** .
        - Введите `dotnet run`
        - В окне консоли `Hello quantum world!` должен отобразиться следующий текст.


> [!NOTE]
> * Сейчас рабочие области с несколькими корневыми папками не поддерживаются в расширении Visual Studio Code. Если в одной рабочей области VS Code несколько проектов, все проекты нужно разместить в одной корневой папке.

## Разработка с использованием Q # C# + с помощью средства командной строки `dotnet`<a name="command"></a>

Разумеется, вы можете создавать и запускать программы Q# и из командной строки. Для этого просто установите шаблоны проектов на основе пакетов QDK и SDK для .NET Core. 

1. Предварительные требования

    - [Пакет SDK для .NET Core 3,1 или более поздней версии](https://www.microsoft.com/net/download)

1. Установите шаблоны проектов Quantum для .NET.

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

    Теперь Quantum Development Kit установлен и готов к использованию в ваших приложениях и библиотеках.

1. Проверьте установку, создав приложение `Hello World`.

    - Создание приложения

       ```dotnetcli
       dotnet new console -lang "Q#" -o runSayHello
       ```

    - Перейдите в новый каталог приложения

       ```bash
       cd runSayHello
       ```

    Должны быть созданы два файла, а также файлы проекта приложения: файл Q# (`Operation.qs`) и файл узла C# (`Driver.cs`).

    - Выполнение приложения

        ```dotnetcli
        dotnet run
        ```

        Вы должны увидеть следующий результат: `Hello quantum world!`.

    
## <a name="whats-next"></a>Дальнейшие действия

После установки Quantum Development Kit в предпочитаемой среде вы можете написать и запустить [первую квантовую программу](xref:microsoft.quantum.write-program).