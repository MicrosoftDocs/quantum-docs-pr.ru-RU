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
# <a name="using-additional-no-locq-libraries"></a><span data-ttu-id="1abf7-103">Использование дополнительных Q# библиотек</span><span class="sxs-lookup"><span data-stu-id="1abf7-103">Using Additional Q# Libraries</span></span>

<span data-ttu-id="1abf7-104">Пакет средств разработки тактов предоставляет дополнительные функции, зависящие от домена, с помощью _пакетов NuGet_ , которые можно добавить в Q# проекты.</span><span class="sxs-lookup"><span data-stu-id="1abf7-104">The Quantum Development Kit provides additional domain-specific functionality through _NuGet packages_ that can be added to your Q# projects.</span></span>

| <span data-ttu-id="1abf7-105">Q# Библиотечная</span><span class="sxs-lookup"><span data-stu-id="1abf7-105">Q# Library</span></span>  | <span data-ttu-id="1abf7-106">Пакет NuGet</span><span class="sxs-lookup"><span data-stu-id="1abf7-106">NuGet package</span></span> | <span data-ttu-id="1abf7-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="1abf7-107">Notes</span></span> |
|---------|---------|--------|
| [<span data-ttu-id="1abf7-108">Q# Стандартная библиотека</span><span class="sxs-lookup"><span data-stu-id="1abf7-108">Q# standard library</span></span>](xref:microsoft.quantum.libraries.standard.intro) | [<span data-ttu-id="1abf7-109">**Microsoft. тактов. Standard**</span><span class="sxs-lookup"><span data-stu-id="1abf7-109">**Microsoft.Quantum.Standard**</span></span>](https://www.nuget.org/packages/Microsoft.Quantum.Standard) | <span data-ttu-id="1abf7-110">Включено по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1abf7-110">Included by default</span></span> |
| [<span data-ttu-id="1abf7-111">Библиотека квантовой химии</span><span class="sxs-lookup"><span data-stu-id="1abf7-111">Quantum chemistry library</span></span>](xref:microsoft.quantum.chemistry.concepts.intro) | [<span data-ttu-id="1abf7-112">**Microsoft.Quantum.Chemistry**</span><span class="sxs-lookup"><span data-stu-id="1abf7-112">**Microsoft.Quantum.Chemistry**</span></span>](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) | |
| [<span data-ttu-id="1abf7-113">Квантовая библиотека числовых значений</span><span class="sxs-lookup"><span data-stu-id="1abf7-113">Quantum numerics library</span></span>](xref:microsoft.quantum.numerics.intro) | [<span data-ttu-id="1abf7-114">**Значения Microsoft. тактов. numeric**</span><span class="sxs-lookup"><span data-stu-id="1abf7-114">**Microsoft.Quantum.Numerics**</span></span>](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) | |
| [<span data-ttu-id="1abf7-115">Библиотека квантового машинного обучения</span><span class="sxs-lookup"><span data-stu-id="1abf7-115">Quantum machine learning library</span></span>](xref:microsoft.quantum.libraries.machine-learning.intro) | [<span data-ttu-id="1abf7-116">**Microsoft.Quantum.MachineLearning**</span><span class="sxs-lookup"><span data-stu-id="1abf7-116">**Microsoft.Quantum.MachineLearning**</span></span>](https://www.nuget.org/packages/Microsoft.Quantum.MachineLearning) | |

<span data-ttu-id="1abf7-117">После установки пакета средств разработки такта для использования с предпочитаемой средой и языком узла можно легко добавлять библиотеки в отдельные Q# проекты без дальнейшей установки.</span><span class="sxs-lookup"><span data-stu-id="1abf7-117">Once you have installed the Quantum Development Kit for use with your preferred environment and host language, you can easily add libraries to individual Q# projects without any further installation.</span></span>

> [!NOTE]
> <span data-ttu-id="1abf7-118">Некоторые Q# библиотеки могут хорошо работать с дополнительными инструментами, которые работают вместе Q# с программами или интегрируются с ведущими приложениями.</span><span class="sxs-lookup"><span data-stu-id="1abf7-118">Some Q# libraries may work well with additional tools that work alongside your Q# programs, or that integrate with your host applications.</span></span>
> <span data-ttu-id="1abf7-119">Например, инструкции по [установке библиотеки химия](xref:microsoft.quantum.chemistry.concepts.installation) описывают, как использовать [пакет **Microsoft. такт. Химия** ](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) вместе с платформой вычислительной химия нвчем и как установить `qdk-chem` программы командной строки для работы с данными такта химия.</span><span class="sxs-lookup"><span data-stu-id="1abf7-119">For example, the [chemistry library installation instructions](xref:microsoft.quantum.chemistry.concepts.installation) describe how to use the [**Microsoft.Quantum.Chemistry** package](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) together with the NWChem computational chemistry platform, and how to install the `qdk-chem` command-line tools for working with quantum chemistry data.</span></span>

## <a name="no-locq-applications-or-net-interopability"></a>[<span data-ttu-id="1abf7-120">Q# взаимодействие приложений или .NET</span><span class="sxs-lookup"><span data-stu-id="1abf7-120">Q# applications or .NET interopability</span></span>](#tab/tabid-csproj)

<span data-ttu-id="1abf7-121">**Командная строка или Visual Studio Code:** Используя командную строку самостоятельно или в Visual Studio Code, можно использовать `dotnet` команду, чтобы добавить ссылку на пакет NuGet в проект.</span><span class="sxs-lookup"><span data-stu-id="1abf7-121">**Command prompt or Visual Studio Code:** Using the command prompt on its own or from within Visual Studio Code, you can use the `dotnet` command to add a NuGet package reference to your project.</span></span>
<span data-ttu-id="1abf7-122">Например, чтобы добавить пакет [**Microsoft. такт. Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) , выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="1abf7-122">For example, to add the [**Microsoft.Quantum.Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) package, run the following command:</span></span>

```dotnetcli
dotnet add package Microsoft.Quantum.Numerics
```

<span data-ttu-id="1abf7-123">**Visual Studio:** При использовании Visual Studio 2019 или более поздней версии можно добавить дополнительные Q# пакеты с помощью диспетчера пакетов NuGet.</span><span class="sxs-lookup"><span data-stu-id="1abf7-123">**Visual Studio:** If you are using Visual Studio 2019 or later, you can add additional Q# packages using the NuGet Package Manager.</span></span>
<span data-ttu-id="1abf7-124">Чтобы загрузить пакет, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1abf7-124">To load a package:</span></span> 
1. <span data-ttu-id="1abf7-125">Откройте проект в Visual Studio и выберите **Управление пакетами NuGet...** в меню **проект** .</span><span class="sxs-lookup"><span data-stu-id="1abf7-125">With a project open in Visual Studio, select **Manage NuGet Packages...** from the **Project** menu.</span></span>

2. <span data-ttu-id="1abf7-126">Нажмите кнопку **Обзор**, выберите **включить предварительный выпуск** и выполните поиск по имени пакета «Microsoft. тактов. numeric».</span><span class="sxs-lookup"><span data-stu-id="1abf7-126">Click **Browse**, select **Include prerelease** and search for the package name "Microsoft.Quantum.Numerics".</span></span> <span data-ttu-id="1abf7-127">В этом списке будут перечислены пакеты, доступные для загрузки.</span><span class="sxs-lookup"><span data-stu-id="1abf7-127">This will list the packages available for download.</span></span>

3. <span data-ttu-id="1abf7-128">Наведите указатель мыши на **Microsoft. тактов. Numerics** и щелкните стрелку вниз справа от номера версии, чтобы установить пакет числовых данных.</span><span class="sxs-lookup"><span data-stu-id="1abf7-128">Hover over **Microsoft.Quantum.Numerics** and click the downward-pointing arrow to the right of the version number to install the numerics package.</span></span>

<span data-ttu-id="1abf7-129">Дополнительные сведения см. в разделе [Путеводитель по пользовательскому интерфейсу диспетчера пакетов](https://docs.microsoft.com/nuget/tools/package-manager-ui).</span><span class="sxs-lookup"><span data-stu-id="1abf7-129">For more details, see the [Package Manager UI guide](https://docs.microsoft.com/nuget/tools/package-manager-ui).</span></span>

<span data-ttu-id="1abf7-130">Кроме того, можно использовать консоль диспетчера пакетов, чтобы добавить библиотеку числовых библиотек в проект с помощью интерфейса командной строки.</span><span class="sxs-lookup"><span data-stu-id="1abf7-130">Alternatively, you can use the Package Manager Console to add the numerics library to your project via the command line interface.</span></span>

![Использование консоли диспетчера пакетов из командной строки](~/media/vs2017-nuget-console-menu.png)

<span data-ttu-id="1abf7-132">В консоли диспетчера пакетов выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="1abf7-132">From the Package Manager Console, run the following:</span></span>

```
Install-Package Microsoft.Quantum.Numerics
```

<span data-ttu-id="1abf7-133">Дополнительные сведения см. в разделе [руководств по консоли диспетчера пакетов](https://docs.microsoft.com/nuget/tools/package-manager-console).</span><span class="sxs-lookup"><span data-stu-id="1abf7-133">For more details, see the [Package Manager Console guide](https://docs.microsoft.com/nuget/tools/package-manager-console).</span></span>

## <a name="ino-locq-notebooks"></a>[<span data-ttu-id="1abf7-134">Q#Записные книжки</span><span class="sxs-lookup"><span data-stu-id="1abf7-134">IQ# Notebooks</span></span>](#tab/tabid-notebook)

<span data-ttu-id="1abf7-135">Можно сделать дополнительные пакеты доступными для использования в Q# записной книжке I с помощью [ `%package` команды Magic](xref:microsoft.quantum.iqsharp.magic-ref.package).</span><span class="sxs-lookup"><span data-stu-id="1abf7-135">You can make additional packages available for use in an IQ# Notebook by using the [`%package` magic command](xref:microsoft.quantum.iqsharp.magic-ref.package).</span></span>
<span data-ttu-id="1abf7-136">Например, чтобы добавить пакет [**Microsoft. такт. Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) для использования в Q# записной книжке I, выполните следующую команду в ячейке записной книжки:</span><span class="sxs-lookup"><span data-stu-id="1abf7-136">For example, to add the [**Microsoft.Quantum.Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) package for use in an IQ# Notebook, run the following command in a notebook cell:</span></span>

```
%package Microsoft.Quantum.Numerics
```

<span data-ttu-id="1abf7-137">После этой команды пакет будет доступен для любых ячеек в записной книжке.</span><span class="sxs-lookup"><span data-stu-id="1abf7-137">Following this command, the package is available to any cells within the notebook.</span></span>
<span data-ttu-id="1abf7-138">Чтобы сделать пакет доступным из Q# кода в текущей рабочей области, перезагрузите рабочую область после добавления пакета:</span><span class="sxs-lookup"><span data-stu-id="1abf7-138">To make the package available from Q# code in the current workspace, reload the workspace after adding your package:</span></span>

```
%workspace reload
```

## <a name="python-interoperability"></a>[<span data-ttu-id="1abf7-139">Совместимость c Python</span><span class="sxs-lookup"><span data-stu-id="1abf7-139">Python interoperability</span></span>](#tab/tabid-python)


<span data-ttu-id="1abf7-140">Можно сделать дополнительные пакеты доступными для использования в основной программе Python с помощью [`qsharp.packages.add`](https://docs.microsoft.com/python/qsharp/qsharp.packages.packages) метода.</span><span class="sxs-lookup"><span data-stu-id="1abf7-140">You can make additional packages available for use in a Python host program by using the [`qsharp.packages.add`](https://docs.microsoft.com/python/qsharp/qsharp.packages.packages) method.</span></span>
<span data-ttu-id="1abf7-141">Например, чтобы добавить пакет [**Microsoft. такт. Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) для использования в Q# записной книжке I, выполните следующий код Python:</span><span class="sxs-lookup"><span data-stu-id="1abf7-141">For example, to add the [**Microsoft.Quantum.Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) package for use in an IQ# Notebook, run the following Python code:</span></span>

```python
import qsharp
qsharp.packages.add("Microsoft.Quantum.Numerics")
```

<span data-ttu-id="1abf7-142">После этой команды пакет будет предоставляться для любого Q# кода, скомпилированного с помощью `qsharp.compile` .</span><span class="sxs-lookup"><span data-stu-id="1abf7-142">Following this command, the package will be made available to any Q# code compiled using `qsharp.compile`.</span></span>
<span data-ttu-id="1abf7-143">Чтобы сделать пакет доступным из Q# кода в текущей рабочей области, перезагрузите рабочую область после добавления пакета:</span><span class="sxs-lookup"><span data-stu-id="1abf7-143">To make the package available from Q# code in the current workspace, reload the workspace after adding your package:</span></span>

```python
qsharp.reload()
```

***
