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
# <a name="develop-with-q-and-python"></a>Разработка на Q# и Python

Установите пакет QDK, чтобы разрабатывать основные программы на Python для вызова операций Q#.

1. Предварительные требования

    - [Python](https://www.python.org/downloads/) 3.6 или более поздней версии
    - Диспетчер пакетов Python [PIP](https://pip.pypa.io/en/stable/installing)
    - [Пакет SDK для .NET Core 3.1](https://dotnet.microsoft.com/download/dotnet-core/3.1)


1. Установите `qsharp` — пакет Python, который обеспечивает взаимодействие между Q# и Python.

    ```
    pip install qsharp
    ```

1. Установите IQ# — ядро, которое в основном используется в Jupyter и Python и предоставляет основные функции для компиляции и выполнения операций Q#.

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > Если на шаге `dotnet iqsharp install` появляется сообщение об ошибке, откройте новое окно терминала и повторите попытку.
    > Если это не поможет, попробуйте найти установленное средство `dotnet-iqsharp` (в Windows это `dotnet-iqsharp.exe`) и воспользуйтесь следующей командой:
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > где `/path/to/dotnet-iqsharp` следует заменить абсолютным путем к средству `dotnet-iqsharp` в вашей файловой системе.
    > Обычно оно находится в `.dotnet/tools` в папке профиля пользователя.
  
1. Хотя Q# можно использовать в коде на Python в любой интегрированной среде разработки, мы настоятельно рекомендуем использовать в качестве IDE для приложений на этих двух языках Visual Studio Code (VS Code). При использовании Visual Studio Code с расширением QDK для Visual Studio Code вы получаете доступ к более широким функциональным возможностям.

    - Установите [VS Code](https://code.visualstudio.com/download) (Windows, Linux и Mac).
    - Установите [расширение QDK для VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).

1. Проверьте установку, создав приложение `Hello World`.

    - Создайте минимальную операцию Q#, создав файл с именем `Operation.qs` и добавив в него следующий код.

        ```qsharp
        namespace HelloWorld {
            open Microsoft.Quantum.Intrinsic;
            open Microsoft.Quantum.Canon;

            operation SayHello() : Unit {
                Message("Hello from quantum world!");
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

        ```
        python hello_world.py
        ```

    - Проверьте выходные данные. Программа должна вывести следующие строки:

        ```
        Hello from quantum world!
        ```


> [!NOTE]
> * Для написания классической программы Python и вызова операций Q# из ячеек можно также использовать записные книжки Jupyter Notebook для Python. Код Python — это просто обычная программа Python.

## <a name="next-steps"></a>Дальнейшие действия

После установки Quantum Development Kit в предпочитаемой среде вы можете написать и запустить [первую квантовую программу](xref:microsoft.quantum.quickstarts.qrng).
