---
uid: Microsoft.Quantum.Research.Chemistry.JWOptimizedFermionEvolutionFunction
title: Функция Жвоптимизедфермионеволутионфунктион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: JWOptimizedFermionEvolutionFunction
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the JWOptimized basis.
ms.openlocfilehash: d70bea8fcb5bd82ddad6dcd2b67c3eb178283bb3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857867"
---
# <a name="jwoptimizedfermionevolutionfunction-function"></a><span data-ttu-id="21645-102">Функция Жвоптимизедфермионеволутионфунктион</span><span class="sxs-lookup"><span data-stu-id="21645-102">JWOptimizedFermionEvolutionFunction function</span></span>

<span data-ttu-id="21645-103">Пространство имен: [Microsoft. тактов. Research. Химия](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="21645-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="21645-104">Пакет: [Microsoft. тактов. Research. Химия](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="21645-104">Package: [Microsoft.Quantum.Research.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span></span>


<span data-ttu-id="21645-105">Представляет динамический генератор как набор моделирующих шлюзов и расширение на основе Жвоптимизед.</span><span class="sxs-lookup"><span data-stu-id="21645-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the JWOptimized basis.</span></span>

```qsharp
function JWOptimizedFermionEvolutionFunction (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex, parityQubit : Qubit) : Microsoft.Quantum.Simulation.EvolutionUnitary
```


## <a name="input"></a><span data-ttu-id="21645-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="21645-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="21645-107">Женераториндекс: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="21645-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="21645-108">Индекс генератора, который должен быть представлен как единое развитие на основе Жвоптимизед.</span><span class="sxs-lookup"><span data-stu-id="21645-108">A generator index to be represented as unitary evolution in the JWOptimized basis.</span></span>


### <a name="parityqubit--qubit"></a><span data-ttu-id="21645-109">Паритикубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="21645-109">parityQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="21645-110">Кубит, определяющий знак времени — развитие.</span><span class="sxs-lookup"><span data-stu-id="21645-110">Qubit that determines the sign of time-evolution.</span></span>



## <a name="output--evolutionunitary"></a><span data-ttu-id="21645-111">Выходные данные: [еволутионунитари](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span><span class="sxs-lookup"><span data-stu-id="21645-111">Output : [EvolutionUnitary](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span></span>

<span data-ttu-id="21645-112">`EvolutionUnitary`Представление, представляющее время развития термина, на который ссылается "женераториндекс.</span><span class="sxs-lookup"><span data-stu-id="21645-112">An `EvolutionUnitary` representing time-evolution by the term referenced in \`generatorIndex.</span></span>