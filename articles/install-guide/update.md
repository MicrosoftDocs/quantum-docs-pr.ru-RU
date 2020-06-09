---
title: Обновление пакета средств разработки такта (КДК)
description: 'Описывает, как обновить проекты Q # и Microsoft Quantum Development Kit до текущей версии.'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: 89db1a671767b0cc083a251918bbeeed2b39b883
ms.sourcegitcommit: c8ebc5d7d8581444754f5d7bfaca2f25601f1b14
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2020
ms.locfileid: "84578187"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a>Обновление Microsoft Quantum Development Kit (КДК)

Узнайте, как обновить Microsoft Quantum Development Kit (КДК) до последней версии.

В этой статье предполагается, что у вас уже установлен КДК. Если вы устанавливаете в первый раз, обратитесь к [руководству по установке](xref:microsoft.quantum.install).

Мы рекомендуем поддерживать последние версии КДК в актуальном состоянии. Следуйте этому руководству по обновлению, чтобы выполнить обновление до последней версии КДК. Процесс состоит из двух частей:
1. Обновление существующих файлов Q # и проектов для согласования кода с любым обновленным синтаксисом.
2. Обновление самого КДК для выбранной среды разработки.

## <a name="updating-q-projects"></a>Обновление проектов Q # 

Независимо от того, используете ли вы C# или Python для размещения операций Q #, следуйте этим инструкциям, чтобы обновить проекты Q #.

