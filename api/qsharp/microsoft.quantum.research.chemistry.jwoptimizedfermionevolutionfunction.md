---
uid: Microsoft.Quantum.Research.Chemistry.JWOptimizedFermionEvolutionFunction
title: Функция Жвоптимизедфермионеволутионфунктион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: JWOptimizedFermionEvolutionFunction
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the JWOptimized basis.
ms.openlocfilehash: 952f3dc4ab0595ace0ee34c040cb21969afa111f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710805"
---
# <a name="jwoptimizedfermionevolutionfunction-function"></a><span data-ttu-id="a4bae-102">Функция Жвоптимизедфермионеволутионфунктион</span><span class="sxs-lookup"><span data-stu-id="a4bae-102">JWOptimizedFermionEvolutionFunction function</span></span>

<span data-ttu-id="a4bae-103">Пространство имен: [Microsoft. тактов. Research. Химия](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="a4bae-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="a4bae-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a4bae-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a4bae-105">Представляет динамический генератор как набор моделирующих шлюзов и расширение на основе Жвоптимизед.</span><span class="sxs-lookup"><span data-stu-id="a4bae-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the JWOptimized basis.</span></span>

```qsharp
function JWOptimizedFermionEvolutionFunction (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex, parityQubit : Qubit) : Microsoft.Quantum.Simulation.EvolutionUnitary
```


## <a name="input"></a><span data-ttu-id="a4bae-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a4bae-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="a4bae-107">Женераториндекс: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="a4bae-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="a4bae-108">Индекс генератора, который должен быть представлен как единое развитие на основе Жвоптимизед.</span><span class="sxs-lookup"><span data-stu-id="a4bae-108">A generator index to be represented as unitary evolution in the JWOptimized basis.</span></span>


### <a name="parityqubit--qubit"></a><span data-ttu-id="a4bae-109">Паритикубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="a4bae-109">parityQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="a4bae-110">Кубит, определяющий знак времени — развитие.</span><span class="sxs-lookup"><span data-stu-id="a4bae-110">Qubit that determines the sign of time-evolution.</span></span>



## <a name="output--evolutionunitary"></a><span data-ttu-id="a4bae-111">Выходные данные: [еволутионунитари](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span><span class="sxs-lookup"><span data-stu-id="a4bae-111">Output : [EvolutionUnitary](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span></span>

<span data-ttu-id="a4bae-112">`EvolutionUnitary`Представление, представляющее время развития термина, на который ссылается "женераториндекс.</span><span class="sxs-lookup"><span data-stu-id="a4bae-112">An `EvolutionUnitary` representing time-evolution by the term referenced in \`generatorIndex.</span></span>