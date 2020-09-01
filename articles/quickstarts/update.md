---
title: Обновление Quantum Development Kit (QDK)
description: Описание процесса обновления проектов Q# и Microsoft Quantum Development Kit до текущей версии.
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
no-loc:
- Q#
- $$v
ms.openlocfilehash: 84782d1628dd100c0939b2b12aa0a9aa8ab2b80e
ms.sourcegitcommit: 75c4edc7c410cc63dc8352e2a5bef44b433ed188
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/25/2020
ms.locfileid: "88863640"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a>Обновление пакета средств разработки Microsoft Quantum Development Kit (QDK)

Узнайте, как обновить Microsoft Quantum Development Kit (QDK) до новейшей версии.

В этой статье предполагается, что у вас уже установлен пакет QDK. Если вы устанавливаете его в первый раз, обратитесь к [руководству по установке](xref:microsoft.quantum.install).

Мы рекомендуем следить за выпуском новых версий QDK. Следуйте этому руководству по обновлению, чтобы выполнить обновление до последней версии QDK. Процесс состоит из двух частей:
1. Обновление имеющихся файлов Q# и проектов для согласования кода с обновленным синтаксисом.
2. Обновление самого пакета QDK для выбранной среды разработки.

## <a name="updating-no-locq-projects"></a>Обновление проектов Q# 

Следуйте этим инструкциям по обновлению проектов Q# независимо от того, на каком языке написана ведущая программа для выполнения операций Q#: C# или Python.

