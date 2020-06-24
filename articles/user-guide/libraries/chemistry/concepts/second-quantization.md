---
title: Второй дискретизация
description: Узнайте о втором дискретизация подходе к моделированию электронных структур в процессе программирования.
author: nathanwiebe2
ms.author: nawiebe@microsoft.com
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.secondquantization
ms.openlocfilehash: e17c97767b05395af46a82c4035337406c7e3218
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2020
ms.locfileid: "85276110"
---
# <a name="second-quantization"></a><span data-ttu-id="afc11-103">Второй дискретизация</span><span class="sxs-lookup"><span data-stu-id="afc11-103">Second Quantization</span></span>

<span data-ttu-id="afc11-104">Вторая дискретизация просматривает проблему с электронной структурой с помощью другой линзы.</span><span class="sxs-lookup"><span data-stu-id="afc11-104">Second quantization looks at the problem of electronic structure through a different lens.</span></span>
<span data-ttu-id="afc11-105">Вместо того, чтобы назначать каждому $N _e $ электронному состоянию (или Орбитал), второй дискретизация отслеживает каждый Орбитал и сохраняет, есть ли электроны в каждом из них, и в то же время автоматически гарантирует свойства симметрии соответствующей функции Wave.</span><span class="sxs-lookup"><span data-stu-id="afc11-105">Rather than assigning each of the $N_e$ electrons to a specific state (or orbital), second quantization tracks each orbital and stores whether there is an electron present in each of them and at the same time automatically ensures symmetry properties of the corresponding wave function.</span></span>
<span data-ttu-id="afc11-106">Это важно, так как позволяет задавать химияные модели, не беспокоясь о том, что симметризинг входное состояние (как это требуется для фермионс), а также потому, что вторая дискретизация позволяет имитировать такие модели с помощью небольших тактовых компьютеров.</span><span class="sxs-lookup"><span data-stu-id="afc11-106">This is important because it allows quantum chemistry models to be specified without having to worry about anti-symmetrizing the input state (as is required for fermions) and also because second quantization allows such models to be simulated using small quantum computers.</span></span>

<span data-ttu-id="afc11-107">В качестве примера второго дискретизация в действии Предположим, что $ \ psi_0 \кдотс \ psi_ {N-1} $ являются орсонормал набором пространственных орбит.</span><span class="sxs-lookup"><span data-stu-id="afc11-107">As an example of second quantization in action, let's assume that $\psi_0\cdots \psi_{N-1}$ are an orthonormal set of spatial orbitals.</span></span>
<span data-ttu-id="afc11-108">Эти орбиты выбираются для представления системы как можно точнее в рамках рассматриваемого базового набора.</span><span class="sxs-lookup"><span data-stu-id="afc11-108">These orbitals are chosen to represent the system as accurately as possible within the finite basis set considered.</span></span>
<span data-ttu-id="afc11-109">Распространенный пример таких орбит — атомарные орбиты, которые формируют еиженбасис для атома водорода.</span><span class="sxs-lookup"><span data-stu-id="afc11-109">A common example of such orbitals are atomic orbitals which form an eigenbasis for the hydrogen atom.</span></span>
<span data-ttu-id="afc11-110">Так как электроны имеют два оборота, два электрона могут быть краммед на каждый такой пространственный Орбитал.</span><span class="sxs-lookup"><span data-stu-id="afc11-110">Because electrons have two spin states, two electrons can be crammed into each such spatial orbital.</span></span>
<span data-ttu-id="afc11-111">Например, допустимыми являются следующие состояния: $ \ psi_ {0, \упарров}, \лдотс, \ psi_ {N-1, \упарров}, \ psi_ {0, \довнарров}, \лдотс, \ psi_ {N-1, \довнарров} $ WHERE $ \упарров $ и $ \довнарров $ являются метками, которые задают две еиженстатес степени свободы.</span><span class="sxs-lookup"><span data-stu-id="afc11-111">That is to say, the valid basis states are of the form $\psi_{0,\uparrow},\ldots,\psi_{N-1,\uparrow}, \psi_{0,\downarrow},\ldots,\psi_{N-1,\downarrow}$ where $\uparrow$ and $\downarrow$ are labels that specify the two eigenstates of the spin degree of freedom.</span></span>
<span data-ttu-id="afc11-112">Этот комбинированный индекс $ (j, \сигма) $ для $ \сигма \ин \{ \упарров, \довнарров \} $ называется Spin-Орбитал, так как он хранит как пространственный, так и степень свободы.</span><span class="sxs-lookup"><span data-stu-id="afc11-112">This combined index of $(j,\sigma)$ for $\sigma \in \{\uparrow,\downarrow\}$ is called a spin-orbital because it stores both the spatial as well as the spin degree of freedom.</span></span>
<span data-ttu-id="afc11-113">В библиотеке химия объект Spin-орбиты хранится в `SpinOrbital` структуре данных и создается следующим образом.</span><span class="sxs-lookup"><span data-stu-id="afc11-113">In the chemistry library, spin-orbitals are stored in a `SpinOrbital` data structure, and are created as follows.</span></span>

```csharp
    // First, we load the namespace containing spin-orbital objects.
    using Microsoft.Quantum.Chemistry.OrbitalIntegrals;

    // First, we assign an orbital index, say `5`. Note that we use 0-indexing,
    // so this is the 6th orbital.
    var orbitalIdx = 5;

    // Second, we assign a spin index, say `Spin.u` for spin up or `Spin.d` for spin down.
    var spin = Spin.d;

    // the spin-orbital (5, ↓) is then
    var spinOrbital = new SpinOrbital(orbitalIdx, spin);

    // A tuple `(int, Spin)` is also implicitly recognized as a spin-orbital.
    (int, Spin) tuple = (orbitalIdx, spin);

    // We explicitly specify the type of `spinOrbital1` to demonstrate
    // the implicit cast to `SpinOrbital`.
    SpinOrbital spinOrbital1 = tuple;
```

