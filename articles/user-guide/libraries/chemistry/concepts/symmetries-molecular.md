---
title: Симметриес Молекулярноеных интегралов
description: Сведения об использовании Q# типа орбиталинтеграл для перечисления молекулярное симметриес.
author: bradben
ms.author: v-benbra
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.symmetries
no-loc:
- Q#
- $$v
ms.openlocfilehash: 9ebb8e9bda06967d3cfa002a7d074933d9135ada
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/21/2020
ms.locfileid: "90833819"
---
# <a name="symmetries-of-molecular-integrals"></a><span data-ttu-id="9e8af-103">Симметриес Молекулярноеных интегралов</span><span class="sxs-lookup"><span data-stu-id="9e8af-103">Symmetries of Molecular Integrals</span></span>

<span data-ttu-id="9e8af-104">Встроенная симметрия Кауломб Хамилтониан (Хамилтониан, заданная в [генераторах тактов для электронных систем](xref:microsoft.quantum.chemistry.concepts.quantummodels)), которая описывает электронную взаимосвязь между собой и с нуклеи, приводит к ряду симметриес, которые можно использовать для сжатия терминов в хамилтониан.</span><span class="sxs-lookup"><span data-stu-id="9e8af-104">The inherent symmetry of the Coulomb Hamiltonian, which is the Hamiltonian given in [Quantum Models for Electronic Systems](xref:microsoft.quantum.chemistry.concepts.quantummodels), that describes electrons interacting electrically with each other and with the nuclei, leads to a number of symmetries that can be exploited to compress the terms in the Hamiltonian.</span></span>
<span data-ttu-id="9e8af-105">В целом, если никаких дальнейших предположений о функциях базисных функций $ \ psi_j $, мы только \бегин{екуатион} h_ {пкрс} = h_ {КПСР}. \таг{★} \лабел{ЕК: хпкрс} \енд{екуатион}, который можно сразу же увидеть из интегралов в [тактовой модели для электронных систем](xref:microsoft.quantum.chemistry.concepts.quantummodels) , чтобы указать, что их значения остаются идентичными, если $p, q $ и $r, s $ являются взаимозаменяемыми по отношению к anti-коммутатион.</span><span class="sxs-lookup"><span data-stu-id="9e8af-105">In general if no further assumptions are made about the basis functions $\psi_j$ then we only have that \begin{equation} h_{pqrs}= h_{qpsr},\tag{★}\label{eq:hpqrs} \end{equation} which can be immediately seen from the integrals in [Quantum Models for Electronic Systems](xref:microsoft.quantum.chemistry.concepts.quantummodels) upon noting that their values remain identical if $p,q$ and $r,s$ are interchanged from anti-commutation.</span></span>

