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
# <a name="quantum-development-kit-qdk-resources-estimator"></a><span data-ttu-id="2a1a1-103">Оценщик ресурсов пакета средств разработки такта (КДК)</span><span class="sxs-lookup"><span data-stu-id="2a1a1-103">Quantum Development Kit (QDK) resources estimator</span></span>

<span data-ttu-id="2a1a1-104">Как следует из названия, `ResourcesEstimator` класс оценивает ресурсы, необходимые для выполнения заданного экземпляра Q# операции на компьютере-такте.</span><span class="sxs-lookup"><span data-stu-id="2a1a1-104">As the name implies, the `ResourcesEstimator` class estimates the resources required to run a given instance of a Q# operation on a quantum computer.</span></span> <span data-ttu-id="2a1a1-105">Это достигается за счет выполнения операции такта без фактической имитации состояния тактового компьютера. по этой причине он оценивает ресурсы для Q# операций, использующих тысячи Кубитс, при условии, что классическая часть кода выполняется в разумное время.</span><span class="sxs-lookup"><span data-stu-id="2a1a1-105">It accomplishes this by executing the quantum operation without actually simulating the state of a quantum computer; for this reason, it estimates resources for Q# operations that use thousands of qubits, provided that the classical part of the code runs in a reasonable time.</span></span>

<span data-ttu-id="2a1a1-106">Средство оценки ресурсов построено на основе [имитатора трассировки тактов](xref:microsoft.quantum.machines.qc-trace-simulator.intro), предоставляющего более широкий набор метрик и средств, помогающих в отладке Q# программ.</span><span class="sxs-lookup"><span data-stu-id="2a1a1-106">The resources estimator is built on top of the [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), which provides a richer set of metrics and tools to help debug Q# programs.</span></span>

## <a name="invoking-and-running-the-resources-estimator"></a><span data-ttu-id="2a1a1-107">Вызов и запуск средства оценки ресурсов</span><span class="sxs-lookup"><span data-stu-id="2a1a1-107">Invoking and running the resources estimator</span></span>

<span data-ttu-id="2a1a1-108">Для выполнения любой операции можно использовать Оценщик ресурсов Q# .</span><span class="sxs-lookup"><span data-stu-id="2a1a1-108">You can use the resources estimator to run any Q# operation.</span></span> <span data-ttu-id="2a1a1-109">Дополнительные сведения см. [в статье способы запуска Q# программы](xref:microsoft.quantum.guide.host-programs).</span><span class="sxs-lookup"><span data-stu-id="2a1a1-109">For additional details, see [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs).</span></span>

### <a name="invoking-the-resources-estimator-from-c"></a><span data-ttu-id="2a1a1-110">Вызов средства оценки ресурсов из C #</span><span class="sxs-lookup"><span data-stu-id="2a1a1-110">Invoking the resources estimator from C#</span></span> 

<span data-ttu-id="2a1a1-111">Как и в случае с другими целевыми компьютерами, вам сначала нужно создать экземпляр класса `ResourceEstimator`, а затем передать его в качестве первого параметра метода `Run` операции.</span><span class="sxs-lookup"><span data-stu-id="2a1a1-111">As with other target machines, you first create an instance of the `ResourceEstimator` class and then pass it as the first parameter of an operation's `Run` method.</span></span>

<span data-ttu-id="2a1a1-112">Учтите, что в отличие от класса `QuantumSimulator` класс `ResourceEstimator` не реализует интерфейс <xref:System.IDisposable>, поэтому вам не нужно заключать его в оператор `using`.</span><span class="sxs-lookup"><span data-stu-id="2a1a1-112">Note that, unlike the `QuantumSimulator` class, the `ResourceEstimator` class does not implement the <xref:System.IDisposable> interface, and thus you do not need to enclose it within a `using` statement.</span></span>

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