<span data-ttu-id="afc11-114">Это означает, что мы можем формально представить базу для прокрутки и пространственной части функции Wave как $ \ psi_ {0} \кдотс \ psi_ {2n-1} $, где каждый из индексов теперь является перечислением $ (j, \сигма) $.</span><span class="sxs-lookup"><span data-stu-id="afc11-114">This means that we can formally think of the basis for both the spin and spatial part of the wave function as $\psi_{0} \cdots \psi_{2N-1}$ where each of the indices now is an enumeration of a $(j,\sigma)$.</span></span>
<span data-ttu-id="afc11-115">Одно возможное перечисление — $g (j, \сигма) = j + Н\сигма ' $.</span><span class="sxs-lookup"><span data-stu-id="afc11-115">One possible enumeration is $g(j,\sigma) = j+N\sigma'$.</span></span>
<span data-ttu-id="afc11-116">Другое возможное перечисление — $h (j, \сигма) = 2 \* j + \сигма $.</span><span class="sxs-lookup"><span data-stu-id="afc11-116">Another possible enumeration is $h(j,\sigma) = 2\*j + \sigma$.</span></span>
<span data-ttu-id="afc11-117">В библиотеке тактов химия можно использовать эти соглашения, а при создании экземпляра этой кодировки можно создать экземпляр с вращением, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="afc11-117">The quantum chemistry library can use these conventions, and the spin-orbitals in such an encoding can be instantiated as follows.</span></span>

```csharp
    // Let us use the spin orbital created in the previous snippet.
   var spinOrbital = new SpinOrbital(5, Spin.d);

   // Let us set the total number of orbitals to be say, `7`.
   var nOrbitals = 7;

    // This converts a spin-orbital index to a unique integer, in this case `12`,
    // using the formula `g(j,σ)`.
    var integerIndexHalfUp = spinOrbital.ToInt(IndexConvention.HalfUp);

    // This converts a spin-orbital index to a unique integer, in this case `11`,
    // using the formula `h(j,σ)`.
    var integerIndexUpDown = spinOrbital.ToInt(IndexConvention.UpDown);

    // The default conversion uses the formula `h(j,σ)`, in this case `11`.
    var integerIndexDefault = spinOrbital.ToInt();
```

<span data-ttu-id="afc11-118">Для систем фермионик принцип исключения Паули предотвращает присутствие более одного электронного представления в каком-Орбитал в то же время.</span><span class="sxs-lookup"><span data-stu-id="afc11-118">For fermionic systems, the Pauli exclusion principle prevents more than one electron from being present in any spin-orbital at the same time.</span></span>
<span data-ttu-id="afc11-119">Это означает, что можно написать два юридических состояния для $ \ psi_1 $ AS \бегин{екуатион} \ psi_1 \ригхтарров \бегин{Касес} \кет {0} _1 & \текст{ИФ $ \ psi_1 $ не занят,}</span><span class="sxs-lookup"><span data-stu-id="afc11-119">This means that we can write the two legal states for $\psi_1$ as \begin{equation} \psi_1 \rightarrow \begin{cases} \ket{0}_1 & \text{if $\psi_1$ is not occupied,} </span></span>\\\
<span data-ttu-id="afc11-120">\кет {1} _1 & \текст{ИФ $ \ psi_1 $ занято.}</span><span class="sxs-lookup"><span data-stu-id="afc11-120">\ket{1}_1 & \text{if $\psi_1$ is occupied.}</span></span> <span data-ttu-id="afc11-121">\енд{Касес} \енд{екуатион} эта кодировка отлично подходит для тактовых компьютеров, так как это означает, что мы можем хранить электронную должность как один тактовый бит.</span><span class="sxs-lookup"><span data-stu-id="afc11-121">\end{cases} \end{equation} This encoding is great for quantum computers because it means that we can store the electronic occupation as a single quantum bit.</span></span>

<span data-ttu-id="afc11-122">Состояния профессий для орбит $2N $ Spin также могут храниться в $2N $ Кубитс.</span><span class="sxs-lookup"><span data-stu-id="afc11-122">The occupation states for the $2N$ spin orbitals can similarly be stored in $2N$ qubits.</span></span>
<span data-ttu-id="afc11-123">Например, если $N = $2, то State $ $ \кет {0} \кет {1} \кет {1} \кет {0} , $ $</span><span class="sxs-lookup"><span data-stu-id="afc11-123">As an example, if $N=2$ then the state $$ \ket{0} \ket{1} \ket{1} \ket{0}, $$</span></span>

<span data-ttu-id="afc11-124">будет соответствовать прокрутки по орбитам $1 $ и $2 $, которые будут свободны с остатком.</span><span class="sxs-lookup"><span data-stu-id="afc11-124">would correspond to spin orbitals $1$ and $2$ being occupied with the remainder empty.</span></span>
<span data-ttu-id="afc11-125">Аналогично, State $ $ \кет {0} \екуив \кет {0} _ {0} \кдотс \кет {0} _{N-1}, $ $</span><span class="sxs-lookup"><span data-stu-id="afc11-125">Similarly, the state $$ \ket{0} \equiv \ket{0}_{0} \cdots \ket{0}_{N-1}, $$</span></span>

<span data-ttu-id="afc11-126">не имеет электронов и называется "состоянием очистки".</span><span class="sxs-lookup"><span data-stu-id="afc11-126">has no electrons and is known as the 'vacuum state'.</span></span>

<span data-ttu-id="afc11-127">Прекрасным побочным эффектом второго дискретизация является то, что больше не нужно явным образом отследить электросимметрию состояния такта.</span><span class="sxs-lookup"><span data-stu-id="afc11-127">A beautiful side-effect of second quantization is that we no longer have to explicitly keep track of the anti-symmetry of the quantum state.</span></span>
<span data-ttu-id="afc11-128">Это связано с тем, что, как мы увидим, неопределенность состояния представляет собой саму себя с помощью коммутатион правил операторов, которые создают и удаляют электронные профессии прокрутки Орбитал.</span><span class="sxs-lookup"><span data-stu-id="afc11-128">This is because, as we will see, the anti-symmetry of the state represents itself instead through the anti-commutation rules of the operators that create and destroy electronic occupations of a spin orbital.</span></span>

## <a name="fermionic-operators"></a><span data-ttu-id="afc11-129">Операторы фермионик</span><span class="sxs-lookup"><span data-stu-id="afc11-129">Fermionic operators</span></span>

