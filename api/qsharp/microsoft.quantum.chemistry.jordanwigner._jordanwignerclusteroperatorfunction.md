---
uid: Microsoft.Quantum.Chemistry.JordanWigner._JordanWignerClusterOperatorFunction
title: Функция _JordanWignerClusterOperatorFunction
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _JordanWignerClusterOperatorFunction
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the JordanWigner basis.
ms.openlocfilehash: 023ac4a6aaee8e3d0514a471c33c575b86004b15
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203830"
---
# <a name="_jordanwignerclusteroperatorfunction-function"></a><span data-ttu-id="3f5de-102">Функция _JordanWignerClusterOperatorFunction</span><span class="sxs-lookup"><span data-stu-id="3f5de-102">_JordanWignerClusterOperatorFunction function</span></span>

<span data-ttu-id="3f5de-103">Пространство имен: [Microsoft. тактов. химия. жорданвигнер](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="3f5de-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="3f5de-104">Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="3f5de-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="3f5de-105">Представляет динамический генератор как набор моделирующих шлюзов и расширение на основе Жорданвигнер.</span><span class="sxs-lookup"><span data-stu-id="3f5de-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the JordanWigner basis.</span></span>

```qsharp
function _JordanWignerClusterOperatorFunction (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.EvolutionUnitary
```


## <a name="input"></a><span data-ttu-id="3f5de-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="3f5de-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="3f5de-107">Женераториндекс: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="3f5de-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="3f5de-108">Индекс генератора, который должен быть представлен как единое развитие в Жорданвигнер.</span><span class="sxs-lookup"><span data-stu-id="3f5de-108">A generator index to be represented as unitary evolution in the JordanWigner.</span></span>



## <a name="output--evolutionunitary"></a><span data-ttu-id="3f5de-109">Выходные данные: [еволутионунитари](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span><span class="sxs-lookup"><span data-stu-id="3f5de-109">Output : [EvolutionUnitary](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span></span>

<span data-ttu-id="3f5de-110">`EvolutionUnitary`Представление, представляющее время развития термина, на который ссылается "женераториндекс.</span><span class="sxs-lookup"><span data-stu-id="3f5de-110">An `EvolutionUnitary` representing time-evolution by the term referenced in \`generatorIndex.</span></span>