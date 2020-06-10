---
title: Разработка на Q# + Jupyter Notebook
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: b80d95a160b5f46c1132d3428ba32ad6dcd5656e
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630334"
---
# <a name="develop-with-q-jupyter-notebooks"></a>Разработка на Q# + Jupyter Notebook

Установите КДК для разработки операций Q # для записных книжек Q # Jupyter.

Записные книжки Jupyter разрешают выполнение кода на месте наряду с инструкциями, примечаниями и другим содержимым. Эта среда идеально подходит для написания кода Q # с внедренными объяснениями или интерактивными учебниками по тактовым вычислениям. Ниже описаны действия, которые помогут вам приступить к созданию собственных записных книжек Q#.

IQ# — это расширение, которое в основном используется в Jupyter и Python с пакетом SDK для .NET Core и предоставляет основные функции для компиляции и моделирования операций Q#.

> [!NOTE]
> * В записных книжках Q # Jupyter можно запустить только Q # Code, и операции нельзя вызывать из внешних программных узлов (например, файлов Python или C#). Эта среда не подходит, если ваша цель заключается в том, чтобы объединить внешнюю программу классического узла с тактовой программой.

1. Предварительные требования

    - [Python](https://www.python.org/downloads/) 3,6 или более поздней версии
    - [Jupyter Notebook](https://jupyter.readthedocs.io/en/latest/install.html)
    - [Пакет SDK для .NET Core 3,1](https://dotnet.microsoft.com/download/dotnet-core/3.1)

1. Установите пакет `iqsharp`.

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

1. Проверьте установку, создав приложение `Hello World`.

    - Выполните следующую команду, чтобы запустить сервер записных книжек.

        ```
        jupyter notebook
        ```

    - Чтобы открыть Jupyter Notebook, скопируйте и вставьте URL-адрес, предоставленный командной строкой, в браузер.

    - Создайте Jupyter Notebook с ядром Q # и добавьте следующий код в первую ячейку записной книжки:

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - Запустите эту ячейку записной книжки.

        ![Jupyter Notebook ячейку с кодом Q #](~/media/install-guide-jupyter.png)

        В выходных данных ячейки должно отобразиться `SayHello`. При выполнении в Jupyter Notebook компилируется код Q #, а Записная книжка выводит имя найденных операций.


    - В новой ячейке выполните только что созданную операцию (в симуляторе) с помощью `%simulate` команды:

        ![Jupyter Notebook ячейка с% имитировать волшебное магическое](~/media/install-guide-jupyter-simulate.png)

        Сообщение должно отобразиться на экране вместе с результатом вызванной операции (здесь мы видим пустой кортеж, `()` так как наша операция просто возвращает `Unit` тип).

## <a name="next-steps"></a>Дальнейшие действия

Теперь, когда вы установили КДК для записных книжек "Q # Jupyter", вы можете написать и запустить [первую тактовую программу](xref:microsoft.quantum.quickstarts.qrng) , написав код Q # непосредственно в среде Jupyter Notebook.

Дополнительные примеры того, что можно делать с записными книжками Q # Jupyter, см. в следующих статьях:
- [Введение в вопросы и ответы # и Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/). Здесь вы найдете вопрос # Jupyter Notebook, в котором показано, как использовать Q # в этой среде.
- [Тактовый Катас](xref:microsoft.quantum.overview.katas), коллекция руководств для самостоятельного обучения и наборы программных упражнений в виде Q # Jupyter Notebooks. Хорошим отправной точкой являются [записные книжки](https://github.com/microsoft/QuantumKatas#tutorial-topics) , посвященные созданию Катас тактов. Тактовая Катас предназначена для обучения элементам тактовых вычислений и программированию Q # в одно и то же время. Это отличный пример того, какой тип содержимого можно создать с помощью записных книжек Q # Jupyter.
