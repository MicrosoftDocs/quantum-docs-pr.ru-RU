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
# <a name="develop-with-q-and-python"></a>Разработка с помощью Q # и Python

Установите КДК, чтобы разрабатывать ведущие программы Python для вызова операций Q #.

1. Предварительные требования

    - [Python](https://www.python.org/downloads/) 3,6 или более поздней версии
    - Диспетчер пакетов Python [PIP](https://pip.pypa.io/en/stable/installing)
    - [Пакет SDK для .NET Core 3,1](https://dotnet.microsoft.com/download/dotnet-core/3.1)


1. Установите `qsharp` пакет, пакет Python, который обеспечивает взаимодействие между Q # и Python.

    ```
    pip install qsharp
    ```

1. Установите IQ #, ядро, используемое Jupyter и Python, которое предоставляет основные функциональные возможности для компиляции и выполнения операций Q #.

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > Если на шаге появляется сообщение об ошибке `dotnet iqsharp install` , откройте новое окно терминала и повторите попытку.
    > Если это не поможет, попробуйте найти установленное `dotnet-iqsharp` средство (в Windows `dotnet-iqsharp.exe` ) и запустить:
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > где `/path/to/dotnet-iqsharp` следует заменить абсолютным путем к `dotnet-iqsharp` средству в файловой системе.
    > Обычно это будет находиться `.dotnet/tools` в папке профиля пользователя.
  
1. Хотя Q # и Python можно использовать в любой интегрированной среде разработки, мы настоятельно рекомендуем использовать интегрированную среду разработки Visual Studio Code (VS Code) для приложений на основе Q # + Python. С помощью Visual Studio Code и расширения КДК Visual Studio Code Вы получаете доступ к более широким функциональным возможностям.

    - Установка [VS Code](https://code.visualstudio.com/download) (Windows, Linux и Mac)
    - Установите [расширение КДК для VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).

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
> * Вы также можете использовать записные книжки Python Jupyter для написания классической программы Python и вызова операций Q # из ячеек. Код Python — это просто обычная программа Python.

## <a name="next-steps"></a>Дальнейшие действия

После установки Quantum Development Kit в предпочитаемой среде вы можете написать и запустить [первую квантовую программу](xref:microsoft.quantum.quickstarts.qrng).
