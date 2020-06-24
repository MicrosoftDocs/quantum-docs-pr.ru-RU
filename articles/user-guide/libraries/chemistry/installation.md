---
title: 'Установка и проверка библиотеки Microsoft Q # химия'
description: Узнайте, как установить библиотеку Microsoft тактов химия и использовать ее с Нвчем вычислительной химия платформой.
author: guanghaolow
ms.author: gulow
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.chemistry.concepts.installation
ms.openlocfilehash: 48bf7bc980e238e622053f5c2bdd09604c572596
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2020
ms.locfileid: "85276101"
---
# <a name="chemistry-library-installation-and-validation"></a>Установка и проверка библиотеки химия

Пакет средств разработки тактов обеспечивает поддержку приложений тактовой химия с помощью [`Microsoft.Quantum.Chemistry`](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) пакета NuGet.
Как и в случае с другими пакетами NuGet, добавление библиотеки химия в проект несложно.

**Visual Studio 2019:** При использовании Visual Studio 2019 можно добавить пакеты тактовой химия с помощью диспетчера пакетов NuGet.
Чтобы открыть диспетчер пакетов, щелкните правой кнопкой мыши проект, в который вы хотите добавить библиотеку химия, и выберите пункт "Управление пакетами NuGet...", как показано на снимке экрана ниже.

![Использование диспетчера пакетов NuGet в Visual Studio 2019](~/media/vs2017-nuget-manage-packages.png)

На вкладке Обзор найдите имя пакета Microsoft. такт. химия.

> [!NOTE]
> Обязательно пометка "включить предварительные выпуски".

![Флажок "включить предварительные выпуски"](~/media/vs2017-nuget-package-search.png)

В этом списке будут перечислены пакеты, доступные для загрузки.
Щелкните элемент "Microsoft. тактов. Химия" в левой области, выберите последнюю предварительную версию на правой панели и нажмите кнопку "установить":

![Установка последнего пакета Microsoft. Тактing. Химия](~/media/vs2017-nuget-select-chem.png)

