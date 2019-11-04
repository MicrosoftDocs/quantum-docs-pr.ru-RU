---
title: Симулятор полного состояния пакета разработки тактов | Документация Майкрософт
description: Обзор симулятора полного состояния пакета разработки такта Майкрософт
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 12/7/2017
ms.topic: article
uid: microsoft.quantum.machines.full-state-simulator
ms.openlocfilehash: ab0e65765d27e301a59948d7c02105a523022e68
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/29/2019
ms.locfileid: "73184684"
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

## <a name="seed"></a>Инициализировать

`QuantumSimulator` использует генератор случайных чисел для имитации случайного выбора такта. В целях тестирования иногда бывает полезно иметь детерминированные результаты. Это можно сделать, предоставив начальное значение генератора случайных чисел в конструкторе `QuantumSimulator`с помощью параметра `randomNumberGeneratorSeed`:

```csharp
    using (var sim = new QuantumSimulator(randomNumberGeneratorSeed: 42))
    {
        var res = myOperationTest.Run(sim).Result;
        ///...
    }
```

## <a name="threads"></a>Потоки

`QuantumSimulator` использует [OpenMP](http://www.openmp.org/) для параллелизации линейной пере. По умолчанию OpenMP использует все доступные аппаратные потоки, что означает, что программы с небольшим количеством Кубитс часто работают медленно, так как требуется координация, dwarf фактическую работу. Это можно исправить, задав для переменной среды `OMP_NUM_THREADS` небольшое число. Как очень грубое правило, 1 поток хорошо подходит для примерно 4 Кубитс, а затем — для дополнительного потока на кубит, хотя это сильно зависит от вашего алгоритма.

