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
# <a name="quantum-development-kit-qdk-toffoli-simulator"></a><span data-ttu-id="e2f11-103">Симулятор Тоффоли для пакета разработки такта (КДК)</span><span class="sxs-lookup"><span data-stu-id="e2f11-103">Quantum Development Kit (QDK) Toffoli simulator</span></span>

<span data-ttu-id="e2f11-104">Симулятор Тоффоли КДК — это специализированный симулятор с ограниченной областью действия, который поддерживает только `X` `CNOT` `X` операции с тактовыми операциями, и с несколькими управляемыми.</span><span class="sxs-lookup"><span data-stu-id="e2f11-104">The QDK Toffoli simulator is a special-purpose simulator with a limited scope and only supports `X`, `CNOT`, and multi-controlled `X` quantum operations.</span></span> <span data-ttu-id="e2f11-105">Доступны все классические логики и вычисления.</span><span class="sxs-lookup"><span data-stu-id="e2f11-105">All classical logic and computations are available.</span></span>

<span data-ttu-id="e2f11-106">В то время как симулятор Тоффоли более ограничен в функциональности, чем [имитатор полного состояния](xref:microsoft.quantum.machines.full-state-simulator), он имеет преимущество в возможности имитировать гораздо больше Кубитс.</span><span class="sxs-lookup"><span data-stu-id="e2f11-106">While the Toffoli simulator is more restricted in functionality than the [full state simulator](xref:microsoft.quantum.machines.full-state-simulator), it has the advantage of being able to simulate far more qubits.</span></span> <span data-ttu-id="e2f11-107">Симулятор Тоффоли можно использовать с миллионами Кубитс, в то время как имитатор полного состояния ограничен 30 Кубитс.</span><span class="sxs-lookup"><span data-stu-id="e2f11-107">The Toffoli simulator can be used with millions of qubits, while the full state simulator is limited to about 30 qubits.</span></span> <span data-ttu-id="e2f11-108">Это полезно, например, при использовании Oracle, оценивающих логические функции. они могут быть реализованы с использованием ограниченного набора поддерживаемых алгоритмов и протестированы в большом количестве Кубитс.</span><span class="sxs-lookup"><span data-stu-id="e2f11-108">This is useful, for example, with oracles that evaluate Boolean functions - they can be implemented using the limited set of supported algorithms and tested on a large number of qubits.</span></span>

## <a name="invoking-the-toffoli-simulator"></a><span data-ttu-id="e2f11-109">Вызов симулятора Тоффоли</span><span class="sxs-lookup"><span data-stu-id="e2f11-109">Invoking the Toffoli simulator</span></span>

