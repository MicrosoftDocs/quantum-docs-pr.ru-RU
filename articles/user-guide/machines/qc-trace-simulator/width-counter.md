---
title: Счетчик ширины — пакет разработки тактов
description: 'Сведения о счетчике ширины Microsoft КДК, который использует симулятор трассировки тактов для подсчета количества Кубитс, выделенных и заимствованных операциями в Q# программе.'
author: vadym-kl
ms.author: vadym
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.width-counter
no-loc:
- 'Q#'
- '$$v'
ms.openlocfilehash: e54e92cc4a76ce9f9c5aead84f2b64320d6b4f1c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92691127"
---
# <a name="quantum-trace-simulator-width-counter"></a><span data-ttu-id="bb442-103">Симулятор тактовой трассировки: Счетчик ширины</span><span class="sxs-lookup"><span data-stu-id="bb442-103">Quantum trace simulator: width counter</span></span>

<span data-ttu-id="bb442-104">Счетчик ширины является частью [имитатора тактовой трассировки](xref:microsoft.quantum.machines.qc-trace-simulator.intro)пакета разработки тактов.</span><span class="sxs-lookup"><span data-stu-id="bb442-104">The width counter is a part of the Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="bb442-105">Его можно использовать для подсчета количества Кубитс, выделенных и заимствованных каждой операцией в Q# программе.</span><span class="sxs-lookup"><span data-stu-id="bb442-105">You can use it to count the number of qubits allocated and borrowed by each operation in a Q# program.</span></span> <span data-ttu-id="bb442-106">Некоторые примитивные операции могут выделять дополнительные Кубитс, например, умножение управляемых `X` операций или контролируемых `T` операций.</span><span class="sxs-lookup"><span data-stu-id="bb442-106">Some primitive operations can allocate extra qubits, for example, multiply controlled `X` operations or controlled `T` operations.</span></span>

## <a name="invoking-the-width-counter"></a><span data-ttu-id="bb442-107">Вызов счетчика ширины</span><span class="sxs-lookup"><span data-stu-id="bb442-107">Invoking the width counter</span></span>

<span data-ttu-id="bb442-108">Чтобы запустить симулятор трассировки тактов с счетчиком Width, необходимо создать <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> экземпляр, установить `UseWidthCounter` свойство в **значение true** , а затем создать новый <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> экземпляр с `QCTraceSimulatorConfiguration` параметром в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="bb442-108">To run the quantum trace simulator with the width counter, you must create a <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instance, set the `UseWidthCounter` property to **true** , and then create a new <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instance with the `QCTraceSimulatorConfiguration` as the parameter.</span></span> 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseWidthCounter = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-width-counter-in-a-c-host-program"></a><span data-ttu-id="bb442-109">Использование счетчика ширины в управляющей программе C#</span><span class="sxs-lookup"><span data-stu-id="bb442-109">Using the width counter in a C# host program</span></span>

<span data-ttu-id="bb442-110">В примере C#, приведенном ниже в этом разделе, вычисляется количество дополнительных Кубитс, выделенных реализацией операции умножения <xref:Microsoft.Quantum.Intrinsic.X> , на основе следующего Q# примера кода:</span><span class="sxs-lookup"><span data-stu-id="bb442-110">The C# example that follows in this section computes the number of extra qubits allocated by the implementation of a multiply controlled <xref:Microsoft.Quantum.Intrinsic.X> operation, based on the following Q# sample code:</span></span>

```qsharp
open Microsoft.Quantum.Intrinsic;
open Microsoft.Quantum.Arrays;
operation ApplyMultiControlledX( numberOfQubits : Int ) : Unit {
    using(qubits = Qubit[numberOfQubits]) {
        Controlled X (Rest(qubits), Head(qubits));
    } 
}
```

<span data-ttu-id="bb442-111">Операция умножения выполняется <xref:Microsoft.Quantum.Intrinsic.X> для всего пяти Кубитс, выделяет два [вспомогательных Кубитс](xref:microsoft.quantum.glossary#ancilla)и имеет ширину ввода **5** .</span><span class="sxs-lookup"><span data-stu-id="bb442-111">The multiply controlled <xref:Microsoft.Quantum.Intrinsic.X> operation acts on a total of five qubits, allocates two [ancillary qubits](xref:microsoft.quantum.glossary#ancilla), and has an input width of **5** .</span></span> <span data-ttu-id="bb442-112">Используйте следующую программу C# для проверки счетчиков:</span><span class="sxs-lookup"><span data-stu-id="bb442-112">Use the following C# program to verify the counts:</span></span>

```csharp 
var config = new QCTraceSimulatorConfiguration();
config.UseWidthCounter = true;
var sim = new QCTraceSimulator(config);
int totalNumberOfQubits = 5;
var res = ApplyMultiControlledX.Run(sim, totalNumberOfQubits).Result;

double allocatedQubits = 
    sim.GetMetric<Primitive.X, ApplyMultiControlledX>(
        WidthCounter.Metrics.ExtraWidth,
        functor: OperationFunctor.Controlled); 

double inputWidth =
    sim.GetMetric<Primitive.X, ApplyMultiControlledX>(
        WidthCounter.Metrics.InputWidth,
        functor: OperationFunctor.Controlled);
```

<span data-ttu-id="bb442-113">Первая часть программы выполняет `ApplyMultiControlledX` операцию.</span><span class="sxs-lookup"><span data-stu-id="bb442-113">The first part of the program runs the `ApplyMultiControlledX` operation.</span></span> <span data-ttu-id="bb442-114">Во второй части используется [`QCTraceSimulator.GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) метод для получения количества выделенных Кубитс, а также количества Кубитс, которые `Controlled X` операция получает в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="bb442-114">The second part uses the [`QCTraceSimulator.GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) method to retrieve the number of allocated qubits as well as the number of qubits that the `Controlled X` operation received as input.</span></span> 

<span data-ttu-id="bb442-115">Наконец, можно вывести всю статистику, собранную счетчиком ширины, в формате CSV, используя следующую команду:</span><span class="sxs-lookup"><span data-stu-id="bb442-115">Finally, you can output all the statistics collected by the width counter in CSV format using the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.widthCounter];
```

## <a name="see-also"></a><span data-ttu-id="bb442-116">См. также статью</span><span class="sxs-lookup"><span data-stu-id="bb442-116">See also</span></span>

- <span data-ttu-id="bb442-117">Обзор [имитатора трассировки такта](xref:microsoft.quantum.machines.qc-trace-simulator.intro) в пакете разработки тактов.</span><span class="sxs-lookup"><span data-stu-id="bb442-117">The Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
- <span data-ttu-id="bb442-118"><xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator>Справочник по API.</span><span class="sxs-lookup"><span data-stu-id="bb442-118">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API reference.</span></span>
- <span data-ttu-id="bb442-119"><xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>Справочник по API.</span><span class="sxs-lookup"><span data-stu-id="bb442-119">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API reference.</span></span>
- <span data-ttu-id="bb442-120"><xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.MetricsNames.WidthCounter>Справочник по API.</span><span class="sxs-lookup"><span data-stu-id="bb442-120">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.MetricsNames.WidthCounter> API reference.</span></span>
