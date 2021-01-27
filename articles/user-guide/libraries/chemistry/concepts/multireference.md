---
title: Коррелированные волновые функции
description: Сведения о динамических и нединамических корреляциях в вавефунктионс с помощью библиотеки Microsoft тактов химия.
author: guanghaolow
ms.author: gulow
ms.date: 05/28/2019
ms.topic: conceptual
uid: microsoft.quantum.chemistry.concepts.multireference
no-loc:
- Q#
- $$v
ms.openlocfilehash: ab3d90d79c7c14a1ef5b3aa833df49be186f3dd7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856278"
---
# <a name="correlated-wavefunctions"></a><span data-ttu-id="8c5fe-103">Коррелированные волновые функции</span><span class="sxs-lookup"><span data-stu-id="8c5fe-103">Correlated wavefunctions</span></span>

<span data-ttu-id="8c5fe-104">Для многих систем, особенно тех, которые близки к равновесия геометрии, [Хартри – Фокк](xref:microsoft.quantum.chemistry.concepts.hartreefock) теоретически предоставляет качественное описание свойств молекулярное через однозначное состояние ссылки.</span><span class="sxs-lookup"><span data-stu-id="8c5fe-104">For many systems, particularly those near the equilibrium geometry, [Hartree–Fock](xref:microsoft.quantum.chemistry.concepts.hartreefock) theory provides a qualitative description of molecular properties through a single-determinant reference state.</span></span> <span data-ttu-id="8c5fe-105">Однако для достижения количественной точности необходимо также рассмотреть эффекты корреляции.</span><span class="sxs-lookup"><span data-stu-id="8c5fe-105">However, in order to achieve quantitative accuracy, one must also consider correlation effects.</span></span> 

<span data-ttu-id="8c5fe-106">В этом контексте важно динстингуиш между динамической и нединамической корреляциями.</span><span class="sxs-lookup"><span data-stu-id="8c5fe-106">In this context, it is important to dinstinguish between dynamic and non-dynamic correlations.</span></span>
<span data-ttu-id="8c5fe-107">Динамическая корреляция возникает из-за тенденции электронов, чтобы остаться в отдельном виде, например в связи с межэлектронным отталкивания.</span><span class="sxs-lookup"><span data-stu-id="8c5fe-107">Dynamical correlations arise from the tendency of electrons to stay apart, such as due to interelectronic repulsion.</span></span> <span data-ttu-id="8c5fe-108">Этот результат можно смоделировать, просматривая ексЦитатионс из состояния ссылки.</span><span class="sxs-lookup"><span data-stu-id="8c5fe-108">This effect can be modelled by considering excitations of electrons out of the reference state.</span></span> <span data-ttu-id="8c5fe-109">Нединамические корреляции возникают, когда вавефунктион определяется двумя или более конфигурациями в начальном порядке, даже чтобы получить только качественное описание системы.</span><span class="sxs-lookup"><span data-stu-id="8c5fe-109">Non-dynamic correlations arise when the wavefunction is dominated by two or more configurations at zeroth order, even to achieve only a qualitative description of the system.</span></span>
<span data-ttu-id="8c5fe-110">Это требует определителями и представляет собой пример многоэталонного вавефунктион.</span><span class="sxs-lookup"><span data-stu-id="8c5fe-110">This necessitates a superposition of determinants and is an example of a multireference wavefunction.</span></span>

