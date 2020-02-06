---
title: Установка и проверка библиотеки химия | Документация Майкрософт
description: Установка и проверка библиотеки химия
author: guanghaolow
ms.author: gulow
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.chemistry.concepts.installation
ms.openlocfilehash: de13d1814821c612ed74a347dc8ffb5881063576
ms.sourcegitcommit: 5094c0a60cbafdee669c8728b92df281071259b9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2020
ms.locfileid: "77036480"
---
# <a name="chemistry-library-installation-and-validation"></a><span data-ttu-id="a9753-103">Установка и проверка библиотеки химия</span><span class="sxs-lookup"><span data-stu-id="a9753-103">Chemistry Library Installation and Validation</span></span>

<span data-ttu-id="a9753-104">Пакет средств разработки тактов обеспечивает поддержку приложений тактовой химия с помощью пакета NuGet [`Microsoft.Quantum.Chemistry`](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) .</span><span class="sxs-lookup"><span data-stu-id="a9753-104">The Quantum Development Kit provides support for quantum chemistry applications through the [`Microsoft.Quantum.Chemistry`](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) NuGet package.</span></span>
<span data-ttu-id="a9753-105">Как и в случае с другими пакетами NuGet, добавление библиотеки химия в проект несложно.</span><span class="sxs-lookup"><span data-stu-id="a9753-105">As with other NuGet packages, it's straightforward to add the chemistry library to your project.</span></span>

<span data-ttu-id="a9753-106">**Visual Studio 2019:** При использовании Visual Studio 2019 можно добавить пакеты тактовой химия с помощью диспетчера пакетов NuGet.</span><span class="sxs-lookup"><span data-stu-id="a9753-106">**Visual Studio 2019:** If you are using Visual Studio 2019, you can add the quantum chemistry packages by using the NuGet Package Manager.</span></span>
<span data-ttu-id="a9753-107">Чтобы открыть диспетчер пакетов, щелкните правой кнопкой мыши проект, в который вы хотите добавить библиотеку химия, и выберите пункт "Управление пакетами NuGet...", как показано на снимке экрана ниже.</span><span class="sxs-lookup"><span data-stu-id="a9753-107">To open the Package Manager, right-click on the project you'd like to add the chemistry library to and select "Manage NuGet Packages...," as in the screenshot below.</span></span>

![](~/media/vs2017-nuget-manage-packages.png)

<span data-ttu-id="a9753-108">На вкладке Обзор найдите имя пакета Microsoft. такт. химия.</span><span class="sxs-lookup"><span data-stu-id="a9753-108">From the Browse tab, search for the package name "Microsoft.Quantum.Chemistry."</span></span>

> [!NOTE]
> <span data-ttu-id="a9753-109">Обязательно пометка "включить предварительные выпуски".</span><span class="sxs-lookup"><span data-stu-id="a9753-109">Make sure to tick "Include prerelease."</span></span>

![](~/media/vs2017-nuget-package-search.png)

<span data-ttu-id="a9753-110">В этом списке будут перечислены пакеты, доступные для загрузки.</span><span class="sxs-lookup"><span data-stu-id="a9753-110">This will list the packages available for download.</span></span>
<span data-ttu-id="a9753-111">Щелкните элемент "Microsoft. тактов. Химия" в левой области, выберите последнюю предварительную версию на правой панели и нажмите кнопку "установить":</span><span class="sxs-lookup"><span data-stu-id="a9753-111">Click on the "Microsoft.Quantum.Chemistry on the left-hand pane, select the latest pre-release version on the right-hand pane, and click "Install":</span></span>

![](~/media/vs2017-nuget-select-chem.png)

