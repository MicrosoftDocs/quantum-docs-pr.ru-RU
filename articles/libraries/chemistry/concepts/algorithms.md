---
title: Имитация Хамилтониан Dynamics | Документация Майкрософт
description: Моделирование концептуальных документов Хамилтониан Dynamics
author: nathanwiebe2
ms.author: nawiebe@microsoft.com
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.simulationalgorithms
ms.openlocfilehash: 905b03478d453e475fc1e49ea5f88dd0cd2704bc
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/26/2019
ms.locfileid: "73184072"
---
# <a name="simulating-hamiltonian-dynamics"></a><span data-ttu-id="84e1c-103">Имитация Хамилтониан Dynamics</span><span class="sxs-lookup"><span data-stu-id="84e1c-103">Simulating Hamiltonian Dynamics</span></span>

<span data-ttu-id="84e1c-104">После того как Хамилтониан выражается в виде суммы элементарных операторов, Dynamics может быть скомпилирована в фундаментальные операции с использованием узла хорошо известных методов.</span><span class="sxs-lookup"><span data-stu-id="84e1c-104">Once the Hamiltonian has been expressed as a sum of elementary operators the dynamics can then be compiled into fundamental gate operations using a host of well-known techniques.</span></span>
<span data-ttu-id="84e1c-105">Вот три эффективных подхода: Троттер – Сузуки формулы, линейные сочетания унитариес и кубитизатион.</span><span class="sxs-lookup"><span data-stu-id="84e1c-105">Three efficient approaches include are Trotter–Suzuki formulas, linear combinations of unitaries, and qubitization.</span></span>
<span data-ttu-id="84e1c-106">Мы объясним эти три подхода ниже и предведем конкретные примеры в Q #, как реализовать эти методы с помощью библиотеки моделирования Хамилтониан.</span><span class="sxs-lookup"><span data-stu-id="84e1c-106">We explain these three approaches below and give concrete Q# examples of how to implement these methods using the Hamiltonian simulation library.</span></span>


## <a name="trottersuzuki-formulas"></a><span data-ttu-id="84e1c-107">Троттер — формулы Сузуки</span><span class="sxs-lookup"><span data-stu-id="84e1c-107">Trotter–Suzuki Formulas</span></span>
<span data-ttu-id="84e1c-108">Идея Троттер – Сузуки формул проста: Express Хамилтониан в качестве суммы простых для имитации Хамилтонианс, а затем приблизительного суммарного развития в виде последовательности этих упрощенных эволюций.</span><span class="sxs-lookup"><span data-stu-id="84e1c-108">The idea behind Trotter–Suzuki formulas is simple: express the Hamiltonian as a sum of easy to simulate Hamiltonians and then approximate the total evolution as a sequence of these simpler evolutions.</span></span>
<span data-ttu-id="84e1c-109">В частности, Let $H = \sum_{j = 1} ^ m H_j $ Хамилтониан.</span><span class="sxs-lookup"><span data-stu-id="84e1c-109">In particular, let $H=\sum_{j=1}^m H_j$ be the Hamiltonian.</span></span>
<span data-ttu-id="84e1c-110">Затем $ $ e ^ {-i\sum_ {j = 1} ^ m H_j t} = \prod_{j = 1} ^ m e ^ {-iH_j t} + O (m ^ 2 t ^ 2), $ $ скажем, если $t \лл $1, то ошибка в этой аппроксимации становится незначительной.</span><span class="sxs-lookup"><span data-stu-id="84e1c-110">Then, $$ e^{-i\sum_{j=1}^m H_j t} =\prod_{j=1}^m e^{-iH_j t} + O(m^2 t^2), $$ which is to say that, if $t\ll 1$, then the error in this approximation becomes negligible.</span></span>
<span data-ttu-id="84e1c-111">Обратите внимание, что если $e ^ {-i H} $ является обычной экспонентой, то ошибка в этой аппроксимации не будет $O (m ^ 2 t ^ 2) $: это будет ноль.</span><span class="sxs-lookup"><span data-stu-id="84e1c-111">Note that if $e^{-i H t}$ were an ordinary exponential then the error in this approximation would not be $O(m^2 t^2)$: it would be zero.</span></span>
<span data-ttu-id="84e1c-112">Эта ошибка возникает потому, что $e ^ {-ИХТ} $ является экспонентой и, как следствие, при использовании этой формулы возникает ошибка, вызванная тем фактом, что $H _j $ не работает (т *. е.* $H _j H_k \Не H_k H_j $ в целом).</span><span class="sxs-lookup"><span data-stu-id="84e1c-112">This error occurs because $e^{-iHt}$ is an operator exponential and as a result there is an error incurred when using this formula due to the fact that the $H_j$ terms do not commute (*i.e.*, $H_j H_k \ne H_k H_j$ in general).</span></span>

