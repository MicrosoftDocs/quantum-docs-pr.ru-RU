---
title: 'Q # Интродутион'
description: 'Краткое введение в тактовые программы в Q #'
author: beheim
ms.author: beheim
ms.date: 11/08/2020
ms.topic: article
uid: microsoft.quantum.guide.programs
ms.openlocfilehash: 975bcda5e0042406b465a83f17f1d2d3f5a1ec4f
ms.sourcegitcommit: b930bb59a1ba8f41d2edc9ed98197109aa8c7f1b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96234323"
---
# <a name="q-quantum-programming-language"></a><span data-ttu-id="43212-103">Язык программирования на такт Q #</span><span class="sxs-lookup"><span data-stu-id="43212-103">Q# Quantum Programming Language</span></span>

<span data-ttu-id="43212-104">Все, что необходимо знать о языке программирования Q #, подробно описано в статье о [языке q #](xref:microsoft.quantum.qsharp.index).</span><span class="sxs-lookup"><span data-stu-id="43212-104">Everything you need to know about the Q# programming language is detailed in the [Q# language guide](xref:microsoft.quantum.qsharp.index).</span></span> <span data-ttu-id="43212-105">Как и все остальное, наш [процесс проектирования языка](https://github.com/microsoft/qsharp-language#q-language-and-core-libraries-design) — это открытый исходный код, и мы будем рады Вашим вкладам.</span><span class="sxs-lookup"><span data-stu-id="43212-105">Like anything else, our [language design process](https://github.com/microsoft/qsharp-language#q-language-and-core-libraries-design) is open source and we welcome contributions.</span></span>
<span data-ttu-id="43212-106">Дополнительные сведения об основах и мотивации в Q # см. в разделе [почему нам требуется q #?](https://devblogs.microsoft.com/qsharp/why-do-we-need-q/).</span><span class="sxs-lookup"><span data-stu-id="43212-106">For more background about the foundations and motivation behind Q#, see [Why do we need Q#?](https://devblogs.microsoft.com/qsharp/why-do-we-need-q/).</span></span>  
<span data-ttu-id="43212-107">Q # поставляется в составе пакета средств разработки тактов (КДК) для краткого обзора. Ознакомьтесь [с тем, что такое КДК?](xref:microsoft.quantum.overview.q-sharp).</span><span class="sxs-lookup"><span data-stu-id="43212-107">Q# is shipped as part of the Quantum Development Kit (QDK) For a quick overview, check out [What is the QDK?](xref:microsoft.quantum.overview.q-sharp).</span></span> 

## <a name="what-is-a-quantum-program"></a><span data-ttu-id="43212-108">Что такое тактовая программа?</span><span class="sxs-lookup"><span data-stu-id="43212-108">What is a quantum program?</span></span>

<span data-ttu-id="43212-109">Тактовая программа может рассматриваться как определенный набор классических подпрограмм, которые при вызове выполняют вычисления путем взаимодействия с тактовой системой. Программа, написанная в Q #, не моделирует состояние такта напрямую, а описывает, как классический контрольный компьютер взаимодействует с Кубитс.</span><span class="sxs-lookup"><span data-stu-id="43212-109">A quantum program can be seen as a particular set of classical subroutines which, when called, perform a computation by interacting with a quantum system; a program written in Q# does not directly model the quantum state, but rather describes how a classical control computer interacts with qubits.</span></span>
<span data-ttu-id="43212-110">Это позволяет нам полностью *не* зависеть от состояния такта, даже на каждом целевом компьютере, для которого в зависимости от компьютера могут использоваться разные интерпретации.</span><span class="sxs-lookup"><span data-stu-id="43212-110">This allows us to be entirely agnostic about what a quantum state even *is* on each target machine, which might have different interpretations depending on the machine.</span></span> 

<span data-ttu-id="43212-111">Важным следствием этого является то, что Q # не имеет возможности интроспект в состояние кубит или других свойств тактовой частоты напрямую, что гарантирует, что программа Q # может быть физически выполнена на тактовой системе.</span><span class="sxs-lookup"><span data-stu-id="43212-111">An important consequence of that is that Q# has no ability to introspect into the state of a qubit or other properties of quantum mechanics directly, which guarantees that a Q# program can be physically executed on a quantum computer.</span></span>
<span data-ttu-id="43212-112">Вместо этого программа может вызывать такие операции, как [`Measure`](xref:Microsoft.Quantum.Intrinsic.Measure) Извлечение классической информации из кубит.</span><span class="sxs-lookup"><span data-stu-id="43212-112">Instead, a program can call operations such as [`Measure`](xref:Microsoft.Quantum.Intrinsic.Measure) to extract classical information from a qubit.</span></span>

