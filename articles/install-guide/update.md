---
title: Сведения об обновлении Microsoft Quantum Development Kit (КДК)
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: ebf1f15d65a12c921cd3f04e4111d463d1060f8e
ms.sourcegitcommit: c93fea5980d1d46fbda1e7c7153831b9337134bf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2019
ms.locfileid: "73463282"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a>Обновление Microsoft Quantum Development Kit (КДК)

Узнайте, как обновить Microsoft Quantum Development Kit (КДК) до последней версии.

В этой статье предполагается, что у вас уже установлен КДК. Если вы устанавливаете в первый раз, обратитесь к [руководству по установке](xref:microsoft.quantum.install).


## <a name="updating-q-projects"></a>Обновление проектов Q # 

1. Сначала установите последнюю версию [пакет SDK для .NET Core 3,0](https://dotnet.microsoft.com/download) и выполните в командной строке следующую команду:
```bash
dotnet --version
```
 Убедитесь, что для выходных данных задано значение 3.0.100 или выше, а затем следуйте приведенным ниже инструкциям в зависимости от настроек.

### <a name="in-visual-studio"></a>В Visual Studio
 
 1. Обновление до последней версии Visual Studio 2019. инструкции см. [здесь](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) .
 2. Открытие решения в Visual Studio
 3. В меню выберите Сборка > Очистить решение. 
 4. [Обновите целевую платформу](https://docs.microsoft.com/visualstudio/ide/visual-studio-multi-targeting-overview?view=vs-2019#change-the-target-framework) в каждом из CSPROJ-файлов до версии netcoreapp 3.0 (или netstandard 2.1, если это проект библиотеки).
 5. Сохранение и закрытие всех файлов в решении
 6. Выберите Инструменты > командной строки > Командная строка разработчика
 7. Для каждого проекта в решении выполните следующую команду:
 ```bash
 dotnet add [project_name].csproj package Microsoft.Quantum.Development.Kit
 ```
Если в проектах используются другие пакеты Microsoft. тактов, выполните эту команду. 
 8. Закройте командную строку и выберите Сборка > сборка решения (не *выбирайте* Перестроение решения, так как перестроение первоначально завершится сбоем).

### <a name="in-visual-studio-code"></a>В Visual Studio Code

1. В Visual Studio Code откройте папку, содержащую обновляемый проект.
1. Выберите терминал > новый терминал
1. Следуйте инструкциям по обновлению с помощью командной строки.

### <a name="using-the-command-line"></a>Использование командной строки

1. Перейдите к папке, содержащей файл проекта
2. Выполните следующую команду:
```bash
dotnet clean [project_name].csproj
```

3. [Обновите целевую платформу](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks) в каждом из CSPROJ-файлов до версии netcoreapp 3.0 (или netstandard 2.1, если это проект библиотеки).
4. Выполните следующую команду:
```bash
dotnet add package Microsoft.Quantum.Development.Kit
```
Если в проекте используются другие пакеты Microsoft. тактов, выполните эту команду.

5. Сохранить и закрыть все файлы
6. Повторите 1-4 для каждой зависимости проекта, а затем вернитесь к папке, содержащей основной проект, и выполните команду:
```bash
dotnet build [project_name].csproj
```

## <a name="update-iq-for-python"></a>Обновление IQ # для Python

1. Обновление ядра `iqsharp`

    ```bash
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. Проверка версии `iqsharp`

    ```bash
    dotnet iqsharp --version
    ```

    Вы должны увидеть следующий результат.

    ```bash
    iqsharp: 0.10.1911.307
    Jupyter Core: 1.2.20112.0
    ```

1. Обновление пакета `qsharp`

    ```bash
    pip install qsharp --upgrade
    ```

1. Проверка версии `qsharp`

    ```bash
    pip show qsharp
    ```

    Вы должны увидеть следующий результат.

    ```bash
    Name: qsharp
    Version: 0.10.1911.307
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```
1. Выполните следующую команду из расположения файлов `.qs`
    ```bash
    python -c "import qsharp; qsharp.reload()"
    ```

1. Теперь вы можете использовать обновленную версию КДК для запуска существующих тактовых программ.

## <a name="update-iq-for-jupyter-notebooks"></a>Обновление IQ # для записных книжек Jupyter

1. Обновление ядра `iqsharp`

    ```bash
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. Проверка версии `iqsharp`

    ```bash
    dotnet iqsharp --version
    ```

    Вы должны увидеть следующий результат.

    ```bash
    iqsharp: 0.10.1911.307
    Jupyter Core: 1.2.20112.0
    ```
1. Выполните следующую команду в ячейке Jupyter Notebook:
    ```
    %workspace reload
    ```

1. Теперь можно открыть имеющуюся записную книжку Jupyter и запустить ее с помощью обновленного КДК.

## <a name="update-visual-studio-qdk-extension"></a>Обновление расширения Visual Studio КДК

1. Обновление расширения Q # Visual Studio

    - Visual Studio предложит принять обновления для [расширения тактовой задержки Visual Studio](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)
    - Принять обновление

    > [!NOTE]
    > Шаблоны проектов обновляются с помощью расширения. Обновленные шаблоны применяются только к только что созданным проектам. Код для существующих проектов не обновляется при обновлении расширения.

## <a name="update-vs-code-qdk-extension"></a>Обновление расширения VS Code КДК

1. Обновление расширения тактового VS Code

    - Перезапустить VS Code
    - Перейдите на вкладку **расширения** .
    - Выберите **Microsoft Quantum Development Kit для расширения Visual Studio Code**
    - Перезагрузить расширение

1. Обновите шаблоны проекта такта:

   - Выберите **Представление** -> **Палитра команд**.
   - Выбор **Q #: Установка шаблонов проектов**

## <a name="c-using-the-dotnet-command-line-tool"></a>C#с помощью средства командной строки `dotnet`

1. Обновление шаблонов проектов тактов для .NET

    ```bash
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

## <a name="whats-next"></a>Что дальше?

После обновления пакета средств разработки тактов в предпочтительной среде можно продолжить разработку и запуск тактовых программ. Если вы еще не написали программу, вы можете начать работу с [первой тактовой программой](xref:microsoft.quantum.write-program).