Дополнительные сведения см. в разделе [Путеводитель по пользовательскому интерфейсу диспетчера пакетов](https://docs.microsoft.com/nuget/tools/package-manager-ui).

Кроме того, с помощью консоли диспетчера пакетов можно добавить в проект библиотеку тактов химия с помощью интерфейса командной строки.

![Использование консоли диспетчера пакетов из командной строки](~/media/vs2017-nuget-console-menu.png)

В консоли диспетчера пакетов выполните следующую команду:

```
Install-Package Microsoft.Quantum.Chemistry
```

Дополнительные сведения см. в разделе [руководств по консоли диспетчера пакетов](https://docs.microsoft.com/nuget/tools/package-manager-console).

**Командная строка или Visual Studio Code:** Используя командную строку самостоятельно или в Visual Studio Code, можно `dotnet` Добавить ссылку на пакет NuGet в проект с помощью команды.

```dotnetcli
dotnet add package Microsoft.Quantum.Chemistry
```

## <a name="verifying-your-installation"></a>Проверка установки 

Как и в остальной части пакета средств разработки тактов, в библиотеке тактов химия имеется ряд полностью документированных примеров, которые помогут быстро приступить к работе.
Чтобы проверить установку с помощью этих примеров, выполните клонирование [основного репозитория примеров](https://github.com/Microsoft/Quantum), а затем запустите один из примеров.  Например, чтобы запустить [`MolecularHydrogen`](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/MolecularHydrogen) Пример:

```bash
git clone https://github.com/Microsoft/Quantum.git
cd Quantum/samples/chemistry/MolecularHydrogen
dotnet run
```

Чтобы проверить установку библиотеки тактов химия с помощью Microsoft Visual Studio после клонирования репозитория:
    1. Откройте решение Чемистрисамплес. sln в папке химия.  
    2. Выберите Samples/1. Простые молекулы/Молекулархидрожен в качестве запускаемого проекта.
    3. Нажмите клавишу F5, чтобы запустить демонстрацию оценки этапа молекулярное водорода.

Дополнительные сведения об оценке значений уровней энергии см. в разделе [получение оценок уровня энергии](xref:microsoft.quantum.chemistry.examples.energyestimate) .   


## <a name="using-the-quantum-development-kit-with-nwchem"></a>Использование пакета средств разработки тактов с Нвчем ##

В примере Молекулархидрожен используются входные данные молекулярное, настроенные вручную.  Хотя это и удобно для небольших примеров, тактовая химия в масштабе требует Хамилтонианс с миллионами или миллиардами терминов. Такие Хамилтонианс, созданные масштабируемыми вычислительными пакетами химия, слишком велики для импорта вручную. 

Библиотека тактовой химия для пакета разработки такта разработана для работы с вычислительными пакетами химия, которая, в первую очередь, является [**нвчем**](http://www.nwchem-sw.org/) вычислительной химияной платформой, разработанной лабораторией молекулярное SCIENCES (емсл) в северо-западной национальной лаборатории.
В частности, `Microsoft.Quantum.Chemistry` пакет предоставляет средства для загрузки экземпляров проблем моделирования тактов химия, представленных в [схеме брумбридже](xref:microsoft.quantum.libraries.chemistry.schema.broombridge), которые также поддерживаются для экспорта в последних версиях нвчем.

Чтобы начать работу с помощью Нвчем вместе с пакетом средств разработки тактов, мы предлагаем один из следующих методов:
- Начните работу с существующих файлов Брумбридже, предоставленных в примерах на сайте [интегралдата/YAML](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML).
- Используйте [Построитель стрелок емсл для Microsoft Quantum Development Kit](https://arrows.emsl.pnnl.gov/api/qsharp_chem) , который является веб-интерфейсом для нвчем, для создания новых входных файлов брумбридже с форматом молекулярное.  
- Используйте [образ DOCKER](https://hub.docker.com/r/nwchemorg/nwchem-qc/) , предоставленный пннл для запуска нвчем, или
- [Скомпилируйте нвчем](http://www.nwchem-sw.org/index.php/Compiling_NWChem) для своей платформы.

Дополнительные сведения о работе с Нвчем для химических моделей для анализа с помощью библиотеки химия пакета персонала [Kit см. в этой](xref:microsoft.quantum.chemistry.examples.endtoend) статье.

### <a name="getting-started-using-broombridge-files-provided-with-the-samples"></a>Приступая к работе с файлами Брумбридже, поставляемыми с образцами

Папка [интегралдата/YAML](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML) в репозитории примеров пакета разработки тактов содержит файлы данных с брумбридже форматом.  

В качестве простого примера используйте пример библиотеки химия, [жетгатекаунт](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/GetGateCount) , чтобы загрузить хамилтониан из одного из брумбридже файлов и выполнить прогнозное моделирование алгоригсмс:

```bash
cd Quantum/Chemistry/GetGateCount
dotnet run -- --path=../IntegralData/YAML/h2.yaml --format=YAML
```

Дополнительные сведения о том, как ввести молекулы, представленные схемой Брумбридже, см. в разделе [Загрузка хамилтониан из файла](xref:microsoft.quantum.chemistry.examples.loadhamiltonian) .  

Дополнительные сведения об оценке ресурсов см. в разделе [Получение количества ресурсов](xref:microsoft.quantum.chemistry.examples.resourcecounts) .  

### <a name="getting-started-using-the-emsl-arrows-builder"></a>Приступая к работе с построителем стрелок ЕМСЛ

Стрелки ЕМСЛ — это средство, которое использует Нвчем и химические вычислительные базы данных для создания данных молекулы.  [Построитель стрелок емсл для Microsoft Quantum Development Kit](https://arrows.emsl.pnnl.gov/api/qsharp_chem) позволяет ввести модель с помощью нескольких построителей Молекулярное моделей и создать файл брумбридже, который будет использоваться пакетом разработки тактов.  

На странице ЕМСЛ щелкните вкладку ["Инстуктионс"] и следуйте инструкциям ["простые примеры"], чтобы создать файлы Брумбридже.  Затем попробуйте запустить [' Жетгатекаунт '], чтобы просмотреть оценки ресурсов такта для этих молекул.

### <a name="installing-nwchem-from-source"></a>Установка Нвчем из источника

Полные инструкции по установке Нвчем из источника [предоставляются пннл](http://www.nwchem-sw.org/index.php/Compiling_NWChem).

> [!TIP]
> Если вы хотите использовать Нвчем из Windows 10, то подсистема Windows для Linux является отличным вариантом.
> После установки [Ubuntu 18,04 LTS для Windows](https://www.microsoft.com/en-us/p/ubuntu-1804-lts/9n9tngvndl3q#activetab=pivot:overviewtab)запустите `ubuntu18.04` из любимого терминала и следуйте инструкциям выше, чтобы установить нвчем из источника.

После компиляции Нвчем из источника можно запустить `yaml_driver` сценарий, поставляемый с нвчем, чтобы быстро создавать экземпляры брумбридже из нвчем входных колод:

```bash
$NWCHEM_TOP/contrib/quasar/yaml_driver input.nw
```

Эта команда создаст новый `input.yaml` файл в формате брумбридже в текущем каталоге.

### <a name="using-nwchem-with-docker"></a>Использование Нвчем с DOCKER

Предварительно созданные образы для использования Нвчем доступны в разных платформах через [центр DOCKER](https://hub.docker.com).
Чтобы приступить к работе, следуйте инструкциям по установке DOCKER для своей платформы:

- [Установка DOCKER для Ubuntu](https://docs.docker.com/install/linux/docker-ce/ubuntu/)
- [Установка DOCKER для macOS](https://docs.docker.com/docker-for-mac/install/)
- [Установка Docker для Windows 10](https://docs.docker.com/docker-for-windows/install/)

> [!TIP]
> При использовании Docker для Windows необходимо предоставить общий доступ к диску, содержащему временный каталог (обычно это `C:\` диск), с помощью управляющей программы DOCKER. Дополнительные сведения см. в [документации по DOCKER](https://docs.docker.com/docker-for-windows/#shared-drives) .

После установки DOCKER можно использовать модуль PowerShell, поставляемый с примерами пакета разработки такта, для запуска образа, или можно запустить образ вручную.
Мы подробно будем использовать PowerShell. Если вы хотите использовать образ DOCKER вручную, обратитесь к [документации, поставляемой с этим изображением](https://hub.docker.com/r/nwchemorg/nwchem-qc/).

#### <a name="running-nwchem-through-powershell-core"></a>Выполнение Нвчем с помощью PowerShell Core

Чтобы использовать образ DOCKER Нвчем с пакетом разработки тактов, мы предоставляем небольшой модуль PowerShell, который обрабатывает перемещение файлов в Нвчем и из него.
Если вы еще не установили PowerShell Core, можно скачать его кросс-платформенную версию из [репозитория PowerShell на сайте GitHub](https://github.com/PowerShell/PowerShell#get-powershell).

> [!NOTE]
> PowerShell Core также используется в некоторых примерах для демонстрации взаимодействия с рабочими процессами обработки и анализа данных и бизнес-аналитики.

После установки PowerShell Core выполните импорт, `InvokeNWChem.psm1` чтобы сделать команды нвчем доступными в текущем сеансе:

```powershell
cd Quantum/utilities/
Import-Module ./InvokeNWChem.psm1
```

Это сделает `Convert-NWChemToBroombridge` команду доступной в текущем сеансе PowerShell.
Чтобы скачать все необходимые образы из DOCKER и использовать их для запуска Нвчем входных колод и отслеживания выходных данных в Брумбридже, выполните следующую команду:

```powershell
Convert-NWChemToBroombridge ./input.nw
```

Будет создан файл Брумбридже, запустив Нвчем в `input.nw` .
По умолчанию выходные данные Брумбридже будут иметь те же имя и путь, что и входной лоток, с `.nw` расширением, замененным на `.yaml` .
Это можно переопределить с помощью `-DestinationPath` параметра в `Convert-NWChemToBroombridge` .
Дополнительные сведения можно получить с помощью встроенных функций справки PowerShell.

```powershell
Convert-NWChemToBroombridge -?
Get-Help Convert-NWChemToBroombridge -Full
```
