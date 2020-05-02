---
title: Разработка на Q# + Python
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.python
ms.openlocfilehash: e1b8a0c68b3ac0c059c6de6e478593321764ff88
ms.sourcegitcommit: db23885adb7ff76cbf8bd1160d401a4f0471e549
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/01/2020
ms.locfileid: "82680146"
---
# <a name="develop-with-q--python"></a>Разработка на Q# + Python

Установите КДК, чтобы разрабатывать ведущие программы Python для вызова операций Q #.

1. Предварительные требования

    - [Python](https://www.python.org/downloads/) 3,6 или более поздней версии
    - Диспетчер пакетов Python [PIP](https://pip.pypa.io/en/stable/installing)
    - [Пакет SDK для .NET Core 3.1 или более поздней версии](https://www.microsoft.com/net/download).


1. Установите `qsharp` пакет, пакет Python, который обеспечивает взаимодействие между Q # и Python.

    ```bash
    pip install qsharp
    ```

1. Установите IQ #, ядро, используемое Jupyter и Python, которое предоставляет основные функциональные возможности для компиляции и выполнения операций Q #.

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```
  
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

        ```bash
        python hello_world.py
        ```

    - Проверьте выходные данные. Программа должна вывести следующие строки:

        ```bash
        Hello from quantum world!
       ```


> [!NOTE]
> * Вы также можете использовать записные книжки Python Jupyter для написания классической программы Python и вызова операций Q # из ячеек. Код Python — это просто обычная программа Python.

## <a name="whats-next"></a>Что дальше?

После установки Quantum Development Kit в предпочитаемой среде вы можете написать и запустить [первую квантовую программу](xref:microsoft.quantum.write-program).
