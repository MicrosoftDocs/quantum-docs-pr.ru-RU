---
title: Хартри-Фоккная теория
description: Узнайте о теории Хартри – Фокк — простой способ создания начального состояния для тактовых систем.
author: bradben
ms.author: v-benbra
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.hartreefock
no-loc:
- Q#
- $$v
ms.openlocfilehash: 53d6e4342e5b58886528e89871591e57d8e70c82
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/21/2020
ms.locfileid: "90835355"
---
# <a name="hartreefock-theory"></a><span data-ttu-id="f8b5f-103">Хартри — теория Фокк</span><span class="sxs-lookup"><span data-stu-id="f8b5f-103">Hartree–Fock Theory</span></span>

<span data-ttu-id="f8b5f-104">Возможно, самым важным количеством в симуляторе тактовой химия является состояние заземления, которое является минимальным еиженвектором энергии в матрице Хамилтониан.</span><span class="sxs-lookup"><span data-stu-id="f8b5f-104">Perhaps the most important quantity in quantum chemistry simulation is the ground state, which is the minimum energy eigenvector of the Hamiltonian matrix.</span></span>
<span data-ttu-id="f8b5f-105">Это связано с тем, что для большинства молекул в таких показателях температуры, как скорость реагирования, обусловлено свободным снижением энергии между состояниями такта, описывающими начало и конец шага в пути реагирования и комнатной температуры, такой как промежуточное состояние, обычно это состояния земли.</span><span class="sxs-lookup"><span data-stu-id="f8b5f-105">This is because for most molecules at room temperature quantities such as reaction rates are dominated by free energy differences between quantum states that describe the beginning and end of a step in a reaction pathway and at room temperature such intermediate state are usually ground states.</span></span>
<span data-ttu-id="f8b5f-106">Хотя состояние заземления обычно слишком сложно для обучения (даже при использовании тактового компьютера), так как это распределение по экспоненциально большому количеству конфигураций.</span><span class="sxs-lookup"><span data-stu-id="f8b5f-106">While the ground state is typically too hard to learn (even with a quantum computer) because it is a distribution over an exponentially large number of configurations.</span></span>
<span data-ttu-id="f8b5f-107">Можно изученировать такие объемы, как энергия в состоянии заземления.</span><span class="sxs-lookup"><span data-stu-id="f8b5f-107">Quantities such as ground state energy can be learned.</span></span>
<span data-ttu-id="f8b5f-108">Например, если $ \кет{\пси} $ является любым чистым состоянием такта, то \бегин{екуатион} E = \бра{\пси} \Хат{х} \кет{\пси} \енд{екуатион} дает среднее значение энергии, в котором система находится в этом состоянии.</span><span class="sxs-lookup"><span data-stu-id="f8b5f-108">For example, if $\ket{\psi}$ is any pure quantum state then \begin{equation} E = \bra{ \psi } \hat{H} \ket{\psi} \end{equation} gives the mean energy that the system has in that state.</span></span>
<span data-ttu-id="f8b5f-109">Состояние заземления затем — это состояние, которое дает наименьшее такое значение.</span><span class="sxs-lookup"><span data-stu-id="f8b5f-109">The ground state then is the state that gives the smallest such value.</span></span> <span data-ttu-id="f8b5f-110">В результате выбор состояния, максимально близкого к истинному состоянию заземления, крайне важно для оценки энергии либо напрямую (как это делается в еиженсолверс), либо с помощью оценки этапа.</span><span class="sxs-lookup"><span data-stu-id="f8b5f-110">As a result, choosing a state that is as close as possible to the true ground state is vitally important for estimating the energy either directly (as is done in variational eigensolvers) or through phase estimation.</span></span>

<span data-ttu-id="f8b5f-111">Хартри — Фокк теоретически предоставляет простой способ создания начального состояния для тактовых систем.</span><span class="sxs-lookup"><span data-stu-id="f8b5f-111">Hartree–Fock theory gives a simple way to construct the initial state for quantum systems.</span></span> <span data-ttu-id="f8b5f-112">Он дает единое Слатер приближение к состоянию заземления тактовой системы.</span><span class="sxs-lookup"><span data-stu-id="f8b5f-112">It yields a single Slater-determinant approximation to the ground state of a quantum system.</span></span> <span data-ttu-id="f8b5f-113">Для этого он находит поворот в Фокк пространстве, который уменьшает энергию штата земли.</span><span class="sxs-lookup"><span data-stu-id="f8b5f-113">To that end, it finds a rotation within Fock-space that minimizes the ground state energy.</span></span> <span data-ttu-id="f8b5f-114">В частности, для системы $N $ электронов метод выполняет поворот \бегин{екуатион} \ prod_ {j = 0} ^ {N-1} a ^ \ dagger_j \кет {0} \мапсто \ prod_ {j = 0} ^ {N-1} e ^ {u} a ^ \ dagger_j e ^ {-u} \кет {0} \дефек\ prod_ {j = 0} ^ {N-1} \видетилде{а} ^ \ dagger_j \кет {0} \енд{екуатион} с Anti-хермитиан (т. е. $u =-u ^ \dagger $) матрица $u = \ sum_ {PQ} u_ {PQ} a ^ \ dagger_p a_q $.</span><span class="sxs-lookup"><span data-stu-id="f8b5f-114">In particular, for a system of $N$ electrons the method performs the rotation \begin{equation} \prod_{j=0}^{N-1} a^\dagger_j \ket{0} \mapsto \prod_{j=0}^{N-1} e^{u} a^\dagger_j e^{-u} \ket{0}\defeq\prod_{j=0}^{N-1}  \widetilde{a}^\dagger_j  \ket{0}, \end{equation} with an anti-Hermitian (i.e. $u= -u^\dagger$) matrix $u = \sum_{pq} u_{pq} a^\dagger_p a_q$.</span></span> <span data-ttu-id="f8b5f-115">Следует отметить, что матрица $u $ представляет повороты Орбитал, а $ \видетилде{а} ^ \ dagger_j $ и $ \видетилде{а} _j $ представляют операторы создания и аннихилатион для электронов, занимающих Хартри – Фокк молекулярное Spin-орбиты.</span><span class="sxs-lookup"><span data-stu-id="f8b5f-115">It should be noted that the matrix $u$ represents the orbital rotations and $\widetilde{a}^\dagger_j$ and $\widetilde{a}_j$ represent creation and annihilation operators for electrons occupying Hartree–Fock molecular spin-orbitals.</span></span>


