---
title: Имитатор Тоффоли Simulator — пакет средств разработки тактов
description: Сведения о симуляторе Тоффоли Microsoft КДК — имитаторе Специального целевого симулятора, который можно использовать с миллионами Кубитс.
author: alan-geller
ms.author: ageller@microsoft.com
ms.date: 6/25/2020
ms.topic: article
uid: microsoft.quantum.machines.toffoli-simulator
ms.openlocfilehash: a6ceee592e628215511ec83475d9e25bf54674f7
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/21/2020
ms.locfileid: "86870623"
---
# <a name="quantum-development-kit-qdk-toffoli-simulator"></a>Симулятор Тоффоли для пакета разработки такта (КДК)

Симулятор Тоффоли КДК — это специализированный симулятор с ограниченной областью действия, который поддерживает только `X` `CNOT` `X` операции с тактовыми операциями, и с несколькими управляемыми. Доступны все классические логики и вычисления.

В то время как симулятор Тоффоли более ограничен в функциональности, чем [имитатор полного состояния](xref:microsoft.quantum.machines.full-state-simulator), он имеет преимущество в возможности имитировать гораздо больше Кубитс. Симулятор Тоффоли можно использовать с миллионами Кубитс, в то время как имитатор полного состояния ограничен 30 Кубитс. Это полезно, например, при использовании Oracle, оценивающих логические функции. они могут быть реализованы с использованием ограниченного набора поддерживаемых алгоритмов и протестированы в большом количестве Кубитс.

## <a name="invoking-the-toffoli-simulator"></a>Вызов симулятора Тоффоли

Вы предоставляете симулятор Тоффоли через `ToffoliSimulator` класс. Дополнительные сведения см. в разделе [способы запуска программы Q #](xref:microsoft.quantum.guide.host-programs).

### <a name="invoking-the-toffoli-simulator-from-c"></a>Вызов симулятора Тоффоли из C #

Как и в случае с другими целевыми компьютерами, сначала необходимо создать экземпляр `ToffoliSimulator` класса, а затем передать его в качестве первого параметра метода операции `Run` .

Обратите внимание, что, в отличие от `QuantumSimulator` класса, `ToffoliSimulator` класс не реализует <xref:System.IDisposable> интерфейс, поэтому вам не нужно заключать его в `using` оператор.

```csharp
    var sim = new ToffoliSimulator();
    var res = myOperation.Run(sim).Result;
    ///...
```

### <a name="invoking-the-toffoli-simulator-from-python"></a>Вызов симулятора Тоффоли из Python

Используйте метод [toffoli_simulate ()](https://docs.microsoft.com/python/qsharp/qsharp.loader.qsharpcallable) из библиотеки Python с импортированной операцией Q #:

```python
qubit_result = myOperation.toffoli_simulate()
```

### <a name="invoking-the-toffoli-simulator-from-the-command-line"></a>Вызов симулятора Тоффоли из командной строки

При выполнении программы Q # из командной строки используйте параметр **--симулятор** (или **-s** ), чтобы указать целевой компьютер имитатора Тоффоли. Следующая команда запускает программу с помощью средства оценки ресурсов: 

```dotnetcli
dotnet run -s ToffoliSimulator
```

### <a name="invoking-the-toffoli-simulator-from-juptyer-notebooks"></a>Вызов симулятора Тоффоли из записных книжек Жуптер

Используйте команду IQ # Magic [% Тоффоли](xref:microsoft.quantum.iqsharp.magic-ref.toffoli) , чтобы выполнить операцию Q #.

```
%toffoli myOperation
```

## <a name="supported-operations"></a>Поддерживаемые операции

Имитатор Тоффоли поддерживает:

* Повороты и возведен пол, например `R` и `Exp` , когда итоговая операция равна `X` или матрица идентификаторов.
* Операции измерения и [утверждения](xref:microsoft.quantum.diagnostics.assertmeasurement) , но только на основе Паули `Z` . Обратите внимание, что вероятность операции измерения всегда равна **0** или **1**. в симуляторе Тоффоли нет случайных значений.
* `DumpMachine``DumpRegister`функции и.
Обе функции выводят текущее `Z` состояние каждого кубит, по одному кубит на строку.

## <a name="specifying-the-number-of-qubits"></a>Указание числа Кубитс

По умолчанию `ToffoliSimulator` экземпляр выделяет место для 65 536 Кубитс.
Если для алгоритма требуется больше Кубитс, можно указать число кубит, указав значение для `qubitCount` параметра конструктору.
Для каждого дополнительного кубит требуется только один байт памяти, поэтому нет значительных затрат на оценку количества Кубитс, которые вам понадобятся.

Пример:

```csharp
    var sim = new ToffoliSimulator(qubitCount: 1000000);
    var res = myLargeOperation.Run(sim).Result;
```

## <a name="see-also"></a>См. также

- [Оценщик ресурсов такта](xref:microsoft.quantum.machines.resources-estimator)
- [Симулятор трассировки тактов](xref:microsoft.quantum.machines.qc-trace-simulator.intro)
- [Имитатор полного состояния такта](xref:microsoft.quantum.machines.full-state-simulator) 