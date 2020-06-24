---
title: Симулятор полного состояния
description: 'Узнайте, как запускать программы Q # на Microsoft Quantum Development Kit симуляторе полного состояния.'
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 12/7/2017
ms.topic: article
uid: microsoft.quantum.machines.full-state-simulator
ms.openlocfilehash: f73abbc4366b003e4b22366ed83ca9c897737307
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275644"
---
# <a name="quantum-development-kit-full-state-simulator"></a>Симулятор полного состояния пакета разработки тактов

Пакет разработки тактов — это полноценный имитатор такта состояния, аналогичный [ликвидному пользовательскому интерфейсу $ \рангле $](http://stationq.github.io/Liquid/) от Microsoft Research.
Этот симулятор можно использовать для выполнения и отладки алгоритмов тактовой задержки, написанных на компьютере Q #.

Этот тактовый симулятор предоставляется через `QuantumSimulator` класс. Чтобы использовать симулятор, просто создайте экземпляр этого класса и передайте его `Run` методу операции такта, которую необходимо выполнить, вместе с остальными параметрами:

```csharp
    using (var sim = new QuantumSimulator())
    {
        var res = myOperation.Run(sim).Result;
        ///...
    }
```

## <a name="idisposable"></a>IDisposable

`QuantumSimulator`Класс реализует <xref:System.IDisposable> , поэтому `Dispose` метод должен вызываться, когда экземпляр симулятора больше не используется. Лучший способ сделать это — обернуть симулятор в `using` оператор, как в примере выше.

## <a name="seed"></a>Seed

`QuantumSimulator`Использует генератор случайных чисел для имитации случайного выбора такта. В целях тестирования иногда бывает полезно иметь детерминированные результаты. Это можно сделать, предоставив начальное значение генератора случайных чисел в `QuantumSimulator` конструкторе с помощью `randomNumberGeneratorSeed` параметра:

```csharp
    using (var sim = new QuantumSimulator(randomNumberGeneratorSeed: 42))
    {
        var res = myOperationTest.Run(sim).Result;
        ///...
    }
```

## <a name="threads"></a>Потоки

`QuantumSimulator`Использует [OpenMP](http://www.openmp.org/) для параллелизации линейной пере, необходимой. По умолчанию OpenMP использует все доступные аппаратные потоки, что приводит к медленному выполнению программ с небольшим количеством кубитов, так как затраты на координацию потоков превышают фактический объем работы. Это можно исправить, присвоив переменной среды `OMP_NUM_THREADS` небольшое число. Для грубого приближения можно считать, что 1-го потока достаточно примерно для 4-х кубитов, а сверх этого добавляйте по одному потоку на кубит. Впрочем, реальные показатели сильно зависят от конкретного алгоритма.

