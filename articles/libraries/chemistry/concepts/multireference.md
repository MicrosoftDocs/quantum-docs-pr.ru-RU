---
title: Коррелированный вавефунктионс | Документация Майкрософт
description: Концептуальные документы по тактовой Dynamics
author: guanghaolow
ms.author: gulow@microsoft.com
ms.date: 05/28/2019
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.multireference
ms.openlocfilehash: 0b14f373d31c5b63e313e07810daf62d9195b1d3
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/26/2019
ms.locfileid: "73184038"
---
# <a name="correlated-wavefunctions"></a>Коррелированные вавефунктионс

Для многих систем, особенно тех, которые близки к равновесия геометрии, [Хартри – Фокк](xref:microsoft.quantum.chemistry.concepts.hartreefock) теоретически предоставляет качественное описание свойств молекулярное через однозначное состояние ссылки. Однако для достижения количественной точности необходимо также рассмотреть эффекты корреляции. 

В этом контексте важно динстингуиш между динамической и нединамической корреляциями.
Динамическая корреляция возникает из-за тенденции электронов, чтобы остаться в отдельном виде, например в связи с межэлектронным отталкивания. Этот результат можно смоделировать, просматривая ексЦитатионс из состояния ссылки. Нединамические корреляции возникают, когда вавефунктион определяется двумя или более конфигурациями в начальном порядке, даже чтобы получить только качественное описание системы.
Это требует определителями и представляет собой пример многоэталонного вавефунктион.

Библиотека химия предоставляет способ указания начальном порядка вавефунктион для проблемы с многоссылками в виде геоположения определителями. Этот подход, который мы вызываем многовавефунктионсую многоссылочную многосправочную функцию, эффективен, когда достаточно нескольких компонентов, чтобы указать эту часть. Библиотека также предоставляет метод для включения динамических корреляций поверх однозначной ссылки с помощью обобщенного универсального ансатз-кластера. Кроме того, он создает тактовые цепи, которые создают эти состояния на компьютере-такте. Эти состояния могут быть указаны в [схеме брумбридже](xref:microsoft.quantum.libraries.chemistry.schema.broombridge). Кроме того, мы предоставляем функции для ручного указания этих состояний в библиотеке химия.

## <a name="sparse-multi-reference-wavefunction"></a>Вавефунктион разреженных нескольких ссылок
Состояние с множественной ссылкой $ \ket{\psi_{\rm {МКСКФ}}} $ может быть задано явным образом как линейное сочетание $N $-электрон Слатер детермининантс.
\бегин{алигн} \ket{\psi_{\rm {МКСКФ}}} \пропто \sum_{I_1 < i_2 < \кдотс < i_N} \lambda_{I_1, i_2, \кдотс, i_N} a ^ \dagger_{I_1}a ^ \dagger_{i_2}\cdots a ^ \dagger_{i_N}\ket{0}.
Например, \енд{алигн} State $ \пропто (0,1 a ^ \dagger_1a ^ \dagger_2a ^ \dagger_6-0,2 a ^ \dagger_2a ^ \dagger_1a ^ \dagger_5) \кет{0}$ может быть указан в библиотеке химия следующим образом.
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
Это явное представление компонентов с четким позиционирование эффективно, если необходимо указать только несколько компонентов. Необходимо избегать использования этого представления, если требуется много компонентов для точного захвата требуемого состояния. Причиной этого является стоимость шлюза тактовой цепи, которая готовит это состояние на тактовый компьютер, который масштабируется по крайней мере линейно в соответствии с количеством компонентов с максимальным позиционированием, и, в большинстве случаев, с одним из этих амплитуд.

## <a name="unitary-coupled-cluster-wavefunction"></a>Единая пара-вавефунктион кластера
Также можно указать отдельный связанный-Cluster вавефунктион $ \ket{\psi_{\rm {УКК}}} $ с помощью библиотеки чемистери. В этом случае у нас есть одно определяющее состояние ссылки, скажем, $ \ket{\psi_{\rm{SCF}}} $. Компоненты единой пары вавефунктион кластера задаются неявно с помощью единого оператора, действующего на состояние ссылки.
Этот единой оператор обычно пишется как $e ^ {T-T ^ \дагжер} $, где $T-T ^ \дагжер $ является оператором кластера Anti-Хермитиан. Таким \бегин{алигн} \ket{\psi_{\rm {УКК}}} = e ^ {T-T ^ \dagger}\ket{\psi_{\rm{SCF}}}.
\енд{алигн}

Также часто можно разделить оператор кластера $T = T_1 + T_2 + \кдотс $ на части, где каждая часть $T _j $ содержит $j термины $-Body. В обобщенной теории с кластеризацией один основной оператор кластера (Single) имеет вид \бегин{алигн} T_1 = \sum_{PQ}t ^ {p} _ {q} a ^ \dagger_p a_q, \енд{алигн}

и оператором кластеризации двух основных значений (Double) является форма \бегин{алигн} T_2 = \sum_{PQRS}t ^ {PQ} _ {RS} a ^ \dagger_p a ^ \dagger_q a_r a_s.
\енд{алигн}

Более высокие условия (Triple, четверные и т. д.) возможны, но в настоящее время не поддерживаются библиотекой химия.

Например, пусть $ \ket{\psi_{\rm{SCF}}} = a ^ \dagger_1 a ^ \dagger_2\ket{0}$, а $T = 0,123 a ^ \dagger_0 A_1 + 0,456 а ^ \dagger_0a ^ \dagger_3 A_1 A_2-0,789 a ^ \dagger_3a ^ \dagger_2 A_1 a_0 $. Затем это состояние создается в библиотеке химия следующим образом.
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

Оператор Spin конверватион можно сделать явным, вместо этого укажите `SpinOrbital` индексы вместо целочисленных индексов. Например, пусть $ \ket{\psi_{\rm{SCF}}} = a ^ \dagger_{1, \упарров} a ^ \dagger_{2, \довнарров}\кет{0}$, а $T = 0,123 a ^ \dagger_{0, \упарров} A_ {1, \упарров} + 0,456 а ^ \dagger_{0, \упарров} a ^ \dagger_{3, \довнарров} A_ {1, \упарров} A_ {2, \ Стрелка вниз}-0,789 a ^ \dagger_{3, \упарров} a ^ \dagger_{2, \упарров} A_ {1, \упарров} A_ {0, \упарров} $ быть Spin конвсервинг. Затем это состояние создается в библиотеке химия следующим образом.
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

Мы также предоставляем удобную функцию, которая выполняет перечисление всех операторов кластеризации, аннихилате только занятые обороты и Стимулируйте обучение только на незанятые обороты.
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