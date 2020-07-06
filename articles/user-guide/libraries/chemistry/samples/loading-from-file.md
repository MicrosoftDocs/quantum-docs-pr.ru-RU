---
title: Загрузка гамильтонова представления из файла
description: Узнайте, как автоматически создать большой Хамилтониан с помощью схемы Брумбридже.
author: guanghaolow
ms.author: gulow
ms.date: 10/23/2018
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.examples.loadhamiltonian
ms.openlocfilehash: 715dbcefc10ecc5af45f2bdd228890f1cb28886b
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275244"
---
# <a name="loading-a-hamiltonian-from-file"></a>Загрузка гамильтонова представления из файла
Ранее мы создали Хамилтонианс, добавив в него отдельные термины. Хотя это и удобно для небольших примеров, тактовая химия в масштабе требует Хамилтонианс с миллионами или миллиардами терминов. Такие Хамилтонианс, созданные пакетами химия, такими как Нвчем, слишком велики для импорта вручную. В этом примере показано, как `FermionHamiltonian` экземпляр может быть автоматически создан из молекулы, представленной [схемой брумбридже](xref:microsoft.quantum.libraries.chemistry.schema.broombridge). Для справки можно проверить предоставленный `LithiumHydrideGUI` образец или `RunSimulation` образец. Ограниченная поддержка также доступна для импорта из формата, используемого [ликуи |>](https://www.microsoft.com/en-us/research/project/language-integrated-quantum-operations-liqui/).

Рассмотрим пример молекулы Нитрожен, которая предоставляется в `IntegralData/YAML` папке репозитория Samples. Метод загрузки `Broombridge` схемы прост.

```csharp
// This is the name of the file we want to load
var filename = @"n2_1_00Re_sto3g.nw.out.yaml";
// This is the directory containing the file
var root = @"IntegralData\YAML";

// This deserializes a Broombridge file, given its filename.
var broombridge = Broombridge.Deserializers.DeserializeBroombridge($@"{root}\{filename}");

// Note that the deserializer returns a list of `ProblemDescription` instances 
// as the file might describe multiple Hamiltonians. In this example, there is 
// only one Hamiltonian. So we use `.First()`, which selects the first element of the list.
var problem = broombridge.ProblemDescriptions.First();

// This extracts the `OrbitalIntegralHamiltonian` from Broombridge format,
// then converts it to a fermion Hamiltonian, then to a Jordan-Wigner
// representation.
var orbitalIntegralHamiltonian = problem.OrbitalIntegralHamiltonian;
var fermionHamiltonian = orbitalIntegralHamiltonian.ToFermionHamiltonian(IndexConvention.UpDown);
var jordanWignerEncoding = fermionHamiltonian.ToPauliHamiltonian(Pauli.QubitEncoding.JordanWigner);
```

Схема Брумбридже также содержит предложения по подготовке первоначального состояния. Метки, например `"|G⟩"` или `"|E1⟩"` , для этих состояний можно просмотреть, изучив файл. Для подготовки этих начальных состояний `qSharpData` алгоритм тактовой задержки (Q #) получается аналогично [предыдущему разделу](xref:microsoft.quantum.chemistry.examples.energyestimate), но с дополнительным параметром, который выбирает нужное начальное состояние. Например,
```csharp
// The desired initial state, assuming that a description of it is present in the
// Broombridge schema.
var state = "|E1>";
var wavefunction = problem.Wavefunctions[state].ToIndexing(IndexConvention.UpDown);

// This creates the qSharpData consumable by the Q# chemistry library algorithms.
var qSharpHamiltonianData = jordanWignerEncoding.ToQSharpFormat();
var qSharpWavefunctionData = wavefunction.ToQSharpFormat();
var qSharpData = QSharpFormat.Convert.ToQSharpFormat(qSharpHamiltonianData, qSharpWavefunctionData);
```

Все описанные выше действия могут быть сокращены с помощью предоставленных удобных методов, как показано ниже.
```csharp
// This is the name of the file we want to load
var filename = "...";

// This deserializes a Broombridge file, given its filename.
var broombridge = Broombridge.Deserializers.DeserializeBroombridge(filename);

// Note that the deserializer returns a list of `ProblemDescription` instances 
// as the file might describe multiple Hamiltonians. In this example, there is 
// only one Hamiltonian. So we use `.Single()`, which selects the only element of the list.
var problem = broombridge.ProblemDescriptions.Single();

// This is a data structure representing the Jordan-Wigner encoding 
// of the Hamiltonian that we may pass to a Q# algorithm.
// If no state is specified, the Hartree-Fock state is used by default.
var qSharpData = problem.ToQSharpFormat("|E1>");
```

Также можно загрузить Хамилтониан из Ликуи | Формат> с использованием очень похожего синтаксиса. 

```csharp
// This is the name of the file we want to load
var filename = @"fe2s2_sto3g.dat"; // This is Ferrodoxin.
// This is the directory containing the file
var root = @"IntegralData\Liquid";

// Deserialize the LiQuiD format.
var problem = LiQuiD.Deserialize($@"{root}\{filename}").First();

// This is a data structure representing the Jordan-Wigner encoding 
// of the Hamiltonian that we may pass to a Q# algorithm.
var qSharpData = problem.ToQSharpFormat();
```

Следуя этому процессу из любого экземпляра Брумбридже или любого промежуточного шага, тактовые алгоритмы, такие как Оценка этапа такта, могут выполняться в указанной статье проблемы с электронной структурой.