1. Сначала убедитесь, что у вас установлена последняя версия [пакета SDK для .NET Core 3.1](https://dotnet.microsoft.com/download). Запустите выполнение следующей команды в командной строке:

    ```dotnetcli
    dotnet --version
    ```

    Убедитесь, что в результате получена версия `3.1.100` или более новая. В противном случае установите [последнюю версию](https://dotnet.microsoft.com/download) и повторите проверку снова. Затем следуйте приведенным ниже инструкциям в зависимости от настроек (в Visual Studio, Visual Studio Code или непосредственно в командной строке).

### <a name="update-no-locq-projects-in-visual-studio"></a>Обновление проектов Q# в Visual Studio
 
1. Обновите Visual Studio 2019 до последней версии. Инструкции см. [здесь](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019).
2. Откройте решение в Visual Studio.
3. В меню выберите **Сборка** -> **Очистить решение**.
4. В каждом из CSPROJ-файлов обновите требуемую версию .NET Framework до `netcoreapp3.1` (или `netstandard2.1`, если это проект библиотеки).
    То есть измените такого рода строки:

    ```xml
    <TargetFramework>netcoreapp3.1</TargetFramework>
    ```

    Дополнительные сведения о том, как указать требуемую версию .NET Framework, см. [здесь](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).

5. В каждом из CSPROJ-файлов задайте в качестве пакета SDK `Microsoft.Quantum.Sdk`, как показано в строке ниже. Обратите внимание, что в качестве номера версии следует указать последний доступный. Его можно узнать из [заметок о выпуске](https://docs.microsoft.com/quantum/relnotes/).

    ```xml
    <Project Sdk="Microsoft.Quantum.Sdk/0.12.20072031">
    ```

6. Сохраните и закройте все файлы в решении.

7. Выберите **Сервис** -> **Командная строка** -> **Командная строка разработчика**. Кроме того, в Visual Studio можно воспользоваться консолью диспетчера пакетов.

8. Чтобы **удалить** все пакеты, воспользуйтесь для каждого проекта в решении следующей командой:

    ```dotnetcli
    dotnet remove [project_name].csproj package Microsoft.Quantum.Development.Kit
    ```

   Если в проектах используются другие пакеты Microsoft.Quantum или Microsoft.Azure.Quantum (например, Microsoft.Quantum.Numerics), запустите для них выполнение команды **add**, чтобы обновить используемую версию.

    ```dotnetcli
    dotnet add [project_name].csproj package [package_name]
    ```

9. Закройте командную строку и выберите **Сборка** -> **Собрать решение** (*не* выбирайте "Пересобрать решение").

Теперь вы можете сразу перейти к [обновлению расширения QDK для Visual Studio](#update-visual-studio-qdk-extension).


### <a name="update-no-locq-projects-in-visual-studio-code"></a>Обновление проектов Q# в Visual Studio Code

1. В Visual Studio Code откройте папку с проектом, который необходимо обновить.
2. Выберите **Терминал** -> **Создать терминал**.
3. Выполните инструкции по обновлению с помощью командной строки (см. ниже).

### <a name="update-no-locq-projects-using-the-command-prompt"></a>Обновление проектов Q# с помощью командной строки

1. Перейдите к папке, содержащей основной файл проекта.

2. Выполните следующую команду:

    ```dotnetcli
    dotnet clean [project_name].csproj
    ```

3. Определите текущую версию QDK. Ее можно узнать из [заметок о выпуске](https://docs.microsoft.com/quantum/relnotes/). Формат версии будет аналогичен следующему: `0.12.20072031`.

4. В каждом из файлов `.csproj` выполните следующие действия:

    - Обновите требуемую версию .NET Framework до `netcoreapp3.1` (или `netstandard2.1`, если это проект библиотеки). То есть измените такого рода строки:

        ```xml
        <TargetFramework>netcoreapp3.1</TargetFramework>
        ```

        Дополнительные сведения о том, как указать требуемую версию .NET Framework, см. [здесь](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).

    - Замените ссылку на пакет SDK в определении проекта. Убедитесь, что номер версии соответствует значению, определенному на **шаге 3**.

        ```xml
        <Project Sdk="Microsoft.Quantum.Sdk/0.12.20072031">
        ```

    - Удалите ссылку на пакет `Microsoft.Quantum.Development.Kit` (если таковая имеется). Она будет указана в следующей записи:

        ```xml
        <PackageReference Include="Microsoft.Quantum.Development.Kit" Version="0.10.1910.3107" />
        ```

    - Обновите версию всех пакетов Microsoft Quantum до последней выпущенной версии QDK (определяется на **шаге 3**). Имена этих пакетов соответствуют следующему шаблону:

        ```
        Microsoft.Quantum.*
        Microsoft.Azure.Quantum.*
        ```
    
        Ссылки на пакеты задаются в следующем формате:

        ```xml
        <PackageReference Include="Microsoft.Quantum.Compiler" Version="0.12.20072031" />
        ```

    - Сохраните обновленный файл.

    - Восстановите зависимости проекта с помощью следующей команды:

        ```dotnetcli
        dotnet restore [project_name].csproj
        ```

4. Вернитесь к папке, содержащей основной файл проекта, и воспользуйтесь следующей командой:

    ```dotnetcli
    dotnet build [project_name].csproj
    ```

После обновления проектов Q# следуйте приведенным ниже инструкциям, чтобы обновить сам пакет QDK.

## <a name="updating-the-qdk"></a>Обновление пакета QDK

Процесс обновления QDK зависит от языка и среды разработки.
Выберите среду разработки ниже.

* [Python: обновление пакета `qsharp`](#update-the-qsharp-python-package)
* [Jupyter Notebooks: обновление ядра IQ#](#update-the-iq-jupyter-kernel)
* [Visual Studio: обновление расширения QDK](#update-visual-studio-qdk-extension)
* [VS Code: обновление расширения QDK](#update-vs-code-qdk-extension)
* [Командная строка и C#: обновление шаблонов проектов](#c-using-the-dotnet-command-line-tool)


### <a name="update-the-qsharp-python-package"></a>Обновление пакета Python `qsharp`

Процедура обновления зависит от того, была ли изначально установка выполнена с помощью conda или с помощью .NET CLI и pip.

#### <a name="update-using-conda-recommended"></a>[Обновление с использованием conda (рекомендуется)](#tab/tabid-conda)

1. Активируйте среду conda, в которой установлен пакет `qsharp`, а затем выполните следующую команду, чтобы обновить ее:

    ```
    conda update -c quantum-engineering qsharp
    ```

1. Запустите выполнение следующей команды из расположения файлов `.qs`:

    ```
    python -c "import qsharp; qsharp.reload()"
    ```

#### <a name="update-using-net-cli-and-pip-advanced"></a>[Обновление с использованием .NET CLI и pip (расширенное)](#tab/tabid-dotnetcli)

1. Обновите ядро `iqsharp`. 

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. Проверьте версию `iqsharp`.

    ```dotnetcli
    dotnet iqsharp --version
    ```

    Вы должны увидеть следующий результат.

    ```
    iqsharp: 0.12.20072031
    Jupyter Core: 1.4.0.0
    ```

    Не беспокойтесь, если ваша версия `iqsharp` выше. Она должна соответствовать [последнему выпуску](xref:microsoft.quantum.relnotes).

1. Обновите версию пакета `qsharp`:

    ```
    pip install qsharp --upgrade
    ```

1. Проверьте версию `qsharp`:

    ```
    pip show qsharp
    ```

    Вы должны увидеть следующий результат.

    ```
    Name: qsharp
    Version: 0.12.2007.2031
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```

1. Запустите выполнение следующей команды из расположения файлов `.qs`:

    ```
    python -c "import qsharp; qsharp.reload()"
    ```

***

Теперь вы можете использовать обновленную версию пакета Python `qsharp` для выполнения имеющихся квантовых программ.

### <a name="update-the-ino-locq-jupyter-kernel"></a>Обновление ядра IQ# для Jupyter

Процедура обновления зависит от того, была ли изначально установка выполнена с помощью conda или с помощью .NET CLI и pip.

#### <a name="update-using-conda-recommended"></a>[Обновление с использованием conda (рекомендуется)](#tab/tabid-conda)

1. Активируйте среду conda, в которой установлен пакет `qsharp`, а затем выполните следующую команду, чтобы обновить ее:

    ```
    conda update -c quantum-engineering qsharp
    ```

1. Выполните следующую команду из ячейки в каждой из существующих записных книжек Jupyter Notebook для Q#:

    ```
    %workspace reload
    ```

#### <a name="update-using-net-cli-and-pip-advanced"></a>[Обновление с использованием .NET CLI и pip (расширенное)](#tab/tabid-dotnetcli)

1. Обновите версию пакета `Microsoft.Quantum.IQSharp`:

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. Проверьте версию `iqsharp`:

    ```dotnetcli
    dotnet iqsharp --version
    ```

    Вывод приложения должен быть аналогичен приведенному ниже:

    ```
    iqsharp: 0.12.20072031
    Jupyter Core: 1.4.0.0
    ```

    Не беспокойтесь, если ваша версия `iqsharp` выше. Она должна соответствовать [последнему выпуску](xref:microsoft.quantum.relnotes).

1. Выполните следующую команду из ячейки в каждой из существующих записных книжек Jupyter Notebook для Q#:

    ```
    %workspace reload
    ```

***

Теперь вы можете использовать обновленное ядро IQ# для запуска существующих записных книжек Jupyter Notebook для Q#.

### <a name="update-visual-studio-qdk-extension"></a>Обновление расширения QDK для Visual Studio

1. Обновление расширения Visual Studio для Q#

    - Visual Studio предложит принять обновления [расширения Quantum для Visual Studio](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).
    - Примите обновление.

    > [!NOTE]
    > Шаблоны проектов обновляются с помощью расширения. Обновленные шаблоны применяются только к новым проектам. При обновлении расширения код имеющихся проектов не обновляется.

### <a name="update-vs-code-qdk-extension"></a>Обновление расширения QDK для VS Code

1. Обновите расширение Quantum для VS Code.

    - Перезапустите VS Code.
    - Перейдите на вкладку **Расширения**.
    - Выберите расширение **Microsoft Quantum Development Kit для Visual Studio Code**.
    - Перезагрузите расширение.

### <a name="c-using-the-dotnet-command-line-tool"></a>C# с использованием программы командной строки `dotnet`

1. Обновите шаблоны проектов Quantum для .NET.

    Из командной строки:

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

   Кроме того, если предполагается использовать шаблоны командной строки и у вас уже установлено расширение QDK VS Code, можно обновить шаблоны проектов из самого расширения:

   - [Обновить расширение QDK](#update-vs-code-qdk-extension)
   - В VS Code выберите **Представление** -> **Палитра команд**.
   - Выберите **Q#: Установка шаблонов проектов командной строки**
   - Через несколько секунд должно появиться всплывающее окно с подтверждением успешной установки шаблонов проектов.