<span data-ttu-id="afc11-130">Два фундаментальных оператора, которые действуют на основе второго квантования, называются операторами создания и аннихилатион.</span><span class="sxs-lookup"><span data-stu-id="afc11-130">The two fundamental operators that act on the second-quantized basis vectors are known as creation and annihilation operators.</span></span>
<span data-ttu-id="afc11-131">Эти операторы вставляют или удаляют электронную страну в определенном месте.</span><span class="sxs-lookup"><span data-stu-id="afc11-131">These operators insert or destroy electrons at a particular location.</span></span>
<span data-ttu-id="afc11-132">Они обозначаются $a ^ \ dagger_j $ и $a _j $ соответственно.</span><span class="sxs-lookup"><span data-stu-id="afc11-132">These are denoted $a^\dagger_j$ and $a_j$ respectively.</span></span>

<span data-ttu-id="afc11-133">Например, \бегин{алигн} a ^ \ dagger_1 \кет {0} _1 = \кет {1} _1, \куад a ^ \ dagger_1 \кет {1} _1 = 0, \куад A_1 \кет {0} _1 = 0, \куад A_1 \кет {1} _1 = \кет {0} _1.</span><span class="sxs-lookup"><span data-stu-id="afc11-133">For example, \begin{align} a^\dagger_1 \ket{0}_1 = \ket{1}_1,\quad a^\dagger_1 \ket{1}_1 = 0,\quad a_1 \ket{0}_1 = 0,\quad a_1 \ket{1}_1 = \ket{0}_1.</span></span>
<span data-ttu-id="afc11-134">\енд{алигн} Обратите внимание, что здесь $a ^ \ dagger_1 \кет {1} _1 = 0 $ and $a _1 \кет {0} _1 $ дает нулевой вектор, отличный от $ \кет {0} _1 $.</span><span class="sxs-lookup"><span data-stu-id="afc11-134">\end{align} Note that here $a^\dagger_1 \ket{1}_1=0$ and $a_1 \ket{0}_1$ yield the zero-vector not $\ket{0}_1$.</span></span>
<span data-ttu-id="afc11-135">Поэтому такие операторы не являются ни Хермитиан, ни единым.</span><span class="sxs-lookup"><span data-stu-id="afc11-135">Such operators are therefore neither Hermitian nor unitary.</span></span>
<span data-ttu-id="afc11-136">Мы представляем общие операторы создания и аннихилатион, использующие <xref:Microsoft.Quantum.Chemistry.LadderOperators.LadderOperator`1> тип.</span><span class="sxs-lookup"><span data-stu-id="afc11-136">We represent general creation and annihilation operators using the <xref:Microsoft.Quantum.Chemistry.LadderOperators.LadderOperator`1> type.</span></span>
<span data-ttu-id="afc11-137">Например, один оператор создания представлен ниже.</span><span class="sxs-lookup"><span data-stu-id="afc11-137">For instance, a single creation operator is represented as follow.</span></span>

```csharp
    // We load the namespace containing ladder operator objects.
    using Microsoft.Quantum.Chemistry.LadderOperators;

    // Let us use the spin orbital created in the previous snippet.
    var spinOrbitalInteger = new SpinOrbital(5, Spin.d).ToInt();

    // We specify either a creation or annihilation operator using 
    // the enumerable type `RaisingLowering.u` or `RaisingLowering.d`
    // respectively;
    var creationEnum = RaisingLowering.u;

    // The type representing a creation operator is then initialized 
    // as follows. Here, we index these operators with integers.
    // Hence we initialize the generic ladder operator with an
    // integer index type.
    var ladderOperator0 = new LadderOperator<int>(creationEnum, spinOrbitalInteger);

    // An alternate constructor for a LadderOperator instead uses
    // a tuple.
    var ladderOperator1 = new LadderOperator<int>((creationEnum, spinOrbitalInteger));
```

<span data-ttu-id="afc11-138">Кроме того, с помощью таких операторов можно выразить $ $ \кет {0} \кет {1} \кет {1} \кет {0} = a ^ \ dagger_1 a ^ \ dagger_2 \кет {0} ^ {\отимес 4}.</span><span class="sxs-lookup"><span data-stu-id="afc11-138">Also using such operators we can express $$ \ket{0} \ket{1} \ket{1} \ket{0} = a^\dagger_1 a^\dagger_2 \ket{0}^{\otimes 4}.</span></span>
<span data-ttu-id="afc11-139">$ $ Эта последовательность операторов будет построена в библиотеке моделирования Хамилтониан с помощью кода C#, подобного орбиталу, рассмотренному выше:</span><span class="sxs-lookup"><span data-stu-id="afc11-139">$$ This sequence of operators would be constructed within the Hamiltonian simulation library using C# code that is similar to the single-spin orbital case considered above above:</span></span>
```csharp
    // We load the namespace containing fermion-related objects.
    using Microsoft.Quantum.Chemistry.Fermion;

    // Let us initialize an array of tuples representing the
    // desired sequence of creation operators.
    var indices = new[] { (RaisingLowering.u, 1), (RaisingLowering.u, 2) };

    // We can convert this array of tuples to a sequence of ladder
    // operators using the `ToLadderSequence()` methods.
    var ladderSequences = indices.ToLadderSequence();

    // Sequences of ladder operators are quite general. For instance,
    // they could be bosonic operators, instead of fermionic operators.
    // We specialize them by constructing a `FermionTerm` representing 
    // a fermion creation operator on the index `2` followed by `1`.
    var fermionTerm = new FermionTerm(ladderSequences);
```

<span data-ttu-id="afc11-140">Для системы $k $ Фермионс в секунду дискретизация действия оператора создания $a ^ \ dagger_i $ задается в $ $ a ^ \ dagger_i \кет{n_1, n_2, \лдотс, 0_i, \лдотс, n_k} = (-1) ^ {S_i} \кет{n_1, n_2, \лдотс, 1_i, \лдотс, n_k}, $ $ и $ $ a ^ \ dagger_i \кет{n_1, n_2, \лдотс, 1_i, \лдотс, n_k} = 0, $ $, где $S _i = \ sum_ {j<i} a ^ \ dagger_j a_j $ измеряет общее число Фермионс, которые находятся в состоянии одной частицы и имеют индекс $j < i $.</span><span class="sxs-lookup"><span data-stu-id="afc11-140">For a system of $k$ Fermions, in second quantization the action of the creation operator $a^\dagger_i$ is given by $$ a^\dagger_i \ket{n_1, n_2, \ldots, 0_i, \ldots, n_k } = (-1)^{S_i} \ket{n_1, n_2, \ldots, 1_i, \ldots, n_k}, $$ and $$ a^\dagger_i \ket{n_1, n_2, \ldots, 1_i, \ldots, n_k } = 0, $$ where $S_i = \sum_{j<i} a^\dagger_j a_j$ measures the total number of Fermions that are in the state of a single particle and that have an index $j < i$.</span></span>