<span data-ttu-id="84e1c-113">Если $t $ имеет большой размер, формулы Троттер – Сузуки можно использовать для точной имитации Dynamics, разбивая ее на последовательность коротких временных шагов.</span><span class="sxs-lookup"><span data-stu-id="84e1c-113">If $t$ is large, Trotter–Suzuki formulas can still be used to simulate the dynamics accurately by breaking it up into a sequence of short time-steps.</span></span>
<span data-ttu-id="84e1c-114">Позвольте $r $ быть числом шагов, предпринятых в ходе эволюции.</span><span class="sxs-lookup"><span data-stu-id="84e1c-114">Let $r$ be the number of steps taken in the time evolution.</span></span>
<span data-ttu-id="84e1c-115">Затем у нас есть $ $ e ^ {-i\sum_ {j = 1} ^ m H_j t} = \лефт (\prod_{j = 1} ^ m e ^ {-iH_j t/r} \ right) ^ r + O (m ^ 2 t ^ 2/r), $ $ что означает, что если $r $ масштабируется как $m ^ 2 t ^ 2/\ Эпсилон $, то ошибку можно сделать не более $ \епсилон $ для любого $ \епсилон > 0 $.</span><span class="sxs-lookup"><span data-stu-id="84e1c-115">Then, we have that $$ e^{-i\sum_{j=1}^m H_j t} =\left(\prod_{j=1}^m e^{-iH_j t/r}\right)^r + O(m^2 t^2/r), $$ which implies that if $r$ scales as $m^2 t^2/\epsilon$ then the error can be made at most $\epsilon$ for any $\epsilon>0$.</span></span>

<span data-ttu-id="84e1c-116">Более точные выражения приближения могут быть построены путем создания последовательности экспоненциальных элементов операторов таким, что условия ошибки отменяются.</span><span class="sxs-lookup"><span data-stu-id="84e1c-116">More accurate approximations can be built by constructing a sequence of operator exponentials such that the error terms cancel.</span></span>
<span data-ttu-id="84e1c-117">Простейшая формула, симметричная Троттер формула или Странг разделение, принимает форму $ $ U_1 (t) = \prod_{j = 1} ^ m e ^ {-iH_j t/2} \ prod_ {j = m} ^ 1 e ^ {-iH_j t} = e ^ {-ИХТ} + O (m ^ 3 t ^ 3), $ $ можно сделать менее $ \епсилон $ для любого $ \епсилон > 0 $, выбрав $ r $ для масштабирования $m ^ {3/2} t ^ {3/2}/\скрт {\ Эпсилон} $.</span><span class="sxs-lookup"><span data-stu-id="84e1c-117">The simplest such formula, the symmetric Trotter formula or Strang splitting, takes the form $$ U_1(t) =\prod_{j=1}^m e^{-iH_j t/2}\prod_{j=m}^1 e^{-iH_j t} = e^{-iHt} + O(m^3 t^3), $$ which can be made less than $\epsilon$ for any $\epsilon>0$ by choosing $r$ to scale as $m^{3/2}t^{3/2}/\sqrt{\epsilon}$.</span></span>

<span data-ttu-id="84e1c-118">На основе $U _1 $ можно создавать еще более высокие формулы Троттер.</span><span class="sxs-lookup"><span data-stu-id="84e1c-118">Even higher-order Trotter formulas can be constructed based on $U_1$.</span></span>
<span data-ttu-id="84e1c-119">Простейший является следующая четвертая формула заказа. впервые появился в Сузуки: $ $ U_2 (t) = U_1 ^ 2 (s_1t) U_1 ([1-4s_1] t) U_1 ^ 2 (s_1 t) = e ^ {-ИХТ} + O (m ^ 5T ^ 5), $ $ Where $s _1 = (4-4 ^ {1/3}) ^{-1}$.</span><span class="sxs-lookup"><span data-stu-id="84e1c-119">The simplest is the following fourth order formula, originally introduced by Suzuki: $$ U_2(t) = U_1^2(s_1t) U_1([1-4s_1]t)U_1^2(s_1 t) = e^{-iHt} +O(m^5t^5), $$ where $s_1 = (4-4^{1/3})^{-1}$.</span></span>
<span data-ttu-id="84e1c-120">Как правило, произвольные формулы высокого порядка могут быть сформированы аналогичным образом. Однако затраты, связанные с использованием более сложных интеграторов, часто перевешивают преимущества за пределы четвертого порядка для большинства практических проблем.</span><span class="sxs-lookup"><span data-stu-id="84e1c-120">In general, arbitrarily high-order formulas can be similarly constructed; however, the costs incurred from using more complex integrators often outweigh the benefits beyond fourth order for most practical problems.</span></span>

