---
title: Оценщик ресурсов такта — пакет средств разработки тактов
description: Сведения о оценщике ресурсов Microsoft КДК, который оценивает ресурсы, необходимые для выполнения определенного экземпляра Q# операции на компьютере-такте.
author: anpaz
ms.author: anpaz
ms.date: 06/26/2020
ms.topic: conceptual
uid: microsoft.quantum.machines.resources-estimator
no-loc:
- Q#
- $$v
ms.openlocfilehash: c3aa94c8b34ad7247fbdeab4bf4dcb96ce746014
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847463"
---
# <a name="quantum-development-kit-qdk-resources-estimator"></a><span data-ttu-id="1cc83-103">Оценщик ресурсов пакета средств разработки такта (КДК)</span><span class="sxs-lookup"><span data-stu-id="1cc83-103">Quantum Development Kit (QDK) resources estimator</span></span>

<span data-ttu-id="1cc83-104">Как следует из названия, `ResourcesEstimator` класс оценивает ресурсы, необходимые для выполнения заданного экземпляра Q# операции на компьютере-такте.</span><span class="sxs-lookup"><span data-stu-id="1cc83-104">As the name implies, the `ResourcesEstimator` class estimates the resources required to run a given instance of a Q# operation on a quantum computer.</span></span> <span data-ttu-id="1cc83-105">Это достигается путем запуска операции такта без фактической имитации состояния тактового компьютера. по этой причине он оценивает ресурсы для Q# операций, использующих тысячи Кубитс, при условии, что классическая часть кода выполняется в разумное время.</span><span class="sxs-lookup"><span data-stu-id="1cc83-105">It accomplishes this by running the quantum operation without actually simulating the state of a quantum computer; for this reason, it estimates resources for Q# operations that use thousands of qubits, provided that the classical part of the code runs in a reasonable time.</span></span>

<span data-ttu-id="1cc83-106">Средство оценки ресурсов построено на основе [имитатора трассировки тактов](xref:microsoft.quantum.machines.qc-trace-simulator.intro), предоставляющего более широкий набор метрик и средств, помогающих в отладке Q# программ.</span><span class="sxs-lookup"><span data-stu-id="1cc83-106">The resources estimator is built on top of the [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), which provides a richer set of metrics and tools to help debug Q# programs.</span></span>

## <a name="invoking-and-running-the-resources-estimator"></a><span data-ttu-id="1cc83-107">Вызов и запуск средства оценки ресурсов</span><span class="sxs-lookup"><span data-stu-id="1cc83-107">Invoking and running the resources estimator</span></span>

<span data-ttu-id="1cc83-108">Для выполнения любой операции можно использовать Оценщик ресурсов Q# .</span><span class="sxs-lookup"><span data-stu-id="1cc83-108">You can use the resources estimator to run any Q# operation.</span></span> <span data-ttu-id="1cc83-109">Дополнительные сведения см. [в статье способы запуска Q# программы](xref:microsoft.quantum.guide.host-programs).</span><span class="sxs-lookup"><span data-stu-id="1cc83-109">For additional details, see [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs).</span></span>

### <a name="invoking-the-resources-estimator-from-c"></a><span data-ttu-id="1cc83-110">Вызов средства оценки ресурсов из C #</span><span class="sxs-lookup"><span data-stu-id="1cc83-110">Invoking the resources estimator from C#</span></span> 

<span data-ttu-id="1cc83-111">Как и в случае с другими целевыми компьютерами, вам сначала нужно создать экземпляр класса `ResourcesEstimator`, а затем передать его в качестве первого параметра метода `Run` операции.</span><span class="sxs-lookup"><span data-stu-id="1cc83-111">As with other target machines, you first create an instance of the `ResourcesEstimator` class and then pass it as the first parameter of an operation's `Run` method.</span></span>

