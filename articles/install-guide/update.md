---
title: Сведения об обновлении Microsoft Quantum Development Kit (КДК)
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: ed2a90749bbe245dde97424fc3191682f995d85b
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "76819745"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a>Обновление Microsoft Quantum Development Kit (КДК)

Узнайте, как обновить Microsoft Quantum Development Kit (КДК) до последней версии.

В этой статье предполагается, что у вас уже установлен КДК. Если вы устанавливаете в первый раз, обратитесь к [руководству по установке](xref:microsoft.quantum.install).

Мы рекомендуем поддерживать последние версии КДК в актуальном состоянии. Следуйте этому руководству по обновлению, чтобы выполнить обновление до последней версии КДК. Процесс состоит из двух частей:
1. Обновление существующих файлов Q # и проектов для согласования кода с любым обновленным синтаксисом
2. Обновление самого КДК для выбранной среды разработки 

## <a name="updating-q-projects"></a>Обновление проектов Q # 

Независимо от того, используете C# ли вы или Python для размещения операций q #, следуйте этим инструкциям, чтобы обновить проекты q #.

1. Сначала убедитесь, что у вас установлена последняя версия [пакет SDK для .NET Core 3,1](https://dotnet.microsoft.com/download). В командной строке выполните следующую команду:
    ```bash
    dotnet --version
    ```
Убедитесь, что выходные данные имеют `3.1.100` или выше. В противном случае установите [последнюю версию](https://dotnet.microsoft.com/download) и снова проверьте. Затем следуйте приведенным ниже инструкциям в зависимости от настроек (Visual Studio, Visual Studio Code или непосредственно в командной строке).

### <a name="update-q-projects-in-visual-studio"></a>Обновление проектов Q # в Visual Studio
 
1. Обновление до последней версии Visual Studio 2019. инструкции см. [здесь](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) .
2. Открытие решения в Visual Studio
3. В меню выберите **сборка** -> **Очистить решение** .
4. В каждом из CSPROJ-файлов обновите целевую платформу до `netcoreapp3.0` (или `netstandard2.1`, если это проект библиотеки).
    То есть измените строки формы:
    ```xml
    <TargetFramework>netcoreapp3.0</TargetFramework>
    ```
    Дополнительные сведения об указании целевых платформ можно найти [здесь](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).
5. Сохранение и закрытие всех файлов в решении
6. Выберите **инструменты** -> **командной строки** -> **Командная строка разработчика**
7. Для каждого проекта в решении выполните следующую команду:
    ```bash
    dotnet add [project_name].csproj package Microsoft.Quantum.Development.Kit
    ```
    Если в проектах используются любые другие пакеты Microsoft. тактов (например, Microsoft. тактов. numeric), выполните для них команду.
8. Закройте командную строку и выберите **сборка** -> **сборка решения** (не *выбирайте* Перестроение решения, так как перестроение первоначально завершится сбоем).

Теперь вы можете перейти к [обновлению расширения Visual Studio КДК](#update-visual-studio-qdk-extension).


### <a name="update-q-projects-in-visual-studio-code"></a>Обновление проектов Q # в Visual Studio Code

1. В Visual Studio Code откройте папку, содержащую обновляемый проект.
2. Выберите **терминал** -> **Новый терминал**
3. Следуйте инструкциям по обновлению с помощью командной строки (непосредственно ниже).

### <a name="update-q-projects-using-the-command-line"></a>Обновление проектов Q # с помощью командной строки

1. Перейдите к папке, содержащей файл проекта
2. Выполните следующую команду:
    ```bash
    dotnet clean [project_name].csproj
    ```

3. В каждом из CSPROJ-файлов обновите целевую платформу до `netcoreapp3.0` (или `netstandard2.1`, если это проект библиотеки).
    То есть измените строки формы:
    ```xml
    <TargetFramework>netcoreapp3.0</TargetFramework>
    ```
    Дополнительные сведения об указании целевых платформ можно найти [здесь](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).
4. Выполните следующую команду:
    ```bash
    dotnet add package Microsoft.Quantum.Development.Kit
    ```
    Если в проекте используются любые другие пакеты Microsoft. тактов (например, Microsoft. тактов. numeric), выполните для них команду.
5. Сохраните и закройте все файлы.
6. Повторите 1-4 для каждой зависимости проекта, а затем вернитесь к папке, содержащей основной проект, и выполните команду:
    ```bash
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

1. Обновление ядра `iqsharp` 

    ```bash
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. Проверка версии `iqsharp`

    ```bash
    dotnet iqsharp --version
    ```

    Вы должны увидеть следующий результат.

    ```bash
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```
    Не беспокойтесь, если ваша версия `iqsharp` более высокая, она должна соответствовать [последнему выпуску](xref:microsoft.quantum.relnotes).

3. Обновление пакета `qsharp`

    ```bash
    pip install qsharp --upgrade
    ```

4. Проверка версии `qsharp`

    ```bash
    pip show qsharp
    ```

    Вы должны увидеть следующий результат.

    ```bash
    Name: qsharp
    Version: 0.10.1912.501
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```
5. Выполните следующую команду из расположения файлов `.qs`
    ```bash
    python -c "import qsharp; qsharp.reload()"
    ```

6. Теперь вы можете использовать обновленную версию КДК для запуска существующих тактовых программ.

### <a name="update-iq-for-jupyter-notebooks"></a>Обновление IQ # для записных книжек Jupyter

1. Обновление ядра `iqsharp`

    ```bash
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. Проверка версии `iqsharp`

    ```bash
    dotnet iqsharp --version
    ```

    Вывод приложения должен быть аналогичен приведенному ниже:

    ```bash
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```
    Не беспокойтесь, если ваша версия `iqsharp` более высокая, она должна соответствовать [последнему выпуску](xref:microsoft.quantum.relnotes).

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

   - Выберите **Представление** -> **Палитра команд**.
   - Выбор **Q #: Установка шаблонов проектов**
   - Через несколько секунд должно появиться всплывающее окно с подтверждением успешной установки шаблонов проектов.

### <a name="c-using-the-dotnet-command-line-tool"></a>C#с помощью средства командной строки `dotnet`

1. Обновление шаблонов проектов тактов для .NET

    ```bash
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

## <a name="whats-next"></a>Что дальше?

После обновления пакета средств разработки тактов в предпочтительной среде можно продолжить разработку и запуск тактовых программ. Если вы еще не написали программу, вы можете начать работу с [первой тактовой программой](xref:microsoft.quantum.write-program).
