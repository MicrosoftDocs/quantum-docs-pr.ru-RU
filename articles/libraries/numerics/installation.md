---
title: Библиотека цифровых чисел (Майкрософт) — Установка и проверка
description: Узнайте, как добавить библиотеку Microsoft тактовых чисел в установку Visual Studio 2019 или более поздней версии.
author: thomashaener
ms.author: thhaner
ms.date: 05/14/2019
ms.topic: article
uid: microsoft.quantum.numerics.installation
ms.openlocfilehash: cb0d00a509b3986b605dd7f15f9bccc0661bb894
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/28/2020
ms.locfileid: "77906344"
---
# <a name="numerics-library-installation-and-validation"></a><span data-ttu-id="01016-103">Установка и проверка библиотеки числовых значений</span><span class="sxs-lookup"><span data-stu-id="01016-103">Numerics Library Installation and Validation</span></span>

<span data-ttu-id="01016-104">Пакет средств разработки тактов обеспечивает поддержку числовых функций с помощью пакета NuGet [`Microsoft.Quantum.Numerics`](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) .</span><span class="sxs-lookup"><span data-stu-id="01016-104">The Quantum Development Kit provides support for numerics functionality through the [`Microsoft.Quantum.Numerics`](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) NuGet package.</span></span>

<span data-ttu-id="01016-105">**Visual Studio > = 2019:** Если вы используете Visual Studio 2019 или более поздней версии, можно добавить пакет числовых пакетов с помощью диспетчера пакетов NuGet.</span><span class="sxs-lookup"><span data-stu-id="01016-105">**Visual Studio >=2019:** If you are using Visual Studio 2019 or later, you can add the numerics package using the NuGet Package Manager.</span></span>
<span data-ttu-id="01016-106">Для этого выберите "Управление пакетами NuGet...". из пункта меню "проект" в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="01016-106">To do so, select "Manage NuGet Packages..." from the "Project" menu item in Visual Studio.</span></span>

<span data-ttu-id="01016-107">На вкладке Обзор выполните поиск по имени пакета "Microsoft. тактов. Numeric".</span><span class="sxs-lookup"><span data-stu-id="01016-107">From the Browse tab, search for the package name "Microsoft.Quantum.Numerics"</span></span>

> [!NOTE]
> <span data-ttu-id="01016-108">Обязательно пометка "включить предварительные выпуски"</span><span class="sxs-lookup"><span data-stu-id="01016-108">Make sure to tick "Include prerelease"</span></span>

<span data-ttu-id="01016-109">В этом списке будут перечислены пакеты, доступные для загрузки.</span><span class="sxs-lookup"><span data-stu-id="01016-109">This will list the packages available for download.</span></span>
<span data-ttu-id="01016-110">При наведении указателя мыши на "Microsoft. тактов. Numerics" отображается стрелка вниз справа от номера версии.</span><span class="sxs-lookup"><span data-stu-id="01016-110">Hovering over "Microsoft.Quantum.Numerics" reveals a downward-pointing arrow to the right of the version number.</span></span>
<span data-ttu-id="01016-111">Щелкните стрелку, чтобы установить пакет "числовые пакеты".</span><span class="sxs-lookup"><span data-stu-id="01016-111">Click on the arrow in order to install the numerics package.</span></span>

<span data-ttu-id="01016-112">Дополнительные сведения см. в разделе [Путеводитель по пользовательскому интерфейсу диспетчера пакетов](https://docs.microsoft.com/nuget/tools/package-manager-ui).</span><span class="sxs-lookup"><span data-stu-id="01016-112">For more details, see the [Package Manager UI guide](https://docs.microsoft.com/nuget/tools/package-manager-ui).</span></span>

<span data-ttu-id="01016-113">Кроме того, можно использовать консоль диспетчера пакетов, чтобы добавить библиотеку числовых библиотек в проект с помощью интерфейса командной строки.</span><span class="sxs-lookup"><span data-stu-id="01016-113">Alternatively, you can use the Package Manager Console to add the numerics library to your project via the command line interface.</span></span>

![Использование консоли диспетчера пакетов из командной строки](../../media/vs2017-nuget-console-menu.png)

<span data-ttu-id="01016-115">В консоли диспетчера пакетов выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="01016-115">From the package manager console, run the following:</span></span>

```
Install-Package Microsoft.Quantum.Numerics
```

<span data-ttu-id="01016-116">Дополнительные сведения см. в разделе [руководств по консоли диспетчера пакетов](https://docs.microsoft.com/nuget/tools/package-manager-console).</span><span class="sxs-lookup"><span data-stu-id="01016-116">For more details, see the [Package Manager Console guide](https://docs.microsoft.com/nuget/tools/package-manager-console).</span></span>

<span data-ttu-id="01016-117">**Командная строка или Visual Studio Code:** Используя командную строку самостоятельно или в Visual Studio Code, можно использовать команду `dotnet`, чтобы добавить ссылку на пакет NuGet в проект:</span><span class="sxs-lookup"><span data-stu-id="01016-117">**Command line or Visual Studio Code:** Using the command line on its own or from within Visual Studio Code, you can use the `dotnet` command to add NuGet package reference to your project:</span></span>

```dotnetcli
dotnet add package Microsoft.Quantum.Numerics
```


## <a name="verifying-your-installation"></a><span data-ttu-id="01016-118">Проверка установки</span><span class="sxs-lookup"><span data-stu-id="01016-118">Verifying your installation</span></span>

<span data-ttu-id="01016-119">Как и в остальной части пакета средств разработки тактов, Библиотека числовых данных поставляется с примерами, которые помогут быстро приступить к работе.</span><span class="sxs-lookup"><span data-stu-id="01016-119">Like the rest of the Quantum Development Kit, the numerics library comes with samples that help you get started as quickly as possible.</span></span>
<span data-ttu-id="01016-120">Чтобы проверить установку с помощью этих примеров, выполните клонирование [основного репозитория образцов](https://github.com/Microsoft/Quantum) и запустите один из примеров.</span><span class="sxs-lookup"><span data-stu-id="01016-120">To test your installation using these samples, clone the [main samples repository](https://github.com/Microsoft/Quantum) and then run one of the samples.</span></span>

<span data-ttu-id="01016-121">Чтобы запустить пример [`CustomModAdd`](https://github.com/microsoft/Quantum/tree/master/samples/numerics/CustomModAdd) :</span><span class="sxs-lookup"><span data-stu-id="01016-121">To run the [`CustomModAdd`](https://github.com/microsoft/Quantum/tree/master/samples/numerics/CustomModAdd) sample:</span></span>

```bash
git clone https://github.com/Microsoft/Quantum.git
cd Quantum/samples/numerics/CustomModAdd
dotnet run
```
