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
# <a name="the-resourcesestimator-target-machine"></a><span data-ttu-id="1884a-103">Целевой компьютер Ресаурцесестиматор</span><span class="sxs-lookup"><span data-stu-id="1884a-103">The ResourcesEstimator Target Machine</span></span>

<span data-ttu-id="1884a-104">Как следует из названия, `ResourcesEstimator` оценивает ресурсы, необходимые для выполнения заданного экземпляра операции Q # на компьютере-такте.</span><span class="sxs-lookup"><span data-stu-id="1884a-104">As the name implies, the `ResourcesEstimator` estimates the resources required to run a given instance of a Q# operation on a quantum computer.</span></span>
<span data-ttu-id="1884a-105">Это достигается за счет выполнения операции такта без фактической имитации состояния тактового компьютера. по этой причине он может оценить ресурсы для операций Q #, использующих тысячи Кубитс.</span><span class="sxs-lookup"><span data-stu-id="1884a-105">It accomplishes this by executing the quantum operation without actually simulating the state of a quantum computer; for this reason, it can estimate resources for Q# operations that use thousands of qubits.</span></span>

## <a name="usage"></a><span data-ttu-id="1884a-106">Использование</span><span class="sxs-lookup"><span data-stu-id="1884a-106">Usage</span></span>

<span data-ttu-id="1884a-107">`ResourcesEstimator` — это просто другой тип целевого компьютера, поэтому его можно использовать для выполнения любой операции Q #.</span><span class="sxs-lookup"><span data-stu-id="1884a-107">The `ResourcesEstimator` is just another type of target machine, thus it can be used to run any Q# operation.</span></span> 

<span data-ttu-id="1884a-108">Как и другие целевые компьютеры, чтобы использовать его C# в основной программе, создайте экземпляр и передайте его как первый параметр метода `Run` операции:</span><span class="sxs-lookup"><span data-stu-id="1884a-108">As other target machines, to use it on a C# host program create an instance and pass it as the first parameter of the operation's `Run` method:</span></span>

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

<span data-ttu-id="1884a-109">Как показано в примере, `ResourcesEstimator` предоставляет метод `ToTSV()` для создания таблицы с разделенными табуляциями значениями (TSV), которые можно сохранить в файл или записать в консоль для анализа.</span><span class="sxs-lookup"><span data-stu-id="1884a-109">As the example shows, the `ResourcesEstimator` provides a `ToTSV()` method to generate a table with tab-seperated-values (TSV) that can be saved into a file or written to the console for analysis.</span></span> <span data-ttu-id="1884a-110">Выходные данные приведенной выше программы должны выглядеть примерно так:</span><span class="sxs-lookup"><span data-stu-id="1884a-110">The output of the above program should look something like this:</span></span>

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
> <span data-ttu-id="1884a-111">`ResourcesEstimator` не сбрасывает свои вычисления при каждом выполнении, если один и тот же экземпляр используется для выполнения другой операции, он будет выполнять статистическую обработку поверх существующих результатов.</span><span class="sxs-lookup"><span data-stu-id="1884a-111">The `ResourcesEstimator` does not reset its calculations on every run, if the same instance is used to execute another operation it will keep aggregating counts on top of existing results.</span></span>
> <span data-ttu-id="1884a-112">Если необходимо сбросить вычисления между запусками, создайте новый экземпляр для каждого выполнения.</span><span class="sxs-lookup"><span data-stu-id="1884a-112">If you need to reset calculations between runs, create a new instance for every execution.</span></span>


## <a name="programmatically-retrieving-the-estimated-data"></a><span data-ttu-id="1884a-113">Получение оценочных данных программными средствами</span><span class="sxs-lookup"><span data-stu-id="1884a-113">Programmatically Retrieving the Estimated Data</span></span>

<span data-ttu-id="1884a-114">Кроме таблицы TSV, оценочные ресурсы можно получить программно с помощью свойства `Data` `ResourcesEstimator`.</span><span class="sxs-lookup"><span data-stu-id="1884a-114">In addition to a TSV table, the resources estimated can be retrieved programmatically via the `ResourcesEstimator`'s `Data` property.</span></span> <span data-ttu-id="1884a-115">`Data` предоставляет экземпляр `System.DataTable` с двумя столбцами: `Metric` и `Sum`, индексируемые по именам метрик.</span><span class="sxs-lookup"><span data-stu-id="1884a-115">`Data` provides a `System.DataTable` instance with two columns: `Metric` and `Sum`, indexed by the metrics names.</span></span>

<span data-ttu-id="1884a-116">В следующем коде показано, как получить и напечатать общее число `QubitClifford`, `T` и `CNOT` шлюзов, используемых операцией Q #:</span><span class="sxs-lookup"><span data-stu-id="1884a-116">The following code shows how to retrieve and print the total number of `QubitClifford`, `T` and `CNOT` gates used by a Q# operation:</span></span>

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

## <a name="metrics-reported"></a><span data-ttu-id="1884a-117">Сообщаемые метрики</span><span class="sxs-lookup"><span data-stu-id="1884a-117">Metrics Reported</span></span>

<span data-ttu-id="1884a-118">Ниже приведен список метрик, предполагаемых для `ResourcesEstimator`.</span><span class="sxs-lookup"><span data-stu-id="1884a-118">The following is the list of metrics estimated by the `ResourcesEstimator`:</span></span>

