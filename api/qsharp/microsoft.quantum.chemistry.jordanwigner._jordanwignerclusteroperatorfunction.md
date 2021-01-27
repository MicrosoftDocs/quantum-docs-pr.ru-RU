---
uid: Microsoft.Quantum.Chemistry.JordanWigner._JordanWignerClusterOperatorFunction
title: Функция _JordanWignerClusterOperatorFunction
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _JordanWignerClusterOperatorFunction
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the JordanWigner basis.
ms.openlocfilehash: 71aa0256b4d2911fe9d8e3ca091735d6375ed23e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839490"
---
# <a name="_jordanwignerclusteroperatorfunction-function"></a><span data-ttu-id="ab14b-102">Функция _JordanWignerClusterOperatorFunction</span><span class="sxs-lookup"><span data-stu-id="ab14b-102">_JordanWignerClusterOperatorFunction function</span></span>

<span data-ttu-id="ab14b-103">Пространство имен: [Microsoft. тактов. химия. жорданвигнер](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="ab14b-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="ab14b-104">Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="ab14b-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="ab14b-105">Представляет динамический генератор как набор моделирующих шлюзов и расширение на основе Жорданвигнер.</span><span class="sxs-lookup"><span data-stu-id="ab14b-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the JordanWigner basis.</span></span>

```qsharp
function _JordanWignerClusterOperatorFunction (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.EvolutionUnitary
```


## <a name="input"></a><span data-ttu-id="ab14b-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ab14b-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="ab14b-107">Женераториндекс: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="ab14b-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="ab14b-108">Индекс генератора, который должен быть представлен как единое развитие в Жорданвигнер.</span><span class="sxs-lookup"><span data-stu-id="ab14b-108">A generator index to be represented as unitary evolution in the JordanWigner.</span></span>



## <a name="output--evolutionunitary"></a><span data-ttu-id="ab14b-109">Выходные данные: [еволутионунитари](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span><span class="sxs-lookup"><span data-stu-id="ab14b-109">Output : [EvolutionUnitary](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span></span>

<span data-ttu-id="ab14b-110">`EvolutionUnitary`Представление, представляющее время развития термина, на который ссылается "женераториндекс.</span><span class="sxs-lookup"><span data-stu-id="ab14b-110">An `EvolutionUnitary` representing time-evolution by the term referenced in \`generatorIndex.</span></span>