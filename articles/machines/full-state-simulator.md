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
# <a name="quantum-development-kit-full-state-simulator"></a>Симулятор полного состояния пакета разработки тактов

Пакет разработки тактов — это полноценный имитатор такта состояния, аналогичный [ликвидному пользовательскому интерфейсу $ \рангле $](http://stationq.github.io/Liquid/) от Microsoft Research.
Этот симулятор можно использовать для выполнения и отладки алгоритмов тактовой задержки, написанных на компьютере Q #.

Этот тактовый симулятор предоставляется через класс `QuantumSimulator`. Чтобы использовать симулятор, просто создайте экземпляр этого класса и передайте его методу `Run` операции такта, которую необходимо выполнить вместе с остальными параметрами:

```csharp
    using (var sim = new QuantumSimulator())
    {
        var res = myOperation.Run(sim).Result;
        ///...
    }
```

## <a name="idisposable"></a>IDisposable

Класс `QuantumSimulator` реализует <xref:System.IDisposable>, поэтому метод `Dispose` должен вызываться, когда экземпляр симулятора больше не используется. Лучший способ сделать это — обернуть симулятор в оператор `using`, как показано в примере выше.

## <a name="seed"></a>Seed

`QuantumSimulator` использует генератор случайных чисел для имитации случайного выбора такта. В целях тестирования иногда бывает полезно иметь детерминированные результаты. Это можно сделать, предоставив начальное значение генератора случайных чисел в конструкторе `QuantumSimulator`с помощью параметра `randomNumberGeneratorSeed`:

```csharp
    using (var sim = new QuantumSimulator(randomNumberGeneratorSeed: 42))
    {
        var res = myOperationTest.Run(sim).Result;
        ///...
    }
```

## <a name="threads"></a>Потоки

`QuantumSimulator` использует [OpenMP](http://www.openmp.org/) для параллелизации линейной пере. По умолчанию OpenMP использует все доступные аппаратные потоки, что приводит к медленному выполнению программ с небольшим количеством кубитов, так как затраты на координацию потоков превышают фактический объем работы. Это можно исправить, задав для переменной среды `OMP_NUM_THREADS` небольшое число. Для грубого приближения можно считать, что 1-го потока достаточно примерно для 4-х кубитов, а сверх этого добавляйте по одному потоку на кубит. Впрочем, реальные показатели сильно зависят от конкретного алгоритма.