<span data-ttu-id="9e8af-106">Если предполагается, что прокрутка с оборотами полагаться на реальные значения (так же, как и для орбиталных баз), то теперь \бегин{екуатион} h_ {пкрс} = h_ {КПСР} = h_ h_ {СРКП} = h_ {рспк} = H_ {ркпс} = h_ {псрк} СПКР {h_} КРСП: хпкрсреал} \end{Equation}, учитывая подобные предположения, мы можем использовать приведенный выше symmetries, чтобы уменьшить объем данных, необходимых для хранения элементов матрицы Hamiltonian, с коэффициентом $8 $; Хотя это делает то же самое, что импорт данных немного сложнее.</span><span class="sxs-lookup"><span data-stu-id="9e8af-106">If we assume that the spin-orbitals are real-valued (as they are for Gaussian orbital bases) then we further have that \begin{equation} h_{pqrs} = h_{qpsr} = h_{srqp} = h_{rspq}=h_{rqps}=h_{psrq}=h_{spqr}=h_{qrsp}.\tag{★}\label{eq:hpqrsreal} \end{equation} Given such assumptions hold, we can use the above symmetries to reduce the data needed to store the matrix elements of the Hamiltonian by a factor of $8$; although doing so makes importing data in a consistent way slightly more challenging.</span></span>
<span data-ttu-id="9e8af-107">К счастью, Библиотека моделирования Хамилтониан содержит подпрограммы, которые можно использовать для импорта целочисленных файлов из [ликуи $ | \рангле $](https://www.microsoft.com/en-us/research/project/language-integrated-quantum-operations-liqui/) или непосредственно из [нвчем](http://www.nwchem-sw.org/index.php/Main_Page).</span><span class="sxs-lookup"><span data-stu-id="9e8af-107">Fortunately the Hamiltonian simulation library has subroutines that can be used to import integral files from either [LIQUI$|\rangle$](https://www.microsoft.com/en-us/research/project/language-integrated-quantum-operations-liqui/) or directly from [NWChem](http://www.nwchem-sw.org/index.php/Main_Page).</span></span>

<span data-ttu-id="9e8af-108">Молекулярное орбиталные интегралы (т. е. $h \_ {PQ} $ и $h \_ {пкрс} $), такие как, представлены с помощью `OrbitalIntegral` типа, который предоставляет ряд полезных функций для выражения этой симметрии.</span><span class="sxs-lookup"><span data-stu-id="9e8af-108">Molecular orbital integrals (i.e. the $h\_{pq}$ and $h\_{pqrs}$ terms) such as these are represented using the `OrbitalIntegral` type, which provides a number of helpful functions to express this symmetry.</span></span>
```csharp
    // Load the namespace containing orbital integral objects.
    using Microsoft.Quantum.Chemistry.OrbitalIntegrals;

    // Create a `OrbitalIntegral` instance to store a one-electron molecular 
    // orbital integral data.
    var oneElectronOrbitalIndices = new[] { 0, 1 };
    var oneElectronCoefficient = 1.0;
    var oneElectronIntegral = new OrbitalIntegral(oneElectronOrbitalIndices, oneElectronCoefficient);

    // This enumerates all one-electron integrals with the same coefficient --
    // an array of equivalent `OrbitalIntegral` instances is generated. In this
    // case, there are two elements.
    var oneElectronIntegrals = oneElectronIntegral.EnumerateOrbitalSymmetries();

    // Create a `OrbitalIntegral` instance to store a two-electron molecular orbital integral data.
    var twoElectronOrbitalIndices = new[] { 0, 1, 2, 3 };
    var twoElectronCoefficient = 0.123;
    var twoElectronIntegral = new OrbitalIntegral(twoElectronOrbitalIndices, twoElectronCoefficient);

    // This enumerates all two-electron integrals with the same coefficient -- 
    // an array of equivalent `OrbitalIntegral` instances is generated. In 
    // this case, there are 8 elements.
    var twoElectronIntegrals = twoElectronIntegral.EnumerateOrbitalSymmetries();
```

<span data-ttu-id="9e8af-109">В дополнение к перечислению всех Орбитал интегралов, которые являются числово идентичными, список всех индексов Spin-Орбитал, содержащихся в Хамилтониан, представленных в, `OrbitalIntegral` может быть сформирован следующим образом.</span><span class="sxs-lookup"><span data-stu-id="9e8af-109">In addition to enumerating over all orbital integrals that are numerically identical, a list of all spin-orbital indices contained in the Hamiltonian represented by an `OrbitalIntegral` may be generated as follows.</span></span>
```csharp
    // Create a `OrbitalIntegral` instance to store a two-electron molecular
    // orbital integral data.
    var twoElectronIntegral = new OrbitalIntegral(new[] { 0, 1, 2, 3 }, 0.123);

    // This enumerates all spin-orbital indices of the `FermionTerm`s in the 
    // Hamiltonian represented by this integral -- this is an array of array 
    // of `SpinOrbital` instances.
    var twoElectronSpinOrbitalIndices = twoElectronIntegral.EnumerateSpinOrbitals();
```
## <a name="constructing-fermionic-hamiltonians-from-molecular-integrals"></a><span data-ttu-id="9e8af-110">Создание Хамилтонианс Фермионик из целых чисел молекулярное</span><span class="sxs-lookup"><span data-stu-id="9e8af-110">Constructing Fermionic Hamiltonians from Molecular Integrals</span></span>

<span data-ttu-id="9e8af-111">Вместо создания Хамилтониан Фермионик путем добавления `FermionTerm` s все термины, соответствующие каждому интегралу Орбитал, можно добавить автоматически.</span><span class="sxs-lookup"><span data-stu-id="9e8af-111">Rather than constructing a Fermionic Hamiltonian by adding `FermionTerm`s, all terms corresponding to each orbital integral may be added automatically.</span></span>
<span data-ttu-id="9e8af-112">Например, следующий код автоматически перечисляет все перестановки симметриес и упорядочивает эти термины в каноническом порядке:</span><span class="sxs-lookup"><span data-stu-id="9e8af-112">For example, the following code automatically enumerates over all permutational symmetries and orders the terms in canonical order:</span></span> 
```csharp
    // Load the namespace containing fermion objects. This
    // example also uses LINQ queries.
    using Microsoft.Quantum.Chemistry.Fermion;
    using System.Linq;

    // Create a `OrbitalIntegral` instance to store a two-electron molecular 
    // orbital integral data.
    var orbitalIntegral = new OrbitalIntegral(new[] { 0, 1, 2, 3 }, 0.123);

    // Create an `OrbitalIntegralHamiltonian` instance to store the orbital integral
    // terms
    var orbitalIntegralHamiltonian = new OrbitalIntegralHamiltonian();
    orbitalIntegralHamiltonian.Add(orbitalIntegral);

    // Convert the orbital integral representation to a fermion
    // representation. This also requires choosing a convention for 
    // mapping spin orbital indices to integer indices.
    var fermionHamiltonian = orbitalIntegralHamiltonian.ToFermionHamiltonian(IndexConvention.UpDown);

    // Alternatively, one can add orbital integrals directly to a fermion Hamiltonian
    // as follows. This automatically enumerates over all symmetries, and then
    // orders the `HermitianFermionTerm` instances in canonical order. We will need to
    // choose an indexing convention as well.
    fermionHamiltonian.AddRange(orbitalIntegral
        .ToHermitianFermionTerms(0, IndexConvention.UpDown)
        .Select(o => (o.Item1, o.Item2.ToDoubleCoeff())));
```