<span data-ttu-id="afc11-141">Третий оператор также часто используется во втором представлении квантования.</span><span class="sxs-lookup"><span data-stu-id="afc11-141">A third operator is also often used in second quantized representations.</span></span>
<span data-ttu-id="afc11-142">Этот оператор известен как оператор Number и определяется \бегин{екуатион} n_i = a ^ \ dagger_i a_i.</span><span class="sxs-lookup"><span data-stu-id="afc11-142">This operator is known as the number operator and is defined by \begin{equation} n_i = a^\dagger_i a_i.</span></span>
<span data-ttu-id="afc11-143">\енд{екуатион}. Этот оператор подсчитывает роду данного цикла Орбитал, который означает \бегин{алигн} n_i \кет {0} _i &= 0 \ нечисловое значение</span><span class="sxs-lookup"><span data-stu-id="afc11-143">\end{equation} This operator counts the occupation of a given spin orbital, which is to say \begin{align} n_i \ket{0}_i &= 0\nonumber</span></span>\\\
<span data-ttu-id="afc11-144">n_i \кет {1} _i &= \кет {1} _i.</span><span class="sxs-lookup"><span data-stu-id="afc11-144">n_i \ket{1}_i &= \ket{1}_i.</span></span>
<span data-ttu-id="afc11-145">\енд{алигн}, как и в приведенных выше `FermionTerm` примерах, этот оператор Number создается следующим образом.</span><span class="sxs-lookup"><span data-stu-id="afc11-145">\end{align} Similar to the above `FermionTerm` examples, this number operator is constructed as follows.</span></span>
```csharp
    // Let us use a new method to compactly create a sequence of ladder
    // operators. Note that we have omitted specifying whether the 
    // operators are raising or lowering. In this case, the first half
    // will be raising operators, and the second half will be lowering 
    // operators.
    var indices = new[] { 1, 1 }.ToLadderSequence();

    // We now construct a `FermionTerm` representing an annihilation operator
    // on the index 1 followed by the creation operator on the index 1.
    var fermionTerm0 = new FermionTerm(indices);
```

<span data-ttu-id="afc11-146">Однако при использовании операторов создания или аннихилатион в системах фермионик возникают тонкости.</span><span class="sxs-lookup"><span data-stu-id="afc11-146">A subtlety emerges though when using creation or annihilation operators in fermionic systems.</span></span>
<span data-ttu-id="afc11-147">Для обмена метками требуется, чтобы любое допустимое состояние такта было несимметричным.</span><span class="sxs-lookup"><span data-stu-id="afc11-147">We require that any valid quantum state is anti-symmetric under exchange of labels.</span></span>
<span data-ttu-id="afc11-148">Это означает, что $ $ a ^ \ dagger_2 а ^ \ dagger_1 \кет {0} =-a ^ \ dagger_1 a ^ \ dagger_2 \кет {0} .</span><span class="sxs-lookup"><span data-stu-id="afc11-148">This means that $$ a^\dagger_2 a^\dagger_1 \ket{0} = -a^\dagger_1 a^\dagger_2 \ket{0}.</span></span>
<span data-ttu-id="afc11-149">$ $ Такие операторы называются «незащищенными» и в целом для любых $i j $ мы добавили, что \бегин{алигн} ^ \ dagger_i a ^ \ dagger_j =-(1 – \ delta_ {i, j}) а ^ \ dagger_j a ^ \ dagger_i, \куад а ^ \ dagger_i a_j = \ delta_ {i, j} — a_j a ^ \ dagger_i.</span><span class="sxs-lookup"><span data-stu-id="afc11-149">$$ Such operators are said to 'anti-commute' and in general for any $i, j$ we have that \begin{align} a^\dagger_i a^\dagger_j  = -(1-\delta_{i,j})a^\dagger_j a^\dagger_i,\quad a^\dagger_i a_j =\delta_{i,j} - a_j a^\dagger_i.</span></span>
<span data-ttu-id="afc11-150">\енд{алигн}, что следующие два <xref:Microsoft.Quantum.Chemistry.LadderOperators.LadderSequence`1> экземпляра считаются неэквивалентными</span><span class="sxs-lookup"><span data-stu-id="afc11-150">\end{align} Thus the following two <xref:Microsoft.Quantum.Chemistry.LadderOperators.LadderSequence`1> instances are considered inequivalent</span></span>
```csharp
    // Let us initialize an array of tuples representing the
    // desired sequence of creation operators.
    var indices = new[] { (RaisingLowering.u, 1), (RaisingLowering.u, 2) };

    // We now construct a `LadderSequence` representing a creation operator
    // on the index 1 followed by 2, then a term with the reverse ordering.
    var laddderSeqeunce = indices.ToLadderSequence();
    var laddderSeqeunceReversed = indices.Reverse().ToLadderSequence();

    // The following Boolean is `false`.
    var equal = laddderSeqeunce == laddderSeqeunceReversed;
```

<span data-ttu-id="afc11-151">Необходимость в каждом из операторов создания означает, что использование второго квантования представления делает избежать проблемы, с которыми сталкиваются сглаживание Фермионс.</span><span class="sxs-lookup"><span data-stu-id="afc11-151">The requirement that each of the creation operators anti-commute means that using a second quantized representation does obviate the challenges faced by the anti-symmetry of Fermions.</span></span>
<span data-ttu-id="afc11-152">Вместо этого запрос перейдет в определение операторов создания.</span><span class="sxs-lookup"><span data-stu-id="afc11-152">Instead the challenge re-emerges in our definition of the creation operators.</span></span> 

