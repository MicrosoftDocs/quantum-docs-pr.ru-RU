---
title: Пример Нвчем тактовой программы
description: С помощью колоды входных данных Нвчем рассмотрим пример получения счетчиков шлюзов для моделирования тактов химия.
author: cgranade
ms.author: chgranad@microsoft.com
ms.date: 10/23/2018
uid: microsoft.quantum.chemistry.examples.endtoend
no-loc:
- Q#
- $$v
ms.openlocfilehash: 78d6488ed5e3972f85f1e6cf1ba2d197596c4cc3
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869313"
---
# <a name="end-to-end-with-nwchem"></a><span data-ttu-id="6bb17-103">Полный цикл работы с NWChem</span><span class="sxs-lookup"><span data-stu-id="6bb17-103">End-to-end with NWChem</span></span> #

<span data-ttu-id="6bb17-104">В этой статье вы узнаете пример получения счетчиков шлюзов для моделирования тактовой химия, начиная с колоды входных данных [нвчем](http://www.nwchem-sw.org/index.php/Main_Page) .</span><span class="sxs-lookup"><span data-stu-id="6bb17-104">In this article, you will walk through an example of getting gate counts for quantum chemistry simulation, starting from an [NWChem](http://www.nwchem-sw.org/index.php/Main_Page) input deck.</span></span>
<span data-ttu-id="6bb17-105">Прежде чем продолжить работу с этим примером, убедитесь, что вы установили DOCKER, следуя [инструкциям по установке и проверке](xref:microsoft.quantum.chemistry.concepts.installation).</span><span class="sxs-lookup"><span data-stu-id="6bb17-105">Before proceeding with this example, make sure that you've installed Docker, following the [installation and validation guide](xref:microsoft.quantum.chemistry.concepts.installation).</span></span>

<span data-ttu-id="6bb17-106">Дополнительные сведения:</span><span class="sxs-lookup"><span data-stu-id="6bb17-106">For more information:</span></span>
- [<span data-ttu-id="6bb17-107">Структура Нвчем входных колод</span><span class="sxs-lookup"><span data-stu-id="6bb17-107">Structure of NWChem input decks</span></span>](https://github.com/nwchemgit/nwchem/wiki/Getting-Started#input-file-structure)
    - [<span data-ttu-id="6bb17-108">Команды колоды ввода для использования с пакетом разработки тактов</span><span class="sxs-lookup"><span data-stu-id="6bb17-108">Input deck commands for use with the Quantum Development Kit</span></span>](https://github.com/nwchemgit/nwchem/tree/master/contrib/quasar)
- [<span data-ttu-id="6bb17-109">Установка библиотеки и зависимостей химия</span><span class="sxs-lookup"><span data-stu-id="6bb17-109">Installing the chemistry library and dependencies</span></span>](xref:microsoft.quantum.chemistry.concepts.installation)
- [<span data-ttu-id="6bb17-110">Подсчет ресурсов</span><span class="sxs-lookup"><span data-stu-id="6bb17-110">Resource counting</span></span>](xref:microsoft.quantum.chemistry.examples.resourcecounts)

> [!NOTE]
> <span data-ttu-id="6bb17-111">Для выполнения этого примера требуется Windows PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="6bb17-111">This example requires Windows PowerShell Core to run.</span></span>
> <span data-ttu-id="6bb17-112">Скачайте PowerShell Core для Windows, macOS или Linux по адресу https://github.com/PowerShell/PowerShell .</span><span class="sxs-lookup"><span data-stu-id="6bb17-112">Download PowerShell Core for Windows, macOS, or Linux at https://github.com/PowerShell/PowerShell.</span></span>

## <a name="importing-required-powershell-modules"></a><span data-ttu-id="6bb17-113">Импорт необходимых модулей PowerShell</span><span class="sxs-lookup"><span data-stu-id="6bb17-113">Importing Required PowerShell Modules</span></span> ##

<span data-ttu-id="6bb17-114">Если вы еще не сделали этого, клонировать [репозиторий Microsoft/тактов](https://github.com/Microsoft/Quantum), содержащий примеры и служебные программы для работы с пакетом средств разработки тактов.</span><span class="sxs-lookup"><span data-stu-id="6bb17-114">If you haven't already done so, clone the [Microsoft/Quantum repository](https://github.com/Microsoft/Quantum), which contains samples and utilities for working with the Quantum Development Kit:</span></span>

```powershell
git clone https://github.com/Microsoft/Quantum
```

<span data-ttu-id="6bb17-115">После клонирования `Microsoft/Quantum` выполните `cd` в `utilities/` папке и импортируйте модуль PowerShell для работы с DOCKER и нвчем:</span><span class="sxs-lookup"><span data-stu-id="6bb17-115">Once you've cloned `Microsoft/Quantum`, perform `cd` into the `utilities/` folder and import the PowerShell module for working with Docker and NWChem:</span></span>

```powershell
cd utilities
Import-Module InvokeNWChem.psm1
```

> [!NOTE]
> <span data-ttu-id="6bb17-116">По умолчанию Windows предотвращает выполнение скриптов или модулей в качестве меры безопасности.</span><span class="sxs-lookup"><span data-stu-id="6bb17-116">By default, Windows prevents the execution of any scripts or modules as a security measure.</span></span>
> <span data-ttu-id="6bb17-117">Чтобы разрешить выполнение модулей, таких как `Invoke-NWChem.psm1` , в Windows, может потребоваться изменить политику выполнения.</span><span class="sxs-lookup"><span data-stu-id="6bb17-117">To allow modules such as `Invoke-NWChem.psm1` to run on Windows, you may need to change the execution policy.</span></span>
> <span data-ttu-id="6bb17-118">Для этого выполните `Set-ExecutionPolicy` команду:</span><span class="sxs-lookup"><span data-stu-id="6bb17-118">To do so, run the `Set-ExecutionPolicy` command:</span></span>
> ```powershell
> Set-ExecutionPolicy RemoteSigned -Scope Process
> ```
> <span data-ttu-id="6bb17-119">После выхода из PowerShell политика выполнения будет возвращена.</span><span class="sxs-lookup"><span data-stu-id="6bb17-119">The execution policy will then be reverted when you exit PowerShell.</span></span>
> <span data-ttu-id="6bb17-120">Если вы хотите сохранить политику выполнения, используйте другое значение для `-Scope` :</span><span class="sxs-lookup"><span data-stu-id="6bb17-120">If you would like to save the execution policy, use a different value for `-Scope`:</span></span>
> ```powershell
> Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
> ```

<span data-ttu-id="6bb17-121">Теперь команда должна быть `Convert-NWChemToBroombridge` доступна:</span><span class="sxs-lookup"><span data-stu-id="6bb17-121">You should now have the `Convert-NWChemToBroombridge` command available:</span></span>

```powershell
Get-Command -Module InvokeNWChem
```

<span data-ttu-id="6bb17-122">Далее мы импортируем `Get-GateCount` команду, предоставленную в примере **жетгатекаунт** .</span><span class="sxs-lookup"><span data-stu-id="6bb17-122">Next, we'll import the `Get-GateCount` command provided with the **GetGateCount** sample.</span></span>
<span data-ttu-id="6bb17-123">Полные сведения см. в [инструкциях, приведенных в примере](https://github.com/Microsoft/Quantum/tree/master/samples/chemistry/GetGateCount).</span><span class="sxs-lookup"><span data-stu-id="6bb17-123">For full details, see the [instructions provided with the sample](https://github.com/Microsoft/Quantum/tree/master/samples/chemistry/GetGateCount).</span></span>
<span data-ttu-id="6bb17-124">Затем выполните следующую команду, заменив на `<runtime>` `win10-x64` , `osx-x64` или `linux-x64` , в зависимости от операционной системы:</span><span class="sxs-lookup"><span data-stu-id="6bb17-124">Next, run the following, substituting `<runtime>` with either `win10-x64`, `osx-x64`, or `linux-x64`, depending on your operating system:</span></span>

```powershell
cd ../Chemistry/GetGateCount
dotnet publish --self-contained -r <runtime>
Import-Module ./bin/Debug/netcoreapp2.1/<runtime>/publish/get-gatecount.dll
```

<span data-ttu-id="6bb17-125">Теперь команда должна быть `Get-GateCount` доступна:</span><span class="sxs-lookup"><span data-stu-id="6bb17-125">You should now have the `Get-GateCount` command available:</span></span>

```powershell
Get-Command Get-GateCount
```

## <a name="input-decks"></a><span data-ttu-id="6bb17-126">Колоды входных данных</span><span class="sxs-lookup"><span data-stu-id="6bb17-126">Input Decks</span></span> ##

<span data-ttu-id="6bb17-127">Пакет Нвчем принимает текстовый файл под названием « _входной лоток_ », указывающий проблему химияи такта, которую необходимо устранить, а также другие параметры, такие как параметры выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="6bb17-127">The NWChem package takes a text file called an _input deck_ which specifies a quantum chemistry problem to be solved, along with other parameters such as memory allocation settings.</span></span>
<span data-ttu-id="6bb17-128">В этом примере мы будем использовать одну из предварительно подготовленных входных колод, которые входят в состав Нвчем.</span><span class="sxs-lookup"><span data-stu-id="6bb17-128">For this example, we'll use one of the pre-made input decks that comes with NWChem.</span></span>
<span data-ttu-id="6bb17-129">Сначала клонировать [репозиторий нвчемгит/нвчем](https://github.com/nwchemgit/nwchem):</span><span class="sxs-lookup"><span data-stu-id="6bb17-129">First, clone the [nwchemgit/nwchem repository](https://github.com/nwchemgit/nwchem):</span></span>

> [!NOTE]
> <span data-ttu-id="6bb17-130">Так как это очень большой репозиторий, можно выполнить неполную клонирование, чтобы сэкономить пропускную способность и дисковое пространство с помощью `--depth 1` аргумента.</span><span class="sxs-lookup"><span data-stu-id="6bb17-130">Since this is a very large repository, we can do a shallow clone to save some bandwidth and disk space, using the `--depth 1` argument.</span></span>
> <span data-ttu-id="6bb17-131">Однако это необязательно.</span><span class="sxs-lookup"><span data-stu-id="6bb17-131">This is optional, however.</span></span>
> <span data-ttu-id="6bb17-132">Клонирование будет работать прекрасно без `--depth 1` .</span><span class="sxs-lookup"><span data-stu-id="6bb17-132">Cloning will work just fine without `--depth 1`.</span></span>

```powershell
git clone https://github.com/nwchemgit/nwchem --depth 1
```

<span data-ttu-id="6bb17-133">`nwchemgit/nwchem`Репозиторий поставляется с различными колодами входных данных, предназначенными для использования с пакетом средств разработки тактов, которые перечислены в [ `QA/chem_library_tests` папке](https://github.com/nwchemgit/nwchem/tree/master/QA/chem_library_tests).</span><span class="sxs-lookup"><span data-stu-id="6bb17-133">The `nwchemgit/nwchem` repository comes with a variety of input decks intended for use with the Quantum Development Kit, listed under the [`QA/chem_library_tests` folder](https://github.com/nwchemgit/nwchem/tree/master/QA/chem_library_tests).</span></span>
<span data-ttu-id="6bb17-134">В этом примере мы будем использовать `H4` колоду входных данных:</span><span class="sxs-lookup"><span data-stu-id="6bb17-134">For this example, we'll use the `H4` input deck:</span></span>

```powershell
cd nwchem/QA/chem_library_tests/H4
Get-Content h4_sto6g_0.000.nw
```

<span data-ttu-id="6bb17-135">Молекула в вопросе — это система из 4 атомов водорода, которые расположены в определенной геометрической области, которая зависит от одного угла, параметра, `alpha` как указано в названии `h4_sto6g_alpha.nw` колоды.</span><span class="sxs-lookup"><span data-stu-id="6bb17-135">The molecule in question is a system of 4 hydrogen atoms that are arranged in a certain geometry that depends on one angle, the parameter `alpha` as indicated in the name `h4_sto6g_alpha.nw` of the deck.</span></span> <span data-ttu-id="6bb17-136">H4 — это известный [тест производительности молекулярное](https://onlinelibrary.wiley.com/doi/abs/10.1002/qua.560180511) для вычислительных химия с момента 1970-х.</span><span class="sxs-lookup"><span data-stu-id="6bb17-136">H4 is a known [molecular benchmark](https://onlinelibrary.wiley.com/doi/abs/10.1002/qua.560180511) for computational chemistry since the 1970s.</span></span> <span data-ttu-id="6bb17-137">Параметр указывает на то `sto6g` , что колода реализует представление по отношению к Слатер-типу Орбитал, в частности, представление с учетом [набора сохранены-NG](https://en.wikipedia.org/wiki/STO-nG_basis_sets) с 6 функциями, основанными на уровне a.</span><span class="sxs-lookup"><span data-stu-id="6bb17-137">The parameter `sto6g` is indicative that the deck implements a representation with respect to a Slater-type orbital, specifically, a representation with respect to an [STO-nG basis set](https://en.wikipedia.org/wiki/STO-nG_basis_sets) with 6 Gaussian basis functions.</span></span> <span data-ttu-id="6bb17-138">Этот входной лоток более подробно содержит несколько инструкций для подсистемы Нвчем тензорные (обработки TCE), которая направляет Нвчем для получения информации, необходимой для взаимодействия с пакетом разработки тактов.</span><span class="sxs-lookup"><span data-stu-id="6bb17-138">This input deck furthermore contains several instructions to the NWChem Tensor Contraction Engine (TCE) that direct NWChem to produce the information needed for interoperating with the Quantum Development Kit:</span></span>

```
...
set tce:print_integrals T
set tce:qorb 18
set tce:qela  9
set tce:qelb  9
```

## <a name="producing-and-consuming-broombridge-output-from-nwchem"></a><span data-ttu-id="6bb17-139">Создание и использование выходных данных Брумбридже из Нвчем</span><span class="sxs-lookup"><span data-stu-id="6bb17-139">Producing and Consuming Broombridge Output from NWChem</span></span> ##

<span data-ttu-id="6bb17-140">Теперь у вас есть все, что нужно для создания и использования документов Брумбридже.</span><span class="sxs-lookup"><span data-stu-id="6bb17-140">You now have everything you need to produce and consume Broombridge documents.</span></span>
<span data-ttu-id="6bb17-141">Чтобы запустить Нвчем и создать документ Брумбридже для `h4_sto6g_0.000.nw` входной колоды, выполните `Convert-NWChemToBroombridge` :</span><span class="sxs-lookup"><span data-stu-id="6bb17-141">To run NWChem and produce a Broombridge document for the `h4_sto6g_0.000.nw` input deck, run `Convert-NWChemToBroombridge`:</span></span>

> [!NOTE]
> <span data-ttu-id="6bb17-142">При первом выполнении этой команды DOCKER загрузит `nwchemorg/nwchem-qc` образ.</span><span class="sxs-lookup"><span data-stu-id="6bb17-142">The first time you run this command, Docker will download the `nwchemorg/nwchem-qc` image for you.</span></span>
> <span data-ttu-id="6bb17-143">Это может занять некоторое время, в зависимости от скорости подключения, возможно, предоставляя возможность получить чашку кофе.</span><span class="sxs-lookup"><span data-stu-id="6bb17-143">This may take a little while, depending on your connection speed, possibly providing an opportunity to get a cup of coffee.</span></span>

```powershell
Convert-NWChemToBroombridge h4_sto6g_0.000.nw 
```

<span data-ttu-id="6bb17-144">Это приведет к созданию документа Брумбридже `h4_sto6g_0.000.yaml` , который можно использовать с `Get-GateCount` :</span><span class="sxs-lookup"><span data-stu-id="6bb17-144">This will produce a Broombridge document called `h4_sto6g_0.000.yaml` that you can use with `Get-GateCount`:</span></span>

```powershell
Get-GateCount -Format YAML h4_sto6g_0.000.yaml
```

<span data-ttu-id="6bb17-145">Теперь должны отобразиться выходные данные консоли, которые содержат оценку ресурсов, например T-Count, число поворотов, число кнот и т. д., для различных методов моделирования такта:</span><span class="sxs-lookup"><span data-stu-id="6bb17-145">You should now see console output which contains resource estimation such as T-count, rotations count, CNOT count, etc. for various quantum simulation methods:</span></span>

```powershell 
IntegralDataPath    : C:\Users\martinro\REPOS\nwchem\qa\chem_library_tests\h4\h4_sto6g_0.000.yaml
HamiltonianName     : hamiltonian_0
SpinOrbitals        : 8
Method              : Trotter
TCount              : 0
RotationsCount      : 92
CNOTCount           : 520
ElapsedMilliseconds : 327

IntegralDataPath    : C:\Users\martinro\REPOS\nwchem\qa\chem_library_tests\h4\h4_sto6g_0.000.yaml
HamiltonianName     : hamiltonian_0
SpinOrbitals        : 8
Method              : Qubitization
TCount              : 438
RotationsCount      : 516
CNOTCount           : 2150
ElapsedMilliseconds : 528

IntegralDataPath    : C:\Users\martinro\REPOS\nwchem\qa\chem_library_tests\h4\h4_sto6g_0.000.yaml
HamiltonianName     : hamiltonian_0
SpinOrbitals        : 8
Method              : Optimized Qubitization
TCount              : 3540
RotationsCount      : 18
CNOTCount           : 7932
ElapsedMilliseconds : 721
```

<span data-ttu-id="6bb17-146">Здесь есть много вещей:</span><span class="sxs-lookup"><span data-stu-id="6bb17-146">There are many things to go do from here:</span></span> 
- <span data-ttu-id="6bb17-147">Попробуйте использовать различные предопределенные колоды ввода, например, путем изменения параметра `alpha` в `h4_sto6g_alpha.nw` ,</span><span class="sxs-lookup"><span data-stu-id="6bb17-147">Try out different predefined input decks, e.g., by varying the parameter `alpha` in `h4_sto6g_alpha.nw`,</span></span> 
- <span data-ttu-id="6bb17-148">Попробуйте изменить колоды, изменив Нвчем колоды напрямую, например, просмотрев `STO-nG` модели для различных вариантов выбора n,</span><span class="sxs-lookup"><span data-stu-id="6bb17-148">Try modifying the decks by editing the NWChem decks directly, e.g., exploring `STO-nG` models for various choices of n,</span></span> 
- <span data-ttu-id="6bb17-149">Опробуйте другие предопределенные Нвчем входные колоды, доступные в `nwchem/qa/chem_library_tests` ,</span><span class="sxs-lookup"><span data-stu-id="6bb17-149">Try other predefined NWChem input decks that are available at `nwchem/qa/chem_library_tests`,</span></span>
- <span data-ttu-id="6bb17-150">Испытайте набор предопределенных тестов производительности Брумбридже YAML, созданных из Нвчем и доступных в составе [репозитория Microsoft/такта](https://github.com/Microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML).</span><span class="sxs-lookup"><span data-stu-id="6bb17-150">Try out a suite of predefined Broombridge YAML benchmarks that were generated from NWChem and are available as part of the [Microsoft/Quantum repository](https://github.com/Microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML).</span></span> <span data-ttu-id="6bb17-151">Ниже перечислены эти тесты производительности.</span><span class="sxs-lookup"><span data-stu-id="6bb17-151">These benchmarks include:</span></span> 
    - <span data-ttu-id="6bb17-152">небольшие молекулы, такие как молекулярное водо(H2), БериллиУМ (быть), литий хидриде (лих),</span><span class="sxs-lookup"><span data-stu-id="6bb17-152">small molecules such as molecular hydrogen (H2), Beryllium (Be), Lithium hydride (LiH),</span></span>
    - <span data-ttu-id="6bb17-153">более крупные молекулы, такие как озоне (O3), Beta-каротене, цитосине и многие другие.</span><span class="sxs-lookup"><span data-stu-id="6bb17-153">larger molecules such as ozone (O3), beta-carotene, cytosine, and many more.</span></span> 
- <span data-ttu-id="6bb17-154">Испытайте графические [стрелки емсл](https://arrows.emsl.pnnl.gov/api/qsharp_chem) , которые применяют интерфейс к Microsoft Quantum Development Kit.</span><span class="sxs-lookup"><span data-stu-id="6bb17-154">Try out the graphical front-end [EMSL Arrows](https://arrows.emsl.pnnl.gov/api/qsharp_chem) that features an interface to the Microsoft Quantum Development Kit.</span></span> 


## <a name="producing-broombridge-output-from-emsl-arrows"></a><span data-ttu-id="6bb17-155">Создание выходных данных Брумбридже из стрелок ЕМСЛ</span><span class="sxs-lookup"><span data-stu-id="6bb17-155">Producing Broombridge Output from EMSL Arrows</span></span> ##

<span data-ttu-id="6bb17-156">Чтобы приступить к работе с веб-интерфейсными стрелками ЕМСЛ, перейдите в [браузере.](https://arrows.emsl.pnnl.gov/api/qsharp_chem)</span><span class="sxs-lookup"><span data-stu-id="6bb17-156">To get started with web-based front end EMSL Arrows, navigate a browser [here](https://arrows.emsl.pnnl.gov/api/qsharp_chem).</span></span> 

> [!NOTE]
> <span data-ttu-id="6bb17-157">Для запуска стрелок ЕМСЛ в веб-браузере необходимо включить JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6bb17-157">Running EMSL Arrows in a web browser requires JavaScript to be enabled.</span></span> <span data-ttu-id="6bb17-158">Дополнительные сведения о включении JavaScript в браузере см. в этих [инструкциях](https://www.enable-javascript.com/) .</span><span class="sxs-lookup"><span data-stu-id="6bb17-158">Please refer to these [instructions](https://www.enable-javascript.com/) on how to enable JavaScript in your browser.</span></span> 

<span data-ttu-id="6bb17-159">Сначала введите молекулу в поле запроса с текстом``Enter an esmiles, esmiles reaction, or other Arrows input, then push the "Run Arrows" button.``</span><span class="sxs-lookup"><span data-stu-id="6bb17-159">First, enter a molecule in the query box that says ``Enter an esmiles, esmiles reaction, or other Arrows input, then push the "Run Arrows" button.``</span></span> 

<span data-ttu-id="6bb17-160">Можно ввести множество молекул по имени разговорной речи, например "каффеине" вместо "1, 3, 7-Тримесилксансине".</span><span class="sxs-lookup"><span data-stu-id="6bb17-160">You can enter many molecules by their colloquial name, such as "caffeine" instead of "1,3,7-Trimethylxanthine".</span></span> 

<span data-ttu-id="6bb17-161">Затем нажмите кнопку с текстом ``theory{qsharp_chem}`` .</span><span class="sxs-lookup"><span data-stu-id="6bb17-161">Next, click the button that says ``theory{qsharp_chem}``.</span></span> <span data-ttu-id="6bb17-162">После этого в поле запроса будет помещена инструкция, которая сообщит приложению выполнить экспорт выходных данных в формате Брумбридже YAML.</span><span class="sxs-lookup"><span data-stu-id="6bb17-162">This will populate the query box further with an instruction that will tell the run to export output in the Broombridge YAML format.</span></span> 

<span data-ttu-id="6bb17-163">Теперь синхронизируйте время ``Run Arrows`` .</span><span class="sxs-lookup"><span data-stu-id="6bb17-163">Now, clock on ``Run Arrows``.</span></span> <span data-ttu-id="6bb17-164">В зависимости от размера входных данных это может занять некоторое время.</span><span class="sxs-lookup"><span data-stu-id="6bb17-164">Depending on the size of the input, this might take a while.</span></span> <span data-ttu-id="6bb17-165">Или, если конкретная модель уже была вычислена ранее, ее можно выполнить очень быстро, так как она будет считаться только уточняющим запросом в базе данных.</span><span class="sxs-lookup"><span data-stu-id="6bb17-165">Or, in case the particular model has already been computed before, it can be done extremely fast as it will only amount to a lookup in a database.</span></span> <span data-ttu-id="6bb17-166">В любом случае вы перейдете на новую страницу, содержащую множество сведений о конкретном запуске Нвчем в колоде, заданной входными данными.</span><span class="sxs-lookup"><span data-stu-id="6bb17-166">In either case, you will be taken to a new page that contains a plethora of information about the particular run of NWChem against the deck specified by your input.</span></span> 

<span data-ttu-id="6bb17-167">Вы можете скачать и сохранить файл Брумбридже YAML из раздела, который начинается со следующего заголовка:</span><span class="sxs-lookup"><span data-stu-id="6bb17-167">You can download and save the Broombridge YAML file from the section that starts with the following header:</span></span> 
```powershell
+==================================================+
||              Molecular Calculation             ||
+==================================================+

Id     = 48443

NWOutput = Link to NWChem Output (download)

Datafiles:
qsharp_chem.yaml-2018-10-23-14:37:42 (download)
...
```

<span data-ttu-id="6bb17-168">Нажмите кнопку ``download`` «вкл.», чтобы сохранить локальную копию с уникальным именем файла, например ``qsharp_chem48443.yaml`` (конкретное имя будет отличаться для каждого запуска).</span><span class="sxs-lookup"><span data-stu-id="6bb17-168">Click on ``download``, which saves a local copy with a unique file name such as ``qsharp_chem48443.yaml`` (the particular name will be different for each run).</span></span> <span data-ttu-id="6bb17-169">Затем можно выполнить дальнейшую обработку этого файла, например, с помощью</span><span class="sxs-lookup"><span data-stu-id="6bb17-169">You can then further process this file as above, e.g., with</span></span> 
```powershell
Get-GateCount -Format YAML qsharp_chem48443.yaml
```
<span data-ttu-id="6bb17-170">для получения количества ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6bb17-170">to get resource counts.</span></span> 

<span data-ttu-id="6bb17-171">Вы можете использовать построитель трехмерной молекулы, доступ к которому можно получить с ``Arrows Entry - 3D Builder`` вкладки на начальной странице стрелок емсл.</span><span class="sxs-lookup"><span data-stu-id="6bb17-171">You might enjoy the 3D molecule builder that can be accessed from the ``Arrows Entry - 3D Builder`` tab on the EMSL Arrows start page.</span></span> <span data-ttu-id="6bb17-172">Щелкнув [жсмол](http://wiki.jmol.org/index.php/JSmol) трехмерный рисунок указанной молекулы, вы сможете изменить ее.</span><span class="sxs-lookup"><span data-stu-id="6bb17-172">Clicking the [JSMol](http://wiki.jmol.org/index.php/JSmol) 3D picture of the shown molecule will let you allow to edit it.</span></span> <span data-ttu-id="6bb17-173">Можно перемещать атомы, перетаскивая атомы, чтобы их межмолекулярноеные расстояния изменялись, добавляют и удаляют атомы и т. д. Для каждого из этих вариантов после добавления ``theory{qsharp_chem}`` в поле запроса можно создать экземпляр схемы БРУМБРИДЖЕ YAML и дополнительно исследовать его с помощью библиотеки тактов химия.</span><span class="sxs-lookup"><span data-stu-id="6bb17-173">You can move atoms around, drag atoms apart so that their inter-molecular distances change, add/remove atoms, etc. For each of these choices, once you added ``theory{qsharp_chem}`` in the query box, you can then generate an instance of the Broombridge YAML schema and further explore it using the Quantum Chemistry Library.</span></span> 
