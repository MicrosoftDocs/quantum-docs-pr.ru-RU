---
title: Использование дополнительных Q# библиотек
description: Узнайте, как добавить дополнительные Q# библиотеки в приложения такта.
author: cgranade
ms.author: chgranad
ms.date: 06/30/2020
ms.topic: article
uid: microsoft.quantum.libraries.using
no-loc:
- Q#
- $$v
ms.openlocfilehash: c558e25bf0d906ba6480cd7c41d3ece4ea97c2d1
ms.sourcegitcommit: 75c4edc7c410cc63dc8352e2a5bef44b433ed188
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/25/2020
ms.locfileid: "88863090"
---
# <a name="using-additional-no-locq-libraries"></a>Использование дополнительных Q# библиотек

Пакет средств разработки тактов предоставляет дополнительные функции, зависящие от домена, с помощью _пакетов NuGet_ , которые можно добавить в Q# проекты.

| Q# Библиотечная  | Пакет NuGet | Примечания |
|---------|---------|--------|
| [Q# Стандартная библиотека](xref:microsoft.quantum.libraries.standard.intro) | [**Microsoft. тактов. Standard**](https://www.nuget.org/packages/Microsoft.Quantum.Standard) | Включено по умолчанию |
| [Библиотека квантовой химии](xref:microsoft.quantum.chemistry.concepts.intro) | [**Microsoft.Quantum.Chemistry**](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) | |
| [Квантовая библиотека числовых значений](xref:microsoft.quantum.numerics.intro) | [**Значения Microsoft. тактов. numeric**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) | |
| [Библиотека квантового машинного обучения](xref:microsoft.quantum.libraries.machine-learning.intro) | [**Microsoft.Quantum.MachineLearning**](https://www.nuget.org/packages/Microsoft.Quantum.MachineLearning) | |

После установки пакета средств разработки такта для использования с предпочитаемой средой и языком узла можно легко добавлять библиотеки в отдельные Q# проекты без дальнейшей установки.

> [!NOTE]
> Некоторые Q# библиотеки могут хорошо работать с дополнительными инструментами, которые работают вместе Q# с программами или интегрируются с ведущими приложениями.
> Например, инструкции по [установке библиотеки химия](xref:microsoft.quantum.chemistry.concepts.installation) описывают, как использовать [пакет **Microsoft. такт. Химия** ](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) вместе с платформой вычислительной химия нвчем и как установить `qdk-chem` программы командной строки для работы с данными такта химия.

## <a name="no-locq-applications-or-net-interopability"></a>[Q# взаимодействие приложений или .NET](#tab/tabid-csproj)

**Командная строка или Visual Studio Code:** Используя командную строку самостоятельно или в Visual Studio Code, можно использовать `dotnet` команду, чтобы добавить ссылку на пакет NuGet в проект.
Например, чтобы добавить пакет [**Microsoft. такт. Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) , выполните следующую команду:

```dotnetcli
dotnet add package Microsoft.Quantum.Numerics
```

**Visual Studio:** При использовании Visual Studio 2019 или более поздней версии можно добавить дополнительные Q# пакеты с помощью диспетчера пакетов NuGet.
Чтобы загрузить пакет, выполните следующие действия. 
1. Откройте проект в Visual Studio и выберите **Управление пакетами NuGet...** в меню **проект** .

2. Нажмите кнопку **Обзор**, выберите **включить предварительный выпуск** и выполните поиск по имени пакета «Microsoft. тактов. numeric». В этом списке будут перечислены пакеты, доступные для загрузки.

3. Наведите указатель мыши на **Microsoft. тактов. Numerics** и щелкните стрелку вниз справа от номера версии, чтобы установить пакет числовых данных.

Дополнительные сведения см. в разделе [Путеводитель по пользовательскому интерфейсу диспетчера пакетов](https://docs.microsoft.com/nuget/tools/package-manager-ui).

Кроме того, можно использовать консоль диспетчера пакетов, чтобы добавить библиотеку числовых библиотек в проект с помощью интерфейса командной строки.

![Использование консоли диспетчера пакетов из командной строки](~/media/vs2017-nuget-console-menu.png)

В консоли диспетчера пакетов выполните следующую команду:

```
Install-Package Microsoft.Quantum.Numerics
```

Дополнительные сведения см. в разделе [руководств по консоли диспетчера пакетов](https://docs.microsoft.com/nuget/tools/package-manager-console).

## <a name="ino-locq-notebooks"></a>[Q#Записные книжки](#tab/tabid-notebook)

Можно сделать дополнительные пакеты доступными для использования в Q# записной книжке I с помощью [ `%package` команды Magic](xref:microsoft.quantum.iqsharp.magic-ref.package).
Например, чтобы добавить пакет [**Microsoft. такт. Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) для использования в Q# записной книжке I, выполните следующую команду в ячейке записной книжки:

```
%package Microsoft.Quantum.Numerics
```

После этой команды пакет будет доступен для любых ячеек в записной книжке.
Чтобы сделать пакет доступным из Q# кода в текущей рабочей области, перезагрузите рабочую область после добавления пакета:

```
%workspace reload
```

## <a name="python-interoperability"></a>[Совместимость c Python](#tab/tabid-python)


Можно сделать дополнительные пакеты доступными для использования в основной программе Python с помощью [`qsharp.packages.add`](https://docs.microsoft.com/python/qsharp/qsharp.packages.packages) метода.
Например, чтобы добавить пакет [**Microsoft. такт. Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) для использования в Q# записной книжке I, выполните следующий код Python:

```python
import qsharp
qsharp.packages.add("Microsoft.Quantum.Numerics")
```

После этой команды пакет будет предоставляться для любого Q# кода, скомпилированного с помощью `qsharp.compile` .
Чтобы сделать пакет доступным из Q# кода в текущей рабочей области, перезагрузите рабочую область после добавления пакета:

```python
qsharp.reload()
```

***
