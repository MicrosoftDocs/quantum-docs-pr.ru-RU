---
title: Разработка с помощью приложений Q# в интегрированной среде разработки
description: Сведения о том, как создать приложение Q#, запускаемое из командной строки.
author: bradben
ms.author: v-benbra
ms.date: 8/20/2020
ms.topic: quickstart
uid: microsoft.quantum.install.standalone
no-loc:
- Q#
- $$v
ms.openlocfilehash: 3e4f1e97477ecb0547b1586b1c7603c8a9954584
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844319"
---
# <a name="develop-with-no-locq-applications-in-an-ide"></a>Разработка с помощью приложений Q# в интегрированной среде разработки

Программы Q# могут выполняться самостоятельно (без драйвера) на основном языке, например C#, F# или Python. Приложения Q# можно разрабатывать в Visual Studio Code (VS Code), Visual Studio, Visual Studio Codespaces либо с помощью любого редактора или IDE, а затем запускать их из консоли .NET. 

## <a name="prerequisites-for-all-environments"></a>Необходимые условия для всех сред

- [Пакет SDK для .NET Core 3.1 или более поздней версии](https://www.microsoft.com/net/download)

## <a name="installation"></a>Установка

Вы можете создавать приложения Q# в любой интегрированной среде разработки. Но мы рекомендуем использовать для локальной разработки приложений Q# интегрированную среду разработки Visual Studio Code (VS Code) или Visual Studio. Для разработки в облаке с помощью веб-браузера мы рекомендуем использовать Visual Studio Codespaces. При разработке в таких средах вам доступны возможности расширения QDK, такие как предупреждения, выделение синтаксиса, шаблоны проектов и пр. 

### <a name="to-configure-for-vs-code"></a>Чтобы настроить VS Code, сделайте следующее:

1. Скачайте и установите [VS Code](https://code.visualstudio.com/download) (Windows, Linux и Mac).
2. Установите [Microsoft QDK для VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).

### <a name="to-configure-for-visual-studio"></a>Чтобы настроить Visual Studio, сделайте следующее:

1. Скачайте и установите [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 или более новой версии с включенной рабочей нагрузкой кроссплатформенной разработки .NET Core.
2. Скачайте и установите [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).

### <a name="to-configure-for-another-environment"></a>Чтобы настроить другую среду, сделайте следующее: 

1. В командной строке введите следующую команду:

```dotnetcli
dotnet new -i Microsoft.Quantum.ProjectTemplates
```

### <a name="to-configure-for-visual-studio-codespaces"></a>Чтобы настроить Visual Studio Codespaces, сделайте следующее:

1. Создайте [учетную запись Azure](https://azure.microsoft.com/free/).
2. Создайте среду Codespaces. Выполните инструкции из [этого краткого руководства](https://docs.microsoft.com/visualstudio/codespaces/quickstarts/browser). При создании Codespaces рекомендуется ввести `microsoft/Quantum` в поле Git Repository (Репозиторий Git), чтобы загрузить параметры, связанные с QDK.
3. Теперь вы можете запустить новую среду и начать разработку в браузере с помощью [облачной интегрированной среды разработки Visual Studio Codespaces](https://online.visualstudio.com/environments). Кроме того, можно использовать локальную установку VS Code и использовать Codespaces в качестве [удаленной среды](https://docs.microsoft.com/visualstudio/online/how-to/vscode).

## <a name="develop-with-no-locq"></a>Разработка на Q#

Следуйте инструкциям на вкладке для вашей среды разработки.

### <a name="vs-code"></a>[Код VS](#tab/tabid-vscode)

Чтобы создать новый проект, выполните следующие действия.

1. Щелкните **Представление** -> **Палитра команд** и выберите **Q#: создать проект**.
2. Щелкните **Standalone console application** (Автономное консольное приложение).
3. Перейдите к расположению, чтобы сохранить проект. Введите имя проекта и щелкните **Создать проект**.
4. После успешного создания проекта нажмите **Открыть новый проект...** в правом нижнем углу.

Проверьте проект. Вы увидите исходный файл с именем `Program.qs`, который представляет собой программу Q#, определяющую простую операцию вывода сообщения в консоль.

Чтобы запустить приложение, выполните следующие действия:

1. Щелкните **Терминал** -> **Создать терминал**.
2. В командной строке терминала введите `dotnet run`.
3. В окне консоли `Hello quantum world!` должен отобразиться следующий текст.

> [!NOTE]
> В настоящее время рабочие области с несколькими корневыми папками не поддерживаются в расширении Q# для VS Code. Если в одной рабочей области VS Code несколько проектов, все проекты нужно разместить в одной корневой папке.

### <a name="visual-studio"></a>[Visual Studio](#tab/tabid-vs)

Проверьте установку Visual Studio, создав приложение `Hello World` на Q#.

Чтобы создать приложение на Q#:

1. Откройте Visual Studio и щелкните **Файл** -> **Создать** -> **Проект**.
2. Введите `Q#` в поле поиска, выберите **Q# Application** (Приложение Q#) и щелкните **Далее**.
3. Введите имя и расположение приложения и щелкните **Создать**.


Проверьте проект. Вы увидите исходный файл с именем `Program.qs`, который представляет собой программу Q#, определяющую простую операцию вывода сообщения в консоль.

Чтобы запустить приложение, выполните следующие действия:

1. Выберите **Отладка** -> **Запустить без отладки**.
2. В окне консоли должен отобразиться текст `Hello quantum world!`.

> [!NOTE]
> Если в одном решении Visual Studio несколько проектов, все включенные в него проекты нужно разместить в той же папке, что и решение, или в одной из вложенных в нее папок.  

### <a name="other-editors-with-the-command-prompt"></a>[Другие редакторы с командной строкой](#tab/tabid-cmdline)

Проверьте установку, создав на Q# приложение `Hello World`.

1. Создайте новое приложение:

    ```dotnetcli
    dotnet new console -lang Q# -o runSayHello
    ```

1. Перейдите в каталог приложения:

    ```dotnetcli
    cd runSayHello
    ```

    Этот каталог теперь должен содержать файл `Program.qs`, который представляет собой программу Q#, определяющую простую операцию вывода сообщения в консоль. Вы можете изменить этот шаблон с помощью текстового редактора и перезаписать его собственными квантовыми приложениями. 

1. Запустите программу.

    ```dotnetcli
    dotnet run
    ```

1. На экране должен появиться следующий текст: `Hello quantum world!`.

***

## <a name="next-steps"></a>Дальнейшие действия

После установки Quantum Development Kit в предпочитаемой среде вы можете написать и запустить [первую квантовую программу](xref:microsoft.quantum.quickstarts.qrng).
