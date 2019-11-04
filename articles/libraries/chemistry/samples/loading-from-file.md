---
title: Загрузка Хамилтониан из файла | Документация Майкрософт
description: Загрузка Хамилтониан из файловых документов
author: guanghaolow
ms.author: gulow
ms.date: 10/23/2018
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.examples.loadhamiltonian
ms.openlocfilehash: 9902e95b09d38323b4b91c29ab897a4f0124b6cd
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/26/2019
ms.locfileid: "73184191"
---
## <a name="loading-a-hamiltonian-from-file"></a>Загрузка Хамилтониан из файла
Ранее мы создали Хамилтонианс, добавив в него отдельные термины. Хотя это и удобно для небольших примеров, тактовая химия в масштабе требует Хамилтонианс с миллионами или миллиардами терминов. Такие Хамилтонианс, созданные пакетами химия, такими как Нвчем, слишком велики для импорта вручную. В этом примере показано, как экземпляр `FermionHamiltonian` может быть автоматически создан из молекулы, представленной [схемой брумбридже](xref:microsoft.quantum.libraries.chemistry.schema.broombridge). Для справки можно проверить предоставленный образец `LithiumHydrideGUI` или образец `RunSimulation`. Ограниченная поддержка также доступна для импорта из формата, используемого [ликуи | >](https://www.microsoft.com/en-us/research/project/language-integrated-quantum-operations-liqui/).

Рассмотрим пример молекулы Нитрожен, которая предоставляется в папке `IntegralData/YAML` репозитория Samples. Метод загрузки схемы `Broombridge` прост.

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

Схема Брумбридже также содержит предложения по подготовке первоначального состояния. Метки, например `"|G⟩"` или `"|E1⟩"`, для этих состояний можно просмотреть, изучив файл. Чтобы подготовить эти начальные состояния, `qSharpData`, потребляемые алгоритмами тактовой задержки Q, получаются аналогично [предыдущему разделу](xref:microsoft.quantum.chemistry.examples.energyestimate), но с дополнительным параметром, который выбирает нужное начальное состояние. Например,
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

Также можно загрузить Хамилтониан из формата Ликуи | >, используя очень похожий синтаксис. 

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