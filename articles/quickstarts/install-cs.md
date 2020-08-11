---
title: Разработка на Q# в среде .NET
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.cs
no-loc:
- Q#
- $$v
ms.openlocfilehash: 13d73bdf0287941c89e03ba63869095e5fca4e70
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2020
ms.locfileid: "87867562"
---
# <a name="develop-with-no-locq-and-net"></a>Разработка на Q# в среде .NET

Язык Q# прекрасно сочетается с языками .NET, например C# и F#.
В этом руководстве мы покажем, как использовать Q# с ведущей программой, написанной на языке .NET.

Сначала мы создадим приложение Q# и ведущую программу .NET, а затем покажем, как вызвать код Q# из ведущей программы.

## <a name="prerequisites"></a>Предварительные требования

- Установите Quantum Development Kit [для использования с проектами командной строки Q#](xref:microsoft.quantum.install.standalone).

## <a name="creating-a-no-locq-library-and-a-net-host"></a>Создание библиотеки Q# и ведущей программы .NET

Первый шаг — создать проекты для библиотеки Q# и ведущей программы .NET, которая будет вызывать операции и функции, определенные в библиотеке Q#.

Следуйте инструкциям на вкладке для вашей среды разработки.
Если вы используете редактор, отличный от Visual Studio или VS Code, просто выполните действия из командной строки.

### <a name="visual-studio-code-or-command-line"></a>[Visual Studio Code или командная строка](#tab/tabid-cmdline)

- Создайте новую библиотеку Q#:

  ```dotnetcli
  dotnet new classlib -lang Q# -o quantum
  ```

- Создайте новый консольный проект C# или F#.

  ```dotnetcli
  dotnet new console -lang C# -o host  
  ```

- Добавьте библиотеку Q# в качестве ссылки из ведущей программы:

  ```dotnetcli
  cd host
  dotnet add reference ../quantum/quantum.csproj
  ```

- (Не обязательно.) Создайте решения для обоих проектов.

  ```dotnetcli
  dotnet new sln -n quantum-dotnet
  dotnet sln quantum-dotnet.sln add ./quantum/quantum.csproj
  dotnet sln quantum-dotnet.sln add ./host/host.csproj
  ```

### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

- Создайте новую библиотеку Q#:
  - Выберите **Файл** -> **Создать** -> **Проект**.
  - Введите "Q#"в поле поиска:
  - Выберите **библиотеку Q#** :
  - Щелкните **Далее**.
  - Выберите имя и расположение библиотеки.
  - Убедитесь, что флажок "Поместить решение и проект в одной папке" **снят**.
  - Нажмите кнопку **Создать**
- Создайте основную программу на C# или F#.
  - Последовательно выберите **Файл** → **Создать** → **Проект**.
  - Выберите "Консольное приложение (.NET Core)" для C# или F#.
  - Щелкните **Далее**.
  - В разделе *Решение* выберите "Добавить в решение".
  - Выберите имя основной программы.
  - Нажмите кнопку **Создать**

***

## <a name="calling-into-no-locq-from-net"></a>Вызов Q# из .NET

После выполнения приведенных выше инструкций по настройке проекта вы можете вызвать Q# из консольного приложения .NET.
Компилятор Q# будет создавать классы .NET для каждой операции и функции Q#, что позволит запускать в симуляторе квантовые программы.

[Пример взаимодействия с .NET](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet) содержит следующий пример операции Q#:

:::code language="qsharp" source="~/quantum/samples/interoperability/dotnet/qsharp/Operations.qs" range="67-75":::

Чтобы вызвать эту операцию из .NET в квантовом симуляторе, можно использовать метод `Run` класса .NET `RunAlgorithm`, созданный компилятором Q#:

### <a name="c"></a>[C#](#tab/tabid-csharp)

:::code language="csharp" source="~/quantum/samples/interoperability/dotnet/csharp/Host.cs" range="4-":::

### <a name="f"></a>[F#](#tab/tabid-fsharp)

:::code language="fsharp" source="~/quantum/samples/interoperability/dotnet/fsharp/Host.fs" range="4-":::

***
    
## <a name="next-steps"></a>Дальнейшие действия

Теперь, когда у вас настроен пакет Quantum Development Kit для программ командной строки Q# и для взаимодействия с .NET, вы можете написать и запустить [свою первую квантовую программу](xref:microsoft.quantum.quickstarts.qrng).