* <span data-ttu-id="1884a-119">__Кнот__: число кнот (также известных как управляемый шлюз Паули X), которые выполняются.</span><span class="sxs-lookup"><span data-stu-id="1884a-119">__CNOT__: The count of CNOT (also known as the Controlled Pauli X gate) gates executed.</span></span>
* <span data-ttu-id="1884a-120">__Кубитклиффорд__: количество всех выполненных шлюзов кубит Клиффорд и Паули.</span><span class="sxs-lookup"><span data-stu-id="1884a-120">__QubitClifford__: The count of any single qubit Clifford and Pauli gates executed.</span></span>
* <span data-ttu-id="1884a-121">__Мера__: количество всех выполненных измерений.</span><span class="sxs-lookup"><span data-stu-id="1884a-121">__Measure__:  The count of any measurements executed.</span></span>
* <span data-ttu-id="1884a-122">__R__: количество всех выполненных поворотов кубит, исключая T, Клиффорд и Паули Gates.</span><span class="sxs-lookup"><span data-stu-id="1884a-122">__R__: The count of any single qubit rotations executed, excluding T, Clifford and Pauli gates.</span></span>
* <span data-ttu-id="1884a-123">__T__: число t шлюзов и их сопряжений, включая t gate, T_x = H. t. H, и T_y = Хи. t. Хи, выполняется.</span><span class="sxs-lookup"><span data-stu-id="1884a-123">__T__: The count of T gates and their conjugates, including the T gate, T_x = H.T.H, and T_y = Hy.T.Hy, executed.</span></span>
* <span data-ttu-id="1884a-124">__Depth__: глубина тактовой цепи, выполненной операцией Q #.</span><span class="sxs-lookup"><span data-stu-id="1884a-124">__Depth__: Depth of the quantum circuit executed by the Q# operation.</span></span> <span data-ttu-id="1884a-125">По умолчанию в глубину учитываются только T шлюзов, дополнительные сведения см. в разделе [счетчик глубины](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter) .</span><span class="sxs-lookup"><span data-stu-id="1884a-125">By default, only T gates are counted in the depth, see [depth counter](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter) for details.</span></span>
* <span data-ttu-id="1884a-126">__Width__: максимальное число Кубитс, выделенных во время выполнения операции Q #.</span><span class="sxs-lookup"><span data-stu-id="1884a-126">__Width__: Maximum number of qubits allocated during the execution of the Q# operation.</span></span>
* <span data-ttu-id="1884a-127">__Борроведвидс__: максимальное число Кубитс, заимствованных в операции Q #.</span><span class="sxs-lookup"><span data-stu-id="1884a-127">__BorrowedWidth__: Maximum number of qubits borrowed inside the Q# operation.</span></span>


## <a name="providing-the-probability-of-measurement-outcomes"></a><span data-ttu-id="1884a-128">Предоставление вероятности результатов измерения</span><span class="sxs-lookup"><span data-stu-id="1884a-128">Providing the Probability of Measurement Outcomes</span></span>

<span data-ttu-id="1884a-129"><xref:microsoft.quantum.intrinsic.assertprob> из пространства имен <xref:microsoft.quantum.intrinsic> можно использовать, чтобы предоставить сведения о ожидаемой вероятности измерения, чтобы обеспечить выполнение программы Q #.</span><span class="sxs-lookup"><span data-stu-id="1884a-129"><xref:microsoft.quantum.intrinsic.assertprob> from the <xref:microsoft.quantum.intrinsic> namespace can be used to provide information about the expected probability of a measurement to help drive the execution of the Q# program.</span></span> <span data-ttu-id="1884a-130">Проиллюстрируем это на примере.</span><span class="sxs-lookup"><span data-stu-id="1884a-130">The following example illustrates this:</span></span>

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

<span data-ttu-id="1884a-131">Когда `ResourcesEstimator` встречает `AssertProb` он записывает `PauliZ` измерения в `source` и `q` должен получить результат `Zero` с вероятностью 0,5.</span><span class="sxs-lookup"><span data-stu-id="1884a-131">When the `ResourcesEstimator` encounters `AssertProb` it will record that measuring `PauliZ` on `source` and `q` should be given an outcome of `Zero` with probability 0.5.</span></span> <span data-ttu-id="1884a-132">Когда она выполняется `M` позже, она найдет записанные значения вероятностей результата и `M` возвратит `Zero` или `One` с вероятностью 0,5.</span><span class="sxs-lookup"><span data-stu-id="1884a-132">When it executes `M` later, it will find the recorded values of the outcome probabilities and `M` will return `Zero` or `One` with probability 0.5.</span></span>


## <a name="see-also"></a><span data-ttu-id="1884a-133">См. также</span><span class="sxs-lookup"><span data-stu-id="1884a-133">See also</span></span>

<span data-ttu-id="1884a-134">`ResourcesEstimator` построены на основе [симулятора трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro)компьютерных компьютеров, который предоставляет более широкий набор метрик, возможность сообщать метрики на полном графе вызовов и такие функции, как [средство проверки различных входных данных](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs) , для поиска ошибок в программах Q #.</span><span class="sxs-lookup"><span data-stu-id="1884a-134">The `ResourcesEstimator` is built on top of the quantum computer [trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), which provides a richer set of metrics, the ability to report metrics on the full call-graph, and features like [distinct inputs checker](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs) to help find bugs on Q# programs.</span></span> <span data-ttu-id="1884a-135">Дополнительные сведения см. в документации по [симулятору трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro) .</span><span class="sxs-lookup"><span data-stu-id="1884a-135">Please refer to the [trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) documentation for more information.</span></span>

