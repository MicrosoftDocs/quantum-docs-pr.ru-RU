---
title: Оценщик ресурсов такта — пакет средств разработки тактов
description: Сведения о оценщике ресурсов Microsoft КДК, который оценивает ресурсы, необходимые для выполнения определенного экземпляра Q# операции на компьютере-такте.
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 06/26/2020
ms.topic: article
uid: microsoft.quantum.machines.resources-estimator
no-loc:
- Q#
- $$v
ms.openlocfilehash: d5338eb740716d9d7f408703347f572688bbccb2
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868191"
---
# <a name="quantum-development-kit-qdk-resources-estimator"></a>Оценщик ресурсов пакета средств разработки такта (КДК)

Как следует из названия, `ResourcesEstimator` класс оценивает ресурсы, необходимые для выполнения заданного экземпляра Q# операции на компьютере-такте. Это достигается за счет выполнения операции такта без фактической имитации состояния тактового компьютера. по этой причине он оценивает ресурсы для Q# операций, использующих тысячи Кубитс, при условии, что классическая часть кода выполняется в разумное время.

Средство оценки ресурсов построено на основе [имитатора трассировки тактов](xref:microsoft.quantum.machines.qc-trace-simulator.intro), предоставляющего более широкий набор метрик и средств, помогающих в отладке Q# программ.

## <a name="invoking-and-running-the-resources-estimator"></a>Вызов и запуск средства оценки ресурсов

Для выполнения любой операции можно использовать Оценщик ресурсов Q# . Дополнительные сведения см. [в статье способы запуска Q# программы](xref:microsoft.quantum.guide.host-programs).

### <a name="invoking-the-resources-estimator-from-c"></a>Вызов средства оценки ресурсов из C # 

Как и в случае с другими целевыми компьютерами, вам сначала нужно создать экземпляр класса `ResourceEstimator`, а затем передать его в качестве первого параметра метода `Run` операции.

Учтите, что в отличие от класса `QuantumSimulator` класс `ResourceEstimator` не реализует интерфейс <xref:System.IDisposable>, поэтому вам не нужно заключать его в оператор `using`.

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

Как показано в примере, `ResourcesEstimator` предоставляет `ToTSV()` метод, создающий таблицу со значениями, разделенными табуляцией (TSV). Можно сохранить таблицу в файл или отобразить ее в консоли для анализа. Ниже приведен пример выходных данных из предыдущей программы:

```output
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
> `ResourcesEstimator`Экземпляр не сбрасывает свои вычисления при каждом запуске. Если вы используете один и тот же экземпляр для выполнения другой операции, он объединяет новые результаты с существующими результатами. Если необходимо сбросить вычисления между запусками, создайте новый экземпляр для каждого запуска.

### <a name="invoking-the-resources-estimator-from-python"></a>Вызов средства оценки ресурсов из Python

Используйте метод [estimate_resources ()](https://docs.microsoft.com/python/qsharp/qsharp.loader.qsharpcallable) из библиотеки Python с импортированной Q# операцией:

```python
qubit_result = myOperation.estimate_resources()
```

### <a name="invoking-the-resources-estimator-from-the-command-line"></a>Вызов средства оценки ресурсов из командной строки

При запуске Q# программы из командной строки используйте параметр **--симулятор** (или **-s** ), чтобы указать `ResourcesEstimator` целевой компьютер. Следующая команда запускает программу с помощью средства оценки ресурсов: 

```dotnetcli
dotnet run -s ResourcesEstimator
```

### <a name="invoking-the-resources-estimator-from-juptyer-notebooks"></a>Вызов средства оценки ресурсов из записных книжек Жуптер

Q#Для выполнения операции используйте команду "я волшеб" [% "Оценка](xref:microsoft.quantum.iqsharp.magic-ref.simulate) " Q# .

```
%estimate myOperation
```

## <a name="programmatically-retrieving-the-estimated-data"></a>Получение оценочных данных программными средствами

Помимо таблицы TSV, можно программным способом получить ресурсы, предполагаемые во время выполнения, с помощью `Data` Свойства средства оценки ресурсов. `Data`Свойство предоставляет `System.DataTable` экземпляр с двумя столбцами: `Metric` и `Sum` , индексированными по именам метрик.

В следующем коде показано, как получить и напечатать общее число `QubitClifford` `T` операций, а также `CNOT` операции, используемые Q# операцией:

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

Оценщик ресурсов отслеживает следующие метрики:

|Метрика|Описание|
|----|----|
|__CNOT__    |Число запусков `CNOT` операций (также известных как контролируемые операции Паули X).|
|__кубитклиффорд__ |Число запусков отдельных операций кубит Клиффорд и Паули.|
|__Measure__ (мера).    |Количество запусков любых измерений.  |
|__R__    |Число запусков однокубитных поворотов, исключая `T` , Клиффорд и Паули операции.  |
|__T__    |Число запусков `T` операций и их сопряжений, включая `T` операции, T_x = H. t. H и T_y = Хи. T. Хи.  |
|__Depth__|Нижняя граница глубины тактовой цепи, выполняемой Q# операцией. По умолчанию метрика глубины подсчитывает только `T` шлюзы. Дополнительные сведения см. в разделе [счетчик глубины](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter).   |
|__Width__    |Нижняя граница максимального числа Кубитс, выделенного во время выполнения Q# операции. При этом может оказаться невозможным одновременное достижение нижней границы __глубины__ и __ширины__ .  |
|__борроведвидс__    |Максимальное количество Кубитс, заимствованных внутри Q# операции.  |

## <a name="providing-the-probability-of-measurement-outcomes"></a>Предоставление вероятности результатов измерения

<xref:microsoft.quantum.diagnostics.assertmeasurementprobability>Из пространства имен можно использовать <xref:microsoft.quantum.diagnostics> для предоставления сведений о ожидаемой вероятности операции измерения. Дополнительные сведения см. в статье [имитатор тактовой трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro) .

## <a name="see-also"></a>См. также

- [Симулятор трассировки тактов](xref:microsoft.quantum.machines.qc-trace-simulator.intro)
- [Квантовый симулятор Тоффоли](xref:microsoft.quantum.machines.toffoli-simulator)
- [Квантовый симулятор полного состояния](xref:microsoft.quantum.machines.full-state-simulator) 