---
title: Разработка на Q# + C#
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.cs
ms.openlocfilehash: 5bcb036b0b32e64d43f90e9a068d9dcc237890ba
ms.sourcegitcommit: db23885adb7ff76cbf8bd1160d401a4f0471e549
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/01/2020
ms.locfileid: "82680160"
---
# <a name="using-q-with-c-and-f"></a>Использование Q # с C\# и F\#

Функция Q # разработана для корректного воспроизведения на языках .NET, таких как C# и F #.
В этом руководство мы покажем, как использовать Q # с основной программой, написанной на языке .NET.

## <a name="prerequisites"></a>Предварительные требования

- Установите пакет средств разработки такта [для использования с проектами командной строки Q #](xref:microsoft.quantum.install.standalone).

## <a name="creating-a-q-library-and-a-net-host"></a>Создание библиотеки Q # и узла .NET

Первым шагом является создание проектов для библиотеки Q # и для узла .NET, который будет вызывать операции и функции, определенные в библиотеке Q #.

### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

- Создать новую библиотеку Q #
  - Переход к **файлу** -> **Новый** -> **проект**
  - Введите "Q #" в поле поиска
  - Выбор **Q # Library**
  - Нажмите кнопку **Далее** .
  - Выберите имя и расположение для библиотеки
  - Убедитесь, что флажок "размещение проекта и решения в одном каталоге" **снят**
  - Выберите **создать** .
- Создание основной программы на C# или F #
  - Последовательно выберите пункты **файл** → **создать** → **проект** .
  - Выберите "консольное приложение (.NET Core") "для C# или F #
  - Нажмите кнопку **Далее** .
  - В разделе *решение*выберите "добавить в решение".
  - Выберите имя для своей основной программы
  - Выберите **создать** .

### <a name="visual-studio-code-or-command-line"></a>[Visual Studio Code или Командная строка](#tab/tabid-cmdline)

- Создать новую библиотеку Q #

  ```dotnetcli
  dotnet new classlib -lang Q# -o quantum
  ```

- Создание нового проекта консоли C# или F #

  ```dotnetcli
  dotnet new console -lang C# -o host  
  ```

- Добавление библиотеки Q # в качестве ссылки из основной программы

  ```dotnetcli
  cd host
  dotnet add reference ../quantum/quantum.csproj
  ```

- Используемых Создание решения для обоих проектов

  ```dotnetcli
  dotnet new sln -n quantum-dotnet
  dotnet sln quantum-dotnet.sln add ./quantum/quantum.csproj
  dotnet sln quantum-dotnet.sln add ./host/host.csproj
  ```

***

## <a name="calling-into-q-from-net"></a>Вызов в Q # из .NET

После выполнения приведенных выше инструкций Вы можете обращаться к Q # из консольного приложения .NET.
Компилятор Q # будет создавать классы .NET для каждой операции и функции Q #, которые позволяют запускать в симуляторе программы-такты.

Например, [Пример взаимодействия с .NET](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet) включает в себя следующий пример операции Q #:

:::code language="qsharp" source="~/quantum/samples/interoperability/dotnet/qsharp/Operations.qs" range="67-75":::

Чтобы вызвать эту операцию из .NET в имитаторе такта, можно использовать `Run` метод класса `RunAlgorithm` .NET, созданный компилятором Q #:

### <a name="c"></a>[C#](#tab/tabid-csharp)

:::code language="csharp" source="~/quantum/samples/interoperability/dotnet/csharp/Host.cs" range="4-":::

### <a name="f"></a>[F#](#tab/tabid-fsharp)

:::code language="fsharp" source="~/quantum/samples/interoperability/dotnet/fsharp/Host.fs" range="4-":::

***
    
## <a name="whats-next"></a>Что дальше?

Теперь, когда у вас есть пакет средств разработки такта для программ командной строки Q # и для взаимодействия с .NET, вы можете написать и запустить [первую тактовую программу](xref:microsoft.quantum.write-program).