<span data-ttu-id="84e1c-121">Чтобы обеспечить работу описанных выше стратегий, необходим метод для имитации широкого класса $e ^ {-iH_j t} $.</span><span class="sxs-lookup"><span data-stu-id="84e1c-121">In order to make the above strategies work, we need to have a method for simulating a wide class of $e^{-iH_j t}$.</span></span>
<span data-ttu-id="84e1c-122">Простейшим семейством Хамилтонианс и, вероятно, наиболее полезным, что мы можем использовать здесь, — это операторы Паули.</span><span class="sxs-lookup"><span data-stu-id="84e1c-122">The simplest family of Hamiltonians, and arguably most useful, that we could use here are Pauli operators.</span></span>
<span data-ttu-id="84e1c-123">Операторы Паули можно легко имитировать, так как они могут быть диагонали с помощью операций Клиффорд (которые являются стандартными шлюзами в тактовых вычислениях).</span><span class="sxs-lookup"><span data-stu-id="84e1c-123">Pauli operators can be easily simulated because they can be diagonalized using Clifford operations (which are standard gates in quantum computing).</span></span>
<span data-ttu-id="84e1c-124">Кроме того, после диагонали их еиженвалуес можно найти, вычисляя четность Кубитс, на которой они работают.</span><span class="sxs-lookup"><span data-stu-id="84e1c-124">Further, once they have been diagonalized, their eigenvalues can be found by computing the parity of the qubits on which they act.</span></span>

<span data-ttu-id="84e1c-125">Например, $ $ e ^ {-Икс\отимес X t} = (Х\отимес H) e ^ {-Из\отимес Z t} (Х\отимес H), $ $ где $ $ e ^ {-i Z \отимес Z t} = \бегин{бматрикс} e ^ {-IT} & 0 & 0 & 0 </span><span class="sxs-lookup"><span data-stu-id="84e1c-125">For example, $$ e^{-iX\otimes X t}= (H\otimes H)e^{-iZ\otimes Z t}(H\otimes H), $$ where $$ e^{-i Z \otimes Z t} = \begin{bmatrix} e^{-it} & 0  & 0  & 0 </span></span>\\\
        <span data-ttu-id="84e1c-126">0 & e ^ {i t} & 0 & 0 </span><span class="sxs-lookup"><span data-stu-id="84e1c-126">0 & e^{i t}  & 0 & 0 </span></span>\\\
        <span data-ttu-id="84e1c-127">0 & 0 & e ^ {IT} & 0 </span><span class="sxs-lookup"><span data-stu-id="84e1c-127">0 & 0 & e^{it} & 0 </span></span>\\\
        <span data-ttu-id="84e1c-128">0 & 0 & 0 & e ^ {-IT} \енд{бматрикс}.</span><span class="sxs-lookup"><span data-stu-id="84e1c-128">0 & 0 & 0 & e^{-it} \end{bmatrix}.</span></span>
<span data-ttu-id="84e1c-129">$ $ Здесь $e ^ {-ИХТ} \кет{00} = e ^ {IT} \кет{00}$ и $e ^ {-ИХТ} \кет{01} = e ^ {-IT} \кет{01}$, который можно увидеть напрямую как следствие того факта, что четность $0 $ равна $0 $, а четность битовой строки $1 $ — $1 $.</span><span class="sxs-lookup"><span data-stu-id="84e1c-129">$$ Here, $e^{-iHt} \ket{00} = e^{it} \ket{00}$ and $e^{-iHt} \ket{01} = e^{-it} \ket{01}$, which can be seen directly as a consequence of the fact that the parity of $00$ is $0$ while the parity of the bit string $01$ is $1$.</span></span>

<span data-ttu-id="84e1c-130">Экспоненциальные операторы Паули можно реализовать непосредственно в Q # с помощью операции <xref:microsoft.quantum.primitive.exp>:</span><span class="sxs-lookup"><span data-stu-id="84e1c-130">Exponentials of Pauli operators can be implemented directly in Q# using the <xref:microsoft.quantum.primitive.exp> operation:</span></span>
```qsharp
    using(qubits = Qubit[2]){
        let pauliString = [PauliX, PauliX];
        let evolutionTime = 1.0;

        // This applies e^{- i X \otimes X t} to qubits 0 and 1.
        Exp(pauliString, - evolutionTime, qubits);
    }
```

