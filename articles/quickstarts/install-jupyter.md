---
title: Разработка с использованием записных книжек Jupyter Notebook с Q#
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: 5c613d29c03525d29893307684f13ccd32d4d4eb
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274161"
---
# <a name="develop-with-q-jupyter-notebooks"></a>Разработка с использованием записных книжек Jupyter Notebook с Q#

Установите QDK для разработки операций Q# для записных книжек Jupyter Notebook с Q#.

Записные книжки Jupyter Notebook разрешают выполнение кода на месте наряду с инструкциями, примечаниями и другим содержимым. Эта среда идеально подходит для написания кода Q# со встроенными объяснениями или интерактивными учебниками по квантовым вычислениям. Ниже описаны действия, которые помогут вам приступить к созданию собственных записных книжек Q#.

IQ# — это расширение, которое в основном используется в Jupyter и Python с пакетом SDK для .NET Core и предоставляет основные функции для компиляции и моделирования операций Q#.

> [!NOTE]
> * Записные книжки Jupyter Notebook позволяют только выполнять код Q#. Вызывать операции Q# из внешних основных программ (например, файлов Python или C#) невозможно. Эта среда не подходит, если вы намерены использовать классическую внешнюю основную программу в сочетании с квантовой программой.

1. Предварительные требования

    - [Python](https://www.python.org/downloads/) 3.6 или более поздней версии
    - [Записная книжка Jupyter](https://jupyter.readthedocs.io/en/latest/install.html)
    - [Пакет SDK для .NET Core 3.1](https://dotnet.microsoft.com/download/dotnet-core/3.1)

1. Установите пакет `iqsharp`.

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

1. Проверьте установку, создав приложение `Hello World`.

    - Выполните следующую команду, чтобы запустить сервер записных книжек.

        ```
        jupyter notebook
        ```

    - Чтобы открыть Jupyter Notebook, скопируйте URL-адрес из командной строки и вставьте его в браузер.

    - Создайте записную книжку Jupyter Notebook с ядром Q# и добавьте следующий код в ее первую ячейку.

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - Запустите эту ячейку записной книжки.

        ![Ячейка Jupyter Notebook с кодом Q#](~/media/install-guide-jupyter.png)

        В выходных данных ячейки должно отобразиться `SayHello`. При запуске в Jupyter Notebook компилируется код Q#, а записная книжка выводит имя найденных операций.


    - В новой ячейке выполните только что созданную (в симуляторе) операцию с помощью команды `%simulate`.

        ![Ячейка Jupyter Notebook с магической командой %simulate](~/media/install-guide-jupyter-simulate.png)

        Сообщение должно отобразиться на экране вместе с результатом вызванной операции (в данном случае получен пустой кортеж `()`, поскольку операция просто возвращает тип `Unit`).

## <a name="next-steps"></a>Дальнейшие действия

Теперь, когда вы установили QDK для записных книжек Jupyter Notebook c Q#, вы можете написать и запустить [свою первую квантовую программу](xref:microsoft.quantum.quickstarts.qrng), создав код Q# непосредственно в среде Jupyter Notebook.

Воспользуйтесь приведенными ниже ресурсами, чтобы ознакомиться с другими примерами использования записных книжек Jupyter Notebook с Q#.
- [Введение в Q# и Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/). Здесь вы найдете записную книжку Jupyter Notebook с Q#, в которой демонстрируется использование Q# в этой среде.
- [Quantum Katas](xref:microsoft.quantum.overview.katas) — коллекция учебников с открытым кодом для обучения в произвольном темпе и наборы упражнений по программированию в виде записных книжек Jupyter Notebook с Q#. [Записные книжки из учебников Quantum Katas](https://github.com/microsoft/QuantumKatas#tutorial-topics) послужат хорошей отправной точкой. Коллекция Quantum Katas предназначена для обучения квантовым вычислениям с одновременным изучением программирования на Q# в произвольном темпе. Это отличный пример того, какого рода содержимое можно создать с помощью записных книжек Jupyter Notebook с Q#.
