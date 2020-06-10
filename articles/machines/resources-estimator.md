---
title: Оценщик ресурсов комплекта разработки тактов
description: 'Сведения о оценщике ресурсов, который оценивает ресурсы, необходимые для выполнения заданного экземпляра операции Q # на тактовый компьютер.'
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 1/22/2019
ms.topic: article
uid: microsoft.quantum.machines.resources-estimator
ms.openlocfilehash: b0c800c3946d2e4ba4457127fb9495dc9dcf2934
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630134"
---
# <a name="the-resources-estimator-target-machine"></a>Целевой компьютер оценщика ресурсов

Как следует из названия, компонент `ResourcesEstimator` оценивает ресурсы, необходимые для выполнения заданного экземпляра операции Q # на компьютере-такте.
Это достигается за счет выполнения операции такта без фактической имитации состояния тактового компьютера. по этой причине он может оценить ресурсы для операций Q #, использующих тысячи Кубитс, если классическая часть кода может выполняться в разумное время.

## <a name="usage"></a>Использование

`ResourcesEstimator`— Это просто другой тип целевого компьютера, поэтому его можно использовать для выполнения любой операции Q #. 

Как и другие целевые компьютеры, чтобы использовать его на хост-программе C#, создайте экземпляр и передайте его в качестве первого параметра `Run` метода операции:

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

Как показано в примере, объект `ResourcesEstimator` предоставляет `ToTSV()` метод для создания таблицы с разделенными табуляциями ЗНАЧЕНИЯМИ (TSV), которые можно сохранить в файл или записать в консоль для анализа. Выходные данные приведенной выше программы должны выглядеть примерно так:

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
> Параметр не `ResourcesEstimator` сбрасывает свои вычисления при каждом выполнении, если один и тот же экземпляр используется для выполнения другой операции, который будет выполнять статистическую обработку поверх существующих результатов.
> Если необходимо сбросить вычисления между запусками, создайте новый экземпляр для каждого выполнения.


## <a name="programmatically-retrieving-the-estimated-data"></a>Получение оценочных данных программными средствами

Кроме таблицы TSV, оценочные ресурсы можно получить программно с помощью `ResourcesEstimator` `Data` Свойства. `Data`предоставляет `System.DataTable` экземпляр с двумя столбцами: `Metric` и `Sum` , индексируемыми по именам метрик.

В следующем коде показано, как получить и напечатать общее количество `QubitClifford` `T` и `CNOT` шлюзов, используемых операцией Q #:

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

Ниже приведен список метрик, которые оцениваются по `ResourcesEstimator` :

* __Кнот__: число кнот (также известных как управляемый шлюз Паули X), которые выполняются.
* __Кубитклиффорд__: количество всех выполненных шлюзов кубит Клиффорд и Паули.
* __Мера__: количество всех выполненных измерений.
* __R__: количество всех выполненных поворотов кубит, исключая T, Клиффорд и Паули Gates.
* __T__: число t шлюзов и их сопряжений, включая t gate, T_x = H. t. H, и T_y = Хи. t. Хи, выполняется.
* __Depth__: глубина тактовой цепи, выполненной операцией Q #. По умолчанию в глубину учитываются только T шлюзов, дополнительные сведения см. в разделе [счетчик глубины](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter) .
* __Width__: максимальное число Кубитс, выделенных во время выполнения операции Q #.
* __Борроведвидс__: максимальное число Кубитс, заимствованных в операции Q #.


## <a name="providing-the-probability-of-measurement-outcomes"></a>Предоставление вероятности результатов измерения

<xref:microsoft.quantum.intrinsic.assertprob>из <xref:microsoft.quantum.intrinsic> пространства имен можно использовать для предоставления сведений о ожидаемой вероятности измерения для помощи в выполнении программы Q #. Проиллюстрируем это на примере.

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

Когда `ResourcesEstimator` встретится `AssertProb` , он запишет эту измерение `PauliZ` на `source` и `q` должен получить результат `Zero` с вероятностью 0,5. При `M` последующем выполнении он найдет записанные значения вероятностей результата и `M` возвратит значение `Zero` или `One` с вероятностью 0,5.


## <a name="see-also"></a>См. также раздел

`ResourcesEstimator`Компонент построен на основе [симулятора трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro)компьютерных тактов, который предоставляет более широкий набор метрик, возможность создания отчетов о метриках на полном графе вызовов и таких функций, как [средство проверки различных входных данных](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs) , для поиска ошибок в программах Q #. Дополнительные сведения см. в документации по [симулятору трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro) .

