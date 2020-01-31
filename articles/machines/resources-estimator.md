---
title: Оценщик ресурсов комплекта разработки тактов | Документация Майкрософт
description: Обзор средства оценки ресурсов пакета разработки такта Майкрософт
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 1/22/2019
ms.topic: article
uid: microsoft.quantum.machines.resources-estimator
ms.openlocfilehash: 960fda3dade7648f9cd24496c3a49fd11d6f807a
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820867"
---
# <a name="the-resourcesestimator-target-machine"></a>Целевой компьютер Ресаурцесестиматор

Как следует из названия, `ResourcesEstimator` оценивает ресурсы, необходимые для выполнения заданного экземпляра операции Q # на компьютере-такте.
Это достигается за счет выполнения операции такта без фактической имитации состояния тактового компьютера. по этой причине он может оценить ресурсы для операций Q #, использующих тысячи Кубитс.

## <a name="usage"></a>Использование

`ResourcesEstimator` — это просто другой тип целевого компьютера, поэтому его можно использовать для выполнения любой операции Q #. 

Как и другие целевые компьютеры, чтобы использовать его C# в основной программе, создайте экземпляр и передайте его как первый параметр метода `Run` операции:

```csharp
using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;

namespace Quantum.MyProgram
{
    class Driver
    {
        static void Main(string[] args)
        {
            ResourcesEstimator estimator = new ResourcesEstimator();
            MyQuantumProgram.Run(estimator).Wait();
            Console.WriteLine(estimator.ToTSV());
        }
    }
}
```

Как показано в примере, `ResourcesEstimator` предоставляет метод `ToTSV()` для создания таблицы с разделенными табуляциями значениями (TSV), которые можно сохранить в файл или записать в консоль для анализа. Выходные данные приведенной выше программы должны выглядеть примерно так:

```Output
Metric          Sum
CNOT            1000
QubitClifford   1000
R               0
Measure         4002
T               0
Depth           0
Width           2
BorrowedWidth   0
```

> [!NOTE]
> `ResourcesEstimator` не сбрасывает свои вычисления при каждом выполнении, если один и тот же экземпляр используется для выполнения другой операции, он будет выполнять статистическую обработку поверх существующих результатов.
> Если необходимо сбросить вычисления между запусками, создайте новый экземпляр для каждого выполнения.


## <a name="programmatically-retrieving-the-estimated-data"></a>Получение оценочных данных программными средствами

Кроме таблицы TSV, оценочные ресурсы можно получить программно с помощью свойства `Data` `ResourcesEstimator`. `Data` предоставляет экземпляр `System.DataTable` с двумя столбцами: `Metric` и `Sum`, индексируемые по именам метрик.

В следующем коде показано, как получить и напечатать общее число `QubitClifford`, `T` и `CNOT` шлюзов, используемых операцией Q #:

```csharp
using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;

namespace Quantum.MyProgram
{
    class Driver
    {
        static void Main(string[] args)
        {
            ResourcesEstimator estimator = new ResourcesEstimator();
            MyQuantumProgram.Run(estimator).Wait();

            var data = estimator.Data;
            Console.WriteLine($"QubitCliffords: {data.Rows.Find("QubitClifford")["Sum"]}");
            Console.WriteLine($"Ts: {data.Rows.Find("T")["Sum"]}");
            Console.WriteLine($"CNOTs: {data.Rows.Find("CNOT")["Sum"]}");
        }
    }
}
```

## <a name="metrics-reported"></a>Сообщаемые метрики

Ниже приведен список метрик, предполагаемых для `ResourcesEstimator`.

* __Кнот__: число кнот (также известных как управляемый шлюз Паули X), которые выполняются.
* __Кубитклиффорд__: количество всех выполненных шлюзов кубит Клиффорд и Паули.
* __Мера__: количество всех выполненных измерений.
* __R__: количество всех выполненных поворотов кубит, исключая T, Клиффорд и Паули Gates.
* __T__: число t шлюзов и их сопряжений, включая t gate, T_x = H. t. H, и T_y = Хи. t. Хи, выполняется.
* __Depth__: глубина тактовой цепи, выполненной операцией Q #. По умолчанию в глубину учитываются только T шлюзов, дополнительные сведения см. в разделе [счетчик глубины](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter) .
* __Width__: максимальное число Кубитс, выделенных во время выполнения операции Q #.
* __Борроведвидс__: максимальное число Кубитс, заимствованных в операции Q #.


## <a name="providing-the-probability-of-measurement-outcomes"></a>Предоставление вероятности результатов измерения

<xref:microsoft.quantum.intrinsic.assertprob> из пространства имен <xref:microsoft.quantum.intrinsic> можно использовать, чтобы предоставить сведения о ожидаемой вероятности измерения, чтобы обеспечить выполнение программы Q #. Проиллюстрируем это на примере.

```qsharp
operation Teleport(source : Qubit, target : Qubit) : Unit {

    using (qubit = Qubit()) {

        H(q);
        CNOT(qubit, target);

        CNOT(source, qubit);
        H(source);

        AssertProb([PauliZ], [source], Zero, 0.5, "Outcomes must be equally likely", 1e-5);
        AssertProb([PauliZ], [qubit], Zero, 0.5, "Outcomes must be equally likely", 1e-5);

        if (M(source) == One)  { Z(target); X(source); }
        if (M(qubit) == One) { X(target); X(qubit); }
    }
}
```

Когда `ResourcesEstimator` встречает `AssertProb` он записывает `PauliZ` измерения в `source` и `q` должен получить результат `Zero` с вероятностью 0,5. Когда она выполняется `M` позже, она найдет записанные значения вероятностей результата и `M` возвратит `Zero` или `One` с вероятностью 0,5.


## <a name="see-also"></a>См. также

`ResourcesEstimator` построены на основе [симулятора трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro)компьютерных компьютеров, который предоставляет более широкий набор метрик, возможность сообщать метрики на полном графе вызовов и такие функции, как [средство проверки различных входных данных](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs) , для поиска ошибок в программах Q #. Дополнительные сведения см. в документации по [симулятору трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro) .