<span data-ttu-id="e2f11-110">Вы предоставляете симулятор Тоффоли через `ToffoliSimulator` класс.</span><span class="sxs-lookup"><span data-stu-id="e2f11-110">You expose the Toffoli simulator via the `ToffoliSimulator` class.</span></span> <span data-ttu-id="e2f11-111">Дополнительные сведения см. [в статье способы запуска Q# программы](xref:microsoft.quantum.guide.host-programs).</span><span class="sxs-lookup"><span data-stu-id="e2f11-111">For additional details, see [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs).</span></span>

### <a name="invoking-the-toffoli-simulator-from-c"></a><span data-ttu-id="e2f11-112">Вызов симулятора Тоффоли из C #</span><span class="sxs-lookup"><span data-stu-id="e2f11-112">Invoking the Toffoli simulator from C#</span></span>

<span data-ttu-id="e2f11-113">Как и в случае с другими целевыми компьютерами, вам сначала нужно создать экземпляр класса `ToffoliSimulator`, а затем передать его в качестве первого параметра метода `Run` операции.</span><span class="sxs-lookup"><span data-stu-id="e2f11-113">As with other target machines, you first create an instance of the `ToffoliSimulator` class and then pass it as the first parameter of an operation's `Run` method.</span></span>

<span data-ttu-id="e2f11-114">Учтите, что в отличие от класса `QuantumSimulator` класс `ToffoliSimulator` не реализует интерфейс <xref:System.IDisposable>, поэтому вам не нужно заключать его в оператор `using`.</span><span class="sxs-lookup"><span data-stu-id="e2f11-114">Note that, unlike the `QuantumSimulator` class, the `ToffoliSimulator` class does not implement the <xref:System.IDisposable> interface, and thus you do not need to enclose it within a `using` statement.</span></span>

```csharp
    var sim = new ToffoliSimulator();
    var res = myOperation.Run(sim).Result;
    ///...
```

### <a name="invoking-the-toffoli-simulator-from-python"></a><span data-ttu-id="e2f11-115">Вызов симулятора Тоффоли из Python</span><span class="sxs-lookup"><span data-stu-id="e2f11-115">Invoking the Toffoli simulator from Python</span></span>

<span data-ttu-id="e2f11-116">Используйте метод [toffoli_simulate ()](https://docs.microsoft.com/python/qsharp-core/qsharp.loader.qsharpcallable) из библиотеки Python с импортированной Q# операцией:</span><span class="sxs-lookup"><span data-stu-id="e2f11-116">Use the [toffoli_simulate()](https://docs.microsoft.com/python/qsharp-core/qsharp.loader.qsharpcallable) method from the Python library with the imported Q# operation:</span></span>

```python
qubit_result = myOperation.toffoli_simulate()
```

### <a name="invoking-the-toffoli-simulator-from-the-command-line"></a><span data-ttu-id="e2f11-117">Вызов симулятора Тоффоли из командной строки</span><span class="sxs-lookup"><span data-stu-id="e2f11-117">Invoking the Toffoli simulator from the command line</span></span>

<span data-ttu-id="e2f11-118">При запуске Q# программы из командной строки используйте параметр **--симулятор** (или **-s** ), чтобы указать целевой компьютер имитатора Тоффоли.</span><span class="sxs-lookup"><span data-stu-id="e2f11-118">When running a Q# program from the command line, use the **--simulator** (or **-s** shortcut) parameter to specify the Toffoli simulator target machine.</span></span> <span data-ttu-id="e2f11-119">Следующая команда запускает программу с помощью средства оценки ресурсов:</span><span class="sxs-lookup"><span data-stu-id="e2f11-119">The following command runs a program using the resources estimator:</span></span> 

```dotnetcli
dotnet run -s ToffoliSimulator
```

### <a name="invoking-the-toffoli-simulator-from-juptyer-notebooks"></a><span data-ttu-id="e2f11-120">Вызов симулятора Тоффоли из записных книжек Жуптер</span><span class="sxs-lookup"><span data-stu-id="e2f11-120">Invoking the Toffoli simulator from Juptyer Notebooks</span></span>

<span data-ttu-id="e2f11-121">Используйте команду I Q# Magic [% Тоффоли](xref:microsoft.quantum.iqsharp.magic-ref.toffoli) для выполнения Q# операции.</span><span class="sxs-lookup"><span data-stu-id="e2f11-121">Use the IQ# magic command [%toffoli](xref:microsoft.quantum.iqsharp.magic-ref.toffoli) to run the Q# operation.</span></span>

```
%toffoli myOperation
```

## <a name="supported-operations"></a><span data-ttu-id="e2f11-122">Поддерживаемые операции</span><span class="sxs-lookup"><span data-stu-id="e2f11-122">Supported operations</span></span>

<span data-ttu-id="e2f11-123">Имитатор Тоффоли поддерживает:</span><span class="sxs-lookup"><span data-stu-id="e2f11-123">The Toffoli simulator supports:</span></span>

* <span data-ttu-id="e2f11-124">Повороты и возведен пол, например `R` и `Exp` , когда итоговая операция равна `X` или матрица идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="e2f11-124">Rotations and exponentiated Paulis, such as `R` and `Exp`, when the resulting operation equals `X` or the identity matrix.</span></span>
* <span data-ttu-id="e2f11-125">Операции измерения и [утверждения](xref:Microsoft.Quantum.Diagnostics.AssertMeasurement) , но только на основе Паули `Z` .</span><span class="sxs-lookup"><span data-stu-id="e2f11-125">Measurement and [assert](xref:Microsoft.Quantum.Diagnostics.AssertMeasurement) operations, but only in the Pauli `Z` basis.</span></span> <span data-ttu-id="e2f11-126">Обратите внимание, что вероятность операции измерения всегда равна **0** или **1**. в симуляторе Тоффоли нет случайных значений.</span><span class="sxs-lookup"><span data-stu-id="e2f11-126">Note that a measurement operation's probability is always either **0** or **1**; there is no randomness in the Toffoli simulator.</span></span>
* <span data-ttu-id="e2f11-127">`DumpMachine``DumpRegister`функции и.</span><span class="sxs-lookup"><span data-stu-id="e2f11-127">`DumpMachine` and `DumpRegister` functions.</span></span>
<span data-ttu-id="e2f11-128">Обе функции выводят текущее `Z` состояние каждого кубит, по одному кубит на строку.</span><span class="sxs-lookup"><span data-stu-id="e2f11-128">Both functions output the current `Z`-basis state of each qubit, one qubit per line.</span></span>

## <a name="specifying-the-number-of-qubits"></a><span data-ttu-id="e2f11-129">Указание числа Кубитс</span><span class="sxs-lookup"><span data-stu-id="e2f11-129">Specifying the number of qubits</span></span>

<span data-ttu-id="e2f11-130">По умолчанию `ToffoliSimulator` экземпляр выделяет место для 65 536 Кубитс.</span><span class="sxs-lookup"><span data-stu-id="e2f11-130">By default, a `ToffoliSimulator` instance allocates space for 65,536 qubits.</span></span>
<span data-ttu-id="e2f11-131">Если для алгоритма требуется больше Кубитс, можно указать число кубит, указав значение для `qubitCount` параметра конструктору.</span><span class="sxs-lookup"><span data-stu-id="e2f11-131">If your algorithm requires more qubits than this, you can specify the qubit count by providing a value for the `qubitCount` parameter to the constructor.</span></span>
<span data-ttu-id="e2f11-132">Для каждого дополнительного кубит требуется только один байт памяти, поэтому нет значительных затрат на оценку количества Кубитс, которые вам понадобятся.</span><span class="sxs-lookup"><span data-stu-id="e2f11-132">Each additional qubit requires only one byte of memory, so there is no significant cost to overestimating the number of qubits you'll need.</span></span>

<span data-ttu-id="e2f11-133">Пример:</span><span class="sxs-lookup"><span data-stu-id="e2f11-133">For example:</span></span>

```csharp
    var sim = new ToffoliSimulator(qubitCount: 1000000);
    var res = myLargeOperation.Run(sim).Result;
```

## <a name="see-also"></a><span data-ttu-id="e2f11-134">См. также</span><span class="sxs-lookup"><span data-stu-id="e2f11-134">See also</span></span>

- [<span data-ttu-id="e2f11-135">Оценщик ресурсов такта</span><span class="sxs-lookup"><span data-stu-id="e2f11-135">Quantum Resources Estimator</span></span>](xref:microsoft.quantum.machines.resources-estimator)
- [<span data-ttu-id="e2f11-136">Симулятор трассировки тактов</span><span class="sxs-lookup"><span data-stu-id="e2f11-136">Quantum Trace simulator</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.intro)
- [<span data-ttu-id="e2f11-137">Имитатор полного состояния такта</span><span class="sxs-lookup"><span data-stu-id="e2f11-137">Quantum Full State simulator</span></span>](xref:microsoft.quantum.machines.full-state-simulator) 