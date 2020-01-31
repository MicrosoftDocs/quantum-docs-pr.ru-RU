---
title: 'Разработка с помощью Q # Jupyter Notebooks'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: b7276f9b273f601f30e4938018398353b6a9102d
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "76831075"
---
# <a name="develop-with-q-jupyter-notebooks"></a>Разработка с помощью Q # Jupyter Notebooks

Установите КДК для разработки операций Q # для записных книжек Q # Jupyter.

Записные книжки Jupyter разрешают выполнение кода на месте наряду с инструкциями, примечаниями и другим содержимым. Эта среда идеально подходит для написания кода Q # с внедренными объяснениями или интерактивными учебниками по тактовым вычислениям. Ниже описаны действия, которые помогут вам приступить к созданию собственных записных книжек Q#.

IQ# — это расширение, которое в основном используется в Jupyter и Python с пакетом SDK для .NET Core и предоставляет основные функции для компиляции и моделирования операций Q#.

> [!NOTE]
> * В записных книжках Q # Jupyter можно запустить только Q # Code, а операции нельзя вызывать из внешних программных узлов (например, Python C# или файлов). Эта среда не подходит, если ваша цель заключается в том, чтобы объединить внешнюю программу классического узла с тактовой программой.

1. Технические условия

    - [Python](https://www.python.org/downloads/) 3.6 или более поздней версии
    - [Записная книжка Jupyter](https://jupyter.readthedocs.io/en/latest/install.html)
    - [Пакет SDK для .NET Core 3,1 или более поздней версии](https://www.microsoft.com/net/download)

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

    - Чтобы открыть записную книжку Jupyter, скопируйте и вставьте в браузер URL-адрес, предоставленный командной строкой.

    - Создайте записную книжку Jupyter с ядром Q# и добавьте следующий код в первую ячейку записной книжки.

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - Запустите эту ячейку записной книжки.

        ![Ячейка записной книжки Jupyter с кодом Q#](~/media/install-guide-jupyter.png)

        В выходных данных ячейки должно отобразиться `SayHello`. При запуске в записных книжках Jupyter компилируется код Q#, а записная книжка выводит имя найденных операций.


    - В новой ячейке выполните только что созданную операцию (в симуляторе) с помощью команды `%simulate`.

        ![Ячейка записной книжки Jupyter с магической командой %simulate](~/media/install-guide-jupyter-simulate.png)

        Сообщение должно отобразиться на экране вместе с результатом вызванной операции (здесь отображается пустой кортеж `()` так как наша операция просто возвращает тип `Unit`).

## <a name="whats-next"></a>Что дальше?

После установки Quantum Development Kit в предпочитаемой среде вы можете написать и запустить [первую квантовую программу](xref:microsoft.quantum.write-program).
