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
# <a name="jordanwigneroptimizedfermionevolutionset-function"></a><span data-ttu-id="c7dc1-102">Функция Жорданвигнероптимизедфермионеволутионсет</span><span class="sxs-lookup"><span data-stu-id="c7dc1-102">JordanWignerOptimizedFermionEvolutionSet function</span></span>

<span data-ttu-id="c7dc1-103">Пространство имен: [Microsoft. тактов. Research. Химия](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="c7dc1-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="c7dc1-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c7dc1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c7dc1-105">Представляет динамический генератор как набор моделирующих шлюзов и расширение на основе Паули.</span><span class="sxs-lookup"><span data-stu-id="c7dc1-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.</span></span>

```qsharp
function JordanWignerOptimizedFermionEvolutionSet (parityQubit : Qubit) : Microsoft.Quantum.Simulation.EvolutionSet
```


## <a name="input"></a><span data-ttu-id="c7dc1-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c7dc1-106">Input</span></span>

### <a name="parityqubit--qubit"></a><span data-ttu-id="c7dc1-107">Паритикубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="c7dc1-107">parityQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="c7dc1-108">Кубит, определяющий знак времени — развитие.</span><span class="sxs-lookup"><span data-stu-id="c7dc1-108">Qubit that determines the sign of time-evolution.</span></span>



## <a name="output--evolutionset"></a><span data-ttu-id="c7dc1-109">Выходные данные: [эволюционный](xref:Microsoft.Quantum.Simulation.EvolutionSet)</span><span class="sxs-lookup"><span data-stu-id="c7dc1-109">Output : [EvolutionSet](xref:Microsoft.Quantum.Simulation.EvolutionSet)</span></span>

<span data-ttu-id="c7dc1-110">Объект `EvolutionSet` , который сопоставляет объект `GeneratorIndex` для жвоптимизед на уровне еволутионунитари.</span><span class="sxs-lookup"><span data-stu-id="c7dc1-110">An `EvolutionSet` that maps a `GeneratorIndex` for the JWOptimized basis to an \`EvolutionUnitary.</span></span>