---
uid: Microsoft.Quantum.Simulation.PauliEvolutionSet
title: Функция Паулиеволутионсет
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliEvolutionSet
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.
ms.openlocfilehash: fb53b90b6ab5ce1003f66b68a8c2ad8b3631f627
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230352"
---
# <a name="paulievolutionset-function"></a>Функция Паулиеволутионсет

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Представляет динамический генератор как набор моделирующих шлюзов и расширение на основе Паули.

```qsharp
function PauliEvolutionSet () : Microsoft.Quantum.Simulation.EvolutionSet
```


## <a name="output--evolutionset"></a>Выходные данные: [эволюционный](xref:Microsoft.Quantum.Simulation.EvolutionSet)

Объект `EvolutionSet` , который сопоставляет объект `GeneratorIndex` для Паули на уровне еволутионунитари.

## <a name="remarks"></a>Комментарии

Это достигается частичным применением <xref:microsoft.quantum.simulation.paulievolutionfunction> .