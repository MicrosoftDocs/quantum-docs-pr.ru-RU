---
title: Установка и проверка библиотеки числовых значений | Документация Майкрософт
description: Установка и проверка библиотеки числовых значений
author: thomashaener
ms.author: thhaner
ms.date: 05/14/2019
ms.topic: article
uid: microsoft.quantum.numerics.installation
ms.openlocfilehash: c41bb73ea484271689eea2ca1b59ce6639dc15a7
ms.sourcegitcommit: 5094c0a60cbafdee669c8728b92df281071259b9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2020
ms.locfileid: "77036463"
---
# <a name="numerics-library-installation-and-validation"></a>Установка и проверка библиотеки числовых значений

Пакет средств разработки тактов обеспечивает поддержку числовых функций с помощью пакета NuGet [`Microsoft.Quantum.Numerics`](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) .

**Visual Studio > = 2019:** Если вы используете Visual Studio 2019 или более поздней версии, можно добавить пакет числовых пакетов с помощью диспетчера пакетов NuGet.
Для этого выберите "Управление пакетами NuGet...". из пункта меню "проект" в Visual Studio.

На вкладке Обзор выполните поиск по имени пакета "Microsoft. тактов. Numeric".

> [!NOTE]
> Обязательно пометка "включить предварительные выпуски"

В этом списке будут перечислены пакеты, доступные для загрузки.
При наведении указателя мыши на "Microsoft. тактов. Numerics" отображается стрелка вниз справа от номера версии.
Щелкните стрелку, чтобы установить пакет "числовые пакеты".

Дополнительные сведения см. в разделе [Путеводитель по пользовательскому интерфейсу диспетчера пакетов](https://docs.microsoft.com/nuget/tools/package-manager-ui).

Кроме того, можно использовать консоль диспетчера пакетов, чтобы добавить библиотеку числовых библиотек в проект с помощью интерфейса командной строки.

![](../../media/vs2017-nuget-console-menu.png)

В консоли диспетчера пакетов выполните следующую команду:

```
Install-Package Microsoft.Quantum.Numerics
```

Дополнительные сведения см. в разделе [руководств по консоли диспетчера пакетов](https://docs.microsoft.com/nuget/tools/package-manager-console).

**Командная строка или Visual Studio Code:** Используя командную строку самостоятельно или в Visual Studio Code, можно использовать команду `dotnet`, чтобы добавить ссылку на пакет NuGet в проект:

```dotnetcli
dotnet add package Microsoft.Quantum.Numerics
```


## <a name="verifying-your-installation"></a>Проверка установки

Как и в остальной части пакета средств разработки тактов, Библиотека числовых данных поставляется с примерами, которые помогут быстро приступить к работе.
Чтобы проверить установку с помощью этих примеров, выполните клонирование [основного репозитория образцов](https://github.com/Microsoft/Quantum) и запустите один из примеров.

Чтобы запустить пример [`CustomModAdd`](https://github.com/microsoft/Quantum/tree/master/samples/numerics/CustomModAdd) :

```bash
git clone https://github.com/Microsoft/Quantum.git
cd Quantum/samples/numerics/CustomModAdd
dotnet run
```
