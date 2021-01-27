---
uid: Microsoft.Quantum.Research.Chemistry.JordanWignerOptimizedFermionEvolutionSet
title: Функция Жорданвигнероптимизедфермионеволутионсет
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: JordanWignerOptimizedFermionEvolutionSet
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.
ms.openlocfilehash: 941d66a936ef1a2ac76230d14ca8437ac2a4a049
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857885"
---
# <a name="jordanwigneroptimizedfermionevolutionset-function"></a><span data-ttu-id="e0b34-102">Функция Жорданвигнероптимизедфермионеволутионсет</span><span class="sxs-lookup"><span data-stu-id="e0b34-102">JordanWignerOptimizedFermionEvolutionSet function</span></span>

<span data-ttu-id="e0b34-103">Пространство имен: [Microsoft. тактов. Research. Химия](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="e0b34-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="e0b34-104">Пакет: [Microsoft. тактов. Research. Химия](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="e0b34-104">Package: [Microsoft.Quantum.Research.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span></span>


<span data-ttu-id="e0b34-105">Представляет динамический генератор как набор моделирующих шлюзов и расширение на основе Паули.</span><span class="sxs-lookup"><span data-stu-id="e0b34-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.</span></span>

```qsharp
function JordanWignerOptimizedFermionEvolutionSet (parityQubit : Qubit) : Microsoft.Quantum.Simulation.EvolutionSet
```


## <a name="input"></a><span data-ttu-id="e0b34-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e0b34-106">Input</span></span>

### <a name="parityqubit--qubit"></a><span data-ttu-id="e0b34-107">Паритикубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="e0b34-107">parityQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="e0b34-108">Кубит, определяющий знак времени — развитие.</span><span class="sxs-lookup"><span data-stu-id="e0b34-108">Qubit that determines the sign of time-evolution.</span></span>



## <a name="output--evolutionset"></a><span data-ttu-id="e0b34-109">Выходные данные: [эволюционный](xref:Microsoft.Quantum.Simulation.EvolutionSet)</span><span class="sxs-lookup"><span data-stu-id="e0b34-109">Output : [EvolutionSet](xref:Microsoft.Quantum.Simulation.EvolutionSet)</span></span>

<span data-ttu-id="e0b34-110">Объект `EvolutionSet` , который сопоставляет объект `GeneratorIndex` для жвоптимизед на уровне еволутионунитари.</span><span class="sxs-lookup"><span data-stu-id="e0b34-110">An `EvolutionSet` that maps a `GeneratorIndex` for the JWOptimized basis to an \`EvolutionUnitary.</span></span>