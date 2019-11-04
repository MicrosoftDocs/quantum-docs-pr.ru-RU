---
title: Сведения об обновлении Microsoft Quantum Development Kit (КДК)
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: fc430a77f88878437e662c5b54507f70f3c6e020
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/30/2019
ms.locfileid: "73185857"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a>Обновление Microsoft Quantum Development Kit (КДК)

Узнайте, как обновить Microsoft Quantum Development Kit (КДК) до последней версии.

В этой статье предполагается, что у вас уже установлен КДК. Если вы устанавливаете в первый раз, обратитесь к [руководству по установке](xref:microsoft.quantum.install).

Действия по обновлению зависят от среды разработки. Выберите среду в следующих разделах.

## <a name="python"></a>Python

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
    iqsharp: 0.9.1909.3002
    Jupyter Core: 1.1.18837.0
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
    Version: 0.9.1909.3002
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```

1. Теперь вы можете использовать обновленную версию КДК для запуска существующих тактовых программ.

## <a name="jupyter-notebooks"></a>Записные книжки Jupyter

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
    iqsharp: 0.9.1909.3002
    Jupyter Core: 1.1.18837.0
    ```

1. Теперь можно открыть имеющуюся записную книжку Jupyter и запустить ее с помощью обновленного КДК.

## <a name="c-on-windows-using-visual-studio"></a>C#в Windows с помощью Visual Studio

1. Обновление расширения Q # Visual Studio

    - Visual Studio предложит принять обновления для [расширения тактовой задержки Visual Studio](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)
    - Принять обновление

    > [!NOTE]
    > Шаблоны проектов обновляются с помощью расширения. Обновленные шаблоны применяются только к только что созданным проектам. Код для существующих проектов не обновляется при обновлении расширения.

1. Обновление пакетов КДК

    - Открытие существующего приложения
    - Выберите **зависимости** в Обозреватель решений
    - Выберите **Управление пакетами NuGet** .
    - Обновление пакетов **Microsoft. тактов** до последней версии

1. Теперь вы можете запустить приложение с помощью последней версии КДК.

## <a name="c-using-vs-code"></a>C#с помощью VS Code

1. Обновление расширения тактового VS Code

    - Перезапустить VS Code
    - Перейдите на вкладку **расширения** .
    - Выберите **Microsoft Quantum Development Kit для расширения Visual Studio Code**
    - Перезагрузить расширение

1. Обновите шаблоны проекта такта:

   - Перейти к **просмотру** -> **палитре команд**
   - Выбор **Q #: Установка шаблонов проектов**

1. Откройте существующее приложение в VS Code

   - Изменение файла CSPROJ для добавления новых версий пакета

    ```xml
    <ItemGroup>
        <PackageReference Include="Microsoft.Quantum.Standard" Version="0.9.1909.3002" />
        <PackageReference Include="Microsoft.Quantum.Development.Kit" Version="0.9.1909.3002" />
    </ItemGroup>
    ```

    Если вы используете другие пакеты `Microsoft.Quantum`, обновите их.

1. Теперь можно запустить приложение с обновленным КДК

## <a name="c-using-the-dotnet-command-line-tool"></a>C#с помощью средства командной строки `dotnet`

1. Обновление шаблонов проектов тактов для .NET

    ```bash
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

1. Обновление и запуск существующего приложения

    - Обновление версий пакета КДК в приложении

        ```bash
        dotnet add package Microsoft.Quantum.Development.Kit
        dotnet add package Microsoft.Quantum.Standard
        ```

        Если приложение использует другие пакеты `Microsoft.Quantum`, обновите их.

    - Выполнение приложения

        ```bash
        dotnet run
        ```

    - Приложение будет запущено с новыми версиями пакетов

## <a name="whats-next"></a>Что дальше?

После обновления пакета средств разработки тактов в предпочтительной среде можно продолжить разработку и запуск тактовых программ. Если вы еще не написали программу, вы можете начать работу с [первой тактовой программой](xref:microsoft.quantum.write-program).