<span data-ttu-id="1cc83-112">Учтите, что в отличие от класса `QuantumSimulator` класс `ResourcesEstimator` не реализует интерфейс <xref:System.IDisposable>, поэтому вам не нужно заключать его в оператор `using`.</span><span class="sxs-lookup"><span data-stu-id="1cc83-112">Note that, unlike the `QuantumSimulator` class, the `ResourcesEstimator` class does not implement the <xref:System.IDisposable> interface, and thus you do not need to enclose it within a `using` statement.</span></span>

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

<span data-ttu-id="1cc83-113">Как показано в примере, `ResourcesEstimator` предоставляет `ToTSV()` метод, создающий таблицу со значениями, разделенными табуляцией (TSV).</span><span class="sxs-lookup"><span data-stu-id="1cc83-113">As the example shows, `ResourcesEstimator` provides the `ToTSV()` method, which generates a table with tab-separated values (TSV).</span></span> <span data-ttu-id="1cc83-114">Можно сохранить таблицу в файл или отобразить ее в консоли для анализа.</span><span class="sxs-lookup"><span data-stu-id="1cc83-114">You can save the table to a file or display it to the console for analysis.</span></span> <span data-ttu-id="1cc83-115">Ниже приведен пример выходных данных из предыдущей программы:</span><span class="sxs-lookup"><span data-stu-id="1cc83-115">The following is a sample output from the preceding program:</span></span>

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
> <span data-ttu-id="1cc83-116">`ResourcesEstimator`Экземпляр не сбрасывает свои вычисления при каждом запуске.</span><span class="sxs-lookup"><span data-stu-id="1cc83-116">A `ResourcesEstimator` instance does not reset its calculations on every run.</span></span> <span data-ttu-id="1cc83-117">Если вы используете один и тот же экземпляр для выполнения другой операции, он объединяет новые результаты с существующими результатами.</span><span class="sxs-lookup"><span data-stu-id="1cc83-117">If you use the same instance to run another operation, it aggregates the new results with the existing results.</span></span> <span data-ttu-id="1cc83-118">Если необходимо сбросить вычисления между запусками, создайте новый экземпляр для каждого запуска.</span><span class="sxs-lookup"><span data-stu-id="1cc83-118">If you need to reset calculations between runs, create a new instance for every run.</span></span>

### <a name="invoking-the-resources-estimator-from-python"></a><span data-ttu-id="1cc83-119">Вызов средства оценки ресурсов из Python</span><span class="sxs-lookup"><span data-stu-id="1cc83-119">Invoking the resources estimator from Python</span></span>