<span data-ttu-id="a9753-112">Дополнительные сведения см. в разделе [Путеводитель по пользовательскому интерфейсу диспетчера пакетов](https://docs.microsoft.com/nuget/tools/package-manager-ui).</span><span class="sxs-lookup"><span data-stu-id="a9753-112">For more details, see the [Package Manager UI guide](https://docs.microsoft.com/nuget/tools/package-manager-ui).</span></span>

<span data-ttu-id="a9753-113">Кроме того, с помощью консоли диспетчера пакетов можно добавить в проект библиотеку тактов химия с помощью интерфейса командной строки.</span><span class="sxs-lookup"><span data-stu-id="a9753-113">Alternatively, you can use the Package Manager Console to add the quantum chemistry library to your project with a command line interface.</span></span>

![](~/media/vs2017-nuget-console-menu.png)

<span data-ttu-id="a9753-114">В консоли диспетчера пакетов выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="a9753-114">From the package manager console, run the following:</span></span>

```
Install-Package Microsoft.Quantum.Chemistry
```

<span data-ttu-id="a9753-115">Дополнительные сведения см. в разделе [руководств по консоли диспетчера пакетов](https://docs.microsoft.com/nuget/tools/package-manager-console).</span><span class="sxs-lookup"><span data-stu-id="a9753-115">For more details, see the [Package Manager Console guide](https://docs.microsoft.com/nuget/tools/package-manager-console).</span></span>

<span data-ttu-id="a9753-116">**Командная строка или Visual Studio Code:** Используя командную строку самостоятельно или в Visual Studio Code, можно использовать команду `dotnet`, чтобы добавить ссылку на пакет NuGet в проект:</span><span class="sxs-lookup"><span data-stu-id="a9753-116">**Command line or Visual Studio Code:** Using the command line on its own or from within Visual Studio Code, you can use the `dotnet` command to add NuGet package reference to your project:</span></span>

```dotnetcli
dotnet add package Microsoft.Quantum.Chemistry
```

## <a name="verifying-your-installation"></a><span data-ttu-id="a9753-117">Проверка установки</span><span class="sxs-lookup"><span data-stu-id="a9753-117">Verifying Your Installation</span></span> 

<span data-ttu-id="a9753-118">Как и в остальной части пакета средств разработки тактов, в библиотеке тактов химия имеется ряд полностью документированных примеров, которые помогут быстро приступить к работе.</span><span class="sxs-lookup"><span data-stu-id="a9753-118">Like the rest of the Quantum Development Kit, the quantum chemistry library comes with a number of fully documented samples to help you get up and running quickly.</span></span>
<span data-ttu-id="a9753-119">Чтобы проверить установку с помощью этих примеров, выполните клонирование [основного репозитория примеров](https://github.com/Microsoft/Quantum), а затем запустите один из примеров.</span><span class="sxs-lookup"><span data-stu-id="a9753-119">To test your installation using these samples, clone the [main samples repository](https://github.com/Microsoft/Quantum), then run one of the samples.</span></span>  <span data-ttu-id="a9753-120">Например, чтобы запустить пример [`MolecularHydrogen`](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/MolecularHydrogen) :</span><span class="sxs-lookup"><span data-stu-id="a9753-120">For example, to run the [`MolecularHydrogen`](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/MolecularHydrogen) sample:</span></span>

```bash
git clone https://github.com/Microsoft/Quantum.git
cd Quantum/samples/chemistry/MolecularHydrogen
dotnet run
```

<span data-ttu-id="a9753-121">Чтобы проверить установку библиотеки тактов химия с помощью Microsoft Visual Studio после клонирования репозитория:</span><span class="sxs-lookup"><span data-stu-id="a9753-121">To verify the installation of the quantum chemistry library using Microsoft Visual Studio after cloning the repository:</span></span>
    1. <span data-ttu-id="a9753-122">Откройте решение Чемистрисамплес. sln в папке химия.</span><span class="sxs-lookup"><span data-stu-id="a9753-122">Open the ChemistrySamples.sln solution in the Chemistry folder.</span></span>  
    2. <span data-ttu-id="a9753-123">Выберите Samples/1.</span><span class="sxs-lookup"><span data-stu-id="a9753-123">Select Samples/1.</span></span> <span data-ttu-id="a9753-124">Простые молекулы/Молекулархидрожен в качестве запускаемого проекта.</span><span class="sxs-lookup"><span data-stu-id="a9753-124">Simple Molecules/MolecularHydrogen as the StartUp project.</span></span>
    3. <span data-ttu-id="a9753-125">Нажмите клавишу F5, чтобы запустить демонстрацию оценки этапа молекулярное водорода.</span><span class="sxs-lookup"><span data-stu-id="a9753-125">Press F5 to run the molecular Hydrogen quantum phase estimation demo.</span></span>

<span data-ttu-id="a9753-126">Дополнительные сведения об оценке значений уровней энергии см. в разделе [получение оценок уровня энергии](xref:microsoft.quantum.chemistry.examples.energyestimate) .</span><span class="sxs-lookup"><span data-stu-id="a9753-126">See [Obtaining energy level estimates](xref:microsoft.quantum.chemistry.examples.energyestimate) for more information on estimating the values of energy levels.</span></span>   


## <a name="using-the-quantum-development-kit-with-nwchem"></a><span data-ttu-id="a9753-127">Использование пакета средств разработки тактов с Нвчем</span><span class="sxs-lookup"><span data-stu-id="a9753-127">Using the Quantum Development Kit with NWChem</span></span> ##

<span data-ttu-id="a9753-128">В примере Молекулархидрожен используются входные данные молекулярное, настроенные вручную.</span><span class="sxs-lookup"><span data-stu-id="a9753-128">The MolecularHydrogen sample uses molecular input data that is manually configured.</span></span>  <span data-ttu-id="a9753-129">Хотя это и удобно для небольших примеров, тактовая химия в масштабе требует Хамилтонианс с миллионами или миллиардами терминов.</span><span class="sxs-lookup"><span data-stu-id="a9753-129">While this is fine for small examples, quantum chemistry at scale require Hamiltonians with millions or billions of terms.</span></span> <span data-ttu-id="a9753-130">Такие Хамилтонианс, созданные масштабируемыми вычислительными пакетами химия, слишком велики для импорта вручную.</span><span class="sxs-lookup"><span data-stu-id="a9753-130">Such Hamiltonians, generated by scalable computational chemistry packages are too large to import by hand.</span></span> 

<span data-ttu-id="a9753-131">Библиотека тактовой химия для пакета разработки такта разработана для работы с вычислительными пакетами химия, которая, в первую очередь, является [**нвчем**](http://www.nwchem-sw.org/) вычислительной химияной платформой, разработанной лабораторией молекулярное SCIENCES (емсл) в северо-западной национальной лаборатории.</span><span class="sxs-lookup"><span data-stu-id="a9753-131">The quantum chemistry library for the Quantum Development Kit is designed to work well with computational chemistry packages, most notably the [**NWChem**](http://www.nwchem-sw.org/) computational chemistry platform developed by the Environmental Molecular Sciences Laboratory (EMSL) at Pacific Northwest National Laboratory.</span></span>
<span data-ttu-id="a9753-132">В частности, пакет `Microsoft.Quantum.Chemistry` предоставляет средства для загрузки экземпляров проблем моделирования тактов химия, представленных в [схеме брумбридже](xref:microsoft.quantum.libraries.chemistry.schema.broombridge), которые также поддерживаются для экспорта в последних версиях нвчем.</span><span class="sxs-lookup"><span data-stu-id="a9753-132">In particular, the `Microsoft.Quantum.Chemistry` package provides tools for loading instances of quantum chemistry simulation problems represented in the [Broombridge schema](xref:microsoft.quantum.libraries.chemistry.schema.broombridge), also supported for export by recent versions of NWChem.</span></span>

<span data-ttu-id="a9753-133">Чтобы начать работу с помощью Нвчем вместе с пакетом средств разработки тактов, мы предлагаем один из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="a9753-133">To get up and running using NWChem together with the Quantum Development Kit, we suggest one of the following methods:</span></span>
- <span data-ttu-id="a9753-134">Начните работу с существующих файлов Брумбридже, предоставленных в примерах на сайте [интегралдата/YAML](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML).</span><span class="sxs-lookup"><span data-stu-id="a9753-134">Get started using existing Broombridge files provided with the samples at [IntegralData/YAML](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML).</span></span>
- <span data-ttu-id="a9753-135">Используйте [Построитель стрелок емсл для Microsoft Quantum Development Kit](https://arrows.emsl.pnnl.gov/api/qsharp_chem) , который является веб-интерфейсом для нвчем, для создания новых входных файлов брумбридже с форматом молекулярное.</span><span class="sxs-lookup"><span data-stu-id="a9753-135">Use the [EMSL Arrows Builder for the Microsoft Quantum Development Kit](https://arrows.emsl.pnnl.gov/api/qsharp_chem) which is a web-based frontend to NWChem, to generate new Broombridge-formated molecular input files.</span></span>  
- <span data-ttu-id="a9753-136">Используйте [образ DOCKER](https://hub.docker.com/r/nwchemorg/nwchem-qc/) , предоставленный пннл для запуска нвчем, или</span><span class="sxs-lookup"><span data-stu-id="a9753-136">Use the [Docker image](https://hub.docker.com/r/nwchemorg/nwchem-qc/) provided by PNNL to run NWChem, or</span></span>
- <span data-ttu-id="a9753-137">[Скомпилируйте нвчем](http://www.nwchem-sw.org/index.php/Compiling_NWChem) для своей платформы.</span><span class="sxs-lookup"><span data-stu-id="a9753-137">[Compile NWChem](http://www.nwchem-sw.org/index.php/Compiling_NWChem) for your platform.</span></span>

<span data-ttu-id="a9753-138">Дополнительные сведения о работе с Нвчем для химических моделей для анализа с помощью библиотеки химия пакета персонала [Kit см. в этой](xref:microsoft.quantum.chemistry.examples.endtoend) статье.</span><span class="sxs-lookup"><span data-stu-id="a9753-138">See [End-to-end with NWChem](xref:microsoft.quantum.chemistry.examples.endtoend) for more information on how to work with NWChem to chemical models to analyze with the Quantum Developmen Kit chemistry library.</span></span>

### <a name="getting-started-using-broombridge-files-provided-with-the-samples"></a><span data-ttu-id="a9753-139">Приступая к работе с файлами Брумбридже, поставляемыми с образцами</span><span class="sxs-lookup"><span data-stu-id="a9753-139">Getting started using Broombridge files provided with the samples</span></span>

<span data-ttu-id="a9753-140">Папка [интегралдата/YAML](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML) в репозитории примеров пакета разработки тактов содержит файлы данных с брумбридже форматом.</span><span class="sxs-lookup"><span data-stu-id="a9753-140">The [IntegralData/YAML](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML) folder in the Quantum Development Kit Samples repository contains Broombridge-formated molecule data files.</span></span>  

<span data-ttu-id="a9753-141">В качестве простого примера используйте пример библиотеки химия, [жетгатекаунт](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/GetGateCount) , чтобы загрузить хамилтониан из одного из брумбридже файлов и выполнить прогнозное моделирование алгоригсмс:</span><span class="sxs-lookup"><span data-stu-id="a9753-141">As a simple example, use the chemistry library sample, [GetGateCount](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/GetGateCount) to load the Hamiltonian from one of Broombridge files and perform gate estimates of quantum simulation algorigthms:</span></span>

```bash
cd Quantum/Chemistry/GetGateCount
dotnet run -- --path=../IntegralData/YAML/h2.yaml --format=YAML
```

<span data-ttu-id="a9753-142">Дополнительные сведения о том, как ввести молекулы, представленные схемой Брумбридже, см. в разделе [Загрузка хамилтониан из файла](xref:microsoft.quantum.chemistry.examples.loadhamiltonian) .</span><span class="sxs-lookup"><span data-stu-id="a9753-142">See [Loading a Hamiltonian from file](xref:microsoft.quantum.chemistry.examples.loadhamiltonian) for more information on how to input molecules represented by the Broombridge schema.</span></span>  

<span data-ttu-id="a9753-143">Дополнительные сведения об оценке ресурсов см. в разделе [Получение количества ресурсов](xref:microsoft.quantum.chemistry.examples.resourcecounts) .</span><span class="sxs-lookup"><span data-stu-id="a9753-143">See [Obtaining resource counts](xref:microsoft.quantum.chemistry.examples.resourcecounts) for more information on resource estimation.</span></span>  

### <a name="getting-started-using-the-emsl-arrows-builder"></a><span data-ttu-id="a9753-144">Приступая к работе с построителем стрелок ЕМСЛ</span><span class="sxs-lookup"><span data-stu-id="a9753-144">Getting started using the EMSL Arrows Builder</span></span>

<span data-ttu-id="a9753-145">Стрелки ЕМСЛ — это средство, которое использует Нвчем и химические вычислительные базы данных для создания данных молекулы.</span><span class="sxs-lookup"><span data-stu-id="a9753-145">EMSL Arrows is a tool that uses NWChem and chemical computational databases to generate molecule data.</span></span>  <span data-ttu-id="a9753-146">[Построитель стрелок емсл для Microsoft Quantum Development Kit](https://arrows.emsl.pnnl.gov/api/qsharp_chem) позволяет ввести модель с помощью нескольких построителей Молекулярное моделей и создать файл брумбридже, который будет использоваться пакетом разработки тактов.</span><span class="sxs-lookup"><span data-stu-id="a9753-146">[EMSL Arrows Builder for the Microsoft Quantum Development Kit](https://arrows.emsl.pnnl.gov/api/qsharp_chem) allows you to enter your model using multiple molecular model builders and generate the Broombridge datafile to be used by the Quantum Development Kit.</span></span>  

<span data-ttu-id="a9753-147">На странице ЕМСЛ щелкните вкладку ["Инстуктионс"] и следуйте инструкциям ["простые примеры"], чтобы создать файлы Брумбридже.</span><span class="sxs-lookup"><span data-stu-id="a9753-147">From the EMSL page, click on the ['Instuctions'] tab, and follow the ['Simple Examples'] instructions to generate Broombridge files.</span></span>  <span data-ttu-id="a9753-148">Затем попробуйте запустить [' Жетгатекаунт '], чтобы просмотреть оценки ресурсов такта для этих молекул.</span><span class="sxs-lookup"><span data-stu-id="a9753-148">Then try running the ['GetGateCount'] to see the quantum resource estimates for these molecules.</span></span>

### <a name="installing-nwchem-from-source"></a><span data-ttu-id="a9753-149">Установка Нвчем из источника</span><span class="sxs-lookup"><span data-stu-id="a9753-149">Installing NWChem from Source</span></span>

<span data-ttu-id="a9753-150">Полные инструкции по установке Нвчем из источника [предоставляются пннл](http://www.nwchem-sw.org/index.php/Compiling_NWChem).</span><span class="sxs-lookup"><span data-stu-id="a9753-150">Full instructions on how to install NWChem from source [are provided by PNNL](http://www.nwchem-sw.org/index.php/Compiling_NWChem).</span></span>

> [!TIP]
> <span data-ttu-id="a9753-151">Если вы хотите использовать Нвчем из Windows 10, то подсистема Windows для Linux является отличным вариантом.</span><span class="sxs-lookup"><span data-stu-id="a9753-151">If you wish to use NWChem from Windows 10, the Windows Subsystem for Linux is a great option.</span></span>
> <span data-ttu-id="a9753-152">После установки [Ubuntu 18,04 LTS для Windows](https://www.microsoft.com/en-us/p/ubuntu-1804-lts/9n9tngvndl3q#activetab=pivot:overviewtab)запустите `ubuntu18.04` из любимого терминала и следуйте инструкциям выше, чтобы установить нвчем из источника.</span><span class="sxs-lookup"><span data-stu-id="a9753-152">Once you have installed [Ubuntu 18.04 LTS for Windows](https://www.microsoft.com/en-us/p/ubuntu-1804-lts/9n9tngvndl3q#activetab=pivot:overviewtab), run `ubuntu18.04` from your favorite terminal and follow the instructions above to install NWChem from source.</span></span>

<span data-ttu-id="a9753-153">После компиляции Нвчем из источника можно запустить сценарий `yaml_driver`, поставляемый с Нвчем, чтобы быстро создавать экземпляры Брумбридже из Нвчем входных колод:</span><span class="sxs-lookup"><span data-stu-id="a9753-153">Once you have compiled NWChem from source, you can run the `yaml_driver` script provided with NWChem to quickly produce Broombridge instances from NWChem input decks:</span></span>

```bash
$NWCHEM_TOP/contrib/quasar/yaml_driver input.nw
```

<span data-ttu-id="a9753-154">Эта команда создаст новый файл `input.yaml` в формате Брумбридже в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="a9753-154">This command will create a new `input.yaml` file in the Broombridge format within your current directory.</span></span>

### <a name="using-nwchem-with-docker"></a><span data-ttu-id="a9753-155">Использование Нвчем с DOCKER</span><span class="sxs-lookup"><span data-stu-id="a9753-155">Using NWChem with Docker</span></span>

<span data-ttu-id="a9753-156">Предварительно созданные образы для использования Нвчем доступны в разных платформах через [центр DOCKER](https://hub.docker.com).</span><span class="sxs-lookup"><span data-stu-id="a9753-156">Pre-built images for using NWChem are available cross-platform via [Docker Hub](https://hub.docker.com).</span></span>
<span data-ttu-id="a9753-157">Чтобы приступить к работе, следуйте инструкциям по установке DOCKER для своей платформы:</span><span class="sxs-lookup"><span data-stu-id="a9753-157">To get started, follow the Docker installation instructions for your platform:</span></span>

- [<span data-ttu-id="a9753-158">Установка DOCKER для Ubuntu</span><span class="sxs-lookup"><span data-stu-id="a9753-158">Install Docker for Ubuntu</span></span>](https://docs.docker.com/install/linux/docker-ce/ubuntu/)
- [<span data-ttu-id="a9753-159">Установка DOCKER для macOS</span><span class="sxs-lookup"><span data-stu-id="a9753-159">Install Docker for macOS</span></span>](https://docs.docker.com/docker-for-mac/install/)
- [<span data-ttu-id="a9753-160">Установка Docker для Windows 10</span><span class="sxs-lookup"><span data-stu-id="a9753-160">Install Docker for Windows 10</span></span>](https://docs.docker.com/docker-for-windows/install/)

> [!TIP]
> <span data-ttu-id="a9753-161">При использовании Docker для Windows необходимо предоставить общий доступ к диску, содержащему временный каталог (как правило, это `C:\` диск) с управляющей программой DOCKER.</span><span class="sxs-lookup"><span data-stu-id="a9753-161">If you are using Docker for Windows, you will need to share the drive containing your temporary directory (usually this is the `C:\` drive) with the Docker daemon.</span></span> <span data-ttu-id="a9753-162">Дополнительные сведения см. в [документации по DOCKER](https://docs.docker.com/docker-for-windows/#shared-drives) .</span><span class="sxs-lookup"><span data-stu-id="a9753-162">See the [Docker documentation](https://docs.docker.com/docker-for-windows/#shared-drives) for more details.</span></span>

<span data-ttu-id="a9753-163">После установки DOCKER можно использовать модуль PowerShell, поставляемый с примерами пакета разработки такта, для запуска образа, или можно запустить образ вручную.</span><span class="sxs-lookup"><span data-stu-id="a9753-163">Once you have Docker installed, you can either use the PowerShell module provided with the Quantum Development Kit samples to run the image, or you can run the image manually.</span></span>
<span data-ttu-id="a9753-164">Мы подробно будем использовать PowerShell. Если вы хотите использовать образ DOCKER вручную, обратитесь к [документации, поставляемой с этим изображением](https://hub.docker.com/r/nwchemorg/nwchem-qc/).</span><span class="sxs-lookup"><span data-stu-id="a9753-164">We detail using PowerShell here; if you would like to use the Docker image manually, please see the [documentation provided with the image](https://hub.docker.com/r/nwchemorg/nwchem-qc/).</span></span>

#### <a name="running-nwchem-through-powershell-core"></a><span data-ttu-id="a9753-165">Выполнение Нвчем с помощью PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="a9753-165">Running NWChem through PowerShell Core</span></span>

<span data-ttu-id="a9753-166">Чтобы использовать образ DOCKER Нвчем с пакетом разработки тактов, мы предоставляем небольшой модуль PowerShell, который обрабатывает перемещение файлов в Нвчем и из него.</span><span class="sxs-lookup"><span data-stu-id="a9753-166">To use the NWChem Docker image with the Quantum Development Kit, we provide a small PowerShell module that handles moving files in and out of NWChem for you.</span></span>
<span data-ttu-id="a9753-167">Если вы еще не установили PowerShell Core, можно скачать его кросс-платформенную версию из [репозитория PowerShell на сайте GitHub](https://github.com/PowerShell/PowerShell#get-powershell).</span><span class="sxs-lookup"><span data-stu-id="a9753-167">If you don't already have PowerShell Core installed, you can download it cross-platform from the [PowerShell repository on GitHub](https://github.com/PowerShell/PowerShell#get-powershell).</span></span>

> [!NOTE]
> <span data-ttu-id="a9753-168">PowerShell Core также используется в некоторых примерах для демонстрации взаимодействия с рабочими процессами обработки и анализа данных и бизнес-аналитики.</span><span class="sxs-lookup"><span data-stu-id="a9753-168">PowerShell Core is also used for some samples to demonstrate interoperability with data science and business analytics workflows.</span></span>

<span data-ttu-id="a9753-169">После установки PowerShell Core импортируйте `InvokeNWChem.psm1`, чтобы сделать команды Нвчем доступными в текущем сеансе:</span><span class="sxs-lookup"><span data-stu-id="a9753-169">Once you have PowerShell Core installed, import `InvokeNWChem.psm1` to make NWChem commands available in your current session:</span></span>

```powershell
cd Quantum/utilities/
Import-Module ./InvokeNWChem.psm1
```

<span data-ttu-id="a9753-170">Это сделает команду `Convert-NWChemToBroombridge` доступной в текущем сеансе PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a9753-170">This will make the `Convert-NWChemToBroombridge` command available in your current PowerShell session.</span></span>
<span data-ttu-id="a9753-171">Чтобы скачать все необходимые образы из DOCKER и использовать их для запуска Нвчем входных колод и отслеживания выходных данных в Брумбридже, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="a9753-171">To download any needed images from Docker and use them to run NWChem input decks and capture output to Broombridge, run the following:</span></span>

```powershell
Convert-NWChemToBroombridge ./input.nw
```

<span data-ttu-id="a9753-172">При этом будет создан файл Брумбридже, запустив Нвчем на `input.nw`.</span><span class="sxs-lookup"><span data-stu-id="a9753-172">This will create a Broombridge file by running NWChem on `input.nw`.</span></span>
<span data-ttu-id="a9753-173">По умолчанию выходные данные Брумбридже будут иметь те же имя и путь, что и входной лоток, с расширением `.nw`, замененным `.yaml`.</span><span class="sxs-lookup"><span data-stu-id="a9753-173">By default, the Broombridge output will have the same name and path as the input deck, with the `.nw` extension replaced by `.yaml`.</span></span>
<span data-ttu-id="a9753-174">Это можно переопределить с помощью параметра `-DestinationPath` для `Convert-NWChemToBroombridge`.</span><span class="sxs-lookup"><span data-stu-id="a9753-174">This can be overridden by using the `-DestinationPath` parameter to `Convert-NWChemToBroombridge`.</span></span>
<span data-ttu-id="a9753-175">Дополнительные сведения можно получить с помощью встроенных функций справки PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a9753-175">More information can be obtained by using PowerShell's built-in help functionality:</span></span>

```powershell
Convert-NWChemToBroombridge -?
Get-Help Convert-NWChemToBroombridge -Full
```