1. Сначала убедитесь, что у вас установлена последняя версия [пакет SDK для .NET Core 3,1](https://dotnet.microsoft.com/download). В командной строке выполните следующую команду:

    ```dotnetcli
    dotnet --version
    ```

    Убедитесь, что выходные данные имеют значение `3.1.100` или выше. В противном случае установите [последнюю версию](https://dotnet.microsoft.com/download) и снова проверьте. Затем следуйте приведенным ниже инструкциям в зависимости от настроек (Visual Studio, Visual Studio Code или непосредственно в командной строке).

### <a name="update-q-projects-in-visual-studio"></a>Обновление проектов Q # в Visual Studio
 
1. Обновление до последней версии Visual Studio 2019. инструкции см. [здесь](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) .
2. Откройте решение в Visual Studio.
3. В меню выберите **Сборка**  ->  **Очистить решение**.
4. В каждом из CSPROJ-файлов обновите целевую платформу до `netcoreapp3.1` (или, `netstandard2.1` если это проект библиотеки).
    То есть измените строки формы:

    ```xml
    <TargetFramework>netcoreapp3.1</TargetFramework>
    ```

    Дополнительные сведения об указании целевых платформ можно найти [здесь](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).

5. В каждом из файлов CSPROJ задайте для пакета SDK значение `Microsoft.Quantum.Sdk` , как указано в строке ниже. Обратите внимание, что номер версии должен быть последним доступным, и его можно определить, просмотрев [заметки о выпуске](https://docs.microsoft.com/quantum/relnotes/).

    ```xml
    <Project Sdk="Microsoft.Quantum.Sdk/0.11.2006.207">
    ```

6. Сохраните и закройте все файлы в решении.

7. Выберите **инструменты**  ->  **Командная строка**  ->  **Командная строка разработчика**. Кроме того, можно использовать консоль управления пакетами в Visual Studio.

8. Для каждого проекта в решении выполните следующую команду, чтобы **Удалить** этот пакет:

    ```dotnetcli
    dotnet remove [project_name].csproj package Microsoft.Quantum.Development.Kit
    ```

   Если в проектах используются любые пакеты Microsoft. тактов или Microsoft. Azure. тактов (например, Microsoft. тактов. numeric), выполните команду **Add** , чтобы обновить используемую версию.

    ```dotnetcli
    dotnet add [project_name].csproj package [package_name]
    ```

9. Закройте командную строку и выберите **Сборка**сборка  ->  **решения** (не *not* выбирайте Перестроение решения).

Теперь вы можете перейти к [обновлению расширения Visual Studio КДК](#update-visual-studio-qdk-extension).


### <a name="update-q-projects-in-visual-studio-code"></a>Обновление проектов Q # в Visual Studio Code

1. В Visual Studio Code откройте папку, содержащую обновляемый проект.
2. Выберите **терминал**  ->  **Новый терминал**.
3. Следуйте инструкциям по обновлению с помощью командной строки (непосредственно ниже).

### <a name="update-q-projects-using-the-command-line"></a>Обновление проектов Q # с помощью командной строки

1. Перейдите к папке, содержащей основной файл проекта.

2. Выполните следующую команду:

    ```dotnetcli
    dotnet clean [project_name].csproj
    ```

3. Определите текущую версию КДК. Чтобы найти его, ознакомьтесь с [заметками о выпуске](https://docs.microsoft.com/quantum/relnotes/). Версия будет иметь формат, аналогичный `0.11.2006.207` .

4. В каждом из `.csproj` файлов выполните следующие действия.

    - Обновите целевую платформу до `netcoreapp3.1` (или, `netstandard2.1` если это проект библиотеки). То есть измените строки формы:

        ```xml
        <TargetFramework>netcoreapp3.1</TargetFramework>
        ```

        Дополнительные сведения об указании целевых платформ можно найти [здесь](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).

    - Замените ссылку на пакет SDK в определении проекта. Убедитесь, что номер версии соответствует значению, определенному на **шаге 3**.

        ```xml
        <Project Sdk="Microsoft.Quantum.Sdk/0.11.2006.207">
        ```

    - Удалите ссылку на пакет `Microsoft.Quantum.Development.Kit` , если он есть, который будет указан в следующей записи:

        ```xml
        <PackageReference Include="Microsoft.Quantum.Development.Kit" Version="0.10.1910.3107" />
        ```

    - Обновите версию всех пакетов Microsoft тактов до последней выпущенной версии КДК (определяется на **шаге 3**). Эти пакеты именуются со следующими шаблонами:

        ```
        Microsoft.Quantum.*
        Microsoft.Azure.Quantum.*
        ```
    
        Ссылки на пакеты имеют следующий формат:

        ```xml
        <PackageReference Include="Microsoft.Quantum.Compiler" Version="0.11.2006.207" />
        ```

    - Сохраните обновленный файл.

    - Восстановите зависимости проекта, выполнив следующие действия.

        ```dotnetcli
        dotnet restore [project_name].csproj
        ```

4. Вернитесь к папке, содержащей основной проект, и выполните команду:

    ```dotnetcli
    dotnet build [project_name].csproj
    ```

После обновления проектов Q # следуйте приведенным ниже инструкциям, чтобы обновить саму КДК.

## <a name="updating-the-qdk"></a>Обновление КДК

Процесс обновления КДК зависит от языка и среды разработки.
Выберите среду разработки ниже.

* [Python: обновление расширения IQ](#update-iq-for-python)
* [Записные книжки Jupyter: обновление расширения IQ](#update-iq-for-jupyter-notebooks)
* [Visual Studio: обновление расширения КДК](#update-visual-studio-qdk-extension)
* [VS Code: обновление расширения КДК](#update-vs-code-qdk-extension)
* [Командная строка и C#: обновление шаблонов проектов](#c-using-the-dotnet-command-line-tool)


### <a name="update-iq-for-python"></a>Обновление IQ # для Python

1. Обновление `iqsharp` ядра 

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. Проверка `iqsharp` версии

    ```dotnetcli
    dotnet iqsharp --version
    ```

    Вы должны увидеть следующий результат.

    ```
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    Не беспокойтесь, если ваша `iqsharp` версия более высокая, она должна соответствовать [последнему выпуску](xref:microsoft.quantum.relnotes).

3. Обновление `qsharp` пакета

    ```
    pip install qsharp --upgrade
    ```

4. Проверка `qsharp` версии

    ```
    pip show qsharp
    ```

    Вы должны увидеть следующий результат.

    ```
    Name: qsharp
    Version: 0.10.1912.501
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```

5. Выполните следующую команду из расположения `.qs` файлов

    ```
    python -c "import qsharp; qsharp.reload()"
    ```

6. Теперь вы можете использовать обновленную версию КДК для запуска существующих тактовых программ.

### <a name="update-iq-for-jupyter-notebooks"></a>Обновление IQ # для записных книжек Jupyter

1. Обновление `iqsharp` ядра

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. Проверка `iqsharp` версии

    ```dotnetcli
    dotnet iqsharp --version
    ```

    Вывод приложения должен быть аналогичен приведенному ниже:

    ```
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    Не беспокойтесь, если ваша `iqsharp` версия более высокая, она должна соответствовать [последнему выпуску](xref:microsoft.quantum.relnotes).

3. Выполните следующую команду в ячейке Jupyter Notebook:

    ```
    %workspace reload
    ```

4. Теперь можно открыть имеющуюся записную книжку Jupyter и запустить ее с помощью обновленного КДК.

### <a name="update-visual-studio-qdk-extension"></a>Обновление расширения Visual Studio КДК

1. Обновление расширения Q # Visual Studio

    - Visual Studio предложит принять обновления для [расширения тактовой задержки Visual Studio](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)
    - Принять обновление

    > [!NOTE]
    > Шаблоны проектов обновляются с помощью расширения. Обновленные шаблоны применяются только к только что созданным проектам. Код для существующих проектов не обновляется при обновлении расширения.

### <a name="update-vs-code-qdk-extension"></a>Обновление расширения VS Code КДК

1. Обновление расширения тактового VS Code

    - Перезапустить VS Code
    - Перейдите на вкладку **расширения** .
    - Выберите **Microsoft Quantum Development Kit для расширения Visual Studio Code**
    - Перезагрузить расширение

2. Обновите шаблоны проекта такта:

   - Перейти к **View**  ->  **палитре команд** просмотра
   - Выбор **Q #: Установка шаблонов проектов**
   - Через несколько секунд должно появиться всплывающее окно с подтверждением успешной установки шаблонов проектов.

### <a name="c-using-the-dotnet-command-line-tool"></a>C# с помощью `dotnet` программы командной строки

1. Обновление шаблонов проектов тактов для .NET

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```
