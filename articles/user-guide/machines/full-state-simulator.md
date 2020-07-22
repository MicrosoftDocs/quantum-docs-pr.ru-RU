---
title: Эмулятор полного состояния — пакет разработки тактов
description: 'Узнайте, как запускать программы Q # на Microsoft Quantum Development Kit симуляторе полного состояния.'
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 06/26/2020
ms.topic: article
uid: microsoft.quantum.machines.full-state-simulator
ms.openlocfilehash: 563fdbd2a45461d112e4c46651eddd75c6fc3db2
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/21/2020
ms.locfileid: "86871184"
---
# <a name="quantum-development-kit-qdk-full-state-simulator"></a><span data-ttu-id="e8fd9-103">Симулятор полного состояния пакета средств разработки такта (КДК)</span><span class="sxs-lookup"><span data-stu-id="e8fd9-103">Quantum Development Kit (QDK) full state simulator</span></span>

<span data-ttu-id="e8fd9-104">КДК предоставляет симулятор с полным состоянием, который имитирует тактовый автомат на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="e8fd9-104">The QDK provides a full state simulator that simulates a quantum machine on your local computer.</span></span> <span data-ttu-id="e8fd9-105">Имитатор полного состояния можно использовать для запуска и отладки алгоритмов тактовой задержки, написанных в Q #, с использованием до 30 Кубитс.</span><span class="sxs-lookup"><span data-stu-id="e8fd9-105">You can use the full state simulator to run and debug quantum algorithms written in Q#, utilizing up to 30 qubits.</span></span> <span data-ttu-id="e8fd9-106">Имитатор полного состояния аналогичен имитатору такта, который используется в платформе [ликв $ UI | \рангле $](http://stationq.github.io/Liquid/) в Microsoft Research.</span><span class="sxs-lookup"><span data-stu-id="e8fd9-106">The full state simulator is similar to the quantum simulator used in the  [LIQ$Ui|\rangle$](http://stationq.github.io/Liquid/) platform from Microsoft Research.</span></span>

## <a name="invoking-and-running-the-full-state-simulator"></a><span data-ttu-id="e8fd9-107">Вызов и запуск симулятора полного состояния</span><span class="sxs-lookup"><span data-stu-id="e8fd9-107">Invoking and running the full state simulator</span></span>

