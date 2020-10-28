---
uid: Microsoft.Quantum.Research.Chemistry.JordanWignerOptimizedFermionEvolutionSet
title: Функция Жорданвигнероптимизедфермионеволутионсет
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: JordanWignerOptimizedFermionEvolutionSet
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.
ms.openlocfilehash: d2d916655b7538b39d5739d67dbb3fc9920cf67a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732153"
---
# <a name="jordanwigneroptimizedfermionevolutionset-function"></a>Функция Жорданвигнероптимизедфермионеволутионсет

Пространство имен: [Microsoft. тактов. Research. Химия](xref:Microsoft.Quantum.Research.Chemistry)

Пакеты [](https://nuget.org/packages/)


Представляет динамический генератор как набор моделирующих шлюзов и расширение на основе Паули.

```qsharp
function JordanWignerOptimizedFermionEvolutionSet (parityQubit : Qubit) : Microsoft.Quantum.Simulation.EvolutionSet
```


## <a name="input"></a>Входные данные

### <a name="parityqubit--qubit"></a>Паритикубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Кубит, определяющий знак времени — развитие.



## <a name="output--evolutionset"></a>Выходные данные: [эволюционный](xref:Microsoft.Quantum.Simulation.EvolutionSet)

Объект `EvolutionSet` , который сопоставляет объект `GeneratorIndex` для жвоптимизед на уровне еволутионунитари.