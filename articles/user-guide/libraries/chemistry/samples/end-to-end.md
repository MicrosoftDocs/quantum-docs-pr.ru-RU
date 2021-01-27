---
title: Пример Нвчем тактовой программы
description: С помощью колоды входных данных Нвчем рассмотрим пример получения счетчиков шлюзов для моделирования тактов химия.
author: cgranade
ms.author: chgranad
ms.date: 10/23/2018
ms.topic: sample
uid: microsoft.quantum.chemistry.examples.endtoend
no-loc:
- Q#
- $$v
ms.openlocfilehash: e0ec7dcbdccbab5c81177a4223c71fd3f2ce57d8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847780"
---
# <a name="end-to-end-with-nwchem"></a>Полный цикл работы с NWChem #

В этой статье вы узнаете пример получения счетчиков шлюзов для моделирования тактовой химия, начиная с колоды входных данных [нвчем](http://www.nwchem-sw.org/index.php/Main_Page) .
Прежде чем продолжить работу с этим примером, убедитесь, что вы установили DOCKER, следуя [инструкциям по установке и проверке](xref:microsoft.quantum.chemistry.concepts.installation).

Дополнительные сведения
- [Структура Нвчем входных колод](https://github.com/nwchemgit/nwchem/wiki/Getting-Started#input-file-structure)
    - [Команды колоды ввода для использования с пакетом разработки тактов](https://github.com/nwchemgit/nwchem/tree/main/contrib/quasar)
- [Установка библиотеки и зависимостей химия](xref:microsoft.quantum.chemistry.concepts.installation)
- [Подсчет ресурсов](xref:microsoft.quantum.chemistry.examples.resourcecounts)

> [!NOTE]
> Для выполнения этого примера требуется Windows PowerShell Core.
> Скачайте PowerShell Core для Windows, macOS или Linux по адресу https://github.com/PowerShell/PowerShell .

## <a name="importing-required-powershell-modules"></a>Импорт необходимых модулей PowerShell ##

Если вы еще не сделали этого, клонировать [репозиторий Microsoft/тактов](https://github.com/Microsoft/Quantum), содержащий примеры и служебные программы для работы с пакетом средств разработки тактов.

```powershell
git clone https://github.com/Microsoft/Quantum
```

После клонирования `Microsoft/Quantum` выполните `cd` в `utilities/` папке и импортируйте модуль PowerShell для работы с DOCKER и нвчем:

```powershell
cd utilities
Import-Module InvokeNWChem.psm1
```

> [!NOTE]
> По умолчанию Windows предотвращает запуск скриптов или модулей в качестве меры безопасности.
> Чтобы разрешить выполнение модулей, таких как `Invoke-NWChem.psm1` , в Windows, может потребоваться изменить политику.
> Для этого выполните `Set-ExecutionPolicy` команду:
> ```powershell
> Set-ExecutionPolicy RemoteSigned -Scope Process
> ```
> Политика будет отменена при выходе из PowerShell.
> Если вы хотите сохранить политику, используйте другое значение для `-Scope` :
> ```powershell
> Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
> ```

Теперь команда должна быть `Convert-NWChemToBroombridge` доступна:

```powershell
Get-Command -Module InvokeNWChem
```

Далее мы импортируем `Get-GateCount` команду, предоставленную в примере **жетгатекаунт** .
Полные сведения см. в [инструкциях, приведенных в примере](https://github.com/Microsoft/Quantum/tree/main/samples/chemistry/GetGateCount).
Затем выполните следующую команду, заменив на `<runtime>` `win10-x64` , `osx-x64` или `linux-x64` , в зависимости от операционной системы:

```powershell
cd ../Chemistry/GetGateCount
dotnet publish --self-contained -r <runtime>
Import-Module ./bin/Debug/netcoreapp2.1/<runtime>/publish/get-gatecount.dll
```

Теперь команда должна быть `Get-GateCount` доступна:

```powershell
Get-Command Get-GateCount
```

## <a name="input-decks"></a>Колоды входных данных ##

Пакет Нвчем принимает текстовый файл под названием « _входной лоток_ », указывающий проблему химияи такта, которую необходимо устранить, а также другие параметры, такие как параметры выделения памяти.
В этом примере мы будем использовать одну из предварительно подготовленных входных колод, которые входят в состав Нвчем.
Сначала клонировать [репозиторий нвчемгит/нвчем](https://github.com/nwchemgit/nwchem):

> [!NOTE]
> Так как это очень большой репозиторий, можно выполнить неполную клонирование, чтобы сэкономить пропускную способность и дисковое пространство с помощью `--depth 1` аргумента.
> Однако это необязательно.
> Клонирование будет работать прекрасно без `--depth 1` .

```powershell
git clone https://github.com/nwchemgit/nwchem --depth 1
```

`nwchemgit/nwchem`Репозиторий поставляется с различными колодами входных данных, предназначенными для использования с пакетом средств разработки тактов, которые перечислены в [ `QA/chem_library_tests` папке](https://github.com/nwchemgit/nwchem/tree/main/QA/chem_library_tests).
В этом примере мы будем использовать `H4` колоду входных данных:

```powershell
cd nwchem/QA/chem_library_tests/H4
Get-Content h4_sto6g_0.000.nw
```

Молекула в вопросе — это система из 4 атомов водорода, которые расположены в определенной геометрической области, которая зависит от одного угла, параметра, `alpha` как указано в названии `h4_sto6g_alpha.nw` колоды. H4 — это известный [тест производительности молекулярное](https://onlinelibrary.wiley.com/doi/abs/10.1002/qua.560180511) для вычислительных химия с момента 1970-х. Параметр указывает на то `sto6g` , что колода реализует представление по отношению к Слатер-типу Орбитал, в частности, представление с учетом [набора сохранены-NG](https://en.wikipedia.org/wiki/STO-nG_basis_sets) с 6 функциями, основанными на уровне a. Этот входной лоток более подробно содержит несколько инструкций для подсистемы Нвчем тензорные (обработки TCE), которая направляет Нвчем для получения информации, необходимой для взаимодействия с пакетом разработки тактов.

```
...
set tce:print_integrals T
set tce:qorb 18
set tce:qela  9
set tce:qelb  9
```

## <a name="producing-and-consuming-broombridge-output-from-nwchem"></a>Создание и использование выходных данных Брумбридже из Нвчем ##

Теперь у вас есть все, что нужно для создания и использования документов Брумбридже.
Чтобы запустить Нвчем и создать документ Брумбридже для `h4_sto6g_0.000.nw` входной колоды, выполните `Convert-NWChemToBroombridge` :

> [!NOTE]
> При первом выполнении этой команды DOCKER загрузит `nwchemorg/nwchem-qc` образ.
> Это может занять некоторое время, в зависимости от скорости подключения, возможно, предоставляя возможность получить чашку кофе.

```powershell
Convert-NWChemToBroombridge h4_sto6g_0.000.nw 
```

Это приведет к созданию документа Брумбридже `h4_sto6g_0.000.yaml` , который можно использовать с `Get-GateCount` :

```powershell
Get-GateCount -Format YAML h4_sto6g_0.000.yaml
```

Теперь должны отобразиться выходные данные консоли, которые содержат оценку ресурсов, например T-Count, число поворотов, число кнот и т. д., для различных методов моделирования такта:

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

Здесь есть много вещей: 
- Попробуйте использовать различные предопределенные колоды ввода, например, путем изменения параметра `alpha` в `h4_sto6g_alpha.nw` , 
- Попробуйте изменить колоды, изменив Нвчем колоды напрямую, например, просмотрев `STO-nG` модели для различных вариантов выбора n, 
- Опробуйте другие предопределенные Нвчем входные колоды, доступные в `nwchem/qa/chem_library_tests` ,
- Испытайте набор предопределенных тестов производительности Брумбридже YAML, созданных из Нвчем и доступных в составе [репозитория Microsoft/такта](https://github.com/Microsoft/Quantum/tree/main/samples/chemistry/IntegralData/YAML). Ниже перечислены эти тесты производительности. 
    - небольшие молекулы, такие как молекулярное водо(H2), БериллиУМ (быть), литий хидриде (лих),
    - более крупные молекулы, такие как озоне (O3), Beta-каротене, цитосине и многие другие. 
- Испытайте графические [стрелки емсл](https://arrows.emsl.pnnl.gov/api/qsharp_chem) , которые применяют интерфейс к Microsoft Quantum Development Kit. 


## <a name="producing-broombridge-output-from-emsl-arrows"></a>Создание выходных данных Брумбридже из стрелок ЕМСЛ ##

Чтобы приступить к работе с веб-интерфейсными стрелками ЕМСЛ, перейдите в [браузере.](https://arrows.emsl.pnnl.gov/api/qsharp_chem) 

> [!NOTE]
> Для запуска стрелок ЕМСЛ в веб-браузере необходимо включить JavaScript. Дополнительные сведения о включении JavaScript в браузере см. в этих [инструкциях](https://www.enable-javascript.com/) . 

Сначала введите молекулу в поле запроса с текстом ``Enter an esmiles, esmiles reaction, or other Arrows input, then push the "Run Arrows" button.`` 

Можно ввести множество молекул по имени разговорной речи, например "каффеине" вместо "1, 3, 7-Тримесилксансине". 

Затем нажмите кнопку с текстом ``theory{qsharp_chem}`` . После этого в поле запроса будет помещена инструкция, которая сообщит приложению выполнить экспорт выходных данных в формате Брумбридже YAML. 

Теперь синхронизируйте время ``Run Arrows`` . В зависимости от размера входных данных это может занять некоторое время. Или, если конкретная модель уже была вычислена ранее, ее можно выполнить очень быстро, так как она будет считаться только уточняющим запросом в базе данных. В любом случае вы перейдете на новую страницу, содержащую множество сведений о конкретном запуске Нвчем в колоде, заданной входными данными. 

Вы можете скачать и сохранить файл Брумбридже YAML из раздела, который начинается со следующего заголовка: 
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

Нажмите кнопку ``download`` «вкл.», чтобы сохранить локальную копию с уникальным именем файла, например ``qsharp_chem48443.yaml`` (конкретное имя будет отличаться для каждого запуска). Затем можно выполнить дальнейшую обработку этого файла, например, с помощью 
```powershell
Get-GateCount -Format YAML qsharp_chem48443.yaml
```
для получения количества ресурсов. 

Вы можете использовать построитель трехмерной молекулы, доступ к которому можно получить с ``Arrows Entry - 3D Builder`` вкладки на начальной странице стрелок емсл. Щелкнув [жсмол](http://wiki.jmol.org/index.php/JSmol) трехмерный рисунок указанной молекулы, вы сможете изменить ее. Можно перемещать атомы, перетаскивая атомы, чтобы их межмолекулярноеные расстояния изменялись, добавляют и удаляют атомы и т. д. Для каждого из этих вариантов после добавления ``theory{qsharp_chem}`` в поле запроса можно создать экземпляр схемы БРУМБРИДЖЕ YAML и дополнительно исследовать его с помощью библиотеки тактов химия. 