<span data-ttu-id="e8fd9-108">Вы предоставляете симулятор полного состояния через `QuantumSimulator` класс.</span><span class="sxs-lookup"><span data-stu-id="e8fd9-108">You expose the full state simulator via the `QuantumSimulator` class.</span></span> <span data-ttu-id="e8fd9-109">Дополнительные сведения см. в разделе [способы запуска программы Q #](xref:microsoft.quantum.guide.host-programs).</span><span class="sxs-lookup"><span data-stu-id="e8fd9-109">For additional details, see [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs).</span></span>

### <a name="invoking-the-simulator-from-c"></a><span data-ttu-id="e8fd9-110">Вызов симулятора из C #</span><span class="sxs-lookup"><span data-stu-id="e8fd9-110">Invoking the simulator from C#</span></span>

<span data-ttu-id="e8fd9-111">Создайте экземпляр `QuantumSimulator` класса и передайте его `Run` методу операции такта, а также дополнительным параметрам.</span><span class="sxs-lookup"><span data-stu-id="e8fd9-111">Create an instance of the `QuantumSimulator` class and then pass it to the `Run` method of a quantum operation, along with any additional parameters.</span></span>
```csharp
    using (var sim = new QuantumSimulator())
    {
        var res = myOperation.Run(sim).Result;
        ///...
    }
```

<span data-ttu-id="e8fd9-112">Поскольку `QuantumSimulator` класс реализует <xref:System.IDisposable> интерфейс, необходимо вызвать `Dispose` метод, когда больше не требуется экземпляр симулятора.</span><span class="sxs-lookup"><span data-stu-id="e8fd9-112">Because the `QuantumSimulator` class implements the <xref:System.IDisposable> interface, you must call the `Dispose` method once you do not need the instance of the simulator anymore.</span></span> <span data-ttu-id="e8fd9-113">Лучший способ сделать это — заключение объявления и операций в симуляторе в операторе [using](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/using-statement) , который автоматически вызывает `Dispose` метод.</span><span class="sxs-lookup"><span data-stu-id="e8fd9-113">The best way to do this is to wrap the simulator declaration and operations within a [using](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/using-statement) statement, which automatically calls the `Dispose` method.</span></span>

### <a name="invoking-the-simulator-from-python"></a><span data-ttu-id="e8fd9-114">Вызов симулятора из Python</span><span class="sxs-lookup"><span data-stu-id="e8fd9-114">Invoking the simulator from Python</span></span>

<span data-ttu-id="e8fd9-115">Используйте метод [имитировать ()](https://docs.microsoft.com/python/qsharp/qsharp.loader.qsharpcallable) из библиотеки q # Python с импортированной операцией q #:</span><span class="sxs-lookup"><span data-stu-id="e8fd9-115">Use the [simulate()](https://docs.microsoft.com/python/qsharp/qsharp.loader.qsharpcallable) method from the Q# Python library with the imported Q# operation:</span></span>

```python
qubit_result = myOperation.simulate()
```

### <a name="invoking-the-simulator-from-the-command-line"></a><span data-ttu-id="e8fd9-116">Вызов симулятора из командной строки</span><span class="sxs-lookup"><span data-stu-id="e8fd9-116">Invoking the simulator from the command line</span></span>

<span data-ttu-id="e8fd9-117">При выполнении программы Q # из командной строки симулятор полного состояния является целевым компьютером по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e8fd9-117">When running a Q# program from the command line, the full state simulator is the default target machine.</span></span> <span data-ttu-id="e8fd9-118">При необходимости можно использовать параметр **--симулятор** (или **-s** ), чтобы указать требуемый целевой компьютер.</span><span class="sxs-lookup"><span data-stu-id="e8fd9-118">Optionally, you can use the **--simulator** (or **-s** shortcut) parameter to specify the desired target machine.</span></span> <span data-ttu-id="e8fd9-119">Обе следующие команды запускают программу с помощью симулятора полного состояния.</span><span class="sxs-lookup"><span data-stu-id="e8fd9-119">Both of the following commands run a program using the full state simulator.</span></span> 

```dotnetcli
dotnet run
dotnet run -s QuantumSimulator
```

### <a name="invoking-the-simulator-from-juptyer-notebooks"></a><span data-ttu-id="e8fd9-120">Вызов симулятора из записных книжек Жуптер</span><span class="sxs-lookup"><span data-stu-id="e8fd9-120">Invoking the simulator from Juptyer Notebooks</span></span>

<span data-ttu-id="e8fd9-121">Используйте команду IQ # Magic [% имитиру](xref:microsoft.quantum.iqsharp.magic-ref.simulate) , чтобы выполнить операцию Q #.</span><span class="sxs-lookup"><span data-stu-id="e8fd9-121">Use the IQ# magic command [%simulate](xref:microsoft.quantum.iqsharp.magic-ref.simulate) to run the Q# operation.</span></span>

```
%simulate myOperation
```
## <a name="seeding-the-simulator"></a><span data-ttu-id="e8fd9-122">Заполнение симулятора</span><span class="sxs-lookup"><span data-stu-id="e8fd9-122">Seeding the simulator</span></span>

<span data-ttu-id="e8fd9-123">По умолчанию имитатор полного состояния использует генератор случайных чисел для имитации случайности тактов.</span><span class="sxs-lookup"><span data-stu-id="e8fd9-123">By default, the full state simulator uses a random number generator to simulate quantum randomness.</span></span> <span data-ttu-id="e8fd9-124">В целях тестирования иногда бывает полезно иметь детерминированные результаты.</span><span class="sxs-lookup"><span data-stu-id="e8fd9-124">For testing purposes, it is sometimes useful to have deterministic results.</span></span> <span data-ttu-id="e8fd9-125">В программе C# это можно сделать, предоставив начальное значение генератора случайных чисел в `QuantumSimulator` конструкторе с помощью `randomNumberGeneratorSeed` параметра.</span><span class="sxs-lookup"><span data-stu-id="e8fd9-125">In a C# program, you can accomplish this by providing a seed for the random number generator in the `QuantumSimulator` constructor via the `randomNumberGeneratorSeed` parameter.</span></span>

```csharp
    using (var sim = new QuantumSimulator(randomNumberGeneratorSeed: 42))
    {
        var res = myOperationTest.Run(sim).Result;
        ///...
    }
```

## <a name="configuring-threads"></a><span data-ttu-id="e8fd9-126">Настройка потоков</span><span class="sxs-lookup"><span data-stu-id="e8fd9-126">Configuring threads</span></span>

<span data-ttu-id="e8fd9-127">Имитатор полного состояния использует [OpenMP](http://www.openmp.org/) для параллелизации линейной пере, необходимой.</span><span class="sxs-lookup"><span data-stu-id="e8fd9-127">The full state simulator uses [OpenMP](http://www.openmp.org/) to parallelize the linear algebra required.</span></span> <span data-ttu-id="e8fd9-128">По умолчанию в OpenMP используются все доступные аппаратные потоки, что означает, что программы с небольшим количеством Кубитс часто работают медленно, так как требуется координация, дварфс фактическую работу.</span><span class="sxs-lookup"><span data-stu-id="e8fd9-128">By default, OpenMP uses all available hardware threads, which means that programs with small numbers of qubits often runs slowly because the coordination that is required dwarfs the actual work.</span></span> <span data-ttu-id="e8fd9-129">Это можно исправить, присвоив переменной среды `OMP_NUM_THREADS` небольшое число.</span><span class="sxs-lookup"><span data-stu-id="e8fd9-129">You can fix this by setting the environment variable `OMP_NUM_THREADS` to a small number.</span></span> <span data-ttu-id="e8fd9-130">Как правило, настройте один поток для до четырех Кубитс, а затем один дополнительный поток на кубит.</span><span class="sxs-lookup"><span data-stu-id="e8fd9-130">As a rule of thumb, configure one thread for up to four qubits, and then one additional thread per qubit.</span></span> <span data-ttu-id="e8fd9-131">Может потребоваться изменить переменную в зависимости от алгоритма.</span><span class="sxs-lookup"><span data-stu-id="e8fd9-131">You might need to adjust the variable depending on your algorithm.</span></span>

## <a name="see-also"></a><span data-ttu-id="e8fd9-132">См. также статью</span><span class="sxs-lookup"><span data-stu-id="e8fd9-132">See also</span></span>

- [<span data-ttu-id="e8fd9-133">Оценщик ресурсов такта</span><span class="sxs-lookup"><span data-stu-id="e8fd9-133">Quantum resources estimator</span></span>](xref:microsoft.quantum.machines.resources-estimator)
- [<span data-ttu-id="e8fd9-134">Имитатор тактовой Тоффоли</span><span class="sxs-lookup"><span data-stu-id="e8fd9-134">Quantum Toffoli simulator</span></span>](xref:microsoft.quantum.machines.toffoli-simulator)
- [<span data-ttu-id="e8fd9-135">Симулятор трассировки тактов</span><span class="sxs-lookup"><span data-stu-id="e8fd9-135">Quantum trace simulator</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.intro)