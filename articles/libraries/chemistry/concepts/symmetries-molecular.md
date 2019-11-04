---
title: Симметриес Молекулярноеных интегралов | Документация Майкрософт
description: Симметриес молекулярное, концептуальные документы
author: nathanwiebe2
ms.author: nawiebe
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.symmetries
ms.openlocfilehash: 041d600bc8d65e7d67f5fe7d61a69426fb42ffbc
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2019
ms.locfileid: "73442396"
---
# <a name="symmetries-of-molecular-integrals"></a>Симметриес Молекулярноеных интегралов

Встроенная симметрия Кауломб Хамилтониан, которая является Хамилтониан, заданной в [генераторах тактов для электронных систем](xref:microsoft.quantum.chemistry.concepts.quantummodels), которые описывают электроны, взаимодействующие друг с другом и с нуклеи, приводит к ряду симметриес, которые могут быть использовать для сжатия терминов в Хамилтониан.
В целом, если никаких дальнейших предположений относительно основных функций $ \psi_j $ не предполагалось, то только \бегин{екуатион} H_ {пкрс} = H_ {КПСР}, \таг{★} \лабел{ЕК: хпкрс} \енд{екуатион}, которые можно сразу увидеть из интегралов в [тактовой модели для В электронных системах](xref:microsoft.quantum.chemistry.concepts.quantummodels) с учетом того, что их значения остаются идентичными, если $p, q $ и $r, s $ взаимозаменяемы от Anti-коммутатион.

Если предполагается, что обороты по оси являются реальными (так же, как для орбиталных баз), то теперь \бегин{екуатион} H_ {пкрс} = H_ {КПСР} = H_ {СРКП} = H_ {рспк} = H_ {ркпс} = H_ {псрк} H_ {★} СПКР: H_} КРСП уравнение}, учитывая подобные предположения, мы можем использовать приведенный выше симметриес, чтобы уменьшить объем данных, необходимых для хранения элементов матрицы Хамилтониан, с коэффициентом $8 $; Хотя это делает то же самое, что импорт данных немного сложнее.
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