<span data-ttu-id="8c5fe-111">Библиотека химия предоставляет способ указания начальном порядка вавефунктион для проблемы с многоссылками в виде геоположения определителями.</span><span class="sxs-lookup"><span data-stu-id="8c5fe-111">The chemistry library provides a way to specify a zeroth order wavefunction for the multireference problem as a superposition of determinants.</span></span> <span data-ttu-id="8c5fe-112">Этот подход, который мы вызываем многовавефунктионсую многоссылочную многосправочную функцию, эффективен, когда достаточно нескольких компонентов, чтобы указать эту часть.</span><span class="sxs-lookup"><span data-stu-id="8c5fe-112">This approach, which we call sparse multireference wavefunctions, is effective when only a few components suffice to specify the superposition.</span></span> <span data-ttu-id="8c5fe-113">Библиотека также предоставляет метод для включения динамических корреляций поверх однозначной ссылки с помощью обобщенного универсального ансатз-кластера.</span><span class="sxs-lookup"><span data-stu-id="8c5fe-113">The library also provides a method to include dynamic correlations on top of a single-determinant reference via the generalized unitary coupled-cluster ansatz.</span></span> <span data-ttu-id="8c5fe-114">Кроме того, он создает тактовые цепи, которые создают эти состояния на компьютере-такте.</span><span class="sxs-lookup"><span data-stu-id="8c5fe-114">Furthermore, it also constructs quantum circuits that generate these states on a quantum computer.</span></span> <span data-ttu-id="8c5fe-115">Эти состояния могут быть указаны в [схеме брумбридже](xref:microsoft.quantum.libraries.chemistry.schema.broombridge). Кроме того, мы предоставляем функции для ручного указания этих состояний в библиотеке химия.</span><span class="sxs-lookup"><span data-stu-id="8c5fe-115">These states may be specified in the [Broombridge schema](xref:microsoft.quantum.libraries.chemistry.schema.broombridge), and we also provide the functionality to manually specify these states through the chemistry library.</span></span>

## <a name="sparse-multi-reference-wavefunction"></a><span data-ttu-id="8c5fe-116">Вавефунктион разреженных нескольких ссылок</span><span class="sxs-lookup"><span data-stu-id="8c5fe-116">Sparse multi-reference wavefunction</span></span>
<span data-ttu-id="8c5fe-117">Состояние с множественной ссылкой $ \кет{\ psi_ {\рм {МКСКФ}}} $ может быть явно задано как линейное сочетание $N $-электрон Слатер детермининантс.</span><span class="sxs-lookup"><span data-stu-id="8c5fe-117">A multi-reference state $\ket{\psi_{\rm {MCSCF}}}$ may be specified explicitly as a linear combination of $N$-electron Slater determininants.</span></span>
<span data-ttu-id="8c5fe-118">\бегин{алигн} \кет{\ psi_ {\рм {МКСКФ}}} \пропто \ sum_ {i_1 < i_2 < \кдотс < i_N} \ lambda_ {i_1, i_2, \кдотс, i_N} a ^ \ dagger_ {i_1} а ^ \ dagger_ {i_2} \кдотс a ^ \ dagger_ {i_N} \кет {0} .</span><span class="sxs-lookup"><span data-stu-id="8c5fe-118">\begin{align} \ket{\psi_{\rm {MCSCF}}} \propto \sum_{i_1 < i_2 < \cdots < i_N} \lambda_{i_1,i_2,\cdots,i_N} a^\dagger_{i_1}a^\dagger_{i_2}\cdots a^\dagger_{i_N}\ket{0}.</span></span>
<span data-ttu-id="8c5fe-119">Например, \енд{алигн} State $ \пропто (0,1 a ^ \ dagger_1a ^ \ dagger_2a ^ \ dagger_6 – 0,2 a ^ \ dagger_2a ^ \ dagger_1a ^ \ dagger_5) \кет {0} $ можно указать в библиотеке химия следующим образом.</span><span class="sxs-lookup"><span data-stu-id="8c5fe-119">\end{align} For example, the state $\propto(0.1 a^\dagger_1a^\dagger_2a^\dagger_6 - 0.2 a^\dagger_2a^\dagger_1a^\dagger_5)\ket{0}$ may be specified in the chemistry library as follows.</span></span>
```csharp
// Create a list of tuples where the first item of each 
// tuple are indices to the creation operators acting on the
// vacuum state, and the second item is the coefficient
// of that basis state.
var superposition = new[] {
    (new[] {1, 2, 6}, 0.1),
    (new[] {2, 1, 5}, -0.2) };

// Create a fermion wavefunction object that represents the superposition.
var wavefunction = new FermionWavefunction<int>(superposition);
```
<span data-ttu-id="8c5fe-120">Это явное представление компонентов с четким позиционирование эффективно, если необходимо указать только несколько компонентов.</span><span class="sxs-lookup"><span data-stu-id="8c5fe-120">This explicit representation of the superposition components is effective when only a few components need to be specified.</span></span> <span data-ttu-id="8c5fe-121">Необходимо избегать использования этого представления, если требуется много компонентов для точного захвата требуемого состояния.</span><span class="sxs-lookup"><span data-stu-id="8c5fe-121">One should avoid using this representation when many components are required to accurately capture the desired state.</span></span> <span data-ttu-id="8c5fe-122">Причиной этого является стоимость шлюза тактовой цепи, которая готовит это состояние на тактовый компьютер, который масштабируется по крайней мере линейно в соответствии с количеством компонентов с максимальным позиционированием, и, в большинстве случаев, с одним из этих амплитуд.</span><span class="sxs-lookup"><span data-stu-id="8c5fe-122">The reason for this is the gate cost of quantum circuit that prepares this state on a quantum computer, which scales at least linearly with the number of superposition components, and at most quadratically with the one-norm of the superposition amplitudes.</span></span>