<span data-ttu-id="1cc83-120">Используйте метод [estimate_resources ()](https://docs.microsoft.com/python/qsharp-core/qsharp.loader.qsharpcallable) из библиотеки Python с импортированной Q# операцией:</span><span class="sxs-lookup"><span data-stu-id="1cc83-120">Use the [estimate_resources()](https://docs.microsoft.com/python/qsharp-core/qsharp.loader.qsharpcallable) method from the Python library with the imported Q# operation:</span></span>

```python
qubit_result = myOperation.estimate_resources()
```

### <a name="invoking-the-resources-estimator-from-the-command-line"></a><span data-ttu-id="1cc83-121">Вызов средства оценки ресурсов из командной строки</span><span class="sxs-lookup"><span data-stu-id="1cc83-121">Invoking the resources estimator from the command line</span></span>

<span data-ttu-id="1cc83-122">При запуске Q# программы из командной строки используйте параметр **--симулятор** (или **-s** ), чтобы указать `ResourcesEstimator` целевой компьютер.</span><span class="sxs-lookup"><span data-stu-id="1cc83-122">When running a Q# program from the command line, use the **--simulator** (or **-s** shortcut) parameter to specify the `ResourcesEstimator` target machine.</span></span> <span data-ttu-id="1cc83-123">Следующая команда запускает программу с помощью средства оценки ресурсов:</span><span class="sxs-lookup"><span data-stu-id="1cc83-123">The following command runs a program using the resources estimator:</span></span> 

```dotnetcli
dotnet run -s ResourcesEstimator
```

### <a name="invoking-the-resources-estimator-from-juptyer-notebooks"></a><span data-ttu-id="1cc83-124">Вызов средства оценки ресурсов из записных книжек Жуптер</span><span class="sxs-lookup"><span data-stu-id="1cc83-124">Invoking the resources estimator from Juptyer Notebooks</span></span>

<span data-ttu-id="1cc83-125">Q#Для выполнения операции используйте команду "я волшеб" [% "Оценка](xref:microsoft.quantum.iqsharp.magic-ref.simulate) " Q# .</span><span class="sxs-lookup"><span data-stu-id="1cc83-125">Use the IQ# magic command [%estimate](xref:microsoft.quantum.iqsharp.magic-ref.simulate) to run the Q# operation.</span></span>

```
%estimate myOperation
```

## <a name="programmatically-retrieving-the-estimated-data"></a><span data-ttu-id="1cc83-126">Получение оценочных данных программными средствами</span><span class="sxs-lookup"><span data-stu-id="1cc83-126">Programmatically retrieving the estimated data</span></span>

<span data-ttu-id="1cc83-127">Помимо таблицы TSV, можно программным способом получить ресурсы, предполагаемые во время выполнения, с помощью `Data` Свойства средства оценки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1cc83-127">In addition to a TSV table, you can programmatically retrieve the resources estimated during the run via the `Data` property of the resources estimator.</span></span> <span data-ttu-id="1cc83-128">`Data`Свойство предоставляет `System.DataTable` экземпляр с двумя столбцами: `Metric` и `Sum` , индексированными по именам метрик.</span><span class="sxs-lookup"><span data-stu-id="1cc83-128">The `Data` property provides a `System.DataTable` instance with two columns: `Metric` and `Sum`, indexed by the metrics' names.</span></span>

<span data-ttu-id="1cc83-129">В следующем коде показано, как получить и напечатать общее число `QubitClifford` `T` операций, а также `CNOT` операции, используемые Q# операцией:</span><span class="sxs-lookup"><span data-stu-id="1cc83-129">The following code shows how to retrieve and print the total number of `QubitClifford`, `T` and `CNOT` operations used by a Q# operation:</span></span>

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

## <a name="metrics-reported"></a><span data-ttu-id="1cc83-130">Сообщаемые метрики</span><span class="sxs-lookup"><span data-stu-id="1cc83-130">Metrics Reported</span></span>

<span data-ttu-id="1cc83-131">Оценщик ресурсов отслеживает следующие метрики:</span><span class="sxs-lookup"><span data-stu-id="1cc83-131">The resources estimator tracks the following metrics:</span></span>

|<span data-ttu-id="1cc83-132">Метрика</span><span class="sxs-lookup"><span data-stu-id="1cc83-132">Metric</span></span>|<span data-ttu-id="1cc83-133">Описание</span><span class="sxs-lookup"><span data-stu-id="1cc83-133">Description</span></span>|
|----|----|
|<span data-ttu-id="1cc83-134">__CNOT__</span><span class="sxs-lookup"><span data-stu-id="1cc83-134">__CNOT__</span></span>    |<span data-ttu-id="1cc83-135">Число запусков `CNOT` операций (также известных как контролируемые операции Паули X).</span><span class="sxs-lookup"><span data-stu-id="1cc83-135">The run count of `CNOT` operations (also known as Controlled Pauli X operations).</span></span>|
|<span data-ttu-id="1cc83-136">__кубитклиффорд__</span><span class="sxs-lookup"><span data-stu-id="1cc83-136">__QubitClifford__</span></span> |<span data-ttu-id="1cc83-137">Число запусков отдельных операций кубит Клиффорд и Паули.</span><span class="sxs-lookup"><span data-stu-id="1cc83-137">The run count of any single qubit Clifford and Pauli operations.</span></span>|
|<span data-ttu-id="1cc83-138">__Measure__</span><span class="sxs-lookup"><span data-stu-id="1cc83-138">__Measure__</span></span>    |<span data-ttu-id="1cc83-139">Количество запусков любых измерений.</span><span class="sxs-lookup"><span data-stu-id="1cc83-139">The run count of any measurements.</span></span>  |
|<span data-ttu-id="1cc83-140">__R__</span><span class="sxs-lookup"><span data-stu-id="1cc83-140">__R__</span></span>    |<span data-ttu-id="1cc83-141">Число запусков однокубитных поворотов, исключая `T` , Клиффорд и Паули операции.</span><span class="sxs-lookup"><span data-stu-id="1cc83-141">The run count of any single-qubit rotations, excluding `T`, Clifford and Pauli operations.</span></span>  |
|<span data-ttu-id="1cc83-142">__T__</span><span class="sxs-lookup"><span data-stu-id="1cc83-142">__T__</span></span>    |<span data-ttu-id="1cc83-143">Число запусков `T` операций и их сопряжений, включая `T` операции, T_x = H. t. H и T_y = Хи. T. Хи.</span><span class="sxs-lookup"><span data-stu-id="1cc83-143">The run count of `T` operations and their conjugates, including the `T` operations, T_x = H.T.H, and T_y = Hy.T.Hy.</span></span>  |
|<span data-ttu-id="1cc83-144">__Depth__</span><span class="sxs-lookup"><span data-stu-id="1cc83-144">__Depth__</span></span>|<span data-ttu-id="1cc83-145">Глубина тактовой цепи, выполняемой Q# операцией (см. [ниже](#depth-width-and-qubitcount)).</span><span class="sxs-lookup"><span data-stu-id="1cc83-145">Depth of the quantum circuit run by the Q# operation (see [below](#depth-width-and-qubitcount)).</span></span> <span data-ttu-id="1cc83-146">По умолчанию метрика глубины подсчитывает только `T` шлюзы.</span><span class="sxs-lookup"><span data-stu-id="1cc83-146">By default, the depth metric only counts `T` gates.</span></span> <span data-ttu-id="1cc83-147">Дополнительные сведения см. в разделе [счетчик глубины](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter).</span><span class="sxs-lookup"><span data-stu-id="1cc83-147">For more details, see [Depth Counter](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter).</span></span>   |
|<span data-ttu-id="1cc83-148">__Width__</span><span class="sxs-lookup"><span data-stu-id="1cc83-148">__Width__</span></span>|<span data-ttu-id="1cc83-149">Ширина тактовой цепи, выполняемой Q# операцией (см. [ниже](#depth-width-and-qubitcount)).</span><span class="sxs-lookup"><span data-stu-id="1cc83-149">Width of the quantum circuit run by the Q# operation (see [below](#depth-width-and-qubitcount)).</span></span> <span data-ttu-id="1cc83-150">По умолчанию метрика глубины подсчитывает только `T` шлюзы.</span><span class="sxs-lookup"><span data-stu-id="1cc83-150">By default, the depth metric only counts `T` gates.</span></span> <span data-ttu-id="1cc83-151">Дополнительные сведения см. в разделе [Счетчик ширины](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter).</span><span class="sxs-lookup"><span data-stu-id="1cc83-151">For more details, see [Width Counter](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter).</span></span>   |
|<span data-ttu-id="1cc83-152">__кубиткаунт__</span><span class="sxs-lookup"><span data-stu-id="1cc83-152">__QubitCount__</span></span>    |<span data-ttu-id="1cc83-153">Нижняя граница максимального числа Кубитс, выделенного во время выполнения Q# операции.</span><span class="sxs-lookup"><span data-stu-id="1cc83-153">The lower bound for the maximum number of qubits allocated during the run of the Q# operation.</span></span> <span data-ttu-id="1cc83-154">Эта метрика может быть несовместима с __глубиной__ (см. ниже).</span><span class="sxs-lookup"><span data-stu-id="1cc83-154">This metric might not be compatible with __Depth__ (see below).</span></span>  |
|<span data-ttu-id="1cc83-155">__борроведвидс__</span><span class="sxs-lookup"><span data-stu-id="1cc83-155">__BorrowedWidth__</span></span>    |<span data-ttu-id="1cc83-156">Максимальное количество Кубитс, заимствованных внутри Q# операции.</span><span class="sxs-lookup"><span data-stu-id="1cc83-156">The maximum number of qubits borrowed inside the Q# operation.</span></span>  |


## <a name="depth-width-and-qubitcount"></a><span data-ttu-id="1cc83-157">Глубина, ширина и Кубиткаунт</span><span class="sxs-lookup"><span data-stu-id="1cc83-157">Depth, Width, and QubitCount</span></span>

<span data-ttu-id="1cc83-158">Сообщаемые оценки глубины и ширины совместимы друг с другом.</span><span class="sxs-lookup"><span data-stu-id="1cc83-158">Reported Depth and Width estimates are compatible with each other.</span></span>
<span data-ttu-id="1cc83-159">(Ранее оба числа были достижимы, но для глубины и ширины потребовались разные цепи.) В настоящее время обе метрики в этой паре могут быть достигнуты одним и тем же каналом одновременно.</span><span class="sxs-lookup"><span data-stu-id="1cc83-159">(Previously both numbers were achievable, but different circuits would be required for Depth and for Width.) Currently both metrics in this pair can be achieved by the same circuit at the same time.</span></span>

<span data-ttu-id="1cc83-160">В отчет включаются следующие метрики:</span><span class="sxs-lookup"><span data-stu-id="1cc83-160">The following metrics are reported:</span></span>

<span data-ttu-id="1cc83-161">__Глубина:__ Для корневой операции время, необходимое для выполнения, при условии, что настроено время шлюза.</span><span class="sxs-lookup"><span data-stu-id="1cc83-161">__Depth:__ For the root operation - time it takes to execute it assuming configured gate times.</span></span>
<span data-ttu-id="1cc83-162">Для операций, которые называются или поочередно выполняются во время операции, разница между последним временем доступности кубит в начале и конце операции.</span><span class="sxs-lookup"><span data-stu-id="1cc83-162">For operations called or subsequent operations - time difference between the latest qubit availability time at the beginning and the end of the operation.</span></span>

<span data-ttu-id="1cc83-163">__Ширина:__ Для корневой операции — количество Кубитс, фактически используемое для ее выполнения (и операции).</span><span class="sxs-lookup"><span data-stu-id="1cc83-163">__Width:__ For the root operation - number of qubits actually used to execute it (and operation it calls).</span></span>
<span data-ttu-id="1cc83-164">Для операций, которые называются или выполняются последующими операциями, сколько больше Кубитс использовалось в дополнение к Кубитс, уже использованному в начале операции.</span><span class="sxs-lookup"><span data-stu-id="1cc83-164">For operations called or subsequent operations - how many more qubits were used in addition to the qubits already used at the beginning of the operation.</span></span>

<span data-ttu-id="1cc83-165">Обратите внимание, что повторно используемые Кубитс не вносят вклад в этот номер.</span><span class="sxs-lookup"><span data-stu-id="1cc83-165">Please note, that reused qubits do not contribute to this number.</span></span>
<span data-ttu-id="1cc83-166">Т. е. Если несколько Кубитс были освобождены до начала операции, а все кубит, запрашиваемые этой операцией A (и операции, вызванные из), были удовлетворены повторной назначением Кубитс, то ширина операции A возвращается как 0.</span><span class="sxs-lookup"><span data-stu-id="1cc83-166">I.e. if a few qubits have been released before operation A starts, and all qubit demanded by this operation A (and operations called from A) were satisfied by reusing previously release qubits, the Width of operation A is reported as 0.</span></span> <span data-ttu-id="1cc83-167">Успешное размещение Кубитс не влияет на ширину.</span><span class="sxs-lookup"><span data-stu-id="1cc83-167">Successfully borrowed qubits do not contribute to the Width either.</span></span>

<span data-ttu-id="1cc83-168">__Кубиткаунт:__ Для корневой операции — минимальное количество Кубитс, которое было бы достаточно для выполнения этой операции (и операций, вызванных из нее).</span><span class="sxs-lookup"><span data-stu-id="1cc83-168">__QubitCount:__ For the root operation - minimum number of qubits that would be sufficient to execute this operation (and operations called from it).</span></span>
<span data-ttu-id="1cc83-169">Для операций с именем или последующими операциями — минимальное количество Кубитс, которое было бы достаточно для выполнения этой операции отдельно.</span><span class="sxs-lookup"><span data-stu-id="1cc83-169">For operations called or subsequent operations - minimum number of qubits that would be sufficient to execute this operation separately.</span></span> <span data-ttu-id="1cc83-170">Это число не включает входные Кубитс.</span><span class="sxs-lookup"><span data-stu-id="1cc83-170">This number doesn't include input qubits.</span></span> <span data-ttu-id="1cc83-171">Он включает в себя заимствованный Кубитс.</span><span class="sxs-lookup"><span data-stu-id="1cc83-171">It does include borrowed qubits.</span></span>

<span data-ttu-id="1cc83-172">Поддерживаются два режима работы.</span><span class="sxs-lookup"><span data-stu-id="1cc83-172">Two modes of operation are supported.</span></span> <span data-ttu-id="1cc83-173">Режим выбирается с помощью параметра Кктрацесимулаторконфигуратион. Оптимизедепс.</span><span class="sxs-lookup"><span data-stu-id="1cc83-173">Mode is selected by setting QCTraceSimulatorConfiguration.OptimizeDepth.</span></span>

<span data-ttu-id="1cc83-174">__Оптимизедепс = false:__ Этот режим используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1cc83-174">__OptimizeDepth=false:__ This is the default mode.</span></span> <span data-ttu-id="1cc83-175">Кубитманажер рекомендуется повторно использовать Кубитс и будет повторно использовать выпущенную Кубитс перед выделением новых.</span><span class="sxs-lookup"><span data-stu-id="1cc83-175">QubitManager is encouraged to reuse qubits and will reuse released qubits before allocating new ones.</span></span> <span data-ttu-id="1cc83-176">Для __ширины__ корневой операции принимает минимальную ширину (Нижняя граница).</span><span class="sxs-lookup"><span data-stu-id="1cc83-176">For the root operation __Width__ becomes the minimal width (lower bound).</span></span> <span data-ttu-id="1cc83-177">Информация __о совместимости может__ быть достигнута.</span><span class="sxs-lookup"><span data-stu-id="1cc83-177">Compatible __Depth__ is reported on which it can be achieved.</span></span> <span data-ttu-id="1cc83-178">__Кубиткаунт__ будет таким же, как и __Ширина__ для корневой операции без займа.</span><span class="sxs-lookup"><span data-stu-id="1cc83-178">__QubitCount__ will be the same as __Width__ for the root operation assuming no borrowing.</span></span>

<span data-ttu-id="1cc83-179">__Оптимизедепс = true:__ Кубитманажер не рекомендуется использовать для повторного использования кубит и оптимизации на основе эвристики для повторного использования кубит во время и после выполнения.</span><span class="sxs-lookup"><span data-stu-id="1cc83-179">__OptimizeDepth=true:__ QubitManager is discouraged from qubit reuse and heuristic-based optimization for qubit reuse is performed during and after execution.</span></span> <span data-ttu-id="1cc83-180">Для __глубины__ корневой операции получает минимальную глубину (нижнюю границу).</span><span class="sxs-lookup"><span data-stu-id="1cc83-180">For the root operation __Depth__ becomes the minimum depth (lower bound).</span></span> <span data-ttu-id="1cc83-181">Для этой глубины отображается совместимая __Ширина__ (оба могут быть достигнуты одновременно).</span><span class="sxs-lookup"><span data-stu-id="1cc83-181">Compatible __Width__ is reported for this depth (both can be achieved at the same time).</span></span> <span data-ttu-id="1cc83-182">Чтобы оптимизировать ширину, шлюзы, обнаруженные позже в программе, могут быть запланированы раньше шлюзов, обнаруженных ранее в программе, но Кубитс планируется повторно использовать таким образом, чтобы глубина осталась минимальной.</span><span class="sxs-lookup"><span data-stu-id="1cc83-182">To optimize width, gates encountered later in the program may be scheduled before the gates encountered earlier in the program, but qubits are scheduled to be reused in such a way that the depth remains minimal.</span></span> <span data-ttu-id="1cc83-183">Поскольку Кубитс повторно используются на основе значений времени, рекомендуется, чтобы время шлюза было настроено как целочисленное значение.</span><span class="sxs-lookup"><span data-stu-id="1cc83-183">As qubits are reused based on time values, it is recommended that the gate times are configured to be integer values.</span></span> <span data-ttu-id="1cc83-184">__Ширина__ не гарантируется оптимальной.</span><span class="sxs-lookup"><span data-stu-id="1cc83-184">__Width__ is not guaranteed to be optimal.</span></span> <span data-ttu-id="1cc83-185">Дополнительные сведения можно найти по [ширине и глубине технического документа в трассировочном](https://github.com/microsoft/qsharp-runtime/tree/main/src/Simulation/Simulators/QCTraceSimulator/Docs)документе.</span><span class="sxs-lookup"><span data-stu-id="1cc83-185">More information can be found in the whitepaper [Width and Depth in the Tracer](https://github.com/microsoft/qsharp-runtime/tree/main/src/Simulation/Simulators/QCTraceSimulator/Docs).</span></span>

## <a name="providing-the-probability-of-measurement-outcomes"></a><span data-ttu-id="1cc83-186">Предоставление вероятности результатов измерения</span><span class="sxs-lookup"><span data-stu-id="1cc83-186">Providing the probability of measurement outcomes</span></span>

<span data-ttu-id="1cc83-187"><xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability>Из пространства имен можно использовать <xref:Microsoft.Quantum.Diagnostics> для предоставления сведений о ожидаемой вероятности операции измерения.</span><span class="sxs-lookup"><span data-stu-id="1cc83-187">You can use <xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability> from the <xref:Microsoft.Quantum.Diagnostics> namespace to provide information about the expected probability of a measurement operation.</span></span> <span data-ttu-id="1cc83-188">Дополнительные сведения см. в статье [имитатор тактовой трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro) .</span><span class="sxs-lookup"><span data-stu-id="1cc83-188">For more information, see [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro)</span></span>

## <a name="see-also"></a><span data-ttu-id="1cc83-189">См. также</span><span class="sxs-lookup"><span data-stu-id="1cc83-189">See also</span></span>

- [<span data-ttu-id="1cc83-190">Симулятор трассировки тактов</span><span class="sxs-lookup"><span data-stu-id="1cc83-190">Quantum trace simulator</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.intro)
- [<span data-ttu-id="1cc83-191">Квантовый симулятор Тоффоли</span><span class="sxs-lookup"><span data-stu-id="1cc83-191">Quantum Toffoli simulator</span></span>](xref:microsoft.quantum.machines.toffoli-simulator)
- [<span data-ttu-id="1cc83-192">Квантовый симулятор полного состояния</span><span class="sxs-lookup"><span data-stu-id="1cc83-192">Quantum full state simulator</span></span>](xref:microsoft.quantum.machines.full-state-simulator) 
