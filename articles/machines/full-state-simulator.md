---
title: Симулятор полного состояния
description: 'Узнайте, как запускать программы Q # на Microsoft Quantum Development Kit симуляторе полного состояния.'
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 12/7/2017
ms.topic: article
uid: microsoft.quantum.machines.full-state-simulator
ms.openlocfilehash: f73abbc4366b003e4b22366ed83ca9c897737307
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/28/2020
ms.locfileid: "77906123"
---
# <a name="quantum-development-kit-full-state-simulator"></a><span data-ttu-id="399b4-103">Симулятор полного состояния пакета разработки тактов</span><span class="sxs-lookup"><span data-stu-id="399b4-103">Quantum Development Kit Full State Simulator</span></span>

<span data-ttu-id="399b4-104">Пакет разработки тактов — это полноценный имитатор такта состояния, аналогичный [ликвидному пользовательскому интерфейсу $ \рангле $](http://stationq.github.io/Liquid/) от Microsoft Research.</span><span class="sxs-lookup"><span data-stu-id="399b4-104">The Quantum Development Kit provides a full state quantum simulator similar to [LIQ$Ui|\rangle$](http://stationq.github.io/Liquid/) from Microsoft Research.</span></span>
<span data-ttu-id="399b4-105">Этот симулятор можно использовать для выполнения и отладки алгоритмов тактовой задержки, написанных на компьютере Q #.</span><span class="sxs-lookup"><span data-stu-id="399b4-105">This simulator can be used to execute and debug quantum algorithms written in Q# on your computer.</span></span>

<span data-ttu-id="399b4-106">Этот тактовый симулятор предоставляется через класс `QuantumSimulator`.</span><span class="sxs-lookup"><span data-stu-id="399b4-106">This quantum simulator is exposed via the `QuantumSimulator` class.</span></span> <span data-ttu-id="399b4-107">Чтобы использовать симулятор, просто создайте экземпляр этого класса и передайте его методу `Run` операции такта, которую необходимо выполнить вместе с остальными параметрами:</span><span class="sxs-lookup"><span data-stu-id="399b4-107">To use the simulator, simply create an instance of this class and pass it to the `Run` method of the quantum operation you want to execute along with the rest of the parameters:</span></span>

```csharp
    using (var sim = new QuantumSimulator())
    {
        var res = myOperation.Run(sim).Result;
        ///...
    }
```

## <a name="idisposable"></a><span data-ttu-id="399b4-108">IDisposable</span><span class="sxs-lookup"><span data-stu-id="399b4-108">IDisposable</span></span>

<span data-ttu-id="399b4-109">Класс `QuantumSimulator` реализует <xref:System.IDisposable>, поэтому метод `Dispose` должен вызываться, когда экземпляр симулятора больше не используется.</span><span class="sxs-lookup"><span data-stu-id="399b4-109">The `QuantumSimulator` class implements <xref:System.IDisposable>, thus the `Dispose` method should be called once the instance of the simulator is not used anymore.</span></span> <span data-ttu-id="399b4-110">Лучший способ сделать это — обернуть симулятор в оператор `using`, как показано в примере выше.</span><span class="sxs-lookup"><span data-stu-id="399b4-110">The best way to do this is to wrap the simulator within a `using` statement, as in the example above.</span></span>

## <a name="seed"></a><span data-ttu-id="399b4-111">Seed</span><span class="sxs-lookup"><span data-stu-id="399b4-111">Seed</span></span>

<span data-ttu-id="399b4-112">`QuantumSimulator` использует генератор случайных чисел для имитации случайного выбора такта.</span><span class="sxs-lookup"><span data-stu-id="399b4-112">The `QuantumSimulator` uses a random number generator to simulate quantum randomness.</span></span> <span data-ttu-id="399b4-113">В целях тестирования иногда бывает полезно иметь детерминированные результаты.</span><span class="sxs-lookup"><span data-stu-id="399b4-113">For testing purposes, it is sometimes useful to have deterministic results.</span></span> <span data-ttu-id="399b4-114">Это можно сделать, предоставив начальное значение генератора случайных чисел в конструкторе `QuantumSimulator`с помощью параметра `randomNumberGeneratorSeed`:</span><span class="sxs-lookup"><span data-stu-id="399b4-114">This can be accomplished by providing a seed for the random number generator in the `QuantumSimulator`'s constructor via the `randomNumberGeneratorSeed` parameter:</span></span>

```csharp
    using (var sim = new QuantumSimulator(randomNumberGeneratorSeed: 42))
    {
        var res = myOperationTest.Run(sim).Result;
        ///...
    }
```

## <a name="threads"></a><span data-ttu-id="399b4-115">Потоки</span><span class="sxs-lookup"><span data-stu-id="399b4-115">Threads</span></span>

<span data-ttu-id="399b4-116">`QuantumSimulator` использует [OpenMP](http://www.openmp.org/) для параллелизации линейной пере.</span><span class="sxs-lookup"><span data-stu-id="399b4-116">The `QuantumSimulator` uses [OpenMP](http://www.openmp.org/) to parallelize the linear algebra required.</span></span> <span data-ttu-id="399b4-117">По умолчанию OpenMP использует все доступные аппаратные потоки, что приводит к медленному выполнению программ с небольшим количеством кубитов, так как затраты на координацию потоков превышают фактический объем работы.</span><span class="sxs-lookup"><span data-stu-id="399b4-117">By default OpenMP uses all available hardware threads, which means that programs with small numbers of qubits will often run slowly because the coordination required will dwarf the actual work.</span></span> <span data-ttu-id="399b4-118">Это можно исправить, задав для переменной среды `OMP_NUM_THREADS` небольшое число.</span><span class="sxs-lookup"><span data-stu-id="399b4-118">This can be fixed by setting the environment variable `OMP_NUM_THREADS` to a small number.</span></span> <span data-ttu-id="399b4-119">Для грубого приближения можно считать, что 1-го потока достаточно примерно для 4-х кубитов, а сверх этого добавляйте по одному потоку на кубит. Впрочем, реальные показатели сильно зависят от конкретного алгоритма.</span><span class="sxs-lookup"><span data-stu-id="399b4-119">As a very rough rule of thumb, 1 thread is good for up to about 4 qubits, and then an additional thread per qubit is good, although this is highly dependent on your algorithm.</span></span>

