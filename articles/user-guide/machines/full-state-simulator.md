---
title: Эмулятор полного состояния — пакет разработки тактов
description: Узнайте, как запускать Q# программы на Microsoft Quantum Development Kit симуляторе полного состояния.
author: anpaz-msft
ms.author: anpaz
ms.date: 06/26/2020
ms.topic: article
uid: microsoft.quantum.machines.full-state-simulator
no-loc:
- Q#
- $$v
ms.openlocfilehash: 632af681c5818ab7246c0f5849a8b8e716b570cb
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/21/2020
ms.locfileid: "90833385"
---
# <a name="quantum-development-kit-qdk-full-state-simulator"></a>Симулятор полного состояния пакета средств разработки такта (КДК)

КДК предоставляет симулятор с полным состоянием, который имитирует тактовый автомат на локальном компьютере. Имитатор полного состояния можно использовать для запуска и отладки алгоритмов такта, написанных в Q# , с использованием до 30 Кубитс. Имитатор полного состояния аналогичен имитатору такта, который используется в платформе  [ликв $ UI | \рангле $](http://stationq.github.io/Liquid/) в Microsoft Research.

## <a name="invoking-and-running-the-full-state-simulator"></a>Вызов и запуск симулятора полного состояния

Вы предоставляете симулятор полного состояния через `QuantumSimulator` класс. Дополнительные сведения см. [в статье способы запуска Q# программы](xref:microsoft.quantum.guide.host-programs).

### <a name="invoking-the-simulator-from-c"></a>Вызов симулятора из C #

Создайте экземпляр `QuantumSimulator` класса и передайте его `Run` методу операции такта, а также дополнительным параметрам.
```csharp
    using (var sim = new QuantumSimulator())
    {
        var res = myOperation.Run(sim).Result;
        ///...
    }
```

Поскольку `QuantumSimulator` класс реализует <xref:System.IDisposable> интерфейс, необходимо вызвать `Dispose` метод, когда больше не требуется экземпляр симулятора. Лучший способ сделать это — заключение объявления и операций в симуляторе в операторе [using](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/using-statement) , который автоматически вызывает `Dispose` метод.

### <a name="invoking-the-simulator-from-python"></a>Вызов симулятора из Python

Используйте метод [имитировать ()](https://docs.microsoft.com/python/qsharp-core/qsharp.loader.qsharpcallable) из Q# библиотеки Python с импортированной Q# операцией:

```python
qubit_result = myOperation.simulate()
```

### <a name="invoking-the-simulator-from-the-command-line"></a>Вызов симулятора из командной строки

При запуске Q# программы из командной строки симулятор полного состояния является целевым компьютером по умолчанию. При необходимости можно использовать параметр **--симулятор** (или **-s** ), чтобы указать требуемый целевой компьютер. Обе следующие команды запускают программу с помощью симулятора полного состояния. 

```dotnetcli
dotnet run
dotnet run -s QuantumSimulator
```

### <a name="invoking-the-simulator-from-juptyer-notebooks"></a>Вызов симулятора из записных книжек Жуптер

Используйте команду "I Q# Magic" [% имитируйте](xref:microsoft.quantum.iqsharp.magic-ref.simulate) , чтобы выполнить Q# операцию.

```
%simulate myOperation
```
## <a name="seeding-the-simulator"></a>Заполнение симулятора

По умолчанию имитатор полного состояния использует генератор случайных чисел для имитации случайности тактов. В целях тестирования иногда бывает полезно иметь детерминированные результаты. В программе C# это можно сделать, предоставив начальное значение генератора случайных чисел в `QuantumSimulator` конструкторе с помощью `randomNumberGeneratorSeed` параметра.

```csharp
    using (var sim = new QuantumSimulator(randomNumberGeneratorSeed: 42))
    {
        var res = myOperationTest.Run(sim).Result;
        ///...
    }
```

## <a name="configuring-threads"></a>Настройка потоков

Имитатор полного состояния использует [OpenMP](http://www.openmp.org/) для параллелизации линейной пере, необходимой. По умолчанию в OpenMP используются все доступные аппаратные потоки, что означает, что программы с небольшим количеством Кубитс часто работают медленно, так как требуется координация, дварфс фактическую работу. Это можно исправить, присвоив переменной среды `OMP_NUM_THREADS` небольшое число. Как правило, настройте один поток для до четырех Кубитс, а затем один дополнительный поток на кубит. Может потребоваться изменить переменную в зависимости от алгоритма.

## <a name="see-also"></a>См. также раздел

- [Квантовый оценщик ресурсов](xref:microsoft.quantum.machines.resources-estimator)
- [Квантовый симулятор Тоффоли](xref:microsoft.quantum.machines.toffoli-simulator)
- [Симулятор трассировки тактов](xref:microsoft.quantum.machines.qc-trace-simulator.intro)