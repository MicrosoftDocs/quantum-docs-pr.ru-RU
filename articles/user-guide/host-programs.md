---
title: 'Способы запуска программы Q #'
description: 'Обзор различных способов выполнения Q # Programs. Из командной строки, Q # Jupyter Notebooks и классических ведущих приложений на языке Python или .NET.'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 05/15/2020
ms.topic: article
uid: microsoft.quantum.guide.host-programs
ms.openlocfilehash: 132c138d7c392ed2b4bd3d0079180b68adae4cfc
ms.sourcegitcommit: a3775921db1dc5c653c97b8fa8fe2c0ddd5261ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2020
ms.locfileid: "85887736"
---
# <a name="ways-to-run-a-q-program"></a>Способы запуска программы Q #

Один из самых сильных достоинств набора разработки такта — это гибкость в различных платформах и средах разработки.
Однако это также означает, что новые пользователи Q # могут найти их в замешательстве или в подавляющем множестве вариантов, приведенных в этом [разделе.](xref:microsoft.quantum.install)
На этой странице объясняется, что происходит при запуске программы Q #, и сравниваются различные способы, которые могут сделать пользователи.

Основное отличие состоит в том, что Q # может быть запущен:
- в качестве автономного приложения, где Q # — это единственный применяемый язык, и программа вызывается напрямую. В этой категории есть два метода:
  - интерфейс командной строки
  - Записные книжки Jupyter Notebook для Q#