<span data-ttu-id="afc11-153">Используя правила защиты от коммутатион, некоторые `LadderSequence` экземпляры фактически соответствуют одной последовательности операторов фермионик, иногда до знака минус.</span><span class="sxs-lookup"><span data-stu-id="afc11-153">Using the anti-commutation rules, some `LadderSequence` instances actually correspond to the same sequence of fermionic operators, sometimes up to a minus sign.</span></span>
<span data-ttu-id="afc11-154">Например, рассмотрим Хамилтониан $a _0 ^ \дагжер a_1 ^ \дагжер a_1 a_0 =-a_1 ^ \дагжер a_0 ^ \дагжер a_1 a_0 $.</span><span class="sxs-lookup"><span data-stu-id="afc11-154">For instance, consider the Hamiltonian $a_0^\dagger a_1^\dagger a_1 a_0 = - a_1^\dagger a_0^\dagger a_1 a_0$.</span></span>
<span data-ttu-id="afc11-155">Это мотивация, что нам нужно определить каноническую сортировку для каждого из них `FermionTerm` .</span><span class="sxs-lookup"><span data-stu-id="afc11-155">This motivates us to define a canonical ordering for every `FermionTerm`.</span></span>
<span data-ttu-id="afc11-156">Любой `FermionTerm` из них автоматически помещается в канонический порядок, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="afc11-156">Any `FermionTerm` is automatically put into canonical order as follows.</span></span>
```csharp
    // We now construct two `FermionTerms` that are equivalent with respect to
    // anti-commutation up to a sign change.
    var fermionTerm0 = new FermionTerm(new[] { 0, 1, 1, 0 }.ToLadderSequence());
    var fermionTerm1 = new FermionTerm(new[] { 1, 0, 1, 0 }.ToLadderSequence());

    // The following Boolean is `true`.
    var sequenceEqual = fermionTerm0 == fermionTerm1;

    // The change in sign is not compared above, but is an internally tracked
    // property of `FermionTerm`.
    int sign0 = fermionTerm0.Coefficient;
    var sign1 = fermionTerm1.Coefficient;

    // The following Boolean is `false`.
    var signEqual = sign0 == sign1;
```

## <a name="second-quantized-fermionic-hamiltonian"></a><span data-ttu-id="afc11-157">Второй-квантования Фермионик Хамилтониан</span><span class="sxs-lookup"><span data-stu-id="afc11-157">Second-Quantized Fermionic Hamiltonian</span></span>

<span data-ttu-id="afc11-158">Возможно, неудивительно, что Хамилтониан в [тактовых моделях для электронных систем](xref:microsoft.quantum.chemistry.concepts.quantummodels) можно написать с точки зрения операторов создания и аннихилатион.</span><span class="sxs-lookup"><span data-stu-id="afc11-158">It is perhaps unsurprising that the Hamiltonian in [Quantum Models for Electronic Systems](xref:microsoft.quantum.chemistry.concepts.quantummodels) can be written in terms of creation and annihilation operators.</span></span>
<span data-ttu-id="afc11-159">В частности, если $ \пси \_ j $ — это оборотные орбиты, которые формируют базу, то</span><span class="sxs-lookup"><span data-stu-id="afc11-159">In particular, if $\psi\_j$ are the spin orbitals that form the basis then</span></span>

