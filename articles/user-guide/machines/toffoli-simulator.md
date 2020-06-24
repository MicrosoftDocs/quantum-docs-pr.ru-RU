---
title: Симулятор Тоффоли для пакета разработки тактов
description: Сведения о симуляторе Тоффоли Microsoft КДК — имитаторе Специального целевого симулятора, который можно использовать с миллионами Кубитс.
author: alan-geller
ms.author: ageller@microsoft.com
ms.date: 01/16/2019
ms.topic: article
uid: microsoft.quantum.machines.toffoli-simulator
ms.openlocfilehash: 8a29caaa0fa058600a74e7d130e644374cbfa19c
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2020
ms.locfileid: "85276029"
---
# <a name="quantum-development-kit-toffoli-simulator"></a><span data-ttu-id="0150b-103">Симулятор Тоффоли для пакета разработки тактов</span><span class="sxs-lookup"><span data-stu-id="0150b-103">Quantum Development Kit Toffoli Simulator</span></span>

<span data-ttu-id="0150b-104">Пакет разработки такта — это симулятор Тоффоли, который представляет собой специализированный симулятор, который может имитировать алгоритмы обработки тактов, ограниченные X, кнот и несколькими управляемыми тактовыми операциями X (все классическая логика и вычисления доступны).</span><span class="sxs-lookup"><span data-stu-id="0150b-104">The Quantum Development Kit provides a Toffoli simulator, which is a special-purpose simulator that can simulate quantum algorithms that are limited to X, CNOT, and multi-controlled X quantum operations (all classical logic and computations are available).</span></span>

<span data-ttu-id="0150b-105">Хотя симулятор Тоффоли гораздо более ограничен в работе, чем [имитатор полного состояния](xref:microsoft.quantum.machines.full-state-simulator), он может имитировать гораздо больше Кубитс.</span><span class="sxs-lookup"><span data-stu-id="0150b-105">While the Toffoli simulator is much more restricted in operation than the [full state simulator](xref:microsoft.quantum.machines.full-state-simulator), it can simulate far more qubits.</span></span>
<span data-ttu-id="0150b-106">Симулятор Тоффоли можно использовать с миллионами Кубитс, а полный симулятор штата обычно ограничен 30.</span><span class="sxs-lookup"><span data-stu-id="0150b-106">The Toffoli simulator can be used with millions of qubits, while the full state simulator is generally limited to about 30.</span></span>
<span data-ttu-id="0150b-107">Он может выполнять и отлаживать ограниченный набор тактовых алгоритмов, написанных на компьютере Q #. Например, Oracle, которые оценивают логические функции, могут быть реализованы с помощью этих шлюзов и поэтому протестированы на изменение большого количества Кубитс с помощью этого симулятора.</span><span class="sxs-lookup"><span data-stu-id="0150b-107">It can execute and debug a limited set of quantum algorithms written in Q# on your computer; for instance, oracles that evaluate Boolean functions can be implemented using these gates and so tested on vary large numbers of qubits using this simulator.</span></span>

<span data-ttu-id="0150b-108">Этот тактовый симулятор предоставляется через `ToffoliSimulator` класс.</span><span class="sxs-lookup"><span data-stu-id="0150b-108">This quantum simulator is exposed via the `ToffoliSimulator` class.</span></span>
<span data-ttu-id="0150b-109">Чтобы использовать симулятор, просто создайте экземпляр этого класса и передайте его `Run` методу операции такта, которую необходимо выполнить, вместе с остальными параметрами:</span><span class="sxs-lookup"><span data-stu-id="0150b-109">To use the simulator, simply create an instance of this class and pass it to the `Run` method of the quantum operation you want to execute along with the rest of the parameters:</span></span>

```csharp
    var sim = new ToffoliSimulator();
    var res = myOperation.Run(sim).Result;
    ///...
```

## <a name="other-operations"></a><span data-ttu-id="0150b-110">Другие операции</span><span class="sxs-lookup"><span data-stu-id="0150b-110">Other Operations</span></span>

<span data-ttu-id="0150b-111">`ToffoliSimulator`Поддерживает вращение и возведен пол, например `R` и `Exp` , когда полученная операция равна `X` или к удостоверению.</span><span class="sxs-lookup"><span data-stu-id="0150b-111">The `ToffoliSimulator` supports rotations and exponentiated Paulis, such as `R` and `Exp`, when the resulting operation is equal to `X` or to the identity.</span></span>

<span data-ttu-id="0150b-112">Измерения и Assert поддерживаются, но только на основе Паули `Z` .</span><span class="sxs-lookup"><span data-stu-id="0150b-112">Measurement and assert are supported, but only in the Pauli `Z` basis.</span></span>
<span data-ttu-id="0150b-113">Обратите внимание, что вероятность какого-либо измерения всегда равна 0 или 1; в симуляторе Тоффоли нет случайных значений.</span><span class="sxs-lookup"><span data-stu-id="0150b-113">Note that the probability of some measurement is always either 0 or 1; there is no randomness in the Toffoli simulator.</span></span>

<span data-ttu-id="0150b-114">Поддерживаются `DumpMachine` и `DumpRegister`.</span><span class="sxs-lookup"><span data-stu-id="0150b-114">`DumpMachine` and `DumpRegister` are supported.</span></span>
<span data-ttu-id="0150b-115">Оба они выводят текущее `Z` состояние каждого кубит, по одному кубит на строку.</span><span class="sxs-lookup"><span data-stu-id="0150b-115">They both output the current `Z`-basis state of each qubit, one qubit per line.</span></span>

## <a name="qubitcount"></a><span data-ttu-id="0150b-116">кубиткаунт</span><span class="sxs-lookup"><span data-stu-id="0150b-116">QubitCount</span></span>

<span data-ttu-id="0150b-117">По умолчанию `ToffoliSimulator` выделяется место для 65 536 Кубитс.</span><span class="sxs-lookup"><span data-stu-id="0150b-117">By default, the `ToffoliSimulator` allocates space for 65,536 qubits.</span></span>
<span data-ttu-id="0150b-118">Если алгоритм требует больше этого значения, можно изменить счетчик кубит, предоставив значение для `qubitCount` параметра конструктору.</span><span class="sxs-lookup"><span data-stu-id="0150b-118">If your algorithm requires more than this, you can change the qubit count by providing a value for the `qubitCount` parameter to the constructor.</span></span>
<span data-ttu-id="0150b-119">Для каждого дополнительного кубит требуется дополнительный байт памяти, поэтому нет значительных затрат на оценку количества Кубитс, которые вам понадобятся.</span><span class="sxs-lookup"><span data-stu-id="0150b-119">Each additional qubit requires an additional byte of memory, so there is no significant cost to overestimating the number of qubits you'll need.</span></span>

<span data-ttu-id="0150b-120">Пример:</span><span class="sxs-lookup"><span data-stu-id="0150b-120">For example:</span></span>

```csharp
    var sim = new ToffoliSimulator(qubitCount: 1000000);
    var res = myLargeOperation.Run(sim).Result;
```