<span data-ttu-id="43212-113">После выделения кубит можно передать в операции и функции, которые также называются *вызываемыми*.</span><span class="sxs-lookup"><span data-stu-id="43212-113">Once allocated, a qubit can be passed to operations and functions, also referred to as *callables*.</span></span> <span data-ttu-id="43212-114">В определенном смысле, это все, что программа Q # может делать с кубит; Любые прямые действия с состоянием кубит определяются *встроенными* вызываемыми функциями, такими как [`X`](xref:Microsoft.Quantum.Intrinsic.X) и [`H`](xref:Microsoft.Quantum.Intrinsic.H) -т. е. вызываемые объекты, реализации которых не определяются в Q #, а определяются целевым компьютером.</span><span class="sxs-lookup"><span data-stu-id="43212-114">In some sense, this is all that a Q# program can do with a qubit; Any direct actions on state of a qubit are all defined by *intrinsic* callables such as [`X`](xref:Microsoft.Quantum.Intrinsic.X) and [`H`](xref:Microsoft.Quantum.Intrinsic.H) - i.e. callables whose implementations are not defined within Q# but are instead defined by the target machine.</span></span> <span data-ttu-id="43212-115">*Фактически эти операции делаются* только на целевом компьютере, используемом для запуска конкретной программы Q #.</span><span class="sxs-lookup"><span data-stu-id="43212-115">What these operations actually *do* is only made concrete by the target machine we use to run the particular Q# program.</span></span>

<span data-ttu-id="43212-116">Например, если запустить программу в [симуляторе полного состояния](xref:microsoft.quantum.machines.full-state-simulator), симулятор выполняет соответствующие математические операции с имитацией тактовой системы.</span><span class="sxs-lookup"><span data-stu-id="43212-116">For example, if running the program on our [full-state simulator](xref:microsoft.quantum.machines.full-state-simulator), the simulator performs the corresponding mathematical operations to the simulated quantum system.</span></span>
<span data-ttu-id="43212-117">Но в будущем, когда целевой компьютер является реальным компьютером-тактом, вызов таких операций в Q # направляет компьютер-такт для выполнения соответствующих *реальных* операций в *реальной* тактовой системе (например, для точного времени лазерных импульсов).</span><span class="sxs-lookup"><span data-stu-id="43212-117">But looking toward the future, when the target machine is a real quantum computer, calling such operations in Q# will direct the quantum computer to perform the corresponding *real* operations on the *real* quantum system (e.g. precisely timed laser pulses).</span></span>

<span data-ttu-id="43212-118">Программа Q # повторно объединяет эти операции, как определено на целевом компьютере, для создания новых операций более высокого уровня для вычисления тактовых вычислений.</span><span class="sxs-lookup"><span data-stu-id="43212-118">A Q# program recombines these operations as defined by a target machine to create new, higher-level operations to express quantum computation.</span></span>
<span data-ttu-id="43212-119">Таким образом, Q # упрощает выражать логику базового и гибридного такта, а также общие алгоритмы в отношении структуры целевого компьютера или симулятора.</span><span class="sxs-lookup"><span data-stu-id="43212-119">In this way, Q# makes it easy to express the logic underlying quantum and hybrid quantum–classical algorithms, while also being general with respect to the structure of a target machine or simulator.</span></span>

<span data-ttu-id="43212-120">Простой пример — Следующая программа, которая выделяет один кубит в состоянии $ \кет {0} $, затем применяет `H` к ней операцию хадамард и измеряет результат на `PauliZ` основе.</span><span class="sxs-lookup"><span data-stu-id="43212-120">A simple example is the following program, which allocates one qubit in the $\ket{0}$ state, then applies a Hadamard operation `H` to it and measures the result in the `PauliZ` basis.</span></span>

```qsharp
@EntryPoint()
operation MeasureOneQubit() : Result {
    // The following using block creates a fresh qubit and initializes it
    // in the |0〉 state.
    using (qubit = Qubit()) {
        // We apply a Hadamard operation H to the state, thereby preparing the
        // state 1 / sqrt(2) (|0〉 + |1〉).
        H(qubit);
        // Now we measure the qubit in Z-basis.
        let result = M(qubit);
        // As the qubit is now in an eigenstate of the measurement operator,
        // we reset the qubit before releasing it.
        if (result == One) { X(qubit); }
        // Finally, we return the result of the measurement.
        return result;
    }
}
```

<span data-ttu-id="43212-121">Наш [тактовый Катас](https://github.com/microsoft/QuantumKatas#introduction) дает хорошее представление о [концепциях тактовых вычислений](https://github.com/microsoft/QuantumKatas#quantum-computing-concepts-qubits-and-gates) , таких как общие операции с тактами, а также об управлении Кубитс.</span><span class="sxs-lookup"><span data-stu-id="43212-121">Our [Quantum Katas](https://github.com/microsoft/QuantumKatas#introduction) give a good introduction on [Quantum Computing Concepts](https://github.com/microsoft/QuantumKatas#quantum-computing-concepts-qubits-and-gates) such as common quantum operations and how to manipulate qubits.</span></span> <span data-ttu-id="43212-122">Дополнительные примеры также можно найти в [подставляемых операциях и функциях](xref:microsoft.quantum.libraries.standard.prelude).</span><span class="sxs-lookup"><span data-stu-id="43212-122">More examples can also be found in [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude).</span></span>