<span data-ttu-id="afc11-160">\бегин{екуатион} \Хат{х} = \сум \_ {PQ} h \_ {PQ} a ^ \дагжер \_ p a \_ q + \фрак {1} {2} \сум \_ {пкрс} h \_ {пкрс} a ^ \дагжер \_ p a ^ \дагжер \_ \_ \_ \_ . \текстрм} NUC, где $h \_ {\лабел{ЕК totalHam} $ — это ядерная энергия (которая является константой в соответствии с аппроксимацией \end{Equation}) и</span><span class="sxs-lookup"><span data-stu-id="afc11-160">\begin{equation} \hat{H} = \sum\_{pq} h\_{pq}a^\dagger\_p a\_q + \frac{1}{2}\sum\_{pqrs} h\_{pqrs}a^\dagger\_p a^\dagger\_q a\_ra\_s +h\_{\textrm nuc},\label{eq:totalHam} \end{equation} where $h\_{\textrm nuc}$ is the nuclear energy (which is a constant under the Born-Oppenheimer approximation) and</span></span>

<span data-ttu-id="afc11-161">\бегин{алигн} h \_ {PQ} &= \инт \_ {-\инфти} ^ \инфти \пси ^ \* \_ p (x \_ 1) \лефт (-\Фрак{\набла ^ 2} {2} + V (x \_ 1) \ригхт) \пси \_ q (x \_ 1) \масрм{д} ^ 3 раза \_ 1, \енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="afc11-161">\begin{align} h\_{pq} &= \int\_{-\infty}^\infty \psi^\*\_p(x\_1) \left(-\frac{\nabla^2}{2} +V(x\_1)\right)  \psi\_q(x\_1)\mathrm{d}^3x\_1, \end{align}</span></span>

<span data-ttu-id="afc11-162">где $V (x) $ является потенциалом среднего поля и</span><span class="sxs-lookup"><span data-stu-id="afc11-162">where $V(x)$ is the mean-field potential, and</span></span>

<span data-ttu-id="afc11-163">\бегин{алигн} h \_ {пкрс} &= \инт \_ {-\инфти} ^ \инфти \инт \_ {-\инфти} ^ \инфти\пси \_ p ^ \* (x \_ 1) \пси \_ q ^ \* (x \_ 2) \лефт (\фрак {1} {| x_1-x_2 |} \ригхт) \psi \_ r (x \_ 2) \psi \_ s (x \_ 1) \mathrm{d} ^ 3 раза \_ 1 \ mathrm {d} ^ 3 раза \_ 2. \ Label {EQ: интегралы} \end{align}</span><span class="sxs-lookup"><span data-stu-id="afc11-163">\begin{align} h\_{pqrs} &= \int\_{-\infty}^\infty \int\_{-\infty}^\infty\psi\_p^\*(x\_1)\psi\_q^\*(x\_2) \left(\frac{1}{|x_1-x_2|} \right)\psi\_r(x\_2)\psi\_s(x\_1)\mathrm{d}^3x\_1\mathrm{d}^3x\_2.\label{eq:integrals} \end{align}</span></span>

<span data-ttu-id="afc11-164">Термины $h \_ {PQ} $ называются одноэлектронными интегралами, так как все эти термины содержат только отдельные электроны и точно так же $h \_ {пкрс} $ — это два электронных интеграла.</span><span class="sxs-lookup"><span data-stu-id="afc11-164">The terms $h\_{pq}$ are referred to as one-electron integrals because all such terms only involve single electrons and likewise $h\_{pqrs}$ are the two-electron integrals.</span></span>
<span data-ttu-id="afc11-165">Они называются интегралами, так как вычисление значений этих коэффициентов требует целого.</span><span class="sxs-lookup"><span data-stu-id="afc11-165">They are called integrals because computing the values of these coefficients requires an integral.</span></span>
<span data-ttu-id="afc11-166">В одном электронном соглашении описываются Кинетик энергия отдельных электронов и их взаимодействие с электрическими полями нуклеи.</span><span class="sxs-lookup"><span data-stu-id="afc11-166">The one electron terms describe the kinetic energy of the individual electrons and their interactions with the electric fields of the nuclei.</span></span>
<span data-ttu-id="afc11-167">Два электронных интеграла с другой стороны описывают взаимодействие между электронными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="afc11-167">The two-electron integrals on the other hand describe the interactions between the electrons.</span></span>

<span data-ttu-id="afc11-168">Интуиция для того, что означают эти термины, можно получить от операторов создания и аннихилатион, составляющих каждый из них.</span><span class="sxs-lookup"><span data-stu-id="afc11-168">An intuition for what these terms mean can be gleaned from the creation and annihilation operators that comprise each of them.</span></span>
<span data-ttu-id="afc11-169">Например, $h _ {PQ} a ^ \ dagger_p a_q $ описывает электронную прыгающее» из счетчика Орбитал $q $ to Spin Орбитал $p $.</span><span class="sxs-lookup"><span data-stu-id="afc11-169">For example, $h_{pq}a^\dagger_p a_q$ describes the electron hopping from spin orbital $q$ to spin orbital $p$.</span></span>
<span data-ttu-id="afc11-170">Аналогичным образом, термин $h _ {пкрс} a ^ \ dagger_p a ^ \ dagger_q a_r a_s $ (для различных $p, q, r, s $) описывает два электрона в обороте по орбитам $r $ и $s $ разбросанность друг от друга и завершается на обороте по орбите $p $ и $q $.</span><span class="sxs-lookup"><span data-stu-id="afc11-170">Similarly, the term $h_{pqrs} a^\dagger_p a^\dagger_q a_r a_s$ (for distinct $p,q,r,s$) describes two electrons in spin orbitals $r$ and $s$ scattering off of each other and ending up in spin orbitals $p$ and $q$.</span></span>
<span data-ttu-id="afc11-171">Если $r = q $ and $p = s $, $h _ {ПРРП} a ^ \ dagger_p a ^ \ dagger_r a_r a_p = h_ {ПРРП} n_p n_r $ обеспечивает снижение энергии, связанное с двумя электронными, которые находятся ближе друг к другу, но не описывает динамический процесс.</span><span class="sxs-lookup"><span data-stu-id="afc11-171">If $r=q$ and $p=s$ then $h_{prrp} a^\dagger_p a^\dagger_r a_r a_p = h_{prrp} n_p n_r$ gives the energy penalty associated with the two electrons being near each other, but does not describe a dynamical process.</span></span>

<span data-ttu-id="afc11-172">Мы можем представить такие Хамилтонианс с помощью `FermionHamiltonian` класса, который, по сути, является списком, содержащим все нужные `FermionTerm` экземпляры.</span><span class="sxs-lookup"><span data-stu-id="afc11-172">We may represent such Hamiltonians using the `FermionHamiltonian` class, which is essentially a list containing all the desired `FermionTerm` instances.</span></span>
<span data-ttu-id="afc11-173">Поскольку Хамилтонианс являются Хермитиан по определению, мы индексируют термины, использующие более специализированный тип `HermitianFermionTerm` , который также использует симметрию хермитиан при проверке эквивалентности терминов.</span><span class="sxs-lookup"><span data-stu-id="afc11-173">As Hamiltonians are Hermitian by definition, we index terms using the more specialized type `HermitianFermionTerm` that also uses Hermitian symmetry when checking whether terms are equivalent.</span></span>

<span data-ttu-id="afc11-174">Позвольте нам создать несколько наглядных примеров.</span><span class="sxs-lookup"><span data-stu-id="afc11-174">Let us construct a few illustrative examples.</span></span>
<span data-ttu-id="afc11-175">Рассмотрим Хамилтониан $ \Хат{х} = a_0 ^ \дагжер a_1 + a_1 ^ \дагжер a_0 $.</span><span class="sxs-lookup"><span data-stu-id="afc11-175">Consider the Hamiltonian $\hat{H} = a_0^\dagger a_1 + a_1^\dagger a_0$.</span></span>
```csharp
    // We create a `FermionHamiltonian` instance to store the fermion terms.
    var hamiltonian = new FermionHamiltonian();

    // We construct the terms to be added.
    var fermionTerm0 = new FermionTerm(new[] { 1, 0 }.ToLadderSequence());
    var fermionTerm1 = new FermionTerm(new[] { 0, 1 }.ToLadderSequence());

    // These fermion terms are not equal. The following Boolean is `false`.
    var sequenceEqual = fermionTerm0 == fermionTerm1;

    // However, these terms are equal under Hermitian symmetry.
    // We also take the opportunity to demonstrate equivalent constructors
    // for hermitian fermion terms
    var hermitianFermionTerm0 = new HermitianFermionTerm(fermionTerm0);
    var hermitianFermionTerm1 = new HermitianFermionTerm(new[] { 0, 1 });

    // These Hermitian fermion terms are equal. The following Boolean is `true`.
    var hermitianSequenceEqual = hermitianFermionTerm0 == hermitianFermionTerm1;

    // We add the terms to the Hamiltonian with the appropriate coefficient.
    // Note that these terms are identical.
    hamiltonian.Add(hermitianFermionTerm0, 1.0);
    hamiltonian.Add(hermitianFermionTerm1, 1.0);
```
<span data-ttu-id="afc11-176">Мы можем упростить эту конструкцию, используя тот факт, что операторы Хамилтониан являются операторами Хермитиан.</span><span class="sxs-lookup"><span data-stu-id="afc11-176">We may simplify this construction using the fact that Hamiltonian operators are Hermitian operators.</span></span>
<span data-ttu-id="afc11-177">При добавлении терминов в Хамилтониан с помощью `Add` любой термин, не относящийся к хермитиан, например `fermionTerm0` , считается сопряженным с его хермитианным сопряженным.</span><span class="sxs-lookup"><span data-stu-id="afc11-177">When adding terms to the Hamiltonian using `Add`, any non-Hermitian term such as `fermionTerm0` is assumed to be paired with its Hermitian conjugate.</span></span>
<span data-ttu-id="afc11-178">Таким образом, следующий фрагмент кода также представляет один и тот же Хамилтониан:</span><span class="sxs-lookup"><span data-stu-id="afc11-178">Thus the following snippet also represents the same Hamiltonian:</span></span>
```csharp
    // We create a `FermionHamiltonian` instance to store the fermion terms.
    var hamiltonian = new FermionHamiltonian();

    // We construct the term to be added -- note the doubled coefficient.
    hamiltonian.Add(new HermitianFermionTerm(new[] { 1, 0 }), 2.0);
```

<span data-ttu-id="afc11-179">Используя правила защиты от коммутатион, некоторые `FermionTerm` экземпляры в хамилтониан на самом деле соответствуют одной последовательности операторов фермионик, иногда до знака минус.</span><span class="sxs-lookup"><span data-stu-id="afc11-179">Using the anti-commutation rules, some `FermionTerm` instances in the Hamiltonian actually correspond to the same sequence of fermionic operators, sometimes up to a minus sign.</span></span>
<span data-ttu-id="afc11-180">Например, рассмотрим Хамилтониан $H = a_0 ^ \дагжер a_1 ^ \дагжер a_1 a_0-a_1 ^ \дагжер a_0 ^ \дагжер a_1 a_0 = 2a_0 ^ \дагжер a_1 ^ \дагжер a_1 a_0 $, который является суммой ранее построенных терминов.</span><span class="sxs-lookup"><span data-stu-id="afc11-180">For instance, consider the Hamiltonian $H=a_0^\dagger a_1^\dagger a_1 a_0 - a_1^\dagger a_0^\dagger a_1 a_0 =2a_0^\dagger a_1^\dagger a_1 a_0$, which is a sum of terms constructed above.</span></span>
<span data-ttu-id="afc11-181">Не всегда ясно, что это эквивалентно условиям, и поэтому их можно добавить в Хамилтониан отдельно.</span><span class="sxs-lookup"><span data-stu-id="afc11-181">It may not always be clear to the user that these are equivalent terms, and so they may be added to the Hamiltonian separately.</span></span>
<span data-ttu-id="afc11-182">Кроме того, может быть интересно изменить уже существующие термины в Хамилтониан.</span><span class="sxs-lookup"><span data-stu-id="afc11-182">Alternatively, one may be interested in modifying already-existing terms in the Hamiltonian.</span></span>
<span data-ttu-id="afc11-183">В этих случаях можно сочетать эквивалентные термины следующим образом.</span><span class="sxs-lookup"><span data-stu-id="afc11-183">In these cases, we may combine equivalent terms as follows.</span></span>
```csharp
    // We create a `FermionHamiltonian` instance to store the fermion terms.
    var hamiltonian = new FermionHamiltonian();

    // We now create two Hermitian fermion terms that are equivalent with respect to
    // anti-commutation and Hermitian symmetry.
    var terms = new[] {
        (new[] { 0, 1, 1, 0 }, 1.0),
        (new[] { 1, 0, 1, 0 }, 1.0) }
    .Select(o => (new HermitianFermionTerm(o.Item1.ToLadderSequence()), o.Item2.ToDoubleCoeff()));

    // Now add `terms` to the Hamiltonian.
    hamiltonian.AddRange(terms);

    // There is only one unique term. `nTerms == 1` is `true`.
    var nTerms = hamiltonian.CountTerms();
```
<span data-ttu-id="afc11-184">Комбинируя коэффициенты эквивалентных терминов, мы уменьшаем общее количество терминов в Хамилтониан.</span><span class="sxs-lookup"><span data-stu-id="afc11-184">By combining coefficients of equivalent terms, we reduce the total number of terms in the Hamiltonian.</span></span>
<span data-ttu-id="afc11-185">В дальнейшем это сокращает количество шлюзов, необходимых для имитации Хамилтониан.</span><span class="sxs-lookup"><span data-stu-id="afc11-185">Later on, this reduces the number of quantum gates required to simulate the Hamiltonian.</span></span>

### <a name="internal-representation"></a><span data-ttu-id="afc11-186">Внутреннее представление</span><span class="sxs-lookup"><span data-stu-id="afc11-186">Internal Representation</span></span>

<span data-ttu-id="afc11-187">Фермионик Хамилтониан с двумя и двусторонними взаимодействиями представлен в нотации Second-квантования как</span><span class="sxs-lookup"><span data-stu-id="afc11-187">A fermionic Hamiltonian with one- and two-body interactions is represented in second-quantized notation as</span></span>

<span data-ttu-id="afc11-188">$ $ \бегин{алигн} H = \сум \_ {PQ} h \_ {PQ} a ^ \дагжер \_ {p} a \_ {q} + \фрак {1} {2} \сум \_ {пкрс} H \_ {пкрс} а ^ \дагжер \_ {p} a ^ \дагжер \_ {q} a \_ {r} a \_ {s}.</span><span class="sxs-lookup"><span data-stu-id="afc11-188">$$ \begin{align} H=\sum\_{pq}h\_{pq}a^\dagger\_{p}a\_{q}+\frac{1}{2}\sum\_{pqrs}h\_{pqrs}a^\dagger\_{p}a^\dagger\_{q}a\_{r}a\_{s}.</span></span>
<span data-ttu-id="afc11-189">\енд{алигн} $ $</span><span class="sxs-lookup"><span data-stu-id="afc11-189">\end{align} $$</span></span>

<span data-ttu-id="afc11-190">В этой нотации существует не более $N коэффициентов: ^ 2 + N ^ 4 $.</span><span class="sxs-lookup"><span data-stu-id="afc11-190">In this notation, there are at most $N^2+N^4$ coefficients.</span></span>
<span data-ttu-id="afc11-191">Однако многие из этих коэффициентов можно собрать, так как они соответствуют одному оператору.</span><span class="sxs-lookup"><span data-stu-id="afc11-191">However, many of these coefficients may be collected as they correspond to the same operator.</span></span>
<span data-ttu-id="afc11-192">Например, если $p, q, r, s $ — это разные индексы. мы можем использовать правила защиты от коммутатион, чтобы отобразить следующее: $ $ a ^ \дагжер \_ {p} a ^ \дагжер \_ {q} \_ {r} a \_ {s} =-a ^ \дагжер \_ {q} a ^ \дагжер \_ {p} a \_ {r} a \_ {s} =-a ^ \дагжер \_ {p} a ^ \дагжер \_ {q} a \_ {s} a \_ {r} = a ^ \дагжер \_ {q} a ^ \дагжер \_ {p} a \_ {s} a \_ {r}.</span><span class="sxs-lookup"><span data-stu-id="afc11-192">For instance, in the case where $p,q,r,s$ are distinct indices, we may use the anti-commutation rules to show that: $$ a^\dagger\_{p}a^\dagger\_{q}a\_{r}a\_{s} = -a^\dagger\_{q}a^\dagger\_{p}a\_{r}a\_{s} = -a^\dagger\_{p}a^\dagger\_{q}a\_{s}a\_{r} = a^\dagger\_{q}a^\dagger\_{p}a\_{s}a\_{r}.</span></span>
$$

<span data-ttu-id="afc11-193">Более того, поскольку $H $ является Хермитиан, каждый оператор, не Хермитиан фермионик, скажем $h \_ {пкрс} a ^ \дагжер \_ {p} a ^ \дагжер \_ {q} a \_ {r} a \_ {s} $, имеет хермитиан сопряженный, который также находится в $H $.</span><span class="sxs-lookup"><span data-stu-id="afc11-193">Furthermore, as $H$ is Hermitian, every non-Hermitian fermionic operator, say $h\_{pqrs}a^\dagger\_{p}a^\dagger\_{q}a\_{r}a\_{s}$, has a Hermitian conjugate that is also found in $H$.</span></span> <span data-ttu-id="afc11-194">Чтобы обеспечить уникальную индексацию групп терминов, характеризующих эти симметриес, мы определяем каноническое упорядочение по индексам $ (i \_ 1, \кдотс, i \_ n, j \_ 1, \кдотс, j \_ m) $ любой последовательности $n + m $ фермионик Operators $a ^ \дагжер \_ {i \_ 1} \кдотс a \_ \_ \_ \_ \_ {j \_ m} $as следующим образом:</span><span class="sxs-lookup"><span data-stu-id="afc11-194">In order to uniquely index groups of terms characterized by these symmetries, we define a canonical ordering on the indices $(i\_1,\cdots,i\_n,j\_1,\cdots,j\_m)$ of any sequence of $n+m$ fermionic operators $a^\dagger\_{i\_1}\cdots a^\dagger\_{i\_n}a\_{j\_1}\cdots a\_{j\_m}$as follows:</span></span>
-   <span data-ttu-id="afc11-195">Все операторы создания $a ^ \дагжер \_ {i \_ \кдот} $ помещаются перед всеми операторами аннихилатион $a \_ {j \_ \кдот} $.</span><span class="sxs-lookup"><span data-stu-id="afc11-195">All creation operators $a^\dagger\_{i\_\cdot}$ are placed before all annihilation operators $a\_{j\_\cdot}$.</span></span>
-   <span data-ttu-id="afc11-196">Все индексы операторов создания сортируются в возрастающем порядке, то есть $i \_ 1< i \_ 2< \кдотс < я \_ n $.</span><span class="sxs-lookup"><span data-stu-id="afc11-196">All creation operator indices are sorted in ascending order, that is $i\_1< i\_2< \cdots < i\_n$.</span></span>
-   <span data-ttu-id="afc11-197">Все индексы операторов аннихилатион сортируются в убывающем порядке, то есть $j \_ 1> j \_ 2 \кдотс > j \_ m $.</span><span class="sxs-lookup"><span data-stu-id="afc11-197">All annihilation operator indices are sorted in descending order, that is $j\_1> j\_2 \cdots > j\_m$.</span></span>
-   <span data-ttu-id="afc11-198">Самый левый индекс меньше или равен правому индексу, то есть $i \_ 1 – Le j \_ m $.</span><span class="sxs-lookup"><span data-stu-id="afc11-198">The left-most index is less than or equal to the right-most index, that is $i\_1\le j\_m$.</span></span>

<span data-ttu-id="afc11-199">Мы можем определить этот набор канонических упорядоченных индексов как $ $ \бегин{алигн} (i \_ 1, \кдотс, i \_ n, j \_ 1, \кдотс, j \_ m) \ин S \_ {n, m}.</span><span class="sxs-lookup"><span data-stu-id="afc11-199">Let us identify this set of canonically ordered indices as $$ \begin{align} (i\_1,\cdots,i\_n,j\_1,\cdots,j\_m) \in S\_{n,m}.</span></span>
<span data-ttu-id="afc11-200">\енд{алигн} $ $</span><span class="sxs-lookup"><span data-stu-id="afc11-200">\end{align} $$</span></span>

<span data-ttu-id="afc11-201">При таком каноническом упорядочении фермионик Хамилтониан может быть выражен как $ $ \бегин{алигн} H = \сум \_ {(p, q) \Ин S \_ {1,1} } H ' \_ {PQ} \фрак{а ^ \дагжер \_ {p} a \_ {q} + a ^ \дагжер { \_ q} a \_ {p}} {2} + \сум \_ {(p, q, r, s) \ин S \_ {2,2} } H ' \_ {пкрс} \фрак{а ^ \dagger \_ {p} a ^ \dagger \_ {q} a \_ {r} a \_ {S} + a ^ \dagger \_ {s} a ^ \dagger \_ {r} \_ {q} a \_ {p}} {2} , \end{align} $ $ с соответствующим образом адаптированные и два электронных $h " \_ {PQ} $ и $h" \_ {PQRS} $ соответственно ".</span><span class="sxs-lookup"><span data-stu-id="afc11-201">With this canonical ordering, the fermionic Hamiltonian may be expressed as $$ \begin{align} H=\sum\_{(p,q)\in S\_{1,1}}h'\_{pq}\frac{a^\dagger\_{p}a\_{q}+a^\dagger\_{q}a\_{p}}{2}+\sum\_{(p,q,r,s)\in S\_{2,2}}h'\_{pqrs}\frac{a^\dagger\_{p}a^\dagger\_{q}a\_{r}a\_{s}+a^\dagger\_{s}a^\dagger\_{r}a\_{q}a\_{p}}{2}, \end{align} $$ with suitably adapted one- and two-electron integrals $h'\_{pq}$ and $h'\_{pqrs}$, respectively.</span></span>

