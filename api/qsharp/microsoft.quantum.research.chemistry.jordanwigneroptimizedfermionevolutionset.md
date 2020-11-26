---
uid: Microsoft.Quantum.Research.Chemistry.JordanWignerOptimizedFermionEvolutionSet
title: Функция Жорданвигнероптимизедфермионеволутионсет
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: JordanWignerOptimizedFermionEvolutionSet
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.
ms.openlocfilehash: 2cd555882792c29cb2ed71972739505df11fbabc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225743"
---
# <a name="jordanwigneroptimizedfermionevolutionset-function"></a>Функция Жорданвигнероптимизедфермионеволутионсет

Пространство имен: [Microsoft. тактов. Research. Химия](xref:Microsoft.Quantum.Research.Chemistry)

Пакет: [Microsoft. тактов. Research. Химия](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)


Представляет динамический генератор как набор моделирующих шлюзов и расширение на основе Паули.

```qsharp
function JordanWignerOptimizedFermionEvolutionSet (parityQubit : Qubit) : Microsoft.Quantum.Simulation.EvolutionSet
```


## <a name="input"></a>Входные данные

### <a name="parityqubit--qubit"></a>Паритикубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Кубит, определяющий знак времени — развитие.



## <a name="output--evolutionset"></a>Выходные данные: [эволюционный](xref:Microsoft.Quantum.Simulation.EvolutionSet)

Объект `EvolutionSet` , который сопоставляет объект `GeneratorIndex` для жвоптимизед на уровне еволутионунитари.