- с помощью дополнительной *основной программы*, написанной на Python или на языке .NET (например, C# или F #), который затем вызывает программу и может обрабатывать возвращенные результаты.

Чтобы лучше понять эти процессы и их различия, рассмотрим простую программу Q # и Сравните способы их выполнения.

## <a name="basic-q-program"></a>Базовая программа Q #

Базовая программа-тактовая частота может состоять из подготовки Кубит в равной части Штатов $ \кет {0} $ and $ \кет {1} $, ее измерения и возврата результата, который будет случайным или одним из этих двух состояний с одинаковой вероятностью.
В самом деле, этот процесс является ядром краткого руководства [генератора случайных чисел](xref:microsoft.quantum.quickstarts.qrng) .

В Q # это будет выполнено с помощью следующего кода:

```qsharp
        using (q = Qubit()) {    // allocates qubit for use (automatically in |0>)
            H(q);                // puts qubit in superposition of |0> and |1>
            return MResetZ(q);   // measures qubit, returns result (and resets it to |0> before deallocation)
        }
```

Однако этот код не может быть выполнен с помощью Q #.
Для этого ему нужно сделать тело [операции](xref:microsoft.quantum.guide.basics#q-operations-and-functions), которое затем выполняется при вызове---либо напрямую, либо другой операцией. Таким образом, можно написать операцию следующего вида:
```qsharp
    operation MeasureSuperposition() : Result {
        using (q = Qubit()) {
            H(q);
            return MResetZ(q);
        }
    }
```
Вы определили операцию, `MeasureSuperposition` которая не принимает входные данные и возвращает значение типа [result](xref:microsoft.quantum.guide.types).

Хотя примеры на этой странице состоят только из *операций*q #, все концепции, которые мы будем обсуждать, относятся к *функциям*q #, и поэтому мы вместе называемся *вызываемыми*. Их различия обсуждаются в разделе [Q # основы: операции и функции](xref:microsoft.quantum.guide.basics#q-operations-and-functions), а дополнительные сведения об их определении можно найти в разделе [операции и функции](xref:microsoft.quantum.guide.operationsfunctions).

### <a name="callable-defined-in-a-q-file"></a>Вызываемый в файле Q #

Вызываемый метод — это именно то, что вызывается и выполняется в Q #.
Однако для этого требуется еще несколько дополнений к полному `*.qs` файлу Q #.

Все типы Q # и вызываемые методы (как определяемые, так и встроенные в язык) определяются в *пространствах имен*, которые предоставляют полные имена, на которые затем можно ссылаться.

Например, [`H`](xref:microsoft.quantum.intrinsic.h) операции и находятся [`MResetZ`](xref:microsoft.quantum.measurement.mresetz) в [`Microsoft.Quantum.Instrinsic`](xref:microsoft.quantum.intrinsic) [`Microsoft.Quantum.Measurement`](xref:microsoft.quantum.measurement) пространствах имен и (в составе [стандартных библиотек Q #](xref:microsoft.quantum.qsharplibintro)).
Таким образом, они всегда могут вызываться с помощью *полных* имен `Microsoft.Quantum.Intrinsic.H(<qubit>)` , `Microsoft.Quantum.Measurement.MResetZ(<qubit>)` но всегда это приведет к очень небыстрому выполнению кода.

Вместо этого `open` инструкции позволяют ссылаться на вызываемые команды с более кратким сокращенным именем, как мы сделали в теле операции выше.
Таким образом, полный файл Q #, содержащий нашу операцию, состоит из определения нашего пространства имен, открытия пространств имен для этих вызываемых операций, а затем нашей операции:

```qsharp
namespace NamespaceName {
    open Microsoft.Quantum.Intrinsic;     // for the H operation
    open Microsoft.Quantum.Measurement;   // for MResetZ

    operation MeasureSuperposition() : Result {
        using (q = Qubit()) { 
            H(q);
            return MResetZ(q);
        }
    }
}
```

> [!NOTE]
> Пространства имен могут также быть *псевдонимами* при открытии, что может оказаться полезным, если имена вызываемых и типов в двух пространствах имен конфликтуют.
> Например, можно использовать `open Microsoft.Quantum.Instrinsic as NamespaceWithH;` метод выше, а затем вызвать `H` через `NamespaceWithH.H(<qubit>)` .

> [!NOTE]
> Единственным исключением является [`Microsoft.Quantum.Core`](xref:microsoft.quantum.core) пространство имен, которое всегда открывается автоматически.
> Таким образом, вызываемые, например, [`Length`](xref:microsoft.quantum.core.length) всегда можно использовать напрямую.

### <a name="execution-on-target-machines"></a>Выполнение на целевых компьютерах

Теперь общая модель выполнения программы Q # становится ясной.

<br/>
<img src="../media/hostprograms_general_execution_model.png" alt="Q# program execution diagram" width="400">

Во – первых, конкретный вызываемый тип имеет доступ к любым другим вызываемым и типам, определенным в том же пространстве имен.
Он также обращается к ним из любой [библиотеки Q #](xref:microsoft.quantum.libraries), но на них должны быть ссылки либо с помощью полного имени, либо с помощью `open` инструкций, описанных выше.

Затем сам вызываемый объект выполняется на *[целевом компьютере](xref:microsoft.quantum.machines)*.
Такие целевые компьютеры могут быть реальным оборудованием такта или несколькими симуляторами, доступными в составе КДК.
Для наших целей наиболее полезным целевым компьютером является экземпляр [симулятора полного состояния](xref:microsoft.quantum.machines.full-state-simulator), `QuantumSimulator` который вычисляет поведение программы так, как если бы оно выполнялось на компьютере такта без помех.

До сих пор мы описывали, что происходит при выполнении определенного вызова Q #.
Независимо от того, используется ли Q # в автономном приложении или с ведущим приложением, этот общий процесс является более или менее---поэтому гибкость КДК.
Различия между различными способами вызова пакета разработки тактов, таким образом, показывают, *как* выполняется вызов Q # вызываемого метода и каким образом возвращаются любые результаты.
В частности, различия связаны с 
1. Указывает, какую Q # вызываемый вызов должен выполняться,
2. как предоставляются потенциальные вызываемые аргументы,
3. Указание целевого компьютера, на котором выполняется, и
4. возвращаемые результаты.

Сначала мы обсудим, как это делается с помощью автономного приложения Q # из командной строки, а затем приступите к работе с ведущими программами Python и C#.
Мы зарезервировани автономное приложение Q # Jupyter записных книжек для последнего, так как в отличие от первых трех, основная функциональность не центрируется вокруг локального файла Q #.

> [!NOTE]
> Хотя мы не продемонстрируем его в этих примерах, одно соответствие между методами выполнения заключается в том, что все сообщения, выводимые из программы Q # ( [`Message`](xref:microsoft.quantum.intrinsic.message) например, или [`DumpMachine`](xref:microsoft.quantum.diagnostics.dumpmachine) ), обычно всегда будут напечатаны в соответствующей консоли.

## <a name="q-from-the-command-line"></a>Q # из командной строки
Один из самых простых способов приступить к написанию программ Q # заключается в том, чтобы не беспокоиться о отдельных файлах и на втором языке.
Использование Visual Studio Code или Visual Studio с расширением КДК позволяет легко работать с вызываемыми вызовами Q # только из одного файла Q #.

Для этого в конечном итоге будет вызвано выполнение программы путем ввода
```dotnetcli
dotnet run
```
в командной строке.
Самый простой рабочий процесс заключается в том, что расположение каталога терминала совпадает с файлом Q #, который можно легко обрабатывать наряду с редактированием файла Q # с помощью интегрированного терминала в VS Code, например.
Однако [ `dotnet run` команда](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) принимает множество параметров, и программа также может запускаться из другого расположения, просто указав `--project <PATH>` расположение файла Q #.


### <a name="add-entry-point-to-q-file"></a>Добавить точку входа в Q # файл

Большинство файлов Q # будет содержать несколько вызываемых, поэтому, естественно, нам нужно позволить компилятору знать *, какую* вызываемую команду выполнить при вводе `dotnet run` команды.
Это делается простым изменением самого файла Q #: 
    - Добавьте строку `@EntryPoint()` непосредственно перед вызываемым.

Следовательно, наш файл, приведенный выше, стал
```qsharp
namespace NamespaceName {
    open Microsoft.Quantum.Intrinsic;     // for the H operation
    open Microsoft.Quantum.Measurement;   // for MResetZ

    @EntryPoint()
    operation MeasureSuperposition() : Result {
        using (q = Qubit()) { 
            H(q);
            return MResetZ(q);
        }
    }
}
```

Теперь вызов `dotnet run` из командной строки ведет к `MeasureSuperposition` выполнению, а возвращаемое значение затем распечатывается непосредственно в терминале.
Таким образом, вы увидите `One` или `Zero` печатаете. 

Обратите внимание, что при наличии нескольких вызываемых, определенных ниже, `MeasureSuperposition` будет выполняться только запуск.
Кроме того, нет проблем, если вызываемый объект включает [Комментарии к документации](xref:microsoft.quantum.guide.filestructure#documentation-comments) до объявления, `@EntryPoint()` атрибут можно просто поместить над ними.

### <a name="callable-arguments"></a>Вызываемые аргументы

До сих пор мы рассматривали только операцию, которая не принимает входные данные.
Предположим, что мы хотели выполнить аналогичную операцию, но на нескольких Кубитс---число, предоставленное в качестве аргумента.
Такую операцию можно написать так:
```qsharp
    operation MeasureSuperpositionArray(n : Int) : Result[] {
        using (qubits = Qubit[n]) {              // allocate a register of n qubits
            ApplyToEach(H, qubits);              // apply H to each qubit in the register
            return ForEach(MResetZ, qubits);     // perform MResetZ on each qubit, returns the resulting array
        }
    }
```
, где возвращаемое значение является массивом результатов измерения.
Обратите внимание, что [`ApplyToEach`](xref:microsoft.quantum.canon.applytoeach) и [`ForEach`](xref:microsoft.quantum.arrays.foreach) находятся в [`Microsoft.Quantum.Canon`](xref:microsoft.quantum.canon) [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) пространствах имен и, для каждого из которых требуются дополнительные `open` инструкции.

Если переместить `@EntryPoint()` атрибут в перед этой новой операцией (Обратите внимание, что в файле может быть только одна строка), попытка запустить ее с помощью просто `dotnet run` приведет к появлении сообщения об ошибке, которое указывает, какие дополнительные параметры командной строки требуются и как их выразить.

В действительности в командной строке используется общий формат `dotnet run [options]` , а в нем предоставляются вызываемые аргументы.
В этом случае аргумент `n` отсутствует и показывает, что необходимо предоставить параметр `-n <n>` . Для запуска `MeasureSuperpositionArray` для `n=4` Кубитс мы используем

```dotnetcli
dotnet run -n 4
```

выдается результат, аналогичный

```output
[Zero,One,One,One]
```

Этот курс распространяется на несколько аргументов.

> [!NOTE]
> Имена аргументов, определенные в `camelCase` , немного изменяются компилятором для принятия в качестве входных данных Q #. Например, если вместо `n` используется имя, указанное `numQubits` выше, то эти входные данные будут предоставлены в командной строке с помощью `--num-qubits 4` вместо `-n 4` .

В сообщении об ошибке также содержатся другие параметры, которые можно использовать, включая изменение целевого компьютера.

### <a name="different-target-machines"></a>Разные целевые компьютеры

По мере того, как выходные данные наших операций были ожидаемыми результатами их действия над реальным Кубитс, ясно, что целевой компьютер по умолчанию из командной строки является симулятором куаунтум полного состояния `QuantumSimulator` .
Однако можно указать, что вызываемые функции должны выполняться на определенном целевом компьютере с параметром `--simulator` (или сокращенным `-s` ).

Например, мы можем запустить его на [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) :

```dotnetcli
dotnet run -n 4 -s ResourcesEstimator
```

Затем напечатанные выходные данные

```output
Metric          Sum
CNOT            0
QubitClifford   4
R               0
Measure         4
T               0
Depth           0
Width           4
BorrowedWidth   0
```

Дополнительные сведения о том, что означают эти метрики, см. в разделе [Resource оценщик: сообщаемые метрики](xref:microsoft.quantum.machines.resources-estimator#metrics-reported).

### <a name="command-line-execution-summary"></a>Сводка выполнения командной строки
<br/>
<img src="../media/hostprograms_command_line_diagram.png" alt="Q# program from command line" width="700">

### <a name="non-q-dotnet-run-options"></a>Параметры, отличные от Q # `dotnet run`

Как мы вкратце упоминали выше с помощью `--project` параметра, [ `dotnet run` команда](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) также принимает параметры, не связанные с вызываемыми аргументами Q #.
При предоставлении обоих типов параметров `dotnet` необходимо сначала указать параметры, а `--` затем разделителем, а затем Параметры Q #.
Например, указании пути вместе с числом Кубитс для операции выше, можно выполнить с помощью `dotnet run --project <PATH> -- -n <n>` .

## <a name="q-with-host-programs"></a>Q # с ведущими программами

С помощью нашего файла Q # вместо вызова операции или функции непосредственно из командной строки следует использовать *управляющую программу* на другом классическом языке. В частности, это можно сделать с помощью Python или языка .NET, такого как C# или F # (для краткости мы будем подробно описать только C#).
Для обеспечения взаимодействия требуется небольшая Настройка, но эти сведения можно найти в [руководствах по установке](xref:microsoft.quantum.install).

В двух словах ситуация теперь включает файл программы узла (например, `*.py` или `*.cs` ) в том же расположении, что и файл Q #.
Теперь она *работает, и* в процессе ее выполнения она может вызывать конкретные операции и функции q # из файла Q #.
Ядро взаимодействия основано на компиляторе Q #, делающем содержимое файла Q # доступным для хост-программы, чтобы их можно было вызывать.

Одним из основных преимуществ использования основной программы является то, что классические данные, возвращаемые программой Q #, затем можно обрабатывать на основном языке.
Это может состоять из сложной обработки данных (например, не может быть выполнена внутри Q #), а затем вызывать дальнейшие действия Q # на основе этих результатов или что-то простое, например отобразить результаты Q #.

Общая схема показана здесь, и мы рассмотрим конкретные реализации для Python и C# ниже. Пример использования программы F # Host можно найти в [примерах взаимодействия с .NET](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet).

<br/>
<img src="../media/hostprograms_host_program_diagram.png" alt="Q# program from a host program" width="700">

> [!NOTE]
> `@EntryPoint()`Атрибут, используемый для приложений командной строки Q #, нельзя использовать с ведущими программами.
> При наличии в файле Q #, вызываемом узлом, возникнет ошибка. 

Для работы с разными ведущими программами не требуется вносить изменения в `*.qs` файл Q #.
Следующие реализации основной программы работают с одним и тем же файлом Q #:

```qsharp
namespace NamespaceName {
    open Microsoft.Quantum.Intrinsic;     // contains H
    open Microsoft.Quantum.Measurement;   // MResetZ
    open Microsoft.Quantum.Canon;         // ApplyToEach
    open Microsoft.Quantum.Arrays;        // ForEach

    operation MeasureSuperposition() : Result {
        using (q = Qubit()) { 
            H(q);
            return MResetZ(q);
        }
    }

    operation MeasureSuperpositionArray(n : Int) : Result[] {
        using (qubits = Qubit[n]) {  
            ApplyToEach(H, qubits); 
            return ForEach(MResetZ, qubits);    
        }
    }
}
```

Выберите вкладку, соответствующую интересующему языку узла.

### <a name="python"></a>[Python](#tab/tabid-python)
Главное приложение Python создается следующим образом:
1. Импортируйте `qsharp` модуль, который регистрирует загрузчик модуля для взаимодействия Q #. 
    Это позволяет пространствам имен Q # отображаться как модули Python, из которых можно импортировать вызываемые вопросы Q #.
    Обратите внимание, что технически не вызываемые функции Q #, которые импортируются, а представляют собой заглушки Python, которые позволяют вызывать их.
    Они ведут себя как объекты классов Python, на которых мы используем методы для указания целевых компьютеров для отправки операции для выполнения.

2. Импортируйте эти вызываемые вопросы Q #, которые будут напрямую вызывать---в этом случае `MeasureSuperposition` и `MeasureSuperpositionArray` .
    ```python
    import qsharp
    from NamespaceName import MeasureSuperposition, MeasureSuperpositionArray
    ```
    `qsharp`После импорта модуля можно также импортировать вызываемые модули непосредственно из пространств имен библиотеки Q #.

3. Помимо любого другого кода Python теперь можно вызывать эти вызовы на конкретных целевых компьютерах и присваивать их переменным (если они возвращают значение) для дальнейшего использования.

#### <a name="specifying-target-machines"></a>Указание целевых компьютеров
Вызов операции для выполнения на определенном целевом компьютере выполняется с помощью различных методов Python для импортированного объекта.
Например, `.simulate(<args>)` использует `QuantumSimulator` для выполнения операции, тогда как `.estimate_resources(<args>)` это делается в `ResourcesEstimator` .

#### <a name="passing-inputs-to-q"></a>Передача входных данных в Q\#
Аргументы для вызываемого параметра Q # должны быть предоставлены в виде аргумента ключевого слова, где ключевое слово — это имя аргумента в определении Q #.
Это `MeasureSuperpositionArray.simulate(n=4)` допустимо, тогда как `MeasureSuperpositionArray.simulate(4)` вызовет ошибку.

Таким образом, ведущее приложение Python 

```python
import qsharp
from NamespaceName import MeasureSuperposition, MeasureSuperpositionArray

single_qubit_result = MeasureSuperposition.simulate()
single_qubit_resources = MeasureSuperposition.estimate_resources()

multi_qubit_result = MeasureSuperpositionArray.simulate(n=4)
multi_qubit_resources = MeasureSuperpositionArray.estimate_resources(n=4)

print('Single qubit:\n' + str(single_qubit_result))
print(single_qubit_resources)

print('\nMultiple qubits:\n' + str(multi_qubit_result))
print(multi_qubit_resources)
```

выводит результат следующего вида:

```python
Single qubit:
1
{'CNOT': 0, 'QubitClifford': 1, 'R': 0, 'Measure': 1, 'T': 0, 'Depth': 0, 'Width': 1, 'BorrowedWidth': 0}

Multiple qubits:
[0, 1, 1, 1]
{'CNOT': 0, 'QubitClifford': 4, 'R': 0, 'Measure': 4, 'T': 0, 'Depth': 0, 'Width': 4, 'BorrowedWidth': 0}
```

### <a name="c"></a>[C#](#tab/tabid-csharp)

Управляющая программа C# имеет несколько компонентов и тесно работает с некоторыми компонентами КДК, например симуляторами, которые сами по себе основаны на C#.

Компилятор Q # работает здесь, создавая имя пространства имен C# с эквивалентным именем из пространства имен Q # в нашем файле Q #.
В дальнейшем он создает класс C# с эквивалентным именем для каждого из определенных вызываемых из Q # или типов.

Во первых, мы делаем классы, используемые в нашей основной программе, доступными с `using` инструкциями, которые примерно аналогом на `open` инструкции в нашем файле Q #:

```csharp
using System;
using System.Threading.Tasks;
using Microsoft.Quantum.Simulation.Simulators;    // contains the target machines (e.g. QuantumSimulator, ResourcesEstimator)
using NamespaceName;                              // make the Q# namespace available
```

Далее мы объявляем пространство имен C#, несколько других битов и частей (см. полный блок кода ниже), а затем любое классическое программирование, которое нам бы хотелось (например, вычисление аргументов для вызываемых параметров Q #).
В нашем случае Последнее не требуется, но пример такого использования можно найти в [примере взаимодействия с .NET](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet).

#### <a name="target-machines"></a>Целевые компьютеры

Вернемся к Q #, нам нужно создать экземпляр целевого компьютера, на котором будут выполняться наши операции.

```csharp
            using var sim = new QuantumSimulator();
```

Использование других целевых компьютеров настолько просто, как создание экземпляра другого, хотя способ выполнения этих и обработки возвратов может немного отличаться.
Для краткости мы подносимся к [`QuantumSimulator`](xref:microsoft.quantum.machines.full-state-simulator) Now и включаем приведенный [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) [ниже](#including-the-resources-estimator).

Каждый класс C#, созданный из операций Q #, имеет `Run` метод, первый аргумент которого должен быть экземпляром целевого компьютера.
Итак, для запуска `MeasureSuperposition` в `QuantumSimulator` мы используем `MeasureSuperposition.Run(sim)` .
Возвращаемые результаты могут быть назначены переменным в C#:

```csharp
            var singleQubitResult = await MeasureSuperposition.Run(sim);
```

> [!NOTE]
> `Run`Метод выполняется асинхронно, так как это будет так для реального аппаратного оборудования, и поэтому `await` ключевое слово блокирует дальнейшее выполнение до завершения задачи.

Если вызываемый метод Q # не содержит возвращаемых значений (т. е. тип возвращаемого значения `Unit` ), то выполнение можно выполнять таким же образом, не назначая его переменной.
В этом случае вся строка будет просто состоять из 
```csharp
await <callable>.Run(<simulator>);
```

#### <a name="arguments"></a>Аргументы

Все аргументы вызываемого аргумента Q # просто передаются как дополнительные аргументы, объект после на целевой компьютер.
Следовательно, результаты `MeasureSuperpositionArray` в `n=4` Кубитс будут выбирались через 

```csharp
            var multiQubitResult = await MeasureSuperpositionArray.Run(sim, 4);
```

Таким образом, полная управляющая программа C# может выглядеть следующим образом:

```csharp
using System;
using System.Threading.Tasks;
using Microsoft.Quantum.Simulation.Simulators;
using NamespaceName;

namespace host
{
    static class Program
    {
        static async Task Main(string[] args)
        {
            using var sim = new QuantumSimulator();

            var singleQubitResult = await MeasureSuperposition.Run(sim);
            var multiQubitResult = await MeasureSuperpositionArray.Run(sim, 4);

            Console.WriteLine($"Single qubit result: {singleQubitResult}");
            Console.WriteLine($"Multiple qubit result: {multiQubitResult}");
        }
    }
}
```

В расположении файла C# приложение может быть запущено из командной строки путем ввода
```dotnetcli
dotnet run
```
и в этом случае выходные данные будут записаны в консоль аналогично 
```output
Single qubit result: One
Multiple qubit result: [One,One,Zero,Zero]
```

> [!NOTE]
> Из-за взаимодействия компилятора с пространствами имен можно было бы сделать так, чтобы вызываемые директивы Q # были доступны без `using NamespaceName;` оператора, и просто сопоставлять заголовок пространства имен C# с ним.
> Это происходит путем замены `namespace host` на `namespace NamespaceName` .

#### <a name="including-the-resources-estimator"></a>Включение средства оценки ресурсов

[`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator)Для получения выходных данных требуется немного другая реализация.

Во-первых, вместо того, чтобы создавать экземпляры в качестве переменных с помощью `using` оператора (как мы делаем с `QuantumSimulator` ), мы более просто создаем экземпляры объектов класса с помощью

```csharp
            var estimatorSingleQ = new ResourcesEstimator();
            var estimatorMultiQ = new ResourcesEstimator();
```

Обратите внимание, что вместо одного целевого симулятора, используемого несколькими операциями Q #, мы создали один экземпляр для каждого из них. Это связано с тем, что сами объекты изменяются при использовании в качестве целевых компьютеров, после чего их результаты можно извлечь с помощью метода класса `.ToTSV()` .

Чтобы выполнить операции с помощью оценщиков ресурсов, мы используем

```csharp
            await MeasureSuperposition.Run(estimatorSingleQ);
            await MeasureSuperpositionArray.Run(estimatorMultiQ, 4);
```
а затем получить результаты в виде значений с разделителями-табуляциями (TSV) с помощью `estimatorSingleQ.ToTSV()` и `estimatorMultiQ.ToTSV()` .

Таким образом, полная управляющая программа C#, `QuantumSimulator` которая использует и, и `ResourcesEstimator` может принимать форму:

```csharp
using System;
using System.Threading.Tasks;
using Microsoft.Quantum.Simulation.Simulators;
using NamespaceName;

namespace host
{
    static class Program
    {
        static async Task Main(string[] args)
        {
            using var sim = new QuantumSimulator();
            var estimatorSingleQ = new ResourcesEstimator();
            var estimatorMultiQ = new ResourcesEstimator();

            var singleQubitResult = await MeasureSuperposition.Run(sim);
            var multiQubitResult = await MeasureSuperpositionArray.Run(sim, 4);

            await MeasureSuperposition.Run(estimatorSingleQ);
            await MeasureSuperpositionArray.Run(estimatorMultiQ, 4);

            Console.WriteLine($"Single qubit result: {singleQubitResult}");
            Console.WriteLine("Single qubit resources:");
            Console.WriteLine(estimatorSingleQ.ToTSV());

            Console.WriteLine($"\nMultiple qubit result: {multiQubitResult}");
            Console.WriteLine("Multiple qubit resources:");
            Console.WriteLine(estimatorMultiQ.ToTSV());
        }
    }
}
```


что выдаст результат, аналогичный

```output
Single qubit result: One
Single qubit resources:
Metric          Sum
CNOT            0
QubitClifford   1
R               0
Measure         1
T               0
Depth           0
Width           1
BorrowedWidth   0

Multiple qubit result: [One,One,One,Zero]
Multiple qubit resources:
Metric          Sum
CNOT            0
QubitClifford   4
R               0
Measure         4
T               0
Depth           0
Width           4
BorrowedWidth   0
```

***

## <a name="q-jupyter-notebooks"></a>Записные книжки Jupyter Notebook для Q#
Q # Jupyter записные книжки используют ядро IQ #, которое позволяет определять, компилировать и выполнять вызываемые вопросы в одной записной книжке---все вместе с инструкциями, примечаниями и другим содержимым.
Это означает, что хотя можно импортировать и использовать содержимое `*.qs` файлов Q #, они не являются обязательными в модели выполнения.

Здесь мы подробно рассмотрим выполнение операций Q #, описанных выше, но более обширные общие сведения об использовании записных книжек Q # Jupyter приведены в статье [q # и Jupyter Notebooks](https://github.com/microsoft/Quantum/blob/master/samples/getting-started/intro-to-iqsharp/Notebook.ipynb).

### <a name="defining-operations"></a>Определение операций

В Jupyter Notebook Q # вы вводите Q # Code точно так же, как в пространстве имен файла Q #.

Таким образом, можно обеспечить доступ к вызываемым функциям из [стандартных библиотек Q #](xref:microsoft.quantum.qsharplibintro) с помощью `open` операторов для соответствующих пространств имен.
При выполнении ячейки с такой инструкцией определения из этих пространств имен доступны во всей рабочей области.

> [!NOTE]
> Вызываемые из [Microsoft. тактов. внутренних](xref:microsoft.quantum.intrinsic) и [Microsoft. тактов. Canon](xref:microsoft.quantum.canon) (например [`H`](xref:microsoft.quantum.intrinsic.h) , и [`ApplyToEach`](xref:microsoft.quantum.canon.applytoeach) ) автоматически доступны для операций, определенных в ячейках в записных книжках Q # Jupyter.
> Однако это не верно для кода, который помещается из внешних исходных файлов Q # (процесс, показанный в [Введение в Q # и Jupyter Notebooks](https://github.com/microsoft/Quantum/blob/master/samples/getting-started/intro-to-iqsharp/Notebook.ipynb)). 
> 

Аналогично, для определения операций требуется только написание кода Q # и выполнение ячейки.

<img src="../media/hostprograms_jupyter_op_def_crop.png" alt="Jupyter cell defining Q# operations" width="600">

Затем в выходных данных перечисляются операции, которые затем могут быть вызваны из будущих ячеек.

### <a name="target-machines"></a>Целевые компьютеры

Функциональные возможности выполнения операций на конкретных целевых компьютерах предоставляются с помощью [команд IQ # Magic](xref:microsoft.quantum.guide.quickref.iqsharp).
Например, `%simulate` `QuantumSimulator` использует, и `%estimate` используется `ResourcesEstimator` :

<img src="../media/hostprograms_jupyter_no_args_sim_est_crop.png" alt="Simulate and estimate resources Jupyter cell" width="500">

### <a name="passing-inputs-to-functions-and-operations"></a>Передача входных данных в функции и операции

В настоящее время команды Magic Execution можно использовать только с операциями, не принимающими аргументов. Поэтому для запуска `MeasureSuperpositionArray` необходимо определить операцию "оболочки", которая затем вызывает операцию с аргументами:

<img src="../media/hostprograms_jupyter_wrapper_def_sim_crop.png" alt="Wrapper function and simulate Jupyter cell" width="550">

Эту операцию можно использовать аналогично с `%estimate` и другими командами выполнения.