<span data-ttu-id="2a1a1-113">Как показано в примере, `ResourcesEstimator` предоставляет `ToTSV()` метод, создающий таблицу со значениями, разделенными табуляцией (TSV).</span><span class="sxs-lookup"><span data-stu-id="2a1a1-113">As the example shows, `ResourcesEstimator` provides the `ToTSV()` method, which generates a table with tab-separated values (TSV).</span></span> <span data-ttu-id="2a1a1-114">Можно сохранить таблицу в файл или отобразить ее в консоли для анализа.</span><span class="sxs-lookup"><span data-stu-id="2a1a1-114">You can save the table to a file or display it to the console for analysis.</span></span> <span data-ttu-id="2a1a1-115">Ниже приведен пример выходных данных из предыдущей программы:</span><span class="sxs-lookup"><span data-stu-id="2a1a1-115">The following is a sample output from the preceding program:</span></span>

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
> <span data-ttu-id="2a1a1-116">`ResourcesEstimator`Экземпляр не сбрасывает свои вычисления при каждом запуске.</span><span class="sxs-lookup"><span data-stu-id="2a1a1-116">A `ResourcesEstimator` instance does not reset its calculations on every run.</span></span> <span data-ttu-id="2a1a1-117">Если вы используете один и тот же экземпляр для выполнения другой операции, он объединяет новые результаты с существующими результатами.</span><span class="sxs-lookup"><span data-stu-id="2a1a1-117">If you use the same instance to run another operation, it aggregates the new results with the existing results.</span></span> <span data-ttu-id="2a1a1-118">Если необходимо сбросить вычисления между запусками, создайте новый экземпляр для каждого запуска.</span><span class="sxs-lookup"><span data-stu-id="2a1a1-118">If you need to reset calculations between runs, create a new instance for every run.</span></span>

### <a name="invoking-the-resources-estimator-from-python"></a><span data-ttu-id="2a1a1-119">Вызов средства оценки ресурсов из Python</span><span class="sxs-lookup"><span data-stu-id="2a1a1-119">Invoking the resources estimator from Python</span></span>