<span data-ttu-id="84e1c-131">Для Фермионик Хамилтонианс [декомпозиция "Иордания — Вигнер](xref:microsoft.quantum.chemistry.concepts.jordanwigner) " удобно сопоставляет хамилтониан с суммой операторов Паули.</span><span class="sxs-lookup"><span data-stu-id="84e1c-131">For Fermionic Hamiltonians, the [Jordan–Wigner decomposition](xref:microsoft.quantum.chemistry.concepts.jordanwigner) conveniently maps the Hamiltonian into a sum of Pauli operators.</span></span>
<span data-ttu-id="84e1c-132">Это означает, что описанный выше подход можно легко адаптировать для имитации химия.</span><span class="sxs-lookup"><span data-stu-id="84e1c-132">This means that the above approach can easily be adapted to simulating chemistry.</span></span>
<span data-ttu-id="84e1c-133">Вместо того, чтобы выполнять циклическое переключение всех Паулиных терминов в представлении "Иордания-Вигнер", ниже приведен простой пример того, как будет выглядеть такая имитация в химия.</span><span class="sxs-lookup"><span data-stu-id="84e1c-133">Rather than manually looping over all Pauli terms in the Jordan-Wigner representation, below is a simple example of how executing such a simulation within the chemistry would look.</span></span>
<span data-ttu-id="84e1c-134">Наша начальная точка – это [Вигнер кодировка](xref:microsoft.quantum.chemistry.concepts.jordanwigner) фермионик хамилтониан, выраженная в коде как экземпляр класса `JordanWignerEncoding`.</span><span class="sxs-lookup"><span data-stu-id="84e1c-134">Our starting point is a [Jordan–Wigner encoding](xref:microsoft.quantum.chemistry.concepts.jordanwigner) of the Fermionic Hamiltonian, expressed in code as an instance of the `JordanWignerEncoding` class.</span></span>

```csharp
    // This example uses the following namespaces:
    // using Microsoft.Quantum.Chemistry.OrbitalIntegrals;
    // using Microsoft.Quantum.Chemistry.Fermion;
    // using Microsoft.Quantum.Chemistry.Pauli;
    // using Microsoft.Quantum.Chemistry.QSharpFormat;

    // We create an instance of the `FermionHamiltonian` objecclasst to store the terms.
    var hamiltonian = new OrbitalIntegralHamiltonian(new[] 
    {
        new OrbitalIntegral(new[] { 0, 1, 2, 3 }, 0.123),
        new OrbitalIntegral(new[] { 0, 1 }, 0.456)
    }).ToFermionHamiltonian(IndexConvention.UpDown);

    // We convert this fermion Hamiltonian to a Jordan-Wigner representation.
    var jordanWignerEncoding = hamiltonian.ToPauliHamiltonian(QubitEncoding.JordanWigner);

    // We now convert this representation into a format consumable by Q#.
    var qSharpData = jordanWignerEncoding.ToQSharpFormat();
```

<span data-ttu-id="84e1c-135">Этот формат Вигнер репрсентатион, который используется алгоритмами моделирования Q #, является определяемым пользователем типом `JordanWignerEncodingData`.</span><span class="sxs-lookup"><span data-stu-id="84e1c-135">This format of the Jordan–Wigner reprsentation that is consumable by the Q# simulation algorithms is a user-defined type `JordanWignerEncodingData`.</span></span>
<span data-ttu-id="84e1c-136">В Q # этот формат передается в удобную функцию `TrotterStepOracle`, которая возвращает оператор, приближенный к времени на развитие с помощью Троттер — Сузуки Integrator, в дополнение к другим параметрам, необходимым для его выполнения.</span><span class="sxs-lookup"><span data-stu-id="84e1c-136">Within Q#, this format is passed to a convenience function `TrotterStepOracle` that returns an operator approximating time-evolution using the Trotter—Suzuki integrator, in addition to other parameters required for its execution.</span></span>

```qsharp
// qSharpData passed from driver
let qSharpData = ... 

// Choose the integrator step size
let stepSize = 1.0;

// Choose the order of the Trotter—Suzuki integrator.
let integratorOrder = 4;

// `oracle` is an operation that applies a single time-step of evolution for duration `stepSize`.
// `rescale` is just `1.0/stepSize` -- the number of steps required to simulate unit-time evolution.
// `nQubits` is the number of qubits that must be allocated to run the `oracle` operatrion.
let (nQubits, (rescale, oracle)) =  TrotterStepOracle (qSharpData, stepSize, integratorOrder);

// Let us now apply a single time-step.
using(qubits = Qubit[nQubits]){

    // Apply single step of time-evolution
    oracle(qubits);

    // Reset all qubits to the 0 state to be successfully released.
    ResetAll(qubits);
}
```

<span data-ttu-id="84e1c-137">Важно, что эта реализация применяет некоторые оптимизации, обсуждаемые при [моделировании электронных структур Хамилтонианс с помощью тактовых компьютеров](https://arxiv.org/abs/1001.3855) , и [улучшая тактовые алгоритмы для химия тактов](https://arxiv.org/abs/1403.1539) , чтобы максимально увеличить число требуются однокубитные повороты, а также сокращение ошибок моделирования.</span><span class="sxs-lookup"><span data-stu-id="84e1c-137">Importantly, this implementation applies some optimizations discussed in [Simulation of Electronic Structure Hamiltonians Using Quantum Computers](https://arxiv.org/abs/1001.3855) and [Improving Quantum Algorithms for Quantum Chemistry](https://arxiv.org/abs/1403.1539) to minimize the number of single-qubit rotations required, as well as reduce simulation errors.</span></span>

## <a name="qubitization"></a><span data-ttu-id="84e1c-138">кубитизатион</span><span class="sxs-lookup"><span data-stu-id="84e1c-138">Qubitization</span></span>

<span data-ttu-id="84e1c-139">Кубитизатион — это альтернативный подход к моделированию, в котором для имитации тактовой корректировки используются идеи из примеров тактов.</span><span class="sxs-lookup"><span data-stu-id="84e1c-139">Qubitization is an alternative approach to simulation that uses ideas from quantum walks to simulate quantum dynamics.</span></span>
<span data-ttu-id="84e1c-140">Хотя для кубитизатион требуется больше Кубитс, чем Троттер формул, метод обещает оптимальное масштабирование с учетом времени развития и допустимости ошибок.</span><span class="sxs-lookup"><span data-stu-id="84e1c-140">While qubitization requires more qubits than Trotter formulas, the method promises optimal scaling with the evolution time and the error tolerance.</span></span>
<span data-ttu-id="84e1c-141">По этим причинам он стал предпочтительным методом для имитации Хамилтониан Dynamics в целом, а также для решения проблемы с электронной структурой в частности.</span><span class="sxs-lookup"><span data-stu-id="84e1c-141">For these reasons it has become a favored method for simulating Hamiltonian dynamics in general, and for solving the electronic structure problem in particular.</span></span>

<span data-ttu-id="84e1c-142">На высоком уровне кубитизатион выполняет эту задачу, выполнив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="84e1c-142">At a high level, qubitization accomplishes this through the following steps.</span></span>
<span data-ttu-id="84e1c-143">Сначала позвольте $H = \sum_j h_j H_j $ для единой и Хермитиан $H _j $ и $h _j \ GE $0.</span><span class="sxs-lookup"><span data-stu-id="84e1c-143">First, let $H=\sum_j h_j H_j$ for unitary and Hermitian $H_j$ and $h_j\ge 0$.</span></span>
<span data-ttu-id="84e1c-144">Выполняя пару отражений, кубитизатион реализует оператор, эквивалентный $ $W = e ^ {\пм i \кос ^{-1}(H/| h | _1)}, $ $ где $ | h | _1 = \sum_j | h_j | $.</span><span class="sxs-lookup"><span data-stu-id="84e1c-144">By performing a pair of reflections, qubitization implements an operator that is equivalent to $$W=e^{\pm i \cos^{-1}(H/|h|_1)},$$ where $|h|_1 = \sum_j |h_j|$.</span></span>
<span data-ttu-id="84e1c-145">Следующий шаг включает преобразование еиженвалуес оператора обхода из $e ^ {и\пм \кос ^{-1}(E_k/| h | _1)} $, где $E _k $ — это еиженвалуес $H $ в $e ^ {-iE_k t} $.</span><span class="sxs-lookup"><span data-stu-id="84e1c-145">The next step involves transforming the eigenvalues of the walk operator from $e^{i\pm \cos^{-1}(E_k/|h|_1)}$, where $E_k$ are the eigenvalues of $H$ to $e^{-iE_k t}$.</span></span>
<span data-ttu-id="84e1c-146">Это можно сделать с помощью различных методов преобразования значений в единственном значении такта, включая [обработку тактовых сигналов](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.118.010501).</span><span class="sxs-lookup"><span data-stu-id="84e1c-146">This can be achieved using a variety of quantum singular value transformation methods including [quantum signal processing](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.118.010501).</span></span>

<span data-ttu-id="84e1c-147">Кроме того, если требуется только статическое количество (например, энергия состояния заземления Хамилтониан), то вполне достаточно применить [оценку этапа](xref:microsoft.quantum.libraries.characterization) непосредственно к $W $, чтобы оценить энергопотребление от результата, выполнив косинус результата.</span><span class="sxs-lookup"><span data-stu-id="84e1c-147">Alternatively, if only static quantities are desired (such as the ground state energy of the Hamiltonian) then it suffices to apply [phase estimation](xref:microsoft.quantum.libraries.characterization) directly to $W$ to estimate the ground state energy from the result by taking the cosine of the result.</span></span>
<span data-ttu-id="84e1c-148">Это важно, так как позволяет сделать преобразование Спектрал классическим, а не использовать метод преобразования значения в единственном значении в такте.</span><span class="sxs-lookup"><span data-stu-id="84e1c-148">This is significant because it allows the spectral transformation to be performed classically rather than using a quantum singular value transformation method.</span></span>

<span data-ttu-id="84e1c-149">На более подробном уровне для реализации кубитизатион требуется две подпрограммы, предоставляющие интерфейсы для Хамилтониан.</span><span class="sxs-lookup"><span data-stu-id="84e1c-149">On a more detailed level, the implementation of qubitization requires two subroutines that provide the interfaces for the Hamiltonian.</span></span>
<span data-ttu-id="84e1c-150">В отличие от методов Троттер – Сузуки эти подпрограммы являются тактовыми, а их реализация требует использования пропорциональны логарифму больше Кубитс, чем потребуется для моделирования на основе Троттер.</span><span class="sxs-lookup"><span data-stu-id="84e1c-150">Unlike Trotter–Suzuki methods, these subroutines are quantum not classical and their implementation will necessitate using logarithmically more qubits than would be required for a Trotter-based simulation.</span></span>

<span data-ttu-id="84e1c-151">Первая подпрограммы такта, используемая кубитизатион, называется $ \Операторнаме{Селект} $, и предполагается возвращать \бегин{екуатион} \Операторнаме{Селект} \кет{ж} \ket{\psi} = \ket{j} H_j \ket{\psi}, \end{Equation}, где каждый $H _j $ считается Hermitian и единая.</span><span class="sxs-lookup"><span data-stu-id="84e1c-151">The first quantum subroutine that qubitization uses is called $\operatorname{Select}$ and it is promised to yield \begin{equation} \operatorname{Select} \ket{j} \ket{\psi} = \ket{j} H_j \ket{\psi}, \end{equation} where each $H_j$ is assumed to be Hermitian and unitary.</span></span>
<span data-ttu-id="84e1c-152">Хотя это может показаться неограниченным, помните, что операторы Паули являются Хермитиан и едиными, поэтому приложения, такие как имитация химия, естественным образом попадают в эту инфраструктуру.</span><span class="sxs-lookup"><span data-stu-id="84e1c-152">While this may seem to be restrictive, recall that Pauli operators are Hermitian and unitary and so applications like quantum chemistry simulation naturally fall into this framework.</span></span>
<span data-ttu-id="84e1c-153">Операция $ \Операторнаме{Селект} $, возможно, удивительно, является на самом деле операцией отражения.</span><span class="sxs-lookup"><span data-stu-id="84e1c-153">The $\operatorname{Select}$ operation, perhaps surprisingly, is actually a reflection operation.</span></span>
<span data-ttu-id="84e1c-154">Это видно из того факта, что $ \Операторнаме{Селект} ^ 2 \ Сисакет {j} \кет{\пси} = \кет{ж} \кет{\пси} $, так как каждый $H _j $ является единым и Хермитиан и, таким же, имеет еиженвалуес $ \пм $1.</span><span class="sxs-lookup"><span data-stu-id="84e1c-154">This can be seen from the fact that $\operatorname{Select}^2\ket{j} \ket{\psi} = \ket{j} \ket{\psi}$ since each $H_j$ is unitary and Hermitian and thus has eigenvalues $\pm 1$.</span></span>

<span data-ttu-id="84e1c-155">Вторая подпрограммы называется $ \Операторнаме{ПРЕПАРЕ} $.</span><span class="sxs-lookup"><span data-stu-id="84e1c-155">The second subroutine is called $\operatorname{Prepare}$.</span></span>
<span data-ttu-id="84e1c-156">Хотя операция SELECT предоставляет средства для согласованного доступа к каждому из Хамилтониан условий $H _j $, подподпрограмма Prepare предоставляет метод для доступа к коэффициентам $h _j $, \бегин{екуатион} \Операторнаме{ПРЕПАРЕ}\кет{0} = \sum_j \sqrt{\frac{h_j}{ | h | _1}} \кет{ж}.</span><span class="sxs-lookup"><span data-stu-id="84e1c-156">While the select operation provides a means to coherently access each of the Hamiltonian terms $H_j$ the prepare subroutine gives a method for accessing the coefficients $h_j$, \begin{equation} \operatorname{Prepare}\ket{0} = \sum_j \sqrt{\frac{h_j}{|h|_1}}\ket{j}.</span></span>
<span data-ttu-id="84e1c-157">\енд{екуатион} затем, используя шлюз фаз с умножением, мы видим, что $ $ \Ламбда\кет{0}^ {\отимес n} = \бегин{Касес} \-\кет{КС} & \текст{ИФ} x = 0 </span><span class="sxs-lookup"><span data-stu-id="84e1c-157">\end{equation} Then, by using a multiply controlled phase gate, we see that $$ \Lambda\ket{0}^{\otimes n} = \begin{cases} \-\ket{x} & \text{if } x = 0 </span></span>\\\
        <span data-ttu-id="84e1c-158">\кет{КС} & \текст{осервисе} \енд{Касес}.</span><span class="sxs-lookup"><span data-stu-id="84e1c-158">\ket{x}   & \text{otherwise} \end{cases}.</span></span>
$$

<span data-ttu-id="84e1c-159">Операция $ \Операторнаме{ПРЕПАРЕ} $ не используется непосредственно в кубитизатион, а используется для реализации отражения состояния, которое $ \Операторнаме{ПРЕПАРЕ} $ создает $ $ \бегин{алигн} R &amp; = 1-2 \ операторнаме {Prepare} \ket{0}\bra @no_ _t_2_ \Операторнаме{ПРЕПАРЕ} ^{-1} \\\\ &amp; = \Операторнаме{ПРЕПАРЕ} \Ламбда \Операторнаме{ПРЕПАРЕ} ^{-1}.</span><span class="sxs-lookup"><span data-stu-id="84e1c-159">The $\operatorname{Prepare}$ operation is not used directly in qubitization, but rather is used to implement a reflection about the state that $\operatorname{Prepare}$ creates $$ \begin{align} R &amp; = 1 - 2\operatorname{Prepare} \ket{0}\bra{0} \operatorname{Prepare}^{-1} \\\\ &amp; = \operatorname{Prepare} \Lambda \operatorname{Prepare}^{-1}.</span></span>
<span data-ttu-id="84e1c-160">\енд{алигн} $ $</span><span class="sxs-lookup"><span data-stu-id="84e1c-160">\end{align} $$</span></span>

<span data-ttu-id="84e1c-161">Оператор обхода, $W $, может быть выражен в терминах $ $ \Операторнаме{Селект} $ и $R $ в виде $ $ W = \Операторнаме{Селект} R, $ $, который опять можно увидеть для реализации оператора, эквивалентного (до исометри), для $e ^ {\пм i \кос ^{-1}(H/| H | _1)} $.</span><span class="sxs-lookup"><span data-stu-id="84e1c-161">The walk operator, $W$, can be expressed in terms of the $\operatorname{Select}$ and $R$ operations as $$ W = \operatorname{Select} R, $$ which again can be seen to implement an operator that is equivalent (up to an isometry) to $e^{\pm i \cos^{-1}(H/|h|_1)}$.</span></span>

<span data-ttu-id="84e1c-162">Эти подпрограммы легко настроить в Q #.</span><span class="sxs-lookup"><span data-stu-id="84e1c-162">These subroutines are easy to set up in Q#.</span></span>
<span data-ttu-id="84e1c-163">В качестве примера рассмотрим простой кубит с поворотом Исинг Хамилтониан, где $H = X_1 + X_2 + Z_1 Z_2 $.</span><span class="sxs-lookup"><span data-stu-id="84e1c-163">As an example, consider the simple qubit transverse-Ising Hamiltonian where $H = X_1 + X_2 + Z_1 Z_2$.</span></span>
<span data-ttu-id="84e1c-164">В этом случае код Q #, который мог бы реализовать операцию $ \Операторнаме{Селект} $, вызывается <xref:microsoft.quantum.canon.multiplexoperations>, тогда как операция $ \Операторнаме{ПРЕПАРЕ} $ может быть реализована с помощью <xref:microsoft.quantum.preparation.preparearbitrarystate>.</span><span class="sxs-lookup"><span data-stu-id="84e1c-164">In this case, Q# code that would implement the $\operatorname{Select}$ operation is invoked by <xref:microsoft.quantum.canon.multiplexoperations>, whereas the $\operatorname{Prepare}$ operation can be implemented using <xref:microsoft.quantum.preparation.preparearbitrarystate>.</span></span>
<span data-ttu-id="84e1c-165">Пример, включающий моделирование модели Хуббард, можно найти в виде [образца Q #](https://github.com/Microsoft/Quantum/tree/master/Samples/src/HubbardSimulation).</span><span class="sxs-lookup"><span data-stu-id="84e1c-165">An example that involves simulating the Hubbard model can be found as a [Q# sample](https://github.com/Microsoft/Quantum/tree/master/Samples/src/HubbardSimulation).</span></span>

<span data-ttu-id="84e1c-166">Чтобы вручную указать эти шаги для произвольных проблем химия, потребуется много усилий, что позволит избежать использования библиотеки химия.</span><span class="sxs-lookup"><span data-stu-id="84e1c-166">Manually specifying these steps for arbitrary chemistry problems would require much effort, which is avoided using the chemistry library.</span></span>
<span data-ttu-id="84e1c-167">Аналогично алгоритму моделирования Троттер – Сузуки, приведенному выше, `JordanWignerEncodingData` передается в удобную функцию `QubitizationOracle`, возвращающую оператор обхода, в дополнение к другим параметрам, необходимым для его выполнения.</span><span class="sxs-lookup"><span data-stu-id="84e1c-167">Similarly to the Trotter–Suzuki simulation algorithm above, the `JordanWignerEncodingData` is passed to the convenience function `QubitizationOracle` that returns the walk-operator, in addition to other parameters required for its execution.</span></span>

```qsharp
// qSharpData passed from driver
let qSharpData = ... 

// `oracle` is an operation that applies a single time-step of evolution for duration `stepSize`.
// `rescale` is just `1.0/oneNorm`, where oneNorm is the sum of absolute values of all probabilities in state prepared by `Prepare`.
// `nQubits` is the number of qubits that must be allocated to run the `oracle` operatrion.
let (nQubits, (rescale, oracle)) =  QubitizationOracle (qSharpData, stepSize, integratorOrder);

// Let us now apply a single step of the quantum walk.
using(qubits = Qubit[nQubits]){

    // Apply single step of quantum walk.
    oracle(qubits);

    // Reset all qubits to the 0 state to be successfully released.
    ResetAll(qubits);
}
```

<span data-ttu-id="84e1c-168">Что важнее, <xref:microsoft.quantum.chemistry.jordanwigner.qubitizationoracle> реализации применима к произвольным Хамилтонианс, указанным в виде линейного сочетания строк Паули.</span><span class="sxs-lookup"><span data-stu-id="84e1c-168">Importantly, the implementation <xref:microsoft.quantum.chemistry.jordanwigner.qubitizationoracle> is applicable to arbitrary Hamiltonians specified as a linear combination of Pauli strings.</span></span>
<span data-ttu-id="84e1c-169">Версия, оптимизированная для имитации химия, вызывается с помощью <xref:microsoft.quantum.chemistry.jordanwigner.optimizedqubitizationoracle>.</span><span class="sxs-lookup"><span data-stu-id="84e1c-169">A version optimized for chemistry simulations is invoked using <xref:microsoft.quantum.chemistry.jordanwigner.optimizedqubitizationoracle>.</span></span>
<span data-ttu-id="84e1c-170">Эта версия оптимизирована для минимального числа T-шлюзов с помощью методик, описанных в разделе [кодирование электронных спектра в тактовых каналах с помощью линейной T-сложности](https://arxiv.org/abs/1805.03662).</span><span class="sxs-lookup"><span data-stu-id="84e1c-170">This version is optimized to minimize the number of T gates using techniques discussed in [Encoding Electronic Spectra in Quantum Circuits with Linear T Complexity](https://arxiv.org/abs/1805.03662).</span></span>
