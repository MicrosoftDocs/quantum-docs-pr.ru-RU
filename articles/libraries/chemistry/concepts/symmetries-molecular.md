---
title: Симметриес Молекулярноеных интегралов
description: 'Узнайте, как использовать тип Q # Орбиталинтеграл для перечисления молекулярное симметриес.'
author: nathanwiebe2
ms.author: nawiebe
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.symmetries
ms.openlocfilehash: b7e7b79af17af544c4a784eff08500498afc9f67
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/28/2020
ms.locfileid: "77904474"
---
# <a name="symmetries-of-molecular-integrals"></a>Симметриес Молекулярноеных интегралов

Встроенная симметрия Кауломб Хамилтониан (Хамилтониан, заданная в [генераторах тактов для электронных систем](xref:microsoft.quantum.chemistry.concepts.quantummodels)), которая описывает электронную взаимосвязь между собой и с нуклеи, приводит к ряду симметриес, которые можно использовать для сжатия терминов в хамилтониан.
В целом, если никаких дальнейших предположений о функциях базисных функций $ \ psi_j $, мы только \бегин{екуатион} h_ {пкрс} = h_ {КПСР}. \таг{★} \лабел{ЕК: хпкрс} \енд{екуатион}, который можно сразу же увидеть из интегралов в [тактовой модели для электронных систем](xref:microsoft.quantum.chemistry.concepts.quantummodels) , чтобы указать, что их значения остаются идентичными, если $p, q $ и $r, s $ являются взаимозаменяемыми по отношению к anti-коммутатион.

Если предполагается, что обороты по оси являются реальными (так же, как для орбиталных баз), то теперь \бегин{екуатион} h_ {пкрс} = h_ {КПСР} = h_ h_ {СРКП} = h_ {рспк} = H_ {ркпс} = h_ {псрк} СПКР {h_} КРСП: .\таг} \лабел{ЕК уравнение}, учитывая подобные предположения, мы можем использовать приведенный выше симметриес, чтобы уменьшить объем данных, необходимых для хранения элементов матрицы Хамилтониан, с коэффициентом $8 $; Хотя это делает то же самое, что импорт данных немного сложнее.
К счастью, Библиотека моделирования Хамилтониан содержит подпрограммы, которые можно использовать для импорта целочисленных файлов из [ликуи $ | \рангле $](https://www.microsoft.com/en-us/research/project/language-integrated-quantum-operations-liqui/) или непосредственно из [нвчем](http://www.nwchem-sw.org/index.php/Main_Page).

Молекулярное орбиталные интегралы (т. е. $h\_{PQ} $ и $h\_{пкрс} $), такие как, представлены с помощью типа `OrbitalIntegral`, который предоставляет ряд полезных функций для выражения этой симметрии.
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

Помимо перечисления всех Орбитал интегралов, которые являются числовыми, список всех индексов Spin-Орбитал, содержащихся в Хамилтониан, представленных `OrbitalIntegral`, может быть создан следующим образом.
```csharp
    // Create a `OrbitalIntegral` instance to store a two-electron molecular
    // orbital integral data.
    var twoElectronIntegral = new OrbitalIntegral(new[] { 0, 1, 2, 3 }, 0.123);

    // This enumerates all spin-orbital indices of the `FermionTerm`s in the 
    // Hamiltonian represented by this integral -- this is an array of array 
    // of `SpinOrbital` instances.
    var twoElectronSpinOrbitalIndices = twoElectronIntegral.EnumerateSpinOrbitals();
```
## <a name="constructing-fermionic-hamiltonians-from-molecular-integrals"></a>Создание Хамилтонианс Фермионик из целых чисел молекулярное

Вместо создания Фермионик Хамилтониан путем добавления `FermionTerm`s все термины, соответствующие каждому интегралу Орбитал, могут быть добавлены автоматически.
Например, следующий код автоматически перечисляет все перестановки симметриес и упорядочивает эти термины в каноническом порядке: 
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