<span data-ttu-id="f8b5f-116">Матрица $u $ оптимизирована для сворачивания ожидаемого энергопотребления \* \бра {0} \ prod_ {j = 0} ^ {N-1} \видетилде{а} \_ j H \прод \_ {k = 0} ^ {N-1} \видетилде{а} ^ \ dagger_k \кет {0} $.</span><span class="sxs-lookup"><span data-stu-id="f8b5f-116">The matrix $u$ is then optimized to minimize the expected energy $\bra{0} \prod_{j=0}^{N-1}  \widetilde{a}\_j  H \prod\_{k=0}^{N-1}  \widetilde{a}^\dagger_k\ket{0}$.</span></span> <span data-ttu-id="f8b5f-117">Хотя такие проблемы оптимизации могут быть общими, на практике алгоритм Хартри – Фокк, как правило, быстро сходится к ближайшему решению проблемы оптимизации, особенно для молекул с закрытой оболочкой в геометрических фигурах равновесия.</span><span class="sxs-lookup"><span data-stu-id="f8b5f-117">While such optimization problems may be generically hard, in practice the Hartree–Fock algorithm tends to rapidly converge to a near-optimal solution to the optimization problem, especially for closed-shell molecules in the equilibrium geometries.</span></span> <span data-ttu-id="f8b5f-118">Эти состояния можно указать как экземпляр `FermionWavefunction` объекта.</span><span class="sxs-lookup"><span data-stu-id="f8b5f-118">We may specify these states as an instance of the `FermionWavefunction` object.</span></span> <span data-ttu-id="f8b5f-119">Например, состояние $a ^ \ dagger_ a ^ \ {1} dagger_ {2} a ^ \ dagger_ {6} \кет {0} $ создается в библиотеке химия следующим образом.</span><span class="sxs-lookup"><span data-stu-id="f8b5f-119">For instance, the state $a^\dagger_{1}a^\dagger_{2}a^\dagger_{6}\ket{0}$ is instantiated in the chemistry library as follows.</span></span>
```csharp
// Create a list of integer indices of the creation operators
var indices = new[] { 1, 2, 6 };

// Convert the list of indices to a `FermionWavefunction` object.
// In this case, the indices are integers, so we use the `int`
// type specialization.
var wavefunction = new FermionWavefunction<int>(indices);
```
<span data-ttu-id="f8b5f-120">Также можно индексировать функции Wave с `SpinOrbital` индексами, а затем преобразовывать эти индексы в целые числа, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="f8b5f-120">It is also possible to index wave functions with `SpinOrbital` indices, and then convert these indices to integers as follows.</span></span>
```csharp
// Create a list of spin orbital indices of the creation operators
var indices = new[] { (0, Spin.d), (1,Spin.u), (3, Spin.u) };

// Convert the list of indices to a `FermionWavefunction` object.
var wavefunctionSpinOrbital = new FermionWavefunction<SpinOrbital>(indices.ToSpinOrbitals());

// Convert a wavefunction indexed by spin orbitals to
// one indexed by integers
var wavefunctionInt = wavefunctionSpinOrbital.ToIndexing(IndexConvention.UpDown);
```

<span data-ttu-id="f8b5f-121">Самая некоторая функция Хартри – Фокк теоретически заключается в том, что она дает состояние такта, в котором нет замкнутые между электронными обработкой.</span><span class="sxs-lookup"><span data-stu-id="f8b5f-121">The most striking feature about Hartree–Fock theory is that it yields a quantum state that has no entanglement between the electrons.</span></span>
<span data-ttu-id="f8b5f-122">Это означает, что он часто предоставляет качественное описание свойств систем молекулярное.</span><span class="sxs-lookup"><span data-stu-id="f8b5f-122">This means that it often provides a suitable qualitative description of properties of molecular systems.</span></span> 

<span data-ttu-id="f8b5f-123">Состояние Хартри-Фокк также может быть восстановлено из, `FermionHamiltonian`  как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="f8b5f-123">The Hartree-Fock state may also be reconstructed from a `FermionHamiltonian`  as follows.</span></span>
```csharp
// We initialize a fermion Hamiltonian.
var fermionHamiltonian = new FermionHamiltonian();

// Create a Hartree-Fock state from the Hamiltonian 
// with, say, `4` occupied spin orbitals.
var wavefunction = fermionHamiltonian.CreateHartreeFockState(nElectrons: 4);
```

<span data-ttu-id="f8b5f-124">Однако получение точных результатов, особенно для строго связанных систем, требует состояний тактов, выходящих за рамки Хартри – Фокк теории.</span><span class="sxs-lookup"><span data-stu-id="f8b5f-124">However, obtaining accurate results, especially for strongly correlated systems, necessitate quantum states that go beyond Hartree–Fock theory.</span></span>