<span data-ttu-id="2a1a1-120">Используйте метод [estimate_resources ()](https://docs.microsoft.com/python/qsharp/qsharp.loader.qsharpcallable) из библиотеки Python с импортированной Q# операцией:</span><span class="sxs-lookup"><span data-stu-id="2a1a1-120">Use the [estimate_resources()](https://docs.microsoft.com/python/qsharp/qsharp.loader.qsharpcallable) method from the Python library with the imported Q# operation:</span></span>

```python
qubit_result = myOperation.estimate_resources()
```

### <a name="invoking-the-resources-estimator-from-the-command-line"></a><span data-ttu-id="2a1a1-121">Вызов средства оценки ресурсов из командной строки</span><span class="sxs-lookup"><span data-stu-id="2a1a1-121">Invoking the resources estimator from the command line</span></span>

<span data-ttu-id="2a1a1-122">При запуске Q# программы из командной строки используйте параметр **--симулятор** (или **-s** ), чтобы указать `ResourcesEstimator` целевой компьютер.</span><span class="sxs-lookup"><span data-stu-id="2a1a1-122">When running a Q# program from the command line, use the **--simulator** (or **-s** shortcut) parameter to specify the `ResourcesEstimator` target machine.</span></span> <span data-ttu-id="2a1a1-123">Следующая команда запускает программу с помощью средства оценки ресурсов:</span><span class="sxs-lookup"><span data-stu-id="2a1a1-123">The following command runs a program using the resources estimator:</span></span> 

```dotnetcli
dotnet run -s ResourcesEstimator
```

### <a name="invoking-the-resources-estimator-from-juptyer-notebooks"></a><span data-ttu-id="2a1a1-124">Вызов средства оценки ресурсов из записных книжек Жуптер</span><span class="sxs-lookup"><span data-stu-id="2a1a1-124">Invoking the resources estimator from Juptyer Notebooks</span></span>

<span data-ttu-id="2a1a1-125">Q#Для выполнения операции используйте команду "я волшеб" [% "Оценка](xref:microsoft.quantum.iqsharp.magic-ref.simulate) " Q# .</span><span class="sxs-lookup"><span data-stu-id="2a1a1-125">Use the IQ# magic command [%estimate](xref:microsoft.quantum.iqsharp.magic-ref.simulate) to run the Q# operation.</span></span>

```
%estimate myOperation
```

## <a name="programmatically-retrieving-the-estimated-data"></a><span data-ttu-id="2a1a1-126">Получение оценочных данных программными средствами</span><span class="sxs-lookup"><span data-stu-id="2a1a1-126">Programmatically retrieving the estimated data</span></span>

<span data-ttu-id="2a1a1-127">Помимо таблицы TSV, можно программным способом получить ресурсы, предполагаемые во время выполнения, с помощью `Data` Свойства средства оценки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2a1a1-127">In addition to a TSV table, you can programmatically retrieve the resources estimated during the run via the `Data` property of the resources estimator.</span></span> <span data-ttu-id="2a1a1-128">`Data`Свойство предоставляет `System.DataTable` экземпляр с двумя столбцами: `Metric` и `Sum` , индексированными по именам метрик.</span><span class="sxs-lookup"><span data-stu-id="2a1a1-128">The `Data` property provides a `System.DataTable` instance with two columns: `Metric` and `Sum`, indexed by the metrics' names.</span></span>

<span data-ttu-id="2a1a1-129">В следующем коде показано, как получить и напечатать общее число `QubitClifford` `T` операций, а также `CNOT` операции, используемые Q# операцией:</span><span class="sxs-lookup"><span data-stu-id="2a1a1-129">The following code shows how to retrieve and print the total number of `QubitClifford`, `T` and `CNOT` operations used by a Q# operation:</span></span>

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

## <a name="metrics-reported"></a><span data-ttu-id="2a1a1-130">Сообщаемые метрики</span><span class="sxs-lookup"><span data-stu-id="2a1a1-130">Metrics Reported</span></span>

<span data-ttu-id="2a1a1-131">Оценщик ресурсов отслеживает следующие метрики:</span><span class="sxs-lookup"><span data-stu-id="2a1a1-131">The resources estimator tracks the following metrics:</span></span>

|<span data-ttu-id="2a1a1-132">Метрика</span><span class="sxs-lookup"><span data-stu-id="2a1a1-132">Metric</span></span>|<span data-ttu-id="2a1a1-133">Описание</span><span class="sxs-lookup"><span data-stu-id="2a1a1-133">Description</span></span>|
|----|----|
|<span data-ttu-id="2a1a1-134">__CNOT__</span><span class="sxs-lookup"><span data-stu-id="2a1a1-134">__CNOT__</span></span>    |<span data-ttu-id="2a1a1-135">Число запусков `CNOT` операций (также известных как контролируемые операции Паули X).</span><span class="sxs-lookup"><span data-stu-id="2a1a1-135">The run count of `CNOT` operations (also known as Controlled Pauli X operations).</span></span>|
|<span data-ttu-id="2a1a1-136">__кубитклиффорд__</span><span class="sxs-lookup"><span data-stu-id="2a1a1-136">__QubitClifford__</span></span> |<span data-ttu-id="2a1a1-137">Число запусков отдельных операций кубит Клиффорд и Паули.</span><span class="sxs-lookup"><span data-stu-id="2a1a1-137">The run count of any single qubit Clifford and Pauli operations.</span></span>|
|<span data-ttu-id="2a1a1-138">__Measure__ (мера).</span><span class="sxs-lookup"><span data-stu-id="2a1a1-138">__Measure__</span></span>    |<span data-ttu-id="2a1a1-139">Количество запусков любых измерений.</span><span class="sxs-lookup"><span data-stu-id="2a1a1-139">The run count of any measurements.</span></span>  |
|<span data-ttu-id="2a1a1-140">__R__</span><span class="sxs-lookup"><span data-stu-id="2a1a1-140">__R__</span></span>    |<span data-ttu-id="2a1a1-141">Число запусков однокубитных поворотов, исключая `T` , Клиффорд и Паули операции.</span><span class="sxs-lookup"><span data-stu-id="2a1a1-141">The run count of any single-qubit rotations, excluding `T`, Clifford and Pauli operations.</span></span>  |
|<span data-ttu-id="2a1a1-142">__T__</span><span class="sxs-lookup"><span data-stu-id="2a1a1-142">__T__</span></span>    |<span data-ttu-id="2a1a1-143">Число запусков `T` операций и их сопряжений, включая `T` операции, T_x = H. t. H и T_y = Хи. T. Хи.</span><span class="sxs-lookup"><span data-stu-id="2a1a1-143">The run count of `T` operations and their conjugates, including the `T` operations, T_x = H.T.H, and T_y = Hy.T.Hy.</span></span>  |
|<span data-ttu-id="2a1a1-144">__Depth__</span><span class="sxs-lookup"><span data-stu-id="2a1a1-144">__Depth__</span></span>|<span data-ttu-id="2a1a1-145">Нижняя граница глубины тактовой цепи, выполняемой Q# операцией.</span><span class="sxs-lookup"><span data-stu-id="2a1a1-145">The lower bound for the depth of the quantum circuit run by the Q# operation.</span></span> <span data-ttu-id="2a1a1-146">По умолчанию метрика глубины подсчитывает только `T` шлюзы.</span><span class="sxs-lookup"><span data-stu-id="2a1a1-146">By default, the depth metric only counts `T` gates.</span></span> <span data-ttu-id="2a1a1-147">Дополнительные сведения см. в разделе [счетчик глубины](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter).</span><span class="sxs-lookup"><span data-stu-id="2a1a1-147">For more details, see [Depth Counter](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter).</span></span>   |
|<span data-ttu-id="2a1a1-148">__Width__</span><span class="sxs-lookup"><span data-stu-id="2a1a1-148">__Width__</span></span>    |<span data-ttu-id="2a1a1-149">Нижняя граница максимального числа Кубитс, выделенного во время выполнения Q# операции.</span><span class="sxs-lookup"><span data-stu-id="2a1a1-149">The lower bound for the maximum number of qubits allocated during the run of the Q# operation.</span></span> <span data-ttu-id="2a1a1-150">При этом может оказаться невозможным одновременное достижение нижней границы __глубины__ и __ширины__ .</span><span class="sxs-lookup"><span data-stu-id="2a1a1-150">It might not be possible to achieve both __Depth__ and __Width__ lower bounds simultaneously.</span></span>  |
|<span data-ttu-id="2a1a1-151">__борроведвидс__</span><span class="sxs-lookup"><span data-stu-id="2a1a1-151">__BorrowedWidth__</span></span>    |<span data-ttu-id="2a1a1-152">Максимальное количество Кубитс, заимствованных внутри Q# операции.</span><span class="sxs-lookup"><span data-stu-id="2a1a1-152">The maximum number of qubits borrowed inside the Q# operation.</span></span>  |

## <a name="providing-the-probability-of-measurement-outcomes"></a><span data-ttu-id="2a1a1-153">Предоставление вероятности результатов измерения</span><span class="sxs-lookup"><span data-stu-id="2a1a1-153">Providing the probability of measurement outcomes</span></span>

<span data-ttu-id="2a1a1-154"><xref:microsoft.quantum.diagnostics.assertmeasurementprobability>Из пространства имен можно использовать <xref:microsoft.quantum.diagnostics> для предоставления сведений о ожидаемой вероятности операции измерения.</span><span class="sxs-lookup"><span data-stu-id="2a1a1-154">You can use <xref:microsoft.quantum.diagnostics.assertmeasurementprobability> from the <xref:microsoft.quantum.diagnostics> namespace to provide information about the expected probability of a measurement operation.</span></span> <span data-ttu-id="2a1a1-155">Дополнительные сведения см. в статье [имитатор тактовой трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro) .</span><span class="sxs-lookup"><span data-stu-id="2a1a1-155">For more information, see [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro)</span></span>

## <a name="see-also"></a><span data-ttu-id="2a1a1-156">См. также</span><span class="sxs-lookup"><span data-stu-id="2a1a1-156">See also</span></span>

- [<span data-ttu-id="2a1a1-157">Симулятор трассировки тактов</span><span class="sxs-lookup"><span data-stu-id="2a1a1-157">Quantum trace simulator</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.intro)
- [<span data-ttu-id="2a1a1-158">Квантовый симулятор Тоффоли</span><span class="sxs-lookup"><span data-stu-id="2a1a1-158">Quantum Toffoli simulator</span></span>](xref:microsoft.quantum.machines.toffoli-simulator)
- [<span data-ttu-id="2a1a1-159">Квантовый симулятор полного состояния</span><span class="sxs-lookup"><span data-stu-id="2a1a1-159">Quantum full state simulator</span></span>](xref:microsoft.quantum.machines.full-state-simulator) 