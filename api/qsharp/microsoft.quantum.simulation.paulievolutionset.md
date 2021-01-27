---
uid: Microsoft.Quantum.Simulation.PauliEvolutionSet
title: Функция Паулиеволутионсет
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliEvolutionSet
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.
ms.openlocfilehash: 961c95e6787b69e35ca531fa36164cc988ad660d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847963"
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

## <a name="remarks"></a>Remarks

Это достигается частичным применением <xref:microsoft.quantum.simulation.paulievolutionfunction> .