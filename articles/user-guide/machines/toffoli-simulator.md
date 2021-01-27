---
title: Имитатор Тоффоли Simulator — пакет средств разработки тактов
description: Сведения о симуляторе Тоффоли Microsoft КДК — имитаторе Специального целевого симулятора, который можно использовать с миллионами Кубитс.
author: alan-geller
ms.author: ageller
ms.date: 6/25/2020
ms.topic: conceptual
uid: microsoft.quantum.machines.toffoli-simulator
no-loc:
- Q#
- $$v
ms.openlocfilehash: 84b958912ab5116a3181c8eff4f331fc8394604c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858570"
---
# <a name="quantum-development-kit-qdk-toffoli-simulator"></a>Симулятор Тоффоли для пакета разработки такта (КДК)

Симулятор Тоффоли КДК — это специализированный симулятор с ограниченной областью действия, который поддерживает только `X` `CNOT` `X` операции с тактовыми операциями, и с несколькими управляемыми. Доступны все классические логики и вычисления.

В то время как симулятор Тоффоли более ограничен в функциональности, чем [имитатор полного состояния](xref:microsoft.quantum.machines.full-state-simulator), он имеет преимущество в возможности имитировать гораздо больше Кубитс. Симулятор Тоффоли можно использовать с миллионами Кубитс, в то время как имитатор полного состояния ограничен 30 Кубитс. Это полезно, например, при использовании Oracle, оценивающих логические функции. они могут быть реализованы с использованием ограниченного набора поддерживаемых алгоритмов и протестированы в большом количестве Кубитс.

## <a name="invoking-the-toffoli-simulator"></a>Вызов симулятора Тоффоли

Вы предоставляете симулятор Тоффоли через `ToffoliSimulator` класс. Дополнительные сведения см. [в статье способы запуска Q# программы](xref:microsoft.quantum.guide.host-programs).

### <a name="invoking-the-toffoli-simulator-from-c"></a>Вызов симулятора Тоффоли из C #

Как и в случае с другими целевыми компьютерами, вам сначала нужно создать экземпляр класса `ToffoliSimulator`, а затем передать его в качестве первого параметра метода `Run` операции.

Учтите, что в отличие от класса `QuantumSimulator` класс `ToffoliSimulator` не реализует интерфейс <xref:System.IDisposable>, поэтому вам не нужно заключать его в оператор `using`.

```csharp
    var sim = new ToffoliSimulator();
    var res = myOperation.Run(sim).Result;
    ///...
```

### <a name="invoking-the-toffoli-simulator-from-python"></a>Вызов симулятора Тоффоли из Python

Используйте метод [toffoli_simulate ()](https://docs.microsoft.com/python/qsharp-core/qsharp.loader.qsharpcallable) из библиотеки Python с импортированной Q# операцией:

```python
qubit_result = myOperation.toffoli_simulate()
```

### <a name="invoking-the-toffoli-simulator-from-the-command-line"></a>Вызов симулятора Тоффоли из командной строки

При запуске Q# программы из командной строки используйте параметр **--симулятор** (или **-s** ), чтобы указать целевой компьютер имитатора Тоффоли. Следующая команда запускает программу с помощью средства оценки ресурсов: 

```dotnetcli
dotnet run -s ToffoliSimulator
```

### <a name="invoking-the-toffoli-simulator-from-juptyer-notebooks"></a>Вызов симулятора Тоффоли из записных книжек Жуптер

Используйте команду I Q# Magic [% Тоффоли](xref:microsoft.quantum.iqsharp.magic-ref.toffoli) для выполнения Q# операции.

```
%toffoli myOperation
```

## <a name="supported-operations"></a>Поддерживаемые операции

Имитатор Тоффоли поддерживает:

* Повороты и возведен пол, например `R` и `Exp` , когда итоговая операция равна `X` или матрица идентификаторов.
* Операции измерения и [утверждения](xref:Microsoft.Quantum.Diagnostics.AssertMeasurement) , но только на основе Паули `Z` . Обратите внимание, что вероятность операции измерения всегда равна **0** или **1**. в симуляторе Тоффоли нет случайных значений.
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