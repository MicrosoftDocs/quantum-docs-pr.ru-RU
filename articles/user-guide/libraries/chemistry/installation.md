---
title: Q#Установка библиотеки Microsoft химия
description: Узнайте, как установить библиотеку Microsoft тактов химия и использовать ее с Нвчем вычислительной химия платформой.
author: guanghaolow
ms.author: gulow
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.chemistry.concepts.installation
no-loc:
- Q#
- $$v
ms.openlocfilehash: f1a7d1d041dab73980d8debc179d6c79acac6d33
ms.sourcegitcommit: 8256ff463eb9319f1933820a36c0838cf1e024e8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/17/2020
ms.locfileid: "90759805"
---
# <a name="chemistry-library-installation"></a>Установка библиотеки химия

В [примере **молекулархидрожен** ](https://github.com/microsoft/Quantum/tree/main/samples/chemistry/MolecularHydrogen) используются входные данные молекулярное, настроенные вручную.
Хотя это и очень удобно для небольших примеров, тактовая химия в масштабе требует Хамилтонианс с миллионами или миллиардами терминов.
Такие Хамилтонианс, созданные масштабируемыми вычислительными пакетами химия, слишком велики для импорта вручную.

Библиотека тактовой химия для пакета разработки такта разработана для работы с вычислительными пакетами химия, которая, в первую очередь, является [**нвчем**](http://www.nwchem-sw.org/) вычислительной химияной платформой, разработанной лабораторией молекулярное SCIENCES (емсл) в северо-западной национальной лаборатории.
В частности, пакет [ **Microsoft. тактов. Химия** ](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) предоставляет средства для загрузки экземпляров проблем моделирования тактов химия, представленных в [схеме брумбридже](xref:microsoft.quantum.libraries.chemistry.schema.broombridge), которые также поддерживаются для экспорта в последних версиях нвчем.

Библиотека химия пакета разработки тактов также предоставляет средство командной строки `qdk-chem` для преобразования между устаревшими форматами и [брумбридже](xref:microsoft.quantum.libraries.chemistry.schema.broombridge).

В этом разделе подробно описано, как использовать пакет средств разработки тактов с Нвчем и Брумбридже, а также с форматами прежних версий и `qdk-chem` .

## <a name="using-the-quantum-development-kit-with-nwchem"></a>Использование пакета средств разработки тактов с Нвчем

Чтобы начать работу с помощью Нвчем вместе с пакетом средств разработки тактов, используйте один из следующих методов.

- Начните работу с существующих файлов Брумбридже, предоставленных в примерах на сайте [интегралдата/YAML](https://github.com/microsoft/Quantum/tree/main/samples/chemistry/IntegralData/YAML).
- Используйте [Построитель стрелок емсл для Microsoft Quantum Development Kit](https://arrows.emsl.pnnl.gov/api/qsharp_chem) , который является веб-интерфейсом для нвчем, для создания новых входных файлов брумбридже с форматом молекулярное.  
- Используйте [образ DOCKER](https://hub.docker.com/r/nwchemorg/nwchem-qc/) , предоставленный пннл для запуска нвчем, или
- [Скомпилируйте нвчем](http://www.nwchem-sw.org/index.php/Compiling_NWChem) для своей платформы.

Дополнительные сведения о работе с Нвчем для химических моделей для анализа с помощью библиотеки химия пакета персонала [Kit см. в этой](xref:microsoft.quantum.chemistry.examples.endtoend) статье.

### <a name="getting-started-using-broombridge-files-provided-with-the-samples"></a>Приступая к работе с файлами Брумбридже, поставляемыми с образцами

Папка [интегралдата/YAML](https://github.com/microsoft/Quantum/tree/main/samples/chemistry/IntegralData/YAML) в репозитории примеров пакета разработки тактов содержит файлы данных с брумбридже форматом.  

В качестве простого примера используйте пример библиотеки химия, [жетгатекаунт](https://github.com/microsoft/Quantum/tree/main/samples/chemistry/GetGateCount) , чтобы загрузить хамилтониан из одного из брумбридже файлов и выполнить прогнозное моделирование алгоригсмс:

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

## <a name="using-the-quantum-development-kit-with-qdk-chem"></a>Использование пакета средств разработки такта с `qdk-chem`

Для установки `qdk-chem` можно использовать пакет SDK для .NET Core из командной строки:

```dotnetcli
dotnet tool install --global Microsoft.Quantum.Chemistry.Tools
```

После установки `qdk-chem` можно использовать `--help` параметр, чтобы получить дополнительные сведения о функциях, предоставляемых `qdk-chem` средством.

Для преобразования в Брумбридже и обратно можно использовать `qdk-chem convert` команду:

```
qdk-chem convert --from fcidump --to broombridge data.fcidump --out data.yml
```

`qdk-chem convert`Команда также может принимать свои данные из стандартных входных данных и может записывать их в стандартный вывод. Это особенно удобно в сценариях и для интеграции со средствами, которые экспортируют в прежние форматы.
Пример (bash):

```bash
cat data.fcidump | qdk-convert --from fcidump --to broombridge - > data.yml
```