## <a name="unitary-coupled-cluster-wavefunction"></a><span data-ttu-id="8c5fe-123">Единая пара-вавефунктион кластера</span><span class="sxs-lookup"><span data-stu-id="8c5fe-123">Unitary coupled-cluster wavefunction</span></span>
<span data-ttu-id="8c5fe-124">Также можно указать отдельный связанный-Cluster вавефунктион $ \кет{\ psi_ {\рм {УКК}} $ с помощью библиотеки чемистери.</span><span class="sxs-lookup"><span data-stu-id="8c5fe-124">It is also possible to specify a unitary coupled-cluster wavefunction $\ket{\psi_{\rm {UCC}}}$ using the chemistery library.</span></span> <span data-ttu-id="8c5fe-125">В этом случае у нас есть одно детерминированное состояние ссылки, скажем, $ \кет{\ psi_ {\Рм{СКФ}}} $.</span><span class="sxs-lookup"><span data-stu-id="8c5fe-125">In this situation, we have a single-determinant reference state, say, $\ket{\psi_{\rm{SCF}}}$.</span></span> <span data-ttu-id="8c5fe-126">Компоненты единой пары вавефунктион кластера задаются неявно с помощью единого оператора, действующего на состояние ссылки.</span><span class="sxs-lookup"><span data-stu-id="8c5fe-126">The components of the unitary coupled-cluster wavefunction are then specified implicity through a unitary operator acting on a reference state.</span></span>
<span data-ttu-id="8c5fe-127">Этот единой оператор обычно пишется как $e ^ {T-T ^ \дагжер} $, где $T-T ^ \дагжер $ является оператором кластера Anti-Хермитиан.</span><span class="sxs-lookup"><span data-stu-id="8c5fe-127">This unitary operator is commonly written as $e^{T-T^\dagger}$, where $T-T^\dagger$ is the anti-Hermitian cluster operator.</span></span> <span data-ttu-id="8c5fe-128">Таким \бегин{алигн} \кет{\ psi_ {\рм {УКК}}} = e ^ {T-T ^ \дагжер}\кет{\ psi_ {\Рм{СКФ}}}.</span><span class="sxs-lookup"><span data-stu-id="8c5fe-128">Thus \begin{align} \ket{\psi_{\rm {UCC}}} = e^{T-T^\dagger}\ket{\psi_{\rm{SCF}}}.</span></span>
<span data-ttu-id="8c5fe-129">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="8c5fe-129">\end{align}</span></span>

<span data-ttu-id="8c5fe-130">Также часто можно разделить оператор кластера $T = T_1 + T_2 + \кдотс $ на части, где каждая часть $T _j $ содержит $j термины $-Body.</span><span class="sxs-lookup"><span data-stu-id="8c5fe-130">It is also common to split the cluster operator $T = T_1 + T_2 + \cdots$ into parts, where each part $T_j$ contains $j$-body terms.</span></span> <span data-ttu-id="8c5fe-131">В обобщенной паре с кластеризацией один основной оператор кластера (Single) имеет вид \бегин{алигн} T_1 = \ sum_ {PQ} T ^ {p} _ {q} a ^ \ dagger_p a_q, \енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="8c5fe-131">In generalized coupled-cluster theory, the one-body cluster operator (singles) is of the form \begin{align} T_1 = \sum_{pq}t^{p}_{q} a^\dagger_p a_q, \end{align}</span></span>

<span data-ttu-id="8c5fe-132">и оператором кластеризации двух основных значений (Double) является форма \бегин{алигн} T_2 = \ sum_ {пкрс} T ^ {PQ} _ {RS} a ^ \ dagger_p a ^ \ dagger_q a_r a_s.</span><span class="sxs-lookup"><span data-stu-id="8c5fe-132">and two-body cluster operator (doubles) is of the form \begin{align} T_2 = \sum_{pqrs}t^{pq}_{rs} a^\dagger_p a^\dagger_q a_r a_s.</span></span>
<span data-ttu-id="8c5fe-133">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="8c5fe-133">\end{align}</span></span>

<span data-ttu-id="8c5fe-134">Более высокие условия (Triple, четверные и т. д.) возможны, но в настоящее время не поддерживаются библиотекой химия.</span><span class="sxs-lookup"><span data-stu-id="8c5fe-134">Higher-order terms (triples, quadruples, etc.) are possible, but not currently supported by the chemistry library.</span></span>

<span data-ttu-id="8c5fe-135">Например, пусть $ \кет{\ psi_ {\Рм{СКФ}}} = a ^ \ dagger_1 a ^ \ dagger_2 \кет {0} $, а $T = 0,123 a ^ \ dagger_0 A_1 + 0,456 а ^ \ dagger_0a ^ \ dagger_3 A_1 A_2-0,789 a ^ \ dagger_3a ^ \ dagger_2 a_1 a_0 $.</span><span class="sxs-lookup"><span data-stu-id="8c5fe-135">For example, let $\ket{\psi_{\rm{SCF}}} = a^\dagger_1 a^\dagger_2\ket{0}$, and let $T= 0.123 a^\dagger_0 a_1 + 0.456 a^\dagger_0a^\dagger_3 a_1 a_2 - 0.789 a^\dagger_3a^\dagger_2 a_1 a_0$.</span></span> <span data-ttu-id="8c5fe-136">Затем это состояние создается в библиотеке химия следующим образом.</span><span class="sxs-lookup"><span data-stu-id="8c5fe-136">Then this state is instantiated in the chemistry library as follows.</span></span>
```csharp
// Create a list of indices of the creation operators
// for the single-reference state
var reference = new[] { 1, 2 };

// Create a list describing the cluster operator
// The first half of each list of integers will be
// associated with the creation operators, and
// the second half with the annihilation operators.
var clusterOperator = new[]
{
    (new [] {0, 1}, 0.123),
    (new [] {0, 3, 1, 2}, 0.456),
    (new [] {3, 2, 1, 0}, 0.789)
};

// Create a fermion wavefunction object that represents the 
// unitary coupled-cluster wavefunction. It is assumed implicity
// that the exponent of the unitary coupled-cluster operator
// is the cluster operator minus its Hermitian conjugate.
var wavefunction = new FermionWavefunction<int>(reference, clusterOperator);
```

<span data-ttu-id="8c5fe-137">Оператор Spin конверватион можно сделать явным образом, вместо этого задавая `SpinOrbital` индексы вместо целочисленных индексов.</span><span class="sxs-lookup"><span data-stu-id="8c5fe-137">Spin convervation may be made explicit by instead specifying `SpinOrbital` indices instead of integer indices.</span></span> <span data-ttu-id="8c5fe-138">Например, пусть $ \кет{\ psi_ {\Рм{СКФ}}} = a ^ \ dagger_ {1, \упарров} a ^ \ dagger_ {2, \довнарров}\кет {0} $ и let $T = 0,123 a ^ \ dagger_ {0, \упарров} A_ {1, \упарров} + 0,456 a ^ \ dagger_ {0, \упарров} a ^ \ dagger_ {3, \довнарров} A_ {1, \uparrow} A_ {2, \downarrow}-0,789 а ^ \ dagger_ {3, \uparrow} a ^ \ dagger_ {2, \uparrow} A_ {1, \uparrow} A_ {0, \uparrow} $ быть Spin convserving.</span><span class="sxs-lookup"><span data-stu-id="8c5fe-138">For example, let $\ket{\psi_{\rm{SCF}}} = a^\dagger_{1,\uparrow} a^\dagger_{2, \downarrow}\ket{0}$, and let $T= 0.123 a^\dagger_{0, \uparrow} a_{1, \uparrow} + 0.456 a^\dagger_{0, \uparrow} a^\dagger_{3, \downarrow} a_{1, \uparrow} a_{2, \downarrow} - 0.789 a^\dagger_{3,\uparrow} a^\dagger_{2,\uparrow} a_{1,\uparrow} a_{0, \uparrow}$ be spin convserving.</span></span> <span data-ttu-id="8c5fe-139">Затем это состояние создается в библиотеке химия следующим образом.</span><span class="sxs-lookup"><span data-stu-id="8c5fe-139">Then this state is instantiated in the chemistry library as follows.</span></span>
```csharp
// Create a list of indices of the creation operators
// for the single-reference state
var reference = new[] { (1, Spin.u), (2, Spin.d) }.ToSpinOrbitals();

// Create a list describing the cluster operator
// The first half of each list of integers will be
// associated with the creation operators, and
// the second half with the annihilation operators.
var clusterOperator = new[]
{
    (new [] {(0, Spin.u), (1, Spin.u)}, 0.123),
    (new [] {(0, Spin.u), (3, Spin.d), (1, Spin.u), (2, Spin.d)}, 0.456),
    (new [] {(3, Spin.u), (2, Spin.u), (1, Spin.u), (0, Spin.u)}, 0.789)
}.Select(o => (o.Item1.ToSpinOrbitals(), o.Item2);

// Create a fermion wavefunction object that represents the 
// unitary coupled-cluster wavefunction. It is assumed implicity
// that the exponent of the unitary coupled-cluster operator
// is the cluster operator minus its Hermitian conjugate.
var wavefunctionSpinOrbital = new FermionWavefunction<SpinOrbital>(reference, clusterOperator);

// Convert the wavefunction indexed by spin-orbitals to one indexed
// by integers
var wavefunctionInteger = wavefunctionSpinOrbital.ToIndexing(IndexConvention.UpDown);
```

<span data-ttu-id="8c5fe-140">Мы также предоставляем удобную функцию, которая выполняет перечисление всех операторов кластеризации, аннихилате только занятые обороты и Стимулируйте обучение только на незанятые обороты.</span><span class="sxs-lookup"><span data-stu-id="8c5fe-140">We also provide a convenience function that enumerates over all spin-conversing cluster operators that annihilate only occupied spin-orbitals and excite to only unoccupied spin-orbitals.</span></span>
```csharp
// Create a list of indices of the creation operators
// for the single-reference state
var reference = new[] { (1, Spin.u), (2, Spin.d) }.ToSpinOrbitals();

// Generate all spin-conversing excitations from spin-orbitals 
// occupied by the reference state to virtual orbitals.
var generatedExcitations = reference.CreateAllUCCSDSingletExcitations(nOrbitals: 3).Excitations;

// This is the list of expected spin-consvering excitations
var expectedExcitations = new[]
{
    new []{ (0, Spin.u), (1,Spin.u)},
    new []{ (2, Spin.u), (1,Spin.u)},
    new []{ (0, Spin.d), (2,Spin.d)},
    new []{ (1, Spin.d), (2,Spin.d)},
    new []{ (0, Spin.u), (0, Spin.d), (2, Spin.d), (1,Spin.u)},
    new []{ (0, Spin.u), (1, Spin.d), (2, Spin.d), (1,Spin.u)},
    new []{ (0, Spin.d), (2, Spin.u), (2, Spin.d), (1,Spin.u)},
    new []{ (1, Spin.d), (2, Spin.u), (2, Spin.d), (1,Spin.u)}
}.Select(o => new IndexOrderedSequence<SpinOrbital>(o.ToLadderSequence()));

// The following two assertions are true, and verify that the generated 
// excitations exactly match the expected excitations.
var bool0 = generatedExcitations.Keys.All(expectedExcitations.Contains);
var bool1 = generatedExcitations.Count() == expectedExcitations.Count();
```
