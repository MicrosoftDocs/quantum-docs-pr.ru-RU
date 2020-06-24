---
title: Библиотека цифровых чисел (Майкрософт) — Установка и проверка
description: Узнайте, как добавить библиотеку Microsoft тактовых чисел в установку Visual Studio 2019 или более поздней версии.
author: thomashaener
ms.author: thhaner
ms.date: 05/14/2019
ms.topic: article
uid: microsoft.quantum.numerics.installation
ms.openlocfilehash: 60ee91a552fad5becf8eda437406b6e0dfba0eb4
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2020
ms.locfileid: "85276128"
---
# <a name="numerics-library-installation-and-validation"></a>Установка и проверка библиотеки числовых значений

Пакет средств разработки тактов обеспечивает поддержку числовых функций с помощью [`Microsoft.Quantum.Numerics`](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) пакета NuGet.

**>Visual Studio = 2019:** Если вы используете Visual Studio 2019 или более поздней версии, можно добавить пакет числовых пакетов с помощью диспетчера пакетов NuGet.
Для этого выберите "Управление пакетами NuGet...". из пункта меню "проект" в Visual Studio.

На вкладке Обзор выполните поиск по имени пакета "Microsoft. тактов. Numeric".

> [!NOTE]
> Обязательно пометка "включить предварительные выпуски"

В этом списке будут перечислены пакеты, доступные для загрузки.
При наведении указателя мыши на "Microsoft. тактов. Numerics" отображается стрелка вниз справа от номера версии.
Щелкните стрелку, чтобы установить пакет "числовые пакеты".

Дополнительные сведения см. в разделе [Путеводитель по пользовательскому интерфейсу диспетчера пакетов](https://docs.microsoft.com/nuget/tools/package-manager-ui).

Кроме того, можно использовать консоль диспетчера пакетов, чтобы добавить библиотеку числовых библиотек в проект с помощью интерфейса командной строки.

![Использование консоли диспетчера пакетов из командной строки](~/media/vs2017-nuget-console-menu.png)

В консоли диспетчера пакетов выполните следующую команду:

```
Install-Package Microsoft.Quantum.Numerics
```

Дополнительные сведения см. в разделе [руководств по консоли диспетчера пакетов](https://docs.microsoft.com/nuget/tools/package-manager-console).

**Командная строка или Visual Studio Code:** Используя командную строку самостоятельно или в Visual Studio Code, можно `dotnet` Добавить ссылку на пакет NuGet в проект с помощью команды.

```dotnetcli
dotnet add package Microsoft.Quantum.Numerics
```


## <a name="verifying-your-installation"></a>Проверка установки

Как и в остальной части пакета средств разработки тактов, Библиотека числовых данных поставляется с примерами, которые помогут быстро приступить к работе.
Чтобы проверить установку с помощью этих примеров, выполните клонирование [основного репозитория образцов](https://github.com/Microsoft/Quantum) и запустите один из примеров.

Чтобы запустить пример, выполните [`CustomModAdd`](https://github.com/microsoft/Quantum/tree/master/samples/numerics/CustomModAdd) следующие действия.

```bash
git clone https://github.com/Microsoft/Quantum.git
cd Quantum/samples/numerics/CustomModAdd
dotnet run
```
